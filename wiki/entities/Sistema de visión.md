---
type: entity
status: verified
domain: diagnostico-celda-automatizada
last_verified: 2026-09-16
sources:
  - "[[Cognex In-Sight 3800]]"
---

# Sistema de visión

Sistema que adquiere imágenes y aplica herramientas de inspección para obtener resultados utilizables por la automatización.

## Relaciones
- recibe una condición de adquisición o disparo;
- produce resultados de inspección;
- puede comunicarse con [[PLC]] mediante protocolos industriales;
- genera [[Estado observable]] y [[Evidencia]] para [[Diagnóstico de fallas]].

## Alcance

La semántica exacta de bits, handshakes y resultados depende de la configuración y documentación del equipo.
