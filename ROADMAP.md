# Roadmap CCAR-F

Este roadmap separa claramente **recursos de preparación** de **dominios evaluados en el examen**.

## Etapa A — Preparación oficial recomendada por Anthropic

La página oficial de CCAR-F indica que los siguientes cursos gratuitos de Anthropic Academy cubren los dominios del examen y que la mayoría de los candidatos los completa antes de registrarse.

1. **AI Fluency: Framework & Foundations** — Level 100
2. **Claude 101** — Level 100
3. **Building with the Claude API** — Level 100–200
4. **Claude with Amazon Bedrock** — Level 100–200
5. **Claude on Google Cloud** — Level 100–200
6. **Introduction to Model Context Protocol** — Level 200
7. **Claude Code in Action** — Level 200

Estos cursos **no sustituyen los task statements oficiales** y tampoco son prerequisitos formales para rendir el examen.

### Regla del proyecto

- Los cursos introductorios como **AI Fluency** y **Claude 101** se estudiarán cuando aporten fundamentos necesarios, aunque no sean task statements del blueprint.
- **Building with the Claude API**, **Introduction to MCP** y **Claude Code in Action** se consideran especialmente relevantes para construir la base técnica.
- Los cursos específicos de plataforma (**Amazon Bedrock** y **Google Cloud**) se evaluarán cuando lleguemos a selección de plataforma / deployment. Se estudiarán las partes relevantes para CCAR-F y se decidirá entonces si conviene completarlos íntegramente.
- **AI Capabilities and Limitations** puede utilizarse como complemento oficial si aporta a un tema, pero a fecha 2026-08-30 no figura en la lista de cursos recomendados publicada específicamente para CCAR-F; sí aparece como prerequisito recomendado en otras rutas como CCAR-P.
- Cuando un curso incluya contenido ajeno al examen se marcará como **complementario**, no como requisito artificial.

## Etapa B — Blueprint CCAR-F

### Domain 1 — Agentic Architecture & Orchestration — 27%

Task statements:

1. Agentic Loops
2. Multi-Agent Orchestration
3. Subagent Invocation and Context Passing
4. Workflow Enforcement and Handoff
5. Agent SDK Hooks
6. Task Decomposition Strategies
7. Session State and Resumption

### Domain 2 — Tool Design & MCP Integration — 18%

Task statements:

1. Tool Interface Design
2. Structured Error Responses
3. Tool Distribution & Tool Choice
4. MCP Server Integration
5. Built-in Tools

### Domain 3 — Claude Code Configuration & Workflows — 20%

Task statements:

1. CLAUDE.md Hierarchy, Scoping, and Modular Organisation
2. Custom Slash Commands and Skills
3. Path-Specific Rules for Conditional Convention Loading
4. Plan Mode vs Direct Execution
5. Iterative Refinement Techniques
6. CI/CD Integration

### Domain 4 — Prompt Engineering & Structured Output — 20%

Task statements:

1. System Prompts with Explicit Criteria
2. Few-Shot Prompting
3. Structured Output with Tool Use
4. Validation, Retry, and Feedback Loops
5. Batch Processing Strategies
6. Multi-Instance and Multi-Pass Review

### Domain 5 — Context Management & Reliability — 15%

Task statements:

1. Context Window Management
2. Escalation & Ambiguity Resolution
3. Error Propagation in Multi-Agent Systems
4. Codebase Exploration & Context Degradation
5. Human Review & Confidence Calibration
6. Information Provenance & Multi-Source Synthesis

## Etapa C — Consolidación CCAR-F

Una vez completados todos los task statements:

1. revisión cruzada de dominios;
2. preguntas mixtas;
3. mocks completos;
4. error log;
5. refuerzo dirigido;
6. simulación final en condiciones de examen.

## Etapa D — CCAR-P

Sólo después de completar CCAR-F se creará el roadmap detallado de CCAR-P con el mismo protocolo.

## Nota de mantenimiento

Los porcentajes, cursos recomendados y task statements deben revisarse contra la versión vigente del Exam Guide y la Certification Page antes de cerrar cada dominio. Cualquier cambio se registra en `DIVERGENCES.md`.
