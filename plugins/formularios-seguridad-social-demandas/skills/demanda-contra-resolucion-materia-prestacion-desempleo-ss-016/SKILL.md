---
name: demanda-contra-resolucion-materia-prestacion-desempleo-ss-016
description: "Demanda contra la resolución en materia de prestación por desempleo. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda contra la resolución en materia de prestación por desempleo

> Formulario **SS-016** del plugin **Seguridad Social: demandas y recursos ante lo social** (`formularios-seguridad-social-demandas`) · Seguridad Social › Demandas y escritos ante la jurisdicción social · normativa revisada el 24-11-2026.

## Qué es

Demanda ante la jurisdicción social para impugnar la resolución de la entidad gestora (SEPE) que reconoce la prestación por desempleo en cuantía o duración inferior a la que corresponde, una vez agotada la reclamación previa.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda contra la resolución en materia de prestación por desempleo» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda contra la resolución en materia de prestación por desempleo” para mi caso». También puedes invocarla directamente con `/formularios-seguridad-social-demandas:demanda-contra-resolucion-materia-prestacion-desempleo-ss-016`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-seguridad-social-demandas:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Seguridad Social: demandas y recursos ante lo social) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (6 veces)
- [ ] Nº (6 veces)
- [ ] Nº DE MESES (4 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] FECHA (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL LETRADO/A (2 veces)
- [ ] SEDE (2 veces)
- [ ] ACTIVIDAD DE LA EMPRESA
- [ ] AÑO
- [ ] CATEGORÍA PROFESIONAL
- [ ] CORREO ELECTRÓNICO
- [ ] DNI/NIE
- [ ] DOMICILIO COMPLETO
- [ ] DOMICILIO COMPLETO DEL SEPE
- [ ] DOMICILIO SOCIAL
- [ ] DÍA
- [ ] FECHA DE INICIO
- [ ] MES
- [ ] Nº DE PROCEDIMIENTO
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

Se trata de la modalidad procesal de prestaciones de Seguridad Social (arts. 140 y ss. LRJS).

Formulada la reclamación previa, que es requisito necesario para formular demanda en materia de prestaciones de Seguridad Social (con la excepción de la impugnación de altas médicas transcurridos 365 días), la Entidad deberá contestar expresamente a la misma en el plazo de cuarenta y cinco días. En caso contrario se entenderá denegada la reclamación por silencio administrativo.

La demanda habrá de formularse en el plazo de treinta días, a contar desde la fecha en que se notifique la denegación de la reclamación previa o desde el día en que se entienda denegada por silencio administrativo (art. 71 LRJS).


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

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI n.º [DNI/NIE], y con domicilio en [DOMICILIO COMPLETO], teléfono [TELÉFONO] y correo electrónico [CORREO ELECTRÓNICO], ante la Sección de lo Social del Tribunal de Instancia comparece y, como mejor proceda en Derecho, DICE:

Que mediante el presente escrito interpone demanda de IMPUGNACIÓN DE LA PRESTACIÓN DE DESEMPLEO, en tiempo y forma legalmente establecidos, contra el Servicio Público de Empleo Estatal, con domicilio en [DOMICILIO COMPLETO DEL SEPE], y contra la empresa [DENOMINACIÓN SOCIAL], con domicilio social en [DOMICILIO SOCIAL], todos ellos en la persona de sus representantes legales, en base a los siguientes hechos y fundamentos de derecho:

HECHOS

PRIMERO.– Que el/la demandante ha venido prestando servicios en la aludida empresa desde el día [FECHA DE INICIO], con la categoría profesional de [CATEGORÍA PROFESIONAL] y un salario mensual de [IMPORTE] euros, incluida la prorrata de pagas extras, dedicándose la empresa demandada a la actividad de [ACTIVIDAD DE LA EMPRESA].

SEGUNDO.– Que el/la demandante fue despedido/a de dicha empresa, declarándose improcedente el despido por sentencia de fecha [FECHA] dictada por la Sección de lo Social del Tribunal de Instancia de [SEDE], plaza n.º [Nº], en el procedimiento n.º [Nº DE PROCEDIMIENTO], y tras haberse llevado a efecto todos los trámites oportunos, incluida la ejecución de sentencia, solicitó del Servicio Público de Empleo, en tiempo y forma, las prestaciones correspondientes.

TERCERO.– Que durante los últimos cinco años ha cotizado de forma ininterrumpida, incluida la contingencia por desempleo, en la empresa codemandada.

CUARTO.– Que la base reguladora de los 6 meses anteriores a la situación de desempleo asciende a la cantidad de [IMPORTE] euros, y proporcionalmente corresponde una cantidad diaria de [IMPORTE] euros.

QUINTO.– Que mediante resolución del Servicio Público de Empleo de fecha [FECHA] se me reconoce la prestación económica correspondiente a una base reguladora de [IMPORTE] euros diarios y por un período de [Nº DE MESES] meses. Se acompaña copia de dicha resolución como DOC. Nº [Nº].

SEXTO.– Que no estoy conforme con dicha resolución por cuanto:

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— (Si no está de acuerdo con la cantidad) La base reguladora diaria reconocida por el Servicio Público de Empleo es inferior a la que realmente me corresponde conforme a las cotizaciones efectuadas por la empresa, tal y como se acredita con los recibos de salarios que a esta demanda se adjuntan como DOC. Nº [Nº], siendo la que se tiene que tener en cuenta la base reguladora de [IMPORTE] euros diarios.

— (Si no está de acuerdo con el tiempo de la prestación) Me corresponde cobrar la prestación de desempleo durante un período de [Nº DE MESES] meses, en lugar de los [Nº DE MESES] meses que me reconoce el Servicio Público de Empleo, según queda acreditada la relación laboral en la empresa por un período de cinco años inmediatamente anteriores a la fecha del despido. Se acompaña copia del contrato de trabajo como DOC. Nº [Nº] e informe de vida laboral como DOC. Nº [Nº].

SÉPTIMO.– Que ha agotado la reclamación previa ante el Servicio Público de Empleo, según se acredita en el documento que se adjunta como DOC. Nº [Nº].

FUNDAMENTOS DE DERECHO

I.– Artículos 1, 2 o), 6, 10, 71 a 73 y 140 a 147 de la Ley 36/2011, reguladora de la jurisdicción social, siendo competente el Tribunal de Instancia al que me dirijo en razón de la materia y territorio.

II.– Artículo 269 del Real Decreto Legislativo 8/2015, de 30 de octubre, por el que se aprueba el texto refundido de la Ley General de la Seguridad Social.

III.– Artículos 3 y 4 del Real Decreto 625/1985, de 2 de abril, que desarrolla la Ley de protección por desempleo.

En virtud de cuanto antecede es por lo que,

SUPLICO AL TRIBUNAL que, teniendo por presentado este escrito con sus copias y documentos que se adjuntan, se digne admitirlo, tenga por formulada demanda de impugnación de la prestación de desempleo contra el Servicio Público de Empleo y contra la empresa [DENOMINACIÓN SOCIAL], se proceda a convocar a las partes para los actos de conciliación y juicio, en la debida forma, por el que, seguidos todos sus trámites, se dicte en su día sentencia estimando íntegramente la presente demanda, por la que se condene a los demandados, en su respectivo carácter, a reconocer mi derecho al percibo de prestación por desempleo en la cantidad diaria de [IMPORTE] euros, y por un periodo de [Nº DE MESES] meses.

OTROSÍ DIGO: Que al acto de juicio compareceré asistido de Letrado/a para que me defienda, de conformidad con el artículo 21.2 de la Ley reguladora de la jurisdicción social, designando el domicilio profesional del/de la Letrado/a D./Dña. [NOMBRE Y APELLIDOS DEL LETRADO/A] en [LOCALIDAD], a efectos de notificaciones y demás diligencias.

SUPLICO AL TRIBUNAL: Tenga por hecha tal manifestación a los efectos oportunos.

SEGUNDO OTROSÍ DIGO: Que interesa al derecho de esta parte, y sin perjuicio de ampliación en el momento procesal oportuno, los siguientes MEDIOS DE PRUEBA:

— INTERROGATORIO del representante legal de la empresa demandada, que deberá ser citado en el domicilio indicado.

— DOCUMENTAL, consistente en que se requiera a la empresa demandada para que aporte a juicio los siguientes documentos:

1) Parte de alta y baja en la Seguridad Social.

2) Nóminas acreditativas de los salarios percibidos.

3) Boletines de cotización a la Seguridad Social.

— DOCUMENTAL, consistente en que se requiera al Servicio Público de Empleo para que aporte el expediente administrativo correspondiente.

SUPLICO AL TRIBUNAL tenga por hecha tal manifestación a los efectos oportunos, admita y declare pertinentes las pruebas que se dejan propuestas, y acuerde cuanto sea preciso para llevarlas a efecto.

Es de Justicia que pide en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del demandante: [NOMBRE Y APELLIDOS]

Firma del Letrado/a: [NOMBRE Y APELLIDOS DEL LETRADO/A]
