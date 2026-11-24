---
name: demanda-reconocimiento-incapacidad-permanente-parcial-ss-021
description: "Demanda de reconocimiento de incapacidad permanente parcial. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de reconocimiento de incapacidad permanente parcial

> Formulario **SS-021** del plugin **Seguridad Social: demandas y recursos ante lo social** (`formularios-seguridad-social-demandas`) · Seguridad Social › Demandas y escritos ante la jurisdicción social · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de reconocimiento de incapacidad permanente parcial» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de reconocimiento de incapacidad permanente parcial” para mi caso». También puedes invocarla directamente con `/formularios-seguridad-social-demandas:demanda-reconocimiento-incapacidad-permanente-parcial-ss-021`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-seguridad-social-demandas:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Seguridad Social: demandas y recursos ante lo social) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (7 veces)
- [ ] DENOMINACIÓN SOCIAL (5 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] IMPORTE (4 veces)
- [ ] PROFESIÓN HABITUAL (4 veces)
- [ ] NÚMERO (3 veces)
- [ ] DIRECCIÓN (2 veces)
- [ ] Nº (2 veces)
- [ ] Nº DE EXPEDIENTE (2 veces)
- [ ] COLEGIO
- [ ] CORREO ELECTRÓNICO
- [ ] DESCRIBIR
- [ ] DNI/NIE
- [ ] DOCUMENTOS A APORTAR
- [ ] DOLENCIAS
- [ ] EXPONER LOS HECHOS
- [ ] FUNCIONES Y TAREAS
- [ ] LUGAR
- [ ] MOTIVO
- [ ] OTROS DATOS
- [ ] SEDE
- [ ] TELÉFONO
- [ ] ÓRGANO

## Normas que cita el formulario

- art. 94.2 LRJS
- art. 78.2 LRJS
- art. 143 LRJS

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

La incapacidad permanente parcial se configura como una situación en la que, tras una lesión o enfermedad, la personal trabajadora sufre una disminución de su capacidad laboral superior al 33% respecto a su profesión habitual, sin que ello le impida realizar las tareas fundamentales de la misma. Su reconocimiento exige la existencia de secuelas crónicas e irreversibles y la valoración conjunta de todas las limitaciones funcionales, debiendo detallarse en la demanda las funciones afectadas para acreditar el grado de menoscabo exigido legalmente. La prestación económica correspondiente a la incapacidad permanente parcial consiste en una cantidad a tanto alzado, equivalente a 24 mensualidades de la base reguladora que sirvió para el cálculo del subsidio de incapacidad temporal de la que se deriva la incapacidad permanente.

La demanda ante el Tribunal de Instancia debe formularse en el plazo de treinta días, a contar desde la fecha en que se notifique la denegación de la reclamación previa o desde el día en que se entienda denegada por silencio administrativo.

Se trata de la modalidad procesal de prestaciones de Seguridad Social (arts. 140 y ss.LRJS).

La demanda debe contener una exposición detallada de las lesiones y secuelas, que deben ser objetivables y previsiblemente definitivas, así como la descripción de las limitaciones funcionales que provocan en la persona trabajadora. No basta con la mera enumeración de dolencias, sino que es necesario concretar cómo afectan a la capacidad de trabajo y al rendimiento en la profesión habitual. No es necesario aportar prueba terminante del porcentaje exacto de disminución del rendimiento, pero sí justificar la existencia de una merma significativa y objetiva, apoyada en informes médicos y periciales.

Este formulario es aplicable tanto al supuesto de enfermedad común como enfermedad profesional y accidente de trabajo.

En el caso de contingencias profesionales habrá que demandar también a la Mutua de Accidentes y a la empresa.


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

D./Dña. [NOMBRE Y APELLIDOS], Letrado/a del Ilustre Colegio de Abogados de [COLEGIO], en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS], con DNI nº [DNI/NIE], según se acredita mediante [ÓRGANO] (apud acta, escritura de poder), con domicilio a efectos de notificaciones en su despacho sito en [LOCALIDAD] de [DIRECCIÓN], teléfono [TELÉFONO] y correo electrónico [CORREO ELECTRÓNICO], ante el Tribunal comparece y como mejor proceda en Derecho DICE:

Que por medio del presente escrito, y en la representación que ostenta formulo demanda de incapacidad permanente en el grado de incapacidad permanente parcial derivada de [ELEGIR: enfermedad común / accidente de trabajo], que deberá tramitarse por el procedimiento establecido en los arts. 140 y siguientes de la Ley Reguladora de la Jurisdicción Social, contra el INSTITUTO NACIONAL DE LA SEGURIDAD SOCIAL, la TESORERÍA GENERAL DE LA SEGURIDAD la Empresa [DENOMINACIÓN SOCIAL], con domicilio en [LOCALIDAD] y la Mutua de Accidentes de Trabajo y Enfermedades Profesionales [DENOMINACIÓN SOCIAL], con domicilio en [LOCALIDAD], en la persona de sus representantes legales

A fin de que sean condenadas en los términos que en el suplico de esta demanda se dirán.

Se funda la presente demanda en los siguientes

HECHOS

Primero.- El/La demandante, de [Nº] años de edad, está afiliado/a al Régimen General de la Seguridad Social con el núm. [NÚMERO], siendo su profesión habitual la de [PROFESIÓN HABITUAL]. El/La actor/a ha prestado servicios en la empresa [DENOMINACIÓN SOCIAL] desde el

Su puesto de trabajo incluye las siguientes funciones y tareas [FUNCIONES Y TAREAS].

Segundo.- Con fecha [FECHA] el actor causó baja médica por Incapacidad Temporal derivada de [ELEGIR: enfermedad común / accidente de trabajo], situación en la que estuvo hasta el día [FECHA].

La empresa [DENOMINACIÓN SOCIAL] tiene concertado el riesgo de accidente de trabajo con la Mutua [DENOMINACIÓN SOCIAL].

Tercero.- El actor presenta el siguiente cuadro clínico [DOLENCIAS].

Se acompañan como DOCS. Nº informes médicos [OTROS DATOS].

Cuarto.- Además, del informe pericial que se acompaña a este escrito como DOC. Nº [NÚMERO] se desprende sin género de dudas que el actor se encuentra incapacitado/a de manera permanente y parcial para su profesión habitual de [PROFESIÓN HABITUAL]. Estas dolencias irreversibles y carentes de tratamiento médico eficaz le ocasionan una disminución superior al 33 por 100 en el rendimiento normal para su profesión, sin que le impidan la realización de las tareas fundamentales de la misma.

Quinto.- La base reguladora de la prestación que se solicita asciende a [IMPORTE] euros y, por tanto, la cantidad a tanto alzado que le corresponde es de [IMPORTE] euros, como consecuencia de tener que percibir veinticuatro mensualidades de la base reguladora.

Sexto.- Que con fecha [FECHA], y tras haber agotado la duración máxima de 365 días de IT y habiéndose prorrogado dicha situación, se inició un expediente de incapacidad permanente total en el grado de parcial (nº [Nº] de expediente [Nº DE EXPEDIENTE]), incapacidad que fue denegada por Resolución del INSS de fecha [FECHA], por no alcanzar las lesiones que padece un grado suficiente de disminución de su capacidad laboral para ser constitutivas de una incapacidad permanente en ningún grado.

Se aporta como DOC. Nº [NÚMERO] copia de dicha Resolución.

Séptimo.- Que con fecha [FECHA] mi mandante presentó reclamación previa ante la Dirección Provincial del INSS por no estar de acuerdo con dicha resolución, que ha sido desestimada por Resolución de fecha [FECHA], Expediente nº [Nº DE EXPEDIENTE] la cual no ha sido resuelta de forma expresa habiendo transcurrido 45 días desde la interposición de la reclamación previa

Se aportan como DOCS. Nº copia de la reclamación previa y de dicha Resolución desestimatoria.

Octavo.- Que no encontrando conforme a Derecho la Resolución del INSS, por cuanto mis lesiones, como se acreditará en el momento procesal oportuno, me impiden realizar mi trabajo de [PROFESIÓN HABITUAL] por medio del presente escrito, dentro del plazo legalmente establecido y de conformidad con lo señalado por el artículo 71 de la Ley Reguladora de la Jurisdicción Social, viene a interponer DEMANDA ante la Sección Social del Tribunal de Instancia.

FUNDAMENTOS DE DERECHO

Primero.- Artículo 9 del Decreto 1646/1972, de 23 de junio.

Segundo.- Artículos 193 a 197 y Disposición transitoria vigésima sexta del Real Decreto Legislativo 8/2015, de 30 de octubre, por el que se aprueba el Texto Refundido de la Ley General de la Seguridad Social.

Tercero.- Artículos 2, 71 a 73, 80, 140 y siguientes de la Ley 36/2011, de 10 de octubre, reguladora de la Jurisdicción Social:

Cuarto.- Real Decreto 1300/1995, de 21 de julio.

Quinto.- Orden de 18 de enero de 1996 para la aplicación y desarrollo del Real Decreto 1300/1995, de 21 de julio.

Sexto.- La incapacidad permanente atenderá fundamentalmente a las limitaciones funcionales derivadas de los padecimientos del trabajador, en cuanto tales limitaciones determinen la efectiva restricción de la capacidad laboral. Son esas limitaciones funcionales resultantes las que en el caso han de ponerse en relación con los requerimientos de las tareas que constituyen el núcleo de la concreta profesión habitual que se analiza.

No cabe llevar a cabo un análisis aislado de las lesiones que presente un trabajador, sino que las mismas han de proyectarse sobre las tareas habituales que el ejercicio de la profesión habitual comporta (STS 21 de marzo de 2005, rec. 1211/2004)

A efectos del grado parcial la disminución del rendimiento de trabajo puede ser cuantitativa o cualitativa. La jurisprudencia (entre otras, STSJ Asturias 1/2024, de 9 de enero) tiene dicho por ello y con apoyo en inveterada jurisprudencia que, dada la dificultad -cuando no imposibilidad- que en la mayoría de los casos entraña el determinar el porcentaje exacto o siquiera por aproximación de la disminución en el rendimiento que pueden determinar en un trabajador unas secuelas, se viene admitiendo que el grado parcial deviene no solo atendiendo a lo que objetivamente puede rendir el trabajador afectado, sino teniendo en cuenta también la mayor peligrosidad o penalidad que comporta. Como quiera que lo que se viene a indemnizar en la incapacidad permanente parcial para la profesión habitual es la disminución de la capacidad de trabajo y no la mera disminución del rendimiento, se mantiene la tesis de que, aun sin merma del rendimiento, se deba reconocer la misma siempre que para mantener aquel el trabajador tenga que emplear un esfuerzo físico superior que haga que su trabajo le resulte más penoso o peligroso ( Sentencias de la Sala de lo Social del Tribunal Supremo de 29 enero 1987 y 30 junio 1987).

En el caso concreto que nos ocupa [EXPONER LOS HECHOS].

Por lo expuesto,

SUPLICO AL TRIBUNAL que, teniendo por presentada esta demanda, junto con los documentos que se acompañan, se sirva admitirla a trámite, darle el turno que le corresponda, citar a las partes para la celebración del acto del juicio y dictar sentencia por la que se declare que como consecuencia de las dolencias que padece el/la actor/a, se encuentra afecto de una incapacidad derivada de [ELEGIR: enfermedad común / accidente de trabajo], en el grado de incapacidad permanente parcial para su profesión habitual de [PROFESIÓN HABITUAL], condenando a los demandados en su respectiva responsabilidad a que le abonen una pensión a tanto alzado de veinticuatro mensualidades conforme a una base reguladora de [IMPORTE] euros, ascendiendo la cantidad total a percibir a [IMPORTE] euros.

PRIMER OTROSÍ DIGO. Que sin perjuicio de las pruebas que se aporten en su momento, esta parte intenta valerse de las siguientes:

INTERROGATORIO de la persona representante legal de la empresa demandada, previa citación judicial bajo los apercibimientos legales.

DOCUMENTAL PRIVADA, consistente en que se requiera a la empresa demandada para que aporte los siguientes documentos [DOCUMENTOS A APORTAR].

Todos ellos se encuentran en poder de la demandada, por lo que de conformidad con el artículo 94.2 LRJS, procede requerirla para que los aporte al acto del juicio, con apercibimiento de tenerla por confesa en caso contrario.

TESTIFICAL, de las personas que a continuación se relacionan, y que se solicita se las cite al juicio, con los apercibimientos legales pertinentes.

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD].

DOCUMENTAL, TESTIFICAL y PERICIAL: la que esta parte aportará en el acto del juicio.

SEGUNDO OTROSÍ DIGO. Que designo para mi representación y defensa en juicio a D./Dña. [NOMBRE Y APELLIDOS], quien suscribe conmigo esta demanda, con despacho profesional en [LOCALIDAD] de [DIRECCIÓN] domicilio que designo a efectos de notificaciones, a quien confiero poder tan amplio como en Derecho proceda a efectos de representación.

TERCER OTROSÍ DIGO. Que, a tenor del artículo 78.2 LRJS, interesa la PRACTICA ANTICIPADA DE PRUEBA consistente en [DESCRIBIR], cuya realización en el acto de juicio presenta graves dificultades en razón a que [MOTIVO].

CUARTO OTROSÍ DIGO. Que a los efectos legalmente previstos interesa a esta parte que por ese tribunal se requiera a la entidad gestora para que, de conformidad con los artículos 143 a 145 LRJS proceda a remitir el expediente administrativo instruido.

DOCUMENTACIÓN QUE SE ACOMPAÑA

Al presente escrito de demanda se adjunta, como es exigible en el presente caso, la siguiente documentación ya citada:

SUPLICO AL TRIBUNAL que tenga por hechas las anteriores manifestaciones a los efectos procesales oportunos y, en su virtud, se dicte resolución en las que se acceda a las mismas, efectuándose las oportunas diligencias de requerimiento para la práctica de las pruebas solicitadas.

Es justicia pido en [LUGAR], a [FECHA].

Firma: D./Dña. [NOMBRE Y APELLIDOS]
