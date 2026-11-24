---
name: demanda-contra-mutua-extinguirse-subsidio-incapacidad-ss-008
description: "Demanda contra la mutua por extinguirse el subsidio de incapacidad temporal por incomparecencia. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda contra la mutua por extinguirse el subsidio de incapacidad temporal por incomparecencia

> Formulario **SS-008** del plugin **Seguridad Social: demandas y recursos ante lo social** (`formularios-seguridad-social-demandas`) · Seguridad Social › Demandas y escritos ante la jurisdicción social · normativa revisada el 24-11-2026.

## Qué es

Demanda ante el orden social contra la Mutua que ha extinguido el subsidio de incapacidad temporal y dado el alta por incomparecencia del beneficiario a un reconocimiento médico, para que se anule el alta y se declare que continúa la situación de baja; exige reclamación previa.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda contra la mutua por extinguirse el subsidio de incapacidad temporal por incomparecencia» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda contra la mutua por extinguirse el subsidio de incapacidad temporal por incomparecencia” para mi caso». También puedes invocarla directamente con `/formularios-seguridad-social-demandas:demanda-contra-mutua-extinguirse-subsidio-incapacidad-ss-008`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-seguridad-social-demandas:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Seguridad Social: demandas y recursos ante lo social) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (8 veces)
- [ ] DENOMINACIÓN DE LA MUTUA (3 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] RELACIÓN DE DOCUMENTOS (2 veces)
- [ ] AÑO
- [ ] CATEGORÍA / GRUPO PROFESIONAL
- [ ] CENTRO DE TRABAJO
- [ ] CONVENIO COLECTIVO
- [ ] CORREO ELECTRÓNICO
- [ ] DENOMINACIÓN SOCIAL
- [ ] DIAGNÓSTICO
- [ ] DIRECCIÓN DEL DESPACHO
- [ ] DNI/NIE
- [ ] DOMICILIO DE LA MUTUA
- [ ] DÍA
- [ ] ENTIDAD O PERSONA REQUERIDA
- [ ] EXPLICAR EL MOTIVO DE LA INCOMPARECENCIA
- [ ] FECHA DE ANTIGÜEDAD
- [ ] IMPORTE
- [ ] JORNADA
- [ ] MES
- [ ] N.º DE AFILIACIÓN
- [ ] N.º DE DOCUMENTOS
- [ ] N.º DE EXPEDIENTE
- [ ] NOMBRE DEL LETRADO/A
- [ ] NOMBRE Y APELLIDOS
- [ ] SEDE
- [ ] TELÉFONO
- [ ] TIPO DE CONTRATO

## Normas que cita el formulario

- art. 174.1 LGSS
- art. 1104 Código Civil
- art. 1256 Código Civil
- art. 59.4 Ley 30/1992
- art. 42 Real Decreto 1829/1999

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

- Junto a «… que no debe aplicarse en este supuesto litigioso el art. 59.4 de la Ley 30/1992»: La Ley 30/1992 está derogada; hoy rigen la Ley 39/2015 (procedimiento administrativo común) y la Ley 40/2015 (régimen jurídico del sector público). La Ley 39/2015 suprimió la reclamación previa a la vía judicial civil.
- Junto a «…o, en la fecha en la que el trabajador recogió el burofax en la oficina postal».»: las referencias a la Ley 30/1992 y a la LRJAPYPAC dentro de la cita jurisprudencial son históricas (la doctrina se dictó bajo esa ley, hoy sustituida por las Leyes 39/2015 y 40/2015); comprobar el artículo equivalente en la Ley 39/2015 antes de invocarlas, y verificar la vigencia del art. 42 del Real Decreto 1829/1999 y las referencias de las sentencias citadas.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

NOTAS DE USO (suprimir antes de presentar):

La mutua puede extinguir el derecho al subsidio de incapacidad temporal por contingencias comunes cuando exista incomparecencia injustificada del beneficiario a las convocatorias para exámenes y reconocimientos médicos, pues esa causa de extinción está expresamente prevista en el art. 174.1 de la Ley General de la Seguridad Social (LGSS). Además, el art. 82.4.d) LGSS atribuye a las mutuas la facultad de realizar actos de control y seguimiento desde el mismo día de la baja médica y dispone que la incomparecencia injustificada a las citaciones para examen o reconocimiento médico será causa de extinción del derecho.

La demanda contra la mutua por extinción de la prestación de incapacidad temporal por incomparecencia debe centrarse en verificar si concurrió realmente una incomparecencia injustificada y, sobre todo, si la mutua respetó íntegramente el procedimiento del art. 9 del Real Decreto 625/2014 y del art. 82.4 LGSS: citación con cuatro días hábiles de antelación, advertencia expresa de consecuencias, suspensión cautelar previa, concesión de diez días hábiles para justificar, valoración de la justificación aportada, acuerdo motivado y notificación eficaz. Si cualquiera de esos requisitos falta, existen fundamentos para solicitar la anulación de la extinción y la reposición del subsidio. La acción exige reclamación previa del art. 71 de la Ley 36/2011, reguladora de la jurisdicción social (LRJS).


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

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI número [DNI/NIE], con domicilio a efectos de notificaciones en el Despacho del Letrado/a [NOMBRE DEL LETRADO/A], del Ilustre Colegio de Abogados de [LOCALIDAD], sito en [DIRECCIÓN DEL DESPACHO], teléfono [TELÉFONO] y correo electrónico [CORREO ELECTRÓNICO], ante ese Tribunal comparezco y como mejor proceda en Derecho

DIGO:

Que por medio del presente escrito formulo DEMANDA POR EXTINCIÓN DE PRESTACIÓN POR INCAPACIDAD TEMPORAL POR INCOMPARECENCIA A RECONOCIMIENTO MÉDICO contra la Mutua [DENOMINACIÓN DE LA MUTUA], con domicilio en [DOMICILIO DE LA MUTUA], en la persona de su representante legal.

Se apoya la presente demanda en los siguientes

HECHOS

PRIMERO.- Que figuro afiliado/a al Régimen General de la Seguridad Social con el número [N.º DE AFILIACIÓN], estando contratado/a por la empresa [DENOMINACIÓN SOCIAL], con las siguientes condiciones laborales:

Antigüedad: [FECHA DE ANTIGÜEDAD]
Tipo de contrato: [TIPO DE CONTRATO]
Jornada: [JORNADA]
Categoría / grupo profesional: [CATEGORÍA / GRUPO PROFESIONAL]
Centro de trabajo: [CENTRO DE TRABAJO]
Salario: [IMPORTE]
Convenio colectivo de aplicación: [CONVENIO COLECTIVO]

SEGUNDO.- Que, debido a un accidente sufrido con fecha [FECHA], me encuentro en situación de incapacidad temporal derivada de [ELEGIR: accidente de trabajo / contingencia común] desde el día [FECHA] y con un diagnóstico de [DIAGNÓSTICO].

He permanecido en esta situación de incapacidad temporal hasta el [FECHA], fecha en que he sido dado/a de alta médica por la Mutua demandada por incomparecencia a la cita médica prevista para ese día.

TERCERO.- Que el motivo por el que no pude acudir a la cita médica está totalmente justificado ya que [EXPLICAR EL MOTIVO DE LA INCOMPARECENCIA].

Se aportan los siguientes documentos justificativos de los anteriores extremos: [RELACIÓN DE DOCUMENTOS].

CUARTO.- Que el alta médica emitida por la Mutua me ha dejado totalmente indefenso/a, ya que no estoy en condiciones para reincorporarme a mi puesto de trabajo y cumplo todos los requisitos legales para estar en situación de baja médica por [ELEGIR: el accidente sufrido en el trabajo / la contingencia que originó la baja].

QUINTO.- No estando conforme con el alta médica, presenté reclamación administrativa previa que ha sido desestimada por la Resolución de la Mutua de fecha [FECHA], expediente n.º [N.º DE EXPEDIENTE], notificada el [FECHA].

Se aportan como documentos n.º [N.º DE DOCUMENTOS] copia de la reclamación previa y de dicha Resolución desestimatoria.

FUNDAMENTOS DE DERECHO

I.- Artículos 1, 2.o), 6, 10 y 140 de la Ley 36/2011, de 10 de octubre, reguladora de la jurisdicción social, siendo competente dicho Tribunal de Instancia en razón de la materia y territorio.

II.- Artículos 169 a 176 del texto refundido de la Ley General de la Seguridad Social, aprobado por Real Decreto Legislativo 8/2015, de 30 de octubre.

III.- Art. 9 del Real Decreto 625/2014, de 18 de julio, por el que se regulan determinados aspectos de la gestión y control de los procesos por incapacidad temporal en los primeros trescientos sesenta y cinco días de su duración.

IV.- Art. 80.2 del Real Decreto 1993/1995, de 7 de diciembre, Reglamento de colaboración de las Mutuas de Accidentes de Trabajo y Enfermedades Profesionales de la Seguridad Social.

V.- FONDO DEL ASUNTO

Según el art. 174.1 LGSS, el derecho al subsidio de incapacidad temporal se extinguirá en los casos de incomparecencia injustificada del beneficiario a cualquiera de las convocatorias para los exámenes y reconocimientos establecidos por los médicos adscritos a las Mutuas de Accidentes de Trabajo y Enfermedades Profesionales de la Seguridad Social. El legislador ha establecido un sistema de control más eficaz de las incapacidades temporales, conforme a las previsiones contenidas en la reforma operada por la Ley 24/1997, en respuesta a la Recomendación 13.ª del Pacto de Toledo. Se trata por tanto de una medida de lucha contra el fraude cuando el beneficiario no acude a la convocatoria sin causa justificada que lo impida.

Por consiguiente, la Mutua está obligada a remitir las notificaciones al beneficiario por los conductos adecuados que aseguren su recepción, y la decisión extintiva del derecho al subsidio ha de tener en cuenta las circunstancias del caso, para determinar si la incomparecencia se hallaba o no justificada.

La Mutua demandada no puede proceder a extinguir directamente la prestación por incomparecencia del beneficiario, sino que viene obligada a emplear la máxima diligencia en el cumplimiento efectivo de un acto de comunicación de tanta trascendencia para el beneficiario; porque si la ley le otorga la facultad de extinguir una prestación cuando concurren determinadas circunstancias, antes de adoptar una medida de tal naturaleza debe cuidar siempre de asegurar, cuando ello sea factible, que la comunicación ha llegado al conocimiento real del asegurado para que éste pueda defender sus derechos y, en su caso, acreditar una causa justificativa de su incomparecencia.

Es totalmente aplicable al caso la doctrina establecida por la Sala Cuarta, de lo Social, del Tribunal Supremo, en su Sentencia n.º 470/2020, de 18 de junio (rec. 3302/2017), que establece:

«Desde la perspectiva jurisprudencial, en STS IV de fecha 9.05.2018, rcud 2840/2016, recogiendo la argumentación de la STS de 12.11.2013, rcud. 2780/2012, la Sala viene a considerar injustificada la incomparecencia de la actora al reconocimiento médico: "Alegar que recogió el burofax pasado el día para el que había sido citada es una mera excusa que no justifica la incomparecencia, al haber probado que concurrían causas justificadoras del retraso. Si las obligaciones, conforme al art. 1104 del Código Civil deben cumplirse con la diligencia de un buen padre de familia y con la que requiere la naturaleza de la obligación, es claro que la demandante no obró con la diligencia debida al tardar veinticinco días en recoger el burofax, porque, si estaba en situación de baja laboral, su principal obligación era curarse cuanto antes y acudir a cuantos reconocimientos médicos fuese citada para controlar la evolución de su patología, razón por la que no obra con la diligencia debida quien tarda más de veinte días en acudir a recoger el burofax que le envía la Mutua que le asiste, controla su enfermedad y paga la prestación económica, pues, aparte que teóricamente no tiene nada que hacer, salvo cumplir con los deberes dichos, resulta que no es lógica tal demora en acudir a recibir una comunicación enviada por y sobre materia que afecta a la situación de baja, pues aceptar la posible validez de ese retraso equivale a dejar a su arbitrio el cumplimiento de ese deber, lo que veda el art. 1256 del Código Civil. Además, su conducta tras recibir el fax no fue tampoco acorde con la buena fe, porque envió escritos a la Mutua en lugar de presentarse en persona a dar explicaciones y a ofrecerse para un reconocimiento médico que su conducta demoró más y dio lugar a que se acordara la extinción de su derecho por causa imputable a su negligente proceder". Adiciona seguidamente la carencia de toda justificación, sea mediante la aportación de algún documento o mediante manifestaciones objetivamente justificativas, de la ausencia a la cita médica, precisando igualmente que no debe aplicarse en este supuesto litigioso el art. 59.4 de la Ley 30/1992 "que obliga a las administraciones públicas a practicar la notificación, que no se pudo practicar de otra manera, por cualquier medio que permita tener constancia de recepción por el interesado o su representante, pues, como antes se ha expuesto, si el interesado no tuvo conocimiento de la comparecencia a que fue requerido por la Mutua se debió a su conducta omisiva, siendo de resaltar, que la constancia en el aviso de que el telegrama notificado de la comparecencia procedía de la Mutua, hacía presumir que su contenido hacía referencia a su situación de incapacidad temporal, cuyo control correspondía, legalmente, a la Mutua aseguradora".

Sin embargo, en el pronunciamiento emitido por la Sala IV en fecha 9.05.2019, rcud 3427/2017, reiteramos el criterio expresado en la STS de 12.01.2017, rcud 3433/2015 y el resuelto por la STS de 12.01.2014, rcud 2433/2015, acerca de la suficiencia o insuficiencia de la doble notificación practicada en el domicilio conocido del beneficiario en relación con la exigencia edictal que contempla el art. 59.5 de la LRJAPYPAC, cuando se tratare de reclamaciones por indebidas de prestación por desempleo. Procede subrayar la siguiente argumentación: se intentó infructuosamente en el domicilio del demandante en dos ocasiones, cumpliendo con el requisito a que hace referencia el artículo 42 del Real Decreto 1829/1999, de 3 de diciembre, por el que se aprueba el Reglamento por el que se regula la prestación de los servicios postales, y que es exigible en supuestos de notificación de resoluciones del SPEE, tal como tiene señalado esta Sala en su sentencia de 22 de julio de 2014 (rcud 2930/2013). Sin embargo, como señala el Ministerio Fiscal en su preceptivo informe, ello no excluye el cumplimiento de las previsiones del ya transcrito apartado 5 del artículo 59 de la LRJAPPAC, norma de jerarquía superior, y que da un paso más al exigir la citación en el Boletín Oficial si falla la domiciliaria, entre otros supuestos, en el caso, como aquí acontece de que "o bien intentada la notificación, no se hubiese podido practicar" ello en aras de una mayor garantía jurídica del afectado por la resolución administrativa máxime, cuando en el presente caso le resulta claramente perjudicial. Esta interpretación se deduce tanto de la doctrina jurisprudencial sentadas en recursos de casación para la unificación de doctrina por la de la Sala de lo Contencioso Administrativo de este Tribunal (sentencias de 20 de enero de 2003 (recurso 275/1998) y 16 de diciembre de 2015 (recurso 1302/2014), como de los fundamentos jurídico décimo y decimosexto de la sentencia de esta Sala de 22 de diciembre de 2015 (recurso casación 75/2015), dictada asimismo en supuesto de exclusión de la prestación por desempleo y reintegro de prestaciones indebidas, supuesto resuelto en sentido desestimatorio, pero en el que, precisamente, estaba acreditada la publicación en el boletín oficial de la resolución administrativa, tras el intento infructuoso de notificación.

Más recientemente, en STS de fecha 29.01.2020, rcud 2578/2017, si bien dictada en materia de despido, afirmamos que se han de aplicar las reglas que rigen el medio de comunicación elegido para notificarlo. Y concretamente en el supuesto que enjuicia, dado que la notificación se habría realizado por burofax, con nitidez precisamos que ha de acudirse a lo establecido en el Real Decreto 1829/1999, de 3 de diciembre, por el que se aprueba el Reglamento por el que se regula la prestación de los servicios postales, en desarrollo de lo establecido en la Ley 24/1998, de 13 de julio, del Servicio Postal Universal y de Liberalización de los Servicios Postales. El artículo 42 establece:

"Supuestos de notificaciones con dos intentos de entrega.

1. Si intentada la notificación en el domicilio del interesado, nadie pudiera hacerse cargo de la misma, se hará constar este extremo en la documentación del empleado del operador postal y, en su caso, en el aviso de recibo que acompañe a la notificación, junto con el día y la hora en que se intentó la misma, intento que se repetirá por una sola vez y en una hora distinta dentro de los tres días siguientes.

2. Si practicado el segundo intento, éste resultase infructuoso por la misma causa consignada en el párrafo anterior o bien por el conocimiento sobrevenido de alguna de las previstas en el artículo siguiente, se consignará dicho extremo en la oportuna documentación del empleado del operador postal y, en su caso, en el aviso de recibo que acompañe a la notificación, junto con el día y la hora en que se realizó el segundo intento.

3. Una vez realizados los dos intentos sin éxito, el operador al que se ha encomendado la prestación del servicio postal universal deberá depositar en lista las notificaciones, durante el plazo máximo de un mes, a cuyo fin se procederá a dejar al destinatario aviso de llegada en el correspondiente casillero domiciliario, debiendo constar en el mismo, además de la dependencia y plazo de permanencia en lista de la notificación, las circunstancias expresadas relativas al segundo intento de entrega. Dicho aviso tendrá carácter ordinario.

4. Si estando en el domicilio la persona que pueda recibir la notificación, se niega a aceptarla y a manifestar por escrito dicha circunstancia con su firma, identificación y fecha en la documentación del empleado del operador postal, se entenderá que no quiere hacerse cargo de la misma, haciéndose constar este extremo en la expresada documentación del empleado del operador postal y, en su caso, en el aviso de recibo que acompañe a la notificación, junto con el día y la hora en que se intentó la misma, intento que se repetirá por una sola vez y en una hora distinta dentro de los tres días siguientes.

5. Si practicado el segundo intento, éste resultase infructuoso por la misma causa consignada en el párrafo anterior o bien por el conocimiento sobrevenido de alguna de las previstas en el artículo siguiente, se consignará dicho extremo en la oportuna documentación del empleado del operador postal y, en su caso, en el aviso de recibo que acompañe a la notificación, junto con el día y la hora en que se realizó el segundo intento. A partir de este momento, dicha notificación tendrá el mismo tratamiento que las que hubieren sido rehusadas o rechazadas.

6. En todos los supuestos previstos en los párrafos anteriores, el empleado del operador postal deberá hacer constar su firma y número de identificación en el aviso de recibo que, en su caso, acompañe a la notificación y en el aviso de llegada si el mismo procede". Su proyección en aquel caso determinó la fijación del "dies a quo", para el plazo de caducidad de la acción de despido, en la fecha en la que el trabajador recogió el burofax en la oficina postal».

Por lo expuesto,

SUPLICO AL TRIBUNAL que, teniendo por presentado este escrito, con sus copias, se sirva admitirlo y, en su virtud, tenga por interpuesta DEMANDA POR EXTINCIÓN DE PRESTACIÓN POR INCAPACIDAD TEMPORAL POR INCOMPARECENCIA A RECONOCIMIENTO MÉDICO contra la Mutua [DENOMINACIÓN DE LA MUTUA], en la persona de su representante legal, tramitando la misma conforme a Derecho, citando a las partes para los trámites previos de conciliación y, en su caso, de juicio, concluyendo las actuaciones con una sentencia por la que se anule y deje sin efecto el alta médica acordada mediante Resolución de fecha [FECHA], y en la que se acuerde, por tanto, declarar la baja médica en el período comprendido entre el [FECHA] y el [FECHA], con lo demás procedente en Derecho.

Por ser de Justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

PRIMER OTROSÍ DIGO que esta parte acudirá al acto del juicio oral asistida de Letrado.

SEGUNDO OTROSÍ DIGO que se solicita la reclamación de oficio a la Mutua [DENOMINACIÓN DE LA MUTUA] del expediente y antecedentes que posea en relación con el contenido de la demanda.

TERCER OTROSÍ DIGO que interesa al Derecho de esta parte que se practiquen los siguientes

MEDIOS DE PRUEBA:

[OPCIONAL — incluir si procede]

DOCUMENTAL consistente en que por [ENTIDAD O PERSONA REQUERIDA] se aporten los siguientes documentos: [RELACIÓN DE DOCUMENTOS].

[OPCIONAL — incluir si procede]

DOCUMENTAL y TESTIFICAL: la que esta parte aportará en el acto del juicio.

SUPLICO AL TRIBUNAL que tenga por hechas las anteriores manifestaciones y por propuesta la prueba, la admita y la estime pertinente.

Por ser de Justicia que reitero en el lugar y fecha «ut supra».
