---
type: analysis
status: proposed
domain: diagnostico-celda-automatizada
last_verified: 2026-09-16
---

# Arquitectura del sistema experto

## Entrada
Estados de:
- [[PLC]]
- [[Robot industrial]]
- [[Sistema de visión]]
- [[HMI]]
- [[Red industrial]]

## Capa de conocimiento
- [[Knowledge Graph]]
- [[Reglas de producción]]
- historial técnico;
- fuentes con [[Proveniencia]].

## Motor lógico
[[Inferencia]]

## Salida
- hipótesis priorizadas por evidencia disponible;
- pruebas sugeridas;
- evidencia faltante;
- relación con páginas técnicas;
- estado `requires_validation` mientras no exista confirmación.

## Restricción
La arquitectura no debe transformar ausencia de evidencia en evidencia de ausencia.
