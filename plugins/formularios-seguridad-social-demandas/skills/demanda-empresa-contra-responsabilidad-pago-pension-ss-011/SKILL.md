---
name: demanda-empresa-contra-responsabilidad-pago-pension-ss-011
description: "Demanda de la empresa contra la responsabilidad de pago de la pensión por contrato de relevo. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de la empresa contra la responsabilidad de pago de la pensión por contrato de relevo

> Formulario **SS-011** del plugin **Seguridad Social: demandas y recursos ante lo social** (`formularios-seguridad-social-demandas`) · Seguridad Social › Demandas y escritos ante la jurisdicción social · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de la empresa contra la responsabilidad de pago de la pensión por contrato de relevo» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de la empresa contra la responsabilidad de pago de la pensión por contrato de relevo” para mi caso». También puedes invocarla directamente con `/formularios-seguridad-social-demandas:demanda-empresa-contra-responsabilidad-pago-pension-ss-011`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-seguridad-social-demandas:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Seguridad Social: demandas y recursos ante lo social) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (15 veces)
- [ ] NOMBRE Y APELLIDOS (8 veces)
- [ ] LOCALIDAD (4 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] Nº DE DOCUMENTO (2 veces)
- [ ] SEDE

## Normas que cita el formulario

- art. 12.6 ET
- art. 215.2.e LGSS
- art. 215.2 LGSS
- art. 9.5 LOPJ
- art. 2.o Ley 36/2011
- art. 71 Ley 36/2011
- art. 215 LGSS

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

Con arreglo al art. 12.6 ET, en supuestos de jubilación parcial anticipada la empresa debe concertar un contrato de relevo indefinido y a tiempo completo, con un trabajador desempleado o con contrato de duración determinada en la empresa; y conforme al art. 215.2.e LGSS, debe mantener dicho contrato al menos hasta dos años después de la jubilación plena del trabajador relevado, so pena de responsabilidad en el reintegro de la pensión parcial si incumple tal obligación.

La presente demanda tiene por objeto la impugnación de la resolución del INSS que declara a la empresa responsable del reintegro de la pensión de jubilación parcial de un trabajador, por supuestas irregularidades en el contrato de relevo celebrado.

A LA SECCIÓN DE LO SOCIAL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS], Procurador/a de los Tribunales, en representación de sociedad [DENOMINACIÓN SOCIAL], según acredito mediante copia digitalizada de poder que acompaño, y bajo la dirección letrada de D./Dña. [NOMBRE Y APELLIDOS], Abogado/a del Iltre. Colegio de la Abogacía de [LOCALIDAD], ante el Tribunal de Instancia comparezco y, como mejor proceda en Derecho,

DIGO:

Que, por medio del presente escrito, interpongo en tiempo y forma legal, DEMANDA EN IMPUGNACIÓN DE LA RESOLUCIÓN ADMINISTRATIVA DE FECHA [FECHA], la cual declara la responsabilidad de la empresa que represento en el pago de la pensión de jubilación parcial, la cual dirijo contra el INSTITUTO NACIONAL DE LA SEGURIDAD SOCIAL, con domicilio en [LOCALIDAD], y contra la TESORERÍA GENERAL DE LA SEGURIDAD SOCIAL, con domicilio en [LOCALIDAD], la cual deberá tramitarse por la modalidad procesal de impugnación de actos administrativos en materia laboral y de Seguridad Social, a fin de que se anule dicha resolución en los términos que en el suplico de esta demanda se dirán y todo ello sobre la base de los siguientes:

HECHOS

PRIMERO.- La resolución administrativa impugnada declara la responsabilidad de la empresa que represento con motivo de la contratación de D./Dña. [NOMBRE Y APELLIDOS] con quien la empresa formalizó en fecha [FECHA] un contrato de relevo para sustituir a la persona trabajadora D./Dña. [NOMBRE Y APELLIDOS] que, por acceder a la jubilación parcial, había reducido su jornada en un %.

SEGUNDO.- Por resolución del INSS, de fecha [FECHA] se declaró la responsabilidad de la empresa a que represento en el pago de la pensión de jubilación parcial de D./Dña. [NOMBRE Y APELLIDOS] durante el periodo comprendido entre el día [FECHA] y del día [FECHA], por un importe de [IMPORTE] euros (acompaño como documento número [Nº DE DOCUMENTO] copia de la citada resolución).

TERCERO.- La declaración de responsabilidad se funda en que la persona trabajadora relevista D./Dña. [NOMBRE Y APELLIDOS] estuvo de alta en el RETA en el periodo comprendido entre el día [FECHA] y el día [FECHA] No obstante, y tal como consta en el expediente, la persona trabajadora relevista tenía concertado anteriormente un contrato de trabajo temporal con la empresa que represento, de fecha [FECHA], por lo que reunía los requisitos establecidos en el artículo 12.6 y 7 del ET y en el art. 215.2 LGSS para ser sujeto de un contrato de relevo, sin que constituya obstáculo alguno que el relevista figurase de alta en el RETA.

CUARTO.- Disconforme con dicha resolución, y de acuerdo a los hechos expresados, esta parte interpuso reclamación administrativa previa en fecha [FECHA] en la cual exponían, en síntesis, los siguientes motivos de impugnación:

• Que el art. 12.6 y 12.7 del Estatuto de los Trabajadores permiten que el contrato de relevo se celebre con trabajador que tenga concertado con la empresa un contrato de duración determinada, sin exigir exclusividad ni prohibir el desempeño de otras actividades.

• Que el art. 215.2 de la LGSS no añade requisito alguno en cuanto a incompatibilidades del relevista con otras actividades, sino que se centra en la naturaleza (indefinida y a tiempo completo) y duración del contrato de relevo, así como en su mantenimiento hasta, al menos, los dos años posteriores a la jubilación plena del relevado.

QUINTO.- La reclamación previa interpuesta fue desestimada por resolución del INSS de fecha [FECHA], que declara la responsabilidad de la empresa, notificada el día [FECHA], y que ahora se impugna por medio de la presente demanda (acompaño como documentos nº [Nº DE DOCUMENTO] escrito de reclamación previa y copia de la resolución de fecha [FECHA]).

FUNDAMENTOS DE DERECHO

PRIMERO.- En cuanto a los sujetos procesales y procedimiento, este órgano judicial al que se dirige la demanda tiene jurisdicción (art. 9.5 LOPJ) y competencia objetiva, funcional y territorial [arts. 2.o), 6 y 10 Ley 36/2011, de 10 de octubre, reguladora de la jurisdicción social] para conocer del juicio que se suscita, quedando válidamente constituida la relación jurídico-procesal por ostentar las partes legitimación activa y pasiva; por otra parte, la pretensión deducida debe seguirse por los trámites de la modalidad procesal de impugnación de actos administrativos en materia laboral y de Seguridad Social.

SEGUNDO.- El art. 71 de la Ley 36/2011, en cuanto acreditación del cumplimiento del trámite de la reclamación previa ante la entidad demandada.

TERCERO.- El art. 12 del texto refundido de la Ley del Estatuto de los Trabajadores, aprobado por Real Decreto Legislativo 2/2015, que regula el contrato a tiempo parcial y el contrato de relevo. El contrato de relevo se concierta para sustituir la jornada dejada vacante por el trabajador que accede a la jubilación parcial. Puede celebrarse con un trabajador en situación de desempleo o que tuviese concertado con la empresa un contrato de duración determinada. En los supuestos de jubilación parcial anticipada, el contrato de relevo debe ser indefinido y a tiempo completo, y mantenerse al menos hasta los dos años posteriores a la jubilación plena, so pena de responsabilidad empresarial.

CUARTO.- El art. 215 LGSS (Real Decreto Legislativo 8/2015) regula la jubilación parcial. Su apartado 2.e) establece:

- Que, para acceder a la jubilación parcial antes de la edad ordinaria, la empresa debe concertar simultáneamente un contrato de relevo indefinido y a tiempo completo, que se mantendrá al menos durante los dos años posteriores a la extinción de la jubilación parcial.

- Que, si el contrato de relevo se extingue antes de que el jubilado parcial acceda a la jubilación plena y no se celebra un nuevo contrato de relevo “en los mismos términos”, el empresario será responsable del reintegro de la pensión percibida por el pensionista parcial.

Petitum

Por lo expuesto,

SUPLICO AL TRIBUNAL DE INSTANCIA que teniendo por presentado este escrito, con sus copias y documentos adjuntos, se sirva admitirlo, tenga por interpuesta DEMANDA EN IMPUGNACIÓN DE RESOLUCIÓN ADMINISTRATIVA en materia de Seguridad Social contra el INSTITUTO NACIONAL DE LA SEGURIDAD SOCIAL y la TESORERÍA GENERAL DE LA SEGURIDAD SOCIAL, y, previos los trámites legales oportunos, dicte en su día sentencia por la que se declare no conforme a Derecho y se anule la resolución del INSS de fecha de [FECHA] así como la resolución de [FECHA] que desestima la reclamación previa, ambas por las que se declara la responsabilidad de la empresa demandante en el pago de la pensión de jubilación parcial de D./Dña. [NOMBRE Y APELLIDOS] y se declare la inexistencia de responsabilidad empresarial de [DENOMINACIÓN SOCIAL] en el pago o reintegro de la pensión de jubilación parcial de D./Dña. [NOMBRE Y APELLIDOS] dejando sin efecto la obligación de reintegro por importe de [IMPORTE] euros impuesta a la empresa.

OTROSÍ DIGO: Que de conformidad a lo establecido en el art. 21.2 de la Ley reguladora de la jurisdicción social, hago constar que a los actos que se deriven de la presente demanda mi representada asistirá con la representación y defensa que figuran en el encabezamiento.

Por ser de justicia que pido en [LOCALIDAD], en fecha [FECHA].
