# Prompt listo para OpenCode

Administra este proyecto como una wiki técnica persistente.

Lee primero `AGENTS.md`, `wiki/index.md`, `wiki/conventions.md` y `wiki/log.md`.

Tu dominio es el diagnóstico de fallas en una celda de inspección automatizada.

Reglas:
- no inventes datos;
- `raw/` es inmutable;
- toda afirmación técnica debe tener fuente o quedar como `requires_validation`;
- actualiza páginas existentes antes de crear duplicados;
- usa `[[wikilinks]]`;
- conserva contradicciones y versiones;
- después de cada ingesta actualiza `wiki/index.md` y agrega una entrada a `wiki/log.md`;
- una hipótesis nunca debe presentarse como causa raíz confirmada.

Primera tarea:
1. Ejecuta un lint lógico del vault.
2. Revisa enlaces rotos, páginas huérfanas y conceptos sin definición.
3. No cambies información verificada sin una fuente mejor.
4. Propón, sin inventar, qué fuentes técnicas faltan para convertir este grafo inicial en un sistema experto operativo.
