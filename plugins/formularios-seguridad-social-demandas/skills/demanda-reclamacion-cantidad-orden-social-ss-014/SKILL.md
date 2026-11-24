---
name: demanda-reclamacion-cantidad-orden-social-ss-014
description: "Demanda de reclamación de cantidad en el orden social. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de reclamación de cantidad en el orden social

> Formulario **SS-014** del plugin **Seguridad Social: demandas y recursos ante lo social** (`formularios-seguridad-social-demandas`) · Seguridad Social › Demandas y escritos ante la jurisdicción social · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de reclamación de cantidad en el orden social» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de reclamación de cantidad en el orden social” para mi caso». También puedes invocarla directamente con `/formularios-seguridad-social-demandas:demanda-reclamacion-cantidad-orden-social-ss-014`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-seguridad-social-demandas:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Seguridad Social: demandas y recursos ante lo social) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (3 veces)
- [ ] IMPORTE (3 veces)
- [ ] LUGAR (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] SECTOR O EMPRESA (2 veces)
- [ ] ASEGURADORA
- [ ] CORREO ELECTRÓNICO
- [ ] DENOMINACIÓN SOCIAL
- [ ] DNI/NIE
- [ ] GRUPO O CATEGORÍA PROFESIONAL
- [ ] LOCALIDAD
- [ ] NIF
- [ ] NOMBRE DE LA PARTE
- [ ] SEDE
- [ ] TELÉFONO

## Normas que cita el formulario

- art. 33 ET
- art. 90.1 LRJS
- art. 66 LRJS

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

Modelo de demanda en reclamación de cantidad en el ámbito Social, de conformidad con el procedimiento ordinario establecido en los artículos 80 y siguientes de la Ley reguladora de la jurisdicción social, que refunde los siguientes supuestos –no taxativos- que puede seleccionar individualmente:

- Reclamación de salarios.

- Reclamación de horas extras.

- Reclamación de indemnización por despido.

- Reclamación de compensación y absorción indebida.

- Reclamación de plus de antigüedad (trienios).

- Reclamación de indemnización derivada de contrato de seguro establecido por convenio colectivo.

- Reclamación de diferencia de indemnización derivada de contrato de seguro establecido por convenio colectivo.

- Reclamación por diferencias de convenio o aplicación de convenio diferente.


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

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con NIF/NIE número [DNI/NIE] y domicilio en [LOCALIDAD], teléfono [TELÉFONO] y correo electrónico [CORREO ELECTRÓNICO], ante la Sección de lo Social del Tribunal de Instancia comparece y DICE:

Que mediante el presente escrito, interpone demanda en reclamación de cantidad por [ELEGIR: salarios / horas extraordinarias / indemnización por despido / compensación y absorción indebida / plus de antigüedad / indemnización derivada de contrato de seguro establecido por convenio colectivo / diferencias de indemnización derivada de contrato de seguro establecido por convenio colectivo / aplicación de un convenio diferente / diferencias de convenio], en tiempo y forma legalmente establecido, contra la empresa [DENOMINACIÓN SOCIAL], CIF [NIF], C.C.C., en la persona de su representante legal

[OPCIONAL — incluir si procede]

y contra la entidad aseguradora [ASEGURADORA], en la persona de su representante legal

[OPCIONAL — incluir si procede]

y contra el Fondo de Garantía Salarial, en la persona de su representante legal

Todo ello en base a los siguientes hechos y fundamentos legales:

HECHOS

PRIMERO.- Que el demandante ha venido prestando servicios para la referida empresa a la que le resulta de aplicación el convenio colectivo de [SECTOR O EMPRESA], desde el día [FECHA], en el grupo profesional de [GRUPO O CATEGORÍA PROFESIONAL], percibiendo con un salario bruto mensual de [IMPORTE] euros, incluida la prorrata de pagas extras, que se abona mediante transferencia bancaria y cuyo desglose es el siguiente:

Salario Base:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]

[ELEGIR UNA OPCIÓN: Si se reclaman salarios / Si se reclaman horas extras / Si se reclama indemnización por despido / Si se reclama por compensación y absorción indebida / Si se reclama plus de antigüedad / Si se reclama indemnización derivada de contrato de seguro establecido por convenio colectivo / Si se reclaman diferencias de indemnización derivada de contrato de seguro establecido por convenio colectivo / Si se reclama cantidad por aplicación de un convenio diferente o diferencias de convenio]

TERCERO.- Que en fecha [FECHA] se celebró el preceptivo Acto de Conciliación ante el Servicio de Mediación, Arbitraje y Conciliación, el cual finalizó [ELEGIR: sin avenencia / sin efecto], tal y como acredito mediante el Acta de la celebración de dicha conciliación que a este escrito se acompaña.

[OPCIONAL — incluir si procede]

(Si se demanda también al FOGASA, como consecuencia de insolvencia o concurso de la entidad demandada)

CUARTO.- Que, dada la situación económica de la empresa demandada y la elevada posibilidad de ser declarada [ELEGIR: insolvente / en concurso], de conformidad con lo establecido en el artículo 33 del Estatuto de los Trabajadores el FOGASA será responsable del abono de la cantidad reclamada en caso de que así se declare.

A los anteriores hechos les resultan de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

[ELEGIR UNA OPCIÓN: Si se reclama también al FOGASA / Si se reclaman salarios / Si se reclaman horas extras / Si se reclama indemnización por despido / Si se reclama compensación y absorción indebida, plus de antigüedad o diferencias de convenio / Si se reclama indemnización o diferencias de indemnización derivada de contrato de seguro establecido por convenio colectivo]

II.- Normativa de aplicación del convenio colectivo de [SECTOR O EMPRESA].

III.- Demás fundamentos legales y jurisprudenciales que se expondrán en el momento procesal oportuno.

En virtud de cuanto antecede es por lo que,

SUPLICO AL TRIBUNAL, que teniendo por presentado este escrito, con sus copias y documentos que lo acompañan, se sirva admitirlo y citar a las partes para la celebración del Acto de Juicio y tras el intento previo de conciliación siga con los demás trámites hasta dictar sentencia por la que con estimación de la demanda se acuerde condenar a [NOMBRE DE LA PARTE] al abono al demandante de la cantidad de [IMPORTE] euros, en concepto de salarios devengados y no abonados, más el diez por ciento en concepto de intereses por mora,

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]
— (Si se reclama indemnización o diferencias de indemnización derivadas de contrato de seguro)
— (Si se reclaman salarios, salarios de tramitación o indemnización por despido o extinción de contrato al FOGASA, a causa insolvencia o concurso del empresario, conforme al art. 33 ET)
— (Si se reclama por compensación y absorción indebida)
— (Si se reclama plus de antigüedad)

[OPCIONAL — incluir si procede]

(Si se reclama por diferencias de convenio)

y a abonar a la actora las cantidades salariales que se le adeudan, más el diez por ciento de recargo por mora en el pago dado lo injustificado del comportamiento empresarialy que se concretará en el acto del juicio, cantidad que a fecha de hoy asciende a un total de [IMPORTE] euros, con todo cuanto más proceda en Derecho.

PRIMER OTROSI DIGO: Que al acto de juicio este demandante comparecerá asistido de Letrado que le defienda, en conformidad con el artículo 21.2 de la Ley reguladora de la jurisdicción social, designando – sin perjuicio de las notificaciones via Lexnet- el domicilio profesional del Letrado D./Dña. [NOMBRE Y APELLIDOS] en [LUGAR], a efectos de notificaciones y demás diligencias.

SUPLICO AL TRIBUNAL que tenga por hecha tal manifestación, a los efectos oportunos.

SEGUNDO OTROSI DIGO: Que interesan al derecho de esta parte, y sin perjuicio de ampliación en el momento procesal oportuno, los siguientes MEDIOS DE PRUEBA:

[OPCIONAL — repetir el párrafo siguiente por cada persona adicional]
(Se detallan a continuación todos los medios de prueba (interrogatorio, documental, etc.) que interesen presentar junto a la demanda)

En cumplimiento de lo dispuesto por el artículo 90.1 de la LRJS entiende esta parte que la prueba documental solicitada por medio del presente escrito es útil y directamente pertinente al objeto del presente juicio, en razón de que resultará útil para acreditar:

SUPLICO AL TRIBUNAL que tenga por hechas tales manifestaciones a los efectos oportunos, admita y declare pertinentes las pruebas propuestas, y acuerde cuanto sea preciso.

Para el caso de que la empresa no haya acudido al acto de conciliación:

[OPCIONAL — incluir si procede]

(Para el caso de que la empresa no haya acudido al acto de conciliación)

TERCER OTROSI DIGO, que si la sentencia que en su día dicte coincidiera esencialmente con la pretensión contenida en la papeleta de conciliación, y en virtud de lo establecido en el art. 66 de la LRJS, deberán imponerse las costas del proceso a la empresa por no haber comparecido al acto de conciliación.

SUPLICO AL TRIBUNAL que tenga por hecha la anterior manifestación a los efectos legales oportunos.

Es de Justicia que pide en [LUGAR], a [FECHA].
