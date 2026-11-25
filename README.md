# Formularios jurídicos de España para Claude · Seguridad Social

3 plugins de formularios de Seguridad Social, uno por materia. Cada formulario es una skill que Claude rellena paso a paso con los datos del caso y entrega en Word tal cual es el formulario (Times New Roman 11, interlineado 1,15 y texto justificado): 102 skills en total, contando la skill `indice` de cada plugin, que sirve para encontrar el formulario adecuado.

Todas las skills trabajan con **Jurisprudenciator** (https://jurisprudenciator.lexiaipro.org): antes de redactar comprueban que el conector responde y verifican en fuentes oficiales las normas que cita el formulario. Sin Jurisprudenciator conectado, las skills no redactan. Normativa revisada el 25-11-2026.

Las demás jurisdicciones están en repositorios propios: [Mercantil](https://github.com/DerechoVirtual/formularios-juridicos-mercantil-espana), [Civil](https://github.com/DerechoVirtual/formularios-juridicos-civil-espana), [Administrativo y Tributario](https://github.com/DerechoVirtual/formularios-juridicos-administrativo-tributario-espana), [Laboral](https://github.com/DerechoVirtual/formularios-juridicos-laboral-espana), [Penal](https://github.com/DerechoVirtual/formularios-juridicos-penal-espana).

## Instalación

En Claude Code:

```
/plugin marketplace add DerechoVirtual/formularios-juridicos-seguridad-social-espana
/plugin install formularios-seguridad-social-demandas@formularios-juridicos-seguridad-social-espana
```

Cada plugin ocupa contexto en la conversación, así que conviene instalar solo los de las materias con las que se trabaja.

En Claude (web, escritorio y Cowork) se puede añadir este repositorio desde **Personalizar → Plugins → Añadir marketplace** con la dirección `https://github.com/DerechoVirtual/formularios-juridicos-seguridad-social-espana`, o subir cada plugin como ZIP. Los ZIP están en la página de [versiones](https://github.com/DerechoVirtual/formularios-juridicos-seguridad-social-espana/releases/latest).

## Plugins

| Plugin | Contenido | Skills | ZIP |
|---|---|---:|---|
| `formularios-seguridad-social-demandas` | Seguridad Social: demandas y recursos ante lo social | 69 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-seguridad-social-espana/releases/latest/download/formularios-seguridad-social-demandas.zip) |
| `formularios-seguridad-social-tramites` | Seguridad Social: reclamaciones previas y recursos administrativos | 16 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-seguridad-social-espana/releases/latest/download/formularios-seguridad-social-tramites.zip) |
| `formularios-seguridad-social-certificados-y-convenios` | Seguridad Social: certificados, declaraciones y convenios internacionales | 17 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-seguridad-social-espana/releases/latest/download/formularios-seguridad-social-certificados-y-convenios.zip) |

## Estructura

```
.claude-plugin/marketplace.json  catálogo del marketplace
plugins/<plugin>/                .claude-plugin/plugin.json, .mcp.json, skills/<skill>/SKILL.md y assets/formulario.md, README.md, PRIVACY.md, LICENSE
```

## Aviso

Los documentos que se generan son borradores que debe revisar un abogado; no constituyen asesoramiento jurídico. Las skills no guardan datos del cliente y las consultas a Jurisprudenciator describen el problema jurídico, no los datos personales.

Soporte: https://jurisprudenciator.lexiaipro.org/incidencias · Licencia: ver [LICENSE](LICENSE).
