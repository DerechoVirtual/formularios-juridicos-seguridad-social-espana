---
name: demanda-reconocimiento-accidente-trabajo-dana-octubre-ss-004
description: "Demanda de reconocimiento de accidente de trabajo por la DANA de octubre y noviembre de 2024. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de reconocimiento de accidente de trabajo por la DANA de octubre y noviembre de 2024

> Formulario **SS-004** del plugin **Seguridad Social: demandas y recursos ante lo social** (`formularios-seguridad-social-demandas`) · Seguridad Social › Demandas y escritos ante la jurisdicción social · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de reconocimiento de accidente de trabajo por la DANA de octubre y noviembre de 2024» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de reconocimiento de accidente de trabajo por la DANA de octubre y noviembre de 2024” para mi caso». También puedes invocarla directamente con `/formularios-seguridad-social-demandas:demanda-reconocimiento-accidente-trabajo-dana-octubre-ss-004`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-seguridad-social-demandas:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Seguridad Social: demandas y recursos ante lo social) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (6 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] CORREO ELECTRÓNICO
- [ ] DNI/NIE
- [ ] DOCUMENTOS ACREDITATIVOS
- [ ] FECHAS
- [ ] LUGAR
- [ ] NOMBRE DEL CENTRO MÉDICO
- [ ] Nº
- [ ] Nº DE AFILIACIÓN
- [ ] Nº DE EXPEDIENTE
- [ ] NÚMERO
- [ ] SEDE
- [ ] TELÉFONO

## Normas que cita el formulario

- art. 25 Real Decreto-ley 6/2024
- art. 71 Ley 36/2011
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

### Avisos de actualización (1) — se aplican en el texto, nunca se copian en el documento

- Junto a «…e A LA SECCIÓN DE LO SOCIAL DEL TRIBUNAL DE INSTANCIA DE [SEDE] – PLAZA N.º [Nº]»: Desde el 31-12-2025 los Juzgados de lo Social son la Sección de lo Social del Tribunal de Instancia; el Tribunal no se numera, se numera la plaza. En la demanda inicial (antes del reparto) se omite la plaza. Fuente: arts. 84.2.i) y 94 LOPJ (red. LO 1/2025); LO 1/2025 DA 1.ª y DT 1.ª (la plaza conserva la numeración del Juzgado; Juzgados de lo Social transformados el 31-12-2025); LOPJ (LO 6/1985), BOE-A-1985-12666; LO 1/2025, BOE-A-2025-76.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

El artículo 25 del Real Decreto-Ley 6/2024 expresa que los procesos de incapacidad temporal producidos en los municipios afectados por la DANA que se inicien desde el 28 de octubre hasta el 31 de diciembre de 2024 como consecuencia de los siniestros tendrán (excepcionalmente) la consideración de situación asimilada a accidente de trabajo, exclusivamente a efectos de la prestación económica de incapacidad temporal del sistema de Seguridad Social. Asimismo, las pensiones de incapacidad permanente, muerte y supervivencia, así como la prestación económica por incapacidad permanente parcial tendrán la consideración, con carácter excepcional, de situación asimilada a accidente de trabajo a los exclusivos efectos del cálculo de su cuantía económica.

Formulario actualizado conforme a las novedades introducidas por el Real Decreto-ley 8/2024, de 28 de noviembre


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

A LA SECCIÓN DE LO SOCIAL DEL TRIBUNAL DE INSTANCIA DE [SEDE] – PLAZA N.º [Nº]

D./Dña. [NOMBRE Y APELLIDOS], con DNI nº [DNI/NIE], y número de afiliación a la Seguridad Social [Nº DE AFILIACIÓN], y con domicilio a efectos de notificaciones en el Despacho del Letrado/a D./Dña. [NOMBRE Y APELLIDOS], sito en [LOCALIDAD], teléfono [TELÉFONO], correo electrónico [CORREO ELECTRÓNICO], ante ese Tribunal comparezco y como mejor proceda en Derecho, DICE:

Que por medio del presente escrito formula DEMANDA DE DECLARACIÓN DE CONTINGENCIA COMO ACCIDENTE DE TRABAJO, causante de los períodos de incapacidad temporal y baja médica entre el [FECHA] y el [FECHA] y, por tanto, del derecho de este demandante a beneficiarse de las prestaciones de [ELEGIR: INCAPACIDAD TEMPORAL / INCAPACIDAD PERMANENTE] correspondientes a dicha contingencia contra el INSTITUTO NACIONAL DE LA SEGURIDAD SOCIAL, en la persona de su representante legal, todo ello en base a los siguientes hechos y fundamentos de Derecho:

HECHOS

PRIMERO.- Que como consecuencia de la DANA acaecida en [LOCALIDAD] los días [FECHAS], sufrí una serie de [ELEGIR: daños personales / lesiones / accidente]
daños personales
lesiones
accidente
  que determinaron mi situación de [ELEGIR: Incapacidad Temporal / Incapacidad Permanente] con efectos desde el día o una IT que posteriormente derivó en IP

SEGUNDO.- Que

el médico facultativo de [NOMBRE DEL CENTRO MÉDICO]

el Equipo de Valoración de Incapacidades determinó que la contingencia de la que derivaba mi patología era enfermedad común y no accidente de trabajo.

TERCERO.- Que, al no estar conforme con dicha calificación de la contingencia, este demandante solicitó la determinación de la contingencia como accidente de trabajo, que fue denegada por resolución de fecha [FECHA], contra la que se formuló reclamación previa a la vía judicial que, asimismo fue denegada por resolución de fecha [FECHA], expediente [Nº DE EXPEDIENTE].

Se acompañan como DOCS. N.º [NÚMERO] copia de las citadas resoluciones y la reclamación previa.

CUARTO.- Que el hecho causante se produjo el día [FECHA], en la localidad de [LOCALIDAD] y fue consecuencia directa de un siniestro ocasionado por la DANA que azotó a diferentes municipios de España, como se acredita con la siguiente documentación: [DOCUMENTOS ACREDITATIVOS], por lo que debe considerarse la contingencia derivada de accidente de trabajo en virtud de lo establecido en el artículo 25 del Real Decreto-ley 6/2024, de 5 de noviembre, por el que se adoptan medidas urgentes de respuesta ante los daños causados por la Depresión Aislada en Niveles Altos (DANA) en diferentes municipios entre el 28 de octubre y el 4 de noviembre de 2024.

Asimismo, y en aplicación de lo establecido en el apartado 1 del citado artículo, como consecuencia de la asimilación a accidente de trabajo, no se requiere para su percepción, período mínimo de cotización.

QUINTO.- Que, por lo anteriormente expuesto y no encontrando conforme a Derecho la referida Resolución en cuanto a la contingencia de la que deriva la incapacidad reconocida, por medio del presente escrito, dentro del plazo legalmente establecido y de conformidad con lo señalado por el artículo 71 de la Ley 36/2011, de 10 de octubre, reguladora de la jurisdicción social, vengo a interponer DEMANDA ante la Sección de lo Social del Tribunal de Instancia.

A los anteriores hechos les son de aplicación los siguientes,

FUNDAMENTOS DE DERECHO

I.- Es competente el Tribunal al que me dirijo en virtud de lo dispuesto en los artículos 1, 2, 6 y 10 de la Ley 36/2011, de 10 de octubre, reguladora de la Jurisdicción Social.

II.- Son de aplicación el artículo 71 de la Ley 36/2011, que regula la reclamación previa, y los artículos 140 a 146 de la misma, reguladores de los procesos seguidos ante Seguridad Social.

III.- En cuanto al fondo del asunto, resulta de aplicación el art. 25 del Real Decreto-ley 6/2024, de 5 de noviembre, por el que se adoptan medidas urgentes de respuesta ante los daños causados por la Depresión Aislada en Niveles Altos (DANA) en diferentes municipios entre el 28 de octubre y el 4 de noviembre de 2024.

Por lo expuesto,

SUPLICO A LA SECCIÓN DE LO SOCIAL DEL TRIBUNAL DE INSTANCIA, que teniendo por presentado este escrito en tiempo y forma, con los documentos que se acompañan, se sirva admitirlo y, en su virtud, tenga por interpuesta demanda sobre DETERMINACIÓN DE CONTINGENCIAS contra el INSTITUTO NACIONAL DE LA SEGURIDAD SOCIAL, tramitando la misma conforme a Derecho, citando a las partes para los trámites previos de conciliación y, en su caso, de juicio, concluyendo las actuaciones con una sentencia estimatoria de la demanda, con los efectos legales que se deriven de tal pronunciamiento, en la que se acuerde declarar que mi situación de incapacidad [ELEGIR: temporal / permanente] deriva de accidente de trabajo.

Por ser de Justicia que pido en [LUGAR], a [FECHA].

PRIMER OTROSI DIGO que se solicita la reclamación de oficio al INSS del expediente y antecedentes que posea en relación con el contenido de la demanda.

SEGUNDO OTROSI DIGO que esta parte acudirá al acto del juicio oral representada de Letrado/a.

TERCER OTROSI DIGO que interesa al Derecho de esta parte que se practiquen en el acto del juicio oral los siguientes

MEDIOS DE PRUEBA

- DOCUMENTAL, TESTIFICAL Y PERICIAL: la aportada con la demanda y la que esta parte aportará en el acto del juicio.

SUPLICO AL TRIBUNAL que tenga por hechas las anteriores manifestaciones y por propuesta la prueba, la admita y la estime pertinente.

Por ser de Justicia que reitero en el lugar y fecha "ut supra"

Fdo.: D./Dña. [NOMBRE Y APELLIDOS]
