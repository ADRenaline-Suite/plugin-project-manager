---
name: order-backlog
description: Writes the ordered delivery list, each item tied to a use case, a task, or a tracker id the person gave. Use it when someone asks for the backlog or for the order of the work.
---

<p align="right">Idioma:&emsp;<a href="SKILL.md" style="vertical-align:middle"><img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-off.svg" align="middle" style="vertical-align:middle"></a> <img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-on.svg" align="middle" style="vertical-align:middle"></p>

[🏠 Project Manager](../../README.es.md)

# Ordenar el backlog

Una lista ordenada. El orden es el que dio la persona. El tracker conserva las tarjetas.

Fuente: Scrum Guide, 2020. El Product Backlog es la lista ordenada. El resultado de negocio se queda en `plugin-product`.

## Antes de escribir

1. Lee [backlog](references/backlog.es.md). Escribe solo esa situación.
2. No crees un issue, no muevas una columna y no sincronices un tablero. Cita `plugin-product` cuando se nombra un resultado accepted. No lo reescribas.

## Entrega

El archivo es `<NNN>-backlog-<tema>.md` en `adrenaline/project-manager/`, o en `outputDirs["plugin-project-manager"]` cuando esa ruta es válida. `<NNN>` es el siguiente número libre de esa carpeta. El artefacto sigue el idioma del pedido. El id de tipo se queda `backlog`. Las columnas de `STATUS.md` siguen `N`, `archivo`, `estado`, `sustituye`, `notas`. `ORIGIN.json` va a su lado, con `suite` `ADRenaline-Suite`, `plugin` `plugin-project-manager`, `repository` `https://github.com/ADRenaline-Suite/plugin-project-manager` y `convention` `adr-001`. No tiene fila en `STATUS.md`. Un archivo numerado de un proyecto nombrado va en `<asunto>/`. Un archivo numerado de todo el producto se queda en la raíz de la salida. `<NNN>` es el siguiente libre de toda la carpeta. La celda `archivo` es `<asunto>/<archivo>` cuando hay asunto (`doc/arch/adr-008-asunto-subcarpeta.md`).

## Ejemplo

La persona lista primero el pago con tarjeta y segundo el recibo, y da el issue de GitHub del primero. El archivo los numera en ese orden y registra esa URL. No abre el segundo issue y no decide que el recibo vale más.

## Done

Antes de cerrar, evalúa esta lista y la lista `## Done` de la referencia de esta situación. Un command fija la situación: usa la referencia que ese command nombra. Cada ítem es cierto, o corriges la entrega en este turno. No dejes un archivo que falle un ítem. No lo marques `accepted` mientras un ítem falle. Una plantilla que nombra la referencia se aplica y se registra bajo Assumed; la entrega usa el estado que nombra esa referencia. Una lista sin orden dado por la persona no es una lista fallida: la referencia deja el archivo `proposed` y nombra el hueco.

- La situación de este turno es la única que se escribe, salvo que el pedido haya pedido dos. Cada entrega tiene su `<NNN>`.
- Los archivos están solo en la carpeta de salida, con el nombre que dice Entrega. `<NNN>` no se reutiliza. `STATUS.md` coincide con los archivos y con el estado que esta situación permite. `ORIGIN.json` está en esa carpeta, sus cuatro campos coinciden con este plugin y no tiene fila en `STATUS.md`. Un hueco que la referencia deja en `proposed` sigue en `proposed`.
- El idioma del artefacto coincide con el pedido. Las columnas de `STATUS.md` siguen `N`, `archivo`, `estado`, `sustituye`, `notas`.
- Cada campo que la plantilla exige está lleno. No queda un hueco (`#…`, `<task>`, `TBD`, lorem ipsum). Un campo que la referencia manda dejar en blanco hasta que llegue el dato está en blanco a propósito, y el estado es el que nombra la referencia.
- No se añadió nada que este skill prohíbe. La referencia nombra qué se queda fuera.
- La respuesta nombra la carpeta, los archivos, el `N` y el estado. Un blanco dejado a propósito nombra el command que lo llena.
