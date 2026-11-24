---
name: recurso-alzada-contra-sancion-seguridad-social-ss-039
description: "Recurso de alzada contra sanción de Seguridad Social a empresarios, entidades formativas y autónomos. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Recurso de alzada contra sanción de Seguridad Social a empresarios, entidades formativas y autónomos

> Formulario **SS-039** del plugin **Seguridad Social: reclamaciones previas y recursos administrativos** (`formularios-seguridad-social-tramites`) · Seguridad Social › Solicitudes, reclamaciones y recursos ante la Administración · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **recursos**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Recurso de alzada contra sanción de Seguridad Social a empresarios, entidades formativas y autónomos» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Recurso de alzada contra sanción de Seguridad Social a empresarios, entidades formativas y autónomos” para mi caso». También puedes invocarla directamente con `/formularios-seguridad-social-tramites:recurso-alzada-contra-sancion-seguridad-social-ss-039`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-seguridad-social-tramites:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Seguridad Social: reclamaciones previas y recursos administrativos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (4 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] IMPORTE (3 veces)
- [ ] DATO CONSIGNADO EN EL ACTA
- [ ] DESCRIBIR
- [ ] DNI/NIE
- [ ] DOMICILIO A EFECTOS DE NOTIFICACIONES
- [ ] EXPONER LOS HECHOS
- [ ] LOCALIDAD
- [ ] MEDIOS PROBATORIOS CONSIGNADOS
- [ ] MOTIVO
- [ ] Nº
- [ ] Nº DE EXPEDIENTE
- [ ] NÚMERO
- [ ] PRUEBAS NO ADMITIDAS
- [ ] TIPIFICACIÓN DE LA INFRACCIÓN
- [ ] ÓRGANO AL QUE SE DIRIGE
- [ ] ÓRGANO O PERSONA

## Normas que cita el formulario

- art. 54 Real Decreto Legislativo 5/2000
- art. 23 Real Decreto 928/1998
- art. 25.2 Ley 40/2015
- art. 25.1 Ley 40/2015
- art. 53.1.b Real Decreto Legislativo 5/2000
- art. 53.2 Real Decreto Legislativo 5/2000
- art. 14.1 Real Decreto 928/1998
- art. 21.1 Ley 23/2015
- art. 39 Real Decreto Legislativo 5/2000

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

AL ÓRGANO SUPERIOR JERÁRQUICO DEL QUE DICTÓ LA RESOLUCIÓN, ARTS. 121.1 L 39/2015, 23 RD 928/1998 y 48 LISOS
HECHOS
FUNDAMENTOS DE DERECHO
Firmas

Modelo de recurso de alzada, ante el órgano superior jerárquico del que dictó la resolución, contra resolución sancionadora por infracción de empresarios, entidades de formación o que asuman la organización de la formación, trabajadores por cuenta propia y asimilados, conforme establecen los artículos 54 del Real Decreto Legislativo 5/2000, de 4 de agosto, por el que se aprueba el texto refundido de la Ley sobre Infracciones y Sanciones en el Orden Social, 23 del Real Decreto 928/1998, de 14 de mayo, por el que se aprueba el Reglamento General sobre Procedimientos para la Imposición de las Sanciones por Infracciones de Orden Social y para los Expedientes Liquidatorios de Cuotas de la Seguridad Social, y 121 y 122 de la Ley 39/2015, de 1 de octubre, del Procedimiento Administrativo Común de las Administraciones Públicas, por las siguientes causas establecidas en el artículo 21, 22 o 23.1 de la LISOS:

- No conservar la documentación o los registros o soportes informáticos

- No exponer, poner a disposición o entregar los documentos de cotización

- No comunicar las bajas o variaciones de los trabajadores o su no transmisión por medios informáticos, electrónicos o telemáticos

- No cumplir el deber de información

- No comunicar el cambio en los documentos de asociación o de adhesión

- No remitir a la entidad las copias de los partes médicos de baja, confirmación de la baja o alta de incapacidad temporal facilitadas por los trabajadores, o no transmitirlos por medios informáticos, electrónicos o telemáticos

- No solicitar la inscripción, no comunicar la apertura y cese de actividad de los centros de trabajo y demás variaciones, o su no transmisión

- No solicitar o solicitar fuera de plazo la afiliación inicial o el alta de los trabajadores a su servicio

- Falta de ingreso total o parcial de las cuotas, habiendo cumplido las obligaciones de solicitud y transmisión de liquidaciones

- Incumplir las obligaciones económicas derivadas de su colaboración obligatoria

- Formalizar la protección por accidentes de trabajo y enfermedades profesionales, incapacidad temporal o la protección por cese de actividad, en entidad distinta

- Falta de entrega o no transmisión de documentos precisos para solicitar y tramitar cualquier prestación, incluido el certificado de empresa

- Falta de solicitud de afiliación o alta en el Régimen Especial de Trabajadores Autónomos

- Falta de abono de prestaciones a las entidades por las empresas responsables de su pago

- Obtener o disfrutar indebidamente cualquier tipo de reducciones, bonificaciones o incentivos en relación las cuotas sociales

- Solicitud de afiliación o alta fuera de plazo de los trabajadores a su servicio cuando no medie actuación inspectora, o su no transmisión

- No comprobar los empresarios que contraten o subcontraten con otros la afiliación o alta de los trabajadores

- No proceder al alta y cotización por los salarios de tramitación y por las vacaciones devengadas y no disfrutadas antes de la extinción de la relación laboral

- No comunicar a la entidad gestora de la prestación por desempleo las medidas de despido colectivo o de suspensión o reducción de jornada

- Ocupar a beneficiarios de pensiones incompatibles con el trabajo por cuenta ajena

- Incumplir las entidades de formación u organizadoras los requisitos de las acciones formativas

- Ocupar a beneficiarios o solicitantes de pensiones incompatibles con el trabajo por cuenta ajena

- No ingresar ni liquidar las cuotas de Seguridad Social, o actuar fraudulentamente para eludir esa responsabilidad

- Falsear documentos o la connivencia con los trabajadores para la obtención o disfrute fraudulento de prestaciones de la Seguridad Social o eludir obligaciones

- Pactar con sus trabajadores que paguen cuotas a cargo del empresario, o su renuncia a derechos de Seguridad Social

- Incremento indebido de la base de cotización o simulación de la contratación laboral

- Efectuar deducciones o compensaciones fraudulentas en las cuotas

- No facilitar los datos identificativos de prestaciones sociales públicas

- Falsear documentos para obtener o disfrutar indebidamente de bonificaciones en materia de formación profesional para el empleo

- No suscribir el convenio especial de trabajadores con 55 o más años afectados por un despido colectivo

- Ocupar trabajadores afectados por la suspensión de contratos o reducción de jornada

- Retener o descontar de más indebidamente, y no ingresar en plazo, la parte de cuota de Seguridad Social de sus trabajadores

- Incumplir lo dispuesto en los Reglamentos de la Unión Europea sobre Coordinación de Sistemas de Seguridad Social, respecto a la determinación de la legislación de seguridad social aplicable, cuando dicho incumplimiento dé lugar a la inscripción o alta en el sistema de seguridad social español de empresas, trabajadores por cuenta ajena o por cuenta propia, o dé lugar a la falta de alta y cotización en el sistema de seguridad social español de personas desplazadas a España desde otro Estado Miembro de la UE.

AL [ÓRGANO AL QUE SE DIRIGE]

D./Dña. [NOMBRE Y APELLIDOS], con NIF/NIE número [DNI/NIE] y domicilio a efectos de notificaciones en [DOMICILIO A EFECTOS DE NOTIFICACIONES], actuando [ELEGIR: en su propio nombre / en nombre de ..., cuya representación acredita conforme a la escritura de poder cuya copia acompaña], como mejor proceda comparece y DICE:

Que el día [FECHA] me ha sido notificada la resolución sancionadora dictada por [ÓRGANO O PERSONA] en el expediente número [Nº DE EXPEDIENTE], y en la que se acuerda imponer a la empresa una multa de [IMPORTE] euros.

Que, contra dicha resolución, por considerarla no ajustada a Derecho, interpone RECURSO DE ALZADA en el plazo de un mes concedido al efecto, conforme establecen los artículos 23 del Real Decreto 928/1998, de 14 de mayo, por el que se aprueba el Reglamento General sobre Procedimientos para la Imposición de las Sanciones por Infracciones de Orden Social y para los Expedientes Liquidatorios de Cuotas de la Seguridad Social, y 122 de la Ley 39/2015, de 1 de octubre, del Procedimiento Administrativo Común de las Administraciones Públicas, en base a los siguientes hechos y fundamentos legales:

HECHOS

PRIMERO.- Que con fecha [FECHA] se dictó resolución sancionadora que tiene su origen en el acta de infracción número [NÚMERO], en la que se impone una multa de [IMPORTE] euros, ya que, de conformidad con el artículo
21
22
23.1
[NOMBRE Y APELLIDOS], del Real Decreto Legislativo 5/2000, de 4 de agosto, por el que se aprueba el texto refundido de la Ley sobre Infracciones y Sanciones en el Orden Social, los hechos descritos han sido calificados como constitutivos de la siguiente infracción

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

LEVE:

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

No conservar la documentación o los registros o soportes informáticos.

No exponer, poner a disposición o entregar los documentos de cotización.

No comunicar las bajas o variaciones de los trabajadores o su no transmisión por medios informáticos, electrónicos o telemáticos.

No cumplir el deber de información.

No comunicar el cambio en los documentos de asociación o de adhesión.

No remitir a la entidad las copias de los partes médicos de baja, confirmación de la baja o alta de incapacidad temporal facilitadas por los trabajadores, o no transmitirlos por medios informáticos, electrónicos o telemáticos.

GRAVE:

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

No solicitar la inscripción, no comunicar la apertura y cese de actividad de los centros de trabajo y demás variaciones, o su no transmisión.

No solicitar o solicitar fuera de plazo la afiliación inicial o el alta de los trabajadores a su servicio.

Falta de ingreso total o parcial de las cuotas, habiendo cumplido las obligaciones de solicitud y transmisión de liquidaciones.

Incumplir las obligaciones económicas derivadas de su colaboración obligatoria.

Formalizar la protección por accidentes de trabajo y enfermedades profesionales, incapacidad temporal o la protección por cese de actividad, en entidad distinta.

Falta de entrega o no transmisión de documentos precisos para solicitar y tramitar cualquier prestación, incluido el certificado de empresa.

Falta de solicitud de afiliación o alta en el Régimen Especial de Trabajadores Autónomos.

Falta de abono de prestaciones a las entidades por las empresas responsables de su pago.

Obtener o disfrutar indebidamente cualquier tipo de reducciones, bonificaciones o incentivos en relación las cuotas sociales.

Solicitud de afiliación o alta fuera de plazo de los trabajadores a su servicio cuando no medie actuación inspectora, o su no transmisión.

No comprobar los empresarios que contraten o subcontraten con otros la afiliación o alta de los trabajadores.

No proceder al alta y cotización por los salarios de tramitación y por las vacaciones devengadas y no disfrutadas antes de la extinción de la relación laboral.

No comunicar a la entidad gestora de la prestación por desempleo las medidas de despido colectivo o de suspensión o reducción de jornada.

Ocupar a beneficiarios de pensiones incompatibles con el trabajo por cuenta ajena.

Incumplir las entidades de formación u organizadoras los requisitos de las acciones formativas.

MUY GRAVE:

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

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

Incumplir lo dispuesto en los Reglamentos de la Unión Europea sobre Coordinación de Sistemas de Seguridad Social, respecto a la determinación de la legislación de seguridad social aplicable, cuando dicho incumplimiento dé lugar a la inscripción o alta en el sistema de seguridad social español de empresas, trabajadores por cuenta ajena o por cuenta propia, o dé lugar a la falta de alta y cotización en el sistema de seguridad social español de personas desplazadas a España desde otro Estado Miembro de la UE.

SEGUNDO.- Que en el acta de infracción más arriba referenciada y en el informe complementario posterior que sirven de fundamento a la resolución sancionadora, se reflejan unos hechos que no responden a la realidad de lo acaecido, al no describirse pormenorizadamente el supuesto comportamiento infractor, ni destacar cuáles son los hechos relevantes a efectos de la tipificación y graduación de la sanción. En concreto, los hechos tal y como sucedieron son los siguientes: [EXPONER LOS HECHOS].

TERCERO.- Que la calificación realizada en el expediente sancionador de los anteriores hechos no es conforme al ordenamiento jurídico puesto que no se dan los elementos objetivos y subjetivos de la infracción presuntamente cometida, en base a las siguientes razones:

A) En relación a los elementos objetivos de la infracción, los hechos reflejados en el acta de infracción no son ciertos, por cuanto que [MOTIVO].

[OPCIONAL — incluir si procede]

(Si no se refleja el nombre de los trabajadores en el acta)

Además, el acta de infracción nos causa una gran indefensión porque no refleja el nombre de las personas trabajadoras afectadas por la supuesta infracción que ha originado el acta, por lo que no podemos conocer con exactitud cuál ha sido el supuesto comportamiento infractor y, en consecuencia, proceder a desvirtuar tales afirmaciones.

[OPCIONAL — incluir si procede]

(Si el acta se limita a calificar los hechos de forma genérica)

Además, el acta de infracción califica genéricamente los hechos como [TIPIFICACIÓN DE LA INFRACCIÓN], sin describir pormenorizadamente la conducta realizada por el empresario, y no se aportan los elementos de juicio necesarios, dado lo escaso del relato, para que el órgano competente sancionador pueda adoptar su decisión, ni tampoco para que el inculpado pueda defenderse de unos hechos que no se describen con el detalle necesario para poder ser calificados como constitutivos de esta infracción, tal y como reiteradamente viene exigiendo la jurisprudencia de nuestro Tribunal Supremo.

B) En cuanto al elemento subjetivo, los hechos acaecidos no son susceptibles de incardinarse en la infracción administrativa tal y como se hizo en el acta de infracción, sino que en atención a lo sucedido y a las circunstancias de hechos concurrentes no existe culpabilidad del empresario.

CUARTO.- Que la sanción impuesta, consistente en el pago de una multa en cuantía de [IMPORTE] euros, vulnera el principio de proporcionalidad y demás principios que informan el ejercicio de la potestad sancionadora en materia de infracciones en el orden social, atendiendo al relato de hechos más arriba reseñado.

Que, para la demostración de las afirmaciones anteriormente manifestadas, se propone la práctica de los siguientes MEDIOS DE PRUEBA, que incomprensiblemente los órganos instructor y sancionador no admitieron con anterioridad a dictarse la resolución sancionadora: [PRUEBAS NO ADMITIDAS].

[OPCIONAL — incluir si procede]

Testifical, consistente en que se tome declaración a [NOMBRE Y APELLIDOS], en cuanto [ELEGIR: personas trabajadoras / clientes] y testigos presenciales de los hechos reflejados en el acta de infracción, por tener un conocimiento directo de los mismos en razón de su presencia física en el momento en que tuvo lugar la infracción presuntamente cometida.

[OPCIONAL — incluir si procede]

Documental, consistente en los escritos que se acompañan como números [Nº], consistentes en [DESCRIBIR], todos ellos necesarios para el conocimiento más preciso de los hechos reflejados en el acta de infracción, así como de las posibles responsabilidades.

A los anteriores hechos son de aplicación los siguientes

FUNDAMENTOS DE DERECHO

I.- Procede la interposición del presente recurso de alzada conforme establecen los artículos 54 del Real Decreto Legislativo 5/2000, de 4 de agosto, por el que se aprueba el texto refundido de la Ley sobre Infracciones y Sanciones en el Orden Social, 23 del Real Decreto 928/1998, de 14 de mayo, por el que se aprueba el Reglamento General sobre Procedimientos para la Imposición de las Sanciones por Infracciones de Orden Social y para los Expedientes Liquidatorios de Cuotas de la Seguridad Social, y 121 y 122 de la Ley 39/2015, de 1 de octubre, del Procedimiento Administrativo Común de las Administraciones Públicas.

II.-

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

La resolución sancionadora es nula de pleno derecho al ser dictada por un órgano manifiestamente incompetente, puesto que se ha firmado vulnerando lo establecido en el artículo 25.2 de la Ley 40/2015, de 1 de octubre, de Régimen Jurídico del Sector Público.

La resolución sancionadora es contraria al principio de tipicidad (artículos 25.1 de la Constitución, 27 de la Ley 40/2015, de 1 de octubre, de Régimen Jurídico del Sector Público, y 1.1 del Real Decreto Legislativo 5/2000, de 4 de agosto, por el que se aprueba el texto refundido de la Ley sobre Infracciones y Sanciones en el Orden Social), puesto que los hechos reflejados en el acta de infracción no se corresponden con el precepto que supone o implica la vulneración del ordenamiento ni tampoco con el precepto que tipifica tal infracción, por lo que en el expediente sancionador se ha realizado una aplicación analógica de la norma sancionadora que no comprende en su descripción a los hechos sancionados. En consecuencia, el acta de la Inspección infringe el artículo 53.1.b del citado Real Decreto Legislativo 5/2000, de 4 de agosto.

La resolución sancionadora no es correcta porque vulnera el derecho a la tutela judicial efectiva consagrado en el artículo 24.1 de la Constitución pues el acta de infracción no goza de la presunción legal de certeza del artículo 53.2 del Real Decreto Legislativo 5/2000, de 4 de agosto, por el que se aprueba el texto refundido de la Ley sobre Infracciones y Sanciones en el Orden Social, por realizar una descripción insuficiente o inadecuada de los hechos relevantes a los efectos de la tipificación de la infracción y graduación de la sanción y de los medios probatorios empleados. De la simple lectura del acta de infracción, resulta que en ésta no se consignan los hechos o circunstancias del caso con precisión, incurriendo en una obvia inconcreción al limitarse a realizar meras calificaciones jurídicas.

En el expediente sancionador se ha vulnerado el derecho a la presunción de inocencia proclamado en el artículo 24.2 de la Constitución, por cuanto que la carga de la prueba corresponde a la Administración y en ningún momento se ha probado la culpabilidad de la supuesta conducta infractora, no siendo posible destruir la mencionada presunción de inocencia mediante indicios, sospechas de culpabilidad o a través de una valoración subjetiva del derecho sancionador sin respaldo de pruebas de los hechos en que pudiera fundarse. Es evidente que en el acta de infracción no se reflejan los elementos trascendentales para el juicio de culpabilidad.

En el expediente administrativo sancionador se han vulnerado los derechos de defensa reconocidos a todos los ciudadanos en el artículo 24 de la Constitución, porque no se ha informado de la imputación de los hechos, de las infracciones y de las sanciones, así como del instructor y, en segundo lugar, porque no se han admitido a trámite las pruebas propuestas sin resolución motivada y las demás que sean conducentes para la comprobación de los hechos presuntamente infractores.

La resolución sancionadora no es correcta en cuanto que el acta de infracción infringe lo dispuesto en el artículo 14.1 del Real Decreto 928/1998, de 14 de mayo, por el que se aprueba el Reglamento general sobre procedimientos para la imposición de sanciones por infracciones de orden social y para los expedientes liquidatorios de cuotas de la Seguridad Social. En concreto, el acta de infracción adolece de las siguientes graves irregularidades formales que condicionan o menoscaban la defensa del imputado:

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

Omisión o error en la identificación del presunto sujeto infractor, así como en los datos societarios relevantes pues en el acta de infracción se hace constar [DATO CONSIGNADO EN EL ACTA].

Falta de consignación de los medios probatorios pues en el acta de infracción se hace constar [MEDIOS PROBATORIOS CONSIGNADOS], con la consiguiente inadecuación o insuficiencia.

Falta de consignación del funcionario que levanta el acta de infracción y firma del mismo.

Falta de consignación de la fecha del acta de infracción, que resulta necesario para el conocimiento y la defensa de cuándo se produjeron el presunto comportamiento infractor.

En el procedimiento sancionador se han infringido todos los trámites esenciales destinados a la comprobación efectiva y adecuada de los hechos, por lo que resulta vulnerado el artículo 21.1 de la Ley 23/2015, de 21 de julio, Ordenadora del Sistema de Inspección de Trabajo y Seguridad Social.

[ELEGIR UNA DE LAS ALTERNATIVAS QUE SIGUEN Y SUPRIMIR LAS DEMÁS]

Existe un excesivo lapso de tiempo entre los supuestos hechos infractores y la actuación inspectora que invalida el acta de infracción recurrida. Así, una inspección realizada en fecha [FECHA], no puede acreditar los hechos acaecidos en el pasado, en concreto en fecha [FECHA].

No existe una comprobación efectiva de los supuestos hechos infractores por cuanto que no se ha procedido a una comprobación in situ, sino en virtud de expediente administrativo.

El acta de la inspección de trabajo carece de eficacia probatoria, por tratarse de una deducción o conjetura, sin base fáctica objetiva, lo que resulta evidente de la comprobación efectuada.

Existe una falta de comprobación efectiva y adecuada de los hechos, al extenderse el acta sólo en base a declaraciones de las personas trabajadoras sedicentes contra el empresario, por lo que estamos ante un acta basada en pruebas parciales.

Téngase presente que el acta de la Inspección se basa en la denuncia de una sola persona trabajadora que, según manifestaciones de sus propios compañeros, presumía de que podía cerrar la empresa, resultando contradicha por la prueba testifical de las personas trabajadoras afectadas ante fedatario público, que tiene por ello relevancia a efectos de desvirtuar la presunción legal de certeza del acta de la Inspección.

III.–

[ELEGIR UNA OPCIÓN: Infracciones leves / Infracciones graves / Infracciones muy graves]

[OPCIONAL — incluir si procede]

IV.- La sanción impuesta vulnera el principio de proporcionalidad establecido en el artículo 39 del Real Decreto Legislativo 5/2000, de 4 de agosto, por el que se aprueba el texto refundido de la Ley sobre Infracciones y Sanciones en el Orden Social, puesto que no se adapta a la gravedad de la infracción, así como a las circunstancias de hecho concurrentes que no han sido tenidas en cuenta a la hora de graduar la multa infligida. Al no considerarse relevantes las circunstancias de graduación, la sanción debe imponerse en la cuantía inferior del grado mínimo, máxime cuando el acta de infracción no contiene una descripción detallada de tales circunstancias, incurriéndose en arbitrariedad y discrecionalidad impropia de un expediente administrativo sancionador.

En virtud de lo expuesto,

SOLICITA DE ESE que, tenga por interpuesto Recurso de Alzada con los documentos que se acompañan y, previa la práctica de las pruebas propuestas y la tramitación que proceda, dicte resolución en la que declare la invalidez de la resolución sancionadora impugnada y del acta de infracción, con el consiguiente archivo del expediente sancionador o, subsidiariamente y para el caso de no estimar la petición de archivo del expediente, disponga la reducción de la sanción inicialmente propuesta a la cuantía inferior de su grado mínimo, sin perjuicio de la interposición ulterior de los recursos procedentes.

Es de Justicia que pide en [LOCALIDAD].

D./Dña. [NOMBRE Y APELLIDOS]
