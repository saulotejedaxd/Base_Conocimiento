---
type: analysis
status: proposed
domain: diagnostico-celda-automatizada
last_verified: 2026-09-16
sources:
  - "[[Karpathy LLM Wiki]]"
---

# Diagnóstico de fallas en una celda de inspección automatizada

Este Knowledge Graph organiza conocimiento para apoyar el diagnóstico de una [[Celda de inspección automatizada]].

## Núcleo

Una celda puede integrar:
- [[PLC]]
- [[Robot industrial]]
- [[Sistema de visión]]
- [[HMI]]
- [[Red industrial]]
- funciones de [[Seguridad funcional]]

El [[Sistema experto]] no sustituye las comprobaciones del equipo. Organiza [[Evidencia]], aplica [[Reglas de producción]] y genera hipótesis de [[Diagnóstico de fallas]].

## Cadena conceptual

[[Estado observable]] → [[Evidencia]] → [[Reglas de producción]] → [[Inferencia]] → hipótesis → validación → [[Causa raíz]]

## Principio

La salida del sistema debe conservar [[Proveniencia]] y nivel de certeza. Una hipótesis no debe etiquetarse como [[Causa raíz]] hasta haber sido validada.

## Navegación

- Para arquitectura: [[Arquitectura del sistema experto]]
- Para relaciones: [[Modelo de relaciones]]
- Para procedimiento: [[Flujo de diagnóstico]]
- Para calidad epistemológica: [[Separación entre hecho e hipótesis]]
