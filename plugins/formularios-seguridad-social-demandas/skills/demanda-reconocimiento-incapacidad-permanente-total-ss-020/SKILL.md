---
name: demanda-reconocimiento-incapacidad-permanente-total-ss-020
description: "Demanda de reconocimiento de incapacidad permanente total. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de reconocimiento de incapacidad permanente total

> Formulario **SS-020** del plugin **Seguridad Social: demandas y recursos ante lo social** (`formularios-seguridad-social-demandas`) · Seguridad Social › Demandas y escritos ante la jurisdicción social · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de reconocimiento de incapacidad permanente total» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de reconocimiento de incapacidad permanente total” para mi caso». También puedes invocarla directamente con `/formularios-seguridad-social-demandas:demanda-reconocimiento-incapacidad-permanente-total-ss-020`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-seguridad-social-demandas:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Seguridad Social: demandas y recursos ante lo social) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (8 veces)
- [ ] DENOMINACIÓN SOCIAL (7 veces)
- [ ] LOCALIDAD (5 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] PROFESIÓN HABITUAL (3 veces)
- [ ] Nº (2 veces)
- [ ] CAUSAS DE DENEGACIÓN
- [ ] COLEGIO
- [ ] CORREO ELECTRÓNICO
- [ ] DESCRIPCIÓN DEL ACCIDENTE
- [ ] DIAGNÓSTICO
- [ ] DIRECCIÓN
- [ ] DNI/NIE
- [ ] DOCUMENTOS A APORTAR
- [ ] DOLENCIAS
- [ ] FUNCIONES Y TAREAS
- [ ] IMPORTE
- [ ] LUGAR
- [ ] Nº DE DOCUMENTO
- [ ] NÚMERO
- [ ] SEDE
- [ ] TELÉFONO
- [ ] ÓRGANO

## Normas que cita el formulario

- No cita artículos concretos; Claude localizará las normas aplicables con Jurisprudenciator si el documento las necesita.

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

La incapacidad permanente total es aquella situación en la que la persona trabajadora, tras haber estado sometido al tratamiento prescrito, presenta reducciones anatómicas o funcionales graves, susceptibles de determinación objetiva y previsiblemente definitivas, que le inhabilitan para la realización de todas o de las fundamentales tareas de su profesión habitual, siempre que pueda dedicarse a otra distinta. No es obstáculo para su reconocimiento la posibilidad de recuperación si esta se estima médicamente incierta o a largo plazo. Se entiende por profesión habitual, en caso de accidente, la desempeñada normalmente por la persona trabajadora al tiempo de sufrirlo; en caso de enfermedad común o profesional, aquella a la que la persona trabajadora dedicaba su actividad fundamental durante el periodo anterior a la incapacidad

La prestación económica correspondiente a la incapacidad permanente total consiste en una pensión vitalicia equivalente al 55% de la base reguladora. Si el beneficiario tiene 55 años o más y se presume dificultad para obtener empleo en actividad distinta a la habitual, la pensión se incrementa en un 20% de la base reguladora, salvo que el pensionista esté trabajando. Excepcionalmente, esta pensión puede ser sustituida por una indemnización a tanto alzado cuando el beneficiario sea menor de sesenta años.

La demanda ante el Tribunal de Instancia debe formularse en el plazo de treinta días, a contar desde la fecha en que se notifique la denegación de la reclamación previa o desde el día en que se entienda denegada por silencio administrativo.

Se trata de la modalidad procesal de prestaciones de Seguridad Social (arts. 140 y ss LRJS).

La demanda debe contener una exposición detallada de las lesiones y secuelas, que deben ser objetivables y previsiblemente definitivas, así como la descripción de las limitaciones funcionales que provocan en la persona trabajadora. No basta con la mera enumeración de dolencias, sino que es necesario concretar cómo afectan a la capacidad de trabajo y al rendimiento en la profesión habitual

Este formulario es aplicable tanto al supuesto de enfermedad común como enfermedad profesional y accidente de trabajo.

En el caso de contingencias profesionales hay que demandar también a la Mutua y a la empresa.


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

D./Dña [NOMBRE Y APELLIDOS] Letrado/a del Ilustre Colegio de Abogados de [COLEGIO], en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS], con DNI nº [DNI/NIE], según se acredita mediante [ÓRGANO], con domicilio a efectos de notificaciones en su despacho sito en [LOCALIDAD] de [DIRECCIÓN], teléfono [TELÉFONO] y correo electrónico [CORREO ELECTRÓNICO], ante el Tribunal comparezco y, como mejor proceda en Derecho DIGO:

Que por medio del presente escrito y en la representación que ostento formulo demanda de incapacidad permanente total derivada de [ELEGIR: enfermedad común / enfermedad profesional / accidente de trabajo], que deberá tramitarse por el procedimiento establecido en los arts. 140 y siguientes de la Ley Reguladora de la Jurisdicción Social, contra el INSTITUTO NACIONAL DE LA SEGURIDAD SOCIAL, la TESORERÍA GENERAL DE LA SEGURIDAD y la Empresa [DENOMINACIÓN SOCIAL], con domicilio en [LOCALIDAD] y la Mutua de Accidentes de Trabajo y Enfermedades Profesionales [DENOMINACIÓN SOCIAL], con domicilio en [LOCALIDAD], en la persona de sus representantes legales.

A fin de que sean condenados en los términos que en la súplica de esta demanda se dirán.

Se funda la presente demanda en los siguientes

HECHOS

Primero.— El/La actor/a nació el [FECHA], en [LOCALIDAD], está afiliado/a al Régimen General de la Seguridad Social con nº [Nº], siendo su profesión habitual la de [PROFESIÓN HABITUAL]. El/La actora ha prestado servicios en la empresa [DENOMINACIÓN SOCIAL] desde el [FECHA].

Su puesto de trabajo incluye las siguientes funciones y tareas [FUNCIONES Y TAREAS].

El día [FECHA], cuando estaba trabajando sufrí un accidente, consistente en: [DESCRIPCIÓN DEL ACCIDENTE]. Dicho accidente fue objeto de investigación por el Servicio de Prevención de la empresa concluyendo que tenía el carácter de [ELEGIR: leve / grave / muy grave]

Segundo.— Con fecha [FECHA], y tras un periodo de [Nº] meses en situación de incapacidad temporal, el/la demandante presentó solicitud de reconocimiento de incapacidad permanente total para su profesión habitual. Con fecha fue emitido dictamen propuesta por el Equipo de valoración de incapacidades, quien emitió el siguiente diagnóstico: [DIAGNÓSTICO].

Se adjunta como documento nº [Nº DE DOCUMENTO] copia del informe médico de síntesis del EVI.

Tercero.— Mediante resolución del INSS de fecha [FECHA], expediente n.º [NÚMERO], se acuerda denegar la prestación solicitada por las siguientes causas: [CAUSAS DE DENEGACIÓN]. Contra la citada resolución interpuso reclamación previa el día [FECHA], la cual fue desestimada mediante resolución de [FECHA] la cual no ha sido resuelta de forma expresa habiendo transcurrido 45 días desde la interposición de la reclamación previa.

Cuarto.— Del informe pericial que se aporta a esta demanda y que será ratificado por el perito que lo suscribe en el acto de la vista, quedará acreditado que el/la actor/a se encuentra incapacitado/a de manera permanente y total para su profesión habitual de [PROFESIÓN HABITUAL], como consecuencia de padecer: [DOLENCIAS]. Estas dolencias irreversibles y carentes de tratamiento médico eficaz me incapacitan de manera permanente y total para mi profesión habitual de

Quinto.— Que se establece la base reguladora en [IMPORTE]

Sexto.— La empresa [DENOMINACIÓN SOCIAL] tiene concertado el riesgo de accidente de trabajo con la Mutua [DENOMINACIÓN SOCIAL].

Séptimo.— Que no encontrando conforme a Derecho la Resolución del INSS, por cuanto mis lesiones, como se acreditará en el momento procesal oportuno, me impiden realizar mi trabajo de [PROFESIÓN HABITUAL] por medio del presente escrito, dentro del plazo legalmente establecido y de conformidad con lo señalado por el artículo 71 de la Ley Reguladora de la Jurisdicción Social, viene a interponer DEMANDA ante la Sección Social del Tribunal de Instancia.

FUNDAMENTOS DE DERECHO

Primero.— Artículo 6 del Decreto 1646/1972, de 23 de junio, Decreto 298/1973, de 8 de febrero, Orden de 3 de abril de 1973 y Orden de 15 de abril de 1969.

Segundo.— Artículos 156, 157, 161, 167, 193 a 199 y Disposición transitoria vigésima sexta del Real Decreto Legislativo 8/2015, de 30 de octubre, por el que se aprueba el Texto Refundido de la Ley General de la Seguridad Social

Tercero.— Artículos 2, 71 a 73, 80, 140 y siguientes de la Ley 36/2011, de 10 de octubre, reguladora de la Jurisdicción Social.

Cuarto.— Real Decreto 1300/1995, de 21 de julio.

Quinto.— Orden de 18 de enero de 1996 para la aplicación y desarrollo del Real Decreto 1300/1995, de 21 de julio, sobre incapacidades laborales del sistema de la Seguridad Social, en su disposición final segunda.

Sexto.— Decreto 1646/1972, de 23 de junio: Artículo 6.

Séptimo.— La jurisprudencia ha precisado que la valoración de la incapacidad debe realizarse en relación con la profesión habitual del trabajador, entendida como la desempeñada normalmente al tiempo de sufrir el accidente o, en caso de enfermedad, aquella a la que el trabajador dedicaba su actividad fundamental durante el periodo anterior a la incapacidad. La Sala de lo Social del Tribunal Supremo ha reiterado que la incapacidad permanente total no exige la imposibilidad absoluta para toda tarea, sino la inhabilitación para las tareas fundamentales de la profesión habitual, permitiendo que el trabajador pueda dedicarse a otra distinta. La pensión de incapacidad permanente total es compatible con el ejercicio de una actividad distinta de la habitual para la que sí tenga habilidad o capacidad física, pero no con el desempeño retribuido de la misma profesión habitual respecto de la que se ha declarado la incapacidad.

La valoración de la incapacidad debe hacerse atendiendo fundamentalmente a las limitaciones funcionales derivadas de los padecimientos del trabajador, en cuanto tales restricciones son las que determinan la efectiva restricción de la capacidad de ganancia. Deben ponerse en relación las limitaciones funcionales resultantes con los requerimientos de las tareas que constituyen el núcleo de la concreta profesión.

La aptitud para el desempeño de la actividad laboral habitual implica la posibilidad de llevar a cabo todas o las fundamentales tareas de la misma, con profesionalidad y con unas exigencias mínimas de continuidad, dedicación, rendimiento y eficacia, sin que el desempeño de las mismas genere riesgos adicionales o suponga una continuación de sufrimiento en el trabajo cotidiano. No es obstáculo para la declaración de este grado de incapacidad el que el trabajador pueda realizar otras actividades distintas, más livianas y sedentarias, o incluso pueda desempeñar tareas menos importantes o secundarias de su propia profesión habitual, siempre que exista una imposibilidad de continuar trabajando en dicha actividad y conserve una aptitud residual relevante.

Debe entenderse por profesión habitual no un determinado puesto de trabajo, sino aquella que el trabajador está cualificado para realizar y a la que la empresa le haya destinado o pueda destinarle en la movilidad funcional.

La jurisprudencia destaca que unas mismas lesiones o secuelas pueden ser constitutivas o no de incapacidad permanente total en función de las actividades o tareas que requiera la profesión del presunto incapaz. Por tanto, la valoración debe ser individualizada y referida a las tareas fundamentales de la profesión habitual, no a un puesto concreto.

SUPLICO A LA SECCIÓN DE LO SOCIAL DEL TRIBUNAL DE INSTANCIA que teniendo por presentado este escrito, con sus copias, se sirva admitirlo y, en su virtud, tenga por interpuesta demanda en nombre de D./Dña [NOMBRE Y APELLIDOS] en RECLAMACIÓN DE LA DECLARACIÓN DE INCAPACIDAD PERMANENTE TOTAL derivada de contingencias [ELEGIR: comunes / profesionales], contra el INSS y la TGSS En su caso, la Mutua [DENOMINACIÓN SOCIAL] y la empresa [DENOMINACIÓN SOCIAL], en la persona de sus representantes legales, tramitando la misma conforme a Derecho, citando a las partes para los trámites previos de conciliación y, en su caso, de juicio, concluyendo las actuaciones con una sentencia estimatoria de la demanda, con los efectos legales que se deriven de tal pronunciamiento, en la que se acuerde declarar a mi representado en situación de INCAPACIDAD PERMANENTE TOTAL PARA SU PROFESIÓN HABITUAL, con el consiguiente abono de las prestaciones que, en su caso, correspondan.

Por ser de Justicia que pido en [LUGAR], a [FECHA].

PRIMER OTROSI DIGO que se solicita la reclamación de oficio al INSS en su caso también a la Mutua del expediente y antecedentes que posea en relación con el contenido de la demanda.

SEGUNDO OTROSI DIGO que esta parte acudirá al acto del juicio oral [ELEGIR: asistido/a / representado/a] de Letrado/a.

TERCER OTROSI DIGO que interesa al Derecho de esta parte que se practiquen los siguientes MEDIOS DE PRUEBA:

1º) INTERROGATORIO de la persona representante legal de la empresa demandada, previa citación judicial bajo los apercibimientos legales.

2º) DOCUMENTAL consistente en que se requiera a la empresa/Mutua demandada para que aporten los siguientes documentos [DOCUMENTOS A APORTAR].

3º) TESTIFICAL, de las personas que a continuación se relacionan, y que se solicita se las cite al juicio, con los apercibimientos legales pertinentes.

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

D./Dña [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD].

4º) DOCUMENTAL, TESTIFICAL y PERICIAL: la que esta parte aportará en el acto del juicio.

SUPLICO AL TRIBUNAL que tenga por hechas las anteriores manifestaciones y por propuesta la prueba, la admita y la estime pertinente.

Por ser de Justicia que reitero en el lugar y fecha “ut supra”
