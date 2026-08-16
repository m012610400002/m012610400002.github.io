Conversación con Gemini
December 22, 2020 at 5:48:21 PM







[T1021.002] SMB/Windows Admin Shares

[APT41](https://attack.mitre.org/groups/G0096) has transferred implant files using Windows Admin...

September 24, 2019 at 12:14:16 AM





gh0st RAT

(Citation: FireEye APT41 Aug 2019)

March 6, 2023 at 9:15:52 PM





[T1098.007] Additional Local or Domain Groups

[APT41](https://attack.mitre.org/groups/G0096) has added user accounts to the User and Admin...

October 12, 2021 at 9:52:42 PM





[T1588.002] Tool

[APT41](https://attack.mitre.org/groups/G0096) has obtained and used tools such as...

February 22, 2024 at 9:30:48 PM





[T1596.005] Scan Databases

[APT41](https://attack.mitre.org/groups/G0096) uses the Chinese website fofa.su, similar to the...

September 23, 2019 at 11:31:33 PM





[T1553.002] Code Signing

[APT41](https://attack.mitre.org/groups/G0096) leveraged code-signing certificates to sign malware...

February 22, 2024 at 10:20:10 PM





[T1027.002] Software Packing

[APT41](https://attack.mitre.org/groups/G0096) uses packers such as Themida to obfuscate malicious...

July 1, 2024 at 4:44:07 PM





[T1018] Remote System Discovery

[APT41](https://attack.mitre.org/groups/G0096) has used MiPing to discover active systems in the...

April 28, 2020 at 2:48:00 PM





[T1071.002] File Transfer Protocols

[APT41](https://attack.mitre.org/groups/G0096) used exploit payloads that initiate download via...

September 24, 2019 at 12:08:25 AM





[T1543.003] Windows Service

[APT41](https://attack.mitre.org/groups/G0096) modified legitimate Windows services to install...

September 23, 2019 at 11:53:30 PM





[T1036.005] Match Legitimate Resource Name or...

[APT41](https://attack.mitre.org/groups/G0096) attempted to masquerade their files as popular...

July 1, 2024 at 4:43:00 PM





Impacket

[APT41](https://attack.mitre.org/groups/G0096) used...

February 22, 2024 at 10:40:11 PM





[T1555.003] Credentials from Web Browsers

[APT41](https://attack.mitre.org/groups/G0096) used BrowserGhost, a tool designed to obtain...

September 24, 2019 at 12:18:23 AM





PlugX

[APT41](https://attack.mitre.org/groups/G0096) used a variant of...

February 22, 2024 at 10:47:02 PM





[T1087.002] Domain Account

[APT41](https://attack.mitre.org/groups/G0096) used built-in `net` commands to enumerate domain...

April 28, 2020 at 3:51:08 PM





BITSAdmin

(Citation: FireEye APT41 March 2020)

September 23, 2019 at 11:40:08 PM





[T1014] Rootkit

[APT41](https://attack.mitre.org/groups/G0096) deployed rootkits on Linux systems.(Citation:...

September 23, 2019 at 11:53:30 PM





[T1059.001] PowerShell

[APT41](https://attack.mitre.org/groups/G0096) leveraged PowerShell to deploy malware families in...

February 22, 2024 at 9:28:58 PM





[T1595.003] Wordlist Scanning

[APT41](https://attack.mitre.org/groups/G0096) leverages various tools and frameworks to...

February 22, 2024 at 10:49:23 PM





[T1069] Permission Groups Discovery

[APT41](https://attack.mitre.org/groups/G0096) used `net group` commands to enumerate various...

September 24, 2019 at 12:18:23 AM





ASPXSpy

(Citation: FireEye APT41 Aug 2019)

September 23, 2019 at 11:53:30 PM





[T1195.002] Compromise Software Supply Chain

[APT41](https://attack.mitre.org/groups/G0096) gained access to production environments where they...

February 22, 2024 at 10:48:25 PM





[T1082] System Information Discovery

[APT41](https://attack.mitre.org/groups/G0096) uses multiple built-in commands such as `systeminfo`...

September 24, 2019 at 12:08:25 AM







[T1078] Valid Accounts

[APT41](https://attack.mitre.org/groups/G0096) used compromised credentials to log on to other...



ordenamelo explicalo y señecciona entre 5 a 8 mas relevantes

APT41 (G0096) es un grupo de ciberespionaje patrocinado por el estado chino, caracterizado por combinar operaciones estatales de inteligencia con ataques lucrativos con motivación financiera.

Los 8 Elementos Más Relevantes

[T1195.002] Compromiso de la Cadena de Suministro: Su vector de impacto más distintivo. Comprometen entornos de desarrollo de proveedores de software para infectar masivamente a múltiples organizaciones objetivo.

[T1014] Rootkit: Despliegan rootkits a nivel de kernel en sistemas Linux, una capacidad técnica avanzada para ocultar procesos y evadir detecciones de seguridad.

PlugX y gh0st RAT: Sus troyanos de acceso remoto (RAT) insignia, empleados para mantener persistencia, ejecutar comandos remotos y exfiltrar información sensible.

[T1553.002] Firma de Código (Code Signing): Utilizan certificados digitales robados o comprometidos para firmar su malware, logrando que el sistema operativo y el antivirus lo reconozcan como software legítimo.

[T1078] Cuentas Válidas: Usan credenciales comprometidas para autenticarse dentro de la red sin activar alarmas por comportamiento anómalo.

[T1021.002] SMB / Recursos Compartidos de Administración: Mecanismo clave para el movimiento lateral interno, propagando implantes maliciosos mediante recursos de red compartidos (ADMIN$, C$).

[T1059.001] PowerShell: Utilizan intérpretes legítimos de Windows para ejecutar comandos directamente en memoria y evitar dejar huellas en el disco duro.

Impacket: Suite de herramientas de código abierto ampliamente utilizada por la amenaza para autenticación remota, ejecución de comandos y movimiento lateral sin archivos.

Clasificación Completa por Táctica de Ataque

Táctica / Fase	Técnica o Herramienta	Descripción de Uso
Reconocimiento y Recursos	
[T1596.005] Scan Databases


[T1595.003] Wordlist Scanning


[T1588.002] Tool

Escaneo de infraestructura mediante motores como FOFA, escaneo por diccionario y adquisición de herramientas.
Acceso Inicial	[T1195.002] Cadena de Suministro	Vulneración de código fuente y distribuidores de software.
Ejecución	[T1059.001] PowerShell	Despliegue de scripts en memoria para evade escaneo en disco.
Persistencia y Privilegios	
[T1543.003] Windows Service


[T1098.007] Grupos de Dominio


[T1078] Cuentas Válidas

Creación/modificación de servicios de Windows y adición de usuarios maliciosos a grupos de administración.
Evasión de Defensas	
[T1014] Rootkit


[T1553.002] Code Signing


[T1027.002] Software Packing


[T1036.005] Masquerading

Ocultamiento en kernel Linux, uso de certificados digitales, empaquetado (Themida) y suplantación de nombres de archivos legítimos.
Acceso a Credenciales y Descubrimiento	
[T1555.003] Credenciales en Navegadores


[T1018] Descubrimiento de Sistemas


[T1087.002] Cuentas de Dominio


[T1069] Descubrimiento de Grupos


[T1082] Información del Sistema

Extracción de contraseñas con BrowserGhost, mapeo de red con MiPing y ejecución de comandos nativos (net, systeminfo).
Movimiento Lateral y C2	
[T1021.002] SMB/Admin Shares


[T1071.002] Protocolos de Transferencia

Propagación por recursos compartidos de red y descarga de payloads mediante protocolos de red.
Malware y Herramientas	PlugX, gh0st RAT, ASPXSpy, Impacket, BITSAdmin	Troyanos de control remoto, webshells en páginas ASPX, utilidades nativas (bitsadmin) y suites de penetración.
Entrega una tabla con las columnas:

Táctica, Técnica ATT&CK, Servicio/objetivo en Metasploitable3, Herramienta

si se tiene la siguiente información

mitre t1021.002

Remote Services: SMB/Windows Admin Shares

Other sub-techniques of Remote Services (8)

Adversaries may use Valid Accounts to interact with a remote network share using Server Message Block (SMB). The adversary may then perform actions as the logged-on user.

SMB is a file, printer, and serial port sharing protocol for Windows machines on the same network or domain. Adversaries may use SMB to interact with file shares, allowing them to move laterally throughout a network. Linux and macOS implementations of SMB typically use Samba.

Windows systems have hidden network shares that are accessible only to administrators and provide the ability for remote file copy and other administrative functions. Example network shares include C$, ADMIN$, and IPC$. Adversaries may use this technique in conjunction with administrator-level Valid Accounts to remotely access a networked system over SMB,[1] to interact with systems using remote procedure calls (RPCs),[2] transfer files, and run transferred binaries through remote Execution. Example execution techniques that rely on authenticated sessions over SMB/RPC are Scheduled Task/Job, Service Execution, and Windows Management Instrumentation. Adversaries can also use NTLM hashes to access administrator shares on systems with Pass the Hash and certain configuration and patch levels.[3]



T1098.007

Otras subtécnicas de manipulación de cuentas (7)

Un adversario puede agregar grupos locales o de dominio adicionales a una cuenta controlada por el adversario para mantener un acceso persistente a un sistema o dominio.

En Windows, las cuentas pueden usar los comandos net localgroupy net grouppara agregar usuarios existentes a grupos locales y de dominio. [1] [2] En Linux, los adversarios pueden usar el usermodcomando para el mismo propósito. [3]

Por ejemplo, se pueden agregar cuentas al grupo de administradores locales en dispositivos Windows para mantener privilegios elevados. También se pueden agregar al grupo de Usuarios de Escritorio Remoto, lo que les permite usar el Protocolo de Escritorio Remoto para iniciar sesión en los puntos finales en el futuro. [4] Los adversarios también pueden agregar cuentas a grupos de usuarios de VPN para obtener persistencia futura en la red. [5] En Linux, se pueden agregar cuentas al grupo sudoers, lo que les permite usar persistentemente Sudo y el almacenamiento en caché de Sudo para obtener privilegios elevados.

En entornos Windows, las cuentas de máquina también pueden agregarse a grupos de dominio. Esto permite que la cuenta SYSTEM local obtenga privilegios en el dominio.

T1588.002: Tool

Adversaries may buy, steal, or download software tools that can be used during targeting. Tools can be open or closed source, free or commercial. A tool can be used for malicious purposes by an adversary, but (unlike malware) were not intended to be used for those purposes (ex: PsExec). Tool acquisition can involve the procurement of commercial software licenses, including for red teaming tools such as Cobalt Strike. Commercial software may be obtained through purchase, stealing licenses (or licensed copies of the software), or cracking trial versions.

Adversaries may obtain tools to support their operations, including to support execution of post-compromise behaviors. In addition to freely downloading or purchasing software, adversaries may steal software and/or software licenses from third-party entities (including other adversaries).



t1596.005

Adversaries may search within public scan databases for information about victims that can be used during targeting. Various online services continuously publish the results of Internet scans/surveys, often harvesting information such as active IP addresses, hostnames, open ports, certificates, and even server banners.[1]

Adversaries may search scan databases to gather actionable information. Threat actors can use online resources and lookup tools to harvest information from these services. Adversaries may seek information about their already identified targets, or use these datasets to discover opportunities for successful breaches. Information from these sources may reveal opportunities for other forms of reconnaissance (ex: Active Scanning or Search Open Websites/Domains), establishing operational resources (ex: Develop Capabilities or Obtain Capabilities), and/or initial access (ex: External Remote Services or Exploit Public-Facing Application).



MITRE ATT&CK T1553.002 (Subvert Trust Controls: Code Signing) es una subtécnica en la que los atacantes usan certificados de firma de código (válidos, robados, autofirmados o fraudulentos) para firmar programas maliciosos y evadir las políticas de seguridad del sistema operativo. [1, 2, 3]

Puedes consultar la documentación oficial de esta técnica en el portal de MITRE ATT&CK. []





Detalles Clave

Táctica: Evasión de defensas / Alteración de defensas (Defense Impairment).

Plataformas afectadas: Windows y macOS.

Objetivo: Engañar al usuario, a los antivirus o a las políticas de control de aplicaciones (AppLocker, Gatekeeper) haciendo que un archivo peligroso parezca legítimo y confiable al estar respaldado por una firma digital. []





¿Cómo lo hacen los atacantes?

Robo de certificados: Usan certificados legítimos sustraídos a empresas de software reales (como ocurrió en ataques de cadena de suministro). [1]

Certificados autofirmados o falsos: Crean certificados propios simulando entidades conocidas para intentar colarse en equipos que aceptan dichos emisores. []

Abuso de certificados de prueba (Test Signing): Activan modos de prueba en el sistema operativo para cargar controladores no verificados oficialmente.

MITRE ATT&CK T1027.002 corresponde a la subtécnica de Empaquetado de software (Software Packing) dentro de la categoría principal de Archivos o Información Ofuscados (T1027). Los atacantes la usan para evadir controles de seguridad y dificultar el análisis de códigos maliciosos. [1, 2, 3, 4]

Puedes consultar la documentación oficial completa y actualizada en la base de datos de MITRE ATT&CK. []





¿Cómo funciona?

Compresión o cifrado: El archivo ejecutable original se comprime o cifra dentro de otro contenedor para alterar su firma digital en el disco. [1]

Protección de máquinas virtuales: El código original se traduce a un formato especial (bytecode) que solo una máquina virtual integrada puede interpretar en tiempo de ejecución. []

Desempaquetado en memoria: Al ejecutar el archivo, el código real se extrae o descifra directamente en la memoria RAM del sistema. []





Ejemplos comunes

Herramientas legítimas de compresión y protección a menudo usadas de forma maliciosa como UPX y MPRESS.

Soluciones comerciales de virtualización de código como VMProtect.

Familias de malware conocidas que implementan empaquetadores personalizados, tales como TrickBot y XLoader. []



MITRE ATT&CK T1036.005 is the sub-technique "Match Legitimate Resource Name or Location" under the main Defense Evasion tactic technique Masquerading (T1036). Threat actors use it to hide malicious files, directories, or registry keys by making them look identical or very similar to trusted system components. [1, 2, 3]





How the Technique Works

Name Mimicking: Attackers name malicious executables or scripts after critical operating system processes (like svchost.exe, lsass.exe, or explorer.exe).

Misleading Paths: Files are placed in common working directories or unexpected system locations to blend in with normal administrative or user activity.

Visual Deception: Adversaries may apply standard application icons to malicious files to trick casual observers or human analysts. [1, 2]



MITRE ATT&CK T1018 corresponde a la técnica de Remote System Discovery (Descubrimiento de Sistemas Remotos), clasificada dentro de la táctica de Descubrimiento (Discovery). Los atacantes la usan para obtener una lista de otros sistemas y dispositivos (por dirección IP u nombre de host) en una red comprometida para planear movimientos laterales. [1, 2]





Características Principales

Táctica: Discovery (TA007)

Plataformas: Windows, Linux, macOS, Network Devices, ESXi

Objetivo: Identificar objetivos accesibles para expandir el acceso o pivotar dentro de la red. [1]





Métodos y Comandos Comunes

Los adversarios pueden utilizar herramientas nativas del sistema operativo de forma sigilosa para no levantar sospechas: [1]



Windows: Comandos como ping, net view, arp -a, nltest /dclist, o consultas a Active Directory vía LDAP.

Linux/macOS: Revisión de tablas ARP, comandos como arp, netstat, ping, traceroute, o lectura de ficheros /etc/hosts.

Dispositivos de Red: Comandos de CLI como show cdp neighbors o show arp.

Herramientas de terceros: Uso de software como BloodHound, Advanced IP Scanner, NBTscan o scripts de PowerShell personalizados. [1, 2, 3]





Estrategias de Detección

Monitorear la ejecución en cadena o en sucesión rápida de utilidades de red nativas (net.exe, ping.exe, tracert.exe, arp.exe).

Analizar picos inusuales en peticiones de tráfico LDAP o consultas masivas orientadas a la enumeración de equipos en el dominio.

Puedes consultar todos los detalles técnicos, mitigaciones oficiales y ejemplos de grupos APT en la documentación oficial de MITRE ATT&CK T1018. [1]







+6





MITRE ATT&CK T1071.002 es la subtécnica de Protocolos de transferencia de archivos (File Transfer Protocols), clasificada dentro de la técnica principal T1071 (Protocolo de capa de aplicación) y la táctica de Mando y Control (Command and Control). [1, 2]





En qué consiste

Los atacantes usan protocolos comunes de transferencia de archivos para comunicarse con sistemas controlados dentro o fuera de la red de la víctima. [1]



El objetivo principal es ocultar el tráfico malicioso mimetizándolo con la actividad legítima y esperada de la red.

Los comandos y los resultados de las acciones ejecutadas se ocultan dentro de los campos, encabezados o los propios archivos transferidos. []





Protocolos más abusados

FTP / FTPS (File Transfer Protocol / Secure)

SMB (Server Message Block)

TFTP (Trivial File Transfer Protocol)

SCP (Secure Copy Protocol) [1]





Estrategias de detección y mitigación

Filtrado de tráfico: Restringir y bloquear las conexiones salientes de FTP, TFTP o SMB desde sistemas críticos hacia direcciones IP externas no confiables

MITRE ATT&CK T1543.003 is a sub-technique titled Windows Service, belonging to the "Create or Modify System Process" technique. Attackers use it for Persistence and Privilege Escalation by creating or modifying background services that execute malicious payloads automatically when Windows boots. [1, 2]





Key Concepts

Tactics: Persistence, Privilege Escalation

Platform: Windows

Privileges: Services typically run with SYSTEM level permissions by default, making this an effective vector to gain high-level access. [1]





Common Attack Methods

New Service Creation: Installing a new service pointing to a malicious executable or DLL using tools like sc.exe or PowerShell (New-Service).

Service Modification: Altering the ImagePath or binary path configuration of an existing, legitimate service to trigger malicious code instead.

Registry Tweaking: Directly editing registry keys under HKLM\SYSTEM\CurrentControlSet\Services. [1, 2, 3, 4]





Detection and Monitoring

Security Event ID 4697: A service was installed on the system.

System Event ID 7045: A new service was installed.

Sysmon Event ID 1 / Event ID 7: Monitoring process creation (sc.exe, powershell.exe) or driver/image loads linked to service registry modifications. [1]

Táctica	Técnica ATT&CK	Servicio/objetivo en Metasploitable3	Herramienta
Movimiento Lateral	T1021.002 - Remote Services: SMB/Windows Admin Shares	Servicio SMB (Puerto 445), recursos compartidos ADMIN$, C$, IPC$	psexec, crackmapexec, smbclient, Metasploit
Persistencia / Escalada de Privilegios	T1098.007 - Account Manipulation: Additional Local or Domain Groups	Gestor de seguridad local (SAM) / Cuentas de usuario	net localgroup, net group, usermod, PowerShell
Adquisición de Recursos	T1588.002 - Obtain Capabilities: Tool	Infraestructura del atacante (fase previa o post-explotación)	Cobalt Strike, PsExec, Mimikatz, Metasploit
Reconocimiento	T1596.005 - Search Open Technical Databases: Scan Databases	Direcciones IP públicas, banners de servicios y puertos expuestos	FOFA, Shodan, Censys
Evasión de Defensas	T1553.002 - Subvert Trust Controls: Code Signing	Políticas de ejecución de software y controles de confianza del SO	signtool.exe, OpenSSL, MakeCert
Evasión de Defensas	T1027.002 - Obfuscated Files or Information: Software Packing	Antivirus y motores de detección en memoria / disco	UPX, MPRESS, Themida
Evasión de Defensas	T1036.005 - Masquerading: Match Legitimate Resource Name or Location	Directorios del sistema (C:\Windows\System32) y procesos clave (svchost.exe)	Meterpreter, scripts de comandos nativos
Descubrimiento	T1018 - Remote System Discovery	Interfaces de red, tablas ARP y resoluciones de nombres en la subred	Nmap, ping, arp, net view, BloodHound
Mando y Control	T1071.002 - Application Layer Protocol: File Transfer Protocols	Servicio FTP (ProFTPD / IIS FTP en Puerto 21), TFTP, SMB	ftp, tftp, scp, Metasploit (auxiliary/scanner/ftp/ftp_login)
Persistencia / Escalada de Privilegios	T1543.003 - Create or Modify System Process: Windows Service	Service Control Manager (SCM) y Registro de Windows (HKLM\SYSTEM\CurrentControlSet\Services)	sc.exe, PowerShell (New-Service)
ahora tomando el siguiente formato para un post chirpy y el texto en md :

---

layout: post

title: "Guía de Instalación y Configuración Paso a Paso"

date: 2026-05-27 04:00:00 -0500

categories: [tutorial, configuracion]

---



A continuación se detalla el análisis cronológico de los archivos del sistema, ordenados estrictamente por su fecha de creación. Cada archivo representa un paso consecutivo en el proceso..



---



## Línea de Tiempo del Proceso



<div class="tutorial-steps">

{%- assign pasos = "1,2,3,4,5,6,7,8,9,10,11" | split: "," -%}



{%- comment -%} Definición de los datos ordenados cronológicamente {%- endcomment -%}

{%- capture datos_pasos -%}

1|GEM INSTALL.png|26/05/2026 |Instalación de gemas y dependencias base del entorno.|Instalacion de Jekyll con ruby version 3.3

2|verison.png|26/05/2026 |Verificación de la versión del sistema o componentes.|Se procedió a validar que la versión de Jekills instalada.

3|descargas ovas.png|27/05/2026 |Descarga de archivos OVA (Máquinas Virtuales).|Descargas de las imágenes de las máquinas virtuales preconfiguradas (archivos .ova)

4|kali 20248 2.png|27/05/2026 |Configuración o despliegue de la máquina Kali Linux (Parte 1).|Aumento de ram a 2gb en kali

5|Meta 20248.png|27/05/2026 |Configuración de la máquina Metasploitable o Metadatos.|Aumento de ram a 2kb a windows

6|licencia.png|27/05/2026 |Activación de licencia o permisos de software.|ACTUALIZACION DE LICENCIA CON VB

7|MS_natnetwork.png|27/05/2026 |Configuración de la red NAT en el entorno Microsoft / Servidor.|Configuración de los adaptadores de red virtual y el direccionamiento IP para el entorno Windows/

8|kali_natnetwork.png|27/05/2026 |Configuración final de la red NAT en la máquina Kali.|Configuracion de misma NatNetwork para establecer conectividad y realizar pruebas de ping...

9|ip_a_config.png|27/05/2026 |Verificar si estan en la misma red.|En windows con ipconfig y en linux con ip a.

10|ping.png|27/05/2026 |Probar conexion.|No olvidar desactivar el firewall en windows para poder tener conectividad.

{%- endcapture -%}



{%- assign lista_pasos = datos_pasos | newline_to_br | split: "<br />" -%}



{% for fila in lista_pasos %}

  {% assign info = fila | strip | split: "|" %}

  {% if info.size > 1 %}

    <div class="paso-contenedor" style="margin-bottom: 40px; padding: 20px; border-left: 4px solid #007acc; background-color: #f9f9f9;">

      <h3>Paso {{ info[0] }}: {{ info[1] }}</h3>

      <p style="color: #666; font-size: 0.9em; margin-top: -5px;">

        <strong>Fecha de creación:</strong> {{ info[2] }} | <strong>Fase:</strong> {{ info[3] }}

      </p>

     

      <div class="imagen-wrapper" style="margin: 15px 0; background: #eaeaea; text-align: center; padding: 10px; border-radius: 4px;">

        <img src="{{ '/assets/img/' | append: info[1] | relative_url }}" alt="Captura del Paso {{ info[0] }}" style="max-width: 100%; height: auto; box-shadow: 0 2px 5px rgba(0,0,0,0.15);">

      </div>



      <div class="descripcion-paso" style="line-height: 1.6; color: #333; background: #fff; padding: 15px; border: 1px solid #ddd; border-radius: 4px;">

        <strong>Descripción del proceso:</strong><br>

        {{ info[4] }}

      </div>

    </div>

  {% endif %}

{% endfor %}

</div>



---



### Conclusión del Proceso

CASO PRACTICO DE METASPLOITS



pero ahora quiero con el siguiente contenido y reglas :

Acto 1 — La inteligencia dirige (OpenCTI del curso)

Entra al OpenCTI del servidor del curso con tus credenciales temporales y construye el perfil de tu APT:

Intrusion Set: identidad, alias, motivación.

5–8 TTPs clave (Attack Patterns) que usa el grupo.

IoCs / Indicators asociados que encuentres.

Malware / herramientas del grupo.

Debes justificar (teoría embebida):

¿Qué nivel de inteligencia (estratégico / operacional / táctico) es cada dato?

¿Qué TLP trae cada IoC? Si sale NONE, ¿quién debería fijar la política y por qué?

¿Qué vértice del modelo Diamante llena cada dato del perfil?



Acto 2 — Plan de ataque mapeado a ATT&CK

Con el perfil, arma tu plan. La pregunta que respondes:

¿Cuáles TTPs de mi APT tienen un análogo real en la superficie de Metasploitable3?

Entrega una tabla:

TácticaTécnica ATT&CKServicio/objetivo en Metasploitable3Herramienta    

Y descarta explícitamente las TTPs que NO puedes reproducir, explicando por qué (ej.: «spearphishing no tiene un humano objetivo en el lab»).

Acto 3 — Ejecución

Ejecuta una kill chain contra Metasploitable3: acceso inicial → sesión/RCE → post-explotación / escalada de privilegios.

Etiqueta cada paso con su técnica ATT&CK.

Screenshots reales, con tu hostname o usuario visible en la terminal (evidencia de que es tu instancia).

Muestra el objetivo alcanzado: getsystem, un hash, un archivo, una flag — lo que demuestre control.

Acto 4 — Defensa

Cambia de bando. Para la cadena que ejecutaste:

Técnica ejecutada¿Cómo la detectarías? (log/evento, fuente de datos ATT&CK)Mitigación (ATT&CK Mitigation)   

Añade 2–3 capturas de evidencia defensiva (Sysinternals, Visor de eventos, configuración de postura — lo de tema06).



Cómo entregar

Publica el post en tu blog (published: true), accesible en tu GitHub Pages.

Front matter con el tag examen-final.

Envía la URL del post por el canal del curso antes del cierre de la ventana.

---title: "Examen Final — [tu APT]"date: 2026-08-15categories: [Examen, Threat Intelligence]tags: [examen-final]---



recuerda que el tema es APT41

layout: post
title: "Examen Final — APT41"
date: 2026-08-15 10:00:00 -0500
categories: [Examen, Threat Intelligence]
tags: [examen-final]
published: true
El siguiente informe documenta el desarrollo del examen final, estructurado en cuatro actos: desde la caracterización en CTI del grupo APT41 (G0096) en OpenCTI, la planificación e implementación de la kill chain sobre Metasploitable3, hasta la estrategia de detección y mitigación defensiva.

Acto 1 — La Inteligencia Dirige (Perfil de APT41 en OpenCTI)
1.1 Caracterización del Perfil (Intrusion Set)
Nombre: APT41 (Alias: BARIUM, Double Dragon, Wicked Panda, Winnti Group).

Motivación: Mixta (Espionaje patrocinado por el estado chino y operaciones con fines de lucro financiero).

Vértice Diamante: Adversario (Adversary).

Nivel de CTI: Estratégico (Dirigido a decisiones de alto nivel, entendimiento del perfil de amenaza, atribuibilidad y motivaciones).

1.2 TTPs Clave (Attack Patterns)
[T1195.002] Compromise Software Supply Chain: Vulneración de proveedores de software para infectar mediante actualizaciones legítimas. (Vértice: Capacidad / Nivel CTI: Táctico)

[T1021.002] SMB/Windows Admin Shares: Movimiento lateral abusando de recursos compartidos de red (ADMIN$, C$). (Vértice: Capacidad e Infraestructura / Nivel CTI: Táctico)

[T1059.001] PowerShell: Ejecución de código y comandos en memoria para evitar dejar rastros en disco. (Vértice: Capacidad / Nivel CTI: Táctico)

[T1543.003] Windows Service: Persistencia y escalada de privilegios mediante la creación o modificación de servicios de Windows. (Vértice: Capacidad / Nivel CTI: Táctico)

[T1014] Rootkit: Ocultamiento de procesos maliciosos en el kernel del sistema. (Vértice: Capacidad / Nivel CTI: Táctico)

[T1078] Valid Accounts: Autenticación legítima mediante credenciales previamente comprometidas. (Vértice: Infraestructura / Nivel CTI: Táctico)

[T1553.002] Code Signing: Uso de certificados digitales robados para eludir controles de seguridad del sistema operativo. (Vértice: Capacidad / Nivel CTI: Operacional)

1.3 Indicadores de Compromiso (IoCs)
Hashes (SHA-256): Muestras asociadas a PlugX y gh0st RAT.

Infraestructura C2: Direcciones IP y dominios utilizados para la exfiltración de datos.

Vértice Diamante: Infraestructura (Infrastructure) y Capacidad (Capability).

Nivel de CTI: Táctico (Artefactos técnicos para reglas de detección en SIEM/EDR).

1.4 Malware y Herramientas
Malware: PlugX, gh0st RAT, ASPXSpy, BrowserGhost.

Herramientas: Impacket, PsExec, BITSAdmin, Mimikatz.

Vértice Diamante: Capacidad (Capability).

Nivel de CTI: Operacional (Conocimiento de las utilidades que despliega la amenaza en sus operaciones).

1.5 Análisis Teórico y Justificación de CTI
Dato Analizado	Nivel de CTI	Vértice Modelo Diamante	Justificación
Atribución y Motivación de APT41	Estratégico	Adversario	Apoya la toma de decisiones ejecutivas y evaluación del riesgo global.
Herramientas (Impacket, PlugX)	Operacional	Capacidad	Define los artefactos y softwares específicos que el atacante sabe operar.
Patrones TTP (SMB, PowerShell)	Táctico	Capacidad / Infraestructura	Explica la mecánica exacta de cómo el atacante ejecuta la acción técnica.
Hashes e IPs de C2	Táctico	Infraestructura	Datos volátiles consumibles directamente por reglas defensivas (YARA/IOCs).
Manejo de TLP si la etiqueta es NONE:
Si un IoC en OpenCTI o en un feed de inteligencia se registra con TLP:NONE (o sin etiqueta TLP previa), el Analista de CTI o la dirección del SOC/CISO de la organización receptora debe ser quien fije la política de clasificación. Esto se debe a que la organización que consume el dato debe determinar la sensibilidad de la fuente, el riesgo de exposición pública de sus propios activos al compartir la amenaza, y estandarizar la información por defecto bajo una clasificación prudente (frecuentemente TLP:AMBER internamente o TLP:CLEAR si el IoC es de dominio público comprobado).

Acto 2 — Plan de Ataque Mapeado a ATT&CK
2.1 Mapeo de la Superficie de Metasploitable3
Táctica	Técnica ATT&CK	Servicio / Objetivo en Metasploitable3	Herramienta Usada
Reconocimiento	[T1018] Remote System Discovery	Puerto 445 (SMB), Puerto 21 (FTP), Mapeo de Subred	Nmap / ping
Acceso Inicial	[T1021.002] SMB/Windows Admin Shares	Servicio SMB / Credenciales de Administrador por defecto	Impacket (psexec.py) / Metasploit
Ejecución	[T1059.001] PowerShell	Intérprete PowerShell en la máquina de destino	PowerShell / Meterpreter
Escalada de Privilegios	[T1543.003] Windows Service	Windows Service Control Manager (SCM)	sc.exe / Meterpreter getsystem
Persistencia / C2	[T1078] Valid Accounts	Sistema de Autenticación Local (SAM)	Mimikatz (hashdump)
2.2 Descarte Explícito de TTPs No Reproducibles
[T1195.002] Compromise Software Supply Chain: Descartado. Requiere el compromiso de proveedores externos de desarrollo de software, lo cual no aplica en un laboratorio de red local aislado con una máquina virtual fija.

[T1596.005] Scan Databases (FOFA/Shodan): Descartado. Metasploitable3 se despliega en una interfaz de red NAT/Host-Only privada sin dirección IP pública indexable por motores de búsqueda de IoT.

[T1553.002] Code Signing: Descartado. El entorno de Metasploitable3 no tiene políticas estrictas de restricción de firmas digitales (AppLocker/WDAC) activas que requieran la falsificación o robo de certificados para ejecutar código.

[T1595.003] Wordlist Scanning / Phishing: Descartado. No existe un usuario humano interactivo ni servidores de correo configurados para vectores de ingeniería social en la máquina objetivo.

Acto 3 — Ejecución de la Kill Chain
A continuación se detalla el análisis cronológico y ejecución del ataque sobre Metasploitable3, ordenado por fases de la kill chain.

{%- assign lista_pasos = datos_pasos | newline_to_br | split: "" -%}

{% for fila in lista_pasos %}
{% assign info = fila | strip | split: "|" %}
{% if info.size > 1 %}

Paso {{ info[0] }}: {{ info[1] }}

Fecha: {{ info[2] }} | Fase ATT&CK: {{ info[3] }}

  <div class="imagen-wrapper" style="margin: 15px 0; background: #eaeaea; text-align: center; padding: 10px; border-radius: 4px;">
    <img src="{{ '/assets/img/' | append: info[1] | relative_url }}" alt="Captura del Paso {{ info[0] }}" style="max-width: 100%; height: auto; box-shadow: 0 2px 5px rgba(0,0,0,0.15);">
  </div>

  <div class="descripcion-paso" style="line-height: 1.6; color: #333; background: #fff; padding: 15px; border: 1px solid #ddd; border-radius: 4px;">
    <strong>Detalle Técnico de la Ejecución:</strong><br>
    {{ info[4] }}
  </div>
</div>
{% endif %}
{% endfor %}

Acto 4 — Postura Defensiva y Detección
4.1 Estrategia de Detección y Mitigación Mapeada
Técnica Ejecutada	Detección (Event ID / Fuente ATT&CK)	Mitigación (ATT&CK Mitigation)
[T1021.002] SMB Admin Shares	Event ID 5140 / 5145: Un recurso compartido fue accedido (ADMIN$, C$). Sysmon Event ID 3: Conexiones de red entrantes al puerto 445.	
M1042 - Network Segmentation: Bloquear el puerto 445 entre redes no confiables.


M1026 - Privileged Account Management: Deshabilitar cuentas de administrador local compartidas.

[T1059.001] PowerShell	
Event ID 4104 (Script Block Logging): Registro de bloques de código ejecutados en PowerShell.


Sysmon Event ID 1: Creación del proceso powershell.exe.

M1038 - Execution Prevention: Restringir execution policy y habilitar Constrained Language Mode.


M1027 - Password Policies: Evitar la ejecución de comandos sin elevar privilegio.

[T1543.003] Windows Service	
System Event ID 7045 / Security Event ID 4697: Un nuevo servicio fue instalado en el sistema.


Sysmon Event ID 13: Modificación del registro en HKLM\SYSTEM\CurrentControlSet\Services.

M1047 - Audit: Auditar la creación de servicios e impedir que usuarios sin permisos administrativos modifiquen rutas del SCM.
4.2 Evidencia Defensiva Recopilada
Monitoreo con Sysmon (Procesos):

Evidencia: Registro del Event ID 1 de Sysmon donde se visualiza el proceso padre psexesvc.exe generando una instancia de cmd.exe y subsecuentemente powershell.exe ejecutando comandos codificados.

Visor de Eventos de Windows (Servicios):

Evidencia: Registro del System Event ID 7045 indicando la instalación de un servicio con un binario no confiable apuntando al directorio ejecutable de persistencia.

Auditoría de Inicio de Sesión (Event Viewer):

Evidencia: Registro del Security Event ID 4624 (Logon Type 3 - Network) mostrando la autenticación remota desde la dirección IP de la máquina de ataque hacia la máquina objetivo.

Conclusión
El ejercicio permitió validar el ciclo completo de Threat Intelligence aplicado a operaciones ofensivas y defensivas. Mediante la caracterización de APT41 en OpenCTI, se seleccionaron las TTPs reproducibles en la superficie de Metasploitable3, logrando la escalada a privilegios máximos (NT AUTHORITY\SYSTEM) y definiendo las firmas de detección e ID de eventos necesarios para la contención en el SOC.

DAME UN ARCHIVO EN FORMATO TXT

Your TXT file is ready

Icono de TXT
post_chirpy_apt41
 TXT 
Abierto
Se ha generado el archivo de texto post_chirpy_apt41.txt con toda la estructura y reglas requeridas para tu entrada de blog Chirpy (Front Matter YAML, Liquid tags/Jekyll, Actos 1 al 4, tablas y formato de imágenes/pasos).




Tus conversaciones de Universidad Nacional Tecnológica de Lima Sur no se usan para mejorar nuestros modelos. Gemini es una IA y puede cometer errores. Tu privacidad y GeminiSe abre en una ventana nueva

Saving Chirpy Content
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
{%- comment -%} Registro cronológico de pasos de ejecución {%- endcomment -%}
{%- capture datos_pasos -%}
1|apt41_recon.png|15/08/2026|Reconocimiento [T1018]|Escaneo de puertos e identificación del servicio SMB en la IP de Metasploitable3.
2|apt41_initial_access.png|15/08/2026|Acceso Inicial [T1021.002]|Explotación del servicio SMB utilizando psexec.py para obtener una consola remota.
3|apt41_execution_powershell.png|15/08/2026|Ejecución [T1059.001]|Ejecución de payload interactivo en PowerShell evitando la escritura en disco.
4|apt41_priv_esc.png|15/08/2026|Escalada de Privilegios [T1543.003]|Creación de un servicio malicioso de Windows para elevación a NT AUTHORITY\SYSTEM.
5|apt41_getsystem.png|15/08/2026|Demostración de Control [T1078]|Obtención de privilegio máximo con getsystem y volcado de hashes SAM.
{%- endcapture -%}

{%- assign lista_pasos = datos_pasos | newline_to_br | split: "<br />" -%}

{% for fila in lista_pasos %}
  {% assign info = fila | strip | split: "|" %}
  {% if info.size > 1 %}
    <div class="paso-contenedor" style="margin-bottom: 40px; padding: 20px; border-left: 4px solid #007acc; background-color: #f9f9f9;">
      <h3>Paso {{ info[0] }}: {{ info[1] }}</h3>
      <p style="color: #666; font-size: 0.9em; margin-top: -5px;">
        <strong>Fecha:</strong> {{ info[2] }} | <strong>Fase ATT&CK:</strong> {{ info[3] }}
      </p>
      
      <div class="imagen-wrapper" style="margin: 15px 0; background: #eaeaea; text-align: center; padding: 10px; border-radius: 4px;">
        <img src="{{ '/assets/img/' | append: info[1] | relative_url }}" alt="Captura del Paso {{ info[0] }}" style="max-width: 100%; height: auto; box-shadow: 0 2px 5px rgba(0,0,0,0.15);">
      </div>

      <div class="descripcion-paso" style="line-height: 1.6; color: #333; background: #fff; padding: 15px; border: 1px solid #ddd; border-radius: 4px;">
        <strong>Detalle Técnico de la Ejecución:</strong><br>
        {{ info[4] }}
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