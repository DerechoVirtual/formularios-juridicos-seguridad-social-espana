---
name: demanda-contra-mutua-extinguirse-subsidio-incapacidad-ss-008
description: "Demanda contra la mutua por extinguirse el subsidio de incapacidad temporal por incomparecencia. Lo redacta con los datos del caso y comprueba las normas con Jurisprudenciator."
---

# Demanda contra la mutua por extinguirse el subsidio de incapacidad temporal por incomparecencia

> Formulario **SS-008** del plugin **Seguridad Social: demandas y recursos ante lo social** (`formularios-seguridad-social-demandas`) · Seguridad Social › Demandas y escritos ante la jurisdicción social · normativa revisada el 24-11-2026.

## Qué es

Demanda ante el orden social contra la Mutua que ha extinguido el subsidio de incapacidad temporal y dado el alta por incomparecencia del beneficiario a un reconocimiento médico, para que se anule el alta y se declare que continúa la situación de baja; exige reclamación previa.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Demanda contra la mutua por extinguirse el subsidio de incapacidad temporal por incomparecencia» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Demanda contra la mutua por extinguirse el subsidio de incapacidad temporal por incomparecencia” para mi caso». También puedes invocarla directamente con `/formularios-seguridad-social-demandas:demanda-contra-mutua-extinguirse-subsidio-incapacidad-ss-008`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-seguridad-social-demandas:indice`.

## Qué contiene esta skill

- `formulario.md`: el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `marco.md`: la guía del tema (Seguridad Social: demandas y recursos ante lo social) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (8 veces)
- [ ] DENOMINACIÓN DE LA MUTUA (3 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] RELACIÓN DE DOCUMENTOS (2 veces)
- [ ] AÑO
- [ ] CATEGORÍA / GRUPO PROFESIONAL
- [ ] CENTRO DE TRABAJO
- [ ] CONVENIO COLECTIVO
- [ ] CORREO ELECTRÓNICO
- [ ] DENOMINACIÓN SOCIAL
- [ ] DIAGNÓSTICO
- [ ] DIRECCIÓN DEL DESPACHO
- [ ] DNI/NIE
- [ ] DOMICILIO DE LA MUTUA
- [ ] DÍA
- [ ] ENTIDAD O PERSONA REQUERIDA
- [ ] EXPLICAR EL MOTIVO DE LA INCOMPARECENCIA
- [ ] FECHA DE ANTIGÜEDAD
- [ ] IMPORTE
- [ ] JORNADA
- [ ] MES
- [ ] N.º DE AFILIACIÓN
- [ ] N.º DE DOCUMENTOS
- [ ] N.º DE EXPEDIENTE
- [ ] NOMBRE DEL LETRADO/A
- [ ] NOMBRE Y APELLIDOS
- [ ] SEDE
- [ ] TELÉFONO
- [ ] TIPO DE CONTRATO

## Normas que cita el formulario

- art. 174.1 LGSS
- art. 1104 Código Civil
- art. 1256 Código Civil
- art. 59.4 Ley 30/1992
- art. 42 Real Decreto 1829/1999

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

- Junto a «… que no debe aplicarse en este supuesto litigioso el art. 59.4 de la Ley 30/1992»: La Ley 30/1992 está derogada; hoy rigen la Ley 39/2015 (procedimiento administrativo común) y la Ley 40/2015 (régimen jurídico del sector público). La Ley 39/2015 suprimió la reclamación previa a la vía judicial civil.
- Junto a «…o, en la fecha en la que el trabajador recogió el burofax en la oficina postal».»: las referencias a la Ley 30/1992 y a la LRJAPYPAC dentro de la cita jurisprudencial son históricas (la doctrina se dictó bajo esa ley, hoy sustituida por las Leyes 39/2015 y 40/2015); comprobar el artículo equivalente en la Ley 39/2015 antes de invocarlas, y verificar la vigencia del art. 42 del Real Decreto 1829/1999 y las referencias de las sentencias citadas.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

NOTAS DE USO (suprimir antes de presentar):

La mutua puede extinguir el derecho al subsidio de incapacidad temporal por contingencias comunes cuando exista incomparecencia injustificada del beneficiario a las convocatorias para exámenes y reconocimientos médicos, pues esa causa de extinción está expresamente prevista en el art. 174.1 de la Ley General de la Seguridad Social (LGSS). Además, el art. 82.4.d) LGSS atribuye a las mutuas la facultad de realizar actos de control y seguimiento desde el mismo día de la baja médica y dispone que la incomparecencia injustificada a las citaciones para examen o reconocimiento médico será causa de extinción del derecho.

La demanda contra la mutua por extinción de la prestación de incapacidad temporal por incomparecencia debe centrarse en verificar si concurrió realmente una incomparecencia injustificada y, sobre todo, si la mutua respetó íntegramente el procedimiento del art. 9 del Real Decreto 625/2014 y del art. 82.4 LGSS: citación con cuatro días hábiles de antelación, advertencia expresa de consecuencias, suspensión cautelar previa, concesión de diez días hábiles para justificar, valoración de la justificación aportada, acuerdo motivado y notificación eficaz. Si cualquiera de esos requisitos falta, existen fundamentos para solicitar la anulación de la extinción y la reposición del subsidio. La acción exige reclamación previa del art. 71 de la Ley 36/2011, reguladora de la jurisdicción social (LRJS).


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
