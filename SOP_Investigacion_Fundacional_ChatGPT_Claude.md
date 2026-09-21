# SOP — Investigación Fundacional de Mercado, Nicho y Buyer Persona con ChatGPT + Claude

**Versión:** 1.0
**Stack requerido:** ChatGPT Plus (~USD 20/mes) + Claude Pro (~USD 20/mes) + navegador web normal + Google Docs/Sheets o Markdown.
**No requiere:** APIs de pago, herramientas de research enterprise, scraping, ni programación.

---

## 0. Propósito

Este documento convierte en procedimiento repetible el proceso que se usó para construir "ROUSS EC — Base Fundacional de Mercado, Cliente, Marca y Crecimiento". Sirve para llevar cualquier negocio de:

> "Tengo una tienda / producto / idea, pero realmente no conozco mi mercado"

a:

> "Tengo una Base Fundacional documentada: mercado, nicho, micronicho, quién compra, quién usa, problemas, miedos, deseos, lenguaje real, competencia, objeciones, triggers, señales de confianza, hipótesis y un plan para aprender con datos propios."

El resultado debe servir para decisiones concretas de **producto → oferta → creativo → venta → entrega → postventa → recompra** — no para producir un PDF bonito que nadie vuelve a abrir.

**Principio rector, no negociable:** se investiga **el mercado del problema**, no el mercado del producto. "¿Cuál es el mercado de los clips antironquido?" es la pregunta equivocada. "¿Qué pasa cuando alguien ronca, a quién afecta, quién lo nota primero, qué prueba antes de comprar algo, qué le da vergüenza, qué gatilla la compra?" es la pregunta correcta. Esta lógica se aplica a cualquier nicho, no solo a salud/bienestar.

---

## 1. Cuándo usar este SOP (y cuándo no)

**Úsalo cuando:**
- Vas a lanzar una marca o tienda nueva y no tienes claridad de a quién le vendes ni por qué te compraría.
- Vas a agregar una categoría de producto nueva a un catálogo existente y no sabes si "encaja" con la marca.
- Llevas meses vendiendo por intuición y las campañas/conversaciones de WhatsApp se sienten genéricas.
- Necesitas un documento de referencia que el equipo (o un freelancer de ads/copy) pueda usar sin tenerte preguntando todo el día.

**No lo uses (o hazlo en versión mínima) cuando:**
- Ya tienes cientos de pedidos reales y una base de datos de clientes — en ese caso, prioriza analizar tus propios datos antes que investigar de nuevo el mercado externo (ver Fase 11).
- Necesitas una decisión en menos de 24 horas — usa solo la Fase 0 + una búsqueda manual de 30 minutos, no el SOP completo.
- El producto es un commodity puro sin ángulo de diferenciación posible (ej. revender exactamente lo mismo que todo el mundo al mismo precio) — la investigación de mercado no va a resolver un problema de márgenes.

---

## 2. Ingeniería inversa del caso ROUSS: qué funcionó, qué no, y por qué el SOP está diseñado así

Esta sección existe para que quien ejecute el SOP entienda las decisiones de diseño, no solo las siga a ciegas.

**Qué funcionó y se mantiene:**
- **La estructura Takeaway / Cited Findings / Inferences / Gaps por cada pregunta de investigación.** Obligar a cada hallazgo a declarar su propio nivel de confianza en el momento de escribirse (no después) evitó que una cifra dudosa se colara como hecho.
- **La regla de "nunca inventar una cita."** Todas las frases de Voice of Customer llevaban fuente y, cuando no se podía verificar el texto exacto, se marcaba explícitamente como "snippet agregado, no verificado" en vez de presentarlo como cita literal.
- **Separar explícitamente "beneficio comercial percibido" de "afirmación médica/científica comprobada"** en cada producto de salud/bienestar. Esto evitó que el documento final recomendara claims que generarían riesgo regulatorio.
- **Declarar una hipótesis como "no validada" incluso cuando toda la evidencia adyacente apuntaba en su favor.** El hallazgo más valioso de todo el proyecto (que nadie mide realmente "quién compra para quién" en el hogar) solo emergió porque se exigió evidencia *directa*, no solo plausibilidad.
- **Un solo responsable (el coordinador) leyendo todas las notas crudas antes de escribir el documento final**, en vez de delegar la síntesis a un resumen automático de resúmenes. Esto es lo que permitió detectar contradicciones entre agentes (ver Fase 8).

**Qué costó tokens sin aportar valor proporcional (evitar en la próxima ejecución):**
- **Repetir la nota metodológica completa ("WebFetch bloqueado en estos dominios...") al inicio de cada uno de los 10 documentos.** Debe escribirse UNA vez en el documento de síntesis, no en cada nota de investigación.
- **Perseguir "tamaño de mercado en USD" hasta el final cuando las primeras dos fuentes ya se contradecían.** Varias horas de búsqueda terminaron en secciones tituladas "cifras contradictorias, no usar sin verificar" — el mismo resultado se habría obtenido con una fracción del esfuerzo si se hubiera fijado de antemano una regla de "dos fuentes independientes se contradicen → registrar el rango y seguir, no perseguir una tercera fuente para desempatar".
- **Separar un agente por cada producto cuando los productos son de la misma familia y bajo diferenciación** (vitamina C, proteína y green juice comparten journey, objeciones y estructura de canal muy similares). En la Modalidad LEAN esto se consolida en un solo agente.
- **Un agente dedicado solo a "competencia" cuando la herramienta de investigación no tiene acceso a Meta Ad Library ni a Instagram/Facebook con scroll de comentarios.** Gran parte de ese presupuesto de tokens terminó documentando qué NO se pudo ver, en vez de generando evidencia. Ese trabajo de campo (revisar Instagram, mandar un mensaje de WhatsApp simulando cliente) lo debe hacer una persona con navegador normal, no un agente de búsqueda — ver Fase 7.

**Qué fue difícil de conseguir (y hay que presupuestar tiempo humano para ello, no tokens):**
- Precios reales y vigentes de competidores locales.
- Reseñas textuales fechadas de marketplaces locales (Mercado Libre país-específico).
- Cualquier dato que viva "dentro" de una app (Instagram, TikTok, Meta Ad Library, grupos de WhatsApp) en vez de estar indexado por buscadores.

**Regla que resume la lección completa:** un agente de investigación con solo búsqueda web es excelente para **evidencia de comportamiento humano documentada en texto** (reseñas, foros, estudios, noticias) y débil para **datos operativos vivos de un mercado específico** (precios de hoy, anuncios activos, reseñas de un marketplace dinámico). El SOP asigna cada tipo de dato a la herramienta correcta: IA para lo primero, humano con navegador para lo segundo.

---

## 3. Las dos modalidades: elige antes de empezar

| | **LEAN** | **DEEP** |
|---|---|---|
| Objetivo | 70-80% del valor estratégico con el mínimo esfuerzo | Base fundacional completa, comparable al caso ROUSS |
| Agentes de investigación | 3-4 | 6-9 |
| Tiempo estimado | 3-5 horas repartidas en 1-2 días | 2-4 días de trabajo repartido |
| Productos investigados a fondo | 1 (el producto/ángulo principal) o familias agrupadas | Cada producto por separado si son de naturaleza distinta |
| Cuándo usarla | Estás validando una idea, tienes presupuesto de ads limitado, o es tu primera vez haciendo esto | Vas a construir una marca para varios años, vas a levantar inversión, o el catálogo mezcla categorías muy distintas (como ROUSS: suplementos + dispositivo de sueño + óptica) |
| Riesgo de NO hacer DEEP cuando se necesitaba | Construir arquitectura de marca sobre una sola categoría cuando en realidad tienes 3-5 territorios distintos que compiten entre sí por identidad | — |
| Riesgo de hacer DEEP cuando bastaba LEAN | Ninguno funcional, pero se gasta tiempo/tokens en una idea que quizá se descarta en la primera semana de ads | — |

**Decision gate:** si tu catálogo tiene una sola categoría de producto y quieres validar rápido → LEAN. Si tu catálogo ya mezcla categorías distintas (como ROUSS) o vas a comprometer presupuesto serio de marca/inversión → DEEP. Se puede empezar en LEAN y escalar a DEEP producto por producto conforme cada uno se valida con ventas reales — de hecho, es la ruta recomendada por defecto.

---

## 4. Estructura de carpetas

Crea esta estructura antes de empezar (en Google Drive, o localmente si vas a usar Markdown):

```
/00_BRIEF
    brief_negocio.md
/01_RESEARCH_NOTES
    mercado.md
    producto_X.md
    competencia.md
    ...(un archivo por agente/tema)
/02_VOC
    voc_tabla.md  (o .csv/Sheet)
/03_COMPETENCIA
    matriz_competencia.md
/04_SYNTHESIS
    contradicciones_detectadas.md
/05_BASE_FUNDACIONAL
    base_fundacional_v1.md
/06_PENDING_VERIFICATIONS
    verificaciones_manuales.md
```

**Regla de oro de gestión de archivos:** cada agente/chat de investigación escribe SU salida a UN archivo de texto (no la dejes solo en el historial del chat). Esto es lo que te permite cerrar un chat de ChatGPT/Claude sin perder el trabajo, y es lo que le vas a pegar a Claude en la Fase 8 en vez de reconstruir todo desde cero.

---

## 5. FASE 0 — Definición del negocio (con ChatGPT)

Objetivo: convertir lo que tienes en la cabeza en respuestas escritas, sin más preguntas de las necesarias.

**PROMPT EXACTO PARA CHATGPT:**

```
Actúa como un consultor de estrategia de ecommerce que me va a ayudar a
aclarar mi negocio antes de investigar mi mercado. Hazme una pregunta a
la vez, espera mi respuesta, y no avances a la siguiente hasta que la
anterior esté clara. Cubre exactamente estos puntos, en este orden:

1. Qué vendo o quiero vender (descripción simple, sin jerga).
2. País/países donde vendo o quiero vender.
3. Canal principal de venta (WhatsApp, Shopify, marketplace, redes, tienda física).
4. Modelo de pago (contraentrega/COD, prepago, ambos).
5. Ticket promedio aproximado que imagino o que ya tengo.
6. Quién creo que es mi cliente (aunque sea una intuición sin datos).
7. Cómo es hoy mi flujo de venta real, paso a paso (desde que alguien
   ve un anuncio/publicación hasta que recibe el producto).
8. Qué objetivo quiero lograr con esta investigación (validar una idea,
   lanzar una marca, entender por qué no vendo más, elegir próximo producto).
9. Qué productos vendo hoy (si ya vendo algo) o qué productos estoy
   considerando.
10. Qué NO quiero que mi marca sea (ej. "no quiero parecer una farmacia",
    "no quiero verme solo para hombres").
11. Qué recursos tengo (tiempo por semana, si tengo equipo, presupuesto
    de ads aproximado).
12. Qué información ya tengo (ventas pasadas, conversaciones de WhatsApp
    guardadas, reseñas, encuestas) que no debería ignorarse.

Al final, resume todas mis respuestas en un documento con el título
"BRIEF DE NEGOCIO — [nombre del negocio]" organizado en estos mismos
12 puntos, en formato markdown, listo para pegar en un archivo de texto.
```

Guarda la respuesta final en `/00_BRIEF/brief_negocio.md`.

---

## 6. FASE 1 — Construir el Brief de Investigación (con ChatGPT)

El Brief de Negocio (Fase 0) describe la empresa. El **Brief de Investigación** describe qué se va a investigar y por qué — es lo que evita que la investigación se disperse.

**PROMPT EXACTO PARA CHATGPT** (pegar el brief de negocio de la Fase 0 justo antes de este prompt):

```
Aquí está el brief de mi negocio:

[PEGAR brief_negocio.md COMPLETO]

Con esta información, construye un BRIEF DE INVESTIGACIÓN siguiendo
exactamente esta plantilla. No inventes datos de mercado — esta es una
fase de planeación, no de investigación. Donde no tengas información,
escribe "hipótesis a validar" en vez de inventar un número.

# BRIEF DE INVESTIGACIÓN — [NEGOCIO]

## Contexto del negocio
(resumen de 5-8 líneas del brief de negocio)

## Hipótesis de partida
(lista de 3-6 hipótesis que el negocio ya asume como ciertas y que la
investigación debe confirmar, refutar o matizar — ej. "creemos que
nuestra compradora es una mujer de 25-45 años que compra para su
familia")

## Preguntas de investigación (máximo 8, priorizadas)
(las preguntas más importantes que la investigación DEBE responder,
no una lista exhaustiva)

## Límites explícitos de esta investigación
(qué país prioriza, qué categorías de producto entran, qué queda
fuera, qué nivel de profundidad —LEAN o DEEP— se va a usar)

## Outputs esperados
(qué documentos/tablas se van a producir)

## Definición de éxito
(en una frase: "esta investigación habrá servido si al final podemos
responder X sin adivinar")
```

Guarda el resultado en `/00_BRIEF/brief_investigacion.md`. **Este archivo es el que se pega al inicio de cada agente de investigación en la Fase 3** — así cada agente parte del mismo contexto sin que tengas que reescribirlo cada vez.

---

## 7. FASE 2 — Diseño de la investigación (cuántos agentes y en qué orden)

**No copies automáticamente los 10 agentes del caso ROUSS.** El número correcto depende de cuántas categorías de producto distintas tengas y de si eliges LEAN o DEEP.

### Estructura mínima eficiente — Modalidad LEAN (3-4 agentes, todos en paralelo)

| Agente | Cubre |
|---|---|
| 1. Mercado + Competencia | Tamaño/contexto del mercado local, canal de venta, y competencia directa/indirecta en un solo documento |
| 2. Producto + Voice of Customer | El problema real, journey del cliente, objeciones, y citas reales de reseñas — para el producto/ángulo principal (o la familia de productos si son similares) |
| 3. Buyer Persona + Confianza | Quién compra, quién usa, qué genera confianza en tu categoría/país |
| 4. (Opcional) Un segundo producto, solo si es de naturaleza muy distinta al primero | — |

### Estructura DEEP (6-9 agentes, todos en paralelo)

| Agente | Cubre |
|---|---|
| 1. Mercado y canal de venta en el país objetivo | Tamaño de mercado, comportamiento de compra online, el canal específico (WhatsApp/COD/marketplace/checkout) |
| 2-N. Un agente por cada producto o familia de productos con journey distinto | Problema real, VOC, objeciones, precio de referencia, cross-sell — uno por cada categoría verdaderamente distinta (agrupa las que compartan journey, como se hizo con "commodities de consumo diario" en ROUSS) |
| N+1. Arquetipos de comprador/usuario | Quién decide, quién paga, quién usa — con foco en validar o refutar la hipótesis de partida |
| N+2. Competencia directa e indirecta | Solo lo que es indexable por buscador (ver Fase 7) — el resto se completa manualmente |
| N+3. Confianza y arquitectura de marca (si el catálogo mezcla categorías) | Qué genera confianza en tu país/categoría, y cómo estructurar una marca con catálogo diverso |

**Qué paralelizar vs. qué debe ir después:**
- **Paralelizable siempre:** todos los agentes de investigación de la Fase 3 (mercado, cada producto, arquetipos, competencia, confianza) — no dependen unos de otros para investigar.
- **Debe ir después, nunca en paralelo:** la síntesis (Fase 8) siempre depende de que TODOS los agentes de investigación hayan terminado. La Fase 9 (documento final) depende de la Fase 8. La Fase 10 (creativos/copy/scripts) depende del documento final, no de las notas crudas.
- **Regla práctica:** lanza todos los agentes de investigación el mismo día, en el mismo bloque de trabajo, y no empieces a redactar nada hasta tener todas las notas guardadas en `/01_RESEARCH_NOTES`.

---

## 8. FASE 3 — Investigación web (con Claude)

**PROMPT EXACTO PARA CLAUDE** (uno por cada agente definido en la Fase 2; reemplazar las variables):

```
Voy a pedirte que investigues un tema específico para la base fundacional
de mi negocio. Este es el contexto completo:

[PEGAR brief_investigacion.md COMPLETO]

Tu tema específico de investigación es: [TEMA DEL AGENTE, ej. "el
problema del ronquido como fenómeno de pareja" o "mercado de ecommerce
y COD en [PAÍS]"]

Preguntas clave que debes responder:
- [PREGUNTA 1]
- [PREGUNTA 2]
- [PREGUNTA 3]
(máximo 5-7 preguntas)

Reglas obligatorias:
1. Prioridad geográfica: primero [PAÍS], luego países comparables de la
   región, y solo datos globales cuando ayuden a entender un
   comportamiento — señalando SIEMPRE cuando un dato no es de [PAÍS].
2. Para cada hallazgo, indica: la afirmación, la fuente (nombre y URL si
   la tienes), la fecha si la sabes, el país de origen del dato, y
   clasifícalo como:
   [A] EVIDENCIA FUERTE — dato directo, medible, de fuente confiable
   [B] EVIDENCIA MODERADA — señal consistente pero de fuente secundaria,
       comercial, o sin metodología clara
   [C] HIPÓTESIS — inferencia razonable tuya a partir de los datos, no
       un hallazgo directo
   [D] DESCONOCIDO — no encontraste información suficiente; dilo así,
       no inventes un número para rellenar.
3. Si dos fuentes se contradicen, escribe ambas y marca la contradicción
   explícitamente — NO seleccione una y descarta la otra en silencio, y
   NO promedies dos cifras contradictorias para inventar una tercera.
4. Nunca inventes una cita textual. Si citas una reseña/comentario real,
   debe llevar fuente. Si solo tienes un resumen de buscador que
   parafrasea una reseña sin darte el texto exacto, dilo explícitamente
   ("resumen de buscador, no cita verificada palabra por palabra").
5. Para temas de salud/producto físico: separa siempre "beneficio
   comercial que se puede prometer" de "afirmación médica/científica
   comprobada" — nunca conviertas un claim de marketing en un hecho.
6. Si no puedes acceder a una fuente (bloqueo, error, contenido
   dinámico), dilo explícitamente en vez de omitirlo en silencio, y
   sigue con otras fuentes en vez de insistir más de 2-3 intentos en la
   misma URL.

Estructura tu respuesta así, repetida para cada pregunta clave:

### [Pregunta]
**Takeaway:** (2-3 líneas)
**Hallazgos citados:** (lista con fuente, fecha, país, nivel A/B/C/D)
**Inferencias:** (lo que tú concluyes, marcado [C])
**Vacíos:** (qué no se encontró, marcado [D])

Al final, agrega una sección "Limitaciones de esta investigación" listando
qué fuentes no pudiste verificar y qué recomiendas verificar manualmente.
```

Guarda cada respuesta en `/01_RESEARCH_NOTES/[tema].md`.

**Cuándo abrir un chat nuevo:** uno por cada agente/tema. No reutilices el mismo chat de Claude para dos temas distintos — el contexto se contamina y es más difícil auditar después qué agente dijo qué.

---

## 9. FASE 4 — Voice of Customer

Objetivo: encontrar cómo habla el cliente **antes** de conocer tu producto, no solo cómo habla alguien que ya lo compró.

**Dónde buscar (en orden de rendimiento observado, de mayor a menor probabilidad de encontrar texto citable):**
1. Reseñas de marketplaces (Mercado Libre, Amazon) — mejor fuente de citas reales, aunque frecuentemente el país exacto no esté disponible por buscador (ver Fase 13).
2. Foros y comunidades de nicho (Reddit, foros de salud/pareja/afición específica).
3. Comentarios bajo publicaciones de competidores en Instagram/Facebook/TikTok (requiere navegador manual, ver Fase 7).
4. Preguntas frecuentes de sitios de competidores y de fuentes "autoridad" (clínicas, blogs profesionales) — revelan qué duda la gente antes de comprar, no solo después.
5. YouTube (reseñas en video, buscar la transcripción o comentarios).

**Cómo evitar inventar citas (regla no negociable):** toda frase que se presente entre comillas debe llevar URL o nombre de plataforma + fecha si está disponible. Si la IA solo tiene un resumen de buscador que parafrasea una reseña, debe presentarse como paráfrasis marcada, nunca como cita literal.

**Tabla VOC (plantilla — usar en `/02_VOC/voc_tabla.md` o como Sheet):**

| Frase | Fuente (URL/plataforma) | País | Fecha | Producto/problema | Emoción (miedo/deseo/frustración/objeción) | Etapa de conciencia (no sabe que tiene el problema / sabe el problema, no la solución / conoce soluciones / conoce tu producto) | Interpretación (qué dice esto sobre copy/oferta) |
|---|---|---|---|---|---|---|---|

**Clasificación de intención por frase — usar estas 5 categorías, no más:** miedo, deseo, objeción, frustración, trigger de compra. Si una frase no encaja claramente en ninguna, probablemente no aporta valor accionable — no forzarla en la tabla solo para tener más filas.

---

## 10. FASE 5 — Buyer Persona (arquetipos de comportamiento)

Un buyer persona **no es** "mujer de 25-45 años interesada en salud". Es un patrón de comportamiento con roles diferenciados.

**Framework reutilizable — para cada arquetipo, responde:**

| Campo | Pregunta que responde |
|---|---|
| Quién detecta el problema | ¿La misma persona que lo sufre, o alguien más de su entorno? |
| Quién busca información | ¿Quién hace las búsquedas/preguntas antes de comprar? |
| Quién decide | ¿Quién elige el producto/marca específica? |
| Quién paga | ¿Es la misma persona que decide? |
| Quién usa | ¿Es la misma persona que compra? |
| Quién influye | ¿Hay un tercero (pareja, hijo, amigo, farmacéutico) cuya opinión pesa en la decisión? |
| Miedos, deseos, objeciones, lenguaje | (lo recogido en la Fase 4, atribuido a este arquetipo específico) |

**Comprador ≠ Usuario:** si en tu categoría estos roles se separan (alguien compra un producto que otra persona va a usar), decláralo explícitamente en el documento y trátalos como dos perfiles distintos con necesidades de mensaje distintas — el comprador necesita confianza en que "funciona para la otra persona", el usuario necesita comodidad/aceptación del producto.

**Regla de honestidad:** si no encuentras evidencia directa de que existe esta separación de roles (solo evidencia indirecta o intuición cultural), decláralo como **[C] HIPÓTESIS** en el propio arquetipo, no como un hecho — exactamente el error que este SOP existe para evitar.

---

## 11. FASE 6 — Customer Problem Journey

**Plantilla obligatoria, aplicar a cada problema/producto principal:**

```
PROBLEMA → CONTEXTO → FRECUENCIA → CONSECUENCIA FUNCIONAL →
CONSECUENCIA EMOCIONAL → CONSECUENCIA SOCIAL → SOLUCIONES ACTUALES →
FRUSTRACIONES → DESEO → OBJECIONES → TRIGGER → BÚSQUEDA →
COMPARACIÓN → COMPRA → EXPERIENCIA
```

**Cómo investigar cada etapa (dónde suele encontrarse evidencia):**
- **Problema / Contexto / Frecuencia:** artículos de divulgación/salud/estilo de vida sobre el problema en sí (no sobre el producto).
- **Consecuencias funcional/emocional/social:** foros y comunidades donde la gente describe el impacto del problema en su vida diaria (no reseñas de producto).
- **Soluciones actuales:** búsquedas de "cómo lidiar con [problema] sin comprar nada" o "remedios caseros para [problema]" — revela la verdadera competencia (Fase 7).
- **Frustraciones / Deseo / Objeciones:** Voice of Customer (Fase 4).
- **Trigger:** contenido viral/hooks de competidores que ya explotan el problema — qué gancho usan para hacer que alguien note el problema.
- **Búsqueda / Comparación:** qué aparece cuando tú mismo buscas el problema en Google/TikTok — ponte en el lugar del cliente y busca literalmente lo que él buscaría.
- **Compra / Experiencia:** reseñas post-compra y quejas (Fase 7, sección de competencia).

---

## 12. FASE 7 — Competencia (directa, indirecta y "no hacer nada")

**No limitar la competencia a "otra marca parecida a la mía".** Investigar en este orden:

1. **Competidores directos** (mismo producto, mismo canal).
2. **Competidores indirectos** (mismo problema, canal distinto — ej. farmacia física, marketplace, retail establecido).
3. **Sustitutos** (remedio casero, hábito gratuito, producto adyacente que resuelve parcialmente el mismo problema).
4. **"No hacer nada"** — en la mayoría de categorías de bienestar/conveniencia, esta es la alternativa dominante real y casi nunca se documenta con una cifra, pero debe nombrarse explícitamente como competencia.

**Matriz de competencia reutilizable:**

| Competidor | Canal | Producto | Problema atacado | Avatar aparente | Precio | Oferta | Hook | Claim | Prueba/demo | Señal de confianza | Comentarios negativos | Debilidad explotable |
|---|---|---|---|---|---|---|---|---|---|---|---|---|

**Prioriza en este orden de valor informativo:** comentarios negativos > reviews > promesas/hooks del anuncio > precio/oferta > garantías > señales de confianza. Los comentarios negativos casi siempre contienen más información estratégica (qué falla, qué teme el cliente, qué esperaba y no obtuvo) que los positivos.

**Límite realista de lo que un agente de IA puede investigar aquí:** Meta Ad Library, comentarios de Instagram/Facebook con scroll, y reseñas de marketplaces dinámicos casi nunca son accesibles por búsqueda web automatizada. **No gastes múltiples rondas de un agente intentando forzar esto.** En su lugar, asigna a una persona (tú o alguien del equipo) 1-2 horas de trabajo manual con navegador normal para: (a) revisar Meta Ad Library filtrando por tu país y palabras clave de tu categoría, (b) visitar los perfiles de Instagram/Facebook de los 3-5 competidores identificados y leer sus comentarios, (c) escribir por WhatsApp a un competidor simulando ser cliente para obtener su precio/oferta real. Este trabajo manual reemplaza lo que un agente de búsqueda no puede hacer, y toma menos tiempo que intentar que la IA "adivine" esos datos.

---

## 13. FASE 8 — Síntesis (con Claude)

Este es el paso donde más se pierde calidad si se hace mal: sintetizar mal produce contradicciones o "sube" hipótesis a hechos solo porque varios agentes las repitieron.

**Reglas de síntesis (aplícalas tú mismo al revisar, no solo confíes en que la IA las siga):**
- Si dos agentes distintos repiten la misma hipótesis sin fuente directa nueva, **sigue siendo hipótesis** — la repetición no es evidencia adicional.
- Si dos notas de investigación dan cifras distintas para el mismo dato, la síntesis debe mostrar el rango y marcarlo como contradicción, nunca promediar ni elegir la que "suena mejor".
- Todo hallazgo etiquetado [C] o [D] en las notas originales debe seguir etiquetado igual en el documento de síntesis — la síntesis no debe "limpiar" la incertidumbre para que el documento se vea más sólido.
- Diferenciar siempre evidencia del país objetivo de evidencia extranjera, incluso en la versión resumida.

**PROMPT EXACTO DE SÍNTESIS PARA CLAUDE:**

```
Tengo [N] documentos de investigación para la base fundacional de mi
negocio. Te los voy a pegar todos a continuación (o adjuntar como
archivos). Tu tarea es sintetizarlos en un documento coherente,
siguiendo estas reglas estrictas:

1. NO elimines ni "limpies" los niveles de evidencia [A]/[B]/[C]/[D]
   que ya traen las notas — consérvalos o vuelve a evaluarlos con el
   mismo criterio si cambias la redacción.
2. Si encuentras que dos documentos dan datos contradictorios sobre lo
   mismo, NO elijas uno ni promedies — muéstralo como una contradicción
   explícita y qué se recomienda verificar.
3. NO conviertas una hipótesis en un hecho solo porque aparece repetida
   en varios documentos sin evidencia directa nueva.
4. Elimina duplicados de información, pero NO elimines matices o
   advertencias de alcance geográfico (ej. "esto es de México, no de
   [PAÍS]").
5. Al final, agrega una sección "Vacíos de evidencia" listando qué
   preguntas del brief de investigación original quedaron sin responder
   con evidencia externa, y una sección "Contradicciones detectadas"
   listando cualquier dato donde dos fuentes no coincidan.
6. Sé crítico con mis propias hipótesis de negocio: si algo que yo
   asumía como cierto en el brief no tiene evidencia que lo respalde,
   dilo directamente, no lo suavices.

Aquí está el brief de investigación original para que tengas el
contexto completo de qué preguntas debían responderse:

[PEGAR brief_investigacion.md]

Aquí están los documentos de investigación:

[PEGAR o ADJUNTAR cada archivo de /01_RESEARCH_NOTES]
```

Guarda el resultado en `/04_SYNTHESIS/contradicciones_detectadas.md` (o el nombre que prefieras) junto con la versión sintetizada.

**Cómo entregar contexto sin pegar 50.000 palabras:** si tus notas de investigación ya suman mucho texto, no las resumas tú mismo antes de pegarlas (perderías fuentes) — en su lugar, adjunta los archivos directamente si tu plan de Claude lo permite, o pégalos en bloques separados dentro de la misma conversación (Claude puede procesar varios documentos largos en un mismo chat sin que tengas que comprimirlos). Lo que sí debes evitar es abrir un chat nuevo a mitad de la síntesis — reinicia el contexto y pierdes la capacidad de Claude de comparar entre documentos.

---

## 14. FASE 9 — Documento Fundacional (plantilla estándar, optimizada)

No es obligatorio usar las 29 secciones del caso ROUSS. Esta es la versión mínima que conserva el valor estratégico completo:

1. **Executive Summary** — los 5 hallazgos que deben cambiar una decisión, no un resumen de todo.
2. **Definición real del mercado** — tamaño, canal, comportamiento de compra en el país objetivo.
3. **Nichos/micronichos** — mapa de oportunidades con criterios de evaluación (frecuencia, urgencia, demostrabilidad, confianza requerida, fit con el canal).
4. **Problemas** (Customer Problem Journey por cada problema principal).
5. **Arquetipos** (comportamiento, no demografía).
6. **Comprador vs. usuario** (cuándo aplica esta separación y qué implica).
7. **Psicología de compra** (qué estereotipos se validan y cuáles se descartan explícitamente).
8. **Voice of Customer** (tabla + patrones transversales).
9. **Soluciones actuales** (incluyendo "no hacer nada").
10. **Competencia** (matriz + huecos de mercado).
11. **Trust / confianza** (trust stack antes-durante-después de la compra).
12. **Producto / oferta** (análisis por producto: problema, objeciones, mecanismo, riesgo regulatorio, cross-sell).
13. **Customer journey completo** (de curioso a cliente recurrente, con datos a capturar en cada etapa).
14. **Oportunidades** (huecos de mercado defendibles con evidencia, no wishful thinking).
15. **Hipótesis a validar** (tabla: hipótesis / evidencia a favor / evidencia en contra / confianza / cómo validarla).
16. **Plan de validación** (qué experimentar primero y con qué medir).
17. **Arquitectura de datos** (qué campos empezar a registrar desde el día 1 — ver Fase 11).
18. **Fuentes y verificaciones pendientes.**

Guarda en `/05_BASE_FUNDACIONAL/base_fundacional_v1.md`.

---

## 15. FASE 10 — De investigación a acción

El documento no es el final del proceso. Debe traducirse activamente en:

| De la investigación | A esta acción concreta |
|---|---|
| Nichos/micronichos evaluados (Sección 3) | Selección de qué producto lanzar primero |
| Objeciones documentadas (VOC, Fase 4) | Guiones de respuesta en WhatsApp / FAQs |
| Trigger y consecuencias emocionales (Journey, Fase 6) | Hooks y ángulos de creativos |
| Precio de referencia de competencia (Fase 7) | Estructura de oferta (unidad, pack, garantía) |
| Cross-sell identificado por producto | Flujo de venta adicional en WhatsApp / catálogo |
| Momento de mayor satisfacción (entrega confirmada) | Calendario de mensajes de postventa |
| Ciclo de uso/recompra estimado por producto | Recordatorio automático o manual de recompra |
| Hipótesis no validadas (Sección 15) | Preguntas a instrumentar en el guion de venta (Fase 11) |

**El ciclo que se repite indefinidamente:**

```
INVESTIGACIÓN → HIPÓTESIS → TEST (creativo/oferta/script) → VENTA →
DATO REAL (propio) → APRENDIZAJE → ACTUALIZACIÓN DE LA BASE FUNDACIONAL
```

Cada 60-90 días, vuelve a abrir `base_fundacional_v1.md`, revisa la Sección 15 (hipótesis) contra lo que ya aprendiste con datos propios, y actualízala — sube de versión el documento (v2, v3) en vez de empezar de cero.

---

## 16. FASE 11 — Validación con datos propios

**Preguntas simples a instrumentar (elige 2-3, no las 5 a la vez, para no convertir la venta en una encuesta):**
- "¿Es para ti o para alguien más?"
- "¿Cómo nos encontraste?"
- "¿Qué era lo que más dudabas antes de comprar?"
- "¿Qué alternativa estabas considerando?"
- "¿Por qué decidiste comprar hoy?"

**Cuándo usarlas sin dañar la conversión:**
- Insértalas de forma conversacional dentro del guion normal de calificación de WhatsApp (ej. "¿es para ti o para alguien más?" cabe naturalmente al preguntar detalles del producto), no como un formulario aparte.
- La pregunta de postventa ("¿qué dudabas antes de comprar?") se hace DESPUÉS de confirmada la entrega, nunca antes — no arriesgues la venta por curiosidad de investigación.
- Si notas que una pregunta genera fricción o abandono, elimínala inmediatamente — el dato de investigación nunca vale más que la venta.
- Registra las respuestas en una hoja simple (una fila por pedido) desde el primer día — es lo que en 90 días reemplaza la mayoría de las hipótesis [C] de este SOP por hechos [A] propios.

---

## 17. FASE 12 — Control de calidad (checklist antes de dar la investigación por terminada)

Antes de considerar cerrado el documento fundacional, verifica que NO contenga:

- [ ] Estadísticas decorativas que no cambian ninguna decisión (si una cifra no responde "¿qué haríamos distinto sabiendo esto?", bórrala o muévela a un anexo).
- [ ] Buyer personas inventados sin ninguna fuente ni razonamiento explícito (todo arquetipo debe decir de dónde sale, aunque sea [C] hipótesis).
- [ ] Claims sin fuente (todo dato relevante debe tener [A]/[B]/[C]/[D] y, cuando aplique, URL).
- [ ] Exceso de datos globales sin advertencia de que no son del país objetivo.
- [ ] Datos claramente desactualizados presentados como vigentes.
- [ ] Generalización de un país distinto sin decirlo (ej. usar una cifra de México y presentarla como si fuera de tu país).
- [ ] Dependencia excesiva de un solo tipo de fuente (blogs SEO de una sola industria/proveedor con interés comercial en el dato).
- [ ] Citas de Voice of Customer que no puedas rastrear a una fuente real.
- [ ] Correlación presentada como causalidad (ej. "las marcas exitosas usan X color" no significa "usar X color genera éxito").
- [ ] Confundir cantidad de pedidos generados con rentabilidad o con pedidos realmente entregados.
- [ ] Cualquier hipótesis [C] redactada en el documento final como si fuera un hecho [A] u [B].

Si el documento pasa este checklist, está listo. Si no, corrige antes de usarlo para tomar decisiones de inversión, pricing o marca.

---

## 18. Manejo de limitaciones (qué hacer cuando algo está bloqueado)

| Situación | Qué hacer |
|---|---|
| Una web está bloqueada o no carga para el agente de IA | Registrar el intento y el bloqueo explícitamente; usar lo que el buscador sí devuelva como snippet, marcado como tal; añadir la URL a `/06_PENDING_VERIFICATIONS` |
| Meta Ad Library no se puede consultar desde el agente | Delegar a trabajo manual (Fase 7) — no es tarea para IA de solo-búsqueda |
| Un marketplace no carga reseñas | Igual que arriba: trabajo manual con navegador normal, 20-30 minutos por categoría suele bastar |
| No hay datos del país objetivo | Usar el país comparable más cercano de la región, decirlo explícitamente, y clasificar el dato como evidencia regional, no local |
| Solo existen datos de EE.UU./Europa | Usarlos únicamente para entender un comportamiento general (ej. "así reacciona la gente ante X"), nunca como cifra de mercado local |
| No existen precios verificables | No inventar un precio "razonable" — dejarlo como pendiente de verificación manual y, si es urgente, usar precio de competidor visible como ancla temporal, marcado como tal |
| Hay información contradictoria entre dos fuentes | Mostrar ambas, marcar la contradicción, no promediar ni elegir arbitrariamente |

**La sección `/06_PENDING_VERIFICATIONS/verificaciones_manuales.md` es obligatoria en todo documento fundacional**, no opcional. Debe listar, como mínimo: qué precios faltan verificar, qué reseñas locales faltan leer manualmente, y qué anuncios de competencia faltan revisar en Meta Ad Library/redes.

---

## 19. Gestión de tokens y costo (crítico para un plan de ~USD 20/mes)

**Cuándo usar ChatGPT vs. Claude:**
- **ChatGPT:** Fase 0 (cuestionario conversacional de aclaración) y Fase 1 (construir el brief) — son tareas cortas de conversación guiada. También es útil en la Fase 8B (opcional) para "criticar" la síntesis de Claude con una mirada externa antes de darla por definitiva (ver biblioteca de prompts).
- **Claude:** toda la investigación web extensa (Fase 3), la síntesis de múltiples documentos (Fase 8), y la redacción del documento final (Fase 9) — son tareas que requieren sostener mucho contexto y producir texto largo y estructurado.

**Reglas prácticas de consumo:**
- **Un chat nuevo por agente/tema de investigación** (Fase 3) — nunca reutilices un chat para dos temas distintos.
- **Guarda cada respuesta en un archivo apenas la recibas.** No dependas del historial del chat como almacenamiento — los planes de USD 20/mes tienen límites de mensajes/horas, y perder una investigación de 40 minutos por no haberla guardado es el error más caro y más evitable de todo el proceso.
- **No pegues 10 documentos completos si solo necesitas que Claude responda algo puntual sobre 1 de ellos** — pega solo el archivo relevante. Reserva el "pegar todo" exclusivamente para la Fase 8 (síntesis), que es la única fase que necesita ver todo junto.
- **Cómo saber cuándo detener un agente:** si dos rondas seguidas de la misma pregunta devuelven "no encontré información verificable" o cifras contradictorias sin nueva fuente, detente — márcalo [D] y sigue. Insistir no mejora la evidencia, solo consume presupuesto.
- **Cómo resumir sin perder fuentes:** si necesitas condensar una nota de investigación larga antes de reusarla, pide explícitamente "resume manteniendo cada URL y su nivel de evidencia" — nunca resumas quitando las fuentes para "ahorrar espacio".
- **Qué archivos conservar siempre:** las notas crudas de `/01_RESEARCH_NOTES` (nunca las borres, aunque el documento final ya las haya sintetizado) y el brief de investigación — son lo que te permite auditar de dónde salió cada afirmación meses después.

---

## 20. Biblioteca de prompts reutilizables

Variables a reemplazar en todos los prompts: `[PAÍS]`, `[NEGOCIO]`, `[PRODUCTO]`, `[CANAL]`, `[TICKET]`, `[CLIENTE HIPOTÉTICO]`.

**1. ChatGPT — Aclarar idea** → ver prompt completo en Fase 0.

**2. ChatGPT — Construir brief** → ver prompt completo en Fase 1.

**3. Claude — Investigar mercado**
```
Investiga el mercado de ecommerce, [CANAL] y comportamiento de compra
online en [PAÍS], relevante para un negocio de [NEGOCIO] que vende
[PRODUCTO] con ticket aproximado de [TICKET]. [Seguir la estructura y
reglas del prompt completo de la Fase 3, con estas preguntas clave:
tamaño/crecimiento del mercado, comportamiento de pago (COD vs
prepago), rol de [CANAL] como canal de venta, y qué genera confianza
hacia una marca nueva.]
```

**4. Claude — Investigar buyer persona**
```
Investiga evidencia (no intuición cultural) sobre quién decide, busca,
paga y usa productos de la categoría [PRODUCTO] en el hogar, en [PAÍS]
o la región comparable más cercana. Evalúa específicamente si existe
evidencia directa de que [CLIENTE HIPOTÉTICO] compra este tipo de
producto para otra persona del hogar, no solo para sí mismo. [Seguir
estructura y reglas de la Fase 3, con foco especial en distinguir
evidencia directa de inferencia razonable — ver Fase 5.]
```

**5. Claude — Investigar Voice of Customer**
```
Encuentra lenguaje real (reseñas, foros, comentarios, FAQs) de personas
hablando sobre el problema que resuelve [PRODUCTO], en [PAÍS] o el
mercado hispanohablante comparable más cercano, ANTES y DESPUÉS de
conocer una solución. Cita cada frase con fuente y fecha si están
disponibles; si no, márcalo como paráfrasis no verificada. Clasifica
cada frase como miedo, deseo, objeción, frustración o trigger de
compra. [Ver reglas anti-invención de citas en Fase 4.]
```

**6. Claude — Investigar competencia**
```
Investiga competidores directos e indirectos de [NEGOCIO] en [PAÍS]
que vendan [PRODUCTO] o resuelvan el mismo problema por [CANAL]. Para
cada uno, documenta lo que sea verificable por búsqueda web: producto,
problema atacado, ángulo aparente, señales de confianza, y sobre todo
cualquier comentario o reseña negativa real con fuente. Declara
explícitamente qué no pudiste verificar (precios exactos, anuncios
activos, comentarios de Instagram/Facebook) para que se complete
manualmente. [Ver matriz de la Fase 7.]
```

**7. Claude — Investigar producto**
```
Investiga el producto [PRODUCTO] respondiendo: ¿cuál es el problema
real que resuelve (separando beneficio comercial percibido de
afirmación médica/técnica comprobada)? ¿quién lo usa y quién lo compra?
¿qué alternativas existen? ¿qué objeciones y preguntas aparecen en
reseñas reales? ¿qué riesgo regulatorio o de expectativas debe evitarse
al comunicarlo? ¿qué cross-sell y potencial de recompra tiene? [Seguir
estructura y reglas de la Fase 3.]
```

**8. Claude — Sintetizar** → ver prompt completo en Fase 8.

**9. ChatGPT — Criticar la síntesis** (opcional pero recomendado antes de dar el documento por final)
```
Voy a pegarte un documento de investigación de mercado que Claude
sintetizó para mi negocio. Actúa como un revisor escéptico: señala
cualquier afirmación que suene a hecho pero en realidad sea una
suposición sin evidencia directa, cualquier estadística que no cambie
ninguna decisión real, cualquier generalización de otro país presentada
sin advertencia, y cualquier lugar donde el documento sea complaciente
con mis propias ideas de negocio en vez de cuestionarlas. Sé directo,
no diplomático.

[PEGAR base_fundacional_v1.md]
```

**10. Claude — Corregir documento final**
```
Aquí está la crítica que recibí sobre el documento fundacional de mi
negocio:

[PEGAR crítica de ChatGPT]

Y aquí el documento original:

[PEGAR base_fundacional_v1.md]

Corrige el documento incorporando las críticas válidas: si una crítica
señala que algo se presentó como hecho sin evidencia, corrígelo a su
nivel de evidencia real [A]/[B]/[C]/[D] en vez de solo suavizar el
lenguaje. Si una crítica es incorrecta o el documento ya lo cubre
adecuadamente, dilo y no cambies esa parte. Entrega la versión
corregida completa.
```

---

## 21. Ejemplo reducido (walkthrough LEAN de principio a fin)

Negocio ficticio: tienda ecuatoriana que vende **un solo producto** — un cojín ortopédico para dolor lumbar — por Meta Ads → WhatsApp → COD.

1. **Fase 0-1 (ChatGPT, ~30 min):** brief de negocio + brief de investigación. Hipótesis de partida: "lo compran personas de oficina con dolor de espalda, 30-55 años". Pregunta de investigación priorizada #1: "¿quién realmente investiga y compra este tipo de producto — la persona con dolor, o alguien de su entorno (ej. hijos comprando para un padre con dolor crónico)?".
2. **Fase 2-3 (Claude, LEAN = 3 agentes en paralelo, ~2 horas):**
   - Agente 1: mercado de ecommerce/COD en Ecuador + competencia de productos ortopédicos/ergonómicos.
   - Agente 2: el producto — dolor lumbar como problema (journey completo), VOC de reseñas de cojines ortopédicos.
   - Agente 3: arquetipos — quién compra este tipo de producto (evidencia de compra propia vs. regalo/compra para otro).
3. **Fase 4:** de las notas del Agente 2, se extraen 15-20 frases reales de reseñas (dolor, alivio, desconfianza de que "sea igual de duro que el de la clínica") a la tabla VOC.
4. **Fase 8 (Claude, ~1 hora):** se pegan los 3 documentos + el brief, se sintetiza con el prompt de la Fase 8, se detecta que — igual que en ROUSS — no hay evidencia directa de "quién compra para quién", solo evidencia indirecta (testimonios de "se lo compré a mi papá"). Se marca como [C] HIPÓTESIS.
5. **Fase 9 (Claude, ~1 hora):** documento fundacional de 18 secciones, ~3.000-4.000 palabras (mucho más corto que el caso ROUSS porque es un solo producto).
6. **Fase 10:** el hallazgo de VOC sobre "desconfianza de dureza/calidad" se convierte directamente en un ángulo de creativo (demo del cojín) y en una línea de FAQ de WhatsApp.
7. **Fase 11:** se agrega al guion de WhatsApp la pregunta "¿es para ti o para alguien más?" desde el primer día de ventas.

**Tiempo total estimado:** 5-6 horas repartidas en 1-2 días, sin necesidad de más de 3 agentes de investigación — esto es la Modalidad LEAN funcionando como se espera.

---

## 22. Definición de "terminado"

La investigación fundacional está terminada cuando, y solo cuando:

- [ ] Existe un Brief de Investigación con hipótesis y preguntas priorizadas (Fase 1).
- [ ] Cada agente de investigación lanzado tiene su nota guardada en `/01_RESEARCH_NOTES` con niveles de evidencia explícitos.
- [ ] Existe una tabla VOC con al menos 10-15 frases reales con fuente (más en modalidad DEEP).
- [ ] Existe al menos un arquetipo con la distinción comprador/usuario evaluada explícitamente (confirmada o declarada como hipótesis).
- [ ] Existe una matriz de competencia con al menos 3-5 competidores y sus comentarios negativos, cuando sea posible encontrarlos.
- [ ] El documento de síntesis pasó por el checklist de calidad de la Fase 17 sin marcas pendientes de corregir.
- [ ] Existe la sección `/06_PENDING_VERIFICATIONS` con las tareas manuales pendientes claramente listadas.
- [ ] El documento fundacional tiene una sección de hipótesis a validar con un plan de validación concreto (no solo "hay que investigar más").
- [ ] Se ha decidido y documentado qué 2-3 preguntas se van a instrumentar en el flujo real de venta desde el primer pedido (Fase 11).

Si falta cualquiera de estos puntos, la investigación no está terminada — está incompleta y debe decirse así, no presentarse como un documento final.
