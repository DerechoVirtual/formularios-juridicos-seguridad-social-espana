---
name: demanda-autonomo-reconozca-incapacidad-permanente-total-ss-019
description: "Demanda de autónomo para que se reconozca incapacidad permanente total por enfermedad común. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de autónomo para que se reconozca incapacidad permanente total por enfermedad común

> Formulario **SS-019** del plugin **Seguridad Social: demandas y recursos ante lo social** (`formularios-seguridad-social-demandas`) · Seguridad Social › Demandas y escritos ante la jurisdicción social · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de autónomo para que se reconozca incapacidad permanente total por enfermedad común» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de autónomo para que se reconozca incapacidad permanente total por enfermedad común” para mi caso». También puedes invocarla directamente con `/formularios-seguridad-social-demandas:demanda-autonomo-reconozca-incapacidad-permanente-total-ss-019`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-seguridad-social-demandas:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Seguridad Social: demandas y recursos ante lo social) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (12 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] Nº DE DOCUMENTO (3 veces)
- [ ] DOLENCIAS (2 veces)
- [ ] IMPORTE (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] PROFESIÓN HABITUAL (2 veces)
- [ ] ACTIVIDAD
- [ ] COLEGIO
- [ ] CORREO ELECTRÓNICO
- [ ] DIAGNÓSTICO
- [ ] DNI/NIE
- [ ] DOCUMENTOS A APORTAR
- [ ] EXIGENCIAS DEL TRABAJO
- [ ] FUNDAMENTOS
- [ ] LUGAR
- [ ] Nº DE AFILIACIÓN
- [ ] SEDE
- [ ] TELÉFONO
- [ ] ÓRGANO

## Normas que cita el formulario

- art. 140 LRJS

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

DEMANDA DE UN TRABAJADOR AUTÓNOMO SOLICITANDO RECONOCIMIENTO DE INCAPACIDAD PERMANENTE TOTAL DERIVADA DE ENFERMEDAD COMÚN

La acción protectora del RETA comprende la incapacidad permanente total derivada de contingencias comunes, junto con la incapacidad permanente absoluta y la gran incapacidad. La incapacidad permanente total derivada de contingencias comunes en el RETA exige la inhabilitación para la profesión habitual, el cumplimiento de los periodos de cotización y se calcula sobre la base reguladora del autónomo, siendo la prestación del 55% de dicha base, pudiendo incrementarse al 75% si el beneficiario es mayor de 55 años y se cumplen una serie de requisitos. La pensión podrá ser sustituida por una cantidad a tanto alzado equivalente a 40 mensualidades de la base reguladora de estas contingencias, siempre que el interesado ejerza esta opción dentro de los 30 días siguientes a la declaración de incapacidad y tenga menos de 60 años.

La demanda ante el Tribunal de Instancia debe formularse en el plazo de treinta días, a contar desde la fecha en que se notifique la denegación de la reclamación previa o desde el día en que se entienda denegada por silencio administrativo.

Se trata de la modalidad procesal de prestaciones de Seguridad Social (arts. 140 y ss LRJS).

La demanda debe contener una exposición detallada de las lesiones y secuelas, que deben ser objetivables y previsiblemente definitivas, así como la descripción de las limitaciones funcionales que provocan en la persona trabajadora. No basta con la mera enumeración de dolencias, sino que es necesario concretar cómo afectan a la capacidad de trabajo y al rendimiento en la profesión habitual.

A LA SECCIÓN DE LO SOCIAL DEL TRIBUNAL DE INSTANCIA DE [SEDE]

D./Dña. [NOMBRE Y APELLIDOS] Letrado/a del Ilustre Colegio de Abogados de [COLEGIO], en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS], con DNI nº [DNI/NIE], según se acredita mediante [ÓRGANO], con domicilio a efectos de notificaciones en su despacho sito en [LOCALIDAD], teléfono [TELÉFONO] y correo electrónico [CORREO ELECTRÓNICO], ante el Tribunal comparezco ce y, como mejor proceda en Derecho DIGO:

Que por medio del presente escrito y en la representación que ostento formulo demanda de incapacidad permanente total derivada de enfermedad común, que deberá tramitarse por el procedimiento establecido en los arts. 140 y siguientes de la Ley Reguladora de la Jurisdicción Social, contra el INSTITUTO NACIONAL DE LA SEGURIDAD SOCIAL, la TESORERÍA GENERAL DE LA SEGURIDAD, en la persona de sus representantes legales, en base a los siguientes es

HECHOS

Primero.— Comencé a prestar servicios en fecha [FECHA], dedicándome a la actividad de [ACTIVIDAD], encontrándome encuadrado desde el inicio de mi actividad en el Régimen Especial de Trabajadores Autónomos, siendo mi número de afiliación a la Seguridad Social el [Nº DE AFILIACIÓN]. Mi fecha de nacimiento es [FECHA].

Segundo.— En la actualidad no ejerzo ninguna actividad retribuida por cuenta propia ni por cuenta ajena.

Tercero.— No ostento la titularidad de una explotación agraria ni marítimo pesquera, ni de un establecimiento mercantil o industrial cómo propietario, arrendatario, usufructuario u otro concepto análogo.

Cuarto.— Con fecha [FECHA] inicié un proceso de incapacidad temporal, siendo diagnosticado de [DIAGNÓSTICO].

Quinto.— Las dolencias que presento en la actualidad son las siguientes: [DOLENCIAS]. Dichas dolencias me impiden la realización de mi trabajo habitualde [PROFESIÓN HABITUAL], dado que el mismo requiere [EXIGENCIAS DEL TRABAJO], lo que no puedo realizar las tareas fundamentales de mi profesión.

Se acompañan como documentos nº [Nº DE DOCUMENTO] Informes médicos.

Sexto.— Con fecha [FECHA] solicité el reconocimiento de la situación de incapacidad permanente total, derivada de enfermedad común.

El equipo de valoración de incapacidades emitió dictamen-propuesta en fecha [FECHA] objetivando las siguientes dolencias [DOLENCIAS].

La Dirección Provincial del INSS emitió resolución en fecha [FECHA], desestimatoria de mi solicitud, por entender que mis dolencias no tienen carácter invalidante.

Se adjuntan como documentos nº [Nº DE DOCUMENTO] informe médico de síntesis del EVI y resolución del INSS de fecha [FECHA].

Séptimo.— La base reguladora de la pensión que solicito es la de [IMPORTE] euros mensuales.

Octavo.— En fecha [FECHA], interpuse reclamación previa administrativa, siendo desestimada mediante resolución de la Dirección Provincial del Instituto Nacional de la Seguridad Social de fecha [FECHA], que me fue notificada en fecha [FECHA].

Se adjuntan como documentos nº [Nº DE DOCUMENTO] reclamación previa y desestimación del INSS.

FUNDAMENTOS DE DERECHO

Primero.— Artículos 2, 71 a 73, 80, 140 y siguientes de la Ley 36/2011, de 10 de octubre, reguladora de la Jurisdicción Social: [FUNDAMENTOS].

Segundo.— Artículos 193 a 197 y Disposición transitoria vigésima sexta del Real Decreto Legislativo 8/2015, de 30 de octubre, por el que se aprueba el Texto Refundido de la Ley General de la Seguridad Social.

Cuarto.— Orden de 18 de enero de 1996, para la aplicación y desarrollo del Real Decreto 1300/1995, de 21 de julio, sobre incapacidades laborales del sistema de la Seguridad Social.

Quinto.— Decreto 2530/1970, de 20 de agosto, por el que se regula el Régimen Especial de la Seguridad Social de los Trabajadores por Cuenta Propia o Autónomos, modificado por Real Decreto 463/2003, de 25 de abril, en especial el artículo 38.

Sexto.— La jurisprudencia establece que, a efectos de incapacidad permanente total, la "profesión habitual" del trabajador autónomo es aquella actividad que venía desempeñando de forma inmediata y anterior al hecho causante de la incapacidad, y por la que estaba de alta en el Régimen Especial de Trabajadores Autónomos (RETA) en el momento de producirse la incapacidad permanente protegida por el mismo. Así lo dispone el art. 36.2 del Decreto 2530/1970, de 20 de agosto, y lo reitera la doctrina judicial, que equipara el concepto de profesión habitual en el RETA al previsto para el Régimen General, pero con la particularidad de que, en el caso de los autónomos, la profesión habitual abarca el conjunto de actividades propias de la actividad económica desarrollada, no limitándose a un puesto concreto ni a una función específica, sino al haz de tareas que integran la actividad profesional para la que se estaba dado de alta en el RETA al sobrevenir la incapacidad.

La jurisprudencia subraya que la valoración de la incapacidad debe realizarse en función de las limitaciones funcionales del trabajador y su incidencia sobre las tareas fundamentales de la profesión habitual, entendida esta como el conjunto de funciones que objetivamente integran la actividad profesional desarrollada por el autónomo. No se identifica con un puesto de trabajo concreto ni con una categoría profesional, sino con el ámbito de funciones propias de la actividad económica ejercida de forma habitual y personal.

La valoración de la profesión habitual debe realizarse con flexibilidad, teniendo en cuenta las particularidades del trabajo autónomo, donde pueden concurrir actividades diversas o cambios de ocupación. En todo caso, la determinación debe basarse en la realidad profesional y en la documentación acreditativa de la actividad desarrollada, como las altas y bajas en el régimen especial de trabajadores autónomos, declaraciones fiscales, contratos, facturación y cualquier otro medio de prueba admitido en derecho.

Por lo expuesto,

SUPLICO AL TRIBUNAL que, habiendo por presentada esta demanda con sus copias y documentos que acompaño, se sirva admitirla, tenga por formulada demanda en reclamación por incapacidad permanente total, derivada de enfermedad común, contra el Instituto Nacional de la Seguridad Social y la Tesorería General de la Seguridad Social, se proceda a citar a las partes para la celebración del acto del juicio, por el que, en definitiva, seguido que sea por todos sus trámites, incluido el recibimiento del mismo a prueba, que expresamente se solicita, se dicte en su día sentencia, estimando íntegramente la presente demanda, declarando al actor afecto de incapacidad permanente total, derivada de enfermedad común, para su profesión habitual de [PROFESIÓN HABITUAL], condenando a los demandados a estar y pasar por esta declaración y a que satisfagan una pensión del 55% de la base reguladora de [IMPORTE], euros mensuales más un incremento de 20% de dicha base reguladora, más las mejoras y revalorizaciones que procedan, con efectos desde el día [FECHA].

Es justicia que pido en [LUGAR], a [FECHA].

PRIMER OTROSI DIGO que se solicita la reclamación de oficio al INSS del expediente y antecedentes que posea en relación con el contenido de la demanda.

SEGUNDO OTROSI DIGO que esta parte acudirá al acto del juicio oral asistida/representado de Letrado.

TERCER OTROSI DIGO que interesa al Derecho de esta parte que se practiquen los siguientes MEDIOS DE PRUEBA:

1º) INTERROGATORIO de la persona representante legal de la empresa demandada, previa citación judicial bajo los apercibimientos legales.

2º) DOCUMENTAL consistente en que se requiera a la [ELEGIR: empresa / Mutua] demandada para que aporten los siguientes documentos [DOCUMENTOS A APORTAR].

3º) TESTIFICAL, de las personas que a continuación se relacionan, y que se solicita se las cite al juicio, con los apercibimientos legales pertinentes.

D./Dña. [NOMBRE Y APELLIDOS], con domicilio en [LOCALIDAD].

4º) DOCUMENTAL, TESTIFICAL y PERICIAL: la que esta parte aportará en el acto del juicio.

SUPLICO AL TRIBUNAL que tenga por hechas las anteriores manifestaciones y por propuesta la prueba, la admita y la estime pertinente.

Por ser de Justicia que reitero en el lugar y fecha “ut supra”

Firma
