---
name: demanda-reclamacion-cantidades-indebidamente-ingresadas-ss-017
description: "Demanda de reclamación de cantidades indebidamente ingresadas a la Seguridad Social. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de reclamación de cantidades indebidamente ingresadas a la Seguridad Social

> Formulario **SS-017** del plugin **Seguridad Social: demandas y recursos ante lo social** (`formularios-seguridad-social-demandas`) · Seguridad Social › Demandas y escritos ante la jurisdicción social · normativa revisada el 24-11-2026.

## Qué es

Demanda ante la jurisdicción social por la que un empresario autónomo reclama a la Tesorería General de la Seguridad Social la devolución de cuotas ingresadas indebidamente, tras haber agotado (expresa o tácitamente) la reclamación previa.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de reclamación de cantidades indebidamente ingresadas a la Seguridad Social» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de reclamación de cantidades indebidamente ingresadas a la Seguridad Social” para mi caso». También puedes invocarla directamente con `/formularios-seguridad-social-demandas:demanda-reclamacion-cantidades-indebidamente-ingresadas-ss-017`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-seguridad-social-demandas:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Seguridad Social: demandas y recursos ante lo social) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (4 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] CALLE, NÚMERO, PISO (2 veces)
- [ ] CÓDIGO POSTAL (2 veces)
- [ ] AÑO
- [ ] CATEGORÍA/GRUPO PROFESIONAL
- [ ] CONVENIO COLECTIVO / SECTOR DE ACTIVIDAD
- [ ] DETALLAR EL CÁLCULO DE LAS DIFERENCIAS
- [ ] DETALLE DE LAS MENSUALIDADES
- [ ] DOMICILIO PROFESIONAL
- [ ] DÍA
- [ ] ENUMERAR LOS MEDIOS DE PRUEBA
- [ ] FECHA DE FIN DEL PERIODO
- [ ] FECHA DE INICIO DEL PERIODO
- [ ] FECHA DE PRESENTACIÓN DE LA SOLICITUD
- [ ] MES
- [ ] NOMBRE Y APELLIDOS DEL LETRADO/A
- [ ] NOMBRE Y APELLIDOS DEL TRABAJADOR
- [ ] SEDE

## Normas que cita el formulario

- art. 71 Ley 36/2011

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

NOTA PREVIA (suprimir antes de presentar): Debe interponerse en el plazo de 30 días desde la desestimación expresa o tácita de la reclamación previa.


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

D./Dña. [NOMBRE Y APELLIDOS], mayor de edad, con domicilio en [LOCALIDAD], calle [CALLE, NÚMERO, PISO], código postal [CÓDIGO POSTAL], ante ese Tribunal comparece y DICE:

Que, por medio del presente escrito, formula, en tiempo y forma, DEMANDA EN RECLAMACIÓN DE INGRESOS INDEBIDOS contra la DIRECCIÓN PROVINCIAL/ADMINISTRACIÓN DE LA TESORERÍA GENERAL DE LA SEGURIDAD SOCIAL DE [LOCALIDAD], con domicilio en la misma, calle [CALLE, NÚMERO, PISO], código postal [CÓDIGO POSTAL].

Se basa la presente demanda en los siguientes hechos y fundamentos legales:

HECHOS

PRIMERO.– Que el demandante, empresario individual dado de alta en el Régimen de Trabajadores por Cuenta Propia o Autónomos, vino abonando a la Seguridad Social, en el periodo desde [FECHA DE INICIO DEL PERIODO] hasta [FECHA DE FIN DEL PERIODO] (teniendo en cuenta que el plazo para solicitar la devolución de ingresos indebidos es de prescripción de cuatro años) y en concepto de cuotas del trabajador por cuenta ajena a su servicio, D./Dña. [NOMBRE Y APELLIDOS DEL TRABAJADOR], que presta sus servicios con la categoría de [CATEGORÍA/GRUPO PROFESIONAL], la cantidad de [IMPORTE] euros mensuales.

SEGUNDO.– Que tal cantidad derivaba de un error, ya que el salario bruto mensual del citado trabajador ascendía a [IMPORTE] euros en el periodo indicado y, por tanto, la cotización mensual debía ser de [IMPORTE] euros. Se acompañan a tal efecto nóminas referentes a las mensualidades de [DETALLE DE LAS MENSUALIDADES].

El convenio colectivo aplicable a la empresa es el de [CONVENIO COLECTIVO / SECTOR DE ACTIVIDAD].

TERCERO.– Que, en consecuencia, se han generado las siguientes diferencias en concepto de ingresos indebidos a la Seguridad Social: [DETALLAR EL CÁLCULO DE LAS DIFERENCIAS].

CUARTO.– Que el demandante formuló en fecha [FECHA DE PRESENTACIÓN DE LA SOLICITUD] la correspondiente solicitud de devolución de ingresos indebidos ante el órgano hoy demandado, por la cantidad y conceptos indicados y en el modelo oficial TC 13/1 establecido al efecto, mediante el sistema RED.

QUINTO.– Que, transcurridos seis meses desde la presentación de la solicitud, el citado órgano no notificó resolución expresa declarando o no el derecho a la devolución, por lo que, de conformidad con lo establecido en el artículo 45.2 del Reglamento General de Recaudación de la Seguridad Social, aprobado por Real Decreto 1415/2004, de 11 de junio, entendió desestimada la solicitud.

SEXTO.– Que, en cumplimiento de lo establecido por el artículo 71 de la Ley 36/2011, de 10 de octubre, reguladora de la jurisdicción social, el ahora demandante interpuso reclamación previa ante el mismo órgano, dentro de los treinta días siguientes a la fecha en que se entendió producida la desestimación por silencio administrativo.

SÉPTIMO.– Que, transcurrido el plazo de cuarenta y cinco días desde la interposición de la reclamación previa, el órgano competente no ha dictado resolución expresa, por lo que, de nuevo por silencio administrativo y de conformidad con el apartado 5 del artículo 71 citado de la ley procesal, se entendió desestimada y, por tanto, agotada la vía administrativa. En consecuencia, y en defensa de su derecho, interpone la presente demanda dentro del plazo subsiguiente de treinta días.

Lo expuesto se basa en los siguientes:

FUNDAMENTOS DE DERECHO

I.– COMPETENCIA Y LEGITIMACIÓN.

Artículos 2 o), 6 y 10 de la Ley 36/2011, de 10 de octubre, reguladora de la jurisdicción social.

II.– PROCEDIMIENTO.

Artículos 71 y 151 de la Ley 36/2011, de 10 de octubre, reguladora de la jurisdicción social.

III.– FONDO DEL ASUNTO.

Artículo 26 del Real Decreto Legislativo 8/2015, de 30 de octubre, por el que se aprueba el texto refundido de la Ley General de la Seguridad Social.

Artículos 44 y 45 del Real Decreto 1415/2004, de 11 de junio, por el que se aprueba el Reglamento General de Recaudación de la Seguridad Social.

Artículos 43 y siguientes de la Orden TAS/1562/2005, de 25 de mayo, por la que se establecen normas para la aplicación y desarrollo del Reglamento General de Recaudación de la Seguridad Social, aprobado por el Real Decreto 1415/2004, de 11 de junio.

Por lo expuesto,

SUPLICO AL TRIBUNAL que, teniendo por presentado este escrito, con sus documentos y copias, se sirva admitirlo y tener por formulada demanda en reclamación de ingresos indebidos contra la Dirección Provincial/Administración de la Tesorería General de la Seguridad Social, cite a las partes para los actos de conciliación y, en su caso, juicio, y, seguidos que sean los trámites legales oportunos, dicte sentencia por la que, con estimación íntegra de la presente demanda, condene al órgano demandado a devolver al reclamante la cantidad de [IMPORTE] euros, más el interés de demora correspondiente y el importe del reembolso de los costes de las garantías aportadas para suspender el procedimiento recaudatorio y los intereses que procedan sobre éste, con lo demás que proceda en Derecho.

Es de Justicia que pide en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

Firma del demandante: [NOMBRE Y APELLIDOS]

OTROSÍ DIGO: Que comparecerá al acto de juicio asistido de Letrado que le defienda, de conformidad con el artículo 21.2 de la Ley reguladora de la jurisdicción social, designando el domicilio profesional del Letrado D./Dña. [NOMBRE Y APELLIDOS DEL LETRADO/A] en la calle [DOMICILIO PROFESIONAL] de esta localidad, a efectos de notificaciones y demás diligencias.

Por lo que,

SUPLICO AL TRIBUNAL que tenga por hecha tal manifestación a los efectos oportunos.

SEGUNDO OTROSÍ DIGO: Que interesan al derecho de esta parte, y sin perjuicio de su ampliación en el momento procesal oportuno, los siguientes MEDIOS DE PRUEBA: [ENUMERAR LOS MEDIOS DE PRUEBA].

Por lo que,

SUPLICO AL TRIBUNAL que tenga por hecha tal manifestación a los efectos oportunos, admita y declare pertinentes las pruebas que se dejan propuestas, y acuerde cuanto sea preciso para llevarlas a efecto.

Es de Justicia que, en el mismo lugar y fecha, pide.

Firma del demandante: [NOMBRE Y APELLIDOS]
