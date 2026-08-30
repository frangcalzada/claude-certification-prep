# Claude Certification Prep

Guía de estudio en español para preparar **Claude Certified Architect – Foundations (CCAR-F)** y, posteriormente, **Claude Certified Architect – Professional (CCAR-P)**.

## Objetivo

El objetivo principal es adquirir los conocimientos y la práctica necesarios para rendir CCAR-F con criterio de examen real y, una vez completado, repetir la misma metodología para CCAR-P.

El repositorio también busca convertirse en una ruta de preparación reutilizable para futuras personas que quieran certificarse.

## Idioma

- Las explicaciones, ejercicios y notas se escriben en **español**.
- Los conceptos, nombres de productos, parámetros, archivos, comandos y términos relevantes se conservan también en su **idioma original (English)**.
- En la primera aparición de un concepto importante se prioriza el término original; por ejemplo: **context window (ventana de contexto)**, **tool use (uso de herramientas)**, **agentic loop (bucle agéntico)**.
- El objetivo es aprender los términos tal como aparecerán en el examen, que actualmente se rinde en inglés.

---

# CCAR-F — Claude Certified Architect – Foundations

## Datos oficiales del examen

> Datos verificados contra la página oficial de Anthropic Academy y el Exam Guide v1.0, efectivo desde julio de 2026. El programa puede cambiar, por lo que se revisará nuevamente antes de registrar el examen.

| Dato | Valor |
|---|---|
| Certificación | **Claude Certified Architect – Foundations** |
| Exam code | **CCAR-F** |
| Rol | Architect |
| Nivel | Foundations |
| Cantidad de preguntas / items | **60** |
| Duración | **120 minutos** (~135 min de seat time) |
| Formato | **Multiple choice** y **multiple response** |
| Estructura | **4 scenarios** seleccionados de un banco de **6** |
| Idioma | **English** |
| Passing score | **720** en una escala de **100–1,000** |
| Precio | **USD 125** por intento |
| Modalidad | Online proctored o Pearson test center |
| Validez de la certificación | **12 meses** |

### Importante sobre el passing score

El resultado utiliza un **scaled score**. Por lo tanto:

**720/1000 NO debe interpretarse automáticamente como “72% de respuestas correctas”.**

Anthropic establece un puntaje escalado de 720 como corte de aprobación. El score report informa además el porcentaje de respuestas correctas por dominio.

## Qué valida CCAR-F

La certificación valida que una persona pueda tomar decisiones informadas sobre **trade-offs** al implementar soluciones reales con Claude, utilizando principalmente:

- **Claude API**;
- **Claude Agent SDK**;
- **Claude Code**;
- **Model Context Protocol (MCP)**.

El examen no busca solamente conocimiento conceptual. Las preguntas están contextualizadas en escenarios realistas y requieren tomar decisiones sobre arquitectura, configuración, confiabilidad y trade-offs de producción.

---

# Exam Blueprint

| Domain | Peso |
|---|---:|
| **1. Agentic Architecture & Orchestration** | **27%** |
| **2. Tool Design & MCP Integration** | **18%** |
| **3. Claude Code Configuration & Workflows** | **20%** |
| **4. Prompt Engineering & Structured Output** | **20%** |
| **5. Context Management & Reliability** | **15%** |
| **Total** | **100%** |

## Temario / Task Statements

El blueprint actual contiene **30 task statements**. Los nombres en inglés se mantienen porque son los términos que debemos reconocer para el examen.

### Domain 1 — Agentic Architecture & Orchestration — 27%

1. **Agentic Loops** — diseño e implementación del ciclo de ejecución de un agente.
2. **Multi-Agent Orchestration** — coordinación de múltiples agentes especializados.
3. **Subagent Invocation and Context Passing** — invocación de subagentes y transferencia explícita de contexto.
4. **Workflow Enforcement and Handoff** — control determinístico de workflows y handoffs.
5. **Agent SDK Hooks** — uso de hooks para controlar o extender el comportamiento de agentes.
6. **Task Decomposition Strategies** — descomposición de tareas complejas.
7. **Session State and Resumption** — persistencia, recuperación y continuación de sesiones.

### Domain 2 — Tool Design & MCP Integration — 18%

1. **Tool Interface Design** — diseño de interfaces y descripciones de tools.
2. **Structured Error Responses** — errores estructurados que permitan recuperación y razonamiento.
3. **Tool Distribution & Tool Choice** — distribución de herramientas y control de selección/invocación.
4. **MCP Server Integration** — integración y configuración de MCP servers/clients.
5. **Built-in Tools** — selección y utilización correcta de herramientas integradas.

### Domain 3 — Claude Code Configuration & Workflows — 20%

1. **CLAUDE.md Hierarchy, Scoping, and Modular Organisation** — jerarquía, alcance y organización del contexto persistente.
2. **Custom Slash Commands and Skills** — creación y uso de comandos y skills reutilizables.
3. **Path-Specific Rules for Conditional Convention Loading** — reglas específicas por path y carga condicional de convenciones.
4. **Plan Mode vs Direct Execution** — cuándo planificar antes de ejecutar y cuándo actuar directamente.
5. **Iterative Refinement Techniques** — desarrollo iterativo y refinamiento mediante feedback.
6. **CI/CD Integration** — integración segura y reproducible de Claude Code en pipelines.

### Domain 4 — Prompt Engineering & Structured Output — 20%

1. **System Prompts with Explicit Criteria** — instrucciones y criterios explícitos en system prompts.
2. **Few-Shot Prompting** — uso de ejemplos para enseñar patrones esperados.
3. **Structured Output with Tool Use** — obtención de outputs estructurados mediante tool use / schemas.
4. **Validation, Retry, and Feedback Loops** — validación determinística, reintentos y feedback.
5. **Batch Processing Strategies** — elección de estrategias batch según costo, latencia y volumen.
6. **Multi-Instance and Multi-Pass Review** — revisión mediante múltiples instancias o múltiples pasadas.

### Domain 5 — Context Management & Reliability — 15%

1. **Context Window Management** — administración eficiente de la context window.
2. **Escalation & Ambiguity Resolution** — manejo de ambigüedad y criterios de escalamiento.
3. **Error Propagation in Multi-Agent Systems** — prevención de propagación de errores entre agentes.
4. **Codebase Exploration & Context Degradation** — exploración de codebases y degradación de contexto en tareas largas.
5. **Human Review & Confidence Calibration** — human-in-the-loop y decisiones basadas en riesgo/confianza.
6. **Information Provenance & Multi-Source Synthesis** — trazabilidad de fuentes y síntesis confiable de múltiples fuentes.

---

# Preparación oficial recomendada por Anthropic

Anthropic no exige completar cursos como requisito formal para presentarse al examen. Sin embargo, la página oficial de CCAR-F indica que los siguientes cursos gratuitos de **Anthropic Academy** cubren los dominios del examen y señala que la mayoría de los candidatos los completa antes de registrarse.

Ruta oficial actualmente publicada:

1. **AI Fluency: Framework & Foundations** — Level 100
2. **Claude 101** — Level 100
3. **Building with the Claude API** — Level 100–200
4. **Claude with Amazon Bedrock** — Level 100–200
5. **Claude on Google Cloud** — Level 100–200
6. **Introduction to Model Context Protocol** — Level 200
7. **Claude Code in Action** — Level 200

## Regla de este proyecto

Que un curso no sea obligatorio **no significa que lo descartemos**.

Para cada recurso oficial recomendado evaluaremos:

- qué conocimientos del blueprint cubre;
- si aporta fundamentos necesarios para entender temas posteriores;
- si conviene completarlo entero o sólo determinados módulos;
- qué práctica adicional necesitamos para transformar la teoría en conocimiento aplicable.

Por lo tanto, cursos introductorios como **AI Fluency** y **Claude 101** forman parte de nuestra preparación cuando aportan las bases necesarias, aunque sus nombres no sean task statements del examen.

Los cursos específicos de plataforma, como **Claude with Amazon Bedrock** y **Claude on Google Cloud**, se evaluarán cuando corresponda estudiar model/deployment platform selection. No se omitirán automáticamente ni se harán de forma mecánica: primero determinaremos qué partes son relevantes para CCAR-F.

---

# Fuente de verdad

El **Exam Guide oficial de Anthropic** define el alcance del examen. Los cursos, documentación, repositorios, artículos y mocks son material de preparación y deben evaluarse contra ese blueprint.

Prioridad general:

1. **Anthropic Exam Guide / Certification page**
2. **Anthropic Documentation / Anthropic Academy**
3. **Especificaciones oficiales relacionadas**, por ejemplo MCP
4. Recursos externos de alta calidad
5. Mocks y material comunitario

Una fuente comunitaria nunca reemplaza al blueprint oficial.

## Enlaces oficiales

- [Claude Certified Architect – Foundations — Anthropic Academy](https://anthropic-partners.skilljar.com/claude-certified-architect-foundations-certification)
- [Anthropic Certification FAQ](https://anthropic-partners.skilljar.com/page/faq-certifications)
- [Claude Certification Exam Prep Courses](https://anthropic-partners.skilljar.com/page/claude-certification-exam-prep-courses)

---

# Documentos del repositorio

- [STUDY_PROTOCOL.md](STUDY_PROTOCOL.md) — metodología y criterio de finalización de cada tema.
- [ROADMAP.md](ROADMAP.md) — roadmap completo del CCAR-F.
- [PROGRESS.md](PROGRESS.md) — progreso actual.
- [DIVERGENCES.md](DIVERGENCES.md) — inconsistencias o cambios detectados entre fuentes.

## Estado

**Certificación actual:** CCAR-F  
**Tema actual:** AI Fluency: Framework & Foundations  
**Regla:** se trabaja un tema a la vez; no se avanza hasta cerrar teoría, fuentes, práctica, preguntas y documentación.
