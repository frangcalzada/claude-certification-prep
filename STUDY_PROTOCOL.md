# Protocolo de estudio

Este documento define cómo se trabaja cada tema de CCAR-F y, posteriormente, de CCAR-P.

## Principio general

Se estudia **un tema a la vez**. No se desarrolla el siguiente bloque hasta que el actual tenga el nivel de comprensión y experiencia suficiente según su naturaleza.

> No avanzamos simplemente porque terminó un video. Avanzamos cuando el estudiante y ChatGPT consideran que existe comprensión suficiente para el siguiente bloque.

## Jerarquía de fuentes — `Official-first`

1. **Exam Guide / blueprint oficial de Anthropic** — define qué puede ser evaluado.
2. **Anthropic Academy** — ruta de preparación oficial.
3. **Documentación oficial de Anthropic** — fuente técnica principal para profundizar.
4. **Hands-on labs** — cuando el tema requiere experiencia práctica.
5. **Fuentes externas de alta calidad** — sólo cuando cubren un gap concreto o explican algo significativamente mejor.
6. **Mocks / preguntas** — práctica y detección de gaps; nunca fuente de verdad por sí sola.

Si dos fuentes discrepan, se registra en `DIVERGENCES.md` y se prioriza la fuente oficial más reciente y específica.

No se adopta un curso externo integral como backbone de la preparación por defecto.

## Idioma y terminología

El material explicativo se escribe en español, pero los términos relevantes se mantienen en inglés para facilitar el reconocimiento durante el examen.

Ejemplos:

- **tool use (uso de herramientas)**
- **context window (ventana de contexto)**
- **agentic loop (bucle agéntico)**
- **structured output (salida estructurada)**
- `CLAUDE.md`, **hooks**, **skills**, **subagents**, **MCP server**, **MCP client**

No se traducen nombres propios de productos, APIs, archivos, comandos o parámetros.

---

## Tipos de bloque de estudio

No todos los cursos preparatorios requieren el mismo nivel de práctica ni la misma batería de preguntas.

### A. Cursos de orientación / fundamentos

Ejemplos:

- **AI Fluency: Framework & Foundations**;
- **Claude 101**.

Flujo:

```text
Curso oficial
→ resumen
→ conceptos clave
→ comprobación conceptual
→ relación real con CCAR-F
→ GitHub
→ COMPLETO
```

Pueden cerrarse con:

1. completar el curso oficial;
2. elaborar un resumen fiel;
3. conservar los conceptos relevantes;
4. hacer una pequeña comprobación conceptual;
5. documentar su relación real con CCAR-F;
6. consolidar en GitHub.

No se crea un laboratorio técnico artificial sólo para cumplir una plantilla.

La etapa formada por `AI Fluency` + `Claude 101` se denomina en este repositorio **Orientation / Foundations Stage**.

### B. Cursos técnicos / Technical Foundations

Ejemplos:

- **Building with the Claude API**;
- **Claude with Amazon Bedrock**;
- **Claude on Google Cloud**;
- **Introduction to Model Context Protocol**;
- **Claude Code in Action**.

Con `Building with the Claude API` comienza nuestra **Technical Foundations Stage**.

Cuando el contenido necesita experiencia práctica, el flujo recomendado es:

```text
Curso oficial
→ complementar con documentación oficial
→ uno o varios hands-on labs
→ preguntas
→ detectar gaps
→ corregir
→ consolidar en GitHub
→ avanzar
```

La cantidad y dificultad de labs y preguntas debe ser proporcional a la relevancia técnica del tema.

Completar el video/curso **no es suficiente** para marcar un curso técnico como `COMPLETO` si todavía faltan experiencia práctica, conceptos relevantes o gaps detectados.

### C. Task Statements / dominios reales del examen

Estos bloques **sí requieren cobertura exhaustiva**.

Para cada task statement se debe cubrir, cuando aplique:

- teoría;
- documentación oficial;
- complementos cuando realmente sumen;
- práctica hands-on;
- escenarios;
- preguntas tipo examen;
- explicación de distractores;
- revisión de errores;
- trade-offs;
- relación con otros task statements;
- consolidación en GitHub.

El objetivo es poder **decidir, implementar, reconocer y justificar** la opción correcta en escenarios realistas, no sólo repetir definiciones.

---

## Flujo detallado para bloques técnicos y task statements

### 1. Objetivo de examen

- Identificar el `task statement` o conocimiento del blueprint al que corresponde.
- Explicar qué se espera poder decidir, implementar o reconocer.

### 2. Material oficial

- Exam Guide relevante.
- Documentación oficial.
- Curso/video oficial si aporta contenido al tema.
- Registrar exactamente qué recurso debe consumir el estudiante.

### 3. Complemento

Agregar una fuente adicional **sólo cuando aporte valor real**, por ejemplo:

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

Cuando el tema la necesita, la práctica puede incluir:

- ejercicio conceptual;
- modificación de prompts/configuración;
- implementación de código;
- laboratorio;
- debugging;
- decisión arquitectónica;
- comparación entre alternativas.

### 6. Preguntas

Para task statements y temas técnicos relevantes debe existir una batería de preguntas situacionales con:

- opciones plausibles;
- respuesta correcta;
- explicación de por qué es correcta;
- explicación de por qué las demás no lo son;
- referencia conceptual asociada.

El objetivo no es memorizar respuestas sino aprender a razonar los trade-offs.

### 7. Cierre

El checklist se adapta al tipo de bloque.

#### Curso de fundamentos

- [ ] Curso oficial completado.
- [ ] Conceptos principales comprendidos.
- [ ] Relación con CCAR-F documentada.
- [ ] Comprobación corta realizada.
- [ ] Material consolidado en GitHub.
- [ ] `PROGRESS.md` actualizado.

#### Curso técnico / task statement

- [ ] Material oficial revisado.
- [ ] Documentación técnica relevante revisada.
- [ ] Complemento útil revisado si existe un gap real.
- [ ] Conceptos comprendidos y documentados.
- [ ] Práctica realizada cuando corresponde.
- [ ] Preguntas respondidas y revisadas.
- [ ] Errores o dudas aclarados.
- [ ] Material consolidado en GitHub.
- [ ] `PROGRESS.md` actualizado.

Sólo entonces el bloque pasa a **COMPLETO**.

## Estados

- `PENDIENTE`
- `SIGUIENTE / NEXT`
- `EN ESTUDIO`
- `PRACTICA PENDIENTE`
- `PREGUNTAS PENDIENTES`
- `COMPLETO`

## Regla para CCAR-P

No se comienza la preparación formal de CCAR-P hasta completar el recorrido de CCAR-F bajo este protocolo.
