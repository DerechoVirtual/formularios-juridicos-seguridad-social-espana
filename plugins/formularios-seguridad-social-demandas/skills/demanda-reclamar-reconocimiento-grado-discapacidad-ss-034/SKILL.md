---
name: demanda-reclamar-reconocimiento-grado-discapacidad-ss-034
description: "Demanda para reclamar el reconocimiento del grado de discapacidad. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda para reclamar el reconocimiento del grado de discapacidad

> Formulario **SS-034** del plugin **Seguridad Social: demandas y recursos ante lo social** (`formularios-seguridad-social-demandas`) · Seguridad Social › Demandas y escritos ante la jurisdicción social · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda para reclamar el reconocimiento del grado de discapacidad» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda para reclamar el reconocimiento del grado de discapacidad” para mi caso». También puedes invocarla directamente con `/formularios-seguridad-social-demandas:demanda-reclamar-reconocimiento-grado-discapacidad-ss-034`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-seguridad-social-demandas:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Seguridad Social: demandas y recursos ante lo social) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (7 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] MOTIVO (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] PARTE DEMANDADA (2 veces)
- [ ] PORCENTAJE (2 veces)
- [ ] COLEGIO PROFESIONAL
- [ ] CORREO ELECTRÓNICO
- [ ] DOLENCIAS
- [ ] DOLENCIAS NO VALORADAS
- [ ] FUNDAMENTOS
- [ ] LUGAR
- [ ] NOMBRE O DENOMINACIÓN
- [ ] Nº
- [ ] Nº DE COLEGIADO/A
- [ ] NÚMERO
- [ ] OTROS DATOS
- [ ] SEDE
- [ ] TELÉFONO
- [ ] ÓRGANO

## Normas que cita el formulario

- No cita artículos concretos; Claude localizará las normas aplicables con Jurisprudenciator si el documento las necesita.

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

El Real Decreto 888/2022, de 18 de octubre, regula el procedimiento para el reconocimiento, declaración y calificación del grado de discapacidad, el establecimiento de los baremos aplicables, así como la determinación de los órganos competentes para el reconocimiento, La calificación del grado de discapacidad responde a criterios técnicos unificados, fijados mediante los baremos que se acompañan como anexos a este Real Decreto.

Contra las resoluciones de reconocimiento de grado de discapacidad y de revisión del grado de discapacidad que se dicten por la Administración competente, las personas interesadas, con o sin medidas de apoyo para el ejercicio de su capacidad jurídica, podrán interponer reclamación previa a la vía jurisdiccional social, de conformidad con lo dispuesto en el artículo 71 de la Ley 36/2011, de 10 de octubre, reguladora de la jurisdicción social.

Contra la resolución que desestime la reclamación previa podrá interponerse demanda ante la Sección de lo Social del Tribunal de Instancia conforme a la modalidad procesal de prestaciones de Seguridad Social (arts. 140 y ss LRJS).

Actualizado en base al Real Decreto 888/2022, de 18 de octubre, por el que se establece el procedimiento para el reconocimiento, declaración y calificación del grado de discapacidad


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

A LA SECCIÓN DE LO SOCIAL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, provisto/a de D.N.I. nº [NÚMERO], y con domicilio en [LOCALIDAD], ante el Tribunal comparezco y, como mejor proceda en Derecho, DIGO:

Que por medio el presente escrito, formulo demanda de reclamación de RECONOCIMIENTO DE GRADO DE INCAPACIDAD, contra [PARTE DEMANDADA], en su legal representante, con domicilio en [LOCALIDAD], en base a los siguientes

HECHOS

Primero.- Que en fecha [FECHA] presenté solicitud de reconocimiento de grado de incapacidad ante [ÓRGANO] en el modelo establecido al efecto, al que acompañé los informes médicos y psicológicos preceptivos y aquellos que consideré oportunos para hacer valer mi pretensión por padecer [DOLENCIAS].

Segundo.- Por el Equipo de Valoración y Orientación, y tras el reconocimiento médico que tuvo lugar con fecha [FECHA], se emitió dictamen el [FECHA], en el que se hace constar que en el momento del reconocimiento presentoó: «[NOMBRE O DENOMINACIÓN]».

Tercero.- Que en fecha [FECHA] se me notificó la resolución dictada por el órgano indicado, la cual desestimó mi solicitud inicial en base al dictamen emitido por el Equipo de Valoración y Orientación, por entender que tenía un grado de discapacidad inferior al 33%, concretamente del [PORCENTAJE] %.

Cuarto.- Que, dentro del plazo de treinta días, interpuse reclamación previa contra dicha resolución ante el mismo órgano que la dictó, por entender que [MOTIVO].

Quinto.-

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

Que el [FECHA], se me notificó resolución de fecha [FECHA] por la que se desestimaba la reclamación previa en base a [MOTIVO].

El órgano gestor no ha valorado de forma correcta mi situación, ya que no se han tenido en cuenta: [DOLENCIAS NO VALORADAS].

Que habiendo transcurrido cuarenta y cinco días hábiles desde la interposición de la reclamación previa sin haberse dictado resolución alguna, aquella se entiende desestimada por silencio administrativo.

Sexto.- En aplicación de los vigentes baremos de valoración de indiscapacidad me corresponde un grado de incapacidad global del %. Asimismo, examinadas las circunstancias que concurren y en aplicación de los baremos sociales me corresponde una puntuación por factores sociales complementarios de [Nº] puntos, por lo que en conjunto se me debe reconocer un Grado Total de Incapacidad del %. [PORCENTAJE].

FUNDAMENTOS DE DERECHO

PRIMERO.- Los artículos 1, 2 o), 6, 10.2 a) y 71 de la Ley 36/2011, de 10 de octubre, reguladora de la jurisdicción social, siendo competente el Tribunal de Instancia al que me dirijo en razón de la materia y territorio.

SEGUNDO.- El Real Decreto 888/2022, de 18 de octubre, por el que se establece el procedimiento para el reconocimiento, declaración y calificación del grado de incapacidad.

[OPCIONAL — incluir si procede]

TERCERO.- [FUNDAMENTOS].

[OPCIONAL — incluir si procede]

CUARTO.-.

Por lo expuesto,

SUPLICO A LA SECCIÓN DE LO SOCIAL DEL TRIBUNAL DE INSTANCIA que, teniendo por presentado este escrito con las copias y documentos que se adjuntan, se digne admitirlo, tenga por formulada demanda en RECLAMACIÓN DE RECONOCIMIENTO DE GRADO DE INCAPACIDAD, contra [PARTE DEMANDADA] y, previos los trámites legales oportunos, se dicte en su día sentencia estimando íntegramente la presente demanda, por la que se declare al/a la demandante afecto de una incapacidad del %, condenando a la demandada a estar y pasar por esta declaración con todos los derechos inherentes a la misma.

OTROSÍ DIGO: Que acudiré a juicio [OTROS DATOS], D./Dña [NOMBRE Y APELLIDOS], Colegiado/a nº [Nº DE COLEGIADO/A] del [COLEGIO PROFESIONAL], con domicilio en [LOCALIDAD], teléfono [TELÉFONO], correo electrónico [CORREO ELECTRÓNICO].

SEGUNDO OTROSÍ DIGO: Que se requiera al órgano gestor para que remita el expediente administrativo.

Todo ello por ser de Justicia que pido en [LUGAR], a [FECHA].
