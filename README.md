# Knowledge Graph — Diagnóstico de fallas en una celda de inspección automatizada

Este vault está preparado para abrirse directamente en **Obsidian**.

## Objetivo

Construir y mantener una base de conocimiento interconectada para un **sistema experto de diagnóstico de fallas** en una celda de inspección automatizada que puede incluir:

- PLC
- Robot industrial
- Sistema de visión
- HMI
- Red / comunicación industrial
- Seguridad funcional
- Lógica de diagnóstico e inferencia

## Arquitectura

La estructura sigue el patrón LLM-Wiki de Andrej Karpathy:

1. `raw/` — fuentes originales o referencias. El agente **no debe modificarlas**.
2. `wiki/` — conocimiento estructurado, sintetizado y enlazado.
3. `AGENTS.md` — reglas para que un agente como OpenCode administre la wiki.
4. `wiki/index.md` — índice semántico.
5. `wiki/log.md` — historial append-only.
6. `Knowledge Graph.canvas` — vista visual inicial.

## Cómo abrirlo

1. Instala Obsidian.
2. Descomprime esta carpeta.
3. En Obsidian elige **Open folder as vault**.
4. Selecciona `KnowledgeGraph_Diagnostico_Celda_Automatizada`.
5. Abre `wiki/overview.md` o `Knowledge Graph.canvas`.
6. Para ver la red automáticamente usa **Graph view**.

## Regla de confiabilidad

Cada página distingue entre:
- `verified`: información sustentada por fuente.
- `proposed`: estructura o relación propuesta para modelado.
- `requires_validation`: hipótesis que debe comprobarse en la máquina/proceso real.

Nunca convertir una hipótesis en hecho sin evidencia.
