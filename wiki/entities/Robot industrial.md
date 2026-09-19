---
type: entity
status: verified
domain: diagnostico-celda-automatizada
last_verified: 2026-09-16
sources:
  - "[[ISO 10218-1 2025]]"
  - "[[Universal Robots e-Series]]"
---

# Robot industrial

Manipulador programable integrado a una aplicación industrial.

## Relaciones
- forma parte de una [[Celda de inspección automatizada]];
- puede posicionar piezas o sensores respecto a un [[Sistema de visión]];
- intercambia estados con [[PLC]];
- está sujeto a requisitos de [[Seguridad funcional]].

## Nota de seguridad

Las acciones de diagnóstico no deben anular ni automatizar indebidamente el reconocimiento de paros de seguridad o fallas. Consultar [[Universal Robots e-Series]] y la evaluación de riesgos de la aplicación.
