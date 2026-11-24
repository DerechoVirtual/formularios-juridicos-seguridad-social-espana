---
name: demanda-responsabilidad-empresa-materia-infracotizacion-ss-024
description: "Demanda por responsabilidad de la empresa en materia de infracotización. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda por responsabilidad de la empresa en materia de infracotización

> Formulario **SS-024** del plugin **Seguridad Social: demandas y recursos ante lo social** (`formularios-seguridad-social-demandas`) · Seguridad Social › Demandas y escritos ante la jurisdicción social · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda por responsabilidad de la empresa en materia de infracotización» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda por responsabilidad de la empresa en materia de infracotización” para mi caso». También puedes invocarla directamente con `/formularios-seguridad-social-demandas:demanda-responsabilidad-empresa-materia-infracotizacion-ss-024`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-seguridad-social-demandas:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Seguridad Social: demandas y recursos ante lo social) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (13 veces)
- [ ] LOCALIDAD (6 veces)
- [ ] NOMBRE Y APELLIDOS (6 veces)
- [ ] DENOMINACIÓN SOCIAL (5 veces)
- [ ] Nº (5 veces)
- [ ] CATEGORÍA PROFESIONAL (2 veces)
- [ ] COLEGIO (2 veces)
- [ ] OTROS DATOS (2 veces)
- [ ] CORREO ELECTRÓNICO
- [ ] LUGAR
- [ ] Nº DE AFILIACIÓN
- [ ] Nº DE DOCUMENTO
- [ ] NÚMERO
- [ ] SEDE
- [ ] TELÉFONO

## Normas que cita el formulario

- art. 126 LGSS

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

La persona trabajadora afectada por infracotización puede presentar demanda contra la empresa ante el Tribunal de Instancia. En el proceso, la persona trabajadora puede reclamar la regularización de las cotizaciones, el abono de las diferencias salariales y la reparación de los daños y perjuicios derivados de la infracotización. La Inspección de Trabajo puede intervenir como parte o emitir informes sobre los hechos.

La jurisprudencia reconoce la posibilidad de interponer demanda contra la empresa por infracotización, es decir, cuando la empresa ha cotizado por una base inferior a la que legalmente correspondía en relación con el salario real de la persona trabajadora. En el proceso, la persona trabajadora puede reclamar el abono de las diferencias salariales y la reparación de los daños y perjuicios derivados de la infracotización. Además, esta acción puede tener como finalidad tanto la declaración de la base reguladora correcta para el cálculo de prestaciones de la Seguridad Social como la condena a la empresa al abono de las diferencias de cotización y de las prestaciones derivadas de dicha infracotización.

La acción puede dirigirse contra la empresa responsable de la infracotización, así como, en su caso, contra las entidades gestoras de la Seguridad Social. Es fundamental que exista un interés jurídico protegido, lo que normalmente se cumple cuando la infracotización afecta a la cuantía de la prestación o a la propia generación del derecho a la misma. No obstante, si la relación laboral ya está extinguida y no se reclama una prestación, puede apreciarse falta de acción por ausencia de interés jurídico protegido.

La empresa que incurre en infracotización es responsable directa de las consecuencias de su incumplimiento, debiendo abonar la diferencia de prestaciones que se derive de la base reguladora correcta. Esta responsabilidad se mantiene aunque la infracotización no haya influido en el período mínimo de cotización, sino únicamente en la cuantía de la prestación. La empresa debe constituir el capital coste correspondiente en la Tesorería General de la Seguridad Social, sin perjuicio de que la entidad gestora adelante el pago de la prestación y repita contra la empresa.


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

D./Dña. [NOMBRE Y APELLIDOS], Letrado/a en ejercicio del Ilustre Colegio de Abogados de [COLEGIO], con despacho profesional en [LOCALIDAD], teléfono [TELÉFONO] y correo electrónico [CORREO ELECTRÓNICO],en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, provisto/a de D.N.I. número [NÚMERO] y número de la Seguridad Social [Nº DE AFILIACIÓN], con domicilio en [LOCALIDAD], según acredito mediante copia de poder otorgado a tal efecto, que a este escrito se acompaña como documento nº [Nº DE DOCUMENTO] ante el Tribunal que por turno corresponda comparezco y como mejor proceda en Derecho, DIGO:

Que mediante el presente escrito vengo en formular DEMANDA EN MATERIA DE RESPONSABILIDAD EMPRESARIAL POR INFRACOTIZACION (PENSIÓN DE JUBILACIÓN) frente a:

1) INSTITUTO NACIONAL DE LA SEGURIDAD con domicilio en [LOCALIDAD]
2) TESORERIA GENERAL DE LA SEGURIDAD SOCIAL con domicilio en [LOCALIDAD]
3) EMPRESA con domicilio en [LOCALIDAD]

en las personas de sus representantes legales, a fin de que por este Tribunal se dicte Sentencia de conformidad con el suplico de la presente, lo que fundamento en base a los siguientes

HECHOS

PRIMERO.- Que en fecha [FECHA], tras haber comprobado que en su vida laboral no aparecían reflejados determinados periodos trabajados, D./Dña. [NOMBRE Y APELLIDOS] presentó ante la Tesorería General de la Seguridad Social, solicitud de rectificación de datos de vida laboral acreditando que:

I. Prestó servicios en [DENOMINACIÓN SOCIAL] de [LOCALIDAD] como [CATEGORÍA PROFESIONAL] en el período comprendido entre el [FECHA] y el [FECHA],

II. En su caso, prestó servicios para [DENOMINACIÓN SOCIAL] como [CATEGORÍA PROFESIONAL] en los siguientes periodos:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

- del [Nº] al [Nº]

SEGUNDO.- Que en fecha [FECHA] esta parte solicitó ante la Dirección Provincial del Instituto Nacional de la Seguridad Social, el reconocimiento de una pensión de jubilación en favor de mi representado/a.

El [FECHA] fue notificada a esta parte, resolución de fecha [FECHA] de la Dirección Provincial en la que se denegaba la pensión solicitada por los siguientes motivos:

TERCERO.- Que en fecha [FECHA], no estando de acuerdo con la resolución de fecha [FECHA], mi representado/a presentó Reclamación Administrativa Previa frente a la Dirección Provincial de la Seguridad Social, acreditando documentalmente el periodo de carencia exigido para obtener pensión de jubilación.

El mismo día, D./Dña. [NOMBRE Y APELLIDOS]. presentó reclamación administrativa previa frente [OTROS DATOS].

CUARTO.- Que el pasado [FECHA] fue notificada a mi representado/a resolución del INSS datada el [FECHA] del siguiente tenor: "No es admisible la pretensión del interesado de

QUINTO.-. Que la diferencia de días cotizados se debe:

A) A la infracotización por parte de la empresa [DENOMINACIÓN SOCIAL] de [OTROS DATOS], respecto del periodo certificado comprendido entre el [FECHA] y el [FECHA]
B) A la infracotización por parte de la [DENOMINACIÓN SOCIAL] respecto de los periodos certificados siguientes:
[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

- del [Nº] al [Nº]

o al error por parte de la Tesorería General de la Seguridad Social a la hora de reflejarlo en la vida laboral de la persona trabajadora.

En caso de no tratarse de errores por parte de la Tesorería General de la Seguridad Social, y tratarse por tanto de infracotizaciones por parte de [DENOMINACIÓN SOCIAL], esta sería responsable directa por falta de cotización y, en caso de insolvencia de las mismas, serían responsables subsidiarios el Instituto Nacional de la Seguridad Social y la Tesorería General de la Seguridad Social, de acuerdo con el artículo 126 de la LGSS.

A estos hechos les resultan de aplicación los siguientes,

FUNDAMENTOS DE DERECHO

I.- Artículos 1º, 2º, 6º, 16, 17 y 71 de la Ley Reguladora de la Jurisdicción Social.

II.- Artículos 167 y 168 de la LGSS y demás Jurisprudencia y Legislación que se aportará en el momento procesal oportuno.

Por todo lo expuesto,

SUPLICO AL TRIBUNAL, que teniendo por presentado este escrito, con sus copias y documentos que se adjuntan, lo admite a trámite y tenga por formulada DEMANDA EN MATERIA DE RESPONSABILIDAD EMPRESARIAL POR INFRACOTIZACION (PENSIÓN DE JUBILACIÓN)contra el INSTITUTO NACIONAL DE LA SEGURIDAD SOCIAL, la TESORERIA GENERAL DE LA SEGURIDAD SOCIAL, y la EMPRESA, cite a las partes a los actos de conciliación y juicio, se siga este por su trámites habituales, incluyendo el recibimiento a prueba que desde este momento se interesa, y en su momento dicte Sentencia mediante la cual, con estimación de esta demanda, conceda la pensión de jubilación en la cuantía que legalmente corresponda a D./Dña. [NOMBRE Y APELLIDOS]. de acuerdo con la base reguladora que conste en el expediente y los [Nº] años de cotización certificados, y declare la responsabilidad directa por falta de cotización y responsabilidad subsidiaria, en caso de insolvencia de las mismas del Instituto Nacional de la Seguridad Social y Tesorería General de la Seguridad Social, en los términos expuestos en el cuerpo de este escrito, con todo cuanto más proceda en Derecho.

PRIMER OTROSI DIGO: Que esta parte, de acuerdo con lo dispuesto en el artículo 71 de la Ley Reguladora de la Jurisdicción Social presento la Reclamación Previa (copia de la cual se adjunta como Documento nº 1 y 2), la cual fue desestimada mediante la Resolución que se acompaña al presente escrito como documento número 3.

SEGUNDO OTROSI DIGO: Que interesa al derecho de esta parte valerse en el Acto del Juicio, sin perjuicio de su ampliación en el momento procesal oportuno, de los siguientes medios de prueba:

A) DOCUMENTAL.-

1.- para que se tengan por aportados los documentos que se acompañan al presente escrito y los que en su día se aportarán
2.- Que se requiera al INSS para que aporte el expediente administrativo completo, con una antelación mínima de 15 días al Acto del Juicio, para ser estudiado por este Letrado.

TERCER OTROSÍ DIGO: Esta parte comparecerá al Acto de Juicio asistida del/de la Letrado/a del Ilustre Colegio de Abogados de [COLEGIO], D./Dña.. [NOMBRE Y APELLIDOS], con despacho profesional en la

En su virtud,

SUPLICO AL TRIBUNAL, que tenga por efectuadas las anteriores manifestaciones y designaciones a los efectos oportunos, así como la petición de prueba, admitiéndolas y acordando todo lo necesario para su práctica.

En [LUGAR], a [FECHA].
