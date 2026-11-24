---
name: alegaciones-acta-infraccion-seguridad-social-empresarios-ss-012
description: "Alegaciones al acta de infracción de Seguridad Social a empresarios, formadores y autónomos. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Alegaciones al acta de infracción de Seguridad Social a empresarios, formadores y autónomos

> Formulario **SS-012** del plugin **Seguridad Social: demandas y recursos ante lo social** (`formularios-seguridad-social-demandas`) · Seguridad Social › Demandas y escritos ante la jurisdicción social · normativa revisada el 24-11-2026.

## Qué es

Escrito de alegaciones frente a un acta de infracción de la Inspección de Trabajo y Seguridad Social en materia de Seguridad Social (infracciones de los arts. 21, 22 y 23 de la LISOS), dirigido al órgano competente para sancionar, solicitando el sobreseimiento del expediente sancionador o, subsidiariamente, la reducción de la sanción propuesta.

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Alegaciones al acta de infracción de Seguridad Social a empresarios, formadores y autónomos» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Alegaciones al acta de infracción de Seguridad Social a empresarios, formadores y autónomos” para mi caso». También puedes invocarla directamente con `/formularios-seguridad-social-demandas:alegaciones-acta-infraccion-seguridad-social-empresarios-ss-012`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-seguridad-social-demandas:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Seguridad Social: demandas y recursos ante lo social) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (5 veces)
- [ ] DÍA, MES Y AÑO (3 veces)
- [ ] IMPORTE (2 veces)
- [ ] N.º DE ACTA (2 veces)
- [ ] NOMBRE Y APELLIDOS DEL ALEGANTE (2 veces)
- [ ] ARTÍCULO (21, 22 O 23) Y APARTADO QUE CORRESPONDA
- [ ] AÑO
- [ ] CALIFICACIÓN QUE REALIZA EL ACTA
- [ ] CÓDIGO POSTAL, LOCALIDAD Y DIRECCIÓN
- [ ] DENOMINACIÓN SOCIAL O NOMBRE DEL REPRESENTADO
- [ ] DESCRIPCIÓN BREVE DE LOS DOCUMENTOS
- [ ] DETALLAR CÓMO OCURRIERON LOS HECHOS
- [ ] DÍA
- [ ] LOCALIDAD
- [ ] MEDIO
- [ ] MES
- [ ] N.º DE DOCUMENTOS
- [ ] NIF/NIE
- [ ] NOMBRE Y APELLIDOS DE LOS TESTIGOS
- [ ] PROVINCIA
- [ ] ÓRGANO COMPETENTE AL QUE SE DIRIGE

## Normas que cita el formulario

- art. 52.1.b Real Decreto Legislativo 5/2000
- art. 17.1 Real Decreto 928/1998
- art. 52.1 Real Decreto 84/1996
- art. 25.3 Real Decreto 1415/2004
- art. 21.1 Real Decreto Legislativo 5/2000
- art. 25.4 Real Decreto 1415/2004
- art. 21.2 Real Decreto Legislativo 5/2000
- art. 139 Real Decreto Legislativo 8/2015
- art. 28 Real Decreto 84/1996
- art. 21.3 Real Decreto Legislativo 5/2000
- art. 21.4 Real Decreto Legislativo 5/2000
- art. 138.1 Real Decreto Legislativo 8/2015
- art. 17 Real Decreto 84/1996
- art. 21.5 Real Decreto Legislativo 5/2000
- art. 2 Real Decreto 625/2014
- art. 21.6 Real Decreto Legislativo 5/2000
- art. 138 Real Decreto Legislativo 8/2015
- art. 5 Real Decreto 84/1996
- art. 6 Real Decreto-ley 1/1986
- art. 22.1 Real Decreto Legislativo 5/2000
- art. 137.a Real Decreto Legislativo 8/2015
- art. 29 Real Decreto 84/1996
- art. 21 Ley 23/2015
- art. 22.2 Real Decreto Legislativo 5/2000
- art. 15 Real Decreto 2064/1995
- art. 55 Real Decreto 1415/2004
- art. 22.3 Real Decreto Legislativo 5/2000
- art. 22.4 Real Decreto Legislativo 5/2000
- art. 83 Real Decreto Legislativo 8/2015
- art. 61.1 Real Decreto 1993/1995

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

- Junto a «…ema español de personas desplazadas a España desde otro Estado miembro de la UE.»: el modelo cita numerosas disposiciones de desarrollo (reglamentos de afiliación, cotización y recaudación, órdenes ministeriales, normativa de formación profesional para el empleo) que han sido objeto de modificaciones o sustituciones posteriores. Antes de presentar, comprobar la vigencia y el artículo equivalente de cada una, y la redacción vigente de los arts. 21 a 23, 39, 40 y 46 de la LISOS (RDLeg 5/2000). En particular, comprobar el apartado citado del art. 5 del RD 84/1996 (el original traía «5.117») y el apartado del art. 23.1 LISOS relativo a los Reglamentos de la UE (el original traía «23.1.lm»); el modelo lo cita como 23.1.l).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

NOTAS DE USO (suprimir antes de presentar):

Modelo de escrito de alegaciones, ante el órgano competente para dictar resolución, en el caso de acta de infracción por las causas establecidas en los artículos 21, 22 o 23 de la Ley sobre Infracciones y Sanciones en el Orden Social (LISOS), con solicitud de sobreseimiento del expediente sancionador o, subsidiariamente, reducción de la sanción. Infracciones a las que puede referirse:

Leves (art. 21): no conservar la documentación o los registros o soportes informáticos; no exponer, poner a disposición o entregar los documentos de cotización; no comunicar las bajas o variaciones de los trabajadores o su no transmisión por medios informáticos, electrónicos o telemáticos; no cumplir el deber de información; no comunicar el cambio en los documentos de asociación o de adhesión; no remitir a la entidad las copias de los partes médicos de baja, confirmación de la baja o alta de incapacidad temporal facilitadas por los trabajadores, o no transmitirlos por medios informáticos, electrónicos o telemáticos.

Graves (art. 22): no solicitar la inscripción, no comunicar la apertura y cese de actividad de los centros de trabajo y demás variaciones, o su no transmisión; no solicitar o solicitar fuera de plazo la afiliación inicial o el alta de los trabajadores a su servicio; falta de ingreso total o parcial de las cuotas, habiendo cumplido las obligaciones de solicitud y transmisión de liquidaciones; incumplir las obligaciones económicas derivadas de su colaboración obligatoria; formalizar la protección por accidentes de trabajo y enfermedades profesionales, incapacidad temporal o la protección por cese de actividad, en entidad distinta; falta de entrega o no transmisión de documentos precisos para solicitar y tramitar cualquier prestación, incluido el certificado de empresa; falta de solicitud de afiliación o alta en el Régimen Especial de Trabajadores Autónomos; falta de abono de prestaciones a las entidades por las empresas responsables de su pago; obtener o disfrutar indebidamente cualquier tipo de reducciones, bonificaciones o incentivos en relación con las cuotas sociales; solicitud de afiliación o alta fuera de plazo de los trabajadores a su servicio cuando no medie actuación inspectora, o su no transmisión; no comprobar los empresarios que contraten o subcontraten con otros la afiliación o alta de los trabajadores; no proceder al alta y cotización por los salarios de tramitación y por las vacaciones devengadas y no disfrutadas antes de la extinción de la relación laboral; no comunicar a la entidad gestora de la prestación por desempleo las medidas de despido colectivo o de suspensión o reducción de jornada; ocupar a beneficiarios de pensiones incompatibles con el trabajo por cuenta ajena; incumplir las entidades de formación u organizadoras los requisitos de las acciones formativas; comunicar la baja en un régimen de la Seguridad Social de trabajadores por cuenta ajena pese a que continúen la misma actividad laboral o mantengan idéntica prestación de servicios, sirviéndose de un alta indebida en un régimen de trabajadores por cuenta propia.

Muy graves (art. 23): ocupar a beneficiarios o solicitantes de pensiones incompatibles con el trabajo por cuenta ajena; no ingresar ni liquidar las cuotas de Seguridad Social, o actuar fraudulentamente para eludir esa responsabilidad; falsear documentos o connivencia con los trabajadores para la obtención o disfrute fraudulento de prestaciones de la Seguridad Social o eludir obligaciones; pactar con sus trabajadores que paguen cuotas a cargo del empresario, o su renuncia a derechos de Seguridad Social; incremento indebido de la base de cotización o simulación de la contratación laboral; efectuar deducciones o compensaciones fraudulentas en las cuotas; no facilitar los datos identificativos de prestaciones sociales públicas; falsear documentos para obtener o disfrutar indebidamente bonificaciones en materia de formación profesional para el empleo; no suscribir el convenio especial de trabajadores con 55 o más años afectados por un despido colectivo; ocupar trabajadores afectados por la suspensión de contratos o reducción de jornada; retener o descontar de más indebidamente, y no ingresar en plazo, la parte de cuota de Seguridad Social de sus trabajadores; incumplir lo dispuesto en los Reglamentos de la Unión Europea sobre coordinación de sistemas de Seguridad Social respecto a la determinación de la legislación de Seguridad Social aplicable, cuando dicho incumplimiento dé lugar a la inscripción o alta en el sistema de Seguridad Social español de empresas, trabajadores por cuenta ajena o por cuenta propia, o a la falta de alta y cotización en el sistema español de personas desplazadas a España desde otro Estado miembro de la UE.


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

AL [ÓRGANO COMPETENTE PARA SANCIONAR POR RAZÓN DE LA MATERIA, ARTS. 48 Y 52.1.b) LISOS]

D./Dña. [NOMBRE Y APELLIDOS DEL ALEGANTE], con NIF/NIE número [NIF/NIE] y domicilio a efectos de notificaciones en [CÓDIGO POSTAL, LOCALIDAD Y DIRECCIÓN], [ELEGIR: actuando en su propio nombre / en nombre de [DENOMINACIÓN SOCIAL O NOMBRE DEL REPRESENTADO], cuya representación acredita conforme a la escritura de poder cuya copia acompaña], como mejor proceda comparece y

DICE:

Que el día [DÍA, MES Y AÑO] me ha sido notificada el acta de infracción número [N.º DE ACTA], con la que no estoy de acuerdo en cuanto al relato de hechos en los términos descritos, ni con su calificación jurídica, ni con la propuesta de sanción en la misma contenida, por lo que, dentro del plazo de quince días hábiles concedido al efecto, formulo el presente ESCRITO DE ALEGACIONES en base a los siguientes hechos y fundamentos de derecho:

HECHOS

PRIMERO.- Que con fecha [DÍA, MES Y AÑO] se levantó acta de infracción número [N.º DE ACTA] en la que se propone una multa de [IMPORTE] euros, ya que, de conformidad con el artículo [ARTÍCULO (21, 22 O 23) Y APARTADO QUE CORRESPONDA] del Real Decreto Legislativo 5/2000, de 4 de agosto, por el que se aprueba el texto refundido de la Ley sobre Infracciones y Sanciones en el Orden Social, los hechos descritos han sido calificados como constitutivos de la siguiente infracción:

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— (Si la infracción es leve) LEVE: [ELEGIR UNA DE LAS SIGUIENTES:]

No conservar la documentación o los registros o soportes informáticos.

No exponer, poner a disposición o entregar los documentos de cotización.

No comunicar las bajas o variaciones de los trabajadores o su no transmisión por medios informáticos, electrónicos o telemáticos.

No cumplir el deber de información.

No comunicar el cambio en los documentos de asociación o de adhesión.

No remitir a la entidad las copias de los partes médicos de baja, confirmación de la baja o alta de incapacidad temporal facilitadas por los trabajadores, o no transmitirlos por medios informáticos, electrónicos o telemáticos.

— (Si la infracción es grave) GRAVE: [ELEGIR UNA DE LAS SIGUIENTES:]

No solicitar la inscripción, no comunicar la apertura y cese de actividad de los centros de trabajo y demás variaciones, o su no transmisión.

No solicitar o solicitar fuera de plazo la afiliación inicial o el alta de los trabajadores a su servicio.

Falta de ingreso total o parcial de las cuotas, habiendo cumplido las obligaciones de solicitud y transmisión de liquidaciones.

Incumplir las obligaciones económicas derivadas de su colaboración obligatoria.

Formalizar la protección por accidentes de trabajo y enfermedades profesionales, incapacidad temporal o la protección por cese de actividad, en entidad distinta.

Falta de entrega o no transmisión de documentos precisos para solicitar y tramitar cualquier prestación, incluido el certificado de empresa.

Falta de solicitud de afiliación o alta en el Régimen Especial de Trabajadores Autónomos.

Falta de abono de prestaciones a las entidades por las empresas responsables de su pago.

Obtener o disfrutar indebidamente cualquier tipo de reducciones, bonificaciones o incentivos en relación con las cuotas sociales.

Solicitud de afiliación o alta fuera de plazo de los trabajadores a su servicio cuando no medie actuación inspectora, o su no transmisión.

No comprobar los empresarios que contraten o subcontraten con otros la afiliación o alta de los trabajadores.

No proceder al alta y cotización por los salarios de tramitación y por las vacaciones devengadas y no disfrutadas antes de la extinción de la relación laboral.

No comunicar a la entidad gestora de la prestación por desempleo las medidas de despido colectivo o de suspensión o reducción de jornada.

Ocupar a beneficiarios de pensiones incompatibles con el trabajo por cuenta ajena.

Incumplir las entidades de formación u organizadoras los requisitos de las acciones formativas.

Comunicar la baja en un régimen de la Seguridad Social de trabajadores por cuenta ajena pese a que continúen la misma actividad laboral o mantengan idéntica prestación de servicios, sirviéndose de un alta indebida en un régimen de trabajadores por cuenta propia.

— (Si la infracción es muy grave) MUY GRAVE: [ELEGIR UNA DE LAS SIGUIENTES:]

Ocupar a beneficiarios o solicitantes de pensiones incompatibles con el trabajo por cuenta ajena.

No ingresar ni liquidar las cuotas de Seguridad Social, o actuar fraudulentamente para eludir esa responsabilidad.

Falsear documentos o la connivencia con los trabajadores para la obtención o disfrute fraudulento de prestaciones de la Seguridad Social o eludir obligaciones.

Pactar con sus trabajadores que paguen cuotas a cargo del empresario, o su renuncia a derechos de Seguridad Social.

Incremento indebido de la base de cotización o simulación de la contratación laboral.

Efectuar deducciones o compensaciones fraudulentas en las cuotas.

No facilitar los datos identificativos de prestaciones sociales públicas.

Falsear documentos para obtener o disfrutar indebidamente de bonificaciones en materia de formación profesional para el empleo.

No suscribir el convenio especial de trabajadores con 55 o más años afectados por un despido colectivo.

Ocupar trabajadores afectados por la suspensión de contratos o reducción de jornada.

Retener o descontar de más indebidamente, y no ingresar en plazo, la parte de cuota de Seguridad Social de sus trabajadores.

Incumplir lo dispuesto en los Reglamentos de la Unión Europea sobre Coordinación de Sistemas de Seguridad Social, respecto a la determinación de la legislación de seguridad social aplicable, cuando dicho incumplimiento dé lugar a la inscripción o alta en el sistema de seguridad social español de empresas, trabajadores por cuenta ajena o por cuenta propia, o dé lugar a la falta de alta y cotización en el sistema de seguridad social español de personas desplazadas a España desde otro Estado miembro de la UE.

SEGUNDO.- Que, en el acta de infracción arriba referenciada, se reflejan unos hechos que no responden a la realidad de lo acaecido, al no describirse pormenorizadamente el supuesto comportamiento infractor, ni destacar cuáles son los hechos relevantes a efectos de la tipificación y graduación de la sanción. En concreto, los hechos tal y como sucedieron son los siguientes: [DETALLAR CÓMO OCURRIERON LOS HECHOS].

TERCERO.- Que la calificación realizada en el acta de los anteriores hechos no es conforme al ordenamiento jurídico, puesto que no se dan los elementos objetivos y subjetivos de la infracción presuntamente cometida, en base a las siguientes razones:

A) En relación con los elementos objetivos de la infracción, los hechos reflejados en el acta de infracción no son ciertos, por cuanto que [ARGUMENTAR LOS MOTIVOS DE CONTRADICCIÓN; POR EJEMPLO: «el parte de afiliación del trabajador al que alude el acta fue cursado el día [FECHA], y el acta de la inspección se levantó en fecha [FECHA]; es decir, ya había transcurrido el plazo mínimo de cuatro años en los que se está obligado a conservar la mencionada documentación»; o «la inscripción de la empresa se solicitó el día [FECHA] mediante escrito dirigido y presentado ante la Dirección Provincial de la Tesorería General de la Seguridad Social de [PROVINCIA], y la actividad se inició posteriormente en fecha [FECHA]»; o «el parte de alta del trabajador al que alude el acta se comunicó el día [FECHA] mediante [MEDIO], es decir, con carácter previo a la prestación de servicios, que tuvo lugar con posterioridad, por lo que no hubo una ocupación ilegal»].

[OPCIONAL — incluir si procede (si no se refleja el nombre de los trabajadores en el acta)]

Además, el acta de infracción nos causa una gran indefensión porque no refleja el nombre de los trabajadores afectados por la supuesta infracción que ha originado el acta, por lo que no podemos conocer con exactitud cuál ha sido el supuesto comportamiento infractor y, en consecuencia, proceder a desvirtuar tales afirmaciones.

[OPCIONAL — incluir si procede (si el acta se limita a calificar los hechos de forma genérica)]

Además, el acta de infracción califica genéricamente los hechos como [CALIFICACIÓN QUE REALIZA EL ACTA], sin describir pormenorizadamente la conducta realizada por el empresario, y no se aportan los elementos de juicio necesarios, dado lo escaso del relato, para que el órgano competente sancionador pueda adoptar su decisión, ni tampoco para que el inculpado pueda defenderse de unos hechos que no se describen con el detalle necesario para poder ser calificados como constitutivos de esta infracción, tal y como reiteradamente viene exigiendo la jurisprudencia de nuestro Tribunal Supremo.

B) En cuanto al elemento subjetivo, los hechos acaecidos no son susceptibles de incardinarse en la infracción administrativa tal y como se hizo en el acta de infracción, sino que, en atención a lo sucedido y a las circunstancias de hecho concurrentes, no existe culpabilidad del empresario.

CUARTO.- Que la propuesta de sanción realizada en el acta de infracción, consistente en el pago de una multa en cuantía de [IMPORTE] euros, vulnera el principio de proporcionalidad (adaptación de la sanción a la gravedad de los hechos reprochables a los interesados, a partir del carácter intencional de la infracción, la reincidencia, la naturaleza de los daños causados, etc.) y demás principios que informan el ejercicio de la potestad sancionadora en materia de infracciones en el orden social, atendiendo al relato de hechos más arriba reseñado.

Que para la demostración de las afirmaciones anteriormente manifestadas en este escrito de alegaciones, y sin perjuicio de las demás actuaciones que de oficio sean practicadas por el órgano instructor competente, se propone la práctica de los siguientes

MEDIOS DE PRUEBA:

[OPCIONAL — incluir si procede]

Testifical, consistente en que se tome declaración a [NOMBRE Y APELLIDOS DE LOS TESTIGOS], en cuanto [ELEGIR: personas trabajadoras / clientes] y testigos presenciales de los hechos reflejados en el acta de infracción, por tener un conocimiento directo de los mismos en razón de su presencia física en el momento en que tuvo lugar la infracción presuntamente cometida.

[OPCIONAL — incluir si procede]

Documental, consistente en los escritos que se acompañan como números [N.º DE DOCUMENTOS], consistentes en [DESCRIPCIÓN BREVE DE LOS DOCUMENTOS], todos ellos necesarios para el conocimiento más preciso de los hechos reflejados en el acta de infracción, así como de las posibles responsabilidades.

A los anteriores hechos son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

I.- El presente escrito de alegaciones se interpone en virtud de lo establecido en el artículo 52.1.b) del Real Decreto Legislativo 5/2000, de 4 de agosto, por el que se aprueba el texto refundido de la Ley sobre Infracciones y Sanciones en el Orden Social, en relación con lo dispuesto en el artículo 17.1 del Real Decreto 928/1998, de 14 de mayo, por el que se aprueba el Reglamento general sobre procedimientos para la imposición de sanciones por infracciones de orden social y para los expedientes liquidatorios de cuotas de la Seguridad Social.

II.- Aquel a quien me dirijo es el órgano competente para su tramitación, ya que el escrito de alegaciones y los medios de prueba de que intenten valerse serán presentados ante el órgano instructor del expediente, de acuerdo con el citado artículo 17.1 del Real Decreto 928/1998, de 14 de mayo.

III.- Notificada el acta de infracción el día [DÍA, MES Y AÑO], se formula el presente escrito de alegaciones dentro del indicado plazo de quince días.

IV.- [ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS, SEGÚN LA INFRACCIÓN IMPUTADA:]

— (Si la infracción es leve)

(No conservar la documentación o los registros o soportes informáticos) Son de aplicación el artículo 52.1 del Real Decreto 84/1996, de 26 de enero, por el que se aprueba el Reglamento General sobre inscripción de empresas y afiliación, altas, bajas y variaciones de datos de trabajadores en la Seguridad Social, el artículo 25.3 del Real Decreto 1415/2004, de 11 de junio, por el que se aprueba el Reglamento General de Recaudación de la Seguridad Social, el artículo 3 de la Orden de 27 de diciembre de 1994 por la que se aprueba el modelo de recibo individual de salarios, y los artículos 21.1, 39 y 40 del Real Decreto Legislativo 5/2000, de 4 de agosto, por el que se aprueba el texto refundido de la Ley sobre Infracciones y Sanciones en el Orden Social.

(No exponer, poner a disposición o entregar los documentos de cotización) Es de aplicación el artículo 25.4 del Real Decreto 1415/2004, de 11 de junio, por el que se aprueba el Reglamento General de Recaudación de la Seguridad Social, así como la Orden ESS/484/2013, de 26 de marzo, por la que se regula el Sistema de remisión electrónica de datos en el ámbito de la Seguridad Social, y los artículos 21.2, 39 y 40 del Real Decreto Legislativo 5/2000, de 4 de agosto, por el que se aprueba el texto refundido de la Ley sobre Infracciones y Sanciones en el Orden Social.

(No comunicar las bajas o variaciones de los trabajadores o su no transmisión por medios informáticos, electrónicos o telemáticos) Es de aplicación el artículo 139 del Real Decreto Legislativo 8/2015, de 30 de octubre, por el que se aprueba el texto refundido de la Ley General de la Seguridad Social, en relación con los artículos 28 a 32 del Real Decreto 84/1996, de 26 de enero, por el que se aprueba el Reglamento general sobre inscripción de empresas y afiliación, altas, bajas y variaciones de datos de los trabajadores en la Seguridad Social, así como los artículos 21.3, 39 y 40 del Real Decreto Legislativo 5/2000, de 4 de agosto, por el que se aprueba el texto refundido de la Ley sobre Infracciones y Sanciones en el Orden Social.

(No cumplir el deber de información) Son de aplicación los artículos 21.4, 39 y 40 del Real Decreto Legislativo 5/2000, de 4 de agosto, por el que se aprueba el texto refundido de la Ley sobre Infracciones y Sanciones en el Orden Social.

(No comunicar el cambio en los documentos de asociación o de adhesión) El artículo 138.1, párrafo segundo, del Real Decreto Legislativo 8/2015, de 30 de octubre, por el que se aprueba el texto refundido de la Ley General de la Seguridad Social, en relación con el artículo 17 del Real Decreto 84/1996, de 26 de enero, por el que se aprueba el Reglamento General sobre inscripción de empresas y afiliación, altas, bajas y variaciones de datos de trabajadores en la Seguridad Social, así como los artículos 21.5, 39 y 40 del Real Decreto Legislativo 5/2000, de 4 de agosto, por el que se aprueba el texto refundido de la Ley sobre Infracciones y Sanciones en el Orden Social.

(No remitir a la entidad las copias de los partes médicos de baja, confirmación de la baja o alta de incapacidad temporal facilitadas por los trabajadores, o no transmitirlos por medios informáticos, electrónicos o telemáticos) El artículo 2 del Real Decreto 625/2014, de 18 de julio, por el que se regulan determinados aspectos de la gestión y control de los procesos por incapacidad temporal en los primeros trescientos sesenta y cinco días de su duración, así como la Orden ESS/1187/2015, de 15 de junio, que lo desarrolla, y los artículos 21.6, 39 y 40 del Real Decreto Legislativo 5/2000, de 4 de agosto, por el que se aprueba el texto refundido de la Ley sobre Infracciones y Sanciones en el Orden Social.

— (Si la infracción es grave)

(No solicitar la inscripción, no comunicar la apertura y cese de actividad de los centros de trabajo y demás variaciones, o su no transmisión) [ELEGIR UNA O AMBAS:] Es de aplicación el artículo 138 del Real Decreto Legislativo 8/2015, de 30 de octubre, por el que se aprueba el texto refundido de la Ley General de la Seguridad Social, en relación con el artículo 5 del Real Decreto 84/1996, de 26 de enero, por el que se aprueba el Reglamento general sobre inscripción de empresas y afiliación, altas, bajas y variaciones de datos de los trabajadores en la Seguridad Social [COMPROBAR EL APARTADO: el original traía «5.117»]. / Es de aplicación el artículo 6, apartados 1 y 3, del Real Decreto-ley 1/1986, de 14 de marzo, de medidas urgentes administrativas, financieras, fiscales y laborales, en relación con los artículos 1 y siguientes de la Orden TIN/1071/2010, de 27 de abril, sobre los requisitos y datos que deben reunir las comunicaciones de apertura o de reanudación de actividades en los centros de trabajo, así como los artículos 22.1, 39 y 40 del Real Decreto Legislativo 5/2000, de 4 de agosto, por el que se aprueba el texto refundido de la Ley sobre Infracciones y Sanciones en el Orden Social.

(No solicitar o solicitar fuera de plazo la afiliación o alta de los trabajadores a su servicio) Son de aplicación los artículos 137.a) y 139 del Real Decreto Legislativo 8/2015, de 30 de octubre, por el que se aprueba el texto refundido de la Ley General de la Seguridad Social, en relación con los artículos 29 a 32 del Real Decreto 84/1996, de 26 de enero, por el que se aprueba el Reglamento general sobre inscripción de empresas y afiliación, altas, bajas y variaciones de datos de los trabajadores en la Seguridad Social, los artículos 21 y 23 de la Ley 23/2015, de 21 de julio, Ordenadora del Sistema de Inspección de Trabajo y Seguridad Social, sobre actuación inspectora y presunción de certeza de las actas, el artículo 1.1 y 1.3.d) del Real Decreto Legislativo 2/2015, de 23 de octubre, por el que se aprueba el texto refundido de la Ley del Estatuto de los Trabajadores, así como los artículos 22.2, 39 y 40 del Real Decreto Legislativo 5/2000, de 4 de agosto, por el que se aprueba el texto refundido de la Ley sobre Infracciones y Sanciones en el Orden Social.

(Falta de ingreso total o parcial de las cuotas, habiendo cumplido las obligaciones de solicitud y transmisión de liquidaciones) Son de aplicación los artículos 15 y 16 del Real Decreto 2064/1995, de 22 de diciembre, por el que se aprueba el Reglamento general sobre cotización y liquidación de otros derechos de la Seguridad Social, en relación con los artículos 55 y 56 del Real Decreto 1415/2004, de 11 de junio, por el que se aprueba el Reglamento General de Recaudación de la Seguridad Social, así como los artículos 22.3, 39 y 40 del Real Decreto Legislativo 5/2000, de 4 de agosto, por el que se aprueba el texto refundido de la Ley sobre Infracciones y Sanciones en el Orden Social, en relación con el artículo 307 del Código Penal, aprobado por la Ley Orgánica 10/1995, de 23 de noviembre.

(Incumplir las obligaciones económicas derivadas de su colaboración obligatoria) Son de aplicación los artículos 29.2 y 102.1.c) del Real Decreto Legislativo 8/2015, de 30 de octubre, por el que se aprueba el texto refundido de la Ley General de la Seguridad Social, en relación con los artículos 16 y 17 de la Orden de 25 de noviembre de 1966 por la que se regula la colaboración de las empresas en la gestión del Régimen General de la Seguridad Social, así como los artículos 22.4, 39 y 40 del Real Decreto Legislativo 5/2000, de 4 de agosto, por el que se aprueba el texto refundido de la Ley sobre Infracciones y Sanciones en el Orden Social.

(Formalizar la protección por accidentes de trabajo y enfermedades profesionales, incapacidad temporal o la protección por cese de actividad, en entidad distinta) Es de aplicación el artículo 83 del Real Decreto Legislativo 8/2015, de 30 de octubre, por el que se aprueba el texto refundido de la Ley General de la Seguridad Social, en relación con los artículos 61.1 y 69 del Real Decreto 1993/1995, de 7 de diciembre, por el que se aprueba el Reglamento sobre colaboración de las Mutuas de Accidentes de Trabajo y Enfermedades Profesionales, así como los artículos 22.5, 39 y 40 del Real Decreto Legislativo 5/2000, de 4 de agosto, por el que se aprueba el texto refundido de la Ley sobre Infracciones y Sanciones en el Orden Social.

(Falta de entrega o no transmisión de documentos precisos para solicitar y tramitar cualquier prestación, incluido el certificado de empresa) Es de aplicación el artículo 298.d) del Real Decreto Legislativo 8/2015, de 30 de octubre, por el que se aprueba el texto refundido de la Ley General de la Seguridad Social, en relación con los artículos 21.5 y 27 del Real Decreto 625/1985, de 2 de abril, por el que se desarrolla la Ley 31/1984, de 2 de agosto, de protección por desempleo, la Orden TIN/790/2010, de 24 de marzo, por la que se regula el envío por las empresas de los datos del certificado de empresa al Servicio Público de Empleo Estatal por medios electrónicos, así como los artículos 22.6, 39 y 40 del Real Decreto Legislativo 5/2000, de 4 de agosto, por el que se aprueba el texto refundido de la Ley sobre Infracciones y Sanciones en el Orden Social.

(Falta de solicitud de afiliación o alta en el Régimen Especial de Trabajadores Autónomos) Es de aplicación el artículo 46 del Real Decreto 84/1996, de 26 de enero, por el que se aprueba el Reglamento general sobre inscripción de empresas y afiliación, altas, bajas y variaciones de datos de los trabajadores en la Seguridad Social, el artículo 305 del Real Decreto Legislativo 8/2015, de 30 de octubre, por el que se aprueba el texto refundido de la Ley General de la Seguridad Social, en relación con el artículo 2 del Decreto 2530/1970, de 20 de agosto, por el que se regula el Régimen Especial de la Seguridad Social de los Trabajadores por Cuenta Propia o Autónomos, y el artículo 1 de la Orden de 24 de septiembre de 1970 por la que se dictan normas para aplicación y desarrollo del Régimen Especial de la Seguridad Social de los Trabajadores por Cuenta Propia o Autónomos, que exigen para estar incluidos en su campo de aplicación realizar de «forma habitual» una actividad económica, así como los artículos 22.7, 39 y 40 del Real Decreto Legislativo 5/2000, de 4 de agosto, por el que se aprueba el texto refundido de la Ley sobre Infracciones y Sanciones en el Orden Social.

(Falta de abono de prestaciones a las entidades por las empresas responsables de su pago) Son de aplicación los artículos 167 y 281 del Real Decreto Legislativo 8/2015, de 30 de octubre, por el que se aprueba el texto refundido de la Ley General de la Seguridad Social, en relación con el artículo 32.1.c) del Real Decreto 625/1985, de 2 de abril, por el que se desarrolla la Ley 31/1984, de 2 de agosto, de protección por desempleo, así como los artículos 22.8, 39 y 40 del Real Decreto Legislativo 5/2000, de 4 de agosto, por el que se aprueba el texto refundido de la Ley sobre Infracciones y Sanciones en el Orden Social.

(Obtener o disfrutar indebidamente cualquier tipo de reducciones, bonificaciones o incentivos en relación con las cuotas sociales) Es de aplicación el artículo 20 del Real Decreto Legislativo 8/2015, de 30 de octubre, por el que se aprueba el texto refundido de la Ley General de la Seguridad Social, así como los artículos 22.9, 39 y 40 del Real Decreto Legislativo 5/2000, de 4 de agosto, por el que se aprueba el texto refundido de la Ley sobre Infracciones y Sanciones en el Orden Social.

(Solicitud de afiliación o alta fuera de plazo de los trabajadores a su servicio cuando no medie actuación inspectora, o su no transmisión) Son de aplicación los artículos 138 y 139 del Real Decreto Legislativo 8/2015, de 30 de octubre, por el que se aprueba el texto refundido de la Ley General de la Seguridad Social, en relación con los artículos 32, 38 y 39 del Real Decreto 84/1996, de 26 de enero, por el que se aprueba el Reglamento general sobre inscripción de empresas y afiliación, altas, bajas y variaciones de datos de los trabajadores en la Seguridad Social, así como los artículos 22.10, 39 y 40 del Real Decreto Legislativo 5/2000, de 4 de agosto, por el que se aprueba el texto refundido de la Ley sobre Infracciones y Sanciones en el Orden Social.

(No comprobar los empresarios que contraten o subcontraten con otros la afiliación o alta de los trabajadores) Son de aplicación los apartados 5 y 6 del artículo 16 del Real Decreto Legislativo 8/2015, de 30 de octubre, por el que se aprueba el texto refundido de la Ley General de la Seguridad Social, así como los artículos 22.11, 39 y 40 del Real Decreto Legislativo 5/2000, de 4 de agosto, por el que se aprueba el texto refundido de la Ley sobre Infracciones y Sanciones en el Orden Social.

(No proceder al alta y cotización por los salarios de tramitación y por las vacaciones devengadas y no disfrutadas antes de la extinción de la relación laboral) Son de aplicación los artículos 268.6 y 147.1 del Real Decreto Legislativo 8/2015, de 30 de octubre, por el que se aprueba el texto refundido de la Ley General de la Seguridad Social, y el artículo 56 del Real Decreto Legislativo 2/2015, de 23 de octubre, por el que se aprueba el texto refundido de la Ley del Estatuto de los Trabajadores, el Real Decreto 418/2014, de 6 de junio, por el que se modifica el procedimiento de tramitación de las reclamaciones al Estado por salarios de tramitación en juicios por despido, y el artículo 56.1.c).4.º del Real Decreto 1415/2004, de 11 de junio, por el que se aprueba el Reglamento General de Recaudación de la Seguridad Social, así como los artículos 22.12, 39 y 40 del Real Decreto Legislativo 5/2000, de 4 de agosto, por el que se aprueba el texto refundido de la Ley sobre Infracciones y Sanciones en el Orden Social.

(No comunicar a la entidad gestora de la prestación por desempleo las medidas de despido colectivo o de suspensión o reducción de jornada) Es de aplicación el artículo 267.3 del Real Decreto Legislativo 8/2015, de 30 de octubre, por el que se aprueba el texto refundido de la Ley General de la Seguridad Social, el artículo 22 del Real Decreto 625/1985, de 2 de abril, de protección por desempleo, y los artículos 22.13, 39 y 40 del Real Decreto Legislativo 5/2000, de 4 de agosto, por el que se aprueba el texto refundido de la Ley sobre Infracciones y Sanciones en el Orden Social.

(Ocupar a beneficiarios de pensiones incompatibles con el trabajo por cuenta ajena) Son de aplicación los artículos 22.14, 39 y 40 del Real Decreto Legislativo 5/2000, de 4 de agosto, por el que se aprueba el texto refundido de la Ley sobre Infracciones y Sanciones en el Orden Social.

(Incumplir las entidades de formación u organizadoras los requisitos de las acciones formativas) Son de aplicación los artículos 14 a 16 y 19 de la Ley 30/2015, de 9 de septiembre, por la que se regula el Sistema de Formación Profesional para el empleo en el ámbito laboral, así como los artículos 22.15, 39 y 40 del Real Decreto Legislativo 5/2000, de 4 de agosto, por el que se aprueba el texto refundido de la Ley sobre Infracciones y Sanciones en el Orden Social.

— (Si la infracción es muy grave)

(Ocupar a beneficiarios o solicitantes de pensiones incompatibles con el trabajo por cuenta ajena) Son de aplicación los artículos 139 y 137.a) del Real Decreto Legislativo 8/2015, de 30 de octubre, por el que se aprueba el texto refundido de la Ley General de la Seguridad Social, en relación con los artículos 29 a 32 del Real Decreto 84/1996, de 26 de enero, por el que se aprueba el Reglamento general sobre inscripción de empresas y afiliación, altas, bajas y variaciones de datos de los trabajadores en la Seguridad Social, así como los artículos 23.1.a), 39, 40 y 46 del Real Decreto Legislativo 5/2000, de 4 de agosto, por el que se aprueba el texto refundido de la Ley sobre Infracciones y Sanciones en el Orden Social.

(No ingresar ni liquidar las cuotas de Seguridad Social, o actuar fraudulentamente para eludir esa responsabilidad) Son de aplicación los artículos 15 y 16 del Real Decreto 2064/1995, de 22 de diciembre, por el que se aprueba el Reglamento general sobre cotización y liquidación de otros derechos de la Seguridad Social, en relación con los artículos 55 y 56 del Real Decreto 1415/2004, de 11 de junio, por el que se aprueba el Reglamento General de Recaudación de la Seguridad Social, así como los artículos 23.1.b), 39, 40 y 46 del Real Decreto Legislativo 5/2000, de 4 de agosto, por el que se aprueba el texto refundido de la Ley sobre Infracciones y Sanciones en el Orden Social, y el artículo 307 del Código Penal, aprobado por la Ley Orgánica 10/1995, de 23 de noviembre.

(Falsear documentos o la connivencia con los trabajadores para la obtención o disfrute fraudulento de prestaciones de la Seguridad Social o eludir obligaciones) Es de aplicación el artículo 298 del Real Decreto Legislativo 8/2015, de 30 de octubre, por el que se aprueba el texto refundido de la Ley General de la Seguridad Social, en relación con los artículos 21.5 y 27 del Real Decreto 625/1985, de 2 de abril, de protección por desempleo, así como los artículos 23.1.c), 39, 40 y 46 del Real Decreto Legislativo 5/2000, de 4 de agosto, por el que se aprueba el texto refundido de la Ley sobre Infracciones y Sanciones en el Orden Social.

(Pactar con sus trabajadores que paguen cuotas a cargo del empresario, o su renuncia a derechos de Seguridad Social) Son de aplicación los artículos 3 y 143 del Real Decreto Legislativo 8/2015, de 30 de octubre, por el que se aprueba el texto refundido de la Ley General de la Seguridad Social, en relación con el artículo 3.1.c) del Real Decreto Legislativo 2/2015, de 23 de octubre, por el que se aprueba el texto refundido de la Ley del Estatuto de los Trabajadores, así como los artículos 23.1.d), 39, 40 y 46 del Real Decreto Legislativo 5/2000, de 4 de agosto, por el que se aprueba el texto refundido de la Ley sobre Infracciones y Sanciones en el Orden Social.

(Incremento indebido de la base de cotización o simulación de la contratación laboral) Es de aplicación el artículo 209.2 y 3 del Real Decreto Legislativo 8/2015, de 30 de octubre, por el que se aprueba el texto refundido de la Ley General de la Seguridad Social, así como los artículos 23.1.e), 39, 40 y 46 del Real Decreto Legislativo 5/2000, de 4 de agosto, por el que se aprueba el texto refundido de la Ley sobre Infracciones y Sanciones en el Orden Social.

(Efectuar deducciones o compensaciones fraudulentas en las cuotas) Son de aplicación los artículos 23.1.f), 39, 40 y 46 del Real Decreto Legislativo 5/2000, de 4 de agosto, por el que se aprueba el texto refundido de la Ley sobre Infracciones y Sanciones en el Orden Social.

(No facilitar los datos identificativos de prestaciones sociales públicas) Es de aplicación el artículo 72 del Real Decreto Legislativo 8/2015, de 30 de octubre, por el que se aprueba el texto refundido de la Ley General de la Seguridad Social, en relación con el Real Decreto 397/1996, de 1 de marzo, y el artículo 5 de la Orden de 9 de enero de 1997, así como los artículos 23.1.g), 39, 40 y 46 del Real Decreto Legislativo 5/2000, de 4 de agosto, por el que se aprueba el texto refundido de la Ley sobre Infracciones y Sanciones en el Orden Social.

(Falsear documentos para obtener o disfrutar indebidamente de bonificaciones en materia de formación profesional para el empleo) Es de aplicación el Real Decreto 694/2017, de 3 de julio, por el que se desarrolla la Ley 30/2015, de 9 de septiembre, por la que se regula el Sistema de Formación Profesional para el Empleo en el ámbito laboral, en relación con la Orden TAS/2307/2007, de 27 de julio, por la que se regula el subsistema de formación profesional para el empleo en materia de formación de demanda y su financiación, y se crea el correspondiente sistema telemático y los ficheros de datos personales de titularidad del Servicio Público de Empleo Estatal, así como los artículos 23.1.h), 39, 40 y 46 del Real Decreto Legislativo 5/2000, de 4 de agosto, por el que se aprueba el texto refundido de la Ley sobre Infracciones y Sanciones en el Orden Social.

(No suscribir el convenio especial de trabajadores con 55 o más años afectados por un despido colectivo) Es de aplicación el artículo 51.9 del Real Decreto Legislativo 2/2015, de 23 de octubre, por el que se aprueba el texto refundido de la Ley del Estatuto de los Trabajadores, así como los artículos 23.1.i), 39, 40 y 46 del Real Decreto Legislativo 5/2000, de 4 de agosto, por el que se aprueba el texto refundido de la Ley sobre Infracciones y Sanciones en el Orden Social.

(Ocupar trabajadores afectados por la suspensión de contratos o reducción de jornada) Es de aplicación el artículo 298.h) del Real Decreto Legislativo 8/2015, de 30 de octubre, por el que se aprueba el texto refundido de la Ley General de la Seguridad Social, así como los artículos 23.1.j), 39, 40 y 46 del Real Decreto Legislativo 5/2000, de 4 de agosto, por el que se aprueba el texto refundido de la Ley sobre Infracciones y Sanciones en el Orden Social.

(Retener o descontar de más indebidamente, y no ingresar en plazo, la parte de cuota de Seguridad Social de sus trabajadores) Son de aplicación los artículos 18 y 19 del Real Decreto Legislativo 8/2015, de 30 de octubre, por el que se aprueba el texto refundido de la Ley General de la Seguridad Social, y los artículos 9 y 23 y siguientes del Real Decreto 2064/1995, de 22 de diciembre, por el que se aprueba el Reglamento General sobre Cotización y Liquidación de otros derechos de la Seguridad Social, así como los artículos 23.1.k), 39, 40 y 46 del Real Decreto Legislativo 5/2000, de 4 de agosto, por el que se aprueba el texto refundido de la Ley sobre Infracciones y Sanciones en el Orden Social.

(Incumplir lo dispuesto en los Reglamentos de la Unión Europea sobre Coordinación de Sistemas de Seguridad Social, respecto a la determinación de la legislación de seguridad social aplicable, cuando dicho incumplimiento dé lugar a la inscripción o alta en el sistema de seguridad social español de empresas, trabajadores por cuenta ajena o por cuenta propia, o dé lugar a la falta de alta y cotización en el sistema de seguridad social español de personas desplazadas a España desde otro Estado miembro de la UE) Son de aplicación los Reglamentos (CE) n.º 883/2004, de 29 de abril de 2004, sobre la coordinación de los sistemas de seguridad social, y n.º 987/2009, de 16 de septiembre de 2009, de aplicación del anterior, del Parlamento Europeo y del Consejo, así como los artículos 23.1.l), 39, 40 y 46 del Real Decreto Legislativo 5/2000, de 4 de agosto, por el que se aprueba el texto refundido de la Ley sobre Infracciones y Sanciones en el Orden Social.

En virtud de lo expuesto,

SOLICITA DE ESE [ÓRGANO COMPETENTE AL QUE SE DIRIGE] que tenga por presentado este escrito de alegaciones con los documentos que se acompañan y, previa la práctica de las pruebas propuestas y la tramitación que proceda, dicte resolución en la que se deje sin efecto el acta de infracción y, en consecuencia, acuerde el sobreseimiento del expediente sancionador o, subsidiariamente y para el caso de no estimar la petición de archivo del expediente, disponga la reducción de la sanción inicialmente propuesta a la cuantía inferior de su grado mínimo, sin perjuicio de la interposición ulterior de los recursos procedentes.

Es de Justicia que pide en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

D./Dña. [NOMBRE Y APELLIDOS DEL ALEGANTE]
