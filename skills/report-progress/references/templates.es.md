<p align="right">Idioma:&emsp;<a href="templates.md" style="vertical-align:middle"><img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-off.svg" align="middle" style="vertical-align:middle"></a> <img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-on.svg" align="middle" style="vertical-align:middle"></p>

[🏠 Project Manager](../../../README.es.md) / [Reportar el avance](../SKILL.es.md)

# Plantillas del reporte de avance

Fuente: *PMBOK Guide*, 7.ª edición, apartado 4.6.7. Un status report lleva las mismas secciones, en el mismo orden, cada vez. Las notas de práctica de PMI añaden que se queda corto, informa resultados y pone la mala noticia y la decisión donde el lector las ve. Un proyecto adapta las secciones. No sustituye el reporte por un texto libre.

Este archivo elige la plantilla. No es un reporte.

## De serie

| Id | Manual | Cuándo |
| --- | --- | --- |
| `status` | [status-report.es.md](status-report.es.md) | El periodo, el estado, lo que terminó, lo que está bloqueado y lo que sigue. Es la de partida. |

## Qué archivo se lee

La carpeta de salida es `adrenaline/project-manager/`, o la ruta `outputDirs["plugin-project-manager"]` de `.cursor/adrenaline.json` cuando es relativa, no tiene `..` y no es absoluta. Si `adrenaline/project-manager/` aún no existe y `project-manager/` en la raíz ya tiene el `ORIGIN.json` o el `STATUS.md` de este plugin, se usa esa carpeta.

1. La persona nombra un id. Busca `<salida>/templates/status-report/<id>.md`. Si existe, es la plantilla.
2. Si no existe, y el id es `status`, lee [status-report.es.md](status-report.es.md).
3. Si el id no es un archivo del proyecto ni `status`, no escribas el reporte. Nombra `status` y cada `<salida>/templates/status-report/*.md` que haya.
4. Si no nombran plantilla, usa `status`. Regístralo bajo Assumed: plantilla `status`, porque no se eligió ninguna. Nombra cualquier plantilla del proyecto que se haya encontrado. Se cambia nombrando el id en `/pm-status`. Se regenera el reporte con `/pm-status`.

Una plantilla del proyecto no pisa el id de serie `status`. Para cambiar la forma, se le da otro id. El archivo de serie no se edita desde un proyecto.

## Una plantilla del proyecto

Ruta: `<salida>/templates/status-report/<id>.md`. `<id>` va en inglés, en minúsculas y con guiones, y no es `status`.

```markdown
---
id: acme-weekly
piece: status-report
based_on: status
---

## Header
required
Proyecto, periodo y fecha de este reporte.

## Decisions needed
required
Lo que se pide, a quién y para cuándo. Ninguna, cuando no hay petición.
```

`based_on` es `status`. Las reglas de redacción de [status-report.es.md](status-report.es.md) siguen vigentes.

- Un encabezado `required` de la base se queda, con el significado de esa base. El encabezado visible se puede renombrar.
- Un encabezado `optional` de la base se puede quitar.
- Un encabezado nuevo está permitido y pasa a ser obligatorio en cada reporte que nombre este id.
- Un costo, una previsión, una fecha de línea base y el nombre de una persona se escriben solo cuando la persona los da. Un encabezado nuevo no da permiso para inventarlos.
- El artefacto sigue el idioma del pedido. Se traducen los encabezados. Se conserva el id.
- Las instrucciones bajo un encabezado no se copian al reporte.

Cuando la persona pide crear o cambiar una plantilla del proyecto, escribe solo ese archivo. Crea la carpeta de salida si falta, y escribe `ORIGIN.json` junto a `STATUS.md` si falta alguno. No escribas un reporte en ese turno, salvo que también lo hayan pedido.

## Done

Este archivo no es una situación. La entrega es el reporte de avance. Evalúa `## Done` en el manual que este archivo elige. La plantilla que queda anotada en el reporte es la que se eligió aquí.
