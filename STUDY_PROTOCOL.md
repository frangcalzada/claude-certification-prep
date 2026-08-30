# Protocolo de estudio

Este documento define cómo se trabaja cada tema de CCAR-F y, posteriormente, de CCAR-P.

## Principio general

Se estudia **un tema a la vez**. No se desarrolla el tema siguiente hasta que el actual cumpla el criterio de finalización.

## Jerarquía de fuentes

1. **Exam Guide / blueprint oficial de Anthropic** — define qué puede ser evaluado.
2. **Documentación oficial de Anthropic** — fuente técnica principal.
3. **Cursos oficiales de Anthropic** — explicación y práctica guiada.
4. **Fuentes externas de alta calidad** — cursos, repositorios, artículos, labs o videos que agreguen profundidad o una explicación mejor.
5. **Mocks / preguntas comunitarias** — práctica; nunca fuente de verdad por sí sola.

Si dos fuentes discrepan, se registra en `DIVERGENCES.md` y se prioriza la fuente oficial más reciente y específica.

## Idioma y terminología

El material explicativo se escribe en español, pero los términos relevantes se mantienen en inglés para facilitar el reconocimiento durante el examen.

Ejemplos:

- **tool use (uso de herramientas)**
- **context window (ventana de contexto)**
- **agentic loop (bucle agéntico)**
- **structured output (salida estructurada)**
- `CLAUDE.md`, **hooks**, **skills**, **subagents**, **MCP server**, **MCP client**

No se traducen nombres propios de productos, APIs, archivos, comandos o parámetros.

## Flujo obligatorio por tema

### 1. Objetivo de examen

- Identificar el `task statement` o conocimiento del blueprint al que corresponde.
- Explicar qué se espera poder decidir, implementar o reconocer.

### 2. Material oficial

- Exam Guide relevante.
- Documentación oficial.
- Curso/video oficial si aporta contenido al tema.
- Registrar exactamente qué recurso debe consumir el estudiante.

### 3. Complemento

Agregar al menos una fuente adicional cuando aporte valor real, por ejemplo:

- explicación más intuitiva;
- comparación arquitectónica;
- implementación hands-on;
- visualización;
- casos límite;
- preguntas de mejor calidad.

No se agrega material externo únicamente para acumular recursos.

### 4. Explicación

Generar material propio en español con terminología clave en inglés:

- conceptos;
- funcionamiento;
- cuándo utilizarlo;
- cuándo no utilizarlo;
- trade-offs;
- errores comunes;
- relación con otros temas;
- puntos que pueden inducir a error en el examen.

### 5. Práctica

Cada tema debe tener una actividad práctica proporcional a su importancia:

- ejercicio conceptual;
- modificación de prompts/configuración;
- implementación de código;
- laboratorio;
- debugging;
- decisión arquitectónica.

El estudiante debe realizarla antes de cerrar el tema.

### 6. Preguntas tipo examen

Debe existir una batería de preguntas situacionales con:

- opciones plausibles;
- respuesta correcta;
- explicación de por qué es correcta;
- explicación de por qué las demás no lo son;
- referencia conceptual asociada.

El objetivo no es memorizar respuestas sino aprender a razonar los trade-offs.

### 7. Cierre

Antes de avanzar:

- [ ] Material oficial revisado.
- [ ] Fuente complementaria útil revisada.
- [ ] Conceptos comprendidos y documentados.
- [ ] Práctica realizada.
- [ ] Preguntas tipo examen respondidas y revisadas.
- [ ] Errores o dudas aclarados.
- [ ] Material consolidado en GitHub.
- [ ] `PROGRESS.md` actualizado.

Sólo entonces el tema pasa a **COMPLETO**.

## Estados

- `PENDIENTE`
- `EN ESTUDIO`
- `PRACTICA PENDIENTE`
- `PREGUNTAS PENDIENTES`
- `COMPLETO`

## Regla para CCAR-P

No se comienza la preparación formal de CCAR-P hasta completar el recorrido de CCAR-F bajo este protocolo.
