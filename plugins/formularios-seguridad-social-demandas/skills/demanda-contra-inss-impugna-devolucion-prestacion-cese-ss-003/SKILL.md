---
name: demanda-contra-inss-impugna-devolucion-prestacion-cese-ss-003
description: "Demanda contra el INSS que impugna la devolución de la prestación de cese de actividad (COVID-19). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda contra el INSS que impugna la devolución de la prestación de cese de actividad (COVID-19)

> Formulario **SS-003** del plugin **Seguridad Social: demandas y recursos ante lo social** (`formularios-seguridad-social-demandas`) · Seguridad Social › Demandas y escritos ante la jurisdicción social · normativa revisada el 24-11-2026.

## Qué es

Este formulario de demanda está diseñado para que los trabajadores autónomos presenten una impugnación contra el Instituto Nacional de la Seguridad Social (INSS) en relación con la devolución de ingresos percibidos como prestación de cese de actividad durante la pandemia de COVID-19. La situación surge principalmente a raíz de discrepancias sobre los cálculos y criterios utilizados por el INSS para solicitar la devolución de prestaciones ya abonadas.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda contra el INSS que impugna la devolución de la prestación de cese de actividad (COVID-19)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda contra el INSS que impugna la devolución de la prestación de cese de actividad (COVID-19)” para mi caso». También puedes invocarla directamente con `/formularios-seguridad-social-demandas:demanda-contra-inss-impugna-devolucion-prestacion-cese-ss-003`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-seguridad-social-demandas:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Seguridad Social: demandas y recursos ante lo social) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (12 veces)
- [ ] DENOMINACIÓN SOCIAL (4 veces)
- [ ] IMPORTE (3 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] MOTIVO (2 veces)
- [ ] NÚMERO (2 veces)
- [ ] COLEGIO
- [ ] CORREO ELECTRÓNICO
- [ ] DNI/NIE
- [ ] EPÍGRAFE DE ALTA
- [ ] LUGAR
- [ ] Nº DE COLEGIADO/A
- [ ] SEDE
- [ ] TELÉFONO

## Normas que cita el formulario

- art. 17 Ley 8/2020
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

Este formulario de demanda está diseñado para que los trabajadores autónomos presenten una impugnación contra el Instituto Nacional de la Seguridad Social (INSS) en relación con la devolución de ingresos percibidos como prestación de cese de actividad durante la pandemia de COVID-19. La situación surge principalmente a raíz de discrepancias sobre los cálculos y criterios utilizados por el INSS para solicitar la devolución de prestaciones ya abonadas.


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

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con DNI nº [DNI/NIE], asistido/a por el/la Letrado/a [NOMBRE Y APELLIDOS], colegiado/a nº [Nº DE COLEGIADO/A] del Ilustre Colegio de Abogados de [COLEGIO] y con domicilio a efectos de notificaciones en su despacho sito en [LOCALIDAD], teléfono [TELÉFONO] y correo electrónico [CORREO ELECTRÓNICO], ante ese Tribunal comparezco y como mejor proceda en Derecho DIGO:

Que por medio del presente escrito formulo DEMANDA DE IMPUGNACIÓN DE DEVOLUCIÓN DE INGRESOS DE LA PRESTACIÓN POR CESE DE ACTIVIDAD DE TRABAJADORES AUTÓNOMOS DURANTE EL COVID-19 contra el INSTITUTO NACIONAL DE LA SEGURIDAD SOCIAL, la TESORERÍA GENERAL DE LA SEGURIDAD SOCIAL y [DENOMINACIÓN SOCIAL] Mutua de Accidentes de Trabajo y Enfermedades Profesionales de la Seguridad Social nº [NÚMERO], con domicilio en [LOCALIDAD], en la persona de sus legales representantes.

Se apoya la presente demanda en los siguientes

HECHOS

PRIMERO.- Que soy trabajador/a autónomo/a,

afiliado/a, en alta, y al corriente de pago en el Régimen Especial de la Seguridad Social de los Trabajadores por Cuenta Propia o Autónomos (RETA) desde el pasado [FECHA],

estando dado de alta en el Régimen Especial de la Seguridad Social de los Trabajadores por Cuenta Propia o Autónomos desde [FECHA]. hasta [FECHA] con una base de cotización mensual de [IMPORTE] euros y una base reguladora de [IMPORTE], y de alta en el epígrafe [EPÍGRAFE DE ALTA].

SEGUNDO.- Que con fecha [FECHA] solicité a la Mutua [DENOMINACIÓN SOCIAL] la prestación extraordinaria por cese de actividad como consecuencia de la declaración del estado de alarma por la COVID-19.

TERCERO.- Mediante Resolución de fecha [FECHA], y conforme al art. 17 del Real Decreto Ley 8/2020, de 17 de marzo, de medidas urgentes extraordinarias para hacer frente al impacto económico y social del COVID-19.

Se acompañan como DOCS. Nº 1 y 2, copia de la solicitud de prestación y resolución de la Mutua.

CUARTO.- Con fecha [FECHA], el INSS me ha notificado Resolución de fecha [FECHA] por la que me reclama la devolución de la prestación reconocida, por importe de [IMPORTE] euros, al considerar supuestamente incumplidos los requisitos para su percepción, alegando que [MOTIVO].

QUINTO.- Contra dicha comunicación de denegación interpuse reclamación previa a la vía judicial ante el órgano gestor, que fue desestimada por Resolución de fecha [FECHA], notificada el [FECHA], que confirma el Acuerdo de [FECHA].

Se adjunta copia de la reclamación previa como DOC. Nº 3 y Resolución de la Mutua/INSS como DOC. Nº 4

SEXTO.- La Resolución del INSS no es ajustada a Derecho por cuanto [MOTIVO], por lo que debe ser totalmente revocada.

FUNDAMENTOS DE DERECHO

I.- Es competente el Tribunal al que me dirijo en virtud de lo dispuesto en los artículos 1, 2, 6 y 10 de la Ley 36/2011, de 10 de octubre, reguladora de la Jurisdicción Social.

II.- Se cumplen todos los requisitos formales para la presentación de la presente demanda en virtud de lo dispuesto en el artículo 80 de la Ley reguladora de la jurisdicción social, así como en los artículos 71 y 140 a 146 del mismo texto legal que regulan la reclamación administrativa previa.

III.- En cuanto al fondo del asunto es aplicable el arts. 17 y concordantes del Real Decreto Ley 8/2020 de 17 de marzo, de medidas urgentes extraordinarias para hacer frente al impacto económico y social del COVID-19 y normas concordantes.

Por lo expuesto,

SUPLICO AL TRIBUNAL que, teniendo por presentado este escrito con los documentos que lo acompañan, lo admita y, en su virtud, tenga por interpuesta DEMANDA DE IMPUGNACIÓN DE DEVOLUCIÓN DE INGRESOS DE LA PRESTACIÓN POR CESE DE ACTIVIDAD DE TRABAJADORES AUTÓNOMOS DURANTE EL COVID-19 contra el INSS; la TGSS y [DENOMINACIÓN SOCIAL] Mutua de Accidentes de Trabajo y Enfermedades Profesionales de la Seguridad Social nº [NÚMERO], citando a las partes para los trámites previos de conciliación y, en su caso, juicio, concluyendo las actuaciones con una Sentencia en la que se revoque la Resolución/Acuerdo del órgano gestor de fecha [FECHA] acordando que no procede devolver cantidad alguna por la prestación por cese de actividad percibida como consecuencia del COVID-19, con lo que demás proceda en Derecho.

Por ser de Justicia que pido en [LUGAR], a [FECHA].

PRIMER OTROSI DIGO que se solicita la reclamación de oficio a la Mutua [DENOMINACIÓN SOCIAL] y al INSS del expediente y antecedentes que posea en relación con el contenido de la demanda.

SEGUNDO OTROSI DIGO que esta parte acudirá al acto del juicio oral acompañada y asistida de Letrado.

TERCER OTROSI DIGO que interesa al Derecho de esta parte que se practiquen en el acto del juicio oral los siguientes:

MEDIOS DE PRUEBA

- DOCUMENTAL: la que esta parte aportará en el acto del juicio, así como la documental aportada con esta demanda y el expediente administrativo.

SUPLICO AL TRIBUNAL que tenga por hechas las anteriores manifestaciones y por propuesta la prueba, la admita y la estime pertinente.

Por ser de Justicia que reitero en el lugar y fecha "ut supra"

Fdo.: D./Dña. [NOMBRE Y APELLIDOS]
