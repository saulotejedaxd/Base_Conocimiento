---
type: analysis
status: proposed
domain: diagnostico-celda-automatizada
last_verified: 2026-09-17
sources:
  - "[[Separación entre hecho e hipótesis]]"
  - "[[Modelo de relaciones]]"
tags:
  - lint
  - mantenimiento
---

# Revisión del vault 2026-09-17

Revisión LINT del vault completo ejecutada el 2026-09-17. No se modificó `raw/`. No se inventó información técnica.

## 1. Enlaces rotos

- 0 enlaces de dominio rotos. Todos los `[[wikilinks]]` de conceptos, entidades, fuentes y análisis resuelven a páginas existentes.
- Casos no considerados rotos: ejemplos de sintaxis en Bloques de código (`[[wikilinks]]`, `[[Nombre de página]]`) en `wiki/conventions.md`, `AGENTS.md` y `PROMPT_OPENCode.md`, y el ejemplo de esquema `[[Fuente]]` en `AGENTS.md`.

## 2. Páginas huérfanas e integración

- `wiki/index.md`: sin entrantes, esperable por ser punto de entrada.
- `wiki/log.md` y `wiki/conventions.md`: sin entrantes. Corrección aplicada: se enlazan desde `wiki/index.md` (sección Meta) para hacerlas visibles en el grafo.
- `wiki/sources/Karpathy LLM Wiki Plugin.md`: solo 1 entrante (índice). Sin salidas en cuerpo ni frontmatter. Marcado como pendiente de enriquecer con versión/fecha del plugin cuando exista fuente (`requires_validation` granular).
- `wiki/sources/OpenCode oficial.md`: sin salidas. Pendiente de enriquecer sin inventar.
- `wiki/analyses/Separación entre hecho e hipótesis.md`: no tenía salidas. Corrección aplicada: ahora enlaza a [[Estado observable]], [[Evidencia]], [[Proveniencia]], [[Hipótesis]], [[Validación]], [[Causa raíz]] y [[Flujo de diagnóstico]].
- `wiki/concepts/Seguridad funcional.md`: sin salidas en cuerpo (solo frontmatter). Aceptado: el cuerpo describe restricción; las fuentes están en frontmatter.

## 3. Frontmatter

- `wiki/index.md`: usa `type: index`, fuera del enum de `AGENTS.md` (`concept|entity|source|analysis|rule`). Se conserva por ser índice y se añade `status: proposed` para acercarlo a la convención. No se fuerza un tipo incorrecto.
- `wiki/conventions.md` y `wiki/log.md`: sin frontmatter. Se conservan así por ser páginas meta, y se documenta aquí la excepción.
- `wiki/sources/*.md`: usan campo `url:` en lugar de `sources:`. Se conserva `url:` para no romper nada; cuando se edite cada fuente se añadirá `domain: diagnostico-celda-automatizada`.
- `wiki/concepts/Knowledge Graph.md`, `wiki/entities/Obsidian.md`, `wiki/entities/OpenCode.md`: usan `domain: knowledge-management`. Desviación justificable y documentada (infraestructura de conocimiento, no celda física).

## 4. Contradicciones

- No se encontraron contradicciones. El vault es coherente en: hipótesis ≠ [[Causa raíz]], no inventar parámetros, conservar [[Proveniencia]], y restricción de [[Seguridad funcional]].

## 5. Hipótesis etiquetadas como verificadas (correcciones aplicadas sin cambiar fuentes)

- `[[Knowledge Graph]]`: el ejemplo `[[PLC]] → coordina → [[Sistema de visión]]` es modelado del proyecto. Corrección: etiquetado explícito como ejemplo de modelado (`proposed`).
- `[[Red industrial]]`: la lista "Conecta potencialmente" es topología propuesta del proyecto, no afirmación del manual Cognex sobre una instalación. Corrección: aclaración en el texto.
- `[[Sistema de visión]]`: "puede comunicarse con [[PLC]]" es capacidad genérica; la página ya indica que bits/handshakes dependen de configuración. Sin cambio de estado; pendiente de detalle por modelo/protocolo con fuente del fabricante (`requires_validation` granular).

## 6. Conceptos faltantes creados (modelado `proposed`, sin datos inventados)

- [[Hipótesis]]: mencionada en 5+ páginas como texto plano. Nueva página en `wiki/concepts/`.
- [[Síntoma]]: paso 1 del [[Flujo de diagnóstico]]. Nueva página en `wiki/concepts/`.
- [[Validación]]: cadena hipótesis → validación → [[Causa raíz]] en `wiki/overview.md`. Nueva página en `wiki/concepts/`.
- Enlaces actualizados: [[Diagnóstico de fallas]] y [[Sistema experto]] ahora enlazan a [[Hipótesis]] y [[Validación]].

## 7. Fuentes faltantes (no inventadas, pendientes de ingesta)

- Tutorial YouTube de `raw/FUENTES.md` ("segundo cerebro"): referenciado en `raw/` pero sin página en `wiki/sources/`, sin entrada en índice/log. Pendiente de flujo INGEST con autor/fecha/versión/URL verificados.
- ISO 10218-2:2025: mencionada en [[Seguridad funcional]] y [[ISO 10218-1 2025]] como texto plano. Sin página propia porque no hay ingesta con URL/versión en `raw/`. No crear hasta disponer de fuente.
- Manuales/versiones concretas de PLC, HMI, red y cámara (modelo, firmware, páginas del manual) para convertir el grafo inicial en sistema experto operativo. Ver sección 8.

## 8. Qué falta para un sistema experto operativo (sin inventar)

1. Modelo concreto de [[PLC]] (fabricante, CPU, firmware) + manual y mapa de alarmas.
2. Modelo concreto de [[Robot industrial]] (manual e-Series/UR-Series aplicable, versión, páginas de robot stops y diagnóstico).
3. Modelo concreto de [[Sistema de visión]] (In-Sight 3800: versión de manual, configuración de adquisición/disparo, protocolos habilitados).
4. [[HMI]] concreta (lista de alarmas y textos reales).
5. [[Red industrial]] concreta (topología, protocolos habilitados, capturas de diagnóstico).
6. Evaluación de riesgos de la aplicación y funciones de [[Seguridad funcional]] implementadas.
7. Primeras reglas R-XXX instanciadas desde [[Plantilla de regla de diagnóstico]] con prueba discriminante y fuente por regla.
8. Registro de [[Evidencia]] real de máquina con [[Proveniencia]] (fecha, fuente, instrumento).

## Relaciones

- revisa → [[Knowledge Graph]]
- aplica → [[Separación entre hecho e hipótesis]]
- actualiza → [[Flujo de diagnóstico]] y [[Modelo de relaciones]]
- propone → [[Hipótesis]], [[Síntoma]], [[Validación]]
