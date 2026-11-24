---
name: demanda-contra-mutua-reclamando-prestacion-cese-ss-006
description: "Demanda contra la mutua reclamando la prestación por cese de actividad de autónomos. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda contra la mutua reclamando la prestación por cese de actividad de autónomos

> Formulario **SS-006** del plugin **Seguridad Social: demandas y recursos ante lo social** (`formularios-seguridad-social-demandas`) · Seguridad Social › Demandas y escritos ante la jurisdicción social · normativa revisada el 24-11-2026.

## Qué es

Los órganos jurisdiccionales del orden social conocerán de las cuestiones litigiosas que se promuevan en materia de prestaciones de Seguridad Social, incluidas la protección por desempleo y la protección por cese de actividad de las personas trabajadoras por cuenta propia o autónomos (art. 2.o) de la LJS). La protección por cese de actividad se rige por lo dispuesto en los arts. 327 a 343 de la LGSS, y en sus normas de desarrollo, así como, supletoriamente, por las normas que regulan el régimen especial de la Seguridad Social de encuadramiento.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda contra la mutua reclamando la prestación por cese de actividad de autónomos» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda contra la mutua reclamando la prestación por cese de actividad de autónomos” para mi caso». También puedes invocarla directamente con `/formularios-seguridad-social-demandas:demanda-contra-mutua-reclamando-prestacion-cese-ss-006`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-seguridad-social-demandas:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Seguridad Social: demandas y recursos ante lo social) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (13 veces)
- [ ] IMPORTE (3 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] DENOMINACIÓN SOCIAL (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] PARTE DEMANDADA (2 veces)
- [ ] ACTIVIDAD
- [ ] CORREO ELECTRÓNICO
- [ ] DESCRIBIR
- [ ] DIRECCIÓN
- [ ] DNI/NIE
- [ ] EJERCICIO
- [ ] LUGAR
- [ ] Nº DE EXPEDIENTE
- [ ] SEDE
- [ ] TELÉFONO
- [ ] ÓRGANO ADMINISTRATIVO

## Normas que cita el formulario

- art. 331.1.a LGSS
- art. 331 LGSS
- art. 1 Ley 36/2011

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

- Junto a «…40 a 146 del mismo texto legal que regulan la reclamación administrativa previa.»: La reclamación previa es administrativa, no «judicial». En cese de actividad es potestativa (art. 350.1 LGSS) y, si se dirige a una mutua, informa una comisión paritaria (art. 350.2 LGSS). Fuente: art. 71 LRJS; art. 350 LGSS (red. RDL 28/2018); LRJS (Ley 36/2011), BOE-A-2011-15936; LGSS (RDLeg 8/2015), BOE-A-2015-11724.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Los órganos jurisdiccionales del orden social conocerán de las cuestiones litigiosas que se promuevan en materia de prestaciones de Seguridad Social, incluidas la protección por desempleo y la protección por cese de actividad de las personas trabajadoras por cuenta propia o autónomos (art. 2.o) de la LJS).

La protección por cese de actividad se rige por lo dispuesto en los arts. 327 a 343 de la LGSS, y en sus normas de desarrollo, así como, supletoriamente, por las normas que regulan el régimen especial de la Seguridad Social de encuadramiento.


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

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI nº [DNI/NIE], asistido/a por el/la Letrado/a [NOMBRE Y APELLIDOS], y con domicilio a efectos de notificaciones en su despacho sito en [LOCALIDAD], teléfono [TELÉFONO] y correo electrónico [CORREO ELECTRÓNICO], ante ese Tribunal comparezco y como mejor proceda en Derecho DIGO:

Que por medio del presente escrito formulo DEMANDA DE RECONOCIMIENTO DEL DERECHO A LA PRESTACIÓN POR CESE DE ACTIVIDAD DE TRABAJADORES AUTÓNOMOS contra [PARTE DEMANDADA] Mutua de Accidentes de Trabajo y Enfermedades Profesionales de la Seguridad Social nº [NÚMERO], en la persona de su legal representante, con domicilio en [LOCALIDAD].

Se apoya la presente demanda en los siguientes

HECHOS

PRIMERO.- Que soy trabajador/a autónomo/a, afiliado/a, en alta, y al corriente de pago en el Régimen Especial de la Seguridad Social de los Trabajadores por Cuenta Propia o Autónomos desde el pasado [FECHA], con una base de cotización mensual de [IMPORTE] euros y una base reguladora de [IMPORTE].

SEGUNDO.- Que he estado realizando la actividad de [ACTIVIDAD] desde [FECHA] hasta [FECHA], con un local abierto al público en [DIRECCIÓN], fecha en la que por motivos [DESCRIBIR] he tenido que cesar definitivamente en la actividad por ser inviable proseguir con la misma.

TERCERO.- Que con fecha [FECHA] solicité a la Mutua [DENOMINACIÓN SOCIAL] la prestación por cese de actividad, que me ha sido denegada por
[ELEGIR: Resolución / Acuerdo]
 de la citada Mutua con fecha [FECHA], expediente nº [Nº DE EXPEDIENTE].

Se acompañan como DOCS. Nº 1 y 2, copia de la solicitud de prestación y carta de denegación de la Mutua.

CUARTO.- Contra dicha comunicación de denegación interpuse reclamación previa a la vía judicial ante el órgano gestor, que fue desestimada por Resolución de fecha [FECHA], notificada el [FECHA], que confirma el Acuerdo de [FECHA].

Se adjunta copia de la reclamación previa como DOC. Nº 3 y Resolución de la Mutua como DOC. Nº 4

QUINTO.- Fundamenta la Mutua su denegación de la prestación en el hecho de que no se han acreditado las pérdidas alegadas y no se ha demostrado la inviabilidad del negocio según lo establecido en el art. 331.1.a) de la LGSS, extremo que es totalmente incierto ya que, como consta en el expediente, el demandante aportó justificante de cierre del establecimiento, la baja en el Censo tributario de empresarios, profesionales y retenedores y la baja en el RETA. Asimismo, constan aportadas las declaraciones del IRPF y del IVA del ejercicio [EJERCICIO] en la que se reflejan las pérdidas económicas alegadas y que son un fiel reflejo de la cuenta de pérdidas y ganancias del balance contable.

Todos estos se reflejan también en la declaración jurada aportada, cumpliéndose, por tanto, todos los requisitos legalmente establecidos en el apartado a) del art. 331 de la LGSS, para causar derecho a la prestación por cese de actividad solicitada, debiendo por tanto ser revocada la resolución/acuerdo de la Mutua por no ser ajustada a derecho.

SEXTO.- Por todo lo expuesto, teniendo el demandante derecho a la prestación que reclama, ha de estimarse la demanda y revocar la
[ELEGIR: Resolución / Acuerdo]
 de [ÓRGANO ADMINISTRATIVO] de fecha [FECHA] por infringir los arts. 329 y siguientes de la Ley General de la Seguridad Social.

FUNDAMENTOS DE DERECHO

I.- Es competente el Tribunal al que me dirijo en virtud de lo dispuesto en los artículos 1, 2, 6 y 10 de la Ley 36/2011, de 10 de octubre, reguladora de la Jurisdicción Social.

II.- Se cumplen todos los requisitos formales para la presentación de la presente demanda en virtud de lo dispuesto en el artículo 80 de la Ley reguladora de la jurisdicción social, así como en los artículos 71 y 140 a 146 del mismo texto legal que regulan la reclamación administrativa previa.

III.- En cuanto al fondo del asunto son aplicables los arts. 331.1.a), 332.1 y concordantes de la Ley General de la Seguridad Social.

Por lo expuesto,

SUPLICO AL TRIBUNAL que teniendo por presentado este escrito, con sus copias, se sirva admitirlo y, en su virtud, tenga por interpuesta DEMANDA DE RECONOCIMIENTO DEL DERECHO A LA PRESTACIÓN POR CESE DE ACTIVIDAD DE TRABAJADORES AUTÓNOMOS contra [PARTE DEMANDADA] Mutua de Accidentes de Trabajo y Enfermedades Profesionales de la Seguridad Social nº [NÚMERO], en la persona de su legal representante, citando a las partes para los trámites previos de conciliación y, en su caso, de juicio, concluyendo las actuaciones con una Sentencia en la que se revoque la Resolución/Acuerdo de dicho órgano gestor de fecha [FECHA] y se acuerde mi derecho a percibir la prestación por cese de mi actividad desde [FECHA] hasta [FECHA] conforme a una base reguladora de [IMPORTE] euros.

Por ser de Justicia que pido en [LUGAR], a [FECHA].

PRIMER OTROSI DIGO que se solicita la reclamación de oficio a la Mutua [DENOMINACIÓN SOCIAL] del expediente y antecedentes que posea en relación con el contenido de la demanda.

SEGUNDO OTROSI DIGO que esta parte acudirá al acto del juicio oral acompañada y asistida de Letrado.

TERCER OTROSI DIGO que interesa al Derecho de esta parte que se practiquen en el acto del juicio oral los siguientes:

MEDIOS DE PRUEBA

- DOCUMENTAL: la que esta parte aportará en el acto del juicio, así como la documental aportada con esta demanda y el expediente administrativo.

SUPLICO AL TRIBUNAL que tenga por hechas las anteriores manifestaciones y por propuesta la prueba, la admita y la estime pertinente.

Por ser de Justicia que reitero en el lugar y fecha "ut supra"

Fdo.: D./Dña. [NOMBRE Y APELLIDOS]
