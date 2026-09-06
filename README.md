# Claude Certification Prep

Guía de estudio en español para preparar **Claude Certified Architect – Foundations (CCAR-F)** y, posteriormente, **Claude Certified Architect – Professional (CCAR-P)**.

## Objetivo

Este repositorio tiene dos objetivos:

1. prepararme seriamente para aprobar primero **CCAR-F** y luego **CCAR-P**;
2. construir en paralelo una guía/“escuelita” reutilizable para otras personas que quieran hacer la misma certificación.

La preparación no se limita a completar cursos: combina blueprint oficial, documentación, práctica, preguntas, revisión de errores y consolidación progresiva.

## Idioma

- Las explicaciones, ejercicios y notas se escriben en **español**.
- Los conceptos, nombres de productos, parámetros, archivos, comandos y términos relevantes se conservan también en su **idioma original (English)**.
- En la primera aparición de un concepto importante se prioriza el término original; por ejemplo: **context window (ventana de contexto)**, **tool use (uso de herramientas)**, **agentic loop (bucle agéntico)**.
- No se traducen nombres propios de productos, APIs, archivos, parámetros o comandos.
- El objetivo es aprender los términos tal como aparecerán en el examen, que actualmente se rinde en English.

---

# CCAR-F — Claude Certified Architect – Foundations

## Datos oficiales del examen

> Datos revisados contra la página oficial de Anthropic Academy y el Exam Guide vigente al 2026-09-06. El programa puede cambiar, por lo que se revisará nuevamente antes de registrar el examen.

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

El resultado utiliza un **scaled score**.

**720/1000 NO debe interpretarse automáticamente como “72% de respuestas correctas”.**

Anthropic establece un puntaje escalado de 720 como corte de aprobación. El score report informa además desempeño por dominio.

## Qué valida CCAR-F

La certificación valida la capacidad de tomar decisiones informadas sobre **trade-offs** al implementar soluciones reales con Claude, utilizando principalmente conceptos y herramientas asociadas a:

- **Claude API**;
- **Claude Agent SDK**;
- **Claude Code**;
- **Model Context Protocol (MCP)**.

El examen no busca solamente conocimiento conceptual. Las preguntas están contextualizadas en escenarios y requieren decisiones sobre arquitectura, configuración, confiabilidad y trade-offs de producción.

---

# CCAR-F Exam Blueprint

| Domain | Peso |
|---|---:|
| **1. Agentic Architecture & Orchestration** | **27%** |
| **2. Tool Design & MCP Integration** | **18%** |
| **3. Claude Code Configuration & Workflows** | **20%** |
| **4. Prompt Engineering & Structured Output** | **20%** |
| **5. Context Management & Reliability** | **15%** |
| **Total** | **100%** |

## Resumen del temario

### Domain 1 — Agentic Architecture & Orchestration — 27%

Incluye `agentic loops`, multi-agent orchestration, subagents, handoffs, Agent SDK hooks, task decomposition y session state/resumption.

### Domain 2 — Tool Design & MCP Integration — 18%

Incluye tool interface design, structured errors, tool choice/distribution, MCP server integration y built-in tools.

### Domain 3 — Claude Code Configuration & Workflows — 20%

Incluye `CLAUDE.md`, skills/custom commands, path-specific rules, Plan Mode, iterative refinement y CI/CD integration.

### Domain 4 — Prompt Engineering & Structured Output — 20%

Incluye explicit criteria, few-shot prompting, structured output mediante tool use, validation/retry loops, batch strategies y multi-pass/multi-instance review.

### Domain 5 — Context Management & Reliability — 15%

Incluye context window management, escalation/ambiguity, error propagation, codebase exploration/context degradation, human review/confidence calibration e information provenance.

> El detalle completo de los task statements y el recorrido está en [ROADMAP.md](ROADMAP.md).

---

# Official preparation path

La página oficial específica de CCAR-F indica actualmente que estos cursos gratuitos de **Anthropic Academy** cubren los dominios del examen y que la mayoría de candidatos los completa en este orden:

1. **AI Fluency: Framework & Foundations** — `COMPLETO`
2. **Claude 101** — `EN ESTUDIO`
3. **Building with the Claude API** — `PENDIENTE`
4. **Claude with Amazon Bedrock** — `PENDIENTE`
5. **Claude on Google Cloud** — `PENDIENTE`
6. **Introduction to Model Context Protocol** — `PENDIENTE`
7. **Claude Code in Action** — `PENDIENTE`

Los cursos **no son los dominios del examen**. Son una ruta pedagógica oficial que luego complementamos con cobertura exhaustiva del blueprint.

Nuestra ruta completa es:

```text
Official courses
→ labs cuando corresponda
→ cobertura exhaustiva de task statements
→ dominio por dominio
→ mocks
→ examen
```

---

# Metodología — `Official-first`

Por defecto seguimos este orden:

1. **Exam Guide / blueprint oficial**.
2. **Anthropic Academy**.
3. **Documentación oficial de Anthropic**.
4. **Hands-on labs** cuando el tema necesita experiencia práctica.
5. **Fuentes externas** sólo para cubrir gaps concretos o explicar algo significativamente mejor.
6. **Preguntas y mocks** para practicar razonamiento y detectar debilidades.

No usamos un curso externo completo como backbone de la preparación por defecto.

Además, distinguimos entre:

- cursos de orientación/fundamentos, que pueden requerir sólo resumen, conceptos y comprobación corta;
- cursos técnicos, que normalmente requieren documentación + labs + preguntas;
- task statements del examen, que requieren cobertura exhaustiva.

El criterio exacto está documentado en [STUDY_PROTOCOL.md](STUDY_PROTOCOL.md).

---

# AI Fluency — cerrado

**AI Fluency: Framework & Foundations** está `COMPLETO`.

Su aporte a CCAR-F es principalmente conceptual. Anthropic lo incluye oficialmente dentro del path de preparación, pero el **4D Framework** no constituye por sí mismo un dominio ni un task statement del blueprint.

Conceptos conservados:

- **Delegation**;
- **Description**;
- **Discernment**;
- **Diligence**;
- **Automation**;
- **Augmentation**;
- **Agency**.

Clasificación del proyecto:

- **valor directo para el examen:** bajo;
- **valor conceptual:** moderado;
- **lab adicional:** no requerido;
- **recomendación:** comprenderlo y conservarlo, sin sobreestudiarlo.

Material completo: [CCAR-F/00-preparacion/01-ai-fluency/README.md](CCAR-F/00-preparacion/01-ai-fluency/README.md).

---

# Fuente de verdad

La página específica de **Claude Certified Architect – Foundations** y el **Exam Guide oficial de Anthropic** definen el alcance del examen.

Los cursos, documentación, repositorios, artículos y mocks son material de preparación y deben evaluarse contra ese blueprint.

Una fuente comunitaria nunca reemplaza al blueprint oficial.

## Enlaces oficiales

- [Claude Certified Architect – Foundations — Anthropic Academy](https://anthropic-partners.skilljar.com/claude-certified-architect-foundations-certification)
- [Anthropic Certification FAQ](https://anthropic-partners.skilljar.com/page/faq-certifications)
- [Claude Certification Exam Prep Courses](https://anthropic-partners.skilljar.com/page/claude-certification-exam-prep-courses)
- [AI Fluency — Anthropic](https://www.anthropic.com/ai-fluency)

---

# Documentos del repositorio

- [ROADMAP.md](ROADMAP.md) — official path, blueprint y recorrido completo.
- [PROGRESS.md](PROGRESS.md) — progreso actual y próximo paso.
- [STUDY_PROTOCOL.md](STUDY_PROTOCOL.md) — metodología y criterio de cierre según el tipo de bloque.
- [DIVERGENCES.md](DIVERGENCES.md) — cambios, inconsistencias y decisiones pedagógicas relevantes.

## Estado actual

**Certificación actual:** CCAR-F  
**Último curso cerrado:** AI Fluency: Framework & Foundations  
**Tema actual:** Claude 101  
**Estado:** `EN ESTUDIO`

No se desarrolla todavía contenido profundo de Claude 101: el siguiente paso es estudiarlo y cerrarlo aplicando el protocolo correspondiente.
