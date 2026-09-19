---
type: analysis
status: proposed
domain: diagnostico-celda-automatizada
last_verified: 2026-09-16
---

# Modelo de relaciones

## Relaciones principales

[[Celda de inspección automatizada]]
- contiene → [[PLC]]
- contiene → [[Robot industrial]]
- contiene → [[Sistema de visión]]
- contiene → [[HMI]]
- utiliza → [[Red industrial]]
- debe respetar → [[Seguridad funcional]]

[[Sistema experto]]
- consulta → [[Knowledge Graph]]
- procesa → [[Evidencia]]
- aplica → [[Reglas de producción]]
- ejecuta → [[Inferencia]]
- genera → hipótesis de [[Diagnóstico de fallas]]

[[Evidencia]]
- proviene de → [[Estado observable]]
- conserva → [[Proveniencia]]
- puede confirmar → [[Causa raíz]]
