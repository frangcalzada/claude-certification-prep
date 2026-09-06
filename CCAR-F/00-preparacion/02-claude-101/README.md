# Claude 101 — Anthropic Academy

**Estado:** `COMPLETO`  
**Ruta:** CCAR-F → preparación oficial → curso 2/7  
**Nivel oficial:** Level 100

`Claude 101` es un curso introductorio de Anthropic Academy orientado a entender qué es Claude, cómo trabajar mejor con él y cuáles son las principales superficies y capacidades del ecosistema antes de pasar a contenido técnico más profundo.

La página oficial de **Claude Certified Architect – Foundations (CCAR-F)** lo incluye como segundo curso del preparation path, inmediatamente después de `AI Fluency: Framework & Foundations`.

> Este bloque es de orientación/fundamentos. No pretende enseñar en profundidad Claude API, Model Context Protocol (MCP), Agent SDK, Claude Code, RAG ni arquitectura de agents.

---

## Curriculum oficial revisado

A fecha **2026-09-06**, la página oficial de `Claude 101` publica el siguiente recorrido:

1. **Meet Claude**
   - What is Claude?
   - Your first conversation with Claude
   - Getting better results
   - How you'll work with Claude on your desktop
2. **Organizing your work and knowledge**
   - Introduction to projects
   - Creating with artifacts
   - Working with skills
3. **Expanding Claude's reach**
   - Connecting your tools
   - Enterprise search
   - Research for deep dives
4. **Putting it all together**
   - Claude in action: use-cases by role
   - Other ways to work with Claude
5. **Conclusion & certificate**
   - What's next?
   - Certificate of completion

La estructura incluye algunos encabezados de módulo que agrupan las lecciones. Para el estudio importa comprender las capacidades y conceptos, no memorizar la navegación exacta del curso.

---

# 1. Qué busca Claude 101

El curso enseña una visión práctica y general del ecosistema Claude:

- qué es Claude;
- cómo interactuar con Claude;
- cómo mejorar resultados;
- cómo organizar información y contexto;
- qué superficies/productos existen;
- cómo extender Claude mediante conocimiento, capacidades y herramientas conectadas.

No es un curso técnico profundo. Su objetivo es construir el **mapa mental** que necesitamos antes de estudiar los bloques técnicos de CCAR-F.

---

# 2. Qué es Claude

Podemos pensar en **Claude** en varios niveles relacionados pero diferentes.

### Claude como modelos

Claude es una familia de modelos de Anthropic capaz de trabajar con lenguaje, razonamiento, código, archivos y otros tipos de información.

### Claude como aplicación / producto

La aplicación Claude proporciona una experiencia interactiva para conversar y trabajar con esos modelos, además de capacidades de producto como `Projects`, `Artifacts`, `Skills`, `Connectors`, `Enterprise Search` y `Research`.

### Claude API

La **Claude API** permite que software propio consuma modelos y capacidades de Claude programáticamente.

No profundizamos todavía en autenticación, Messages API, tool use, structured output, streaming, evals, RAG o agents. Todo eso se estudiará en `Building with the Claude API` y posteriormente al cubrir los task statements del examen.

### Claude Code

**Claude Code** es la superficie orientada al trabajo de software engineering y codebases. Tiene conceptos y workflows propios que estudiaremos más adelante en `Claude Code in Action` y en el dominio correspondiente del blueprint.

### Integraciones

Claude también puede conectarse con herramientas y fuentes externas. En la aplicación esto aparece mediante capacidades como `Connectors`. Más adelante estudiaremos la arquitectura técnica de integración y **Model Context Protocol (MCP)**.

---

# 3. Conversaciones y prompting básico

Claude 101 introduce principios básicos para obtener mejores resultados.

## Explicar claramente el objetivo

Claude funciona mejor cuando entiende qué queremos conseguir, no sólo qué texto queremos generar.

En vez de una instrucción ambigua, conviene indicar:

- objetivo;
- contexto;
- audiencia o situación;
- criterios importantes.

## Aportar contexto suficiente

Una respuesta depende de la información disponible. Cuando falta contexto relevante, la calidad de la respuesta puede degradarse o Claude puede interpretar el problema de manera distinta a la esperada.

## Especificar restricciones

Cuando existen límites importantes deben hacerse explícitos, por ejemplo:

- tecnología permitida;
- alcance;
- datos que no deben utilizarse;
- longitud;
- reglas de negocio;
- acciones prohibidas.

## Indicar el formato esperado

Definir el resultado esperado reduce ambigüedad:

- tabla;
- lista;
- documento;
- explicación;
- JSON;
- código;
- checklist;
- otro formato apropiado.

## Iterar

El primer resultado no tiene por qué ser el definitivo.

```text
objetivo/contexto
→ primera respuesta
→ revisión
→ feedback
→ refinamiento
```

Esto conecta directamente con **Description** y **Discernment** del `AI Fluency Framework`.

## Dividir tareas cuando conviene

Problemas complejos pueden beneficiarse de dividirse en etapas manejables. El concepto aparecerá mucho más adelante de forma técnica al estudiar task decomposition, workflows y agents.

> `Prompt Engineering` se estudiará de forma específica y profunda en una etapa posterior. Aquí sólo conservamos fundamentos de interacción.

---

# 4. Projects

`Projects` son espacios de trabajo autocontenidos que permiten organizar chats, conocimiento e instrucciones alrededor de un objetivo o ámbito determinado.

Un Project puede contener:

- chats relacionados;
- **project knowledge**;
- documentos, texto, código u otros archivos relevantes;
- **project instructions** que orientan cómo Claude debe responder dentro de ese Project.

## Para qué sirve

Es útil cuando existe continuidad de trabajo y queremos evitar comenzar cada conversación desde cero con el mismo contexto base.

Ejemplos:

- una codebase;
- un proyecto de arquitectura;
- investigación prolongada;
- documentación de un cliente;
- preparación para una certificación.

## Project vs conversación aislada

Una conversación aislada es adecuada para una tarea puntual que no necesita contexto persistente del proyecto.

Un Project resulta más apropiado cuando múltiples conversaciones deben trabajar sobre el mismo conocimiento e instrucciones.

### Matiz importante

Los chats dentro de un Project **no comparten automáticamente el contenido completo de sus conversaciones entre sí**.

La información reutilizable debe formar parte del **project knowledge** o de las **project instructions** para que esté disponible de forma consistente en otros chats del Project.

No debemos confundir “estar en el mismo Project” con “todas las conversaciones comparten automáticamente toda su historia”.

---

# 5. Artifacts

`Artifacts` permiten trabajar con contenido sustancial como un objeto separado de la conversación principal.

Pueden utilizarse para crear y desarrollar, según las capacidades disponibles:

- documentos;
- código;
- visualizaciones;
- herramientas o aplicaciones;
- otros outputs que conviene editar, consultar o reutilizar como una unidad independiente.

## Artifact vs respuesta normal

Una respuesta normal forma parte del flujo conversacional.

Un `Artifact` resulta útil cuando el output tiene entidad propia y queremos:

- verlo separado del chat;
- iterarlo;
- modificarlo;
- construir sobre él;
- conservarlo o compartirlo según las capacidades disponibles.

Esto hace que Artifacts encaje bien en workflows iterativos de creación.

---

# 6. Skills

`Skills` permiten proporcionar a Claude capacidades o procedimientos reutilizables para tareas especializadas.

A nivel conceptual, una Skill puede empaquetar:

- instrucciones;
- conocimiento procedural;
- recursos;
- scripts cuando corresponda;
- convenciones para ejecutar un workflow de forma consistente.

## Skill vs prompt individual

Un prompt individual explica qué hacer en una interacción concreta.

Una `Skill` sirve cuando existe un comportamiento o workflow reutilizable que queremos enseñar una vez y poder aplicar nuevamente cuando sea relevante.

Ejemplos conceptuales:

- generar documentos siguiendo el formato interno de una empresa;
- aplicar un procedimiento repetible de análisis;
- producir entregables según una guía de estilo;
- ejecutar un workflow especializado.

No profundizamos aquí en la estructura técnica de `SKILL.md`, progressive disclosure, distribución ni integración con Claude Code/MCP. Esos detalles pertenecen a módulos posteriores.

---

# 7. Connectors

`Connectors` permiten que Claude acceda a aplicaciones, servicios y fuentes externas autorizadas y, según el connector, pueda recuperar información o realizar acciones.

Conceptualmente ayudan a:

- ampliar el contexto disponible;
- acceder a información de otros sistemas;
- reducir copy/paste manual;
- trabajar con herramientas ya utilizadas por una persona o equipo;
- respetar los permisos que el usuario tiene en el sistema conectado.

Ejemplos de categorías posibles incluyen herramientas de colaboración, almacenamiento, gestión de proyectos y otros servicios empresariales.

## Connector vs MCP

**No son sinónimos.**

- `Connector` es el concepto de integración/capacidad de conexión visible desde la experiencia de producto.
- `Model Context Protocol (MCP)` es un protocolo abierto y una arquitectura técnica para conectar AI systems con herramientas y fuentes de datos.

Algunos connectors pueden apoyarse en MCP, y Claude permite custom connectors hacia servicios compatibles con MCP, pero la perspectiva conceptual es distinta.

> MCP se estudiará posteriormente como tema técnico propio. Aquí sólo necesitamos reconocer la relación sin confundir los términos.

---

# 8. Enterprise Search

`Enterprise Search` permite buscar información distribuida entre fuentes empresariales autorizadas desde una experiencia unificada.

La documentación actual de Claude describe una experiencia dedicada —por ejemplo un Project preconfigurado como `Ask Your Org`— que integra connectors e instrucciones optimizadas para búsqueda organizacional.

Conceptos que debemos conservar:

- búsqueda sobre conocimiento empresarial;
- recuperación de contexto relevante;
- consulta de múltiples fuentes autorizadas;
- respeto de autenticación y permisos;
- síntesis de información proveniente de distintos sistemas.

Puede relacionarse conceptualmente con **retrieval**, pero no debemos adelantarnos a arquitectura de `RAG`, embeddings, chunking, indexing o retrieval pipelines.

---

# 9. Research

`Research` es una capacidad orientada a investigaciones más profundas.

Claude puede realizar múltiples búsquedas de forma iterativa, investigar diferentes ángulos y sintetizar la información encontrada.

Conceptos importantes:

- búsqueda;
- investigación iterativa;
- síntesis;
- análisis;
- revisión de fuentes;
- citations cuando corresponda;
- verificación del resultado.

## Relación con Discernment

`Research` no elimina la responsabilidad de evaluar lo producido.

Una investigación extensa o una respuesta con apariencia convincente puede seguir teniendo:

- fuentes débiles;
- interpretaciones incorrectas;
- información incompleta;
- errores de síntesis.

Por eso el usuario debe revisar fuentes y aplicar **Discernment**.

---

# 10. Other ways to work with Claude

Claude no debe entenderse únicamente como “el chat de la web”.

Un mapa mental simple para esta etapa es:

```text
Claude ecosystem
│
├── Claude app
│   ├── conversations
│   ├── Projects
│   ├── Artifacts
│   ├── Skills
│   ├── Connectors
│   ├── Enterprise Search
│   └── Research
│
├── Claude API          ← se estudiará técnicamente después
├── Claude Code         ← se estudiará técnicamente después
└── MCP / integrations  ← se estudiará técnicamente después
```

El objetivo de Claude 101 no es conocer la implementación interna de cada pieza, sino reconocer qué problema resuelve cada una y cómo encajan dentro del ecosistema.

---

# 11. Relación de Claude 101 con CCAR-F

Anthropic incluye oficialmente `Claude 101` dentro del preparation path de **Claude Certified Architect – Foundations**.

Sin embargo, `Claude 101` **no representa un dominio independiente ni un task statement específico del Exam Blueprint**.

Su principal aporte es proporcionar orientación sobre el ecosistema antes de entrar en temas técnicamente más profundos:

- Claude API;
- agents;
- MCP;
- Claude Code;
- Prompt Engineering;
- Context Management.

## Clasificación para este proyecto

- **Valor técnico directo para el examen:** bajo/moderado.
- **Valor de orientación sobre el ecosistema:** alto.
- **Necesidad de laboratorio técnico adicional:** no.
- **Necesidad de memorizar interfaces de usuario:** baja.
- **Necesidad de reconocer conceptos y nombres:** sí.

Las interfaces y disponibilidades concretas pueden cambiar rápidamente. Para CCAR-F priorizamos el concepto y la decisión que habilita cada feature, no la posición exacta de un botón.

---

# 12. Conceptos que deben quedar reconocibles

| Concepto | Definición corta | Para qué sirve | ¿Se profundiza después? |
|---|---|---|---|
| `Claude` | Familia de modelos y ecosistema de productos/capacidades de Anthropic. | Razonamiento, lenguaje, código, archivos y workflows. | Sí, transversalmente. |
| `Projects` | Workspace autocontenido con chats, knowledge e instrucciones propias. | Mantener contexto e instrucciones alrededor de un objetivo. | Algo, al estudiar context management. |
| `Artifacts` | Contenido sustancial separado del flujo principal del chat. | Crear, editar e iterar outputs con entidad propia. | No es foco técnico central de CCAR-F. |
| `Skills` | Procedimientos/capacidades reutilizables cargados cuando son relevantes. | Estandarizar workflows y conocimiento procedural. | Sí, especialmente Claude Code/workflows. |
| `Connectors` | Integraciones que conectan Claude con apps, datos y acciones autorizadas. | Acceder a sistemas externos sin copy/paste manual. | Sí, al estudiar integración/MCP. |
| `Enterprise Search` | Búsqueda unificada sobre fuentes empresariales autorizadas. | Encontrar y sintetizar conocimiento organizacional. | Los patrones de retrieval se estudian después. |
| `Research` | Capacidad de investigación iterativa y síntesis usando búsquedas y fuentes. | Profundizar preguntas complejas con evidencia. | Se relacionará con reliability/provenance. |
| `Claude API` | Interfaz programática para construir software sobre Claude. | Integrar modelos/capacidades en aplicaciones. | **Sí: siguiente curso.** |
| `Claude Code` | Superficie de Claude orientada a software engineering y codebases. | Trabajar sobre código y workflows de desarrollo. | **Sí, curso específico.** |
| `MCP` | Protocolo abierto para conectar AI systems con herramientas y datos. | Estandarizar integraciones y tool/data access. | **Sí, curso específico.** |

---

# 13. Diferencias que pueden generar confusión

## Project vs conversación común

**Conversación común:** contexto principalmente local a una interacción/chat.

**Project:** espacio de trabajo donde varias conversaciones pueden compartir **project knowledge** e instrucciones comunes alrededor de un objetivo.

Recordatorio: el contenido de una conversación no se transfiere automáticamente a todas las demás conversaciones del Project.

## Artifact vs respuesta normal

**Respuesta normal:** forma parte del intercambio conversacional.

**Artifact:** contenido sustancial tratado como objeto separado, conveniente para iterar, editar o reutilizar.

## Skill vs prompt individual

**Prompt individual:** instrucción para una interacción concreta.

**Skill:** conocimiento procedural/capacidad reusable para ejecutar tipos de tareas o workflows de manera consistente.

## Connector vs MCP

**Connector:** integración desde la experiencia/producto Claude.

**MCP:** protocolo y arquitectura técnica que puede utilizarse para conectar herramientas y datos.

No son términos intercambiables.

## Claude app vs Claude API

**Claude app:** producto interactivo que utiliza una persona directamente.

**Claude API:** interfaz programática que utiliza software para integrar Claude en una aplicación o sistema.

---

# 14. Ejemplo integrado — Tech Lead preparando una ADR

Un Tech Lead necesita analizar documentación de arquitectura, comparar propuestas y producir una **Architecture Decision Record (ADR)**.

### Project

Crea un Project específico para la iniciativa, con instrucciones y conocimiento relevante compartido entre sus chats.

### Project knowledge

Agrega documentos de arquitectura, restricciones, decisiones anteriores y estándares del equipo que deban estar disponibles como contexto estable.

### Skill

Si la organización genera ADRs repetidamente con un formato y proceso específicos, una Skill podría encapsular ese procedimiento reusable.

### Artifact

La ADR puede construirse como Artifact para trabajar sobre el documento como una pieza separada del chat e iterarlo hasta dejarlo listo.

### Connector

Si la documentación vive en una herramienta autorizada, un Connector puede permitir recuperar esa información sin copiarla manualmente.

### Research

Si la decisión requiere comparar tecnologías o consultar información externa, Research puede ayudar a buscar, analizar y sintetizar fuentes. El Tech Lead sigue siendo responsable de validar evidencia y decisión final.

> Este ejemplo sólo integra conceptos. No constituye un laboratorio técnico.

---

# 15. Preguntas de comprobación

## 1. ¿Cuándo conviene usar un Project en vez de una conversación aislada?

**Respuesta:** cuando existe un objetivo sostenido que necesita conocimiento o instrucciones comunes en múltiples chats. El Project ayuda a organizar ese contexto de forma persistente.

## 2. ¿Todos los chats de un Project comparten automáticamente todo lo conversado entre sí?

**Respuesta:** no. El conocimiento reutilizable debe incorporarse al project knowledge o a las project instructions. Estar dentro del mismo Project no implica que toda la historia de cada chat esté disponible en los demás.

## 3. ¿Qué problema resuelve principalmente un Artifact?

**Respuesta:** permite tratar contenido sustancial como una pieza independiente del flujo conversacional para visualizarlo, modificarlo, iterarlo y reutilizarlo con mayor comodidad.

## 4. ¿Cuál es la diferencia conceptual entre una Skill y repetir un prompt?

**Respuesta:** un prompt individual instruye una interacción concreta; una Skill encapsula instrucciones, conocimiento procedural o recursos reutilizables para aplicar un comportamiento/workflow especializado repetidamente.

## 5. ¿Connector y MCP significan lo mismo?

**Respuesta:** no. Connector es la integración/capacidad desde la perspectiva del producto. MCP es un protocolo abierto y una arquitectura técnica para conectar AI systems con tools y data sources. Pueden relacionarse, pero no son sinónimos.

## 6. ¿Cuál es la diferencia entre Claude app y Claude API?

**Respuesta:** Claude app es un producto interactivo usado directamente por personas. Claude API permite que aplicaciones y sistemas consuman Claude programáticamente.

## 7. ¿Qué aporta Enterprise Search?

**Respuesta:** permite buscar y sintetizar conocimiento distribuido entre fuentes empresariales autorizadas, teniendo en cuenta autenticación y permisos de acceso.

## 8. ¿Qué responsabilidad conserva el usuario cuando utiliza Research?

**Respuesta:** debe evaluar la calidad de las fuentes, verificar afirmaciones relevantes, detectar posibles errores y decidir si la evidencia es suficiente. Research ayuda a investigar, pero no elimina la necesidad de Discernment.

## 9. ¿Por qué no conviene memorizar la interfaz exacta de Claude para CCAR-F?

**Respuesta:** porque la interfaz de producto puede cambiar y ese conocimiento es frágil. Para nuestra preparación importa más entender el propósito, las diferencias y los trade-offs de las capacidades que memorizar dónde está cada botón.

## 10. ¿Qué curso continúa después de Claude 101 en el path oficial de CCAR-F?

**Respuesta:** `Building with the Claude API`. Con ese curso comienza nuestra **Technical Foundations Stage**.

---

# 16. Evaluación del curso

## Claude 101

- **Curso oficial:** sí.
- **Recomendado oficialmente para CCAR-F:** sí.
- **Completado:** sí.
- **Tipo:** orientación/fundamentos.
- **Valor directo para task statements:** bajo/moderado.
- **Valor para comprender el ecosistema Claude:** alto.
- **Lab técnico adicional:** no necesario.
- **Recomendación para futuras personas:** completarlo una vez antes de iniciar el contenido técnico y conservar el mapa conceptual, sin sobreestudiar detalles de UI.

No encontramos razones oficiales actuales para cambiar esta evaluación.

---

# 17. Qué necesito recordar para continuar

1. `Claude 101` construye el mapa del ecosistema; no reemplaza el estudio técnico posterior.
2. `Projects` = workspace + knowledge + instructions alrededor de un objetivo.
3. `Artifacts` = outputs sustanciales tratados como objetos separados del chat.
4. `Skills` = capacidades/procedimientos reutilizables.
5. `Connectors` = acceso a apps/data/actions autorizados; **no son sinónimo de MCP**.
6. `Enterprise Search` = búsqueda unificada sobre conocimiento empresarial autorizado.
7. `Research` = investigación iterativa + síntesis + fuentes, pero sigue necesitando Discernment.
8. `Claude app` y `Claude API` son superficies distintas.
9. No memorizar detalles efímeros de interfaz: priorizar conceptos y terminología.
10. El siguiente curso es **Building with the Claude API**.

---

# Fuentes oficiales

- [Claude 101 — Anthropic Academy](https://anthropic-partners.skilljar.com/claude-101)
- [Claude Certified Architect – Foundations — Anthropic Academy](https://anthropic-partners.skilljar.com/claude-certified-architect-foundations-certification)
- [What are projects? — Claude Help Center](https://support.claude.com/en/articles/9517075-what-are-projects)
- [How can I create and manage projects? — Claude Help Center](https://support.claude.com/en/articles/9519177-how-can-i-create-and-manage-projects)
- [What are artifacts and how do I use them? — Claude Help Center](https://support.claude.com/en/articles/9487310-what-are-artifacts-and-how-do-i-use-them)
- [What are skills? — Claude Help Center](https://support.claude.com/en/articles/12512176-what-are-skills)
- [Use connectors to extend Claude's capabilities — Claude Help Center](https://support.claude.com/en/articles/11176164-use-connectors-to-extend-claude-s-capabilities)
- [Use enterprise search — Claude Help Center](https://support.claude.com/en/articles/12489464-use-enterprise-search)
- [Use research on Claude — Claude Help Center](https://support.claude.com/en/articles/11088861-use-research-on-claude)

**Última revisión de fuentes:** 2026-09-06.
