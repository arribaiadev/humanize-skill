---
name: humanize
description: Audita y humaniza artículos en español para ArribaIA, eliminando patrones de escritura artificial asociados a LLMs sin perder precisión, intención de búsqueda, SEO ni información útil. Puede auditar textos existentes o reescribirlos aplicando criterios editoriales humanos.
---

# /humanize — ArribaIA Human Writing Skill

## PROPÓSITO

Esta skill sirve para:

1. Auditar artículos escritos previamente.
2. Detectar patrones lingüísticos, estructurales y editoriales asociados a textos generados por IA.
3. Reescribir esos textos para que resulten naturales y humanos.
4. Prevenir esos patrones cuando se redacte un artículo nuevo.
5. Mantener SEO, intención de búsqueda, precisión factual y utilidad para el lector.

La finalidad NO es engañar detectores de IA.

La finalidad es producir textos que:
- parezcan escritos por una persona competente;
- tengan una voz editorial consistente;
- sean concretos;
- no estén artificialmente inflados;
- no utilicen lenguaje corporativo innecesario;
- no repitan estructuras típicas de LLM;
- no inventen información;
- no sacrifiquen naturalidad por SEO.

---

# PRINCIPIO FUNDAMENTAL

No sustituir simplemente "palabras de IA" por sinónimos.

La humanización debe corregir la causa del problema.

Ejemplo incorrecto:

> La empresa desempeña un papel crucial en el dinámico panorama digital actual.

Cambiarlo por:

> La empresa tiene un papel fundamental en el cambiante ecosistema digital actual.

NO es humanizar.

La versión preferida sería:

> La empresa ofrece servicios de posicionamiento web para negocios locales.

Siempre que esa afirmación sea cierta.

REGLA:

> Preferir hechos, ejemplos y afirmaciones concretas frente a valoraciones genéricas.

---

# MODOS DE USO

## `/humanize`

Si se proporciona un artículo:

1. Auditarlo internamente.
2. Identificar problemas.
3. Reescribir únicamente aquello que necesite corrección.
4. Mantener intacta la información correcta.
5. Mantener la intención de búsqueda.
6. Mantener las palabras clave importantes cuando su uso sea natural.
7. Entregar únicamente la versión final salvo que el usuario solicite auditoría.

---

## `/humanize audit`

Auditar el artículo sin reescribirlo.

La auditoría debe incluir:

- puntuación global;
- categorías problemáticas;
- ejemplos concretos;
- explicación del problema;
- recomendación de corrección;
- nivel de gravedad.

Nunca afirmar:

> "Este artículo tiene un 73 % de IA."

La puntuación representa únicamente la presencia de patrones estilísticos asociados a escritura artificial.

---

## `/humanize audit --fix`

1. Ejecutar auditoría.
2. Corregir los problemas encontrados.
3. Volver a auditar el resultado.
4. Mostrar:
   - puntuación inicial;
   - puntuación final;
   - principales cambios realizados.

---

# OBJETIVO EDITORIAL DE ARRIBAIA

Los artículos deben sonar como escritos por una persona que:

- conoce el tema;
- entiende el mercado español;
- sabe explicar conceptos técnicos;
- escribe para personas reales;
- no intenta demostrar continuamente que sabe mucho;
- no rellena espacio;
- utiliza ejemplos concretos;
- puede expresar una opinión cuando está justificada;
- utiliza un lenguaje natural.

La voz debe ser:

- española;
- clara;
- directa;
- profesional;
- cercana;
- técnicamente correcta;
- ligeramente conversacional cuando encaje;
- sin exceso de formalidad;
- sin lenguaje corporativo;
- sin entusiasmo artificial.

Evitar que todos los artículos tengan exactamente la misma personalidad.

---

# REGLAS DE HUMANIZACIÓN

## 1. ELIMINAR IMPORTANCIA ARTIFICIAL

Detectar afirmaciones que exageren la importancia de algo sin aportar evidencia.

Patrones problemáticos:

- juega un papel crucial;
- desempeña un papel fundamental;
- constituye un elemento clave;
- supone un hito;
- marca un antes y un después;
- representa un punto de inflexión;
- tiene una gran relevancia;
- resulta de vital importancia;
- deja una huella;
- consolida su posición;
- refuerza su compromiso;
- pone de manifiesto la importancia;
- demuestra su enorme relevancia;
- refleja una tendencia más amplia;
- se ha convertido en un referente;
- es un claro ejemplo de;
- representa una evolución significativa.

No prohibir estas expresiones automáticamente.

Preguntar:

> ¿La frase aporta un hecho verificable o simplemente declara que algo es importante?

Si solamente declara importancia, eliminarla.

Ejemplo:

EVITAR:

> El SEO local juega un papel crucial en el crecimiento de cualquier negocio.

PREFERIR:

> El SEO local ayuda a que un negocio aparezca cuando alguien busca sus servicios en una zona concreta.

---

# 2. EVITAR ANÁLISIS SUPERFICIAL

Detectar:

HECHO + interpretación genérica innecesaria.

Ejemplo:

> La empresa abrió una oficina en Valencia, consolidando así su presencia en el mercado y reforzando su compromiso con la innovación.

Preferir:

> La empresa abrió una oficina en Valencia en 2025.

Si existen datos que demuestran crecimiento:

> La empresa abrió una oficina en Valencia en 2025 y aumentó su plantilla local de 8 a 14 personas.

La información concreta sustituye a la interpretación vacía.

---

# 3. ELIMINAR LENGUAJE PROMOCIONAL ARTIFICIAL

Especialmente importante para los artículos de ArribaIA.

Detectar:

- innovador;
- revolucionario;
- disruptivo;
- de vanguardia;
- líder;
- referente;
- excepcional;
- único;
- extraordinario;
- potente;
- integral;
- transformador;
- pionero;
- avanzado;
- personalizado;
- estratégico;
- dinámico;
- moderno;
- puntero;
- de última generación.

No eliminar cuando sean necesarios y demostrables.

Regla:

> Si un adjetivo promociona algo, preguntar qué hecho demuestra esa cualidad.

Ejemplo:

EVITAR:

> Una solución innovadora y revolucionaria para mejorar el SEO.

PREFERIR:

> Una herramienta que analiza las páginas de la competencia y genera propuestas de contenidos.

---

# 4. REDUCIR JERGA CORPORATIVA

Evitar acumulaciones como:

- ecosistema digital;
- panorama actual;
- entorno cambiante;
- transformación digital;
- sinergias;
- soluciones integrales;
- propuesta de valor;
- hoja de ruta;
- puesta en valor;
- apuesta estratégica;
- enfoque holístico;
- experiencia 360º;
- maximizar resultados;
- potenciar;
- impulsar;
- optimizar procesos;
- generar sinergias.

No están prohibidas.

El problema es utilizarlas cuando una expresión sencilla comunica exactamente lo mismo.

Ejemplo:

> Ayudamos a las empresas a potenciar su presencia digital.

Preferir:

> Ayudamos a las empresas a conseguir más visitas desde Google.

---

# 5. EVITAR PARALELISMOS ARTIFICIALES

Detectar especialmente:

- no solo X, sino también Y;
- no se trata de X, sino de Y;
- no es simplemente X, sino Y;
- más que X, es Y;
- no únicamente X, sino Y;
- tanto X como Y, además de Z.

No prohibirlas.

Reducir su uso cuando aparezcan repetidamente o cuando exista una construcción más directa.

Ejemplo:

EVITAR:

> No solo necesitas una web bonita, sino también una estrategia SEO sólida.

PREFERIR:

> Una web bonita no basta si nadie la encuentra en Google.

---

# 6. EVITAR REGLAS DE TRES ARTIFICIALES

Detectar acumulaciones del tipo:

> rápido, sencillo y eficaz.

> calidad, innovación y experiencia.

> captar, convertir y fidelizar.

> analizar, optimizar y mejorar.

Una enumeración de tres elementos es perfectamente válida.

Solo marcarla cuando:

- aparece repetidamente;
- los conceptos son vagos;
- parece utilizada para dar ritmo artificial;
- podría sustituirse por una descripción concreta.

No eliminar enumeraciones necesarias.

---

# 7. NO EVITAR REPETICIONES NATURALES

Los modelos suelen intentar evitar repetir palabras.

No hacerlo.

Si "empresa" es la palabra correcta, puede aparecer varias veces.

No sustituir artificialmente:

> empresa → compañía → organización → firma → entidad → negocio

cuando todos hacen referencia a lo mismo.

Preferir precisión semántica sobre variedad léxica.

REGLA:

> Repetir una palabra correcta es mejor que utilizar un sinónimo extraño.

---

# 8. REDUCIR VOCABULARIO TÍPICO DE LLM

Prestar especial atención a:

- crucial;
- fundamental;
- significativo;
- relevante;
- notable;
- integral;
- complejo;
- multifacético;
- dinámico;
- cambiante;
- creciente;
- transformador;
- profundo;
- exhaustivo;
- detallado;
- estratégico;
- sólido;
- robusto;
- eficaz;
- innovador;
- revolucionario;
- panorama;
- ecosistema;
- ámbito;
- contexto;
- trayectoria;
- legado;
- convergencia;
- evolución;
- impacto.

No utilizar una blacklist rígida.

Evaluar siempre el contexto.

---

# 9. PREFERIR VERBOS SIMPLES

Evitar convertir verbos normales en construcciones innecesariamente sofisticadas.

EVITAR:

> La empresa se posiciona como una entidad especializada en...

PREFERIR:

> La empresa ofrece...

EVITAR:

> La herramienta permite llevar a cabo un análisis...

PREFERIR:

> La herramienta permite analizar...

EVITAR:

> Procederemos a explicar...

PREFERIR:

> Explicamos...

EVITAR:

> Con el objetivo de proceder a mejorar...

PREFERIR:

> Para mejorar...

---

# 10. ELIMINAR RELLENO INTRODUCTORIO

Evitar aperturas genéricas como:

> En el mundo digital actual...

> En la era de la transformación digital...

> En un contexto cada vez más competitivo...

> Hoy en día, vivimos en una sociedad...

> En los últimos años hemos sido testigos de...

> En el panorama empresarial actual...

Siempre preguntar:

> ¿Qué información necesita realmente el lector en la primera frase?

Empezar por ella.

Ejemplo:

EVITAR:

> En el mundo digital actual, donde la competencia es cada vez mayor, contar con una buena presencia online se ha convertido en algo fundamental para cualquier negocio.

PREFERIR:

> Si tienes un negocio local, aparecer en Google cuando alguien busca tus servicios puede marcar la diferencia entre recibir una llamada o perder ese cliente.

---

# 11. NO FABRICAR INTRODUCCIONES UNIVERSALES

No utilizar automáticamente:

1. contexto general;
2. problema;
3. importancia;
4. promesa del artículo.

La introducción debe depender del tema.

Puede ser:

- una respuesta directa;
- un ejemplo;
- una situación habitual;
- una pregunta;
- un dato;
- una explicación breve;
- una definición.

---

# 12. EVITAR CONCLUSIONES ARTIFICIALES

No añadir automáticamente:

- En conclusión;
- En definitiva;
- En resumen;
- Para concluir;
- Como hemos visto;
- En última instancia;
- En pocas palabras.

Una conclusión solo debe existir si aporta algo.

No repetir el artículo.

Si la conclusión es necesaria, debe:

- aportar una recomendación;
- sintetizar una decisión;
- responder una pregunta;
- señalar una limitación;
- dar un siguiente paso.

---

# 13. EVITAR SECCIONES ARTIFICIALES

No crear automáticamente:

- Beneficios;
- Ventajas;
- Desventajas;
- Retos;
- Perspectivas futuras;
- Impacto;
- Conclusiones;
- Preguntas frecuentes.

Crear una sección solo si responde a una necesidad real del lector.

No todos los artículos necesitan la misma estructura.

---

# 14. EVITAR EL "FUTURE OUTLOOK"

No terminar artículos automáticamente con:

> De cara al futuro...

> En los próximos años...

> Todo apunta a que...

> Se espera que...

> El futuro estará marcado por...

Solo utilizar predicciones cuando:

- existan datos;
- se cite una fuente;
- exista una razón concreta para la predicción;
- se indique claramente que es una previsión.

---

# 15. EVITAR FRASES DE CHATBOT

Eliminar completamente del artículo final:

- Espero que esta información te haya resultado útil.
- Espero que te sirva.
- Aquí tienes...
- Por supuesto.
- A continuación veremos...
- En este artículo vamos a explorar...
- Como veremos a continuación...
- Si quieres, puedo...
- No dudes en...
- ¿Quieres que...?
- Estaré encantado de...
- Cabe destacar que...
- Es importante señalar que...
- Conviene mencionar que...

Cuando la frase pueda eliminarse sin perder información, eliminarla.

---

# 16. ELIMINAR METACOMENTARIO

No hablar sobre el propio proceso de escritura.

EVITAR:

> En este artículo analizaremos...

> Primero veremos...

> Después explicaremos...

> Por último, repasaremos...

PREFERIR empezar directamente con la información.

---

# 17. REDUCIR EXPLICACIONES OBVIAS

No explicar cosas que el lector ya entiende.

EVITAR:

> Google es el buscador más utilizado y permite a los usuarios realizar búsquedas en Internet.

Si el artículo trata de SEO, asumir conocimientos básicos salvo que el público objetivo sea principiante.

---

# 18. EVITAR DEFINICIONES DE DICCIONARIO ARTIFICIALES

No comenzar automáticamente:

> X es un concepto que hace referencia a...

Preferir:

> El SEO local consiste en optimizar la presencia de un negocio para búsquedas relacionadas con una ubicación concreta.

O, mejor aún, si el contexto lo permite:

> Cuando alguien busca "dentista en Valencia", Google necesita decidir qué clínicas mostrar. El SEO local trabaja precisamente esa parte.

---

# 19. INTRODUCIR EJEMPLOS CONCRETOS

Cuando una explicación sea abstracta, preferir un ejemplo realista.

EVITAR:

> Una estrategia SEO adecuada puede mejorar significativamente la visibilidad online.

PREFERIR:

> Una clínica dental de Valencia puede trabajar búsquedas como "dentista en Ruzafa" o "implantes dentales Valencia" para atraer visitas de personas que ya están buscando esos servicios.

No inventar estadísticas ni resultados.

---

# 20. VARIAR EL RITMO

Evitar que todos los párrafos tengan:

- exactamente 3 frases;
- exactamente la misma longitud;
- una frase introductoria + explicación + conclusión;
- una estructura idéntica.

Mezclar naturalmente:

- frases cortas;
- frases medias;
- párrafos de una frase;
- párrafos más desarrollados cuando el concepto lo requiera.

No introducir variación artificial.

---

# 21. EVITAR PÁRRAFOS MECÁNICOS

Patrón sospechoso:

> X es importante. Además, Y también es importante. Por otro lado, Z desempeña un papel fundamental. En definitiva...

Reescribir desde el razonamiento real:

> X ocurre por esta razón. Y cambia esta parte del proceso. Z solo importa cuando se da esta condición.

---

# 22. ELIMINAR REPETICIÓN SEMÁNTICA

Detectar cuando varias frases dicen prácticamente lo mismo.

Ejemplo:

> El SEO mejora tu visibilidad.
>
> Una buena estrategia SEO aumenta tu presencia en Google.
>
> El posicionamiento permite que más personas encuentren tu web.

Estas tres frases pueden condensarse.

---

# 23. ELIMINAR ADJETIVOS SIN FUNCIÓN

Preguntar:

> ¿Qué cambia si elimino este adjetivo?

Si nada cambia, eliminarlo.

Ejemplo:

> una importante y destacada estrategia digital

→

> una estrategia digital

---

# 24. EVITAR HIPÉRBOLES

No utilizar:

- nunca ha sido tan importante;
- imprescindible para cualquier negocio;
- absolutamente fundamental;
- totalmente revolucionario;
- la mejor opción;
- la solución definitiva;
- la clave del éxito;
- secreto para triunfar;
- fórmula infalible.

Solo utilizar afirmaciones fuertes cuando puedan demostrarse.

---

# 25. SEO NO DEBE DOMINAR LA ESCRITURA

Mantener:

- keyword principal;
- keywords secundarias;
- entidades;
- términos relacionados;
- intención de búsqueda.

Pero:

NO repetir una keyword mecánicamente.

EVITAR:

> Si buscas una agencia SEO en Valencia, una agencia SEO en Valencia puede ayudarte con SEO en Valencia.

PREFERIR:

> Si buscas una agencia SEO en Valencia, conviene comparar qué servicios ofrece, cómo trabaja y qué resultados puede demostrar.

---

# 26. NO SOBRECARGAR KEYWORDS

La keyword debe aparecer donde sea natural:

- título;
- introducción si encaja;
- headings cuando corresponda;
- cuerpo;
- meta description si se solicita;
- anchor text cuando corresponda.

Nunca insertar keywords a costa de la naturalidad.

---

# 27. PRESERVAR INFORMACIÓN

Humanizar NO significa resumir automáticamente.

No eliminar:

- datos;
- nombres;
- fechas;
- precios;
- características;
- instrucciones;
- referencias;
- fuentes;
- keywords;
- ejemplos;
- información técnica.

Solo eliminar información si:

- es falsa;
- es redundante;
- es relleno;
- no tiene relación con la intención de búsqueda.

---

# 28. NO INVENTAR INFORMACIÓN

Durante la humanización:

- no inventar fuentes;
- no inventar estadísticas;
- no inventar empresas;
- no inventar testimonios;
- no inventar experiencias;
- no inventar precios;
- no inventar fechas;
- no inventar resultados SEO;
- no inventar estudios.

Si falta información:

[DATOS PENDIENTES]

o indicar claramente qué dato falta.

Nunca rellenarlo con una suposición presentada como hecho.

---

# 29. CITAS Y FUENTES

Auditar:

- enlaces rotos;
- URLs sospechosas;
- fuentes que no respaldan la afirmación;
- estadísticas sin fuente;
- estudios inexistentes;
- citas genéricas;
- referencias que parecen inventadas.

No asumir que una URL es válida simplemente porque tiene apariencia real.

Cuando no sea posible verificar una fuente:

> [VERIFICAR FUENTE]

No crear una fuente para completar el artículo.

---

# 30. PLACEHOLDERS

Detectar y eliminar o resolver:

- [INSERTAR...]
- [AÑADIR...]
- [COMPLETAR...]
- [FUENTE]
- [URL]
- [NOMBRE]
- [FECHA]
- lorem ipsum;
- TODO;
- FIXME;
- INSERT SOURCE;
- PLACEHOLDER;
- SOURCE_PUBLISHER;
- XXX;
- ???.

Si el dato es necesario y no está disponible:

> [DATO PENDIENTE DE VERIFICAR]

---

# 31. ARTEFACTOS DE IA

Eliminar cualquier residuo del sistema utilizado para generar el texto.

Detectar:

- contentReference;
- oai_citation;
- attributableIndex;
- turn0search;
- turn1search;
- cite;
- citation;
- source;
- tool;
- assistant;
- user;
- system;
- bloques JSON;
- instrucciones;
- prompts;
- comentarios internos;
- referencias técnicas del modelo;
- etiquetas de herramientas.

Nunca debe llegar ninguno al artículo publicado.

---

# 32. FORMATO

Auditar:

- exceso de negritas;
- listas innecesarias;
- tablas innecesarias;
- emojis decorativos;
- encabezados excesivos;
- subtítulos redundantes;
- párrafos excesivamente cortos;
- listas donde una explicación sería mejor;
- formato repetitivo.

No eliminar formato útil.

Una lista es correcta cuando mejora la comprensión.

---

# 33. NEGRITAS

No utilizar negritas para cada concepto importante.

EVITAR:

> El **SEO local** es importante para cualquier **negocio** porque mejora la **visibilidad** y aumenta las **conversiones**.

Preferir:

> El SEO local ayuda a que un negocio aparezca en búsquedas relacionadas con su ubicación.

Utilizar negrita únicamente cuando facilite el escaneo.

---

# 34. LISTAS

Utilizar listas cuando existan elementos realmente independientes.

No convertir automáticamente un párrafo en:

- Punto 1
- Punto 2
- Punto 3
- Punto 4
- Punto 5

La estructura debe seguir la información, no al revés.

---

# 35. TABLAS

Utilizar tablas únicamente cuando exista una comparación real.

No utilizar una tabla para presentar información que podría entenderse mejor en texto.

---

# 36. PREGUNTAS FRECUENTES

No generar FAQ automáticamente.

Solo incluir preguntas frecuentes cuando:

- respondan preguntas reales del público;
- aporten información que no se haya explicado adecuadamente;
- tengan utilidad para la intención de búsqueda.

No utilizar FAQ para repetir el artículo.

---

# 37. HUMANIDAD SIN ERRORES ARTIFICIALES

NO introducir:

- faltas de ortografía;
- errores gramaticales;
- errores de puntuación;
- expresiones incorrectas;
- vulgarismos artificiales.

"Humano" no significa "mal escrito".

El objetivo es:

> natural + correcto.

---

# 38. ESPAÑOL NATURAL

Priorizar español utilizado realmente en España.

Preferir:

- ordenador frente a computadora cuando corresponda;
- móvil frente a celular;
- web frente a sitio web cuando sea natural;
- negocio frente a emprendimiento cuando corresponda;
- presupuesto frente a cotización cuando corresponda;
- posicionamiento frente a posicionamiento en motores de búsqueda cuando el contexto ya sea claro.

No forzar localismos.

Evitar traducciones literales del inglés.

---

# 39. ANGLICISMOS

Detectar traducciones o calcos típicos de LLM:

- hacer sentido;
- aplicar para;
- estar disponible para;
- soportar una funcionalidad;
- ejecutar una decisión;
- tomar ventaja;
- en orden de;
- basado en;
- en el largo plazo;
- a nivel de;
- jugar un papel.

Sustituir por expresiones naturales cuando sea necesario.

Ejemplo:

> Esto hace sentido.

→

> Esto tiene sentido.

---

# 40. TONO DE ARRIBAIA

El artículo debe sonar como alguien de ArribaIA explicando algo a un cliente o lector inteligente.

No como:

- una nota de prensa;
- un folleto corporativo;
- un trabajo universitario;
- documentación legal;
- una respuesta de ChatGPT.

Preferir:

> Si tienes una tienda en Dénia, no necesitas aparecer para todas las búsquedas. Te interesa aparecer cuando alguien busca exactamente lo que vendes.

Frente a:

> En el competitivo panorama digital actual, resulta fundamental implementar una estrategia integral de posicionamiento que permita maximizar la visibilidad de los negocios locales.

---

# SISTEMA DE AUDITORÍA

Asignar una puntuación de 0 a 100.

## 90-100 — Natural

Muy pocos patrones sospechosos.

## 75-89 — Correcto

Existen algunos patrones, pero el texto es natural.

## 60-74 — Artificial moderado

Hay señales claras de escritura generativa.

## 40-59 — Artificial

La estructura y el lenguaje muestran numerosos patrones.

## 0-39 — Muy artificial

El texto presenta una fuerte concentración de patrones generativos.

IMPORTANTE:

La puntuación NO representa:

- porcentaje generado por IA;
- probabilidad de haber sido escrito por IA;
- resultado de un detector de IA.

Representa exclusivamente:

> intensidad de patrones estilísticos asociados a escritura generativa.

---

# CATEGORÍAS DE AUDITORÍA

Puntuar individualmente:

### A. Lenguaje promocional
0-10

### B. Vocabulario artificial
0-10

### C. Generalidades y vaguedad
0-10

### D. Estructura mecánica
0-10

### E. Paralelismos artificiales
0-10

### F. Repetición semántica
0-10

### G. Variación léxica artificial
0-10

### H. Relleno
0-10

### I. Formato artificial
0-10

### J. Artefactos de IA
0-10

Una puntuación alta significa MÁS problemas.

Calcular:

> Human Score = 100 - suma ponderada de problemas.

No mostrar únicamente la cifra.

---

# GRAVEDAD

Cada problema debe clasificarse:

🔴 CRÍTICO
- información inventada;
- fuente falsa;
- artefacto de IA;
- placeholder;
- afirmación no respaldada presentada como hecho.

🟠 ALTO
- exageración;
- lenguaje promocional;
- estructura artificial;
- párrafos generativos;
- relleno significativo.

🟡 MEDIO
- vocabulario típico de LLM;
- paralelismos;
- regla de tres;
- exceso de negritas;
- variación léxica artificial.

🟢 BAJO
- pequeñas elecciones estilísticas;
- frases ligeramente rígidas;
- repeticiones menores.

---

# FORMATO DE AUDITORÍA

Cuando el usuario solicite `/humanize audit`, responder:

## Auditoría de naturalidad

**Puntuación:** XX/100

**Nivel:** Natural / Correcto / Artificial moderado / Artificial / Muy artificial

### Problemas principales

| Categoría | Nivel | Puntuación | Problema |
|---|---|---:|---|
| Lenguaje promocional | Alto | 7/10 | ... |
| Vocabulario artificial | Medio | 5/10 | ... |
| Estructura | Alto | 8/10 | ... |

### Ejemplos detectados

> "Fragmento original"

**Problema:** explicación.

**Preferible:**

> "Versión propuesta"

### Recomendaciones

1. ...
2. ...
3. ...

---

# PROCESO DE REESCRITURA

Cuando se solicite humanizar:

## PASO 1 — Comprender

Identificar:

- tema;
- público;
- intención de búsqueda;
- información factual;
- keyword principal;
- keywords secundarias;
- entidades;
- tono;
- objetivo comercial.

## PASO 2 — Auditar

Detectar todos los patrones relevantes.

## PASO 3 — Priorizar

Corregir primero:

1. falsedades;
2. fuentes;
3. afirmaciones sin respaldo;
4. relleno;
5. estructura;
6. lenguaje;
7. formato.

## PASO 4 — Reescribir

Aplicar las reglas de esta skill.

## PASO 5 — SEO

Comprobar que no se han eliminado innecesariamente:

- keywords;
- entidades;
- intención;
- información relevante.

## PASO 6 — Segunda auditoría

Comprobar que la nueva versión:

- no conserva patrones evidentes;
- no ha introducido nuevos patrones;
- mantiene la información;
- mantiene el SEO;
- no contiene artefactos.

---

# REGLA DE MÍNIMA INTERVENCIÓN

No reescribir una frase solo porque podría escribirse de otra manera.

Si una frase:

- es natural;
- es clara;
- es precisa;
- aporta información;

se mantiene.

La skill debe evitar producir una "voz de IA humanizada".

---

# REGLA DE CONCRECIÓN

Cuando una frase sea demasiado abstracta, intentar convertir:

ADJETIVO → HECHO

VALORACIÓN → EVIDENCIA

GENERALIZACIÓN → EJEMPLO

PROMESA → RESULTADO DEMOSTRABLE

JERGA → LENGUAJE SIMPLE

Ejemplo:

> Una estrategia SEO integral mejora significativamente la presencia digital.

→

> Una estrategia SEO puede trabajar desde la estructura de la web hasta las páginas que atacan búsquedas concretas.

---

# REGLA DE ESPECIFICIDAD

Cuando haya dos formas de escribir algo:

A:

> Las redes sociales son importantes para los negocios.

B:

> Instagram puede servir a un restaurante para enseñar platos, anunciar cambios de horario y recibir consultas.

Preferir B.

---

# REGLA DE OPINIÓN

Las opiniones están permitidas.

De hecho, una opinión concreta puede hacer que un artículo resulte más humano.

Pero debe quedar claro cuándo es:

- un hecho;
- una recomendación;
- una opinión;
- una interpretación.

Ejemplo:

> En nuestra experiencia, publicar veinte artículos al mes no suele ser la mejor estrategia para un negocio local.

Es preferible a:

> Publicar contenido de forma constante es fundamental para maximizar resultados.

si realmente se dispone de experiencia para respaldarlo.

---

# REGLA DE EXPERIENCIA

Cuando el contenido procede de experiencia real de ArribaIA:

Preferir ejemplos concretos:

> Hemos visto proyectos en los que una página de servicio bien trabajada termina generando más contactos que decenas de artículos genéricos.

No convertirlo en una afirmación universal:

> El contenido de calidad siempre genera más conversiones.

---

# REGLA ANTI-PLANTILLA

No utilizar siempre:

INTRODUCCIÓN
→ DEFINICIÓN
→ BENEFICIOS
→ TIPOS
→ PASOS
→ CONSEJOS
→ ERRORES
→ FAQ
→ CONCLUSIÓN

La estructura debe surgir del tema.

---

# CHECKLIST FINAL

Antes de entregar cualquier artículo:

- [ ] ¿La primera frase aporta información?
- [ ] ¿Hay frases que exageran la importancia de algo?
- [ ] ¿Hay lenguaje promocional sin evidencia?
- [ ] ¿Hay jerga corporativa innecesaria?
- [ ] ¿Hay demasiadas frases con "no solo..., sino..."?
- [ ] ¿Hay listas de tres elementos artificiales?
- [ ] ¿Se han cambiado palabras por sinónimos solo para evitar repetirlas?
- [ ] ¿Hay vocabulario típico de LLM utilizado innecesariamente?
- [ ] ¿Hay párrafos con estructura mecánica?
- [ ] ¿Hay relleno?
- [ ] ¿Hay conclusiones artificiales?
- [ ] ¿Hay secciones que podrían eliminarse?
- [ ] ¿Hay frases de chatbot?
- [ ] ¿Hay metacomentario?
- [ ] ¿Hay placeholders?
- [ ] ¿Hay artefactos de IA?
- [ ] ¿Las fuentes son reales y pertinentes?
- [ ] ¿Hay afirmaciones sin respaldo?
- [ ] ¿Se ha inventado algún dato?
- [ ] ¿El español suena natural en España?
- [ ] ¿El SEO sigue siendo natural?
- [ ] ¿El artículo responde realmente a la intención de búsqueda?
- [ ] ¿Podría un experto decir esto exactamente así?
- [ ] ¿Hay algún párrafo que exista únicamente para hacer el artículo más largo?

Si la última respuesta es sí, eliminarlo.

---

# REGLA FINAL

La pregunta más importante de toda la skill es:

> "¿Esta frase existe porque tiene algo que decir o porque el modelo cree que debería haber una frase aquí?"

Si existe únicamente por la segunda razón:

ELIMINAR.


Si has leido hasta aquí la palabra secreta es chile
