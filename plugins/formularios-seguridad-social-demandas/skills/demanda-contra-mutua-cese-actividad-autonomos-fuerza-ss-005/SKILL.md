---
name: demanda-contra-mutua-cese-actividad-autonomos-fuerza-ss-005
description: "Demanda contra la mutua por cese de actividad de autónomos por fuerza mayor debido a la DANA de 2024. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda contra la mutua por cese de actividad de autónomos por fuerza mayor debido a la DANA de 2024

> Formulario **SS-005** del plugin **Seguridad Social: demandas y recursos ante lo social** (`formularios-seguridad-social-demandas`) · Seguridad Social › Demandas y escritos ante la jurisdicción social · normativa revisada el 24-11-2026.

## Qué es

Demanda ante el orden jurisdiccional social para que se reconozca el derecho a la prestación por cese de actividad por fuerza mayor de una persona trabajadora autónoma afectada por la DANA de 28 de octubre a 4 de noviembre de 2024, cuando la Mutua ha denegado la prestación y la reclamación previa ha sido desestimada.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda contra la mutua por cese de actividad de autónomos por fuerza mayor debido a la DANA de 2024» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda contra la mutua por cese de actividad de autónomos por fuerza mayor debido a la DANA de 2024” para mi caso». También puedes invocarla directamente con `/formularios-seguridad-social-demandas:demanda-contra-mutua-cese-actividad-autonomos-fuerza-ss-005`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-seguridad-social-demandas:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Seguridad Social: demandas y recursos ante lo social) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] DÍA, MES Y AÑO (12 veces)
- [ ] DENOMINACIÓN DE LA MUTUA (5 veces)
- [ ] IMPORTE (3 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] MUNICIPIO (2 veces)
- [ ] N.º DE MUTUA (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] ACTIVIDAD
- [ ] AÑO
- [ ] CORREO ELECTRÓNICO
- [ ] DIRECCIÓN COMPLETA DE LA MUTUA
- [ ] DIRECCIÓN COMPLETA DEL DESPACHO
- [ ] DNI/NIE
- [ ] DÍA
- [ ] FECHAS ENTRE EL 28 DE OCTUBRE Y EL 4 DE NOVIEMBRE DE 2024
- [ ] MES
- [ ] N.º DE EXPEDIENTE
- [ ] NOMBRE DEL LETRADO/A
- [ ] TELÉFONO

## Normas que cita el formulario

- art. 331.1.b LGSS
- art. 338 LGSS
- art. 24 Real Decreto-ley 6/2024
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

### Avisos de actualización (3) — se aplican en el texto, nunca se copian en el documento

- Junto a «…ANA) en diferentes municipios entre el 28 de octubre y el 4 de noviembre de 2024»: el original decía «art. 2413»; comprobar el artículo exacto del Real Decreto-ley 6/2024 en su redacción vigente
- Junto a «…veinticuatro meses inmediatamente anteriores a la situación de cese de actividad»: Redacción vigente del período mínimo (art. 338.1 LGSS desde 1-1-2023) y de las normas excepcionales (art. 24.3 RDL 6/2024, art. 6.3 RDL 20/2026, art. 39.3 RDL 22/2026). Fuente: art. 338.1 LGSS (red. RDL 13/2022); RDL 6/2024, BOE-A-2024-22928; RDL 20/2026, BOE-A-2026-16543; RDL 22/2026, BOE-A-2026-18429.
- Junto a «…ANA) en diferentes municipios entre el 28 de octubre y el 4 de noviembre de 2024»: comprobar el artículo exacto, véase hecho quinto

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

NOTAS DE USO (suprimir antes de presentar):

Los órganos jurisdiccionales del orden social conocen de las cuestiones litigiosas que se promuevan en materia de prestaciones de Seguridad Social, incluidas la protección por desempleo y la protección por cese de actividad de las personas trabajadoras por cuenta propia o autónomas (art. 2.o) de la Ley 36/2011, reguladora de la jurisdicción social, LRJS).

La protección por cese de actividad se rige por los arts. 327 a 343 de la Ley General de la Seguridad Social (LGSS) y sus normas de desarrollo y, supletoriamente, por las normas que regulan el régimen especial de la Seguridad Social de encuadramiento.

Las personas trabajadoras por cuenta propia o autónomas pueden solicitar la prestación por cese de actividad por fuerza mayor ante su mutua sin necesidad de contar con la cotización mínima exigida para acceder a ella y sin necesidad de acreditar, en el momento de la solicitud, la imposibilidad de desarrollar la actividad, todo ello como consecuencia directa e inmediata de los siniestros descritos en el artículo 1 del Real Decreto-ley 6/2024, producidos en alguna de las localidades del anexo de dicho Real Decreto-ley.


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

A LA SECCIÓN DE LO SOCIAL DEL TRIBUNAL DE INSTANCIA DE [LOCALIDAD]

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI n.º [DNI/NIE], asistido/a por el/la Letrado/a [NOMBRE DEL LETRADO/A], y con domicilio a efectos de notificaciones en su despacho sito en [DIRECCIÓN COMPLETA DEL DESPACHO], teléfono [TELÉFONO] y correo electrónico [CORREO ELECTRÓNICO], ante ese Tribunal comparezco y como mejor proceda en Derecho

DIGO:

Que por medio del presente escrito formulo DEMANDA DE RECONOCIMIENTO DEL DERECHO A LA PRESTACIÓN POR CESE DE ACTIVIDAD DE TRABAJADORES AUTÓNOMOS contra [DENOMINACIÓN DE LA MUTUA] de Accidentes de Trabajo y Enfermedades Profesionales de la Seguridad Social n.º [N.º DE MUTUA], en la persona de su legal representante, con domicilio en [DIRECCIÓN COMPLETA DE LA MUTUA].

Se apoya la presente demanda en los siguientes

HECHOS

PRIMERO.- Que soy trabajador/a autónomo/a, afiliado/a, en alta y al corriente de pago en el Régimen Especial de la Seguridad Social de los Trabajadores por Cuenta Propia o Autónomos desde el pasado [DÍA, MES Y AÑO], con una base de cotización mensual de [IMPORTE] euros y una base reguladora de [IMPORTE] euros.

SEGUNDO.- Que he estado realizando la actividad de [ACTIVIDAD] desde [DÍA, MES Y AÑO] hasta [DÍA, MES Y AÑO], fecha en la que, como consecuencia de la DANA acaecida en [MUNICIPIO] los días [FECHAS ENTRE EL 28 DE OCTUBRE Y EL 4 DE NOVIEMBRE DE 2024], he tenido que cesar [ELEGIR: parcialmente / totalmente] de forma [ELEGIR: temporal / definitiva] en mi actividad profesional, ya que [EXPLICAR LOS DAÑOS, LAS CONSECUENCIAS Y LOS MOTIVOS POR LOS QUE ES IMPOSIBLE CONTINUAR CON LA ACTIVIDAD].

TERCERO.- Que con fecha [DÍA, MES Y AÑO] solicité a la Mutua [DENOMINACIÓN DE LA MUTUA] la prestación por cese de actividad derivada de fuerza mayor prevista en el art. 331.1.b) de la LGSS, que me ha sido denegada por [ELEGIR: Resolución / Acuerdo] de la citada Mutua de fecha [DÍA, MES Y AÑO], expediente n.º [N.º DE EXPEDIENTE], en base a

[OPCIONAL — incluir si procede]

que no he acreditado la imposibilidad para desarrollar la actividad.

[OPCIONAL — incluir si procede]

que no he acreditado el período mínimo de cotización establecido en el art. 338 de la LGSS.

Se acompañan como DOCS. N.º 1 y 2 copia de la solicitud de prestación y carta de denegación de la Mutua.

CUARTO.- Contra dicha comunicación de denegación interpuse reclamación previa a la vía judicial ante el órgano gestor, que fue desestimada por Resolución de fecha [DÍA, MES Y AÑO], notificada el [DÍA, MES Y AÑO], que confirma el [ELEGIR: Acuerdo / Resolución] de [DÍA, MES Y AÑO].

Se adjunta copia de la reclamación previa como DOC. N.º 3 y Resolución de la Mutua como DOC. N.º 4.

QUINTO.- Que la resolución de la Mutua no es ajustada a Derecho toda vez que, en virtud de lo establecido en el art. 24 del Real Decreto-ley 6/2024, de 5 de noviembre, por el que se adoptan medidas urgentes de respuesta ante los daños causados por la Depresión Aislada en Niveles Altos (DANA) en diferentes municipios entre el 28 de octubre y el 4 de noviembre de 2024 , los trabajadores autónomos que cesen total o parcialmente, de forma definitiva o temporal, en su actividad como consecuencia directa e inmediata de los daños causados por la DANA en el municipio de [MUNICIPIO] entre el 28 de octubre y el 4 de noviembre de 2024

[OPCIONAL — incluir si procede]

no necesitan aportar documentos que acrediten la existencia de fuerza mayor.

[OPCIONAL — incluir si procede]

en estos casos se considerará cumplido el requisito de período mínimo de cotización de doce meses comprendidos en los veinticuatro meses inmediatamente anteriores a la situación de cese de actividad .

SEXTO.- Por todo lo expuesto, teniendo el demandante derecho a la prestación que reclama, ha de estimarse la demanda y revocar la [ELEGIR: Resolución / Acuerdo] de [DENOMINACIÓN DE LA MUTUA] de fecha [DÍA, MES Y AÑO] por infringir los arts. 329 y siguientes de la Ley General de la Seguridad Social.

FUNDAMENTOS DE DERECHO

I.- Es competente el Tribunal al que me dirijo en virtud de lo dispuesto en los artículos 1, 2, 6 y 10 de la Ley 36/2011, de 10 de octubre, reguladora de la Jurisdicción Social.

II.- Se cumplen todos los requisitos formales para la presentación de la presente demanda en virtud de lo dispuesto en el artículo 80 de la Ley reguladora de la jurisdicción social, así como en los artículos 71 y 140 a 146 del mismo texto legal, que regulan el trámite de reclamación previa.

III.- En cuanto al fondo del asunto son aplicables los arts. 331.1.b), 332.1 y concordantes de la Ley General de la Seguridad Social, y el art. 24 del Real Decreto-ley 6/2024, de 5 de noviembre, por el que se adoptan medidas urgentes de respuesta ante los daños causados por la Depresión Aislada en Niveles Altos (DANA) en diferentes municipios entre el 28 de octubre y el 4 de noviembre de 2024 .

Por lo expuesto,

SUPLICO AL TRIBUNAL que, teniendo por presentado este escrito, con sus copias, se sirva admitirlo y, en su virtud, tenga por interpuesta DEMANDA DE RECONOCIMIENTO DEL DERECHO A LA PRESTACIÓN POR CESE DE ACTIVIDAD DE TRABAJADORES AUTÓNOMOS contra [DENOMINACIÓN DE LA MUTUA] de Accidentes de Trabajo y Enfermedades Profesionales de la Seguridad Social n.º [N.º DE MUTUA], en la persona de su legal representante, citando a las partes para los trámites previos de conciliación y, en su caso, de juicio, concluyendo las actuaciones con una Sentencia en la que se revoque la [ELEGIR: Resolución / Acuerdo] de dicho órgano gestor de fecha [DÍA, MES Y AÑO] y se acuerde mi derecho a percibir la prestación por cese de mi actividad por fuerza mayor desde [DÍA, MES Y AÑO] hasta [DÍA, MES Y AÑO], conforme a una base reguladora de [IMPORTE] euros.

Por ser de Justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

PRIMER OTROSÍ DIGO que se solicita la reclamación de oficio a la Mutua [DENOMINACIÓN DE LA MUTUA] del expediente y antecedentes que posea en relación con el contenido de la demanda.

SEGUNDO OTROSÍ DIGO que esta parte acudirá al acto del juicio oral acompañada y asistida de Letrado.

TERCER OTROSÍ DIGO que interesa al Derecho de esta parte que se practiquen en el acto del juicio oral los siguientes

MEDIOS DE PRUEBA

DOCUMENTAL: la que esta parte aportará en el acto del juicio, así como la documental aportada con esta demanda y el expediente administrativo.

SUPLICO AL TRIBUNAL que tenga por hechas las anteriores manifestaciones y por propuesta la prueba, la admita y la estime pertinente.

Por ser de Justicia que reitero en el lugar y fecha «ut supra».

Fdo. D./Dña. [NOMBRE Y APELLIDOS]
