# Divergences / inconsistencias entre fuentes

Este archivo registra discrepancias, cambios de versión, ambigüedades y decisiones pedagógicas relevantes detectadas durante la preparación.

## Reglas

- La fuente oficial más reciente y específica tiene prioridad.
- Un mock, repositorio o curso externo nunca se toma como fuente de verdad por sí solo.
- Si una respuesta depende de comportamiento que cambió entre versiones de Claude, Claude Code, MCP o la documentación, se registra la fecha y la fuente.
- La página específica de **Claude Certified Architect – Foundations (CCAR-F)** y su Exam Guide definen nuestro alcance actual.

## Registro

### 2026-09-06 — Revalidación de información oficial CCAR-F

**Hallazgo:** se volvió a contrastar el material del repositorio con la información oficial vigente de Anthropic Academy para **Claude Certified Architect – Foundations (CCAR-F)**.

Se mantiene vigente el núcleo ya documentado:

- 60 preguntas;
- 120 minutos;
- formato `multiple choice` y `multiple response`;
- English;
- USD 125 por intento;
- passing score 720 en escala 100–1000;
- validez 12 meses;
- cinco dominios con pesos 27% / 18% / 20% / 20% / 15%;
- siete cursos base en el path oficial.

**Decisión:** no modificar estos datos salvo cambios futuros de la página específica de CCAR-F o del Exam Guide.

**Nota importante:** `720/1000` es un **scaled score** y no debe documentarse como “72% de respuestas correctas”.

---

### 2026-09-06 — AI Fluency vs blueprint

**Hallazgo:** `AI Fluency: Framework & Foundations` está oficialmente recomendado dentro del path de preparación de CCAR-F, pero el **4D Framework** no aparece como dominio ni como task statement independiente del Exam Blueprint.

Los conceptos centrales del curso son:

- `Delegation`;
- `Description`;
- `Discernment`;
- `Diligence`.

También introduce los modos `Automation`, `Augmentation` y `Agency`.

**Decisión:**

- completar el curso oficial;
- conservar sus conceptos principales;
- documentar su relación indirecta con temas del examen;
- no sobreestudiarlo;
- no crear un laboratorio técnico artificial.

**Evaluación para este proyecto:**

- valor directo para el examen: **bajo**;
- valor como framework conceptual: **moderado**;
- necesidad de laboratorio adicional: **no**;
- necesidad de memorizar terminología: **baja/moderada**.

**Impacto:** `AI Fluency` puede cerrarse como curso de fundamentos sin aplicar automáticamente el protocolo exhaustivo reservado para task statements y temas técnicos.

---

### 2026-09-06 — Official-first vs curso externo integral

**Hallazgo:** inicialmente se consideró utilizar un curso general de Udemy como backbone complementario de la preparación.

Después de revisar la amplitud de la ruta oficial, el blueprint y la calidad/comentarios de alternativas externas, no existe actualmente una razón suficiente para introducir un curso integral externo como requisito base.

**Decisión:** adoptar estrategia **`Official-first`**:

1. Exam Guide / blueprint oficial.
2. Anthropic Academy.
3. Documentación oficial de Anthropic.
4. Hands-on labs cuando correspondan.
5. Fuente externa sólo para un gap concreto o una explicación significativamente mejor.
6. Preguntas y mocks.

Actualmente **no se utiliza el curso de Udemy de Vasco Patrício como backbone**.

Si aparece un gap específico —por ejemplo MCP, Agent SDK, RAG, evals o Claude Code— se investigará el mejor recurso puntual para ese tema.

---

### 2026-09-06 — Certificaciones Foundations diferentes

**Hallazgo:** el término `Foundations` aparece en varias certificaciones de Anthropic y puede provocar búsquedas o recomendaciones incorrectas.

Mantener diferenciadas:

- **Claude Certified Architect – Foundations (CCAR-F)**;
- **Claude Certified Developer – Foundations**;
- **Claude Certified Associate – Foundations**.

**Decisión:** el objetivo actual del repositorio es exclusivamente **Claude Certified Architect – Foundations (CCAR-F)**. No se incorporan automáticamente cursos o blueprints de las otras certificaciones.

---

### 2026-08-30 — Cursos recomendados vs. blueprint del examen

**Hallazgo:** cursos como `AI Fluency: Framework & Foundations` y `Claude 101` son recursos de preparación recomendados por Anthropic, pero no constituyen por sí mismos dominios o task statements del blueprint CCAR-F.

**Decisión:**

- `ROADMAP.md` separa una etapa de preparación oficial de los cinco dominios evaluados.
- Para declarar CCAR-F cubierto, deben completarse los task statements oficiales, independientemente de haber terminado un curso concreto.

**Impacto:** evita confundir el orden pedagógico con el alcance real del examen.

---

### 2026-08-30 — Architect Foundations vs. Associate Foundations

**Hallazgo:** Anthropic publica certificaciones diferentes cuyo nombre incluye `Foundations`.

- **Claude Certified Architect – Foundations**: nuestro objetivo CCAR-F, con dominios técnicos como Agentic Architecture & Orchestration, Claude Code, Prompt Engineering & Structured Output, Tool Design & MCP Integration y Context Management & Reliability.
- **Claude Certified Associate – Foundations**: certificación distinta, con otro blueprint.

**Decisión:** todo el repositorio y la preparación previa a CCAR-P se basan exclusivamente en **Claude Certified Architect – Foundations** salvo que se indique expresamente lo contrario.

**Impacto:** al buscar cursos, guías o mocks se debe verificar el nombre completo de la certificación y su blueprint; `Foundations` por sí solo no identifica el examen correcto.

---

### 2026-08-30 — Lista actual de cursos recomendados para CCAR-F

**Hallazgo:** la página oficial específica de CCAR-F enumera como preparación recomendada:

1. `AI Fluency: Framework & Foundations`
2. `Claude 101`
3. `Building with the Claude API`
4. `Claude with Amazon Bedrock`
5. `Claude on Google Cloud`
6. `Introduction to Model Context Protocol`
7. `Claude Code in Action`

`AI Capabilities and Limitations` no aparece actualmente en esa lista específica de CCAR-F, aunque puede aparecer en otras rutas oficiales.

**Decisión:**

- mantener en `ROADMAP.md` la lista publicada específicamente para CCAR-F;
- mantener `AI Capabilities and Limitations` únicamente como material complementario potencial;
- no omitir automáticamente Bedrock ni Google Cloud;
- evaluar recursos adicionales sólo cuando resuelvan un gap concreto.

**Impacto:** la ruta conserva material útil sin confundir una recomendación oficial específica con una decisión pedagógica propia del proyecto.
