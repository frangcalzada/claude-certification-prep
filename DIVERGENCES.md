# Divergences / inconsistencias entre fuentes

Este archivo registra discrepancias, cambios de versión o ambigüedades detectadas durante la preparación.

## Reglas

- La fuente oficial más reciente y específica tiene prioridad.
- Un mock, repositorio o curso externo nunca se toma como fuente de verdad por sí solo.
- Si una respuesta depende de comportamiento que cambió entre versiones de Claude, Claude Code, MCP o la documentación, se registra la fecha y la fuente.

## Registro

### 2026-08-30 — Cursos recomendados vs. blueprint del examen

**Hallazgo:** cursos como `AI Fluency: Framework & Foundations` y `Claude 101` son recursos de preparación recomendados por Anthropic, pero no constituyen por sí mismos dominios o task statements del blueprint CCAR-F.

**Decisión:**

- `ROADMAP.md` separa una etapa de base recomendada de los cinco dominios evaluados.
- Para declarar CCAR-F cubierto, deben completarse los task statements oficiales, independientemente de haber terminado un curso concreto.

**Impacto:** evita confundir el orden pedagógico con el alcance real del examen.

### 2026-08-30 — Architect Foundations vs. Associate Foundations

**Hallazgo:** Anthropic publica actualmente dos certificaciones diferentes cuyo nombre incluye `Foundations`:

- **Claude Certified Architect – Foundations**: nuestro objetivo CCAR-F, con dominios técnicos como Agentic Architecture & Orchestration, Claude Code, Prompt Engineering & Structured Output, Tool Design & MCP Integration y Context Management & Reliability.
- **Claude Certified Associate – Foundations**: certificación distinta, con otro blueprint orientado a workflow integration, governance, prompting, product/model selection, configuration/knowledge management y troubleshooting.

**Decisión:** todo el repositorio y la preparación previa a CCAR-P se basan exclusivamente en **Claude Certified Architect – Foundations** salvo que se indique expresamente lo contrario.

**Impacto:** al buscar cursos, guías o mocks se debe verificar el nombre completo de la certificación y su blueprint; `Foundations` por sí solo no identifica el examen correcto.

### 2026-08-30 — Lista actual de cursos recomendados para CCAR-F

**Hallazgo:** la página oficial actual de CCAR-F enumera como preparación recomendada: `AI Fluency: Framework & Foundations`, `Claude 101`, `Building with the Claude API`, `Claude with Amazon Bedrock`, `Claude on Google Cloud`, `Introduction to Model Context Protocol` y `Claude Code in Action`.

`AI Capabilities and Limitations` no aparece actualmente en esa lista específica de CCAR-F, aunque sí aparece como prerequisito recomendado en otras rutas oficiales, entre ellas CCAR-P.

**Decisión:**

- Actualizar `ROADMAP.md` con la lista publicada específicamente para CCAR-F.
- Mantener `AI Capabilities and Limitations` disponible como material complementario oficial cuando sume a un tema, sin etiquetarlo falsamente como requisito o curso recomendado específico de CCAR-F.
- Evaluar los cursos de Bedrock y Google Cloud por relevancia cuando lleguemos a selección de plataforma/deployment, en lugar de omitirlos automáticamente.

**Impacto:** la ruta conserva todo material útil sin confundir una recomendación oficial específica con una decisión pedagógica propia del proyecto.
