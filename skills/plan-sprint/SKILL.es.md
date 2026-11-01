---
name: plan-sprint
description: Writes the sprint plan, the goal, the selected items, and how they will be delivered. Use it when someone asks what this period will finish.
---

<p align="right">Idioma:&emsp;<a href="SKILL.md" style="vertical-align:middle"><img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-off.svg" align="middle" style="vertical-align:middle"></a> <img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-on.svg" align="middle" style="vertical-align:middle"></p>

[🏠 Project Manager](../../README.es.md)

# Planear el sprint

Un sprint. La meta dice para qué vale el periodo. Los ítems son los que eligió la persona. El plan apunta al trabajo y no lo estima.

Fuente: Scrum Guide, 2020. Sprint Planning.

## Antes de escribir

1. Lee [sprint](references/sprint.es.md). Escribe solo esa situación.
2. Cita un resultado accepted de `plugin-product` cuando la persona ata la meta a ese archivo. No escribas el resultado. No dimensionas los ítems.

## Entrega

El archivo es `<NNN>-sprint-<tema>.md` en `adrenaline/project-manager/`, o en `outputDirs["plugin-project-manager"]` cuando esa ruta es válida. `<NNN>` es el siguiente número libre de esa carpeta. El artefacto sigue el idioma del pedido. El id de tipo se queda `sprint`. Las columnas de `STATUS.md` siguen `N`, `archivo`, `estado`, `sustituye`, `notas`. `ORIGIN.json` va a su lado, con `suite` `ADRenaline-Suite`, `plugin` `plugin-project-manager`, `repository` `https://github.com/ADRenaline-Suite/plugin-project-manager` y `convention` `adr-001`. No tiene fila en `STATUS.md`. Un archivo numerado de un proyecto nombrado va en `<asunto>/`. Un archivo numerado de todo el producto se queda en la raíz de la salida. `<NNN>` es el siguiente libre de toda la carpeta. La celda `archivo` es `<asunto>/<archivo>` cuando hay asunto (`doc/arch/adr-008-asunto-subcarpeta.md`).

## Ejemplo

La persona dice que las próximas dos semanas terminan el pago con tarjeta, y nombra el caso de uso que ya tiene. El archivo registra esa meta, esas fechas, ese archivo y la tarea entre repositorios si existe. No añade un segundo ítem y no escribe un punto de historia.

## Done

Antes de cerrar, evalúa esta lista y la lista `## Done` de la referencia de esta situación. Un command fija la situación: usa la referencia que ese command nombra. Cada ítem es cierto, o corriges la entrega en este turno. No dejes un archivo que falle un ítem. No lo marques `accepted` mientras un ítem falle. Una plantilla que nombra la referencia se aplica y se registra bajo Assumed; la entrega usa el estado que nombra esa referencia. Un sprint sin periodo dado por la persona no es una lista fallida: la referencia deja el archivo `proposed` y nombra el hueco.

- La situación de este turno es la única que se escribe, salvo que el pedido haya pedido dos. Cada entrega tiene su `<NNN>`.
- Los archivos están solo en la carpeta de salida, con el nombre que dice Entrega. `<NNN>` no se reutiliza. `STATUS.md` coincide con los archivos y con el estado que esta situación permite. `ORIGIN.json` está en esa carpeta, sus cuatro campos coinciden con este plugin y no tiene fila en `STATUS.md`. Un hueco que la referencia deja en `proposed` sigue en `proposed`.
- El idioma del artefacto coincide con el pedido. Las columnas de `STATUS.md` siguen `N`, `archivo`, `estado`, `sustituye`, `notas`.
- Cada campo que la plantilla exige está lleno. No queda un hueco (`#…`, `<task>`, `TBD`, lorem ipsum). Un campo que la referencia manda dejar en blanco hasta que llegue el dato está en blanco a propósito, y el estado es el que nombra la referencia.
- No se añadió nada que este skill prohíbe. La referencia nombra qué se queda fuera.
- La respuesta nombra la carpeta, los archivos, el `N` y el estado. Un blanco dejado a propósito nombra el command que lo llena.
