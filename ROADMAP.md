# Roadmap CCAR-F

Este roadmap separa claramente **recursos de preparación** de **dominios evaluados en el examen**.

## Etapa A — Base recomendada por Anthropic

Estos cursos ayudan a construir fundamentos antes de entrar de lleno en el blueprint, pero **no sustituyen los task statements oficiales**.

1. AI Fluency: Framework & Foundations
2. Claude 101
3. Building with the Claude API
4. Introduction to Model Context Protocol (MCP)
5. Claude Code in Action
6. AI Capabilities and Limitations

> Regla del proyecto: se trabajarán sólo en la medida en que aporten conocimiento relevante para CCAR-F. Cuando un curso incluya material ajeno al examen, se marcará como complementario.

## Etapa B — Blueprint CCAR-F

### Domain 1 — Agentic Architecture & Orchestration — 27%

Se estudiarán los task statements oficiales relacionados con:

- **agentic loops**;
- arquitectura single-agent y multi-agent;
- **subagents**;
- task decomposition;
- context passing;
- orchestration;
- handoffs;
- session state / resumption;
- enforcement mediante herramientas y hooks cuando corresponda.

### Domain 2 — Tool Design & MCP Integration — 18%

- diseño de herramientas (**tools**);
- tool schemas;
- structured errors;
- tool selection y boundaries;
- **Model Context Protocol (MCP)**;
- MCP servers y clients;
- built-in tools e integraciones.

### Domain 3 — Claude Code Configuration & Workflows — 20%

- `CLAUDE.md`;
- scopes / hierarchy;
- rules;
- **skills**;
- slash commands;
- **hooks**;
- **subagents**;
- Plan Mode;
- iterative development workflows;
- CI/CD y automatización cuando aplique.

### Domain 4 — Prompt Engineering & Structured Output — 20%

- system prompts;
- explicit instructions / criteria;
- few-shot examples;
- **structured outputs**;
- JSON Schema;
- tool use como mecanismo de salida estructurada;
- validation / retry;
- feedback loops;
- multi-pass workflows;
- Batch API cuando corresponda al blueprint.

### Domain 5 — Context Management & Reliability — 15%

- **context window**;
- context management;
- ambiguity handling;
- escalation;
- context degradation;
- provenance;
- error propagation;
- human-in-the-loop;
- reliability patterns;
- codebase/context exploration;
- multi-source synthesis.

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

Los porcentajes y task statements deben revisarse contra la versión vigente del Exam Guide antes de cerrar cada dominio. Cualquier cambio se registra en `DIVERGENCES.md`.
