# Seguridad Social: reclamaciones previas y recursos administrativos

> Plugin de Claude Code `formularios-seguridad-social-tramites` · **9 formularios** · Seguridad Social · normativa revisada el 24-11-2026 · requiere Jurisprudenciator

## Para qué sirve

Para la vía administrativa ante el INSS, la TGSS, el SEPE y la Inspección de Trabajo: reclamaciones previas, recursos de alzada contra actas y sanciones, solicitudes de prestaciones y certificados de silencio.

Cada formulario es una skill: Claude lo rellena contigo paso a paso y te entrega el documento en Word, con las normas comprobadas en el BOE. Cada skill explica en su `SKILL.md` qué es el formulario, para qué sirve, cómo se usa, qué datos necesita y qué avisos normativos lleva.

## Qué puedes hacer con él

Estos son los tipos de documento que trae, con algunos ejemplos (la lista completa de los 9 está al final):

- **Demandas, peticiones y solicitudes iniciales** (2). Por ejemplo: Recurso contencioso-administrativo frente a actas de la Inspección de Trabajo y Seguridad Social; Solicitud de reconocimiento del derecho a asistencia sanitaria como titular.
- **Recursos** (2). Por ejemplo: Recurso de alzada contra sanción de Seguridad Social a empresarios, entidades formativas y autónomos; Recurso de alzada frente a un acta de liquidación (art. 34 LGSS).
- **Comunicaciones, requerimientos y cartas** (2). Por ejemplo: Reclamación previa por denegación de incapacidad permanente total cualificada a un autónomo; Reclamación previa por denegación de incapacidad permanente absoluta a un trabajador autónomo.
- **Escritos de trámite y otros** (3). Por ejemplo: Pensión asistencial por ancianidad para españoles de origen retornados; Prestación por razón de necesidad por incapacidad o ancianidad para españoles de origen; Prestación para españoles desplazados al extranjero de menores por la guerra civil.

## Cómo se usa

1. **Pídelo con tus palabras.** Cuéntale a Claude qué documento necesitas y para qué caso; él elige el formulario. Por ejemplo:
   - «Reclamación previa contra la denegación de una prestación»
   - «Recurso de alzada contra un acta de liquidación de cuotas»
   - «Alegaciones a un acta de infracción en materia de Seguridad Social»
2. **Si no da con el formulario**, empieza por el índice del plugin: escribe `/formularios-seguridad-social-tramites:indice` y cuéntale lo que necesitas. Te propondrá el formulario que mejor encaja (o dos o tres para que elijas).
3. **Si ya sabes cuál quieres**, llámalo por su nombre de skill, por ejemplo `/formularios-seguridad-social-tramites:recurso-contencioso-administrativo-frente-actas-ss-038`. Los nombres están en la lista de formularios de abajo.

## Qué hace Claude cuando usas un formulario

1. Comprueba que Jurisprudenciator está conectado. Si no lo está, se para y te dice cómo conectarlo: no redacta nada sin él. Todos los datos jurídicos del documento (artículos vigentes, sentencias con su ECLI, datos registrales) salen de Jurisprudenciator; nunca de memoria.
2. Te pide en una sola tanda los datos del caso (partes, órgano, fechas, importes…). Lo que no sepas queda como hueco visible.
3. Resuelve contigo las opciones que el formulario deja abiertas y decide qué párrafos opcionales entran según los hechos.
4. Aplica las notas de actualización de la revisión del 24-11-2026 (reformas legales, órganos judiciales de la LO 1/2025, plazos).
5. Comprueba en el BOE, con Jurisprudenciator, cada norma que cita el documento; si alguna ha cambiado, usa la redacción vigente y te lo dice.
6. Te entrega el documento en Word **tal cual es el formulario**: empieza por su primera línea, sin títulos, notas ni explicaciones añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. En el chat te dice lo que queda pendiente y, si es un escrito, el plazo y ante quién se presenta.

El resultado es un borrador para que lo revise un profesional antes de usarlo.

## Antes de empezar

- **Dónde funciona:** en Claude Code y en Claude (web, escritorio y Cowork). Se instala desde este repositorio de GitHub o subiendo el ZIP del plugin.
- **Jurisprudenciator es imprescindible:** el plugin trae el conector y cada skill trabaja siempre con él. Sin una cuenta de Jurisprudenciator conectada, las skills se paran y no redactan nada. La primera vez hay que iniciar sesión (en Claude Code, con `/mcp`; o con tu URL personal: https://jurisprudenciator.lexiaipro.org/instalacion). Si ya tienes Jurisprudenciator conectado en Claude, las skills usan ese.
- **Espacio que ocupa:** unos 586 tokens en cada conversación mientras esté activado, porque Claude lleva en memoria la descripción de cada skill. Activa solo los plugins que vayas a usar; los demás puedes desactivarlos sin desinstalarlos (`claude plugin disable formularios-seguridad-social-tramites@formularios-juridicos-seguridad-social-espana`).

## Instalación

En Claude Code, añade el catálogo (solo la primera vez) e instala el plugin:

```
/plugin marketplace add DerechoVirtual/formularios-juridicos-seguridad-social-espana
/plugin install formularios-seguridad-social-tramites@formularios-juridicos-seguridad-social-espana
```

En Claude (web, escritorio o Cowork): **Personalizar → Plugins → Añadir marketplace** con la dirección `https://github.com/DerechoVirtual/formularios-juridicos-seguridad-social-espana`, o sube el ZIP del plugin ([descargar ZIP](https://github.com/DerechoVirtual/formularios-juridicos-seguridad-social-espana/releases/latest/download/formularios-seguridad-social-tramites.zip)).

Para comprobar que está instalado: `claude plugin list`.

## Lista completa de formularios (9)

| Código | Formulario | Skill |
|---|---|---|
| SS-038 | Recurso contencioso-administrativo frente a actas de la Inspección de Trabajo y Seguridad Social | `recurso-contencioso-administrativo-frente-actas-ss-038` |
| SS-039 | Recurso de alzada contra sanción de Seguridad Social a empresarios, entidades formativas y autónomos | `recurso-alzada-contra-sancion-seguridad-social-ss-039` |
| SS-040 | Recurso de alzada frente a un acta de liquidación (art. 34 LGSS) | `recurso-alzada-frente-acta-liquidacion-art-34-lgss-ss-040` |
| SS-041 | Solicitud de reconocimiento del derecho a asistencia sanitaria como titular | `solicitud-reconocimiento-derecho-asistencia-sanitaria-ss-041` |
| SS-042 | Pensión asistencial por ancianidad para españoles de origen retornados | `pension-asistencial-ancianidad-espanoles-origen-ss-042` |
| SS-043 | Prestación por razón de necesidad por incapacidad o ancianidad para españoles de origen | `prestacion-razon-necesidad-incapacidad-ancianidad-ss-043` |
| SS-044 | Prestación para españoles desplazados al extranjero de menores por la guerra civil | `prestacion-espanoles-desplazados-extranjero-menores-ss-044` |
| SS-045 | Reclamación previa por denegación de incapacidad permanente total cualificada a un autónomo | `reclamacion-previa-denegacion-incapacidad-permanente-ss-045` |
| SS-046 | Reclamación previa por denegación de incapacidad permanente absoluta a un trabajador autónomo | `reclamacion-previa-denegacion-incapacidad-permanente-ss-046` |

## Privacidad

Ver `PRIVACY.md`.
