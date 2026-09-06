# Roadmap CCAR-F

Este roadmap separa explícitamente **recursos de preparación** de **dominios evaluados en el examen**. La ruta pedagógica y el Exam Blueprint se complementan, pero no son lo mismo.

## A. Official preparation path

La página oficial específica de **Claude Certified Architect – Foundations (CCAR-F)** indica actualmente que los siguientes cursos gratuitos de Anthropic Academy cubren los dominios del examen y que la mayoría de candidatos los completa en este orden:

1. **AI Fluency: Framework & Foundations** — Level 100 — `COMPLETO`
2. **Claude 101** — Level 100 — `EN ESTUDIO`
3. **Building with the Claude API** — Level 100–200 — `PENDIENTE`
4. **Claude with Amazon Bedrock** — Level 100–200 — `PENDIENTE`
5. **Claude on Google Cloud** — Level 100–200 — `PENDIENTE`
6. **Introduction to Model Context Protocol** — Level 200 — `PENDIENTE`
7. **Claude Code in Action** — Level 200 — `PENDIENTE`

Estos cursos **no sustituyen los task statements oficiales** y tampoco son prerequisitos formales para rendir el examen.

### Regla del proyecto

La página oficial específica de CCAR-F define el **path base** de preparación.

Cursos más nuevos asociados a otras certificaciones —por ejemplo `Claude Certified Developer – Foundations`, `Claude Certified Associate – Foundations` o `Claude Certified Architect – Professional`— no se agregan automáticamente a este recorrido.

Un recurso oficial adicional puede incorporarse como **complemento** cuando cubra un gap concreto.

---

## B. CCAR-F Exam Blueprint

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

---

## C. Ruta pedagógica completa

Nuestro recorrido no termina al completar videos o cursos.

```text
Official courses
→ labs cuando corresponda
→ cobertura exhaustiva de los task statements
→ dominio por dominio
→ mocks
→ examen
```

### Estrategia `Official-first`

Por defecto utilizamos esta prioridad:

1. **Exam Guide / blueprint oficial**.
2. **Anthropic Academy**.
3. **Documentación oficial de Anthropic**.
4. **Hands-on labs** cuando el tema necesite experiencia práctica.
5. **Fuente externa** sólo cuando cubra un gap concreto o explique algo significativamente mejor.
6. **Preguntas y mocks** para practicar razonamiento y detectar debilidades.

No vamos a comprar ni seguir un curso externo completo como backbone de la preparación por defecto.

En particular, actualmente **no se recomienda el curso general de Udemy de Vasco Patrício como eje de la preparación**. Si más adelante aparece un gap específico —por ejemplo MCP, Agent SDK, RAG, evals o Claude Code— investigaremos el mejor recurso puntual para ese problema.

---

## D. Consolidación CCAR-F

Una vez completados los task statements de los cinco dominios:

1. revisión cruzada de dominios;
2. preguntas mixtas;
3. mocks por dominio;
4. mocks completos;
5. error log;
6. refuerzo dirigido;
7. simulación final en condiciones de examen.

---

## E. CCAR-P

Sólo después de completar CCAR-F se creará y ejecutará el roadmap detallado de **Claude Certified Architect – Professional (CCAR-P)** con la misma filosofía de trabajo.

## Nota de mantenimiento

Los porcentajes, cursos recomendados y task statements deben revisarse contra la versión vigente del Exam Guide y la Certification Page antes de cerrar cada dominio. Cualquier cambio o diferencia relevante se registra en `DIVERGENCES.md`.
