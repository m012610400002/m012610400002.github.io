---
layout: post
title: "Examen Final — APT41"
date: 2026-08-15 10:00:00 -0500
categories: [Examen, Threat Intelligence]
tags: [examen-final]
published: true
---

El siguiente informe documenta el desarrollo del examen final, estructurado en cuatro actos: desde la caracterización en CTI del grupo **APT41 (G0096)** en OpenCTI, la planificación e implementación de la kill chain sobre **Metasploitable3**, hasta la estrategia de detección y mitigación defensiva.

---

## Acto 1 — La Inteligencia Dirige (Perfil de APT41 en OpenCTI)

### 1.1 Caracterización del Perfil (Intrusion Set)
* **Nombre:** APT41 (Alias: BARIUM, Double Dragon, Wicked Panda, Winnti Group).
* **Motivación:** Mixta (Espionaje patrocinado por el estado chino y operaciones con fines de lucro financiero).
* **Vértice Diamante:** *Adversario* (Adversary).
* **Nivel de CTI:** *Estratégico* (Dirigido a decisiones de alto nivel, entendimiento del perfil de amenaza, atribuibilidad y motivaciones).

### 1.2 TTPs Clave (Attack Patterns)
1. **[T1195.002] Compromise Software Supply Chain:** Vulneración de proveedores de software para infectar mediante actualizaciones legítimas. *(Vértice: Capacidad / Nivel CTI: Táctico)*
2. **[T1021.002] SMB/Windows Admin Shares:** Movimiento lateral abusando de recursos compartidos de red (`ADMIN$`, `C$`). *(Vértice: Capacidad e Infraestructura / Nivel CTI: Táctico)*
3. **[T1059.001] PowerShell:** Ejecución de código y comandos en memoria para evitar dejar rastros en disco. *(Vértice: Capacidad / Nivel CTI: Táctico)*
4. **[T1543.003] Windows Service:** Persistencia y escalada de privilegios mediante la creación o modificación de servicios de Windows. *(Vértice: Capacidad / Nivel CTI: Táctico)*
5. **[T1014] Rootkit:** Ocultamiento de procesos maliciosos en el kernel del sistema. *(Vértice: Capacidad / Nivel CTI: Táctico)*
6. **[T1078] Valid Accounts:** Autenticación legítima mediante credenciales previamente comprometidas. *(Vértice: Infraestructura / Nivel CTI: Táctico)*
7. **[T1553.002] Code Signing:** Uso de certificados digitales robados para eludir controles de seguridad del sistema operativo. *(Vértice: Capacidad / Nivel CTI: Operacional)*

### 1.3 Indicadores de Compromiso (IoCs)
* **Hashes (SHA-256):** Muestras asociadas a PlugX y gh0st RAT.
* **Infraestructura C2:** Direcciones IP y dominios utilizados para la exfiltración de datos.
* **Vértice Diamante:** *Infraestructura* (Infrastructure) y *Capacidad* (Capability).
* **Nivel de CTI:** *Táctico* (Artefactos técnicos para reglas de detección en SIEM/EDR).

### 1.4 Malware y Herramientas
* **Malware:** PlugX, gh0st RAT, ASPXSpy, BrowserGhost.
* **Herramientas:** Impacket, PsExec, BITSAdmin, Mimikatz.
* **Vértice Diamante:** *Capacidad* (Capability).
* **Nivel de CTI:** *Operacional* (Conocimiento de las utilidades que despliega la amenaza en sus operaciones).

### 1.5 Análisis Teórico y Justificación de CTI

| Dato Analizado | Nivel de CTI | Vértice Modelo Diamante | Justificación |
| :--- | :--- | :--- | :--- |
| **Atribución y Motivación de APT41** | Estratégico | Adversario | Apoya la toma de decisiones ejecutivas y evaluación del riesgo global. |
| **Herramientas (Impacket, PlugX)** | Operacional | Capacidad | Define los artefactos y softwares específicos que el atacante sabe operar. |
| **Patrones TTP (SMB, PowerShell)** | Táctico | Capacidad / Infraestructura | Explica la mecánica exacta de cómo el atacante ejecuta la acción técnica. |
| **Hashes e IPs de C2** | Táctico | Infraestructura | Datos volátiles consumibles directamente por reglas defensivas (YARA/IOCs). |

> **Manejo de TLP si la etiqueta es NONE:**
> Si un IoC en OpenCTI o en un feed de inteligencia se registra con `TLP:NONE` (o sin etiqueta TLP previa), el **Analista de CTI** o la dirección del **SOC/CISO** de la organización receptora debe ser quien fije la política de clasificación. Esto se debe a que la organización que consume el dato debe determinar la sensibilidad de la fuente, el riesgo de exposición pública de sus propios activos al compartir la amenaza, y estandarizar la información por defecto bajo una clasificación prudente (frecuentemente `TLP:AMBER` internamente o `TLP:CLEAR` si el IoC es de dominio público comprobado).

---

## Acto 2 — Plan de Ataque Mapeado a ATT&CK

### 2.1 Mapeo de la Superficie de Metasploitable3

| Táctica | Técnica ATT&CK | Servicio / Objetivo en Metasploitable3 | Herramienta Usada |
| :--- | :--- | :--- | :--- |
| **Reconocimiento** | [T1018] Remote System Discovery | Puerto 445 (SMB), Puerto 21 (FTP), Mapeo de Subred | Nmap / `ping` |
| **Acceso Inicial** | [T1021.002] SMB/Windows Admin Shares | Servicio SMB / Credenciales de Administrador por defecto | Impacket (`psexec.py`) / Metasploit |
| **Ejecución** | [T1059.001] PowerShell | Intérprete PowerShell en la máquina de destino | PowerShell / Meterpreter |
| **Escalada de Privilegios** | [T1543.003] Windows Service | Windows Service Control Manager (SCM) | `sc.exe` / Meterpreter `getsystem` |
| **Persistencia / C2** | [T1078] Valid Accounts | Sistema de Autenticación Local (SAM) | Mimikatz (`hashdump`) |

### 2.2 Descarte Explícito de TTPs No Reproducibles

* **[T1195.002] Compromise Software Supply Chain:** **Descartado.** Requiere el compromiso de proveedores externos de desarrollo de software, lo cual no aplica en un laboratorio de red local aislado con una máquina virtual fija.
* **[T1596.005] Scan Databases (FOFA/Shodan):** **Descartado.** Metasploitable3 se despliega en una interfaz de red NAT/Host-Only privada sin dirección IP pública indexable por motores de búsqueda de IoT.
* **[T1553.002] Code Signing:** **Descartado.** El entorno de Metasploitable3 no tiene políticas estrictas de restricción de firmas digitales (AppLocker/WDAC) activas que requieran la falsificación o robo de certificados para ejecutar código.
* **[T1595.003] Wordlist Scanning / Phishing:** **Descartado.** No existe un usuario humano interactivo ni servidores de correo configurados para vectores de ingeniería social en la máquina objetivo.

---

## Acto 3 — Ejecución de la Kill Chain

A continuación se detalla el análisis cronológico y ejecución del ataque sobre Metasploitable3, ordenado por fases de la kill chain.

<div class="tutorial-steps">
{%- comment -%}
Estructura de datos (separada por '|'):
Posición 0: Número de paso
Posición 1: Título legible del paso
Posición 2: Nombre exacto de la imagen en /assets/img/
Posición 3: Fecha (DD/MM/YYYY)
Posición 4: Fase ATT&CK / Táctica
Posición 5: Descripción detallada del procedimiento técnico
{%- endcomment -%}
{%- capture datos_pasos -%}
1|Reconocimiento de Red|apt41_recon.png|15/08/2026|Reconocimiento [T1018]|Escaneo de puertos e identificación del servicio SMB en la IP de Metasploitable3.
2|Acceso Inicial por SMB|apt41_initial_access.png|15/08/2026|Acceso Inicial [T1021.002]|Explotación del servicio SMB utilizando psexec.py para obtener una consola remota.
3|Ejecución en PowerShell|apt41_execution_powershell.png|15/08/2026|Ejecución [T1059.001]|Ejecución de payload interactivo en PowerShell evitando la escritura en disco.
4|Escalada de Privilegios|apt41_priv_esc.png|15/08/2026|Escalada de Privilegios [T1543.003]|Creación de un servicio malicioso de Windows para elevación a NT AUTHORITY\SYSTEM.
5|Obtención de Control Total|apt41_getsystem.png|15/08/2026|Demostración de Control [T1078]|Obtención de privilegio máximo con getsystem y volcado de hashes SAM.
{%- endcapture -%}

{%- assign lista_pasos = datos_pasos | newline_to_br | split: "<br />" -%}

{% for fila in lista_pasos %}
  {% assign info = fila | strip | split: "|" %}
  {% if info.size > 1 %}
    <div class="paso-contenedor" style="margin-bottom: 40px; padding: 20px; border-left: 4px solid #007acc; background-color: #f9f9f9;">
      <h3>Paso {{ info[0] }}: {{ info[1] }}</h3>
      <p style="color: #666; font-size: 0.9em; margin-top: -5px;">
        <strong>Fecha:</strong> {{ info[3] }} | <strong>Fase ATT&CK:</strong> {{ info[4] }}
      </p>
      
      <div class="imagen-wrapper" style="margin: 15px 0; background: #eaeaea; text-align: center; padding: 10px; border-radius: 4px;">
        <img src="{{ '/assets/img/' | append: info[2] | relative_url }}" alt="Captura del Paso {{ info[0] }}" style="max-width: 100%; height: auto; box-shadow: 0 2px 5px rgba(0,0,0,0.15);">
      </div>

      <div class="descripcion-paso" style="line-height: 1.6; color: #333; background: #fff; padding: 15px; border: 1px solid #ddd; border-radius: 4px;">
        <strong>Detalle Técnico de la Ejecución:</strong><br>
        {{ info[5] }}
      </div>
    </div>
  {% endif %}
{% endfor %}
</div>

---

## Acto 4 — Postura Defensiva y Detección

### 4.1 Estrategia de Detección y Mitigación Mapeada

| Técnica Ejecutada | Detección (Event ID / Fuente ATT&CK) | Mitigación (ATT&CK Mitigation) |
| :--- | :--- | :--- |
| **[T1021.002] SMB Admin Shares** | **Event ID 5140 / 5145:** Un recurso compartido fue accedido (`ADMIN$`, `C$`).<br>**Sysmon Event ID 3:** Conexiones de red entrantes al puerto 445. | **M1042 - Network Segmentation:** Bloquear el puerto 445 entre redes no confiables.<br>**M1026 - Privileged Account Management:** Deshabilitar cuentas de administrador local compartidas. |
| **[T1059.001] PowerShell** | **Event ID 4104 (Script Block Logging):** Registro de bloques de código ejecutados en PowerShell.<br>**Sysmon Event ID 1:** Creación del proceso `powershell.exe`. | **M1038 - Execution Prevention:** Restringir execution policy y habilitar Constrained Language Mode.<br>**M1027 - Password Policies:** Evitar la ejecución de comandos sin elevar privilegio. |
| **[T1543.003] Windows Service** | **System Event ID 7045 / Security Event ID 4697:** Un nuevo servicio fue instalado en el sistema.<br>**Sysmon Event ID 13:** Modificación del registro en `HKLM\SYSTEM\CurrentControlSet\Services`. | **M1047 - Audit:** Auditar la creación de servicios e impedir que usuarios sin permisos administrativos modifiquen rutas del SCM. |

### 4.2 Evidencia Defensiva Recopilada

1. **Monitoreo con Sysmon (Procesos):**
   * **Evidencia:** Registro del **Event ID 1** de Sysmon donde se visualiza el proceso padre `psexesvc.exe` generando una instancia de `cmd.exe` y subsecuentemente `powershell.exe` ejecutando comandos codificados.
2. **Visor de Eventos de Windows (Servicios):**
   * **Evidencia:** Registro del **System Event ID 7045** indicando la instalación de un servicio con un binario no confiable apuntando al directorio ejecutable de persistencia.
3. **Auditoría de Inicio de Sesión (Event Viewer):**
   * **Evidencia:** Registro del **Security Event ID 4624** (Logon Type 3 - Network) mostrando la autenticación remota desde la dirección IP de la máquina de ataque hacia la máquina objetivo.

---

### Conclusión personal
De lo revisado me permitio acercarme a conocimientos de despliegue de plaaformas en docker, analizar del proceso  walware utilizados y subtecnicas en general de mitre attack