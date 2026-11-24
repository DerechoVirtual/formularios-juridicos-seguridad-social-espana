---
name: demanda-reconocimiento-prestacion-desempleo-ss-022
description: "Demanda de reconocimiento de la prestación por desempleo. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de reconocimiento de la prestación por desempleo

> Formulario **SS-022** del plugin **Seguridad Social: demandas y recursos ante lo social** (`formularios-seguridad-social-demandas`) · Seguridad Social › Demandas y escritos ante la jurisdicción social · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de reconocimiento de la prestación por desempleo» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de reconocimiento de la prestación por desempleo” para mi caso». También puedes invocarla directamente con `/formularios-seguridad-social-demandas:demanda-reconocimiento-prestacion-desempleo-ss-022`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-seguridad-social-demandas:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Seguridad Social: demandas y recursos ante lo social) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (6 veces)
- [ ] IMPORTE (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] ACTIVIDAD
- [ ] CORREO ELECTRÓNICO
- [ ] DNI/NIE
- [ ] DOMICILIO
- [ ] FUNDAMENTOS
- [ ] GRUPO O CATEGORÍA PROFESIONAL
- [ ] LUGAR
- [ ] MOTIVO
- [ ] Nº
- [ ] PLAZO
- [ ] SEDE
- [ ] TELÉFONO

## Normas que cita el formulario

- art. 1 Ley 36/2011

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

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI núm. [DNI/NIE] y domicilio en [LOCALIDAD], teléfono [TELÉFONO] y correo electrónico [CORREO ELECTRÓNICO], ante ese Tribunal comparece y, como mejor proceda en Derecho, DICE:

Que, por medio del presente escrito, interpone demanda en reclamación del RECONOCIMIENTO DE LA PRESTACIÓN POR DESEMPLEO, en tiempo y forma, contra el SERVICIO PÚBLICO DE EMPLEO, con domicilio en [LOCALIDAD], en base a los siguientes hechos y fundamentos legales:

HECHOS

PRIMERO.- Que, este/a demandante vino prestando servicios en la actividad de [ACTIVIDAD] y en el grupo profesional de [GRUPO O CATEGORÍA PROFESIONAL], mediante un contrato de trabajo por tiempo determinado de [PLAZO] de duración, concretamente desde el [FECHA] hasta el [FECHA], fecha en que la empresa le comunicó la finalización de su contrato de trabajo por haber llegado a su término.

Se acompaña carta de extinción del contrato de trabajo.

Tales servicios no eran de temporada, toda vez que la empresa empleadora, permanece abierta todo el año.

SEGUNDO.- Que, el salario mensual que percibía por tales servicios era de [IMPORTE] euros brutos mensuales, siendo la base reguladora mensual de [IMPORTE] euros.

TERCERO.- Que, en fecha [FECHA] solicitó la prestación por desempleo, siendo denegada mediante resolución de [FECHA] de fecha [FECHA] por [MOTIVO].

Interpuesta reclamación previa contra la citada resolución dentro del plazo de treinta días establecido al efecto, ha sido desestimada por silencio administrativo del organismo demandado.

Se acompaña a la presente demanda copia de la resolución denegatoria y de la reclamación previa.

CUARTO.- Que tiene cotizados más de [Nº] días dentro de los 6 años anteriores al cese, el cual ha sido motivado por expiración del tiempo por el que fue contratado; se ha inscrito como desempleado y ha solicitado la prestación por desempleo dentro de los quince días hábiles siguientes al de finalización del trabajo.

Por ello, considera injustificados los motivos alegados por el organismo para la denegación de la prestación y reclama su reconocimiento mediante la presente demanda, interpuesta dentro del preceptivo plazo de treinta días desde que la reclamación previa debió entenderse denegada por silencio administrativo.

Lo expuesto se basa en los siguientes:

FUNDAMENTOS DE DERECHO

I.- En cuanto a la competencia jurisdiccional, son de aplicación los artículos 1, 2 o), 6 y 10 de la Ley 36/2011, de 10 de octubre, reguladora de la jurisdicción social, siendo competente el Tribunal de Instancia al que me dirijo en razón de la materia y territorio.

II.- En cuanto al procedimiento, los artículos 71 y 140 a 147 de la misma Ley procesal [FUNDAMENTOS].

III.- En cuanto a la reclamación sustantiva, son de aplicación los artículos 266 de la Ley General de la Seguridad Social y concordantes.

Por lo expuesto,

SUPLICA AL TRIBUNAL que, teniendo por presentada esta demanda con sus copias y los documentos adjuntos, se sirva admitirla y tener por interpuesta en tiempo y forma demanda en reclamación de RECONOCIMIENTO DE PRESTACIÓN POR DESEMPLEO, cite a las partes para los actos de conciliación y juicio y, seguidos los trámites legales oportunos, dicte en su día sentencia estimando íntegramente la presente demanda y por tanto el derecho del/de la demandante a percibir la prestación por desempleo, con efectos al día siguiente al de su cese en la ocupación y hasta tanto se cumplan los plazos legales o encuentre ocupación remunerada, condenando al Servicio Público de Empleo a estar y pasar por tal declaración.

Por lo que,

Es de Justicia que pide en [LUGAR], a [FECHA].

Firma demandante

PRIMER OTROSI DICE: Que comparecerá al acto del juicio asistido de Letrado/a que le defienda, en conformidad con el artículo 21.2 de la citada Ley reguladora de la jurisdicción social, designando a estos efectos el domicilio profesional del/de la Letrado/a D./Dña. [NOMBRE Y APELLIDOS], domiciliado en [DOMICILIO], con quien deberán entenderse todas las notificaciones y demás diligencias.

SUPLICA AL TRIBUNAL que tenga por hecha tal manifestación a los efectos oportunos.

SEGUNDO OTROSI DICE: Que se solicita la reclamación de oficio al Servicio Público de Empleo Estatal del expediente y antecedentes que posea en relación con el contenido de la demanda.

SUPLICA AL TRIBUNAL que tenga por hecha tal manifestación a los efectos oportunos.

TERCER OTROSI DICE: Que interesa al Derecho de esta parte que se practiquen en el acto del juicio oral los siguientes:

MEDIOS DE PRUEBA

- DOCUMENTAL y TESTIFICAL: la que esta parte aportará en el acto del juicio, así como la documental aportada con esta demanda.

SUPLICA AL TRIBUNAL que tenga por propuesta la prueba, la admita y la estime pertinente.

Por ser de Justicia que se pide en el lugar y fecha ut supra

Firma demandante
