---
name: recurso-contencioso-administrativo-frente-actas-ss-038
description: "Recurso contencioso-administrativo frente a actas de la Inspección de Trabajo y Seguridad Social. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Recurso contencioso-administrativo frente a actas de la Inspección de Trabajo y Seguridad Social

> Formulario **SS-038** del plugin **Seguridad Social: reclamaciones previas y recursos administrativos** (`formularios-seguridad-social-tramites`) · Seguridad Social › Solicitudes, reclamaciones y recursos ante la Administración · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Recurso contencioso-administrativo frente a actas de la Inspección de Trabajo y Seguridad Social» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Recurso contencioso-administrativo frente a actas de la Inspección de Trabajo y Seguridad Social” para mi caso». También puedes invocarla directamente con `/formularios-seguridad-social-tramites:recurso-contencioso-administrativo-frente-actas-ss-038`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-seguridad-social-tramites:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Seguridad Social: reclamaciones previas y recursos administrativos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] DENOMINACIÓN SOCIAL (19 veces)
- [ ] FECHA (18 veces)
- [ ] LOCALIDAD (8 veces)
- [ ] NÚMERO (8 veces)
- [ ] IMPORTE (5 veces)
- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] MES (3 veces)
- [ ] Nº (3 veces)
- [ ] COMUNIDAD AUTÓNOMA (2 veces)
- [ ] Nº DE ANEXO (2 veces)
- [ ] Nº DE EXPEDIENTE (2 veces)
- [ ] OTROS DATOS (2 veces)
- [ ] SEDE (2 veces)
- [ ] COLEGIO
- [ ] CONVENIO COLECTIVO APLICABLE
- [ ] DIRECCIÓN
- [ ] DÍA
- [ ] LUGAR DE PRESTACIÓN DE SERVICIOS
- [ ] NIF
- [ ] NOMBRE DEL REPRESENTADO/A
- [ ] Nº DE PROTOCOLO
- [ ] Nº DE RESOLUCIÓN
- [ ] PERIODO
- [ ] PROVINCIA
- [ ] RELACIÓN DE DOCUMENTOS
- [ ] ÓRGANO JUDICIAL

## Normas que cita el formulario

- art. 8.3 Ley 29/1998
- art. 36 Código Civil

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

### Avisos de actualización (2) — se aplican en el texto, nunca se copian en el documento

- Junto a «… CONTENCIOSO-ADMINISTRATIVO DEL TRIBUNAL DE INSTANCIA DE [SEDE] – PLAZA N.º [Nº]»: Denominación legal «De lo Contencioso-Administrativo» (con guion). Fuente: arts. 84.2.h) y 93 LOPJ; LOPJ (LO 6/1985), BOE-A-1985-12666.
- Junto a «… CONTENCIOSO-ADMINISTRATIVO DEL TRIBUNAL DE INSTANCIA DE [SEDE] – PLAZA N.º [Nº]»: Denominación legal «De lo Contencioso-Administrativo» (con guion); la plaza va tras la sede. Fuente: arts. 84.2.h) y 93 LOPJ; LO 1/2025 DA 1.ª y DT 1.ª; LOPJ (LO 6/1985), BOE-A-1985-12666.

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

A LA SECCIÓN DE LO CONTENCIOSO-ADMINISTRATIVO DEL TRIBUNAL DE INSTANCIA DE [SEDE] – PLAZA N.º [Nº]

HECHOS
FUNDAMENTOS DE DERECHO
Firmas

Recurso contencioso-administrativo impugnando liquidación de cuotas a la seguridad social y además un acta de Infracción por los mismos hechos

A LA SECCIÓN DE LO CONTENCIOSO-ADMINISTRATIVO DEL TRIBUNAL DE INSTANCIA DE [SEDE] – PLAZA N.º [Nº]

D./Dña. [NOMBRE Y APELLIDOS], Letrado/a en ejercicio del Ilustre Colegio de [COLEGIO], con domicilio profesional a efectos de citaciones y notificaciones en [DIRECCIÓN], en nombre y representación de [NOMBRE DEL REPRESENTADO/A], con NIF [NIF], según escritura de poder otorgada ante el Notario/a D./Dña. [NOMBRE Y APELLIDOS], y obrante al [Nº DE PROTOCOLO] de su protocolo, ante la Sala de lo Contencioso Administrativo del Tribunal de Instancia plaza nº [NÚMERO] de [LOCALIDAD] comparezco, y como mejor proceda en derecho DIGO:

Que en fecha [FECHA] se notificó a esta parte Diligencia de Ordenación, de fecha [FECHA], por la que se concede un plazo de veinte días para la formalización de la demanda, a lo que presto cumplimiento por medio del presente escrito, en el que con la separación exigida por la Ley Reguladora de la Jurisdicción Contencioso Administrativa consigno los siguientes

HECHOS

PRIMERO.- Que en fecha [FECHA] le fueron notificadas a mi representado/a las coordinadas Acta de Liquidación nº [NÚMERO] y Acta Infracción nº [NÚMERO], ambas de fecha [FECHA], en virtud de las cuales se liquidan cuotas por el periodo descubierto de [IMPORTE] € por las diferencias entre las bases declaradas por los salarios abonados y las que corresponderían por el salario realmente devengado, y se impone una sanción de [IMPORTE] € por la comisión de una falta grave del artículo 22.3 del TRLISOS, aprobado por RD Legislativo 5/2000, de 4 de agosto, proponiéndose una sanción en grado medio al apreciarse como circunstancias agravantes la cantidad defraudada no ingresada, la intencionalidad del sujeto infractor y el número de trabajadores afectados.

Frente a dicha Acta de Infracción se presentan alegaciones, en fecha [FECHA], y tras la emisión de Informe ampliatorio de la Inspectora actuante, esta parte presenta nuevas alegaciones en fecha [FECHA]. Ambos escritos de alegaciones son desestimados y, en consecuencia, confirmada la sanción mediante Resolución del Jefe de la Unidad de Impugnaciones de la Dirección Provincial de [LOCALIDAD] de la Tesorería General de la Seguridad Social, de fecha [FECHA].

Frente a dicha Resolución se presentó recurso de alzada en fecha [FECHA], que ha sido desestimado por la Resolución, fechada [FECHA], de la Dirección Provincial de la Tesorería General de la Seguridad Social de [LOCALIDAD] (Unidad de Impugnaciones), notificada el [FECHA], y frente al que se interpone la presente demanda.

SEGUNDO.- Las presentes actas se levantan por no haber ingresado en la cuantía debida, en la forma y plazos reglamentarios, las cuotas correspondientes a los trabajadores contratados por [DENOMINACIÓN SOCIAL] que han prestado servicios en [LUGAR DE PRESTACIÓN DE SERVICIOS] en el periodo comprendido entre [PERIODO] pues se considera que el salario percibido por dichos trabajadores (a jornal) es inferior al que les correspondería percibir (a destajo) practicándose la correspondiente liquidación de cuotas.

El acta de infracción y la de liquidación sostienen que los trabajadores contratados [DENOMINACIÓN SOCIAL] han percibido un salario menor al que, a criterio de la inspectora actuante, les corresponde. La razón fundamental para determinar esta deuda salarial consiste en la afirmación de que si bien los trabajadores cedidos por [DENOMINACIÓN SOCIAL] tienen establecida una retribución salarial en la modalidad de "a jornal" la verdadera retribución salarial que corresponde a dichos trabajadores debe ser calculada en la modalidad de "a destajo".

TERCERO.- El acta de infracción manifiesta que la imputación del impago del salario debido se fundamenta en los siguientes indicios:

- Que del estudio de la documentación requerida se observa que el registro de trabajo de los trabajadores cedidos presenta diferencias significativas entre las distintas ETT y con el registro de la empresa usuaria.
- La rentabilidad obtenida entre la facturación emitida a [DENOMINACIÓN SOCIAL] y el abono de los salarios a los trabajadores.
- Las declaraciones efectuadas por dos trabajadores de la empresa de que el salario establecido era a destajo.
- Que del análisis de los datos registrados en entradas báscula por [DENOMINACIÓN SOCIAL], en concreto de los datos registrados para el mes de [MES] por las cuadrillas de [DENOMINACIÓN SOCIAL] permiten afirmar a la inspectora actuante que el rendimiento por hora trabajada resulta de imposible.

CUARTO.- La Inspección de Trabajo y Seguridad Social de [PROVINCIA], además de imputar en las presentes actas el no haber ingresado en la cuantía debida las cuotas correspondientes y practicar la correspondiente liquidación, al considerar que el salario percibido por dichos trabajadores (a jornal) es inferior al que les correspondería percibir (a destajo) levantó, por los mismos hechos objeto de las presentes actas, otra Acta Infracción, en concreto la nº [NÚMERO], de fecha [FECHA], en la que además de imputar la cesión ilegal de trabajadores también imputaba el impago de los salarios debidos, de la que las presentes actas son su consecuencia, por defecto en la cotización.

Dicha acta nº [NÚMERO] fue impugnada ante la jurisdicción social, correspondiendo su conocimiento al TSJ [ÓRGANO JUDICIAL], que dictó la sentencia nº [Nº DE RESOLUCIÓN], de [FECHA] revocando el acta íntegramente, al considerar que el salario abonado por [DENOMINACIÓN SOCIAL] a sus trabajadores es correcto.

En concreto, y por lo que respecta al impago del salario debido, la sentencia del TSJ de la [COMUNIDAD AUTÓNOMA] establece:

A estos hechos les son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

JURÍDICO PROCESALES

PRIMERO.- Son competentes las Salas de lo Contencioso-Administrativo de los Tribunales de Instancia de [LOCALIDAD] para conocer de la pretensión deducida en aplicación de lo dispuesto en el artículo 8.3 de la Ley 29/1998, de 13 de Julio, reguladora de la Jurisdicción Contenciosa-Administrativa.

SEGUNDO.- La Ley de la Jurisdicción Contencioso-Administrativa, art. 19.1,a) sobre legitimación activa del demandante y art. 21.1, a) sobre legitimación pasiva de la Administración Pública.

TERCERO.- La Ley de la Jurisdicción Contencioso-Administrativa, art. 18, en relación con el art. 7 de la Ley de Enjuiciamiento Civil, y art. 36 del Código Civil sobre capacidad procesal del demandante.

CUARTO.- La Ley de la Jurisdicción Contencioso-Administrativa, art. 23.2, sobre la preceptiva intervención de Letrado y Procurador.

QUINTO.- La Ley de la Jurisdicción Contencioso-Administrativa, art. 25.1, sobre la admisión del Recurso Contencioso-Administrativo, por deducirse la relación contra un Acto de la Administración Pública.

SEXTO.- La Ley de la Jurisdicción Contencioso-Administrativa, art. 52 y siguientes, en relación con los artículos 45 y 56.1, sobre el contenido de este escrito y documentos que lo acompañan.

JURÍDICO MATERIALES

PRIMERO.- Como se ha señalado anteriormente, en fecha [FECHA] le fueron notificadas a mi representada las coordinadas Acta de Liquidación nº [NÚMERO] y Acta Infracción nº [NÚMERO], ambas de fecha [FECHA], en virtud de las cuales se liquidan cuotas por el periodo descubierto de [IMPORTE] € por las diferencias entre las bases declaradas por los salarios abonados y las que corresponderían por el salario realmente devengado, y se impone una sanción de [IMPORTE] € por la comisión de una falta grave del el artículo 22.3 del TRLISOS, aprobado por Real Decreto Legislativo 5/2000, de 4 de agosto, por no ingresar, en la forma y plazos reglamentarios, las cuotas correspondientes, proponiéndose una sanción en grado medio al apreciarse como circunstancias agravantes la cantidad defraudada no ingresada, la intencionalidad del sujeto infractor y el número de trabajadores afectados.

Dichas actas han sido confirmadas por la Resolución, fechada el [FECHA], de la Dirección Provincial de la Tesorería General de la Seguridad Social de [LOCALIDAD] (Unidad de Impugnaciones), notificada el [FECHA], frente la que se interpone la presente demanda.

Como esta manifestó en el procedimiento administrativo, sin haber obtenido ninguna respuesta, la discrepancia con las Actas levantadas se centra, fundamentalmente, en la determinación del salario que correspondió percibir, y en consecuencia cotizar, a los trabajadores contratados. Las presentes actas se levantan al considerar que el salario percibido por dichos trabajadores (a jornal) es inferior al que les correspondería percibir (a destajo) practicándose la correspondiente liquidación de cuotas, cuando el salario a jornal que percibieron los trabajadores es el que realmente les correspondía percibir, y por lo tanto el abono del salario y las cotizaciones efectuadas por la empresa son las correctas.

SEGUNDO.- Como se ha señalado anteriormente, el acta de infracción manifiesta que la imputación del impago del salario debido se fundamenta en los siguientes indicios:

- Que del estudio de la documentación requerida se observa que el registro de trabajo de los trabajadores cedidos presenta diferencias significativas entre las distintas ETT y con el registro de la empresa usuaria.
- La rentabilidad obtenida entre la facturación emitida a [DENOMINACIÓN SOCIAL] y el abono de los salarios a los trabajadores.
- Las declaraciones efectuadas por dos trabajadores de la empresa de que el salario establecido era a destajo.
- Que del análisis de los datos registrados en entradas báscula por [DENOMINACIÓN SOCIAL], en concreto de los datos registrados para el mes de [MES] por las cuadrillas de [DENOMINACIÓN SOCIAL] permiten afirmar a la inspectora actuante que el rendimiento por hora trabajada resulta de imposible.

Como esta parte manifestó en el procedimiento administrativo sin haber obtenido ninguna respuesta por la resolución recurrida, los hechos reflejados en el acta de infracción no constituyen indicios de que el salario abonado por la empresa a jornal no sea el salario debido.

La primera de las presunciones establecidas en las actas viene referido al registro de trabajo de los trabajadores cedidos, y en concreto se señala que del estudio de la documentación requerida se observa que el registro de trabajo de los trabajadores cedidos presenta diferencias significativas entre las distintas ETT y con el registro de la empresa usuaria.

Al respecto ya señalamos en el procedimiento administrativo, sin obtener ninguna respuesta por la resolución recurrida que esta parte no comparte la deducción realizada por la inspectora actuante. En primer lugar porque [DENOMINACIÓN SOCIAL] ni ha llevado ni puede llevar un control o registro de la actividad realizada por los trabajadores cedidos, razón por la que no se entiende que se imponga una sanción por unos hechos totalmente ajenos a la voluntad o actuación realizada por [DENOMINACIÓN SOCIAL].

En segundo lugar porque, precisamente los hechos acreditan [OTROS DATOS] que no le resulta de aplicación las diferencia significativas imputadas por el acta de infracción, pues en el registro de horas que lleva con sus propios trabajadores se reflejan horas completas o fracciones de media hora, exactamente coincidente con el registro de horas de trabajo que aparecen reflejadas en los registros de trabajo de los trabajadores cedidos por [DENOMINACIÓN SOCIAL]. La alegación realizada por esta parte resulta muy fácil de comprobar, pues simplemente hay que realizar una comparación del registro de horas que [DENOMINACIÓN SOCIAL] lleva con sus propios trabajadores con el registro de horas de trabajo de los trabajadores cedidos por [DENOMINACIÓN SOCIAL], información que refleja las propias actas de infracción y liquidación.

TERCERO.- La resolución recurrida no contiene ninguna respuesta a las alegaciones efectuadas por esta parte en relación a la segunda presunción establecida para fundamentar la infracción imputada, consistente en la afirmación de que es en la vulneración de los derechos salariales de los trabajadores y en la infracotización al sistema de seguridad social donde [DENOMINACIÓN SOCIAL] obtiene su rentabilidad.

En primer lugar no se puede compartir la deducción realizada de que [DENOMINACIÓN SOCIAL] obtiene rentabilidad de sus trabajadores en concepto de salario tanto si la modalidad retributiva fuera a destajo como si fuera a jornal, pues la cantidad abonada por [DENOMINACIÓN SOCIAL] es superior al salario a jornal que corresponde a los trabajadores por lo que la percepción de dicha retribución siempre ha estado garantizada.

A este respecto ya manifestamos en el procedimiento administrativo que no entendíamos cómo la inspectora actuante, en los anexos [Nº DE ANEXO] que se acompañan a las actas, liquida, por el periodo de referencia, y teniendo en cuenta un salario a destajo, un total de [Nº].

Como ya manifestamos el Convenio Colectivo de aplicación es el de [CONVENIO COLECTIVO APLICABLE].

El criterio que sostiene esta parte es compartido por la Sala de lo Social del TSJ [COMUNIDAD AUTÓNOMA].

El criterio que mantiene la administración demandada en ambos supuestos no es solo distinto sino totalmente contrario u opuesto.

CUARTO.- En tercer lugar, señala el Informe de la inspectora actuante que constituye una prueba directa del derecho que tenían los trabajadores a percibir un salario superior al que realmente percibieron las propias declaraciones prestadas por los trabajadores ante la inspectora, en las que dos trabajadores manifiestan que [NOMBRE Y APELLIDOS] les informó de las condiciones retributivas, siendo éstas a destajo hasta que alcanzaran una retribución de [IMPORTE] €.

La resolución hoy recurrida no contiene ninguna respuesta a las alegaciones efectuadas por esta parte respecto al presente indicio, por lo que entendemos que sigue sosteniendo que constituye una prueba directa del derecho que tenían los trabajadores a percibir un salario superior las declaraciones prestadas por dos trabajadores ante la inspectora. En dichas alegaciones esta parte manifestó que aunque según la inspectora los trabajadores no se habían puesto de acuerdo, el contenido de las declaraciones es prácticamente idéntico, palabra por palabra, en las dos declaraciones reflejadas. Para no ponerse de acuerdo llama la atención la absoluta coincidencia.

La inspectora manifiesta, en su informe ampliatorio, que la absoluta coincidencia, palabra por palabra, de las declaraciones, no debe asombrar, pues fue la inspectora quien trascribió el contenido de las declaraciones y tomada la primera, dicho formato sirvió para registrar la siguiente. Respecto a la absoluta coincidencia manifestada por la inspectora esta parte no puede efectuar alegación alguna, pues es la propia inspectora quien se encarga de no reflejar ni las preguntas efectuadas ni las respuestas dadas, redactando ella misma la declaración que supuestamente efectúan los trabajadores.

No obstante, y ante la ausencia de respuesta por parte de la Administración demandada reiteramos que, aunque esta parte no puede confirmar ni desmentir dichas declaraciones, pues no estaba presente en esa supuesta conversación mantenida por el trabajador y [NOMBRE Y APELLIDOS] y, además, en el acta no se identifica [OTROS DATOS].

También resulta destacable, al respecto, que el acta de infracción no considere relevante que, tal y como la misma refleja, ninguno de los trabajadores pretenda resarcimiento ni haya denunciado irregularidad alguna ni ante la Inspección de Trabajo ni ante la jurisdicción social. Si en el contrato de trabajo se ha establecido por ambas partes un salario a jornal y ningún trabajador pretende resarcimiento ni ha denunciado irregularidad alguna por percibir su salario a jornal, jurídicamente no se puede sostener otro salario aplicable que el salario a jornal, pues en caso contrario se estaría vulnerando la autonomía individual, fuente del contrato de trabajo.

Hay que señalar que la presente imputación se sustenta más en conjeturas que en datos incontrovertidos, lo que no es compatible con una actuación sancionadora que, por sus características, exige pruebas de lo aseverado.

QUINTO.-

SEXTO.- En último lugar, y nuevamente ante la ausencia de respuesta de la resolución recurrida volvemos a reiterar las alegaciones efectuadas en el procedimiento administrativo, con carácter subsidiario, tanto para las agravantes aplicadas como para el hecho de que se está sancionando dos veces la misma conducta.

[NOMBRE Y APELLIDOS], un mismo hecho se está considerando como hecho constitutivo de la infracción y como agravante, lo cual es jurídicamente inadmisible.

Incluso entendemos que no han sido apreciadas las atenuantes que concurren en el presente supuesto, pues del Anexo [Nº DE ANEXO] del acta se deprenden numerosos supuestos en que el salario realmente abonado a los trabajadores es superior al que el acta considera como devengado, lo que determinaría la aplicación de la sanción en grado mínimo.

En su virtud,

SUPLICO AL TRIBUNAL, que teniendo por presentado este escrito, con sus copias, los documentos que se acompañan, ordene su unión al recurso Contencioso Administrativo de referencia, y previa la admisión de la presente, tenga por deducida DEMANDA, y, previos los trámites legales oportunos, dicte en su día sentencia por la que, con estimación del Recurso Contencioso-Administrativo por mi instado en la representación que ostento de [DENOMINACIÓN SOCIAL], contra la Resolución, fechada el [DÍA] de [MES], de la Dirección Provincial de la Tesorería General de la Seguridad Social de [LOCALIDAD] (Unidad de Impugnaciones), notificada el [FECHA] y dictada en el expediente nº [Nº DE EXPEDIENTE] incoado por el Acta de Infracción nº [Nº DE EXPEDIENTE] y Acta de Liquidación nº [NÚMERO], en virtud de la cual se desestima el Recurso de Alzada interpuesto por mi representada contra la Resolución del Jefe de la Unidad de Impugnaciones de la Dirección Provincial de [LOCALIDAD] de la Tesorería General de la Seguridad Social de fecha [FECHA], declare la misma no ser conforme a derecho, revocándola totalmente, de conformidad con lo manifestado en el cuerpo del presente escrito, con todo cuanto más proceda en Derecho.

PRIMER OTROSÍ DIGO: Esta parte manifiesta que la cuantía del procedimiento asciende a EUROSCÉNTIMOS (€).

SUPLICO AL TRIBUNAL que tenga por efectuada la determinación de la cuantía del objeto del procedimiento.

SEGUNDO OTROSÍ DIGO: Que esta parte presenta junto con la demanda documentos en los que funda directamente su derecho en concreto, los siguientes documentos:

- [RELACIÓN DE DOCUMENTOS]

SUPLICO AL TRIBUNAL, que admita el recibimiento a prueba del proceso en los términos interesados.

TERCER OTROSÍ DIGO: Que dado que algunos de los argumentos que mi representada esgrimió en sus escritos de alegaciones y recurso de alzada en el procedimiento administrativo no fueron contestados por la Administración demandada, y dado que tales argumentos se han reproducido en la presente demanda, esta parte cree necesario el trámite de presentación de conclusiones, una vez sea contestada la demanda, al amparo de lo dispuesto en el artículo 62 de la Ley Reguladora de la Jurisdicción Contencioso-Administrativa.

SUPLICO AL TRIBUNAL que admita y acuerde el trámite de presentación de conclusiones.

CUARTO OTROSÍ DIGO: Se devuelve la copia compulsada y única del expediente administrativo.

Es justicia que solicito en [LOCALIDAD].
