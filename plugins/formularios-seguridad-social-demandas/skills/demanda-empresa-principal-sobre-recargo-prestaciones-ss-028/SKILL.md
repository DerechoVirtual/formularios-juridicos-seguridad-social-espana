---
name: demanda-empresa-principal-sobre-recargo-prestaciones-ss-028
description: "Demanda de la empresa principal sobre recargo de prestaciones por falta de medidas de seguridad. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de la empresa principal sobre recargo de prestaciones por falta de medidas de seguridad

> Formulario **SS-028** del plugin **Seguridad Social: demandas y recursos ante lo social** (`formularios-seguridad-social-demandas`) · Seguridad Social › Demandas y escritos ante la jurisdicción social · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de la empresa principal sobre recargo de prestaciones por falta de medidas de seguridad» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de la empresa principal sobre recargo de prestaciones por falta de medidas de seguridad” para mi caso». También puedes invocarla directamente con `/formularios-seguridad-social-demandas:demanda-empresa-principal-sobre-recargo-prestaciones-ss-028`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-seguridad-social-demandas:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Seguridad Social: demandas y recursos ante lo social) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] DENOMINACIÓN SOCIAL (25 veces)
- [ ] NÚMERO (11 veces)
- [ ] FECHA (10 veces)
- [ ] LOCALIDAD (6 veces)
- [ ] DESCRIPCIÓN DEL BIEN (4 veces)
- [ ] PROHIBICIÓN ESTABLECIDA (3 veces)
- [ ] DESCRIBIR (2 veces)
- [ ] EXPONER LOS HECHOS (2 veces)
- [ ] NIF (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] ACTIVIDAD
- [ ] CATEGORÍA PROFESIONAL
- [ ] CONDUCTA DE LA PERSONA TRABAJADORA
- [ ] DESCRIPCIÓN DE LA OPERACIÓN
- [ ] DOMICILIO A EFECTOS DE NOTIFICACIONES
- [ ] LUGAR
- [ ] MOTIVO
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] Nº
- [ ] OBJETO DE LA PERICIAL
- [ ] OBJETO DEL CONTRATO
- [ ] OBLIGACIÓN ESTABLECIDA
- [ ] RIESGOS EVALUADOS
- [ ] RIESGOS IDENTIFICADOS
- [ ] SEDE
- [ ] TAREAS REALIZADAS

## Normas que cita el formulario

- art. 24 Ley 31/1995
- art. 24 LP
- art. 164 LGSS
- art. 2.o Ley 36/2011
- art. 71 LRJS
- art. 71.6 LRJS
- art. 42 ET
- art. 15.4 LP

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

El art. 164 del Texto Refundido de la Ley General de la Seguridad Social dispone que todas las prestaciones económicas que tengan su causa en accidente de trabajo o enfermedad profesional se incrementarán, según la gravedad de la falta, entre un 30 y un 50%, cuando la lesión se produzca en instalaciones o lugares de trabajo que carezcan de medios de protección reglamentarios, los tengan inutilizados o cuando no se hayan observado las medidas generales o particulares de seguridad y salud en el trabajo o de adecuación personal al trabajo, recayendo la responsabilidad del pago del recargo “directamente sobre el empresario infractor”, siendo inasegurable, y compatible con cualesquiera otras responsabilidades, incluso penal.

Es preceptivo agotar la vía administrativa previa

A LA SECCIÓN DE LO SOCIAL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS] Letrado/a, en nombre y representación de la mercantil [NOMBRE DEL REPRESENTADO/A], con NIF [NIF], y domicilio a efectos de notificaciones en [DOMICILIO A EFECTOS DE NOTIFICACIONES], según acredito mediante escritura de poder que acompaño como documento n.º 1, ante el Tribunal comparezco y, como mejor proceda en Derecho, DIGO:

Que, por medio del presente escrito, formulo DEMANDA EN MATERIA DE SEGURIDAD SOCIAL (RECARGO DE PRESTACIONES) contra:

1. INSTITUTO NACIONAL DE LA SEGURIDAD SOCIAL (INSS), Dirección Provincial de [LOCALIDAD], con domicilio en [LOCALIDAD];

2. TESORERÍA GENERAL DE LA SEGURIDAD SOCIAL (TGSS), Dirección Provincial de [LOCALIDAD], con domicilio en [LOCALIDAD];

3. La mercantil [DENOMINACIÓN SOCIAL], con NIF [NIF], y domicilio en [LOCALIDAD], en su condición de empleadora de la persona trabajadora accidentada;

todo ello en impugnación de la resolución del INSS que declara la responsabilidad de mi representado/a en un recargo del 30% sobre las prestaciones de Seguridad Social derivadas de accidente de trabajo, con base en los siguientes

HECHOS

PRIMERO.- Mi representado/a [DENOMINACIÓN SOCIAL], es titular del centro de trabajo sito en [LOCALIDAD], donde desarrolla su actividad principal consistente en [DESCRIBIR].

En fecha [FECHA] suscribió con la mercantil [DENOMINACIÓN SOCIAL] contrato de prestación de servicios de [OBJETO DEL CONTRATO] de la planta (doc. n.º [NÚMERO]).

presta dicho servicio con personal propio, encuadrado en su código de cuenta de cotización, bajo su exclusiva dependencia orgánica y funcional, siendo responsable de la evaluación de riesgos específicos de las tareas de mantenimiento, de la formación de sus trabajadores y de la dotación de equipos de trabajo y de protección individual (docs. n.º [NÚMERO]).

SEGUNDO.- El día [FECHA] la persona trabajadora (en adelante, la “persona trabajdora accidentada”), empleada de [DENOMINACIÓN SOCIAL] con categoría de [CATEGORÍA PROFESIONAL], sufrió un accidente mientras realizaba tareas de [TAREAS REALIZADAS] situado en

La operación consistía en [DESCRIPCIÓN DE LA OPERACIÓN].

De acuerdo con la versión de los testigos y la propia persona accidentada, [EXPONER LOS HECHOS].

Mediante resolución de fecha [FECHA], el INSS declaró a la persona trabajadora afectada en situación de IPT derivada de accidente de trabajo, con derecho a la correspondiente pensión, así como diversas prestaciones de incapacidad temporal anteriores (doc. n.º [NÚMERO]).

TERCERO.- Mi representado/a dispone de evaluación de riesgos del centro de trabajo elaborada por su servicio de prevención ajeno, en la que se identifican, entre otros, los riesgos de [RIESGOS IDENTIFICADOS], y se contemplan medidas técnicas de protección colectiva y organizativas (doc. n.º [NÚMERO]).

La empresa tiene implantado un procedimiento de coordinación de actividades empresariales conforme al art. 24 de la Ley 31/1995 de Prevención de Riesgos Laborales, aplicable a todas las empresas concurrentes en su centro, entre ellas [DENOMINACIÓN SOCIAL]. Dicho procedimiento incluye, entre otros extremos el intercambio de evaluaciones de riesgos, reuniones periódicas de coordinación, procedimiento de permisos de trabajo para tareas no rutinarias o de riesgo especial y entrega de normas de seguridad del centro a todas las empresas concurrentes (doc. n.º [NÚMERO]).

La persona trabajadora accidentada asistió a la formación específica impartida por [DENOMINACIÓN SOCIAL] sobre [DESCRIBIR] y uso de EPIs el día [FECHA], figurando su firma en el correspondiente registro de formación (doc. n.º [NÚMERO]), así como en el documento de información de riesgos del centro de trabajo de [DENOMINACIÓN SOCIAL], donde consta la prohibición de [PROHIBICIÓN ESTABLECIDA] y la obligación de [OBLIGACIÓN ESTABLECIDA] (doc. n.º [NÚMERO]).

El/La demandante había verificado en la última inspección periódica del [DESCRIPCIÓN DEL BIEN] el buen estado estructural de [DESCRIPCIÓN DEL BIEN], no existiendo defecto alguno en las mismas. La [DESCRIPCIÓN DEL BIEN] cumplía los requisitos reglamentarios, no produciéndose el accidente por rotura o falta de resistencia de la protección colectiva, sino por el uso inadecuado que hizo de ella el trabajador.

CUARTO.- A raíz del accidente, la Inspección de Trabajo y Seguridad Social levantó Acta de Infracción núm. [Nº] de fecha [FECHA], en la que, con carácter genérico, se imputó a [DENOMINACIÓN SOCIAL] una infracción grave en materia de prevención de riesgos laborales por [MOTIVO], sin que el acta haya adquirido firmeza, al estar recurrida en vía administrativa (doc. n.º [NÚMERO]).

Sobre la base exclusiva de dicha acta, el INSS incoó expediente de recargo de prestaciones y, mediante resolución de fecha [FECHA], declaró la responsabilidad de [DENOMINACIÓN SOCIAL] en la producción del accidente, imponiendo un recargo del % sobre todas las prestaciones económicas derivadas del mismo, con efectos retroactivos (doc. n.º [NÚMERO]).

Frente a dicha resolución, mi representado/a formuló reclamación administrativa previa el [FECHA], alegando, entre otros extremos, la ausencia de infracción de medidas de seguridad imputable a ella, la correcta coordinación de actividades y la falta de nexo causal entre la organización preventiva de [DENOMINACIÓN SOCIAL] y el accidente, que obedece a una conducta personal y gravemente imprudente de la persona trabajadora. La reclamación fue desestimada por silencio administrativo, al no haberse dictado resolución expresa en el plazo de 45 días (doc. n.º [NÚMERO]).

La presente demanda se formula dentro del plazo de 30 días desde la desestimación presunta de la reclamación previa.

QUINTO.- De lo expuesto y de la documental que se aportará se desprende que mi representado/a dispone de evaluación de riesgos y medidas colectivas de protección en la zona del accidente, adecuadas a la normativa vigente, ha implantado un sistema de coordinación de actividades empresariales conforme al art. 24 LPRL y exigido a [DENOMINACIÓN SOCIAL] el cumplimiento de sus obligaciones preventivas, ha puesto en conocimiento de [DENOMINACIÓN SOCIAL] y de sus personas trabajadoras las normas de seguridad del centro, incluyendo la prohibición expresa de [PROHIBICIÓN ESTABLECIDA] y no presenta defectos estructurales ni ausencia de medios de protección en la zona del siniestro.

El accidente se produce exclusivamente por la decisión de la persona trabajadora accidentada de [CONDUCTA DE LA PERSONA TRABAJADORA], contraviniendo las instrucciones de [DENOMINACIÓN SOCIAL] y de su propia empleadora [DENOMINACIÓN SOCIAL], y prescindiendo de los equipos auxiliares y EPIs disponibles.

En consecuencia, no concurre infracción de medidas de seguridad imputable a mi representado/a en los términos del art. 164 LGSS, ni nexo causal entre una conducta omisiva de la empresa y el resultado lesivo. La calificación de “empresario infractor” que hace la resolución del INSS carece de base fáctica y jurídica.

FUNDAMENTOS DE DERECHO

I. Jurisdicción y competencia objetiva.

Compete al orden jurisdiccional social conocer de la presente demanda en virtud de lo dispuesto en el art. 2.o) de la Ley 36/2011, de 10 de octubre, reguladora de la jurisdicción social (LRJS), que atribuye a este orden el conocimiento de los procesos en materia de prestaciones de Seguridad Social y sobre imputación de responsabilidades a empresarios respecto de dichas prestaciones en los casos legalmente establecidos.

II. Legitimación activa y pasiva

Mi representado/a [DENOMINACIÓN SOCIAL], ostenta legitimación activa en cuanto sujeto directamente afectado por la resolución del INSS que le declara responsable del recargo de prestaciones.

Son legitimados pasivos el INSS, en cuanto entidad gestora que dictó la resolución impugnada; la TGSS, como entidad gestora de la recaudación y garante de la integridad del sistema y [DENOMINACIÓN SOCIAL], como empleadora de la persona trabajadora accidentadaI, interesada por la eventual repercusión indirecta del recargo.

III. Reclamación previa y plazo.

Se ha cumplido el requisito de reclamación administrativa previa previsto en el art. 71 LRJS, habiendo sido interpuesta frente a la resolución del INSS y desestimada por silencio administrativo; se acompaña copia como documento n.º [NÚMERO].

La presente demanda se interpone dentro del plazo de 30 días siguientes a la desestimación presunta, de conformidad con el art. 71.6 LRJS.

IV. Requisitos formales de la demanda.

La demanda reúne los requisitos del art. 80 y ss. LRJS en cuanto a contenido, identificación de partes, hechos y fundamentos.

Fondo del asunto

Primero.– El art. 164 del Texto Refundido de la Ley General de la Seguridad Social dispone que todas las prestaciones económicas que tengan su causa en accidente de trabajo o enfermedad profesional se incrementarán, según la gravedad de la falta, entre un 30 y un 50%, cuando la lesión se produzca en instalaciones o lugares de trabajo que carezcan de medios de protección reglamentarios, los tengan inutilizados o cuando no se hayan observado las medidas generales o particulares de seguridad y salud en el trabajo o de adecuación personal al trabajo, recayendo la responsabilidad del pago del recargo “directamente sobre el empresario infractor”, siendo inasegurable, y compatible con cualesquiera otras responsabilidades, incluso penal.

La jurisprudencia social ha configurado esta responsabilidad como autónoma, específica y cerrada, precisando la concurrencia de tres requisitos: a) incumplimiento de medidas de seguridad; b) daño derivado de AT/EP que genera prestaciones; c) nexo causal entre la infracción y el resultado.

A su vez, se ha reiterado que el recargo sólo recae sobre el “empresario infractor”, sin que quepa extenderlo mecánicamente a terceros por aplicación analógica del art. 42 ET u otros regímenes, salvo que se acredite una infracción preventiva propia e imputable a cada empresa concurrente, generándose entonces una responsabilidad solidaria, pero siempre por infracción propia, no por mera titularidad del centro de trabajo.

En el presente caso el empresario de la persona trabajadora accidentada es [DENOMINACIÓN SOCIAL], que ejercía sobre él el poder de dirección, organización y control. Mi representado/a es empresa principal y titular del centro, pero no empleadora de la persona trabajadora accidentada.

Para calificar a [DENOMINACIÓN SOCIAL] como “empresario infractor” y hacerle soportar un recargo de prestaciones, hubiera sido necesario acreditar una infracción cierta, seria y concreta de sus obligaciones propias de seguridad en el centro, y que tal infracción hubiese contribuido causalmente al accidente, extremos que, como se verá, no concurren.

Segundo.– La Ley 31/1995 de Prevención de Riesgos Laborales, en su art. 14, impone al empresario el deber de garantizar la seguridad y salud de sus personas trabajadoras, articulando su actuación mediante la evaluación de riesgos, la planificación de la actividad preventiva, información y formación, etc.

En supuestos de concurrencia de empresas en un mismo centro de trabajo —como es el presente— el art. 24 LPRL establece deberes específicos de cooperación y coordinación, de forma que la empresa titular del centro debe informar a las concurrentes de los riesgos propios del centro, las empresas concurrentes deben intercambiar información sobre los riesgos derivados de su actividad, deben establecerse medios de coordinación adecuados a la naturaleza de las actividades concurrentes.

Como se ha expuesto en los hechos, [DENOMINACIÓN SOCIAL] ha evaluado los riesgos del centro, incluyendo [RIESGOS EVALUADOS], adoptando medidas de protección colectiva reglamentarias. Ha implantado un procedimiento de coordinación de actividades empresariales y exigido a [DENOMINACIÓN SOCIAL] la remisión de su evaluación de riesgos específica y la aplicación de medidas adecuadas. Asimismo, ha informado a las personas trabajadoras de empresas concurrentes, incluyendo al accidentado, de las normas de seguridad del centro y de la prohibición de [PROHIBICIÓN ESTABLECIDA]. Y, por último, ha certificado periódicamente el buen estado de [DESCRIPCIÓN DEL BIEN] de la zona del siniestro, sin que se haya acreditado defecto alguno estructural.

Por su parte, la empleadora [DENOMINACIÓN SOCIAL] elaboró su evaluación de riesgos específica de trabajos [ACTIVIDAD], formó a la persona trabajadora y le dotó de equipos de trabajo y EPIs adecuados), como demuestran los documentos aportados.

En consecuencia, no puede imputarse a mi representado/a infracción alguna de las obligaciones preventivas que le correspondían ni de sus deberes de coordinación. La resolución del INSS se limita a reproducir el acta de la ITSS, sin individualizar infracciones concretas ni razonar cómo la organización preventiva de [DENOMINACIÓN SOCIAL] ha contribuido al accidente, incurriendo en falta de motivación.

Tercero.– La procedencia del recargo exige, además de la infracción preventiva, la existencia de un nexo causal entre la conducta del empresario y el accidente, de forma que el incumplimiento de las medidas de seguridad resulte revelador de la peligrosidad que se concreta en el daño.

La jurisprudencia social ha reiterado que la imprudencia profesional o no temeraria de la persona trabajadora no rompe el nexo causal, debiendo el empresario prever “las distracciones o imprudencias no temerarias” (art. 15.4 LPRL). Sin embargo, una imprudencia temeraria cualificada o la conducta gravemente negligente de un tercero, totalmente contraria a las normas elementales de prudencia e imprevisible para el empresario, pueden llegar a romper el nexo causal y excluir el recargo, siempre que el empresario haya cumplido razonablemente sus deberes de prevención.

En el presente caso [EXPONER LOS HECHOS]

Por tanto, no concurre el presupuesto típico del art. 164 LGSS (“empresario infractor”), ni el nexo causal necesario entre la supuesta infracción y el daño, lo que hace improcedente el recargo.

Cuarto.– La resolución del INSS se limita a transcribir parcialmente el acta de la ITSS, declarar que “existen incumplimientos de las medidas de prevención imputables a la empresa titular del centro de trabajo” sin especificar cuáles ni en qué extremos se considera incumplida la normativa y fijar, sin mayor razonamiento, un recargo del %.

Ello vulnera las exigencias de motivación que, de forma general, impone la normativa de procedimiento administrativo y, en el ámbito específico de Seguridad Social, su normativa de desarrollo, así como el derecho a la tutela judicial efectiva y a no padecer indefensión, dado que dificulta en extremo el ejercicio del derecho de defensa al desconocerse cuáles son las medidas concretas supuestamente incumplidas.

La ausencia de motivación suficiente en una resolución de carácter sancionador material, como es la que impone recargo de prestaciones, determina su nulidad o, cuando menos, su anulabilidad, máxime cuando afecta a derechos patrimoniales de la empresa con carácter indefinido.

Por lo expuesto,

SUPLICO AL TRIBUNAL, que teniendo por presentado este escrito, junto con los documentos que se acompañan, se sirva admitirlo, tenga por FORMULADA DEMANDA EN MATERIA DE SEGURIDAD SOCIAL (RECARGO DE PRESTACIONES) contra el INSTITUTO NACIONAL DE LA SEGURIDAD SOCIAL, la TESORERÍA GENERAL DE LA SEGURIDAD SOCIAL y [DENOMINACIÓN SOCIAL], y la empresa [DENOMINACIÓN SOCIAL], y, previos los trámites legales oportunos, dicte en su día sentencia por la que se declare no ajustada a Derecho la resolución del INSS de fecha [FECHA], así como la desestimación presunta de la reclamación previa, dejándolas sin efecto, se declare que no existe infracción de medidas de seguridad imputable a [DENOMINACIÓN SOCIAL] en relación con el accidente sufrido por [NOMBRE Y APELLIDOS] el día [FECHA] y que, en consecuencia, no procede imponer a mi representadoa recargo alguno sobre las prestaciones de Seguridad Social derivadas del referido accidente.

PRIMER OTROSÍ DIGO: Que esta parte comparecerá al acto del juicio asistida de Letrado, señalándose como domicilio de notificaciones el indicado en el encabezamiento.

SEGUNDO OTROSÍ DIGO: Que esta parte interesa el recibimiento del pleito a prueba, proponiendo expresamente desde este momento los siguientes medios:

[OPCIONAL — incluir si procede]

DOCUMENTAL: consistentes en los documentos aportados con la demanda y los que en su momento se aportarán.

[OPCIONAL — incluir si procede]

TESTIFICAL:.

[OPCIONAL — incluir si procede]

PERICIAL: constiente en [OBJETO DE LA PERICIAL]

TERCER OTROSÍ DIGO: que interesa al derecho de esta parte que se oficie al INSS con el fin de que aporta a los autos el expediente administrativo.

En su virtud,

SUPLICO AL TRIBUNAL, que tenga por hechas las anteriores manifestaciones, por solicitada la práctica de la prueba propuesta, acordando lo necesario para su realización en el acto del juicio, con lo demás que proceda en Derecho.

Por ser de Justicia que se pide en [LUGAR], a [FECHA].
