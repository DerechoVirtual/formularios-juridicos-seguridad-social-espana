---
name: indice
description: "Índice de los 15 formularios de Seguridad Social: reclamaciones previas y recursos administrativos. Úsala cuando el usuario pida un documento de esta materia y no esté claro qué formulario usar: propone el adecuado y lo abre. Requiere Jurisprudenciator."
---

# Seguridad Social: reclamaciones previas y recursos administrativos: índice de formularios

> Plugin `formularios-seguridad-social-tramites` · 15 formularios · normativa revisada el 25-11-2026.

## Qué es

Para la vía administrativa ante el INSS, la TGSS, el SEPE y la Inspección de Trabajo: reclamaciones previas, recursos de alzada contra actas y sanciones, solicitudes de prestaciones y certificados de silencio.

## Cómo se usa

Cuéntale a Claude qué documento necesitas y para qué caso. Esta skill busca en la lista de abajo el formulario que mejor encaja (por tipo de documento y por su nombre) y lo abre. Si hay dos o tres que encajan, te los propone para que elijas.

Ejemplos de petición:

- «Reclamación previa contra la denegación de una prestación»
- «Recurso de alzada contra un acta de liquidación de cuotas»
- «Alegaciones a un acta de infracción en materia de Seguridad Social»

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

### Cómo elegir

Busca por tipo de documento y por nombre. Cada formulario es una skill de este plugin (`/formularios-seguridad-social-tramites:<skill>`). Si dudas entre dos, elige el que mejor encaje con los hechos y dilo; si la petición es ambigua, propón al usuario los dos o tres formularios que mejor encajan y pregúntale cuál quiere. Las reglas del tema están en `marco.md`.

### Cómo usar el formulario elegido

Invoca su skill. Si esa skill no aparece en tu lista de skills disponibles (puede pasar cuando hay muchas skills instaladas), lee directamente su fichero `SKILL.md`: está en la carpeta hermana de esta (`../<skill>/SKILL.md`). Síguelo igual que si la hubieras invocado: el formulario que se rellena está en `../<skill>/assets/formulario.md` y la guía del tema es el `marco.md` de esta carpeta.

### Demandas, peticiones y solicitudes iniciales (2)

| Código | Formulario | Skill |
|---|---|---|
| SS-038 | Recurso contencioso-administrativo frente a actas de la Inspección de Trabajo y Seguridad Social | `recurso-contencioso-administrativo-frente-actas-ss-038` |
| SS-041 | Solicitud de reconocimiento del derecho a asistencia sanitaria como titular | `solicitud-reconocimiento-derecho-asistencia-sanitaria-ss-041` |

### Contestaciones, oposiciones y alegaciones (1)

| Código | Formulario | Skill |
|---|---|---|
| SS-103 | Alegaciones del interesado en un expediente ante la Dirección Provincial de la entidad gestora | `alegaciones-interesado-expediente-ante-direccion-ss-103` |

### Recursos (2)

| Código | Formulario | Skill |
|---|---|---|
| SS-039 | Recurso de alzada contra sanción de Seguridad Social a empresarios, entidades formativas y autónomos | `recurso-alzada-contra-sancion-seguridad-social-ss-039` |
| SS-040 | Recurso de alzada frente a un acta de liquidación (art. 34 LGSS) | `recurso-alzada-frente-acta-liquidacion-art-34-lgss-ss-040` |

### Comunicaciones, requerimientos y cartas (5)

| Código | Formulario | Skill |
|---|---|---|
| SS-045 | Reclamación previa por denegación de incapacidad permanente total cualificada a un autónomo | `reclamacion-previa-denegacion-incapacidad-permanente-ss-045` |
| SS-046 | Reclamación previa por denegación de incapacidad permanente absoluta a un trabajador autónomo | `reclamacion-previa-denegacion-incapacidad-permanente-ss-046` |
| SS-099 | Reclamación previa ante el INSS en materia de prestaciones de la Seguridad Social | `reclamacion-previa-ante-inss-materia-prestaciones-ss-099` |
| SS-101 | Reclamación previa contra la denegación del SOVI por no tener 1800 días cotizados ni Retiro Obrero | `reclamacion-previa-contra-denegacion-sovi-no-tener-1800-ss-101` |
| SS-102 | Reclamación previa por denegarse el SOVI sin computar cotizaciones a mutualidades anteriores a 1967 | `reclamacion-previa-denegarse-sovi-sin-computar-ss-102` |

### Escritos de trámite y otros (5)

| Código | Formulario | Skill |
|---|---|---|
| SS-042 | Pensión asistencial por ancianidad para españoles de origen retornados | `pension-asistencial-ancianidad-espanoles-origen-ss-042` |
| SS-043 | Prestación por razón de necesidad por incapacidad o ancianidad para españoles de origen | `prestacion-razon-necesidad-incapacidad-ancianidad-ss-043` |
| SS-044 | Prestación para españoles desplazados al extranjero de menores por la guerra civil | `prestacion-espanoles-desplazados-extranjero-menores-ss-044` |
| SS-100 | Escrito al INSS para optar entre prestaciones incompatibles | `escrito-inss-optar-entre-prestaciones-incompatibles-ss-100` |
| SS-104 | Ampliación o aclaración de una reclamación previa ya presentada | `ampliacion-aclaracion-reclamacion-previa-ya-presentada-ss-104` |
