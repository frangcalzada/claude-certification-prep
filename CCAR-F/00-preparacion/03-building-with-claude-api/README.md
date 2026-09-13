# Building with the Claude API — Anthropic Academy

## Estado del curso

**Estado:** `EN ESTUDIO`  
**Checkpoint:** 2026-09-13  
**Etapa:** Technical Foundations  
**Último contenido completado:** Prompt Evaluation  
**Siguiente contenido:** A typical eval workflow

Este documento registra **solamente** el contenido estudiado hasta el checkpoint actual. El bloque completo de **Prompt evaluation** todavía no está terminado.

## Progreso registrado

### Introduction

- [x] Welcome to the course

### Anthropic overview

- [x] Overview of Claude models

### Accessing Claude with the API

- [x] Accessing the API
- [x] Getting an API key
- [x] Making a request
- [x] Multi-Turn conversations
- [x] Chat exercise
- [x] System prompts
- [x] System prompts exercise
- [x] Temperature
- [x] Response streaming
- [x] Structured data
- [x] Structured data exercise
- [x] Quiz on accessing Claude with the API

### Prompt evaluation

- [x] Prompt Evaluation
- [ ] A typical eval workflow — **SIGUIENTE / NEXT**
- [ ] Resto del bloque — **NO ESTUDIADO TODAVÍA**

---

## Claude models

Anthropic ofrece distintos **Claude models**. Cada modelo puede presentar capacidades y trade-offs diferentes, por lo que la elección depende de las necesidades de la aplicación.

En este checkpoint conservamos la idea conceptual: no existe una única elección universalmente óptima. Al seleccionar un modelo se deben considerar los requisitos concretos del caso de uso sin inventar capacidades o comparaciones que no hayan sido verificadas contra la documentación oficial vigente.

## Accessing the API

La **Anthropic API** es la interfaz programática que permite a una aplicación enviar solicitudes a Claude y recibir respuestas.

Una **API key** identifica y autentica al cliente autorizado frente a la API. La aplicación la presenta al realizar una solicitud según el mecanismo definido por Anthropic.

Conceptos principales:

- **autenticación:** permite que el servicio valide que la solicitud proviene de un cliente autorizado;
- **request:** datos e instrucciones enviados desde la aplicación hacia la API;
- **response:** resultado devuelto por la API;
- **API:** contrato HTTP que expone las capacidades del servicio;
- **SDK:** biblioteca que facilita desde un lenguaje de programación el uso de esa API.

Las API keys son secretos. No deben hardcodearse en el código ni subirse a repositorios. Deben almacenarse mediante mecanismos apropiados para secretos o variables de entorno, limitar su exposición y rotarse si se comprometen.

## Making a request

La estructura conceptual de una llamada es:

```text
application
→ API request
→ Claude model
→ response
```

La aplicación construye un request con los datos requeridos por la API. Según el SDK o endpoint utilizado, aparecen propiedades reales en English como `model`, `max_tokens` y `messages`. La API procesa la solicitud con el Claude model elegido y devuelve una response que la aplicación debe interpretar.

La idea importante no es memorizar una llamada aislada, sino entender sus partes:

1. la aplicación prepara la entrada;
2. autentica y envía el request;
3. el modelo procesa el contexto recibido;
4. la API devuelve la response;
5. la aplicación consume, presenta o procesa ese resultado.

## Multi-Turn Conversations

Una **multi-turn conversation** contiene varios intercambios entre el usuario y Claude.

Para conservar la continuidad, la aplicación debe mantener y volver a enviar el historial necesario dentro de `messages`:

- **user messages:** entradas, preguntas o instrucciones aportadas por el usuario;
- **assistant messages:** respuestas previas producidas por el modelo;
- **conversation history/context:** secuencia relevante de esos mensajes que permite interpretar correctamente el nuevo turno.

Un esquema conceptual es:

```text
user message
→ assistant message
→ user message
→ assistant message
```

Cada API request independiente contiene el contexto que la aplicación decide enviar. No se debe asumir que el modelo conserva mágicamente el estado interno del cliente entre requests independientes.

El **Chat exercise** de esta sección fue realizado.

## System prompts

Un **system prompt** define el comportamiento general esperado del modelo para una interacción o conversación. Puede establecer:

- el rol o perspectiva esperada;
- reglas e instrucciones globales;
- restricciones de comportamiento;
- criterios generales para las respuestas.

La diferencia conceptual principal es:

- un **system prompt** establece el marco global de comportamiento;
- un **user message** expresa la solicitud o entrada concreta del usuario dentro de ese marco.

Ambos forman parte del contexto, pero cumplen funciones distintas. El system prompt no reemplaza el contenido específico que debe aportar el usuario.

La lección y el **System prompts exercise** fueron completados.

## Temperature

`temperature` es un parámetro que influye en la variabilidad o randomness del output.

En términos generales:

- valores menores suelen favorecer respuestas menos variables;
- valores mayores suelen permitir mayor diversidad en la generación.

El valor apropiado depende del caso de uso. No se debe afirmar que `temperature: 0` garantiza que todas las ejecuciones producirán exactamente el mismo resultado, salvo que la documentación oficial lo garantice explícitamente.

## Response streaming

**Response streaming** permite recibir una respuesta incrementalmente mientras se genera, en lugar de esperar a que esté completa para comenzar a procesarla o mostrarla.

Esto puede mejorar:

- la **latency percibida**;
- la sensación de respuesta inmediata;
- la UX en respuestas extensas;
- el procesamiento progresivo cuando la aplicación lo necesita.

La diferencia conceptual es:

- **sin streaming:** la aplicación espera la respuesta completa;
- **con streaming:** la aplicación recibe eventos o fragmentos progresivos hasta que termina la generación.

Streaming mejora principalmente cómo se entrega la respuesta; no implica por sí mismo que el contenido sea más correcto.

## Structured data

**Structured data** consiste en pedir o producir información con una forma predecible para facilitar su interpretación y procesamiento.

Por ejemplo, una aplicación puede solicitar campos definidos, categorías consistentes o una estructura JSON esperada. Para obtener mejores resultados, el prompt debe explicar claramente:

- qué datos se necesitan;
- qué nombres y estructura se esperan;
- qué restricciones debe respetar el output;
- cómo tratar datos ausentes o ambiguos, cuando corresponda.

Una estructura predecible facilita que el software posterior valide, transforme o consuma la respuesta. En este checkpoint no se profundiza en **Structured Outputs**, JSON Schema avanzado ni `tool use`.

La lección y el **Structured data exercise** fueron completados.

## Prompt Engineering vs Prompt Evaluation

### Prompt Engineering

**Prompt Engineering** es el conjunto de técnicas y best practices utilizadas para mejorar prompts.

Puede incluir:

- instrucciones más claras;
- contexto relevante;
- ejemplos;
- criterios explícitos;
- mejor estructuración;
- formato de salida esperado.

### Prompt Evaluation

**Prompt Evaluation** es el proceso sistemático para medir cómo funcionan esos prompts.

Puede incluir:

- evaluar resultados contra outputs o criterios esperados;
- comparar versiones de un mismo prompt;
- revisar outputs;
- identificar errores y patrones de fallo;
- utilizar evidencia para decidir si una versión mejora realmente el comportamiento.

La idea central del checkpoint es:

> **Writing a good prompt is only the beginning.**

Para construir aplicaciones confiables necesitamos combinar:

```text
Prompt Engineering + Prompt Evaluation
```

Este documento no desarrolla todavía el workflow completo de evals, porque el siguiente contenido del curso es precisamente **A typical eval workflow**.

---

## Conceptos vistos hasta ahora

| Término | Explicación breve |
|---|---|
| **Claude model** | Modelo de Anthropic seleccionado para procesar el contexto y generar una respuesta. |
| **Anthropic API** | Interfaz programática para que una aplicación se comunique con Claude. |
| **API key** | Secreto utilizado para autenticar el acceso autorizado a la API. |
| **request** | Solicitud que la aplicación envía a la API con configuración, mensajes y datos necesarios. |
| **response** | Resultado que la API devuelve a la aplicación. |
| **multi-turn conversation** | Conversación con múltiples intercambios cuyo contexto relevante debe conservarse y enviarse. |
| **system prompt** | Instrucciones globales que establecen comportamiento, rol, reglas o criterios generales. |
| **user message** | Mensaje que contiene la entrada o solicitud concreta del usuario. |
| **assistant message** | Mensaje producido por Claude y conservable como parte del historial. |
| **temperature** | Parámetro que influye en la variabilidad o randomness del output. |
| **response streaming** | Entrega incremental de la respuesta durante su generación. |
| **structured data** | Información solicitada o producida con una estructura predecible. |
| **Prompt Engineering** | Técnicas y best practices para diseñar y mejorar prompts. |
| **Prompt Evaluation** | Evaluación sistemática del rendimiento de prompts contra criterios y resultados esperados. |

## Relación con CCAR-F

Este curso empieza a tocar directamente conocimientos relevantes del blueprint, especialmente:

- **Prompt Engineering & Structured Output**;
- **Context Management & Reliability**.

La relación es parcial: completar lecciones de un curso no equivale a completar un dominio del examen. Más adelante el curso probablemente tocará otros dominios, pero no se registran ni anticipan aquí hasta que hayan sido estudiados.

**Ningún dominio CCAR-F se marca como completado en este checkpoint.**

## Metodología Official-first

Este bloque conserva la metodología del repositorio:

1. **Exam Guide / blueprint oficial**;
2. **Anthropic Academy**;
3. **Anthropic docs**;
4. **hands-on labs** cuando exista suficiente contenido técnico;
5. fuentes externas sólo para cubrir gaps concretos;
6. questions y mocks posteriormente.

## Ejercicios y evaluaciones internas completadas

- [x] Chat exercise
- [x] System prompts exercise
- [x] Structured data exercise
- [x] Quiz on accessing Claude with the API

## Actividades que todavía no corresponden

- [ ] Hands-on labs finales del curso
- [ ] Preguntas finales tipo examen
- [ ] Mock final del curso
- [ ] Desarrollo completo del workflow de evals

Estas actividades se incorporarán cuando se complete suficiente contenido. Los ejercicios internos ya realizados sí quedan registrados.

## Checkpoint explícito

**Último contenido completado:** Prompt Evaluation  
**Siguiente contenido:** A typical eval workflow

## Fuentes

- Curso oficial: **Building with the Claude API — Anthropic Academy**.
- Complemento permitido: documentación oficial de Anthropic, siguiendo la metodología `Official-first`.

**Última actualización:** 2026-09-13.
