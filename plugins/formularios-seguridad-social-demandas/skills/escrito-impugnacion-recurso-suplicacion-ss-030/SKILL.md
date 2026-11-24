---
name: escrito-impugnacion-recurso-suplicacion-ss-030
description: "Escrito de impugnación del recurso de suplicación. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito de impugnación del recurso de suplicación

> Formulario **SS-030** del plugin **Seguridad Social: demandas y recursos ante lo social** (`formularios-seguridad-social-demandas`) · Seguridad Social › Demandas y escritos ante la jurisdicción social · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito de impugnación del recurso de suplicación» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito de impugnación del recurso de suplicación” para mi caso». También puedes invocarla directamente con `/formularios-seguridad-social-demandas:escrito-impugnacion-recurso-suplicacion-ss-030`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-seguridad-social-demandas:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Seguridad Social: demandas y recursos ante lo social) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] LOCALIDAD (7 veces)
- [ ] FECHA (3 veces)
- [ ] NOMBRE DE LA PARTE (3 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] Nº (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] COLEGIO
- [ ] LUGAR
- [ ] MOTIVO
- [ ] Nº DE ARTÍCULO
- [ ] Nº DE PROCEDIMIENTO
- [ ] Nº DE RESOLUCIÓN

## Normas que cita el formulario

- art. 197 LRJS
- art. 197 Ley 36/2011
- art. 193 LRJS
- art. 97.2 LRJS
- art. 196.3 LRJS
- art. 235 LRJS

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

A LA SECCIÓN DE LO SOCIAL DEL TRIBUNAL DE LA INSTANCIA NÚM. DE PARA ANTE LA SALA DE LO SOCIAL DEL TRIBUNAL SUPERIOR DE JUSTICIA DE [LOCALIDAD]
ANTECEDENTES
FUNDAMENTACIÓN PROCESAL
MOTIVOS JURÍDICOS DE IMPUGNACIÓN
Firmas

En virtud del art. 197 LRJS, interpuesto el recurso de suplicación en tiempo y forma, el Letrado de la Administración de Justicia proveerá en el plazo de 2 días dando traslado del mismo para su impugnación, a la parte o partes recurridas por un plazo común de 5 días para todas ellas. En los escritos de impugnación, podrán alegarse motivos de inadmisibilidad del recurso, así como eventuales rectificaciones de hecho o causas de oposición subsidiarias aunque no hubieran sido estimadas en la sentencia.

Del escrito o escritos de impugnación se dará traslado a las partes. De haberse formulado en dichos escritos alegaciones sobre inadmisibilidad del recurso o los motivos a que se refiere el párrafo anterior, las demás partes podrán presentar directamente sus alegaciones al respecto, dentro de los 2 días siguientes a recibir el traslado del escrito de impugnación.

Transcurrido el plazo de impugnación, y en su caso el de alegaciones del párrafo anterior, háyanse presentado o no escritos en tal sentido y previo traslado de las alegaciones si se hubieran presentado, se elevarán los autos a la Sala de lo Social del Tribunal Superior de Justicia, junto con el recurso y escritos presentados, dentro de los 2 días siguientes.

A LA SECCIÓN DE LO SOCIAL DEL TRIBUNAL DE LA INSTANCIA NÚM. DE [LOCALIDAD] PARA ANTE LA SALA DE LO SOCIAL DEL TRIBUNAL SUPERIOR DE JUSTICIA DE [LOCALIDAD]

D./Dña. [NOMBRE Y APELLIDOS] Letrado/a del Ilustre Colegio de Abogados de [COLEGIO], con domicilio profesional en [LOCALIDAD], en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS] según consta acreditado en el procedimiento nº [Nº DE PROCEDIMIENTO] de la Sección de lo Social del Tribunal de Instancia nº [NÚMERO] de [LOCALIDAD] ante la Sala comparezco y como mejor proceda en Derecho DIGO:

Que con fecha [FECHA], se nos ha notificado providencia por medio de la cual se nos da traslado del escrito de formalización del recurso de suplicación interpuesto por D./Dña. [NOMBRE Y APELLIDOS] contra la sentencia del procedimiento y Tribunal arriba referenciado, al mismo tiempo que se nos confiere un plazo de cinco días para su impugnación conforme al artículo 197 de la Ley 36/2011, de 10 de octubre, reguladora de la jurisdicción social.

Que mediante el presente escrito y dentro del plazo legal vengo a formular IMPUGNACIÓN DEL RECURSO DE SUPLICACIÓN presentado de contrario, en base a los siguientes antecedentes, fundamentación procesal y motivos jurídicos de impugnación

ANTECEDENTES

Se dan aquí por reproducidos los que como tales constan en la Sentencia de Instancia recurrida.

FUNDAMENTACIÓN PROCESAL

Se encuentra en el artículo 197 de la Ley 36/2011, de 10 de octubre, Reguladora de la Jurisdicción Social, presentándose esta impugnación con la firma del Letrado/a que suscribe, habiéndose cumplimentado el requisito atinente a señalar domicilio de la recurrida en el propio Despacho profesional de quien suscribe, en el mismo lugar de la Sede de esa Ilma. Sala de lo Social del Tribunal Superior de Justicia de Madrid.

MOTIVOS JURÍDICOS DE IMPUGNACIÓN

IMPUGNACIÓN AL MOTIVO PRIMERO

De contrario se plantea como primer motivo de recurso, el establecido en el apartado a) del artículo 193 LRJS para reponer los autos al momento de producirse infracción de normas que causen indefensión, por infracción del art. y [Nº DE ARTÍCULO].

No hay fundamentación alguna en el recurso, ni motivo alguno, que sea causa de nulidad de lo actuado, por lo que el motivo primero del recurso debe ser desestimado.

IMPUGNACIÓN AL MOTIVO SEGUNDO

De contrario se plantea como primer motivo de recurso el establecido en el apartado b) del artículo 193 LRJS para la revisión del Hecho Probado [Nº] de la sentencia en base a la prueba documental practicada.

Es necesario, atendiendo a reiterada doctrina judicial, para que pueda operar la revisión de los hechos declarados probados propuesta por las partes que concurran los siguientes requisitos (STSJ Madrid de 17 de enero de 2002):

a) Ha de devenir trascendente a efectos de la solución del litigio, con propuesta de texto alternativo o nueva redacción que al hecho probado tildado de erróneo pudiera corresponder y basada en documento auténtico o prueba pericial que, debidamente identificado y obrante en autos, patentice, de manera clara, evidente y directa, de forma contundente e incuestionable, sin necesidad de acudir a hipótesis, conjeturas, suposiciones o argumentaciones más o menos lógicas, naturales o razonables, el error en que hubiera podido incurrir el juzgador, cuya facultad de apreciación conjunta y según las reglas de la sana critica, (artículo 97.2 LRJS) no puede verse afectada por valoraciones o conclusiones distintas efectuadas por parte interesada. Es al juez de instancia, cuyo conocimiento directo del asunto garantiza el principio de inmediación del proceso laboral, a quien corresponde apreciar los elementos de convicción -concepto más amplio que el de medios de prueba- para establecer la verdad procesal intentando su máxima aproximación a la verdad real, valorando, en conciencia y según las reglas de la sana crítica, la prueba practicada.
b) La revisión pretendida sólo puede basarse en las pruebas documentales o periciales sin que sea admisible su invocación genérica, y sin que las declaraciones de las partes o de testigos sea hábiles para alcanzar la revisión fáctica en el extraordinario recurso de suplicación.
c) El juzgador ha de abstenerse de consignar en la relación de hechos probados cualquier anticipación de conceptos de derecho, que tienen su lugar reservado en la fundamentación jurídica.
d) La alegación de carencia de elementos probatorios eficaces, denominada por la doctrina "obstrucción negativa", resulta completamente inoperante para la revisión de los hechos probados en suplicación ante la facultad otorgada al magistrado de apreciar los elementos de convicción.
e) La revisión pretendida debe ser trascendente para el sentido del fallo, esto es, influir en la variación de la parte dispositiva de la sentencia, y no puede fundarse en hechos nuevos no tratados ante la Sección de lo Social del Tribunal de Instancia.

De los términos de la redacción fáctica solicitada ha de quedar excluido:

a) Todo lo que no sea un dato en sí, como los preceptos de normas reglamentarias de carácter interno o del convenio colectivo aplicable, y, en definitiva, cualquier concepto jurídico.
b) Los hechosnotorios y los conformes.
c) Los juicios de valor predeterminantes del fallo, cuya sede ha de corresponderse con la motivación o fundamentación jurídica del recurso.
d) Las hipótesis, conjeturas o elucubraciones, pues lo no acontecido, por posible, probable o incluso seguro que pudiera resultar llegar a ser, de darse las condiciones correspondientes, no ha llegado a ser, y debe quedar fuera de esa relación.

De lo anterior se deduce que no se cumplen, en el recurso de suplicación planteado por la recurrente, los requisitos necesarios para modificar los hechos declarados probados en la sentencia de instancia ya que [MOTIVO].

Además, la referencia indeterminada e indiscriminada a una documentación, produce la cita que se considera "en masa". Situación que no cumple los requisitos establecidos por la jurisprudencia de la Sala de lo Social de Tribunal Supremo (TS). Los Tribunales parten en tal sentido de lo establecido en el art. 196.3, de la LRJS, y donde se fija que aquellos que pretendan tener efectos revisorios, han de señalarse de "manera suficiente para que sean identificados". En ese mismo orden de cosas, destacaremos, a título de ejemplo ya que es unánime el TS en este punto, la sentencia de 11-6-2019, rec. 132/2018; donde recuerda que a estos fines es necesario reseñar cual o cuales así lo evidencian sin que sea suficiente una genérica remisión a la prueba documental practicada. Más concreta aun es la anterior de 22-3-2002, rec. 1170/2001, al destacar que el recurrente debe mencionar: "el punto específico que ponga de relieve el error alegado, razonando la pertinencia del motivo que muestre la correspondencia entre el contenido del documento y ofrezca la redacción -- por modificación o adición - que se pretende"; lo que no cumple, si: "se alude a numerosos documentos, muchos de ellos, de contenido muy similar, sin identificar en concreto cuál de ellos, evidencia el supuesto error del juzgador".

Por lo tanto, la modificación propuesta por la recurrente al Hecho [Nº], pretendiendo la adición de un nuevo párrafo, carece de toda fundamentación y tampoco se dice cuál es el documento o pericia en que se basa la pretendida modificación, por lo que debe de ser desestimado este motivo de recurso.

IMPUGNACIÓN AL MOTIVO TERCERO

Se plantea de contrario como segundo motivo de recurso el establecido en el apartado c) del artículo 193 LRJS por infracción de los arts. y la jurisprudencia que los desarrolla.

La sentencia recurrida no ha vulnerado ninguna de las normas alegadas por el recurrente ni ha realizado ninguna interpretación errónea de las mismas como reiteradamente se afirma en el escrito de recurso.

Conviene matizar que el recurso de suplicación se configura como de naturaleza extraordinaria, casi casacional, de objeto limitado, en el que el tribunal "ad quem" no puede valorar "ex novo" toda la prueba practicada ni revisar el Derecho aplicable, sino que debe limitarse a las concretas cuestiones planteadas por las partes, (SSTC 18/1993 y 294/1993), lo que no obsta a reconocer que se haya evolucionado hacia la consideración de oficio de determinados temas como son la insuficiencia de hechos probados y los defectos procesales, procedente contra las resoluciones y por las causas o motivos limitativamente tasados o seleccionados por el legislador. De donde se sigue que, a diferencia de lo que ocurre en la apelación civil, recurso este de carácter ordinario, no existe en el proceso laboral una doble instancia que permita traer la cuestión objeto de la resolución impugnada al pleno conocimiento de un órgano superior, sino que el sistema de recursos viene inspirado, según el legislador, por el principio de doble grado jurisdiccional.

Las Secciones de lo Social de los Tribunales de Instancia vienen diseñados como órganos de acceso a la prestación jurisdiccional en primera y única instancia, no habiéndose incorporado al orden jurisdiccional laboral la figura de la apelación. Las sentencias de esos órganos unipersonales podrán ser recurribles en suplicación ante los Tribunales Superiores de Justicia y sólo ante ellos, con lo que se cumple, y en términos rigurosos, la previsión constitucional de culminar la organización judicial en el ámbito territorial de la Comunidad Autónoma.

La sentencia recurrida recoge los hechos que estima probados en términos precisos y claros, y de forma adecuada para la formulación del propio fallo y suficiente para que el Tribunal pueda resolver el recurso.

El recurso planteado por la recurrente pretende que el Tribunal Superior dicte una nueva sentencia, no porque la resolución de instancia haya infringido alguna norma que pueda incardinarse en alguna de las causas previstas en el art. 193 de la LRJS para poder recurrir en suplicación, sino porque la misma no contiene un fallo que responda a sus intereses. Bajo la forma del recurso de suplicación lo que el contrario realmente realiza es una copia de la demanda y pretende que se vuelva a juzgar lo ya juzgado. Su intención, sin base jurídica alguna que lo justifique, es que se modifiquen los fundamentos jurídicos y la valoración conjunta que el juzgador ha hecho de la prueba y, consecuentemente, se modifique el fallo. En definitiva, lo que la recurrente pretende es que se dicte una nueva sentencia conforme a sus intereses y conforme a su criterio, no al del Juzgador.

Los Fundamentos de Derecho de la Sentencia, que resuelven el fondo del pleito, y al que la juzgadora de instancia dedica varios folios, hace una exposición detallada, exhaustiva y contundente, sobre la calificación de los hechos y el derecho aplicable al caso objeto de debate y las normas en las que apoya su resolución.

No procede, por todo lo expuesto, acoger el segundo motivo de recurso.

Por todo cuanto antecede,

SUPLICO A LA SECCIÓN DE LO SOCIAL DEL TRIBUNAL DE INSTANCIA que teniendo por presentado este escrito, se sirva admitirlo y, en su virtud, tenga por evacuado el trámite otorgado y, en mérito a lo expuesto en el cuerpo del mismo, por impugnado el recurso de suplicación formalizado por [NOMBRE DE LA PARTE] y eleve, previos los trámites que procedan, estas actuaciones a la Sala de lo Social del Tribunal Superior de Justicia de [LOCALIDAD].

Y de igual forma,

SUPLICO A LA SALA DE LO SOCIAL DEL TRIBUNAL SUPERIOR DE JUSTICIA DE que, teniendo por impugnado en tiempo y forma por parte de [NOMBRE DE LA PARTE] el recurso de suplicación presentado y formalizado por [NOMBRE DE LA PARTE] frente a la Sentencia nº [Nº DE RESOLUCIÓN] de la Sección de lo Social del Tribunal de Instancia nº [NÚMERO] de [LOCALIDAD] de fecha [FECHA], y previos los trámites legales oportunos, dicte Sentencia en la que se desestime íntegramente el Recurso de Suplicación y se confirme, en todos sus extremos, la sentencia recurrida, y se condene en costas al recurrente en virtud de lo establecido en el art. 235 de la LRJS.

Es justicia que pido en [LUGAR], a [FECHA].
