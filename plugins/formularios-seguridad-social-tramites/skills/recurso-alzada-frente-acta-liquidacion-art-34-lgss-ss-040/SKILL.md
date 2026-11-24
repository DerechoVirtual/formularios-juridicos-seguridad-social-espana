---
name: recurso-alzada-frente-acta-liquidacion-art-34-lgss-ss-040
description: "Recurso de alzada frente a un acta de liquidación (art. 34 LGSS). Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Recurso de alzada frente a un acta de liquidación (art. 34 LGSS)

> Formulario **SS-040** del plugin **Seguridad Social: reclamaciones previas y recursos administrativos** (`formularios-seguridad-social-tramites`) · Seguridad Social › Solicitudes, reclamaciones y recursos ante la Administración · normativa revisada el 24-11-2026.

## Qué es

Recurso de alzada ante el superior jerárquico contra la resolución que eleva a definitiva un acta de liquidación de cuotas de la Seguridad Social levantada por la Inspección de Trabajo (por falta de afiliación o alta, diferencias de cotización, derivación de responsabilidad o aplicación indebida de bonificaciones).

Es un modelo de tipo **recursos**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Recurso de alzada frente a un acta de liquidación (art. 34 LGSS)» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Recurso de alzada frente a un acta de liquidación (art. 34 LGSS)” para mi caso». También puedes invocarla directamente con `/formularios-seguridad-social-tramites:recurso-alzada-frente-acta-liquidacion-art-34-lgss-ss-040`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-seguridad-social-tramites:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Seguridad Social: reclamaciones previas y recursos administrativos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] IMPORTE (5 veces)
- [ ] DÍA, MES Y AÑO (4 veces)
- [ ] FECHA DE FIN (4 veces)
- [ ] FECHA DE INICIO (4 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] ARTÍCULO
- [ ] AÑO
- [ ] COMUNIDAD AUTÓNOMA
- [ ] DNI/NIE
- [ ] DOMICILIO: CALLE, NÚMERO, PISO, CÓDIGO POSTAL, LOCALIDAD
- [ ] DÍA
- [ ] FECHA
- [ ] MES
- [ ] N.º DE ACTA
- [ ] NOMBRE Y APELLIDOS DEL LETRADO/A
- [ ] NOMBRE Y APELLIDOS DEL RECURRENTE
- [ ] NOMBRE Y APELLIDOS DEL RECURRENTE O DE SU REPRESENTANTE
- [ ] TRIBUNAL, FECHA Y N.º DE RECURSO O ECLI
- [ ] ÓRGANO QUE LA DICTÓ

## Normas que cita el formulario

- art. 34 Real Decreto Legislativo 8/2015

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

NOTAS DE USO (suprimir antes de presentar):

Recurso de alzada contra acta de liquidación al amparo de los artículos 34 de la Ley General de la Seguridad Social (texto refundido aprobado por Real Decreto Legislativo 8/2015), 33 del Real Decreto 928/1998 (Reglamento general sobre procedimientos para la imposición de sanciones por infracciones de orden social y para los expedientes liquidatorios de cuotas de la Seguridad Social) y 46, 65 y 66 del Reglamento general de recaudación de la Seguridad Social, por deudas por cuotas originadas por:

- Falta de afiliación o alta.
- Diferencias de cotización.
- Derivación de la responsabilidad del sujeto obligado al pago.
- Aplicación indebida de bonificaciones en las cotizaciones.

El órgano competente para resolver es el superior jerárquico del que dictó la resolución que eleva a definitiva el acta de liquidación, que se identifica en la propia resolución. El plazo de interposición es de un mes desde la notificación (art. 122 de la Ley 39/2015).


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

AL ILMO. SR. DIRECTOR TERRITORIAL DE LA INSPECCIÓN DE TRABAJO Y SEGURIDAD SOCIAL DE [COMUNIDAD AUTÓNOMA] [INDICAR EL ÓRGANO COMPETENTE PARA RESOLVER EL RECURSO DE ALZADA, SUPERIOR JERÁRQUICO DEL QUE DICTÓ LA RESOLUCIÓN QUE ELEVA A DEFINITIVA EL ACTA DE LIQUIDACIÓN]

D./Dña. [NOMBRE Y APELLIDOS DEL LETRADO/A], Abogado/a en ejercicio del Ilustre Colegio de [LOCALIDAD], en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS DEL RECURRENTE], según acredito mediante el poder a mi favor otorgado que acompaño, con DNI número [DNI/NIE] y domicilio a efectos de notificaciones en [DOMICILIO: CALLE, NÚMERO, PISO, CÓDIGO POSTAL, LOCALIDAD], ante esa Dirección comparezco y como mejor proceda en Derecho,

DIGO:

Que, por medio del presente escrito y al amparo de los artículos 34 del Real Decreto Legislativo 8/2015, de 30 de octubre, por el que se aprueba el texto refundido de la Ley General de la Seguridad Social, 33.3 del Real Decreto 928/1998, de 14 de mayo, por el que se aprueba el Reglamento general sobre procedimientos para la imposición de sanciones por infracciones de orden social y para los expedientes liquidatorios de cuotas de la Seguridad Social, y 121 y 122 de la Ley 39/2015, del Procedimiento Administrativo Común de las Administraciones Públicas, interpongo en tiempo y forma RECURSO DE ALZADA, en la representación que ostento, contra la Resolución de fecha [DÍA, MES Y AÑO] que eleva a definitiva el acta de liquidación de la Inspección de Trabajo y Seguridad Social número [N.º DE ACTA] de fecha [DÍA, MES Y AÑO], por considerar que no es ajustada a Derecho, en base a las siguientes

ALEGACIONES

PRIMERA.- Que, en fecha [DÍA, MES Y AÑO], le fue notificada a mi representado la resolución que se recurre, la cual eleva a definitiva el acta de liquidación de cuotas que se formuló contra mi representado, por [ELEGIR: falta de afiliación o alta de persona trabajadora / diferencias de cotización / derivación de responsabilidad / aplicación indebida de bonificaciones en las cotizaciones].

SEGUNDA.- Que,

[ELEGIR UNA DE ESTAS ALTERNATIVAS Y SUPRIMIR LAS DEMÁS:]

— (Falta de afiliación o alta) concretamente, en dicha acta se le reclama la cantidad de [IMPORTE] euros en concepto de falta de afiliación o alta del recurrente en el régimen especial de trabajadores autónomos por el período de liquidación del [FECHA DE INICIO] al [FECHA DE FIN].

Ahora bien, el acta de liquidación no se ajusta a derecho por varios motivos:

[OPCIONAL — incluir si procede]

- Se practicó mediante notificación edictal sin haberse agotado todos los medios previos. De hecho, mi representado figura debidamente empadronado en [LOCALIDAD] y la Inspección no solo trató de notificarle en otro domicilio distinto sin aportar justificación, sino que no ha acreditado que se agotaron todos los medios previos a la notificación edictal, que es excepcional y solo procede cuando el resto de medios resultan insuficientes.

[OPCIONAL — incluir si procede]

- Las deudas reclamadas habían prescrito, al haber transcurrido más de cuatro años desde su vencimiento hasta su reclamación el [FECHA].

[OPCIONAL — incluir si procede]

- Hay un error material aritmético en el cálculo de la deuda reclamada, que no ha tenido en cuenta las reducciones y bonificaciones a las que tenía derecho mi representado.

— (Diferencias de cotización) concretamente, en dicha acta se le reclama la cantidad de [IMPORTE] euros en concepto de diferencias de cotización derivadas de haber cotizado por bases de cotización inferiores a las reales y debidas, al no incluir en las remuneraciones que integran dichas bases el importe anual que excede del 20% de once mensualidades del SMI vigente, o la parte proporcional a los días de trabajo y alta en la empresa, percibido como pluses de transporte y vestuario por las personas trabajadoras, correspondientes al período desde el [FECHA DE INICIO] hasta el [FECHA DE FIN].

La Resolución administrativa impugnada afirma que el umbral que marca el importe exento de cotización es ese 20%, que no incluye la cuantía del mes de vacaciones o parte proporcional de éstas, por lo que el importe anual del SMI a tener en cuenta es de once meses. En base a lo cual levantó el acta de liquidación por las diferencias.

Esta parte considera que, conforme establece el artículo [ARTÍCULO] del convenio colectivo aplicable, el importe exento es el 20% del SMI anual teniendo en cuenta [ELEGIR: 12 / 15] meses, por lo que no ha habido tales diferencias cotizables y, por tanto, el acta de liquidación no se ajusta a derecho.

— (Derivación de la responsabilidad del sujeto obligado al pago) concretamente, en dicha acta se le reclama la cantidad de [IMPORTE] euros por deudas por cuotas pendientes en el período del [FECHA DE INICIO] al [FECHA DE FIN], por considerarle responsable solidario de la misma en su condición de empresa principal de la deudora durante el tiempo de vigencia de la contrata.

Esta parte considera que no concurre el requisito de que la deudora estuviera realizando actividad propia de la comitente, ni utilizan ninguna de las dos personas trabajadoras de la otra, ni participa del capital social ni tiene participación en la empresa deudora, por lo que el acta de liquidación no se ajusta a derecho.

— (Aplicación indebida de bonificaciones en las cotizaciones) concretamente, en dicha acta se reclama a mi representado la cantidad de [IMPORTE] euros derivada de la aplicación indebida de bonificaciones en las cotizaciones en el período del [FECHA DE INICIO] al [FECHA DE FIN].

Esta parte considera que el acta de liquidación no se ajusta a derecho, por varios motivos:

[OPCIONAL — incluir si procede]

- La interpretación que hace la resolución de la normativa sobre bonificaciones a la Seguridad Social contraviene la política de empleo.

[OPCIONAL — incluir si procede]

- Asimismo, supone una sanción encubierta a la empresa, y el principio non bis in idem, puesto que levantarla sin advertencia previa comporta indefensión, arbitrariedad, vulneración de los propios actos, de la confianza legítima y del principio de igualdad.

[OPCIONAL — incluir si procede]

- Vulnera el principio de los propios actos y los derechos legítimamente adquiridos, la buena fe y la confianza legítima, así como los principios de igualdad y proporcionalidad.

[OPCIONAL — incluir si procede]

- La forma en que se ha dictado la resolución recurrida constituye una flagrante vía de hecho, que excede de la legalidad ordinaria, y cita una sentencia de la Sala de lo Social del Tribunal Supremo [TRIBUNAL, FECHA Y N.º DE RECURSO O ECLI] que no se refiere a la obligación de ingresar las cuotas en descubierto por indebida aplicación de bonificaciones, sino al alcance de la responsabilidad empresarial en orden al pago de las prestaciones cuando existen deficiencias en la cotización a la Seguridad Social.

TERCERA.- Que, de conformidad con lo expuesto y en base a la normativa indicada al inicio, interpongo el presente recurso de alzada dentro del plazo de un mes desde la notificación de la resolución.

Por lo que,

SOLICITO DE V.I. que, teniendo por presentado este escrito, junto con los documentos probatorios que lo acompañan, tenga por formalizado el recurso de alzada contra la resolución de fecha [DÍA, MES Y AÑO], dictada por [ÓRGANO QUE LA DICTÓ], para que, previa instrucción del pertinente procedimiento, con apertura del período de prueba, dicte resolución por la que se declare la nulidad de aquélla, dejándose la misma sin efecto o, subsidiariamente, se reduzca la liquidación de cuotas a [IMPORTE] euros.

Es de Justicia que pido en [LOCALIDAD], a [DÍA] de [MES] de [AÑO].

D./Dña. [NOMBRE Y APELLIDOS DEL RECURRENTE O DE SU REPRESENTANTE]
