---
name: incidente-nulidad-providencia-confirma-decreto-termina-ss-023
description: "Incidente de nulidad de la providencia que confirma el decreto que termina el monitorio. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Incidente de nulidad de la providencia que confirma el decreto que termina el monitorio

> Formulario **SS-023** del plugin **Seguridad Social: demandas y recursos ante lo social** (`formularios-seguridad-social-demandas`) · Seguridad Social › Demandas y escritos ante la jurisdicción social · normativa revisada el 24-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Incidente de nulidad de la providencia que confirma el decreto que termina el monitorio» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Incidente de nulidad de la providencia que confirma el decreto que termina el monitorio” para mi caso». También puedes invocarla directamente con `/formularios-seguridad-social-demandas:incidente-nulidad-providencia-confirma-decreto-termina-ss-023`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-seguridad-social-demandas:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Seguridad Social: demandas y recursos ante lo social) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (3 veces)
- [ ] MOTIVO (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] DERECHO FUNDAMENTAL VULNERADO
- [ ] LUGAR
- [ ] NOMBRE DE LA PARTE
- [ ] Nº
- [ ] Nº DE PROCEDIMIENTO
- [ ] OTROS DATOS
- [ ] SEDE

## Normas que cita el formulario

- art. 241.1 Ley Orgánica 6/1985

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

Contra el auto de despacho de la ejecución procederá oposición por: la falta de notificación del requerimiento; las posibles infracciones en que hubiera de incurrir la resolución y el cumplimiento o incumplimiento de los presupuestos y requisitos procesales exigidos; pago o cumplimiento documentalmente justificado, prescripción de la acción ejecutiva u otros hechos impeditivos, extintivos o excluyentes de la responsabilidad que se pretenda ejecutar siempre que hubieren acaecido con posterioridad a su constitución del título, no siendo la compensación de deudas admisible como causa de oposición a la ejecución.

A LA SECCIÓN DE LO SOCIAL DEL TRIBUNAL DE INSTANCIA DE [SEDE] – PLAZA N.º [Nº]

D./Dña. [NOMBRE Y APELLIDOS], Letrado/a, actuando en nombre y representación de D./Dña. [NOMBRE Y APELLIDOS], conforme tengo acreditado en los autos de Procedimiento Monitorio núm. [Nº DE PROCEDIMIENTO] seguido por [NOMBRE DE LA PARTE] ante ese Tribunal, ante el mismo comparezco y DIGO:

Que, con fecha [FECHA], ese órgano jurisdiccional dictó Providencia poniendo fin al citado Procedimiento Monitorio, por haber interpuesto este Letrado/a recurso de reposición en lugar de revisión contra el Decreto de finalización de aquél.

Que, por medio del presente escrito y al amparo de lo establecido en el artículo 241.1 y 2 de la Ley Orgánica 6/1985, de 1 de julio, del Poder Judicial, y por la Ley Orgánica 6/2007, de 24 de mayo, por la que se modifica la Ley Orgánica 2/1979, de 3 de octubre, del Tribunal Constitucional, solicito la declaración de nulidad de la referida providencia, y, en su caso, del Decreto que la precedió en razón de los siguientes MOTIVOS:

1º Es competente para resolver esta solicitud ese órgano jurisdiccional, pues fue el autor de la providencia y del Decreto en el procedimiento en el que fue vulnerado el derecho fundamental del recurrente a [DERECHO FUNDAMENTAL VULNERADO], resolución que ha adquirido firmeza.
El menoscabo [ELEGIR: del mencionado derecho fundamental / de los mencionados derechos fundamentales] no fue posible denunciarlo antes de recaer la resolución judicial por las siguientes causas: [MOTIVO], y aquélla no es susceptible de recurso en el que quepa reparar la indefensión sufrida.
2º La presente solicitud se presenta dentro del plazo de veinte días [OTROS DATOS], sin que, en este último supuesto, haya transcurrido en todo caso el plazo de cinco años desde la notificación de la resolución en cuestión.

En su virtud,

SUPLICO AL TRIBUNAL que, teniendo por presentado este escrito con sus copias y los documentos que lo acompañan, se sirva admitirlo, tenga por solicitada la declaración de nulidad de la providencia de fecha [FECHA] y, en su caso, de las actuaciones procesales que lo procedieron y que se consideren viciadas y causantes de indefensión, y, en consecuencia, lo estime, declarando la nulidad del mismo y, en su caso, la revocación de las actuaciones, con conservación de los trámites que se consideren no afectados por los citados defectos de forma y/o la realización de los trámites que correspondan, con lo demás que proceda en Derecho.

Es de Justicia que pido en [LUGAR], a [FECHA].

OTROSÍ DIGO: Que al amparo de lo establecido en el artículo 241.2 de la citada Ley Orgánica del Poder Judicial, solicito la suspensión de la ejecución o eficacia de la resolución cuya nulidad se solicita, pues de otro modo el presente incidente perdería su finalidad, por las siguientes razones: [MOTIVO].

Es de justicia que en el mismo lugar y fecha pido.

Firma del/de la Letrado/a:
