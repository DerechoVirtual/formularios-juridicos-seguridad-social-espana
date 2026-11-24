---
name: pension-asistencial-ancianidad-espanoles-origen-ss-042
description: "Pensión asistencial por ancianidad para españoles de origen retornados. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Pensión asistencial por ancianidad para españoles de origen retornados

> Formulario **SS-042** del plugin **Seguridad Social: reclamaciones previas y recursos administrativos** (`formularios-seguridad-social-tramites`) · Seguridad Social › Solicitudes, reclamaciones y recursos ante la Administración · normativa revisada el 24-11-2026.

## Qué es

Ficha práctica y modelo de solicitud para pedir el reconocimiento de la pensión asistencial por ancianidad a favor de españoles de origen retornados a España que carecen de recursos.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Pensión asistencial por ancianidad para españoles de origen retornados» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Pensión asistencial por ancianidad para españoles de origen retornados” para mi caso». También puedes invocarla directamente con `/formularios-seguridad-social-tramites:pension-asistencial-ancianidad-espanoles-origen-ss-042`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-seguridad-social-tramites:indice`.

## Qué contiene esta skill

- `formulario.md`: el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `marco.md`: la guía del tema (Seguridad Social: reclamaciones previas y recursos administrativos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (3 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] PROVINCIA (2 veces)
- [ ] AÑO
- [ ] CORREO ELECTRÓNICO
- [ ] DETALLE DE INGRESOS, SI LOS HAY
- [ ] DNI/NIE
- [ ] DOMICILIO
- [ ] DÍA
- [ ] EDAD
- [ ] FECHA DE RETORNO
- [ ] IBAN
- [ ] IMPORTE
- [ ] MES
- [ ] PAÍS DE RESIDENCIA
- [ ] RELACIÓN DE DOCUMENTOS
- [ ] TELÉFONO

## Normas que cita el formulario

- No cita artículos concretos; Claude localizará las normas aplicables con Jurisprudenciator si el documento las necesita.

---

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

### Avisos de actualización (2) — se aplican en el texto, nunca se copian en el documento

- Al principio del formulario: el original no traía el texto del formulario; modelo redactado de nuevo conforme a la normativa vigente.
- Junto a «…o de la ficha se refiere al artículo 25 del Real Decreto 8/2008, de 11 de enero.»: comprobar el artículo 25 del Real Decreto 8/2008 y la norma reguladora vigente de la pensión asistencial por ancianidad de retornados (en particular, el Real Decreto 728/1993 y sus modificaciones, y el Estatuto de la ciudadanía española en el exterior, Ley 40/2006), por si hubieran sido modificados o sustituidos.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

FICHA PRÁCTICA

Qué es: prestación asistencial que garantiza un mínimo de subsistencia a los españoles de origen que, habiendo residido en el extranjero, han retornado a España, han cumplido la edad exigida (65 años) y carecen de recursos suficientes. El título de la ficha se refiere al artículo 25 del Real Decreto 8/2008, de 11 de enero.

Ante quién y por dónde se presenta: la solicitud se presenta en el impreso oficial, que debe descargarse de la sede electrónica de la Seguridad Social o del Ministerio competente en materia de Seguridad Social y migraciones, ante la Dirección Provincial del INSS del lugar de residencia, por sede electrónica, de forma presencial con cita previa o por los demás medios del artículo 16 de la Ley 39/2015.

Requisitos habituales: ser español de origen; haber retornado a España y residir legalmente en territorio español; haber cumplido 65 años; carecer de recursos económicos suficientes, en los términos y límites fijados cada año; haber residido en el exterior durante el periodo mínimo que exija la norma.

Datos que se piden: identificación de la persona solicitante y, en su caso, de la unidad familiar; fecha de retorno a España; países y periodos de residencia en el exterior; ingresos y patrimonio propios y de la unidad de convivencia; datos bancarios para el abono.

Documentos que suelen exigirse: documento nacional de identidad o pasaporte; acreditación de la nacionalidad española de origen; certificado de empadronamiento; justificantes de la residencia en el exterior y de la fecha de retorno; declaración de ingresos y patrimonio; certificados de pensiones o prestaciones públicas percibidas en España o en el extranjero.

Cobertura: el reconocimiento de la prestación puede llevar aparejada la asistencia sanitaria; consúltese en el impreso y en la normativa vigente.


### Flujo

1. **Paso 0**: comprueba Jurisprudenciator (arriba).
2. Lee `formulario.md` entero y la parte de `marco.md` que afecte al caso. Limítate a la materia de este formulario: no añadas contenido ajeno a él.
3. Pide los datos de la lista en una sola tanda. Si un dato aparece varias veces, aclara a qué persona o acto corresponde cada vez. Lo que el usuario no sepa se queda como hueco visible con su etiqueta (p. ej. [FECHA]).
4. Resuelve cada [ELEGIR …] y cada [OPCIONAL …] según los hechos, y sustituye cualquier indicación entre paréntesis del formulario («(se describirá…)», «(indicar…)») por el contenido que corresponda. Redacta las partes que dependen del caso (hechos, motivos, descripción de bienes).
5. Aplica los avisos de actualización en el lugar que indican. Comprueba con `buscar_articulo` cada norma citada; si alguna ha cambiado, usa la redacción vigente. Si citas jurisprudencia, localízala con `buscar_sentencias` o `buscar_por_cita` y léela con `leer_sentencias`.
6. Antes de entregarlo, pasa `verificar_escrito` con las frases que citan normas o sentencias y corrige lo que señale.
7. **Documento final = el formulario tal cual, rellenado y limpio.**
   - Empieza exactamente por la primera línea de `formulario.md` y sigue su estructura y su orden hasta la firma.
   - No pongas en el documento título, nombre del formulario o de la skill, código, encabezados, «Para qué sirve», leyendas, avisos, notas de uso, comentarios ni explicaciones. Tampoco marcas [ELEGIR…] u [OPCIONAL…]: ya están resueltas.
   - Formato Word (.docx, con la skill de Word disponible): **Times New Roman 12 pt** en todo el documento, **interlineado 1,15**, **texto justificado**, márgenes de 2,5 cm. Los rótulos del formulario (REUNIDOS, CLÁUSULAS, HECHOS, SUPLICO…) en su propia línea y en negrita, sin cambiar su texto.
8. En el chat (nunca dentro del documento): datos pendientes, partes redactadas por ti, normas y sentencias comprobadas con Jurisprudenciator (y, si algún dato sale de internet, cuál y su enlace) y, si es un escrito judicial o administrativo, el plazo y el órgano ante el que se presenta.

El resultado es un borrador para que lo revise un profesional antes de usarlo.
