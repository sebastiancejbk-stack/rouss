# ROUSS EC — Base Fundacional de Mercado, Cliente, Marca y Crecimiento

> **Cómo leer este documento.** Cada hallazgo relevante está etiquetado según su nivel de evidencia:
> **[A] EVIDENCIA FUERTE** (dato directo, verificable, con fuente clara) · **[B] EVIDENCIA MODERADA** (señales consistentes pero no definitivas, o de fuentes secundarias/comerciales) · **[C] HIPÓTESIS** (inferencia razonable que ROUSS debe validar con datos propios) · **[D] DESCONOCIDO** (no se encontró información suficiente; no se rellena con certezas inventadas).
>
> **Limitación metodológica transversal, honesta y relevante para cómo se debe usar este documento:** la investigación se realizó con búsqueda web automatizada; el acceso de lectura directa (fetch) a decenas de dominios clave —INEC, CECE, Mercado Libre Ecuador, Fybeca, farmacias, Instagram/Facebook, Meta Ad Library, GNC Ecuador, Pronutrition, Wildland, La Milenaria, y varias plataformas logísticas— estuvo bloqueado en el entorno de investigación. Esto significa que una parte importante de la evidencia proviene de fragmentos de buscador (snippets), no de la lectura verificada de la fuente primaria, y que **casi ningún precio exacto en dólares de competidores ecuatorianos pudo confirmarse de forma independiente**. Esto se señala explícitamente cada vez que aplica, y se listan en la Sección 28 las verificaciones manuales pendientes que el equipo de ROUSS debería completar antes de fijar pricing definitivo o afirmaciones de alto impacto ante inversionistas.
>
> Nota sobre los documentos de Dropper y la API de Rocketfy mencionados en el brief original: **no fue posible acceder a ellos en esta sesión** (el repositorio de trabajo estaba vacío y no se encontraron archivos adjuntos). La Sección 23 describe la arquitectura conceptual de la integración Meta → WhatsApp → Dropper → Rocketfy basada únicamente en la descripción funcional que el propio brief de ROUSS ofrece de estas herramientas, sin inventar detalles técnicos. Esto debe tratarse como [D] DESCONOCIDO en todo lo específico de la implementación y completarse cuando esos documentos estén disponibles.

---

## 1. Executive Summary

**ROUSS EC tiene una oportunidad real, pero está construida sobre una hipótesis central sin validar.** La evidencia recopilada confirma que Ecuador es un mercado de ecommerce grande (~USD 5.500M en 2024, [A]) donde WhatsApp es un canal de venta consolidado (no una moda) y donde el pago contraentrega sigue siendo relevante como mitigador de desconfianza [A]. La categoría de "cuidado cotidiano" (vitamina C, proteína, jugo verde, sueño/ronquidos, visión) tiene demanda validada regionalmente y **poca competencia directa de marcas nativas digitales, faceless, tipo Meta Ads → WhatsApp → COD** [B] — el hueco existe.

Pero la pieza más citada como fundamento de la estrategia de marca — que la compradora es una mujer que gestiona la salud de su pareja/familia y compra "para otro"— **no tiene ninguna evidencia empírica directa que la respalde**, ni en Ecuador ni en LatAm [C, HIPÓTESIS NO VALIDADA explícita]. Hay evidencia sólida de que las mujeres ecuatorianas cargan el 75% del trabajo doméstico no remunerado [A, INEC] y hay evidencia indirecta razonable (automedicación por recomendación familiar, framing editorial de "tu pareja ronca") que hace la hipótesis plausible — pero ROUSS estaría construyendo su arquitectura de marca sobre una suposición, no sobre un hecho medido. Esto no invalida la hipótesis; significa que **debe tratarse como la pregunta de investigación primaria más importante de los próximos 90 días**, no como un cimiento ya probado.

Cinco hallazgos deben cambiar decisiones concretas de ROUSS de inmediato:

1. **El territorio de marca "alivio y cuidado cotidiano" es defendible, pero exige un principio de exclusión explícito**, porque la evidencia de arquitectura de marca (Ritual, Hims & Hers) muestra que la coherencia no viene de la categoría de producto sino de una promesa compartida — ROUSS necesita esa promesa por escrito, no solo el nombre del territorio (Sección 14).
2. **La categoría "detox"/jugo verde tiene un antecedente real y reciente de daño reputacional en Ecuador**: ARCSA detectó plomo en un "Jugo Verde Detox" de una marca ecuatoriana (La Milenaria) en noviembre de 2024 y suspendió su registro sanitario [A]. Cualquier producto de ROUSS en esta categoría debe evitar la palabra "detox" y verificar certificados de metales pesados del proveedor antes de lanzar.
3. **La compra de vitamina C, proteína y kit antironquido converge en una misma mecánica**: alguien identifica un problema de otra persona y actúa. Esto es más fuerte como territorio de marca que "suplementos" o "bienestar" genérico — pero solo si ROUSS instrumenta internamente quién compra para quién, porque hoy no existe ese dato ni en la literatura externa ni (aparentemente) en los sistemas de ROUSS.
4. **La velocidad de respuesta en WhatsApp es la ventaja competitiva más accesible y menos usada**: existe una brecha documentada entre lo que el consumidor latinoamericano espera (minutos) y lo que las empresas entregan (horas) [B]. Ninguna acción de marca es más barata y más alineada con "faceless pero confiable" que responder rápido y con consistencia.
5. **Nadie en el mercado ecuatoriano identificado comunica activamente garantía de devolución ni seguimiento postventa como propuesta de valor** [B, gap de mercado]. Es la oportunidad de diferenciación de menor costo y mayor impacto en confianza que esta investigación encontró.

Este documento no es un plan de marketing terminado. Es la base de conocimiento sobre la cual ROUSS debe decidir, probar y — sobre todo — **medir lo que hoy es hipótesis**, para que dentro de un año este mismo documento pueda reescribirse con hechos propios en lugar de literatura ajena.

---

## 2. Qué es realmente ROUSS

La definición estratégica que ROUSS propone —"una marca de alivio y cuidado cotidiano que ofrece productos confiables, de calidad y de precio accesible, destinados a mejorar pequeñas pero importantes situaciones del día a día mediante el cuidado personal"— **es defendible, pero no es todavía una promesa de marca operativa**. Es una descripción de territorio, no un principio de decisión. La evidencia de arquitectura de marca (Sección 14) muestra que marcas comparables (Ritual, Hims & Hers) no se organizan alrededor de una categoría de producto ni de un adjetivo ("cotidiano"), sino alrededor de una idea concreta y repetible que cualquier persona del equipo puede usar para aceptar o rechazar un producto nuevo en 30 segundos.

**Tensión real que ROUSS debe resolver, no ignorar:** la identidad visual y de comunicación actual nació orientada a rendimiento/fitness con una presencia masculina fuerte (evidenciado por el propio catálogo inicial: proteína, vitamina C con ángulo deportivo). La estrategia declarada apunta hacia "cuidado cotidiano" con un carácter más femenino, limpio y aspiracional. **Esta no es una evolución cosmética menor — es un cambio de audiencia primaria implícito**, y la investigación de arquitectura de marca (Sección 14-15) muestra que las marcas que lo han hecho bien (ej. reposicionamiento de Pascual con Dinamic Protein, o Diabla en Argentina) lo hicieron construyendo comunidad e identidad *antes* de vender el producto reposicionado, no ajustando el copy sobre la marca existente [B]. ROUSS debe decidir explícitamente si está hciendo una **extensión de marca** (mismo nombre, nueva capa de identidad) o si necesita **una segunda piel visual** para el catálogo de cuidado cotidiano que conviva con el ADN fitness original sin canibalizarlo.

Lo que ROUSS **no debe** convertirse en, según el propio brief, es correcto y la evidencia lo refuerza: una tienda random de productos virales (el mercado ecuatoriano ya tiene ese jugador — Distrimass, con ~733K seguidores, vendiendo "productos virales" sin territorio de marca definido [A]); una tienda exclusivamente fitness (el propio mercado ecuatoriano de suplementos está saturado de esa estética — GNC, Prime Nutrition, Pronutrition, todas con comunicación 100% gimnasio [A]); ni una marca médica con afirmaciones clínicas no sustentadas (riesgo regulatorio real y documentado vía ARCSA, ver Secciones 13 y 16).

---

## 3. Mercado relevante en Ecuador

| Dato | Nivel | Fuente / año |
|---|---|---|
| Ecommerce ecuatoriano: ~USD 4.618M en medios bancarizados (+22% vs 2023) o ~USD 5.500M sumando efectivo/COD; proyección >USD 6.000M en 2025-2026 | [A] | CECE-UEES, 7ª medición, ene-2025 (datos 2024) |
| 465M de transacciones digitales en 2024, de las cuales 81,1M son ecommerce | [A] | CECE-UEES / Primicias, 2024 |
| % de transacciones COD en ecommerce ecuatoriano: **cifras contradictorias entre fuentes** (11%, 15-17%, hasta 35% según ciudad/fuente) | [B] | Múltiples fuentes terciarias, 2023-2024 — sin verificación del PDF primario |
| 68-80% de ecuatorianos prefiere pagar en efectivo/transferencia sobre tarjeta | [A] dirección, [B] magnitud exacta | Revista Líderes / CECE |
| Internet cubre >80% del país; 8 de cada 10 compras de ecommerce se hacen desde smartphone | [A] | CECE-UEES 2024 |
| WhatsApp (74%) e Instagram (72%) son las redes más usadas para comprar en línea en Ecuador (2023); en 2021 (pandemia) el 11% de compras online totales se hizo por WhatsApp, con 223.000 hogares comprando medicinas/belleza/cuidado personal por esa vía | [A] | CECE-UEES dic-2023; Kantar 2021 |
| Brecha entre expectativa de respuesta en WhatsApp (minutos) y respuesta real de empresas en LatAm (2-4 horas) | [B] | Fuentes de industria martech, sin journal primario |
| Tasa de entrega efectiva COD en Ecuador: ~65-75% con confirmación previa por WhatsApp/llamada, cae a 45-55% sin confirmación; confirmar antes de despachar reduce rechazo 30-50% | [B] | Fuentes de industria de dropshipping/logística (Pardux, Andrey Business) — sin verificación independiente/oficial |
| Categoría "Salud" en preferencias de compra online ecuatorianas dominada por farmacias de cadena (Fybeca, Pharmacy's, Cruz Azul) y multinivel (Herbalife, Omnilife), no por marcas nativas digitales | [A] | Bloomberg Línea, 2024/2025 |
| No se encontró ninguna marca ecuatoriana de "cuidado personal/bienestar cotidiano" vendida por Meta Ads + WhatsApp + COD que sea un referente reconocido en prensa | [D] hueco confirmado por ausencia | — |

**¿Qué cambia esto para ROUSS?**
- El tamaño del mercado y el peso de WhatsApp como canal de cierre validan la apuesta de canal — no hay necesidad de "inventar" el comportamiento del consumidor, ya existe [A].
- La contradicción en las cifras de % COD significa que **ROUSS no debe anclar proyecciones financieras a un porcentaje externo de "cuánto del mercado es COD"** — debe medir su propio mix de pago desde el primer mes.
- La ausencia de un referente ecuatoriano de bienestar-faceless-COD es simultáneamente una oportunidad (espacio libre) y una ausencia de benchmark (nadie sabe qué tan grande puede llegar a ser esta categoría de negocio en Ecuador) — se debe planificar con escenarios, no con un caso de éxito ya probado localmente.
- El dominio de farmacias de cadena en la categoría "Salud" sugiere que **la competencia real de ROUSS para vitamina C/suplementos "commodity" no es otra tienda de Instagram, es Fybeca/Cruz Azul** — ROUSS gana terreno en productos que requieren explicación/advertorial (kit antironquido, lentes), no en productos donde el comprador ya sabe exactamente qué quiere y compara precio.

---

## 4. Mapa de nichos y micronichos

La hipótesis inicial del brief —"productos que ayudan a cuidar, aliviar o mejorar situaciones cotidianas"— **resiste el análisis, con un matiz importante**: el hilo conductor real no es la categoría del producto (todos son "salud/bienestar" en sentido amplio) sino un patrón de comportamiento que se repite en 4 de los 5 productos actuales: **una persona identifica un problema — a veces suyo, a veces de otra persona en su hogar — y busca una solución de bajo compromiso (sin cita médica, sin gran inversión de tiempo o dinero) antes de escalar a una solución "seria" (médico, óptica, especialista)**. Ese es el territorio real, no "bienestar".

| Micronicho | Frecuencia del problema | Urgencia | Demostrabilidad en anuncio | Confianza requerida | Ticket / recurrencia | Riesgo regulatorio | Fit COD | Fit ROUSS |
|---|---|---|---|---|---|---|---|---|
| **Inmunidad / vitamina C** | Alta, estacional | Media | Baja-media (beneficio invisible) | Media (miedo a falsificación) | Bajo ticket, alta recompra | Bajo (si se evita claim "cura resfriados") | Alto (ya validado, Prime Nutrition ofrece COD) | Alto — ancla de "cuidado diario" |
| **Nutrición / proteína** | Media-alta | Baja | Media | Media (mitos de género/salud) | Ticket medio, recompra 3-5 semanas | Bajo | Alto (ya validado en Ecuador) | Alto si se aleja de estética fitness |
| **Digestión / green juice** | Media | Baja-media (más "culpa" que urgencia real) | Baja (beneficio subjetivo) | **Alta** (antecedente de contaminación en Ecuador) | Ticket medio, recompra mensual | **Alto** (evitar "detox") | Medio | Medio — requiere manejo cuidadoso de naming |
| **Sueño / ronquidos** | Alta (pareja convive con el problema a diario) | Media-alta (erosión acumulada, no crisis) | **Alta** (se puede mostrar el producto y el mecanismo) | Media-alta (categoría con reseñas polarizadas) | Ticket medio, recompra por desgaste 3-12 meses | Medio (evitar mezclar con apnea) | Alto (producto "ganador" ya validado en dropshipping LatAm) | Alto — mejor ángulo emocional de pareja/hogar |
| **Visión / presbicia** | Universal >45 años | Media (vergüenza social puntual) | Alta (antes/después de leer) | **Alta** (antecedente negativo de "lentes dial = estafa") | Ticket medio, recompra por pérdida/rotura, compra múltiple familiar | Medio-alto (no reemplaza examen oftalmológico) | Medio-alto | Alto — patrón de "hijo compra para padre" muy fuerte culturalmente |

**Otros micronichos que emergen de la investigación y que ROUSS debería evaluar con el mismo framework (Sección/Entregable 3) antes de descartarlos o adoptarlos:**
- **Energía sin cafeína** (adyacente a vitamina C/proteína, mencionado como motivador de compra recurrente).
- **Cuidado de adultos mayores / sarcopenia** — respaldo científico real, casi sin explotar como ángulo de marketing en Ecuador [B, whitespace identificado en investigación de proteína].
- **Comodidad para dormir en pareja** (más allá del ronquido: almohadas, aromaterapia) — cross-sell natural del kit antironquido, sin competidor que lo empaquete todavía [B].
- **Autocuidado femenino de bajo compromiso** (colágeno, combos vitamina C+colágeno) — ya validado como SKU en farmacias, con audiencia mayoritariamente femenina documentada [A].

**Territorios que la evidencia sugiere evitar o tratar con extremo cuidado:** cualquier ángulo de "detox"/"elimina toxinas" (riesgo regulatorio y reputacional real, no teórico, en Ecuador); cualquier mecanismo tipo "lente ajustable por dial" (asociación pública negativa fuerte, "estafa de infomercial"); cualquier claim de cura/tratamiento de apnea del sueño (frontera regulatoria de dispositivo médico).

---

## 5. Problemas del consumidor (Customer Problem Journey)

Se reconstruye el journey para los dos problemas con evidencia más rica (ronquido y presbicia, por ser los más "no-commodity" y diferenciadores), y se resume para vitamina C/proteína/green juice (más cercanos a commodity, donde el journey es más corto).

**RONQUIDO**
- Contexto: problema de pareja/convivencia, no percibido por quien lo padece [A, médico: "el roncador está dormido y no puede darse cuenta"].
- Frecuencia: diaria/crónica. Molestia: acumulativa, no aguda.
- Consecuencia funcional: pérdida de sueño de la pareja (~1h/noche, eficiencia de sueño 74%→87% al mejorar) [B, evidencia global].
- Consecuencia emocional: irritabilidad, resentimiento, discusiones más frecuentes [B].
- Consecuencia social: vergüenza en viajes/visitas compartidas [B].
- Soluciones actuales (en orden probable de adopción): pedir cambio de posición → tapones para el que no ronca → tiras nasales de farmacia → dispositivo tipo el de ROUSS → consulta médica → dormir separados [C, reconstrucción lógica no confirmada con datos de journey real].
- Frustraciones: reseñas polarizadas ("funciona de maravilla" vs "no sirve", "se cae en la noche") [A, evidencia real de reseñas].
- Objeciones: eficacia real, comodidad/adaptación, higiene, posible vergüenza de uso (no confirmada directamente) [B/C].
- Trigger: hartazgo acumulado, no un evento único — o exposición a un anuncio con testimonio de pareja [C].
- Compra: probablemente ejecutada por la pareja, no por quien ronca [C, HIPÓTESIS con apoyo indirecto fuerte pero no medido].

**PRESBICIA / LENTES**
- Contexto: evento universal de envejecimiento (100% de la población, desde los 40-45 años) [A].
- Frecuencia: constante una vez que aparece. Molestia: situacional (leer WhatsApp, menús, etiquetas).
- Consecuencia funcional: no poder leer de cerca. Consecuencia emocional: "shock" de asumir la edad. Consecuencia social: vergüenza puntual (no poder leer un menú delante de otros) [B].
- Soluciones actuales: alejar el texto/celular → aumentar zoom del celular → lupa → lentes de farmacia/bazar → óptica tradicional (caro, lento) [A/B].
- Frustraciones: desconfianza hacia lentes "ajustables por dial" (antecedente público fuerte de mala reputación) [A].
- Objeciones: no reemplaza examen oftalmológico, no sirve si hay astigmatismo o graduación distinta entre ojos (95% de la población tiene esto último) [A, médico].
- Trigger: frustración puntual + contenido viral de "¿alejas el celular para leer?" [B].
- Compra: patrón dual autocompra + hijo/hija comprando para padre/madre [B, apoyo de mercado —regalo, "La Casa del Abuelo"— pero sin cita textual verificada].

**VITAMINA C / PROTEÍNA / GREEN JUICE (resumen conjunto — journey más corto, más cercano a hábito que a "descubrimiento de problema"):**
Frecuencia alta (diaria o estacional) → molestia baja/difusa (cansancio, culpa alimentaria, temporada de gripe) → consecuencia principalmente emocional ("estoy haciendo algo por mi salud") más que funcional medible → soluciones actuales: comida real, farmacia, otro suplemento, o no hacer nada (probablemente la opción dominante) [B] → frustraciones: sabor, desconfianza en dosis/autenticidad, escepticismo sobre eficacia real → objeciones médicas ya resueltas por evidencia (no dañan riñón, no engordan, no masculinizan) pero persistentes como mito → trigger: estacionalidad, propósito de año nuevo, contenido de redes → compra: probablemente la propia gestora del hogar, para sí y a veces para hijos (gomitas infantiles) [C].

---

## 6. Arquetipos de cliente

Se presentan cuatro arquetipos de **comportamiento**, no de demografía pura. Todos deben tratarse como **[C] hipótesis de trabajo**, no como segmentos confirmados — el gap de evidencia es el mismo en los cuatro: nadie ha medido directamente el comportamiento de compra-para-otro en Ecuador.

### Arquetipo 1 — "La gestora que resuelve por otros"
Mujer, probablemente 28-50 años, con pareja y/o hijos y/o padres mayores a cargo. Identifica problemas de bienestar en su entorno antes que la persona afectada los verbalice (ronquido de la pareja, vista cansada del padre). Investiga en redes sociales, consulta a su círculo antes de decidir [A, evidencia ecuatoriana sobre boca a boca]. Motivación: no es solo resolver el problema del otro, es aliviar su propia carga (dormir mejor ella también, no tener que ayudar a leer una etiqueta cada vez). Objeción principal: "¿esto realmente funciona para lo que tiene mi [pareja/padre]?" — no el precio. Señal de confianza: reseñas y testimonios de gente "como ella" resolviendo el mismo problema familiar.

### Arquetipo 2 — "La jefa de hogar autosuficiente"
Mujer sin pareja en el hogar (soltera, separada, viuda) que representa el 38,5% de los hogares ecuatorianos y es una tendencia al alza (25,4% en 2001) [A, INEC/Censo 2022]. Compra bienestar para sí misma y su familia como única proveedora y decisora. **Este arquetipo está subrepresentado en la hipótesis original de ROUSS** ("compra para sí y para su pareja"), que asume implícitamente un hogar biparental — el dato demográfico sugiere ampliar el mensaje para no excluir a este segmento creciente.

### Arquetipo 3 — "El escéptico funcional" (usuario, no comprador)
Hombre o mujer que es el *usuario final* de un producto que otra persona compró (el que ronca, el padre con presbicia). No investiga, no decide, a veces ni siquiera acepta usar el producto de buena gana. Su aceptación post-compra determina si hay recompra y testimonio positivo — es el eslabón que ROUSS menos controla y menos mide hoy.

### Arquetipo 4 — "La que se cuida a sí misma primero"
Mujer que compra vitamina C, proteína o green juice exclusivamente para sí misma como parte de un hábito de autocuidado, sin intermediar la compra de nadie más. Consulta más a profesionales antes de comprar que sus contrapartes masculinas (70,2% vs 61,5%, dato regional) [B] y es más influenciada por redes sociales que por recomendación médica (40,4% vs 31%) [B].

**Diferencia usuario vs. comprador — la distinción más operativamente importante de este documento:** en al menos 2 de los 5 productos actuales de ROUSS (kit antironquido, lentes), hay evidencia consistente (aunque indirecta) de que el comprador y el usuario final son personas distintas. Esto tiene una implicación de producto inmediata: **el guion de confirmación de WhatsApp debe preguntar explícitamente "¿es para ti o para alguien más?"**, tanto para mejorar el copy de venta como para empezar a generar el dato que hoy no existe en ninguna fuente externa (Sección 25).

---

## 7. Compradora vs. usuario final

Ver Sección 6 para el desarrollo completo. El resumen ejecutivo: **la hipótesis "gestora del bienestar del hogar" está parcialmente respaldada** por evidencia adyacente sólida (75% del trabajo doméstico no remunerado recae en mujeres ecuatorianas [A, INEC]; 48,1% de compras de medicamentos sin receta en Ecuador se basa en recomendación de familiares [A, estudio UCE]) pero **no está confirmada en su pieza más específica y valiosa**: nadie ha medido si esas mismas mujeres compran productos de bienestar específicamente *para otro miembro del hogar*, con qué frecuencia, y con qué journey. Esto se declara explícitamente como **HIPÓTESIS NO VALIDADA** y se convierte en la pregunta de investigación primaria de ROUSS (ver Entregable 5 y Sección 25).

---

## 8. Psicología de compra

**Dos estereotipos comunes deben descartarse activamente, no adoptarse:**

- *"Las mujeres compran más por impulso"* — la evidencia es mixta; al menos un estudio no encuentra diferencia significativa por género, y donde sí existe diferencia, la compra impulsiva femenina está más asociada a motivación emocional/social y la masculina a lo funcional — no es una regla generalizable ni válida para construir un mensaje de marca [C, evidencia insuficiente y no LatAm].
- *"Las mujeres reclaman menos"* — la evidencia real la **contradice o la matiza fuertemente**: un estudio encuentra que los hombres reclaman más (83% vs 77%); lo mejor respaldado es que hombres y mujeres reclaman con frecuencia similar pero por canales distintos — las mujeres tienden a comentar una mala experiencia en su círculo social/redes antes que exigir una devolución directa a la marca [B, evidencia de EE.UU., no LatAm]. **Implicación operativa real para ROUSS:** una clienta insatisfecha que no escribe a soporte no es necesariamente una clienta satisfecha — puede estar comentándolo en su grupo de WhatsApp o dejando de recomendar la marca en silencio. El sistema de postventa proactivo (Sección 20) es más importante que un canal de reclamos pasivo.

**Lo que sí tiene respaldo y debe informar el copy:** la confianza específica en el vendedor (no la confianza interpersonal general) predice la compra [A, estudio académico Ecuador/Perú] — una marca nueva puede generar confianza sin ser "reconocida", con señales concretas y verificables. El boca a boca en redes sociales y la credibilidad percibida del emisor son factores clave documentados en estudios ecuatorianos (aplicados a cosmética, extensible por analogía) [A].

---

## 9. Voice of Customer

Todas las citas provienen de las notas de investigación con su fuente original; varias son de México/España/EE.UU. por bloqueo de acceso a Mercado Libre Ecuador durante la investigación — se marca el origen en cada caso. **Ninguna cita aquí es inventada.**

**Sobre vitamina C** (objeción de confianza/dosis, Amazon México): *"La descripción del producto dice 500 mg de vitamina C, pero las botellas que recibimos dicen 300 mg."* — refleja el miedo a la falsificación/etiquetado engañoso, reforzado en Ecuador por cierres de farmacias por ARCSA en 2025 por productos falsificados [A].

**Sobre proteína** (disolución/sabor, agregador de reseñas): *"No se disuelve HAGAS LO QUE HAGAS"* y *"los sabores son MUY ARTIFICIALES"*; sobre malestar digestivo: *"la hinchazón, los gases, la diarrea, las náuseas... son señales claras de que la proteína en polvo puede no sentarte bien"*.

**Sobre green juice** (sabor, EE.UU./México): *"MEH... aunque a quienes les gusten los sabores terrosos podría gustarles"*; *"el sabor puede resultar extraño hasta acostumbrarse completamente"* (Mercado Libre México); y la advertencia médica que contradice el claim comercial: *"el concepto de 'detox' es un mito de marketing, no una entidad fisiológica"* (University of Rochester Medicine).

**Sobre kit antironquido** (polarización real, Amazon.es/testimonios de marca): en contra — *"No lo compréis, no sirve de nada, ni quita ronquidos ni respiras mejor porque se caen en cuanto te mueves un poco"*; a favor (testimonio de marca "Silent Pro", tratar con cautela por ser marketing propio) — *"Me sorprende que esto funcione y que mi esposa, por primera vez en años, duerma toda la noche."* Esta segunda cita, aunque es marketing, es la evidencia más directa encontrada del framing "comprador ≠ usuario".

**Sobre lentes de lectura** (desconfianza hacia mecanismos "ajustables", agregador): *"un pedazo de plástico que no sirve para nada"*, *"dinero tirado a la basura"* (sobre lentes tipo "Dial Vision" específicamente — no aplica automáticamente a todo lente multifocal, pero contamina la categoría en la percepción pública).

**Patrón transversal más importante:** en las cinco categorías, la objeción número uno no es el precio — es **"¿esto realmente funciona / es auténtico?"**. El copy y el guion de WhatsApp de ROUSS deben priorizar evidencia y reducción de riesgo (garantías, testimonios reales, trazabilidad) por encima de argumentos de precio.

---

## 10. Soluciones actuales y competencia real

Para los cinco productos, "no hacer nada" o "resolverlo con lo que ya tengo en casa" es probablemente la alternativa dominante real, aunque no cuantificable con la evidencia disponible [C]:

| Producto | Competencia real (lo que la persona hace hoy) |
|---|---|
| Vitamina C | Comer cítricos; farmacia de cadena (Redoxon/Cebion, USD 3,50-27); no hacer nada |
| Proteína | Comer más proteína animal/vegetal; sustitutivos de comida (Boost/Ensure); no hacer nada |
| Green juice | Jugo/licuado casero (competencia más directa en la mente del comprador); ensaladas; no hacer nada |
| Kit antironquido | Tolerar el problema; pedir cambio de posición; tapones de oídos para la pareja; tiras nasales de farmacia; consulta médica; dormir separados |
| Lentes multifocales | Alejar el texto/celular; aumentar zoom del celular; lupa; óptica tradicional (caro/lento) |

La implicación estratégica es la misma en los cinco casos: **el anuncio de ROUSS compite primero contra la inercia de "seguir soportando el problema", no contra otra marca** — el trabajo publicitario más importante es hacer visible el problema y su costo acumulado, no comparar features con un competidor.

---

## 11. Análisis competitivo

Competencia directa identificada en Ecuador (existencia confirmada; precios y ángulos exactos **no verificables** por bloqueo de acceso — ver Sección 28 para lista de verificaciones pendientes):

- **Distrimass / Importadora Massuh** (~733K seguidores IG) — importador de "productos virales" (incluye antironquido), sin territorio de marca ni advertorial por problema; también vende en Mercado Libre Ecuador. Es el jugador más parecido a "lo que ROUSS no debe ser" (tienda random) [A].
- **Prime Nutrition, Enercrease, Proteinas Guayaquil, Pronutrition, Active Life, GNC Ecuador, Right Nutrition, ECUFITNESS, SYF** — tiendas de suplementos, estética 100% fitness/gym, algunas con COD (Prime Nutrition en Guayaquil) [A]. Compiten como catálogo, no como advertorial de un dolor específico.
- **DETOX LIFE, Green Machine, Juice Bar Ecuador** — negocios de delivery/medicina funcional en jugos, no funnels de Meta Ads → WhatsApp → COD [B].
- **Lentes Ecuador, Óptica Carrera Visión, TVentas, Artefacta** — ópticas tradicionales y retail generalista; ninguna tienda de nicho mono-producto en lentes de lectura por COD identificada [B, posible hueco].
- **La Milenaria, Wildland Ecuador, Solanum, Organika** — marcas locales de jugo verde/naturista; La Milenaria con el antecedente de contaminación por plomo ya citado [A].

**Patrones de queja (fuentes agregadas LatAm, no ecuatorianas nominales, pero consistentes con alertas oficiales de Aduana/prensa ecuatoriana sobre estafas de Instagram):** vendedor bloquea al comprador tras el pago; falta de canal de reporte dentro de la propia plataforma (Instagram no permite reportar vendedores que no entregan); tasa de rechazo de pedidos COD reportada entre 15-35% en Ecuador [B, fuente de industria, no oficial].

**Lo que hacen bien los mejor posicionados:** confirmación previa por WhatsApp antes de despachar (reduce rechazo hasta 50%, según fuentes de industria); comunicar "producto 100% original" como respuesta directa al miedo a falsificación (Enercrease, Prime Nutrition) [B].

**El hueco de mercado más defendible con la evidencia disponible:** ninguna tienda ecuatoriana identificada comunica públicamente una política de garantía/devolución ni seguimiento postventa activo. Esto es barato de implementar y de comunicar, y ataca directamente el miedo dominante documentado (que el producto no llegue o no sea auténtico).

---

## 12. Confianza y ecommerce faceless

**Trust Stack de ROUSS**, construido con la evidencia disponible:

- **Antes del click:** coherencia entre el anuncio, el perfil de Instagram y cualquier sitio (mismo tono, mismos precios, sin señales de "cuenta recién creada"); reseñas con fotos/video reales y volumen mínimo visible [B].
- **Después del click / WhatsApp:** velocidad de primera respuesta (el factor más citado y más accionable — brecha real entre expectativa de minutos y respuesta de horas) [B]; tono humano y consistente (no necesariamente "sin bot", pero sí sin fricción cuando el caso es sensible) [B, gap de evidencia sobre si foto/nombre real de asesora cambia conversión — no medido en ninguna fuente encontrada].
- **Confirmación:** mensaje explícito con monto, dirección y fecha de entrega antes de despachar — la práctica individual con más consenso en toda la investigación para reducir rechazo [B].
- **Envío:** notificaciones proactivas de estado, verificación de dirección con Google Maps y puntos de referencia [B].
- **Recepción:** llamada del repartidor minutos antes de la entrega [B].
- **Postventa:** contacto proactivo después de confirmada la entrega (momento de mayor satisfacción documentado) — ningún competidor ecuatoriano identificado lo comunica activamente como propuesta de valor [B, hueco].

**Sobre "faceless" — un hallazgo que desafía la premisa del brief:** la investigación encontró que el caso más citado de "marca sin rostro" exitosa (Comfrt, EE.UU.) en realidad se apoya fuertemente en la historia personal de su fundador. La conclusión más honesta es que **"faceless" no significa "sin ninguna cara humana"** — las marcas que generan confianza sin depender de un fundador-celebridad lo hacen trasladando lo humano hacia el cliente real (UGC, testimonios en video) y hacia el equipo de atención (asesoras con nombre, no necesariamente foto), no eliminando lo humano por completo [B]. Para ROUSS esto significa que "faceless" debe interpretarse como "sin fundador visible", no como "sin ninguna persona visible en la marca".

---

## 13. Análisis de cada producto

### Vitamina C
**Problema real:** deseo de prevención/protección inmune, más emocional que clínico — la evidencia Cochrane (29 comparaciones, >11.000 participantes) confirma que **no previene el resfriado común en población general**, solo reduce levemente la duración de síntomas ya presentes (~8% adultos) [A, evidencia médica]. Excepción real: en atletas/militares con esfuerzo físico intenso, sí reduce la incidencia a la mitad [A]. **Beneficio comercial defendible:** "hábito de cuidado diario", "apoyo al sistema inmune" — nunca "previene/cura resfriados". **Comprador probable:** mujer que gestiona la salud del hogar, posiblemente comprando también en formato gomita para hijos [C]. **Objeción principal:** autenticidad/dosis real, reforzada por antecedentes de falsificación en Ecuador [A]. **Cross-sell validado en el propio mercado ecuatoriano:** vitamina C + zinc (ya es SKU de Fybeca) y vitamina C + colágeno (colágeno es "el producto más buscado" entre mujeres consumidoras de suplementos en LatAm) [A/B]. **Precio de referencia en farmacia ecuatoriana:** USD 3,50-27 según presentación [B, snippet no verificado en vivo]. **Recompra:** modelo de recordatorio por WhatsApp a los 25-30 días, no suscripción automática (el negocio opera en COD) [C].

### Proteína
**Problema real, más allá del gym:** saciedad/control de peso en mujeres, prevención de sarcopenia en adultos mayores (con estudio ecuatoriano específico sobre Cuenca), complemento en dietas restrictivas [A]. **Riesgo de identidad:** el mercado ecuatoriano de proteína está dominado por estética 100% fitness (GNC, Prime Nutrition, Pronutrition) — si ROUSS comunica este producto igual, refuerza la identidad de la que quiere alejarse. **Casos de reposicionamiento exitoso fuera de fitness** (Pascual/Dinamic Protein, Diabla Argentina +USD9M/año, Birdman México) muestran que es posible, pero ninguno opera bajo el modelo Meta Ads → WhatsApp → COD — es terreno diferenciador, no un modelo ya copiado [B]. **Objeciones a neutralizar activamente (todas con respaldo científico claro para desmentirlas):** "daña los riñones" (falso en personas sanas), "engorda" (depende del balance calórico total), "te vuelve masculina" (mito de género, diferencia hormonal real de 15-20x en testosterona) [A]. **Objeciones reales de producto:** mala disolución, sabor artificial, malestar digestivo — control de calidad, no solo copy [A, voice of customer real]. **Cross-sell:** colágeno, multivitamínicos, snacks proteicos [C].

### Green Juice
**Problema real (psicológico, no fisiológico):** alivio de culpa alimentaria + sensación de acción inmediata sobre la propia salud — la evidencia científica de "detox" es débil o nula (American Cancer Society, U. Rochester Medicine) [A]. **Riesgo más alto de las cinco categorías:** antecedente real y reciente en Ecuador — ARCSA detectó plomo en "Jugo Verde Detox" de La Milenaria en noviembre 2024, con retiro de lote y suspensión de registro sanitario [A]. **Recomendación no negociable:** evitar la palabra "detox" y cualquier claim de "elimina toxinas"; usar "apoyo digestivo", "rutina de bienestar"; exigir certificado de análisis de metales pesados al proveedor antes de lanzar. **Comprador probable:** mujer, consulta más a profesionales antes de comprar que en otras categorías (70,2%) [B, regional]. **Alternativa/competencia real:** el jugo casero, no otro producto en polvo — el mensaje debe vender ahorro de tiempo, no superioridad sobre la comida real (mensaje poco creíble) [C]. **Cross-sell:** probióticos, fibra, vitamina C.

### Kit Antironquido
**Problema real:** erosión de la relación de pareja por mala calidad de sueño compartido, no un riesgo de salud del roncador en sí [A, médico]. **Comprador vs usuario:** evidencia indirecta consistente de que la pareja (probablemente la mujer) es quien busca información y compra — pero no medido directamente [C]. **Mecanismo a explicar honestamente:** clip nasal = ensanchador mecánico; dispositivo bucal = reposicionador mandibular — ambos documentados médicamente, sin necesitar exagerar [A]. **Riesgo regulatorio crítico:** nunca usar lenguaje de "cura/trata la apnea" — el ronquido y la apnea del sueño son clínicamente distintos, y el segundo es un trastorno potencialmente grave regulado como dispositivo médico en Ecuador [A]. **Validación de categoría:** el mismo producto genérico ("Silent Pro") se replica en al menos 6 tiendas de dropshipping en Colombia/Chile — es un producto ya "ganador" en la región, lo cual valida la categoría pero también implica que la audiencia ya vio este ángulo muchas veces [B]. **Demostración creíble:** producto físico + testimonio subjetivo de la pareja + animación simple del mecanismo — evitar medidores de decibeles falsos [C]. **Cross-sell sin competidor identificado que lo haga:** kit + almohada posicional + spray de aceites esenciales, mismo territorio de "dormir mejor en pareja" [C, oportunidad de diferenciación].

### Lentes Multifocales
**Problema real:** presbicia, condición universal desde los 40-45 años [A, médico]. **Riesgo regulatorio más alto de fricción con evidencia profesional:** 95% de la población tiene graduación distinta en cada ojo — un lente pregraduado simétrico "es totalmente desaconsejable" en esos casos; existe riesgo de omitir diagnóstico de cataratas/glaucoma al saltarse el examen oftalmológico [A, consenso médico]. **Antecedente reputacional a evitar activamente:** lentes "ajustables por dial" (tipo Dial Vision) tienen fuerte percepción negativa pública ("estafa de infomercial") — si el producto de ROUSS usa un mecanismo similar, debe diferenciarse explícitamente en copy y calidad real. **Comprador probable:** patrón dual autocompra + hijo/hija comprando para padre/madre (apoyo de mercado vía posicionamiento de "regalo", sin cita textual verificada) [B]. **Mensaje honesto y defendible:** "ayuda visual de apoyo para presbicia leve/moderada simétrica", nunca "corrige tu vista" ni "mejor que el oftalmólogo". **Cross-sell:** estuche, paño de microfibra, cordón — bajo costo, alto valor percibido (evitar pérdida/rotura del producto) [B]. **Ya existe oferta 2x1 en Ecuador** (Equilibrium), señal de que la compra múltiple/familiar es práctica reconocida localmente [B].

---

## 14. Arquitectura de marca

La evidencia de branding (Ritual, Hims & Hers) es clara en un punto que ROUSS debe adoptar como principio de decisión, no como inspiración estética: **la coherencia entre categorías dispares no viene de que los productos "se parezcan", viene de una promesa compartida y un sistema visual estricto aplicado sin excepción**. J&J puede tener Neutrogena y Tylenol como marcas separadas (house of brands) porque tiene la escala para gestionarlas por separado; ROUSS, del tamaño que es, necesita un "branded house": una sola marca, un sistema visual, un territorio.

**Lógica de marca propuesta (a validar y refinar por el equipo, no una decisión ya tomada por esta investigación):**

1. **Esencia:** resolver la fricción cotidiana que alguien más notó antes que tú, o que tú mismo postergaste.
2. **Promesa:** "cuidamos lo que casi nadie más nota" — pequeñas soluciones a problemas reales que la persona (o quien la quiere) ya identificó pero no había resuelto.
3. **Propósito comercial:** ser la marca de referencia ecuatoriana en soluciones de bienestar cotidiano vendidas con la misma confianza con la que se compra en una farmacia, pero con la conveniencia de WhatsApp y COD.
4. **Personalidad:** cercana, honesta, sin exagerar; cuidadosa con el lenguaje médico; cálida pero no infantil.
5. **Territorio:** cuidado cotidiano — explícitamente NO fitness/rendimiento, NO productos milagro, NO categoría médica.
6. **Límites (criterios de rechazo, ver Entregable 3 para el framework completo):** cualquier producto que requiera un claim médico no sustentable para venderse; cualquier producto cuya categoría tenga antecedente reputacional negativo reciente en Ecuador sin forma de diferenciarse claramente; cualquier producto que solo tenga sentido para una identidad 100% fitness o 100% femenina excluyente.
7. **Criterios de aceptación:** resuelve una fricción real y nombrable; es demostrable en video sin exagerar; tiene un mecanismo explicable en una frase; permite recompra o cross-sell natural; es viable en COD (ticket y confianza adecuados).
8. **Tono:** directo, cálido, sin tecnicismos médicos; nunca alarmista.
9. **Lenguaje:** "apoyo", "cuidado", "alivio", "rutina" — evitar sistemáticamente "cura", "trata", "elimina", "detox", "garantizado al 100%".

**Sobre la tensión fitness-origen vs. cuidado-cotidiano-destino (Sección 2):** la recomendación basada en evidencia es tratar el catálogo actual bajo un mismo sistema visual con un acento de color por línea de producto (sueño, nutrición, visión) sobre una base neutra común — el mismo patrón que resuelve Hims & Hers, sin fragmentar en sub-marcas desde el día uno.

---

## 15. Identidad y códigos de comunicación

La investigación de identidad visual "femenina no exclusiva, premium accesible" converge con fuerza en un patrón, aunque **ningún ejemplo encontrado es de Ecuador ni LatAm** (limitación real a reconocer): paleta neutra cálida (beige, arena, gris cálido, greige) + un acento de color no-rosa-puro (terracota, verde salvia, coral suave, o un rosa muy desaturado) + tipografía sans-serif limpia + fotografía real de piel/producto con luz natural (no stock genérico) + iconografía geométrica simple, sin ornamentos florales [B].

**Hallazgo que corrige la intuición de "más curvas = más femenino":** la literatura de femtech (Clue, Elvie, Bodyform) muestra que el diseño tradicionalmente "femenino" (curvas, bordes redondeados) es una taquigrafía visual limitada, y que muchas mujeres responden bien a lenguajes de diseño más geométricos/estructurados. Esto es relevante porque **la identidad visual actual de ROUSS (nacida en fitness) probablemente ya tiene esa geometría** — la evolución hacia "cuidado cotidiano" no exige sustituirla por curvas y rosa, sino suavizarla (paleta más cálida, bordes menos agresivos) [C, síntesis razonada, no una fuente única].

**Sobre no excluir al comprador hombre (caso kit antironquido):** la evidencia de marcas gender-neutral en belleza (Non Gender Specific: 60% mujeres/40% hombres; SkinMedica; Soft Services) muestra que la exclusión de hombres no depende de a quién se dirige el mensaje sino del código visual y del copy centrado en beneficio compartido, no en "para él" vs "para ella" [B]. Recomendación concreta: el kit antironquido y otros productos de "bienestar de pareja/hogar" deben usar la misma paleta neutra del resto del catálogo, con copy de beneficio compartido ("duerman mejor los dos") en vez de crear una sub-identidad de género.

**Sobre "fresa" en sentido sofisticado:** la traducción más defendible con evidencia es *clean girl aesthetic* adaptada — limpio, cuidado, ligeramente premium, accesible — sin caer en "todo rosado", que es precisamente la limitación que Glossier (el caso más citado del género) está corrigiendo activamente en su propio rediseño reciente [B].

---

## 16. Precio y oferta

No fue posible verificar con confianza precios exactos de competidores ecuatorianos en COD para ninguna de las cinco categorías (limitación técnica de la investigación, no ausencia de la información en el mercado — ver Sección 28). Lo que sí es defendible con la evidencia disponible:

- **Anclas de precio en canal farmacia/óptica establecida (referencia, no objetivo de pricing):** vitamina C USD 3,50-27 según presentación [B]; lentes de contacto para presbicia desde USD 89/mes en óptica GMO (referencia de "solución profesional", no comparable directamente) [B].
- **El pago contraentrega es tratado por el propio mercado ecuatoriano como "la oferta" en sí misma**, más que descuentos o packs — ninguna fuente encontrada describe estructuras de combo/pack específicas de competidores locales, lo cual sugiere que **combinar COD + pack/garantía visible es una oportunidad de diferenciación no observada en la competencia identificada** [B].
- **Rango de referencia regional para kit antironquido tipo "Silent Pro":** equivalente aproximado a USD 15-35 en Colombia/Perú vía dropshipping — un kit combinado (nasal + bucal) de ROUSS podría posicionarse por encima de un componente único, sujeto a validación propia [B].
- **No pedir seña/anticipo parcial** — no se encontró evidencia de que esto sea práctica extendida en COD LatAm; la alternativa reportada es ofrecer pago electrónico opcional el día de la entrega [B].
- **Percepción de valor por encima de margen:** dado que la objeción dominante en las cinco categorías es "¿funciona/es auténtico?", no precio, una garantía de devolución visible probablemente rinde más en conversión que un descuento — pero esto es [C], no medido directamente.

---

## 17. Sistema de creativos

**Taxonomía de ángulos con evidencia de aplicabilidad por producto:**

- **Descubrimiento/"no sabía que esto existía"** — fuerte para kit antironquido y lentes (productos de bajo conocimiento previo).
- **POV pareja/convivencia** — el más respaldado por evidencia para kit antironquido (testimonios reales encontrados usan este framing).
- **Vergüenza social puntual** — fuerte para lentes (no poder leer un menú/mensaje delante de otros) y para ronquidos en contexto de viaje.
- **Objection crusher (mito médico desmentido)** — fuerte para proteína (riñón, engorda, género) y vitamina C (falsificación, dosis).
- **Rutina cotidiana / hábito** — fuerte para vitamina C y green juice.
- **Regalo/cuidado familiar** — fuerte para lentes (hijo compra para padre) y vitamina C (formato familiar).
- **Mecanismo simple explicado** — necesario en kit antironquido y lentes para vencer escepticismo de "¿esto realmente puede funcionar sin médico?".
- **Social proof con matiz de credibilidad** — en todas las categorías, dado que la confianza en el vendedor específico (no la fama de marca) predice la compra.

**Matriz base (a expandir por el equipo creativo, no a agotar aquí):**

| Producto | Persona | Ángulo | Hook | Mecanismo | Prueba | Objeción a resolver | CTA |
|---|---|---|---|---|---|---|---|
| Kit antironquido | La pareja que no duerme | POV convivencia | "¿Tu pareja ronca y no te deja dormir?" | Clip nasal + dispositivo bucal, mecanismo físico explicado | Testimonio subjetivo + demo de colocación | "¿De verdad funciona?" | WhatsApp con garantía visible |
| Lentes multifocales | Hijo/a que nota la dificultad del padre | Vergüenza social / regalo | "¿Tu papá aleja el celular para leer tus mensajes?" | Lente de aumento multi-zona, sin reemplazar receta | Demo de lectura antes/después (honesta) | "¿Esto le puede dañar más la vista?" | WhatsApp, oferta 2x1 familiar |
| Vitamina C | Gestora del hogar | Rutina + objection crusher | "Lo que sí hace (y lo que no) la vitamina C" | Dosis real, refuerzo inmune (no cura) | Registro sanitario visible, sello de autenticidad | Miedo a falsificación | WhatsApp, combo con zinc/colágeno |
| Proteína | Mujer que cuida su alimentación (no gym) | Objection crusher + rutina | "La proteína no te hace ganar músculo de hombre" | Saciedad, energía, apoyo nutricional diario | Testimonio no-fitness, textura/sabor real | Mito de género, digestión | WhatsApp, cross-sell colágeno |
| Green juice | La que se cuida a sí misma | Rutina, nunca "detox" | "2 minutos de apoyo digestivo en tu rutina" | Fibra, vitaminas, apoyo digestivo (no "elimina toxinas") | Certificado de análisis, testimonio de sabor honesto | Sabor, escepticismo de eficacia | WhatsApp, cross-sell probiótico |

---

## 18. WhatsApp y customer intent

**Customer Intent Map:**

CURIOSO (clic en anuncio) → INTERESADO (responde en WhatsApp, hace preguntas) → EVALUANDO (pregunta por precio total, garantía, tiempo de entrega — objeción dominante: "¿funciona/es auténtico?") → LISTO PARA COMPRAR (confirma datos) → PEDIDO (se registra) → CONFIRMADO (se valida por WhatsApp/llamada antes de despachar — paso con mayor impacto documentado en reducir rechazo) → ENVIADO (seguimiento activo) → ENTREGADO (pico de satisfacción — momento óptimo para primer contacto postventa) → CLIENTE REPETIDO.

**Datos a capturar en cada etapa (mínimo viable, basado en evidencia + necesidades propias de ROUSS):** nombre completo; ciudad y dirección con referencia (verificada con Google Maps); producto/variante; **si es para uso propio o para otra persona** (dato crítico no capturado hoy en ninguna fuente externa — Sección 25); confirmación explícita de pago contraentrega y monto exacto disponible.

**Recomendación operativa con mejor respaldo de toda la investigación de WhatsApp:** fijar un SLA interno de primera respuesta menor a 5 minutos en horario comercial — es la palanca más citada (aunque con cifras exactas no verificadas de forma independiente) y la más barata de implementar.

---

## 19. COD y entrega

El KPI real de ROUSS no debe ser "pedidos generados" sino el funnel completo: **LEADS → PEDIDOS → CONFIRMADOS → ENVIADOS → ENTREGADOS → CLIENTES SATISFECHOS → RECOMPRA.** Ninguna fuente encontrada (ni de Ecuador ni de LatAm) publica tasas de conversión confiables etapa-por-etapa — esto es [D] DESCONOCIDO a nivel de industria y debe construirse con datos propios de ROUSS desde el primer mes.

**Causas de no-entrega con mejor respaldo (fuentes de industria, no oficiales):** información de entrega incompleta/incorrecta (~35% de los casos); cliente no contesta al repartidor; "enfriamiento" del impulso de compra entre el pedido y la entrega (días después, sin compromiso financiero previo) [B]. **Acciones preventivas con mayor consenso:** confirmación previa obligatoria por WhatsApp/llamada (reduce rechazo 30-50%, la práctica individual con más respaldo de toda la investigación); verificación de dirección con Google Maps y puntos de referencia; llamada del repartidor minutos antes de la entrega; seguimiento activo con notificaciones [B].

**Advertencia metodológica importante para ROUSS:** las cifras de "99% de efectividad de entrega" que ofrecen proveedores logísticos (Gintracom, Rocket) probablemente miden solo la etapa de despacho→entrega, no el funnel completo desde el lead — no deben confundirse con la tasa de conversión real de leads a clientes satisfechos [C, inferencia razonable no confirmada por ninguna fuente].

---

## 20. Postventa

El momento de mayor satisfacción documentado es justo después de confirmada la entrega — es el punto óptimo para el primer contacto postventa [B]. No existe un "calendario universal" de cuándo pedir reseña o presentar recompra; depende del ciclo de uso real del producto. **Recomendación basada en la naturaleza de cada producto:** para consumibles (vitamina C, proteína, green juice), anclar el recontacto a la duración estimada del envase (25-30 días); para productos de desgaste físico (kit antironquido, lentes), anclar el recontacto a la vida útil documentada del producto (3-12 meses según componente) [C].

**Ninguna competencia ecuatoriana identificada comunica activamente seguimiento postventa** — es el hueco de mercado de menor costo y mayor impacto en confianza encontrado en toda esta investigación (Sección 11).

---

## 21. Recompra

Potencial de recompra por producto, de mayor a menor previsibilidad: **kit antironquido y lentes** (recompra por desgaste/pérdida física, documentado en industria dental y de accesorios) [A/B]; **vitamina C, proteína, green juice** (recompra por consumo diario, ciclo de 25-30 días) [C, inferencia de diseño de negocio, sin dato de tasa de recompra real en ninguna fuente]. **Dato crítico ausente en toda la investigación:** no existe ninguna cifra de LTV o tasa de recompra real para ninguna de las cinco categorías en Ecuador o LatAm — es terreno que ROUSS debe medir internamente, no algo que pueda proyectarse desde literatura externa.

---

## 22. Cross-sell

**Mapa de cross-sell con mejor respaldo:**
- Vitamina C ↔ Zinc (ya es SKU validado en farmacias ecuatorianas) ↔ Colágeno (producto más buscado por mujeres en la región).
- Proteína ↔ Colágeno ↔ Multivitamínicos ↔ Snacks proteicos.
- Green Juice ↔ Probióticos ↔ Fibra ↔ Vitamina C.
- Kit Antironquido ↔ Almohada posicional ↔ Spray de aceites esenciales para dormir (combo no observado en ningún competidor identificado — oportunidad real de diferenciación).
- Lentes Multifocales ↔ Estuche rígido ↔ Paño de microfibra ↔ Cordón (bajo costo marginal, alto valor percibido).

**Puente entre categorías con mejor lógica de negocio:** vitamina C/colágeno como entrada de bajo riesgo hacia el resto del catálogo para la "gestora del hogar"; kit antironquido/lentes como entrada hacia el catálogo para quien resuelve el problema de otra persona.

---

## 23. Relación Meta → WhatsApp → Dropper → Rocketfy

**Advertencia explícita:** esta sección se basa únicamente en la descripción funcional que el propio brief de ROUSS ofrece de Dropper y Rocketfy — los documentos técnicos mencionados como adjuntos no estuvieron disponibles en esta sesión de investigación (repositorio vacío, sin archivos adjuntos accesibles). Todo lo específico de la implementación técnica se marca como **[D] DESCONOCIDO** y debe completarse cuando esos documentos existan en el repositorio.

**Arquitectura conceptual del journey (no técnica):**

META ADS (creativo, ángulo, avatar) → clic → WHATSAPP (conversación, calificación de lead, captura de datos incluyendo "para quién es el producto") → DROPPER (según el brief: gestión de conversaciones, pedidos, confirmación, seguimiento, estados, postventa, recompra, memoria del cliente) → integración con ROCKETFY (gestión logística y estados del pedido, según el brief) → ENTREGA → POSTVENTA → RECOMPRA.

El valor conceptual de esta cadena, una vez los sistemas existan y capturen datos reales, es poder relacionar exactamente lo que pide la Sección 10 del brief original: qué creativo/ángulo produce qué tipo de lead, qué objeción predice no-entrega, qué avatar compra para quién. **Hoy ninguno de esos cruces existe como dato — es el objeto del Entregable 5 (Learning Loop).**

---

## 24. Arquitectura de datos

Ver Sección 29 (Anexos) para las 8 tablas maestras completas con su esquema de campos, poblado con ejemplos reales extraídos de esta investigación como semilla inicial.

---

## 25. Hipótesis que debemos validar

Esta es, junto con el Entregable 5, la sección más importante del documento para la operación de los próximos 90 días — consolida toda hipótesis marcada [C] a lo largo del documento:

| Hipótesis | Evidencia a favor | Evidencia en contra | Confianza | Cómo validarla |
|---|---|---|---|---|
| La compradora es una mujer que compra para sí y para su pareja/familia | 75% del trabajo doméstico no remunerado recae en mujeres (INEC); 48,1% de compras de medicamentos sin receta se basa en recomendación familiar | Ningún estudio mide directamente "compra para otro" en salud/bienestar en Ecuador/LatAm; 38,5% de hogares tienen jefatura femenina sin pareja | Media-baja | Pregunta obligatoria en guion de WhatsApp: "¿es para ti o para alguien más?"; análisis de mezcla de productos por pedido |
| El kit antironquido lo compra la pareja, no quien ronca | Framing consistente de contenido médico/marcas ("tu pareja", "tu esposa"); testimonios de marca en esa dirección | Ninguna encuesta directa; testimonios son marketing propio de competidores | Media | Misma pregunta de guion + análisis de nombre/tono de quien escribe primero al WhatsApp |
| Los lentes los compra un hijo/a para su padre/madre | Posicionamiento de mercado como regalo; tienda "La Casa del Abuelo" | Sin cita textual verificada de comprador real | Media-baja | Pregunta de guion + campo "destinatario" en confirmación de pedido |
| Humanizar WhatsApp (foto/nombre de asesora real) mejora conversión | Principio general de marketing conversacional, guías oficiales de Meta | Ningún estudio cuantitativo lo mide, ni en Ecuador ni globalmente | Baja | A/B interno de plantillas de respuesta |
| Responder en <5 min mejora significativamente la conversión | Múltiples fuentes de industria citan cifras direccionales consistentes | Cifras exactas (8x, 21x) no verificadas contra estudio primario | Media | Medir conversión real de ROUSS por bucket de tiempo de respuesta |
| Garantía de devolución visible aumenta conversión más que un descuento | Ningún competidor ecuatoriano la comunica (hueco); lógica de reducción de riesgo consistente con objeción #1 ("¿funciona/es real?") | No hay dato cuantitativo de efecto | Media | A/B de landing/copy con y sin garantía visible |
| El % de pedidos COD de ROUSS será mayor al promedio del ecommerce ecuatoriano | Categoría de marca nueva/redes sociales, no marketplace con checkout de tarjeta | Cifras de % COD del mercado general son contradictorias (11-35%) | Media | Medir mix de pago propio desde el mes 1 |

---

## 26. Plan de experimentación

Sugerido como punto de partida, no como calendario cerrado:

1. **Mes 1-2:** instrumentar en el guion de WhatsApp/Dropper la pregunta "¿es para ti o para alguien más?" en las 5 categorías, y registrar el dato sistemáticamente. Es la acción de mayor apalancamiento de todo el documento: cierra el gap de evidencia más grande encontrado.
2. **Mes 1-2:** A/B de tiempo de respuesta (medir conversión real por bucket: <1 min, 1-5 min, 5-30 min, >30 min).
3. **Mes 2-3:** A/B de garantía de devolución visible vs. no visible en el copy/landing de kit antironquido y lentes (las dos categorías con objeción de eficacia más fuerte).
4. **Mes 2-3:** testear naming alternativo a "detox" para green juice, dado el antecedente de ARCSA — medir si el cambio de naming afecta CTR/conversión sin perder claridad de beneficio.
5. **Mes 3+:** encuesta post-compra corta ("¿para quién compraste este producto? ¿cómo nos conociste? ¿qué revisaste antes de comprar?") para las 5 categorías, acumulando muestra propia que reemplace la literatura externa citada en este documento.
6. **Continuo:** medir funnel completo propio (leads → pedidos → confirmados → enviados → entregados → recompra) por producto y por creativo — no existe benchmark externo confiable, así que el primer trimestre de datos propios se convierte en el benchmark de ROUSS.

---

## 27. Conclusiones estratégicas

- **El territorio "cuidado cotidiano" es defendible, pero ROUSS no lo ha convertido todavía en una promesa operativa** — tiene un territorio, no tiene todavía el principio de decisión que le permitiría aceptar o rechazar un producto nuevo en un minuto (Entregable 3 lo ofrece como punto de partida).
- **La hipótesis central sobre la compradora no está probada y no debe presentarse como un hecho ante el equipo, inversionistas o en brand guidelines** — es la hipótesis de trabajo más importante y también la más frágil del proyecto.
- **La categoría con mayor riesgo reputacional inmediato es green juice/detox**, por el antecedente real y reciente en Ecuador — cualquier decisión de naming o lanzamiento en esta categoría debe pasar primero por esta consideración, no por potencial de venta.
- **La ventaja competitiva más barata y menos explotada por la competencia identificada es la combinación de velocidad de respuesta + garantía visible + seguimiento postventa activo** — ninguna requiere inversión de producto, solo disciplina operativa.
- **ROUSS compite mejor donde el producto necesita explicación (kit antironquido, lentes) que donde compite por precio en un commodity ya conocido (vitamina C genérica, donde gana la farmacia de cadena)** — esto debería influir en dónde se concentra el presupuesto de Meta Ads de aprendizaje inicial.
- **La tensión entre el ADN fitness original y el destino "cuidado cotidiano" es real y debe resolverse explícitamente**, no dejarse a la deriva del copy de cada campaña.

---

## 28. Fuentes

Todas las fuentes primarias citadas están documentadas con URL, fecha (cuando se pudo confirmar) y país de origen dentro de las notas de investigación completas, conservadas en `research_notes/Base fundacional ROUSS EC/` (10 documentos, ~2.000 líneas de evidencia con citas). Los documentos cubren: mercado ecommerce/COD Ecuador, cada uno de los 5 productos, arquetipos de compradora, competencia COD Ecuador, funnel WhatsApp/entrega, y confianza/marca faceless.

**Verificaciones manuales pendientes que el equipo de ROUSS debería completar antes de tomar decisiones de alto impacto (pricing definitivo, proyecciones financieras, claims ante inversionistas), porque el entorno de esta investigación no tuvo acceso de navegador real a estas fuentes:**
- PDF completo del estudio CECE-UEES (séptima medición) y del reporte INEC de TIC más reciente, para confirmar el % real de COD en el ecommerce ecuatoriano.
- Precios vigentes en Mercado Libre Ecuador para: kit antironquido, lentes de lectura multifocales, vitamina C, proteína, green juice.
- Catálogo y precios de Sana Sana y Farmacias Económicas (no accesibles en esta sesión).
- Meta Ad Library filtrado por Ecuador, para las 5 categorías — no fue posible acceder a anuncios activos reales ni a su gasto/alcance.
- Reseñas textuales verificadas con fecha de Mercado Libre Ecuador para las 5 categorías (las citas de este documento provienen mayormente de México/España/EE.UU. por bloqueo de acceso).
- Perfiles de Instagram/Facebook de Distrimass, Prime Nutrition, Enercrease, Proteinas Guayaquil, Lentes Ecuador para precios y ángulos publicitarios reales.

---

## 29. Anexos / Tablas maestras

### TABLA 1 — AVATARES

| avatar_id | nombre | descripción | rol_en_hogar | comprador_usuario | problemas | motivaciones | miedos | deseos | objeciones | triggers | lenguaje | señales_confianza |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| AV-01 | La gestora que resuelve por otros | Mujer 28-50, identifica problemas de bienestar ajenos antes que la persona afectada | Cuidadora del hogar | Comprador (no usuario) | Ronquido de pareja, vista cansada de padre | Aliviar su propia carga; cuidar a los suyos | "¿Esto realmente sirve para lo que tiene él/ella?" | Paz y descanso compartido | Eficacia, no precio | Hartazgo acumulado, testimonio de otra mujer | "para ti y los tuyos", "duerman mejor los dos" | Reseñas de gente "como ella" con el mismo problema familiar |
| AV-02 | La jefa de hogar autosuficiente | Mujer sin pareja en el hogar, única proveedora/decisora | Proveedora y decisora | Comprador y usuario | Bienestar propio y de hijos | Autosuficiencia, que a su familia no le falte nada | Gastar en algo que no funcione | Control, eficiencia | Precio + eficacia | Necesidad puntual propia o de un hijo | "para ti y tu familia" (sin asumir pareja) | Trazabilidad, garantía |
| AV-03 | El escéptico funcional | Usuario final de un producto que otra persona compró | Usuario, no decide | Usuario (no comprador) | El problema que otro identificó por él/ella | Que lo dejen en paz / que funcione sin esfuerzo | Incomodidad, vergüenza de uso | Que el problema desaparezca sin cambiar hábitos | "no lo necesito" | Presión social de quien compró | N/A (no es el receptor del mensaje publicitario) | Facilidad de uso, adaptación rápida |
| AV-04 | La que se cuida a sí misma | Mujer con hábito de autocuidado individual | Usuario y comprador | Comprador y usuario | Energía, inmunidad, digestión propia | Autocuidado, hábito, sentirse bien | Perder tiempo/dinero en algo inútil | Rutina simple y efectiva | Sabor, escepticismo de eficacia | Contenido de redes, estacionalidad | "rutina diaria", "cuídate hoy" | Testimonios de redes, consulta previa a profesional |

### TABLA 2 — PROBLEMAS

| problema_id | categoría | micronicho | descripción | frecuencia | intensidad | consecuencia_funcional | consecuencia_emocional | consecuencia_social | soluciones_actuales | frustraciones | urgencia |
|---|---|---|---|---|---|---|---|---|---|---|---|
| PR-01 | Sueño/pareja | Ronquido | Vibración de tejidos blandos que interrumpe el sueño de la pareja | Diaria/crónica | Media-alta (acumulativa) | Pérdida de sueño de la pareja | Irritabilidad, resentimiento | Vergüenza en viajes/visitas | Cambiar de posición, tapones, tiras nasales, dormir separados | Reseñas polarizadas, incomodidad de dispositivos | Media (erosión, no crisis) |
| PR-02 | Visión | Presbicia | Dificultad para enfocar de cerca por edad | Constante desde los 40-45 | Media | No poder leer texto pequeño | "Shock" de asumir la edad | Vergüenza puntual (menú, mensaje) | Alejar el texto, zoom del celular, óptica tradicional | Desconfianza en lentes genéricos | Media |
| PR-03 | Inmunidad | Resfriados/defensas bajas | Percepción de vulnerabilidad estacional | Estacional | Baja-media | Malestar leve | Sensación de descuido personal | Baja | Cítricos, farmacia, nada | Desconfianza en autenticidad/dosis | Media (estacional) |
| PR-04 | Nutrición | Déficit proteico percibido / control de peso | Dificultad para cubrir proteína diaria o controlar apetito | Diaria | Baja | Cansancio, falta de saciedad | Culpa por mala alimentación | Baja | Comida real, sustitutivos, nada | Sabor artificial, mitos de salud | Baja |
| PR-05 | Digestión | Hinchazón/mala digestión percibida | Sensación de pesadez, culpa alimentaria | Frecuente | Baja-media | Incomodidad digestiva | Culpa, frustración | Baja | Jugo casero, ensaladas, nada | Sabor, escepticismo de eficacia | Baja |

### TABLA 3 — PRODUCTOS

| producto | problema | usuario | comprador | mecanismo_percibido | beneficio | objeciones | preguntas | alternativas | frecuencia_compra | recompra | cross_sell | fit_ROUSS |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| Vitamina C | PR-03 | Sí mismo/familia | Gestora del hogar | Refuerzo inmune | Hábito de cuidado | Autenticidad/dosis | "¿Tiene registro sanitario?" | Farmacia, cítricos | Mensual | Alta (consumible) | Zinc, colágeno | Alto |
| Proteína | PR-04 | Sí mismo | Ella misma o gestora | Aporte proteico diario | Saciedad/energía | Mitos de salud/género | "¿Engorda? ¿daña el riñón?" | Comida real, sustitutivos | Mensual | Alta (consumible) | Colágeno, multivitamínico | Alto (si se aleja de fitness) |
| Green Juice | PR-05 | Sí mismo | Ella misma | Apoyo digestivo (nunca "detox") | Alivio de culpa + practicidad | Sabor, escepticismo, riesgo regulatorio | "¿De verdad desintoxica?" | Jugo casero | Mensual | Alta (consumible) | Probiótico, fibra | Medio (requiere cuidado de naming) |
| Kit Antironquido | PR-01 | Pareja que ronca | Pareja que no ronca | Clip nasal + reposicionador mandibular | Descanso compartido | Eficacia, comodidad | "¿De verdad funciona?" | Tiras nasales, dormir separados | Baja (por desgaste 3-12 meses) | Media | Almohada, spray de aceites | Alto |
| Lentes Multifocales | PR-02 | Usuario con presbicia | A veces hijo/a | Lente de aumento multi-zona | Ver de cerca sin cita médica | No reemplaza examen, calidad óptica | "¿Me daña más la vista?" | Zoom celular, óptica tradicional | Baja (por pérdida/rotura) | Media-alta (compra familiar) | Estuche, paño, cordón | Alto |

### TABLA 4 — VOICE OF CUSTOMER

| frase | fuente | país | producto/problema | emoción | intención | etapa_awareness | interpretación |
|---|---|---|---|---|---|---|---|
| "La descripción dice 500 mg... las botellas dicen 300 mg" | Amazon México | México | Vitamina C | Desconfianza | Advertir a otros | Producto-aware | Miedo a etiquetado/autenticidad falso |
| "No se disuelve HAGAS LO QUE HAGAS" | Agregador de reseñas | Global/México | Proteína | Frustración | Queja | Producto-aware | Barrera de calidad de producto, no de mensaje |
| "El concepto de 'detox' es un mito de marketing, no una entidad fisiológica" | University of Rochester Medicine | EE.UU. (global) | Green juice | Escepticismo | Educar/advertir | Problem-aware | Riesgo de claim no sustentado |
| "No lo compréis, no sirve de nada... se caen en cuanto te mueves" | Amazon.es | España | Kit antironquido (clip nasal) | Frustración | Advertir a otros | Producto-aware | Objeción de fijación física del dispositivo |
| "Me sorprende que esto funcione y que mi esposa... duerma toda la noche" | Testimonio de marca (Silent Pro) | LatAm (Colombia/Chile) | Kit antironquido | Alivio/sorpresa | Recomendar | Solution-aware | Evidencia de framing comprador≠usuario |
| "Un pedazo de plástico que no sirve para nada" | Agregador de reseñas | LatAm/global | Lentes ajustables (Dial Vision) | Enojo | Advertir a otros | Producto-aware | Antecedente reputacional a evitar en mecanismo similar |

### TABLA 5 — COMPETENCIA

| competidor | canal | producto | problema | avatar | precio | oferta | hook | claim | prueba | trust_signal | comentarios | debilidad |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| Distrimass | Instagram/TikTok/Mercado Libre | Antironquido y "productos virales" | Múltiples, sin foco | General/impulso | D | D | "Producto novedoso/viral" | Ninguno específico | D | 733K seguidores | D (no accesible) | Sin territorio de marca, sin advertorial de dolor específico |
| Prime Nutrition | Web/WhatsApp | Proteína | Nutrición deportiva | Fitness | D | COD en Guayaquil | "Asesoría gratuita" | "100% original" | D | Originalidad declarada | D | Estética 100% fitness, no bienestar |
| La Milenaria | Tienda online | Jugo verde detox | Digestión/detox | General bienestar | D | D | D | "Detox" | D | D | Antecedente ARCSA de plomo (nov-2024) | Riesgo reputacional activo en la categoría |
| Silent Pro (multi-tienda dropshipping) | Shopify/Meta Ads | Kit antironquido | Ronquido de pareja | Pareja que no duerme | ~USD 15-35 (regional) | Garantía 30 días | "Mi esposa duerme toda la noche" | Reducción de ronquido | Testimonio de marca | Garantía sin preguntas | D | Copy ya muy visto/saturado en la región |

*(D = Desconocido / no verificable en esta investigación — completar con visita manual, ver Sección 28)*

### TABLA 6 — ÁNGULOS

Ver matriz completa en Sección 17.

### TABLA 7 — CUSTOMER JOURNEY

Ver Customer Intent Map completo en Sección 18.

### TABLA 8 — HIPÓTESIS

Ver tabla completa en Sección 25.

---

# ENTREGABLE 1 — Mapa Fundacional de ROUSS

| Elemento | Respuesta (con nivel de evidencia) |
|---|---|
| **QUIÉN** | Principalmente una mujer 25-50 años que gestiona el bienestar de su hogar [C], y en segundo lugar quien identifica un problema propio de autocuidado [B] |
| **tiene QUÉ PROBLEMA** | Una fricción cotidiana real (sueño, vista, digestión, energía, inmunidad) que ella misma vive o que nota en alguien de su entorno [B/C] |
| **quiere QUÉ RESULTADO** | Que el problema se resuelva sin gran inversión de tiempo, dinero o riesgo (sin cita médica, sin gran compromiso) [B] |
| **actualmente hace QUÉ** | Nada, o una solución casera/de bajo compromiso — no compra a un competidor de marca, compite contra la inercia [B] |
| **ROUSS puede ofrecer QUÉ** | Un producto de bajo riesgo económico (COD), demostrable, con mecanismo explicable honestamente [A/B] |
| **necesita ver QUÉ para confiar** | Reseñas/testimonios reales, respuesta rápida en WhatsApp, garantía de devolución visible, confirmación clara antes del envío [B] |
| **compra por QUÉ** | Reducción de riesgo percibido más que precio — la objeción #1 en las 5 categorías es "¿funciona/es real?", no el costo [A] |
| **puede recomprar QUÉ** | Consumibles con ciclo de 25-30 días (vitamina C, proteína, green juice) o reemplazo por desgaste (kit antironquido, lentes) [C] |

---

# ENTREGABLE 2 — Mapa de Problemas y Oportunidades

Matriz de evaluación para nuevos problemas/productos candidatos (usar junto con el Entregable 3):

| Dimensión | Pregunta que debe responderse antes de aceptar un nuevo problema/territorio |
|---|---|
| Frecuencia | ¿Cuántas veces por semana/mes vive esta persona el problema? |
| Urgencia | ¿Puede esperar semanas sin resolverlo, o genera fricción activa ya? |
| Intensidad emocional | ¿Genera vergüenza, culpa, frustración de pareja, o es indiferente? |
| Demostrabilidad | ¿Se puede mostrar el problema y la solución en 15-30 segundos de video sin exagerar? |
| Confianza requerida | ¿Es un producto "commodity" (gana el precio/la farmacia) o requiere explicación (gana el advertorial)? |
| Riesgo regulatorio | ¿Hay antecedente de ARCSA, de escándalo de categoría, o de claim médico difícil de evitar? |
| Fit COD | ¿El ticket y el nivel de confianza requerido son compatibles con pago contraentrega? |
| Recompra/cross-sell | ¿Genera consumo recurrente o puede conectar con otro producto del catálogo? |
| Fit ROUSS | ¿Encaja en el territorio "cuidado cotidiano" sin forzar la marca hacia fitness, médico o "producto viral random"? |

Esta matriz debe aplicarse a cada uno de los micronichos listados en la Sección 4 (energía sin cafeína, cuidado de adultos mayores, comodidad de pareja, autocuidado femenino) antes de decidir cuáles desarrollar.

---

# ENTREGABLE 3 — Product Fit Framework

**Pregunta central: "¿Este producto pertenece a ROUSS?"**

Un producto nuevo debe responder afirmativamente a la mayoría de estas preguntas para avanzar a testing:

1. **Problema:** ¿Resuelve una fricción cotidiana real y nombrable (no un deseo vago de "bienestar")?
2. **Avatar:** ¿El comprador y/o usuario encaja en alguno de los 4 arquetipos de la Sección 6, o exige crear un arquetipo nuevo y bien fundamentado?
3. **Necesidad:** ¿La persona ya reconoce el problema, o el anuncio tendría que educar desde cero que el problema existe? (ambos son viables, pero el segundo es más caro de testear).
4. **Confianza:** ¿Puede generarse confianza suficiente por WhatsApp + reseñas + garantía, o requiere una autoridad que ROUSS no tiene (médica, técnica)?
5. **Precio:** ¿El ticket es compatible con COD (ni tan bajo que no cubra el costo de rechazo, ni tan alto que dispare el riesgo percibido)?
6. **Demostrabilidad:** ¿Se puede mostrar honestamente en video sin manipular expectativas (antes/después, medidores falsos)?
7. **COD:** ¿La categoría ya tiene precedente de venderse por contraentrega en Ecuador/LatAm, o sería la primera?
8. **Recompra:** ¿Genera consumo recurrente o reemplazo natural?
9. **Cross-sell:** ¿Conecta con al menos un producto ya existente en el catálogo?
10. **Regulación:** ¿Existe riesgo de que se le exija registro sanitario/dispositivo médico, o antecedente reciente de escándalo en esa categoría en Ecuador?
11. **Identidad:** ¿Refuerza el territorio "cuidado cotidiano" o empuja la marca hacia fitness, medicina o "producto viral random"?
12. **Riesgo:** ¿Qué pasa si el producto no cumple la expectativa? ¿El daño reputacional es recuperable con una garantía, o es estructural (ej. seguridad, salud)?

Un producto que falla en las preguntas 4, 10 o 12 debe rechazarse o posponerse, independientemente de qué tan bien responda a las demás — son las preguntas de mayor costo de error.

---

# ENTREGABLE 4 — Creative Intelligence Matrix

La matriz base está desarrollada en la Sección 17. El sistema completo (Producto × Avatar × Problema × Ángulo × Hook × Deseo × Objeción × Prueba × CTA) debe alimentarse continuamente desde el Learning Loop (Entregable 5) a medida que existan datos reales de Meta Ads y WhatsApp — la matriz actual es la semilla inicial construida con evidencia externa, no el estado final.

---

# ENTREGABLE 5 — Learning Loop

```
INVESTIGACIÓN (este documento, evidencia externa)
        ↓
HIPÓTESIS (Sección 25 — ej. "la pareja compra el kit antironquido")
        ↓
CREATIVO (Sección 17 — ángulo/hook diseñado para probar esa hipótesis)
        ↓
META ADS (se publica, se mide CTR/CPL por ángulo y avatar)
        ↓
WHATSAPP (se pregunta explícitamente "¿es para ti o para alguien más?" — Sección 18)
        ↓
PEDIDO (se registra con el dato de destinatario real)
        ↓
DROPPER / ROCKETFY (gestión, confirmación, estado — Sección 23)
        ↓
ENTREGA (se mide tasa real de entrega por creativo/objeción/avatar)
        ↓
POSTVENTA (se mide satisfacción real del usuario final, no solo del comprador)
        ↓
RECOMPRA (se mide qué avatar/producto realmente recompra)
        ↓
APRENDIZAJE (se compara contra la hipótesis original: ¿se confirmó, se refutó, quedó ambigua?)
        ↓
NUEVA HIPÓTESIS (se actualiza este documento con datos propios de ROUSS)
```

**El objetivo de este ciclo no es solo vender más — es que dentro de 12 meses, las tablas de la Sección 29 y las hipótesis de la Sección 25 estén pobladas con datos propios de ROUSS en vez de literatura externa citada de México, España o EE.UU.** Ese es el momento en que ROUSS se convierte, en el sentido literal que pide el brief original, en una empresa que aprende de sus propios clientes.
