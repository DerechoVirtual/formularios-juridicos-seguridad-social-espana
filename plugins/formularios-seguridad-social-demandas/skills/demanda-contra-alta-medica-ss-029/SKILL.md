---
name: demanda-contra-alta-medica-ss-029
description: "Demanda contra el alta médica. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda contra el alta médica

> Formulario **SS-029** del plugin **Seguridad Social: demandas y recursos ante lo social** (`formularios-seguridad-social-demandas`) · Seguridad Social › Demandas y escritos ante la jurisdicción social · normativa revisada el 24-11-2026.

## Qué es

Demanda ante la jurisdicción social por la que el trabajador impugna el alta médica emitida por la entidad gestora (INSS) o la mutua colaboradora, para ser repuesto en la situación de incapacidad temporal.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda contra el alta médica» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda contra el alta médica” para mi caso». También puedes invocarla directamente con `/formularios-seguridad-social-demandas:demanda-contra-alta-medica-ss-029`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-seguridad-social-demandas:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Seguridad Social: demandas y recursos ante lo social) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] DOMICILIO COMPLETO (4 veces)
- [ ] Nº (4 veces)
- [ ] FECHA (3 veces)
- [ ] DENOMINACIÓN DE LA MUTUA (2 veces)
- [ ] FECHA DEL ALTA (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL LETRADO/A (2 veces)
- [ ] AÑO
- [ ] CENTRO DE TRABAJO
- [ ] CENTRO MÉDICO
- [ ] CORREO ELECTRÓNICO
- [ ] CUADRO MÉDICO
- [ ] DENOMINACIÓN SOCIAL
- [ ] DIAGNÓSTICO
- [ ] DNI/NIE
- [ ] DÍA
- [ ] ESPECIALIDAD
- [ ] FECHA DE AFILIACIÓN
- [ ] FECHA DE LA BAJA
- [ ] GENERAL O ESPECIAL QUE CORRESPONDA
- [ ] MES
- [ ] MOTIVO DEL ALTA
- [ ] NOMBRE Y APELLIDOS
- [ ] NOMBRE Y APELLIDOS DEL DEMANDANTE
- [ ] NOMBRE Y APELLIDOS DEL PERITO
- [ ] Nº DE AFILIACIÓN
- [ ] Nº DE DÍAS
- [ ] PROFESIÓN
- [ ] SEDE
- [ ] TELÉFONO

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

NOTAS PREVIAS (suprimir antes de presentar):

La demanda de impugnación de alta médica, regulada en los arts. 140 y siguientes de la LRJS, es la vía judicial prevista para que la persona trabajadora cuestione la resolución de alta médica emitida por los órganos competentes de las entidades gestoras de la Seguridad Social, se haya agotado o no el plazo máximo de duración de trescientos sesenta y cinco días de la prestación de incapacidad temporal.

Debe acreditarse el agotamiento de la vía administrativa correspondiente, salvo en los procesos de impugnación de altas médicas emitidas por los órganos competentes de las entidades gestoras de la Seguridad Social al agotarse el plazo de duración de trescientos sesenta y cinco días de la prestación de incapacidad temporal (art. 71.1 LRJS).

La demanda se dirige exclusivamente contra la entidad gestora (INSS) y, en su caso, contra la mutua colaboradora. No es necesario demandar al servicio público de salud salvo que el alta haya sido emitida por sus servicios médicos, ni a la empresa salvo que se cuestione la contingencia.


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

D./Dña. [NOMBRE Y APELLIDOS DEL DEMANDANTE], mayor de edad, con DNI n.º [DNI/NIE], y con domicilio en [DOMICILIO COMPLETO], teléfono [TELÉFONO], correo electrónico [CORREO ELECTRÓNICO], ante la Sección de lo Social del Tribunal de Instancia comparece y, como mejor proceda en Derecho, DICE:

Que por medio del presente escrito, y dentro del plazo legalmente establecido, interpone demanda de IMPUGNACIÓN DEL ALTA MÉDICA contra:

[ELEGIR LAS QUE PROCEDAN Y SUPRIMIR LAS DEMÁS:]

— EL INSTITUTO NACIONAL DE LA SEGURIDAD SOCIAL

— LA MUTUA COLABORADORA CON LA SEGURIDAD SOCIAL [DENOMINACIÓN DE LA MUTUA]

— LA EMPRESA [DENOMINACIÓN SOCIAL] (solo si se cuestiona la contingencia)

con domicilio en [DOMICILIO COMPLETO], en la persona de sus legales representantes.

Se basa la presente demanda en los siguientes hechos y fundamentos de derecho:

HECHOS

PRIMERO.– Que el/la demandante nació en [LOCALIDAD] el día [FECHA], figurando afiliado/a al Régimen [GENERAL O ESPECIAL QUE CORRESPONDA] de la Seguridad Social desde [FECHA DE AFILIACIÓN], con el número de afiliación [Nº DE AFILIACIÓN], y sin que hasta el momento tenga ningún descubierto de cotización.

SEGUNDO.– Que el día [FECHA DE LA BAJA], [ELEGIR: ante las dolencias que sufría / ante el accidente ocurrido en el centro de trabajo [CENTRO DE TRABAJO]], esta parte acudió [ELEGIR: al Centro Médico [CENTRO MÉDICO] / a la Mutua colaboradora [DENOMINACIÓN DE LA MUTUA]], donde fue dado/a de baja por [ELEGIR: enfermedad común / accidente de trabajo / enfermedad profesional], habiéndosele diagnosticado por los facultativos el siguiente cuadro médico: [CUADRO MÉDICO], e indicándose, de esta manera, una serie de prescripciones médicas a seguir por el/la suscribiente. Se aporta a este escrito parte de baja como documento número [Nº].

TERCERO.– Que en esa situación de incapacidad temporal ha permanecido durante [Nº DE DÍAS] días, siendo dado/a de alta por la entidad gestora en fecha [FECHA DEL ALTA], por entender que [MOTIVO DEL ALTA], y por lo tanto esta parte podía haberse incorporado al trabajo. Se aporta parte de alta como documento número [Nº].

CUARTO.– Que no obstante lo que antecede, el/la demandante sigue teniendo achaques y padecimientos derivados de [ELEGIR: la insuficiente curación de su enfermedad / sus dolencias / su patología / tal enfermedad], y ello pese a que se han seguido todas las prescripciones facultativas que en su día se le han mandado, tanto al inicio como en las subsiguientes revisiones médicas.

QUINTO.– Que por tal motivo ha acudido a otro médico especialista en la materia, a fin de que fuera de nuevo examinado y emitiese su informe, siéndole diagnosticado [DIAGNÓSTICO], y sin que se entienda por dicho especialista que se pueda reanudar la labor de [PROFESIÓN], aportándose a la presente reclamación como documento número [Nº].

SEXTO.– Que, no estando conforme con el alta médica emitida con fecha [FECHA DEL ALTA], se inició el correspondiente procedimiento de disconformidad, que finalizó con una resolución denegatoria de fecha [FECHA]. Se acompaña a este escrito resolución denegatoria como documento número [Nº].

[NOTA: conforme a lo establecido en el art. 71.1 de la Ley reguladora de la jurisdicción social, si el alta médica se emite al agotarse el plazo de 365 días de la prestación de incapacidad temporal, no es preceptiva la reclamación previa.]

SÉPTIMO.– Que no encontrando conforme a Derecho la referida resolución, por medio del presente escrito, dentro del plazo legalmente establecido y de conformidad con lo señalado por los artículos 71 y 140 y siguientes de la Ley reguladora de la jurisdicción social, viene a interponer DEMANDA ante la Sección de lo Social del Tribunal de Instancia.

A los anteriores hechos les son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

I.– Artículos 1, 2 o), 6, 10 y 140 de la Ley 36/2011, de 10 de octubre, reguladora de la jurisdicción social, siendo competente dicha Sección de lo Social del Tribunal de Instancia en razón de la materia y territorio.

II.– Artículos 169 a 176 del texto refundido de la Ley General de la Seguridad Social, aprobado por Real Decreto Legislativo 8/2015, de 30 de octubre.

III.– Real Decreto 1430/2009, de 11 de septiembre, por el que se desarrolla reglamentariamente la Ley 40/2007, de 4 de diciembre, de medidas en materia de Seguridad Social, en relación con la prestación de incapacidad temporal.

En virtud de cuanto antecede es por lo que,

SUPLICO AL TRIBUNAL que, teniendo por presentado este escrito con sus copias y documentos que se adjuntan, se digne admitirlo, tenga por formulada demanda de impugnación del alta médica acordada por el INSS en fecha [FECHA], contra las partes demandadas, se proceda a convocar a las partes para los actos de conciliación y juicio, en la debida forma, por el que, seguidos todos sus trámites legales oportunos, se dicte en su día sentencia estimando íntegramente la presente demanda, por la que se condene a las partes demandadas, en su respectivo carácter, a que repongan al/la actor/a a la anterior situación de incapacidad temporal por no haber sanado en su totalidad, y hasta que se produzca tal situación o se agote el plazo dispuesto en el artículo 169.1.a) del texto refundido de la Ley General de la Seguridad Social.

PRIMER OTROSÍ DIGO: Que al acto de juicio compareceré asistido de Letrado para que me defienda, de conformidad con el artículo 21.2 de la Ley reguladora de la jurisdicción social, designando el domicilio profesional del Letrado D./Dña. [NOMBRE Y APELLIDOS DEL LETRADO/A] en [DOMICILIO COMPLETO], a efectos de notificaciones y demás diligencias.

SUPLICO AL TRIBUNAL tenga por hecha tal manifestación a los efectos oportunos.

SEGUNDO OTROSÍ DIGO: Que interesa al derecho de esta parte proponer, para el acto del juicio oral, la práctica de la prueba pericial médica efectuada por D./Dña. [NOMBRE Y APELLIDOS DEL PERITO], especialidad [ESPECIALIDAD], con domicilio profesional en [DOMICILIO COMPLETO],

SUPLICO AL TRIBUNAL acuerde su citación y notificación personal.

TERCER OTROSÍ DIGO: Que se solicita la reclamación de oficio al INSS (o, en su caso, también a la mutua colaboradora) del expediente y antecedentes que posea en relación con el contenido de la demanda.

SUPLICO AL TRIBUNAL acuerde la solicitud del citado expediente.

Todo ello por ser de Justicia que respetuosamente se pide en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del demandante: [NOMBRE Y APELLIDOS]

Firma del Letrado/a: [NOMBRE Y APELLIDOS DEL LETRADO/A]
