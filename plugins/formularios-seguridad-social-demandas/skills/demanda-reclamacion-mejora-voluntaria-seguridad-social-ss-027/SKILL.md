---
name: demanda-reclamacion-mejora-voluntaria-seguridad-social-ss-027
description: "Demanda de reclamación de la mejora voluntaria de Seguridad Social pactada en convenio colectivo. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Demanda de reclamación de la mejora voluntaria de Seguridad Social pactada en convenio colectivo

> Formulario **SS-027** del plugin **Seguridad Social: demandas y recursos ante lo social** (`formularios-seguridad-social-demandas`) · Seguridad Social › Demandas y escritos ante la jurisdicción social · normativa revisada el 24-11-2026.

## Qué es

Mediante Convenio Colectivo pueden mejorarse las prestaciones de la Seguridad Social. La demanda por mejora voluntaria de Seguridad Social (SS) pactada en convenio colectivo se presenta ante el Tribunal cuando la empresa no paga lo acordado (por incapacidad, accidente, etc.), reclamando la cantidad debida, ya que el convenio tiene fuerza de ley y convierte esa mejora en un derecho adquirido para la persona trabajadora. Se debe formalizar con un modelo de demanda de reclamación de cantidad, aportando pruebas y siguiendo los pasos procesales, pudiendo ser necesaria una denuncia previa ante la Inspección de Trabajo para iniciar el expediente.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda de reclamación de la mejora voluntaria de Seguridad Social pactada en convenio colectivo» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda de reclamación de la mejora voluntaria de Seguridad Social pactada en convenio colectivo” para mi caso». También puedes invocarla directamente con `/formularios-seguridad-social-demandas:demanda-reclamacion-mejora-voluntaria-seguridad-social-ss-027`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-seguridad-social-demandas:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Seguridad Social: demandas y recursos ante lo social) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (7 veces)
- [ ] IMPORTE (6 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] Nº (2 veces)
- [ ] Nº DE ARTÍCULO (2 veces)
- [ ] PARTE DEMANDADA (2 veces)
- [ ] CORREO ELECTRÓNICO
- [ ] DNI/NIE
- [ ] GRUPO O CATEGORÍA PROFESIONAL
- [ ] LUGAR
- [ ] NIF
- [ ] Nº DE AFILIACIÓN
- [ ] NÚMERO
- [ ] SECTOR O EMPRESA
- [ ] SEDE
- [ ] TELÉFONO
- [ ] ÁMBITO TERRITORIAL

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

### Avisos de actualización (1) — se aplican en el texto, nunca se copian en el documento

- Junto a «…. A LA SECCIÓN DE LO SOCIAL DEL TRIBUNAL DE INSTANCIA DE [SEDE] – PLAZA N.º [Nº]»: Desde el 31-12-2025 los Juzgados de lo Social son la Sección de lo Social del Tribunal de Instancia; el Tribunal no se numera, se numera la plaza. En la demanda inicial (antes del reparto) se omite la plaza. Fuente: arts. 84.2.i) y 94 LOPJ (red. LO 1/2025); LO 1/2025 DA 1.ª y DT 1.ª (la plaza conserva la numeración del Juzgado; Juzgados de lo Social transformados el 31-12-2025); LOPJ (LO 6/1985), BOE-A-1985-12666; LO 1/2025, BOE-A-2025-76.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Mediante Convenio Colectivo pueden mejorarse las prestaciones de la Seguridad Social. La demanda por mejora voluntaria de Seguridad Social (SS) pactada en convenio colectivo se presenta ante el Tribunal cuando la empresa no paga lo acordado (por incapacidad, accidente, etc.), reclamando la cantidad debida, ya que el convenio tiene fuerza de ley y convierte esa mejora en un derecho adquirido para la persona trabajadora. Se debe formalizar con un modelo de demanda de reclamación de cantidad, aportando pruebas y siguiendo los pasos procesales, pudiendo ser necesaria una denuncia previa ante la Inspección de Trabajo para iniciar el expediente.


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

A LA SECCIÓN DE LO SOCIAL DEL TRIBUNAL DE INSTANCIA DE [SEDE] – PLAZA N.º [Nº]

D./Dña. [NOMBRE Y APELLIDOS], con DNI nº [DNI/NIE], y número de afiliación a la Seguridad Social [Nº DE AFILIACIÓN], y con domicilio a efectos de notificaciones en el Despacho del/de la Letrado/a D./Dña. [NOMBRE Y APELLIDOS], sito en [LOCALIDAD], teléfono [TELÉFONO], correo electrónico [CORREO ELECTRÓNICO], ante ese Tribunal comparezco y como mejor proceda en Derecho, DIGO:

Que mediante el presente escrito formulo DEMANDA DE RECLAMACIÓN DE CANTIDAD POR MEJORA VOLUNTARIA DE SEGURIDAD SOCIAL ESTABLECIDA POR CONVENIO COLECTIVO, frente a [PARTE DEMANDADA] CIF: [NIF], con domicilio en [LOCALIDAD] a fin de que por el Tribunal se dicte Sentencia de conformidad con el suplico de la presente, lo que fundamento en base a los siguientes

HECHOS

PRIMERO.- Que D./Dña. [NOMBRE Y APELLIDOS] ha venido prestando servicios para la referida empresa, desde el [FECHA], a la cual le resulta de aplicación el Convenio Colectivo de [SECTOR O EMPRESA] de ámbito [ÁMBITO TERRITORIAL], percibiendo un salario bruto mensual, con inclusión de prorrata de pagas extras de [IMPORTE] € y ostentado la categoría profesional de [GRUPO O CATEGORÍA PROFESIONAL].

SEGUNDO.- Que en fecha [FECHA] sufrió un grave accidente de trabajo, y desde entonces se encuentra en situación de incapacidad temporal, por lo que se le abona la correspondiente prestación, por un importe de [IMPORTE] euros brutos.

TERCERO.- Que el Convenio de aplicación establece en su artículo [Nº DE ARTÍCULO] una mejora voluntaria de las prestaciones de la Seguridad Social, consistente en una indemnización complementaria de la que perciba por la Seguridad Social a consecuencia de la incapacidad temporal, hasta alcanzar el 100% de su salario convenio más el complemento ad personam, es decir, [IMPORTE] euros brutos.

CUARTO.- Que los efectos del Convenio se retrotraen al [FECHA], por lo que la empresa adeuda al actor desde dicha fecha hasta el [FECHA] un importe bruto de ( € x [Nº] meses) un total de [IMPORTE] EUROS, al cual debe añadírsele el 10% de mora en el pago, dado lo injustificado del comportamiento empresarial, es decir, [IMPORTE] EUROS.

QUINTO.- Que la empresa debe continuar abonándole la indemnización convencional hasta la finalización de la incapacidad temporal.

SEXTO.- Que en fecha [FECHA] se celebró el preceptivo Acto de Conciliación ante el Servicio de Mediación, Arbitraje y Conciliación el cual finalizó sin avenencia, tal y como se acredita mediante copia de la correspondiente acta que se acompaña como documento n.º [NÚMERO] a la presente demanda.

A estos hechos les resultan de aplicación los siguientes:

FUNDAMENTOS DE DERECHO

I. Es competente la Sección de lo Social del Tribunal de Instancia al que se dirige de conformidad con lo dispuesto en los artículos 1, 2.c), 6 y 10.2.b) de la Ley Reguladora de la Jurisdicción Social.

II. El artículo [Nº DE ARTÍCULO] del convenio colectivo aplicable establece una [ELEGIR: indemnización / prestación] complementaria de la que reciba la persona trabajadora de la Seguridad Social hasta alcanzar el 100% de su salario convenio más el complemento ad personam desde el día de la baja médica hasta la fecha de alta o pase a situación de incapacidad en cualquiera de sus grados.

III. Los demás fundamentos jurídicos y jurisprudencia se alegarán en el momento procesal oportuno.

Por todo ello,

SUPLICO A LA SECCIÓN DE LO SOCIAL DEL TRIBUNAL DE INSTANCIA,

que teniendo por presentado este escrito, con sus copias y documentos que se acompañan, lo admita a trámite, tenga por formulada DEMANDA DE CANTIDAD DE MEJORA VOLUNTARIA DE SEGURIDAD SOCIAL contra [PARTE DEMANDADA], cite a los actos de conciliación y juicio a las partes, se siga éste por sus trámites, y en su momento dicte sentencia por la que se condene a la parte demandada a: A) abonar a la persona trabajadora la cantidad que se concretará en el acto del juicio y que a fecha de hoy asciende a [IMPORTE] EUROS, que le adeuda en concepto de cantidad de mejora voluntaria de Seguridad Social establecida por el Convenio Colectivo de aplicación y B) a continuar abonando dicha indemnización convencional hasta la finalización de su incapacidad temporal o pase a situación de incapacidad en cualquiera de sus grados, con todo cuanto más proceda en Derecho.

PRIMER OTROSÍ DIGO:

Que interesa al Derecho de esta parte valerse en el acto del juicio de los siguientes medios de prueba:

DOCUMENTAL:

1.- Para que se tengan por aportados los documentos que se acompañan a este escrito de demanda y los que en su momento se aportarán.

2.- Que se requiera a la empresa demandada al objeto de que aporten con antelación de quince días al Acto del Juicio para que sea estudiado por el Letrado:

- Contrato de trabajo del/de la actor/a;

- Nóminas de la persona trabajadora desde el [FECHA] hasta la fecha de celebración del juicio.

SEGUNDO OTROSÍ DIGO:

Que esta parte asistirá al acto del juicio, acompañada de Letrado/a que le defienda y cuyo domicilio a efectos de citaciones y notificaciones se designa: D./Dña

Por todo lo expuesto,

SUPLICO A LA SECCIÓN DE LO SOCIAL DEL TRIBUNAL DE INSTANCIA,

que se tengan por hechas las anteriores manifestaciones y por solicitadas las pruebas propuestas, admitiéndolas y ordenando lo necesario para su práctica.

En [LUGAR], a [FECHA].
