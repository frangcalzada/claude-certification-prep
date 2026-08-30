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
