---
layout: post
title: "Examen Final — APT24"
date: 2026-08-15 00:00:00 -0500
categories: [Examen, Threat Intelligence]
tags: [examen-final, apt24, threat-intelligence]
published: true
---

## Introducción

El presente post documenta el análisis del grupo de amenaza **APT24**, con enfoque en su perfil, comportamiento operativo y relación con los conceptos de inteligencia de amenazas y detección defensiva.

## Objetivo del análisis

El objetivo principal es caracterizar la actividad de APT24, identificar sus vectores de acceso, técnicas de ejecución y patrones de persistencia, así como proponer medidas de mitigación y detección aplicables en un entorno real.

## Perfil del adversario

APT24 se presenta como un actor con capacidades de reconocimiento, acceso inicial, ejecución y persistencia en entornos comprometidos. La amenaza combina técnicas de ingeniería social, explotación de servicios y maniobras de acceso remoto con intención de mantener presencia y exfiltrar información.

## Fases de ejecución

### 1. Reconocimiento y enumeración

Se realiza un análisis inicial de la infraestructura objetivo con el fin de identificar puertos, servicios expuestos y posibles rutas de acceso no autorizadas.

### 2. Acceso inicial

Se evalúan mecanismos de ingreso, incluyendo autenticación remota y servicios con exposición directa a la red.

### 3. Ejecución y persistencia

Se revisan técnicas de ejecución en memoria o implantación de artefactos que permitan sobrevivir al entorno comprometido y mantener continuidad operativa.

### 4. Detección y mitigación

La defensa efectiva debe centrarse en la monitorización de anomalías, control de accesos, aplicación de parches y revisión de artefactos en endpoints y red.

---

## Evidencia visual del análisis

<div class="tutorial-steps">
{%- capture datos_pasos -%}
1|examen1.png|15/08/2026|Reconocimiento inicial|Se revisa la superficie expuesta para identificar servicios, puertos y posibles vectores de entrada.
2|examen2.png|15/08/2026|Análisis del entorno|Se evalúa la infraestructura objetivo para mapear comportamiento, exposición y alcance del riesgo.
3|examen3 entrando a knowledge.png|15/08/2026|Acceso a Knowledge|Se documenta la fase de investigación y análisis de contexto para orientar la hipótesis de amenaza.
4|examen4 vemos en el tiempo.png|15/08/2026|Visualización temporal|Se interpreta el comportamiento en el tiempo para detectar secuencias de actividad sospechosa.
5|examen5 malwares.png|15/08/2026|Análisis de malware|Se revisan artefactos y técnicas asociadas a la ejecución maliciosa y persistencia.
6|examen6 indicators none.png|15/08/2026|Indicadores y cierre|Se concluye con la revisión de indicadores para apoyar detección y contención.
{%- endcapture -%}

{%- assign lista_pasos = datos_pasos | newline_to_br | split: "<br />" -%}

{% for fila in lista_pasos %}
  {% assign info = fila | strip | split: "|" %}
  {% if info.size > 1 %}
    <div class="paso-contenedor" style="margin-bottom: 40px; padding: 20px; border-left: 4px solid #007acc; background-color: #f9f9f9;">
      <h3>Paso {{ info[0] }}: {{ info[3] }}</h3>
      <p style="color: #666; font-size: 0.9em; margin-top: -5px;">
        <strong>Captura asociada:</strong> <code>{{ info[1] }}</code> | <strong>Fecha:</strong> {{ info[2] }}
      </p>

      <div class="imagen-wrapper" style="margin: 15px 0; background: #eaeaea; text-align: center; padding: 10px; border-radius: 4px;">
        <img src="{{ '/assets/img/' | append: info[1] | relative_url }}" alt="Captura del Paso {{ info[0] }}" style="max-width: 100%; height: auto; box-shadow: 0 2px 5px rgba(0,0,0,0.15);">
      </div>

      <div class="descripcion-paso" style="line-height: 1.6; color: #333; background: #fff; padding: 15px; border: 1px solid #ddd; border-radius: 4px;">
        <strong>Análisis detallado:</strong><br>
        {{ info[4] }}
      </div>
    </div>
  {% endif %}
{% endfor %}
</div>

---

## Conclusiones

1. **La inteligencia de amenazas es clave:** entender el perfil del adversario permite priorizar la vigilancia y la respuesta.
2. **La detección temprana reduce el impacto:** correlacionar comportamiento anómalo con técnicas conocidas mejora la capacidad operativa.
3. **La contención es una prioridad:** la mitigación debe combinar segmentación, monitorización y controles de acceso con revisiones periódicas de seguridad.
