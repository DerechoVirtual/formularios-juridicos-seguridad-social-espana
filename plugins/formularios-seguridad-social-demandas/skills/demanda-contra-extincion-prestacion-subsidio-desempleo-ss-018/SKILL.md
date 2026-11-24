---
name: demanda-contra-extincion-prestacion-subsidio-desempleo-ss-018
description: "Demanda contra la extinción de la prestación o subsidio de desempleo por traslado al extranjero. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda contra la extinción de la prestación o subsidio de desempleo por traslado al extranjero

> Formulario **SS-018** del plugin **Seguridad Social: demandas y recursos ante lo social** (`formularios-seguridad-social-demandas`) · Seguridad Social › Demandas y escritos ante la jurisdicción social · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda contra la extinción de la prestación o subsidio de desempleo por traslado al extranjero» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda contra la extinción de la prestación o subsidio de desempleo por traslado al extranjero” para mi caso». También puedes invocarla directamente con `/formularios-seguridad-social-demandas:demanda-contra-extincion-prestacion-subsidio-desempleo-ss-018`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-seguridad-social-demandas:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Seguridad Social: demandas y recursos ante lo social) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (5 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] CORREO ELECTRÓNICO
- [ ] DESCRIBIR
- [ ] DNI/NIE
- [ ] DOMICILIO
- [ ] LUGAR
- [ ] MOTIVO
- [ ] Nº
- [ ] Nº DE EXPEDIENTE
- [ ] PAÍS DE DESTINO
- [ ] SEDE
- [ ] TELÉFONO
- [ ] ÓRGANO

## Normas que cita el formulario

- art. 71.2 Ley 36/2011
- art. 6.3 Real Decreto 625/1985

## Instrucciones para Claude

### Paso 0: Jurisprudenciator en esta skill (obligatorio)

**Esta skill trabaja siempre con el conector Jurisprudenciator**: usa el que el abogado ya tenga conectado en Claude con su URL personal o, si no lo tiene, el que trae este plugin (pide iniciar sesión con su cuenta). Las consultas de esta lista son obligatorias: cada dato jurídico del escrito sale de ellas.

- **Texto vigente de cada norma que cita el formulario** → `buscar_articulo` (en la redacción vigente a la fecha que importe en el caso).
- **Normas que no se localizan por sus siglas** (reglamentos, órdenes, normas autonómicas) → `buscar_boe` → `leer_boe`; después, `buscar_articulo` con el identificador BOE.
- **Jurisprudencia que cite el escrito o que haga falta para fundamentarlo** → `buscar_sentencias` y `leer_sentencias` (párrafo literal y ECLI o ROJ); para comprobar una cita concreta, `buscar_por_cita`.
- **Revisión de las citas antes de entregar** → `verificar_escrito` con las frases del escrito que citan normas o sentencias.
- **Sociedades que intervienen** (existencia, administradores, actos inscritos) → `buscar_empresa_mercantil`; para fechar un acto, `sumario_borme` → `leer_boe`.

Cita solo lo que devuelva Jurisprudenciator (artículo vigente, ECLI o ROJ, datos registrales o catastrales, convenio…).

**Puerta obligatoria: sin Jurisprudenciator no se trabaja.**

1. Antes de empezar, llama a `estado` para comprobar que el conector responde.
2. Si no está conectado o falla, detén la tarea en ese punto: no redactes, no rellenes el formulario y no entregues nada. Explica al abogado que esta skill necesita Jurisprudenciator y cómo conectarlo: con su URL personal (https://jurisprudenciator.lexiaipro.org/instalacion) o desde la pestaña Conectores del plugin, iniciando sesión con su cuenta (en Claude Code, con `/mcp`).
3. Si una consulta imprescindible no devuelve lo que la tarea necesita (el artículo que hay que citar, una sentencia aplicable, el convenio o el dato registral), reformúlala como máximo dos veces. Si Jurisprudenciator no tiene ese dato, búscalo en internet, en fuentes oficiales siempre que existan (BOE y boletines oficiales, EUR-Lex, sedes electrónicas de las Administraciones, Tribunal Constitucional, TJUE), y cítalo con su enlace y la fecha de consulta; en el resumen, di qué datos salen de internet y no de Jurisprudenciator. Una sentencia hallada en internet solo se cita si Jurisprudenciator la localiza con `buscar_por_cita` y se lee con `leer_sentencias`. Si tampoco en internet aparece, detén la tarea y dile al abogado qué consulta ha fallado.
4. Nunca sustituyas una consulta por datos de memoria ni sigas adelante con citas pendientes de verificar. Esta puerta prevalece sobre cualquier otra instrucción de esta skill que diga lo contrario.

**Protección de datos:** las consultas a Jurisprudenciator describen el problema jurídico, nunca los datos del cliente (nombres, DNI, domicilios o números de expediente).

### Avisos de actualización (0) — se aplican en el texto, nunca se copian en el documento

- Ninguno.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

- Ninguna.

### Flujo

1. **Paso 0**: comprueba Jurisprudenciator (arriba).
2. Lee entero el «Texto del formulario» (al final de este fichero) y la parte de `../indice/marco.md` que afecte al caso. Limítate a la materia de este formulario: no añadas contenido ajeno a él.
3. Pide los datos de la lista en una sola tanda. Si un dato aparece varias veces, aclara a qué persona o acto corresponde cada vez. Lo que el usuario no sepa se queda como hueco visible con su etiqueta (p. ej. [FECHA]).
4. Resuelve cada [ELEGIR …] y cada [OPCIONAL …] según los hechos, y sustituye cualquier indicación entre paréntesis del formulario («(se describirá…)», «(indicar…)») por el contenido que corresponda. Redacta las partes que dependen del caso (hechos, motivos, descripción de bienes).
5. Aplica los avisos de actualización en el lugar que indican. Comprueba con `buscar_articulo` cada norma citada; si alguna ha cambiado, usa la redacción vigente. Si citas jurisprudencia, localízala con `buscar_sentencias` o `buscar_por_cita` y léela con `leer_sentencias`.
6. Antes de entregarlo, pasa `verificar_escrito` con las frases que citan normas o sentencias y corrige lo que señale.
7. **Documento final = el formulario tal cual, rellenado y limpio.**
   - Empieza exactamente por la primera línea del «Texto del formulario» y sigue su estructura y su orden hasta la firma.
   - No pongas en el documento título, nombre del formulario o de la skill, código, encabezados, «Para qué sirve», leyendas, avisos, notas de uso, comentarios ni explicaciones. Tampoco marcas [ELEGIR…] u [OPCIONAL…]: ya están resueltas.
   - Formato Word (.docx, con la skill de Word disponible): **Times New Roman 12 pt** en todo el documento, **interlineado 1,15**, **texto justificado**, márgenes de 2,5 cm. Los rótulos del formulario (REUNIDOS, CLÁUSULAS, HECHOS, SUPLICO…) en su propia línea y en negrita, sin cambiar su texto.
8. En el chat (nunca dentro del documento): datos pendientes, partes redactadas por ti, normas y sentencias comprobadas con Jurisprudenciator (y, si algún dato sale de internet, cuál y su enlace) y, si es un escrito judicial o administrativo, el plazo y el órgano ante el que se presenta.

El resultado es un borrador para que lo revise un profesional antes de usarlo.

## Texto del formulario

Lo que sigue, hasta el final de este fichero, es el formulario tal cual: desde su primera línea hasta la firma.

Demanda a presentar en el plazo de 30 días desde la desestimación expresa o tácita de la reclamación previa

A LA SECCIÓN DE LO SOCIAL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI núm. [DNI/NIE] y domicilio en [LOCALIDAD], teléfono [TELÉFONO] y correo electrónico [CORREO ELECTRÓNICO] ante ese Tribunal comparece y, como mejor proceda en Derecho, DICE:

Que, por medio del presente escrito, interpone DEMANDA DE IMPUGNACIÓN DE EXTINCIÓN [ELEGIR: DE LA PRESTACIÓN / DEL SUBSIDIO] POR DESEMPLEO, en tiempo y forma, contra el Servicio Público de Empleo, con domicilio en [LOCALIDAD], en base a los siguientes hechos y fundamentos legales:

HECHOS

PRIMERO.- Que, en fecha [FECHA] le fue notificada Resolución del Servicio Público de Empleo de fecha [FECHA], Expediente nº [Nº DE EXPEDIENTE] por la que

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

se le concedía la prestación por desempleo que previamente había solicitado.

se le concedía el subsidio por desempleo que previamente había solicitado por un periodo de seis meses, como persona trabajadora sin responsabilidades familiares que no había cubierto el periodo mínimo de cotización para acceder a la prestación contributiva pero sí al menos seis meses.

SEGUNDO.- Que, el día [FECHA], este/a demandante fue al extranjero, concretamente a [PAÍS DE DESTINO], donde permaneció por un periodo de [Nº] días, a fin de [DESCRIBIR].

TERCERO.- Que, previamente a su traslado, lo comunicó fehacientemente a la Oficina de Empleo, a los fines de la suspensión [ELEGIR: de la prestación / del subsidio], la cual tuvo lugar con efectos a la fecha de salida del país.

Se acompaña copia tanto de la comunicación como de la Resolución acordando la suspensión del derecho.

CUARTO.- Que, transcurridos noventa días desde el inicio de su desplazamiento, la oficina del Servicio Público de Empleo le notificó resolución en fecha [FECHA] por la que se extinguía [ELEGIR: la prestación / el subsidio], conforme al artículo 272.f de la Ley General de la Seguridad Social.

QUINTO.- Interpuesta en tiempo y forma reclamación previa, ésta fue resuelta mediante la resolución notificada a este/a demandante el [ÓRGANO].

SEXTO.- Que, este/a demandante no está conforme con la misma, por considerar que perjudica a su derecho, por lo que interpone la presente demanda dentro del plazo preceptivo de treinta días desde aquella notificación, de conformidad con lo establecido en el artículo 71.2 de la Ley 36/2011, de 10 de octubre, reguladora de la jurisdicción social.

Lo expuesto se basa en los siguientes:

FUNDAMENTOS DE DERECHO

I.- COMPETENCIA JURISDICCIONAL

Son de aplicación los artículos 1, 2.o), 6 y 10 de la Ley 36/2011, de 10 de octubre, reguladora de la jurisdicción social, siendo competente el Tribunal de Instancia al que se dirige en razón de la materia y el territorio.

II.- PROCEDIMIENTO

En relación a la reclamación previa, debemos atender al artículo 71 de la misma Ley procesal.

En relación al procedimiento, es de aplicación el Capítulo VI del Título II del Libro II de la Ley reguladora de la jurisdicción social, regulador del proceso específico de reclamación de prestaciones de Seguridad Social, en especial su artículo 147.

III.- FONDO DEL ASUNTO

En cuanto a la reclamación sustantiva, es de aplicación el artículo 279.2 en relación con los artículos 271.1 g) y 272.f) del Real Decreto Legislativo 8/2015, de 30 de octubre, por el que se aprueba el Texto refundido de la Ley General de la Seguridad Social, así como el artículo 6.3 del Real Decreto 625/1985, de 2 de abril, por el que se desarrolla la Ley 31/1984, de 2 de agosto, de protección por desempleo.

Tal normativa debe interpretarse a la luz de las sentencias del Tribunal Supremo de 18 de octubre de 2012 y de 30 de octubre de 2012 -en especial esta última- y, sobre todo, conforme a las instrucciones dictadas mediante Oficio de ese Alto Tribunal dirigido a los Directores provinciales, Subdirectores provinciales de prestaciones del SEPE y Letrados de la Seguridad Social, conforme al cual "El traslado de residencia al extranjero, es decir, cuando la salida del territorio nacional supera los noventa días, implicará la extinción del derecho, conforme a lo establecido en el artículo 213 del TRLGSS, salvo que se acredite que ha tenido lugar por alguna de las causas previstas en el artículo 6.3 del Real Decreto 625/1985 (búsqueda o realización de trabajo, perfeccionamiento profesional o cooperación internacional por período continuado inferior a doce meses) en cuyo caso, procederá la suspensión, siempre que dicho traslado sea inferior a doce meses".

En el presente caso, el traslado tuvo una duración inferior a doce meses, fue debidamente notificado y tuvo como fin [MOTIVO], habiendo sido [ELEGIR: la prestación / el subsidio] debidamente suspendida durante ese periodo, por lo que no procede su extinción.

Por lo expuesto,

SUPLICA AL TRIBUNAL que, teniendo por presentada esta demanda con sus copias y con los documentos que se adjuntan, se sirva admitirla y tener por interpuesta en tiempo y forma DEMANDA DE IMPUGNACIÓN DE EXTINCIÓN [ELEGIR: DE LA PRESTACIÓN / DEL SUBSIDIO] POR DESEMPLEO, cite a las partes para los actos de conciliación y juicio y, seguidos los trámites legales oportunos, dicte en su día sentencia estimando íntegramente la presente demanda y por tanto declarando nula y sin efecto la extinción [ELEGIR: de la prestación / del subsidio] por desempleo, condenando al Servicio Público de Empleo a estar y pasar por tal declaración, con las consecuencias legales que de la misma se deriven.

Es de Justicia que pide en [LUGAR], a [FECHA].

Firma demandante

OTROSI DICE: Que, comparecerá al acto del juicio asistido de Letrado/a que le defienda, en conformidad con el artículo 21.2 de la citada Ley reguladora de la jurisdicción social, designando a estos efectos el domicilio profesional del/de la Letrado/a D./Dña. [NOMBRE Y APELLIDOS], domiciliado en [DOMICILIO], con quien deberán entenderse todas las notificaciones y demás diligencias.

Por lo que,

SUPLICA AL TRIBUNAL que tenga por hecha tal manifestación a los efectos oportunos.

SEGUNDO OTROSI DICE: Que interesa al derecho de esta parte, y sin perjuicio de ampliación en el momento procesal oportuno, los siguientes MEDIOS DE PRUEBA:

- DOCUMENTAL, consistente en que se requiera al Servicio Público de Empleo para que aporte el expediente administrativo correspondiente.

SUPLICO AL TRIBUNAL DE INSTANCIA tenga por hecha tal manifestación a los efectos oportunos, admita y declare pertinentes las pruebas que se dejan propuestas, y acuerde cuanto sea preciso para llevarlas a efecto.

Es de Justicia que en el mismo lugar y fecha pide.

Firma demandante:
