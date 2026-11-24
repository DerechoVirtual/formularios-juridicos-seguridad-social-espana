---
name: reclamacion-previa-denegacion-incapacidad-permanente-ss-045
description: "Reclamación previa por denegación de incapacidad permanente total cualificada a un autónomo. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Reclamación previa por denegación de incapacidad permanente total cualificada a un autónomo

> Formulario **SS-045** del plugin **Seguridad Social: reclamaciones previas y recursos administrativos** (`formularios-seguridad-social-tramites`) · Seguridad Social › Solicitudes, reclamaciones y recursos ante la Administración · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Reclamación previa por denegación de incapacidad permanente total cualificada a un autónomo» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Reclamación previa por denegación de incapacidad permanente total cualificada a un autónomo” para mi caso». También puedes invocarla directamente con `/formularios-seguridad-social-tramites:reclamacion-previa-denegacion-incapacidad-permanente-ss-045`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-seguridad-social-tramites:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Seguridad Social: reclamaciones previas y recursos administrativos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (9 veces)
- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] IMPORTE (3 veces)
- [ ] Nº (3 veces)
- [ ] DOLENCIAS
- [ ] DOMICILIO A EFECTOS DE NOTIFICACIONES
- [ ] DÍA
- [ ] LUGAR
- [ ] MES
- [ ] Nº DE PROCEDIMIENTO
- [ ] PROFESIÓN HABITUAL
- [ ] PROVINCIA

## Normas que cita el formulario

- art. 71.1 Ley 36/2011
- art. 4 Real Decreto 1300/1995
- art. 193 Real Decreto Legislativo 8/2015
- art. 197 LGSS

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

A LA DIRECCIÓN PROVINCIAL DEL INSS DE [PROVINCIA]

D./Dña. [NOMBRE Y APELLIDOS] o D./Dña. [ELEGIR: Abogado/a / Graduado/a Social], en representación de D./Dña. [NOMBRE Y APELLIDOS], lo que acredita mediante escritura de poder que se acompaña con Documento Nacional de Identidad núm. [Nº], encuadrado en el Régimen de la Seguridad Social, domiciliado a efectos de notificaciones en [DOMICILIO A EFECTOS DE NOTIFICACIONES]., comparezco en el expediente administrativo núm. [Nº DE PROCEDIMIENTO] y como más procedente sea en Derecho,

Que al amparo del artículo 71.1º de la Ley 36/2011, de 10 de octubre, reguladora de la Jurisdicción Social vengo a interponer reclamación previa contra la resolución dictada por esa Administración de fecha [FECHA] notificada el [FECHA] dentro del plazo legal establecido en su artículo 71.2º sobre la base de los siguientes

HECHOS

I. En fecha [FECHA] presenté solicitud de incapacidad permanente para mi profesión habitual por enfermedad común al amparo de lo establecido en los artículos 4 del Real Decreto 1300/1995, de 21 julio y 4 de la Orden de 18 enero de 1996.

II. En fecha [FECHA] se me notificó por correo certificado resolución dictada por el INSS de fecha [FECHA] denegatoria de la prestación solicitada sobre el hecho que las dolencias objetivadas por el Equipo de Valoración de Incapacidades de esa Dirección Provincial no alcanzan la entidad suficiente para poder ser subsumidas en las previsiones de los artículos 193 y 194 del Real Decreto Legislativo 8/2015, de 30 de octubre, por el que se aprueba el texto refundido de la Ley General de la Seguridad Social (en lo sucesivo LGSS) y artículos 11.1º.b) y 12.2º de la Orden de 15 de abril de 1969.

III. Que la base reguladora que pido para la prestación que pueda declararse asciende a la suma de [IMPORTE] €/mes.

IV. Extinguí la incapacidad temporal en fecha [FECHA]

V. Que mi profesión habitual es la de [PROFESIÓN HABITUAL].

FUNDAMENTOS DE DERECHO

Primero Al amparo de los artículos 27.1.a) y 36 y ss. Del Decreto 2530/1970, de 20 de agosto y artículos 56 y 74 y ss. de la Orden de 24 de septiembre de 1970, y Disposición Transitoria 26ª de la LGSS/2015 que remite al artículo 194 de la misma ley:

«1. La incapacidad permanente, cualquiera que sea su causa determinante, se clasificará con arreglo a los siguientes grados:

a) Incapacidad permanente parcial para la profesión habitual.

b) Incapacidad permanente total para la profesión habitual.

c) Incapacidad permanente absoluta para todo trabajo.

d) Gran invalidez.

2. Se entenderá por profesión habitual, en caso de accidente, sea o no de trabajo, la desempeñada normalmente por el trabajador al tiempo de sufrirlo. En caso de enfermedad común o profesional, aquella a la que el trabajador dedicaba su actividad fundamental durante el período de tiempo, anterior a la iniciación de la incapacidad, que reglamentariamente se determine.

3. Se entenderá por incapacidad permanente parcial para la profesión habitual la que, sin alcanzar el grado de total, ocasione al trabajador una disminución no inferior al 33 por ciento en su rendimiento normal para dicha profesión, sin impedirle la realización de las tareas fundamentales de la misma.

4. Se entenderá por incapacidad permanente total para la profesión habitual la que inhabilite al trabajador para la realización de todas o de las fundamentales tareas de dicha profesión, siempre que pueda dedicarse a otra distinta.

5. Se entenderá por incapacidad permanente absoluta para todo trabajo la que inhabilite por completo al trabajador para toda profesión u oficio.

6. Se entenderá por gran invalidez la situación del trabajador afecto de incapacidad permanente y que, por consecuencia de pérdidas anatómicas o funcionales, necesite la asistencia de otra persona para los actos más esenciales de la vida, tales como vestirse, desplazarse, comer o análogos.»

Segundo Viene acreditado por los informes médicos que aporto que las dolencias diagnosticadas son irreversibles y definitivas imposibilitándome para dedicarme a las tareas más habituales de mi profesión habitual de Toda vez que no se ha valorado por el Equipo de Valoración de Incapacidades las nuevas enfermedades, que justifico mediante la aportación de las pruebas médicas realizadas y que se encuentran documentadas en el informe médico suscrito por los Facultativos D./Dña. [NOMBRE Y APELLIDOS] y D./Dña. [NOMBRE Y APELLIDOS], colegiados/as números [Nº] y [Nº], respectivamente.

Las dolencias no valoradas por el Equipo de Valoración de Incapacidades son las siguientes:

- [DOLENCIAS]

Tercero La base reguladora para el cálculo de la prestación, calculada conforme al artículo 197 de la LGSS asciende a [IMPORTE] € mensuales.

La prestación económica correspondiente a la incapacidad permanente total equivale al 55% de la base reguladora de conformidad con el artículo 6 del Decreto 1646/1972 de 23 de junio, en materia de prestaciones del Régimen General de la Seguridad Social y artículo 12.1º.a) del Decreto 3158/1966, de 23 diciembre, que aprueba el Reglamento General que determina la cuantía de las prestaciones económicas del Régimen General de la Seguridad Social y condiciones para el derecho a las mismas.

Hay que incrementar el porcentaje del 55% con un 20%, dado que el solicitante tiene más de 55 años, todo ello al amparo del artículo 6.2º del Decreto 1646/1972, como queda documentado en el expediente administrativo en relación con el artículo 38 del Decreto 2530/1970 en la redacción dada por el Real Decreto 463/2003, de 25 abril, de reconocimiento del incremento de la pensión de incapacidad permanente total para la profesión habitual para los trabajadores por cuenta propia., artículo 3, toda vez que la edad de 55 años se ha cumplido con posterioridad a 1 de enero de 2003, como exige la Disposición Adicional Única del Real Decreto 463/2003.

Cuarto Que la fecha del hecho causante es el [FECHA] fecha de extinción de la prestación de incapacidad temporal al amparo del artículo 76 de la Orden de 24 de septiembre de 1970, en su redacción dada por la Orden ESS/1310/2017, de 28 de diciembre.

Quinto Los efectos económicos serán a partir del día primero del mes siguiente al de la fecha en que se entiendan causadas las mismas [FECHA], fecha [FECHA] por aplicación del artículo 61 de la Orden de 24 de septiembre de 1970, en su redacción dada por la Orden ESS/1310/2017, de 28 de diciembre.

Por todo lo cual,

SOLICITO A ESA DIRECCIÓN PROVINCIAL que con la presentación de este escrito y documentación que se adjunta, lo admita, tenga por formulada en tiempo y forma reclamación previa a la vía judicial, y emita nueva resolución por la que se revoque la anterior recurrida y tenga a bien declarar la incapacidad permanente total cualificada que demando, con derecho a percibir una pensión con-sistente en el 75% de la base reguladora de [IMPORTE] €/mes, con fecha del hecho causante y efectos económicos desde

Es justicia que pido en [LUGAR], a [DÍA] de [MES]

Firmado:

D./Dña. [NOMBRE Y APELLIDOS]
