# AI Fluency: Framework & Foundations

**Estado:** `COMPLETO`  
**Ruta:** CCAR-F → preparación oficial → curso 1/7  
**Nivel oficial:** Level 100

Este documento conserva los conceptos principales de **AI Fluency: Framework & Foundations** sin sobreestudiar un curso cuyo aporte a CCAR-F es principalmente conceptual.

## Qué es AI Fluency

Anthropic define **AI Fluency** como la capacidad de colaborar con sistemas de AI de manera **effective, efficient, ethical and safe**. El objetivo no es solamente aprender técnicas de prompting, sino desarrollar criterios duraderos para decidir cómo colaborar con AI, cómo describir el trabajo, cómo evaluar resultados y cómo asumir responsabilidad sobre su uso.

El framework se organiza alrededor de cuatro competencias interconectadas: **Delegation, Description, Discernment y Diligence**.

---

## 4D Framework

### 1. Delegation

**Delegation** consiste en decidir qué trabajo debe realizar la persona, qué trabajo puede realizar la AI y cómo distribuir responsabilidades entre ambos.

Antes de delegar conviene evaluar:

- qué debería hacer la persona;
- qué debería hacer la AI;
- cómo se divide el trabajo;
- capacidades y limitaciones de la AI disponible;
- riesgo y reversibilidad de la tarea;
- cuánto control humano debe mantenerse.

El framework distingue tres modos frecuentes de interacción:

- **Automation:** la AI ejecuta tareas específicas a partir de instrucciones humanas.
- **Augmentation:** humano y AI colaboran como socios de razonamiento y ejecución.
- **Agency:** la persona configura a la AI para que realice tareas futuras con mayor independencia dentro de límites definidos.

> Que una AI pueda ejecutar una tarea no significa que deba ejecutarla autónomamente.

La decisión correcta depende del contexto, del riesgo y de cuánto juicio humano requiera el problema.

### 2. Description

**Description** es la capacidad de comunicar a la AI de manera suficientemente clara qué se intenta lograr.

Una buena descripción puede incluir:

- objetivo;
- contexto;
- restricciones;
- criterios de éxito;
- formato esperado;
- información relevante;
- ejemplos cuando ayuden a reducir ambigüedad.

Tiene una relación evidente con **prompting**, pero AI Fluency plantea el problema de forma más amplia: no se trata solamente de “escribir un buen prompt”, sino de construir una descripción útil del trabajo y de la colaboración esperada.

### 3. Discernment

**Discernment** es la capacidad de evaluar críticamente el output y el comportamiento de la AI.

Hay que revisar, según el caso:

- **correctness**;
- **completeness**;
- **relevance**;
- **reliability**;
- posibles **hallucinations**;
- necesidad de **verification**;
- necesidad de **iteration**.

Una respuesta convincente, extensa o bien escrita **no necesariamente es correcta**.

Discernment implica no aceptar el resultado sólo por su apariencia: debe contrastarse con los criterios de la tarea y, cuando el riesgo lo amerite, con fuentes, tests, datos o revisión humana.

### 4. Diligence

**Diligence** se refiere al uso responsable de AI y a asumir responsabilidad sobre lo que hacemos con ella.

Incluye considerar:

- privacidad;
- seguridad;
- datos sensibles;
- permisos;
- transparencia;
- **accountability**;
- impacto potencial de una acción incorrecta;
- cumplimiento de políticas o restricciones;
- necesidad de **human-in-the-loop** cuando corresponda.

La autonomía concedida debería ser proporcional al riesgo, a la reversibilidad de las acciones y a la capacidad de verificar el resultado.

---

## Loops importantes

### Description–Discernment loop

Un buen trabajo con AI suele ser iterativo:

**describir → obtener output → evaluar → mejorar la descripción → volver a intentar**.

El punto central es que **Description** y **Discernment** se retroalimentan: la evaluación de un resultado ayuda a mejorar la siguiente interacción.

### Delegation–Diligence loop

La decisión de delegar también debe revisarse según responsabilidad y riesgo:

**decidir qué delegar → analizar riesgos y responsabilidad → ajustar autonomía/controles → volver a evaluar**.

Una tarea inicialmente pensada para **Agency** puede terminar siendo más apropiada para **Augmentation** o incluso para ejecución humana si el costo de un error es demasiado alto.

---

## ¿Cuánto entra realmente en CCAR-F?

Anthropic incluye oficialmente **AI Fluency: Framework & Foundations** en el path de preparación de **Claude Certified Architect – Foundations (CCAR-F)**. Sin embargo, el **4D Framework no aparece como un dominio independiente ni como un task statement específico del Exam Blueprint**.

Su valor para nuestra preparación es principalmente conceptual: varios de sus principios reaparecen de forma indirecta dentro de decisiones arquitectónicas y técnicas que sí están explícitamente evaluadas.

| Concepto de AI Fluency | Relación indirecta con CCAR-F |
|---|---|
| **Delegation** | agent vs workflow vs human decision; grado de autonomía |
| **Description** | prompt engineering, instructions, context y criterios explícitos |
| **Discernment** | validation, evals, structured verification, revisión de outputs |
| **Diligence** | permissions, safety, human review, riesgo y acciones irreversibles |

### Clasificación para este proyecto

- **Valor directo para el examen:** bajo.
- **Valor como framework conceptual:** moderado.
- **Necesidad de laboratorio adicional:** no.
- **Necesidad de memorizar terminología:** baja/moderada.
- **Recomendación:** completar el curso una vez, comprender y conservar sus principios, pero no sobreestudiarlo.

No creamos un laboratorio técnico artificial para este bloque. La experiencia práctica relevante llegará en los cursos técnicos y, sobre todo, durante la cobertura exhaustiva de los task statements del blueprint.

---

## Ejemplo práctico: Claude revisando automáticamente un Pull Request

Supongamos que queremos usar Claude para revisar PRs antes de mergearlos.

### Delegation

Claude puede detectar problemas comunes, inconsistencias, riesgos y sugerir mejoras. La aprobación final de cambios críticos puede mantenerse en una persona. Para un repositorio de bajo riesgo podría automatizarse más; para seguridad, pagos o infraestructura conviene conservar más **human-in-the-loop**.

### Description

La revisión debería recibir contexto y criterios claros: objetivo del PR, convenciones del repositorio, archivos relevantes, restricciones, tipos de problemas a buscar y formato esperado del reporte.

### Discernment

Las observaciones de Claude no deben asumirse correctas automáticamente. Se validan contra código, tests, compilación y criterio técnico. Una sugerencia plausible puede ser incorrecta o ignorar contexto que no estaba disponible.

### Diligence

Hay que controlar qué código y secretos puede leer el sistema, qué permisos posee, si puede modificar el repo y qué acciones requieren aprobación humana. Para revisión automática, normalmente es más seguro separar **analizar/proponer** de **mergear/desplegar**.

---

## Preguntas de repaso

### 1. ¿Qué intenta decidir principalmente Delegation?

**Respuesta:** qué trabajo debe realizar el humano, qué trabajo debe realizar la AI y cómo distribuir responsabilidades entre ambos.

La decisión no depende sólo de capacidad técnica: también importan riesgo, autonomía, verificabilidad y consecuencias de un error.

### 2. ¿Cuál es la diferencia conceptual entre Automation, Augmentation y Agency?

**Respuesta:**

- **Automation:** AI ejecuta una tarea concreta indicada por una persona.
- **Augmentation:** humano y AI trabajan conjuntamente como socios de razonamiento/ejecución.
- **Agency:** la AI opera con mayor independencia dentro de una configuración y límites definidos previamente.

### 3. ¿Por qué Discernment sigue siendo necesario aunque el output parezca convincente?

**Respuesta:** porque fluidez y confianza aparente no garantizan **correctness**, **completeness** ni **reliability**. El output puede contener errores o hallucinations y debe evaluarse según el riesgo de la tarea.

### 4. ¿Qué representa el Description–Discernment loop?

**Respuesta:** un proceso iterativo en el que describimos el objetivo, evaluamos el resultado y usamos esa evaluación para mejorar la siguiente descripción hasta alcanzar un output adecuado.

### 5. ¿Cuándo aumenta la importancia de Diligence?

**Respuesta:** cuando existen datos sensibles, permisos elevados, acciones difíciles de revertir, impacto significativo, requisitos de seguridad/compliance o necesidad de justificar quién es responsable de una decisión. En esos casos pueden necesitarse controles adicionales y **human-in-the-loop**.

---

## Qué necesito recordar para continuar

1. **AI Fluency = effective + efficient + ethical + safe collaboration with AI.**
2. Las 4D son **Delegation, Description, Discernment, Diligence**.
3. Los tres modos principales son **Automation, Augmentation y Agency**.
4. Una buena colaboración requiere describir, evaluar e iterar.
5. El nivel de autonomía debe ajustarse al riesgo y a la responsabilidad.
6. AI Fluency forma parte del path oficial de CCAR-F, pero no constituye un dominio independiente del blueprint.

---

## Fuentes oficiales

- [AI Fluency: Framework & Foundations — Anthropic](https://www.anthropic.com/ai-fluency)
- [AI Fluency — Claude for Personal / Anthropic](https://www.anthropic.com/learn/claude-for-you)
- [The AI Fluency Framework — Anthropic (PDF)](https://www-cdn.anthropic.com/b383cf6baddbfc72fdf8b0ed533a518e2872d531.pdf)

**Última revisión de fuentes:** 2026-09-06.
