---
name: report-progress
description: Writes a progress report from the status template, or from a template the project added. Use it when someone asks for a status report, a progress update, or a report template of their own.
---

<p align="right">Idioma:&emsp;<a href="SKILL.md" style="vertical-align:middle"><img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-off.svg" align="middle" style="vertical-align:middle"></a> <img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-on.svg" align="middle" style="vertical-align:middle"></p>

[🏠 Project Manager](../../README.es.md)

# Reportar el avance

Un reporte de avance, en la plantilla que elige este turno. Las secciones quedan en el mismo orden cada vez. Se informan resultados. Un costo o una fecha se escribe solo cuando la persona lo da.

Fuente: *PMBOK Guide*, 7.ª edición, apartado 4.6.7.

## Antes de escribir

1. Lee [plantillas](references/templates.es.md) y solo el manual que elija. El manual de serie es [reporte de estado](references/status-report.es.md). Un archivo del proyecto lo sustituye cuando la persona nombra su id.
2. Un pedido que no nombra plantilla usa `status`.
3. Un pedido de crear o cambiar una plantilla del proyecto escribe solo `<salida>/templates/status-report/<id>.md`, como dice [plantillas](references/templates.es.md). No escribe un reporte en ese turno, salvo que también lo hayan pedido.
4. Cita casos de uso y tareas que este plugin ya escribió, o nombres que la persona dio en este turno. No escribas un reporte de pruebas, una métrica de producto ni un documento Diátaxis.

## Entrega

El archivo es `<NNN>-status-report-<tema>.md` en `adrenaline/project-manager/`, o en `outputDirs["plugin-project-manager"]` cuando esa ruta es válida. `<NNN>` es el siguiente número libre de esa carpeta. El artefacto sigue el idioma del pedido. Los encabezados de la plantilla se traducen. El id de plantilla se queda en inglés y se anota en `notas`. Las columnas de `STATUS.md` siguen `N`, `archivo`, `estado`, `sustituye`, `notas`. `ORIGIN.json` va a su lado, con `suite` `ADRenaline-Suite`, `plugin` `plugin-project-manager`, `repository` `https://github.com/ADRenaline-Suite/plugin-project-manager` y `convention` `adr-001`. No tiene fila en `STATUS.md`. Un archivo numerado de un proyecto nombrado va en `<asunto>/`. Un archivo numerado de todo el producto se queda en la raíz de la salida. `<NNN>` es el siguiente libre de toda la carpeta. La celda `archivo` es `<asunto>/<archivo>` cuando hay asunto (`doc/arch/adr-008-asunto-subcarpeta.md`). Una plantilla del proyecto sigue bajo `templates/` en la raíz.

## Ejemplo

La persona dice que esta semana el caso de pago con tarjeta quedó accepted, que el recibo sigue abierto y que necesita una decisión sobre la línea de impuesto para el viernes. El reporte dice `on track` solo si dijo que el trabajo va en plazo. Hecho en este periodo cita el archivo del caso de uso. El recibo se queda en En curso. Decisiones pedidas nombra esa petición. No se añade un costo.

## Done

Antes de cerrar, evalúa esta lista y la lista `## Done` de la referencia de esta situación. Un command fija la situación: usa la referencia que ese command nombra. Cada ítem es cierto, o corriges la entrega en este turno. No dejes un archivo que falle un ítem. No lo marques `accepted` mientras un ítem falle. Una plantilla que nombra la referencia se aplica y se registra bajo Assumed; la entrega usa el estado que nombra esa referencia. Un id de plantilla desconocido no es una lista fallida: sigue la referencia de plantillas y no escribas el reporte.

- La situación de este turno es la única que se escribe, salvo que el pedido haya pedido dos. Cada entrega tiene su `<NNN>`. Una plantilla del proyecto no es un archivo `<NNN>`.
- Los archivos están solo en la carpeta de salida, con el nombre que dice Entrega. `<NNN>` no se reutiliza. `STATUS.md` coincide con los archivos y con el estado que esta situación permite. `ORIGIN.json` está en esa carpeta, sus cuatro campos coinciden con este plugin y no tiene fila en `STATUS.md`. Un hueco que la referencia deja en `proposed` sigue en `proposed`.
- El idioma del artefacto coincide con el pedido. Las columnas de `STATUS.md` siguen `N`, `archivo`, `estado`, `sustituye`, `notas`.
- Cada campo que la plantilla exige está lleno. No queda un hueco (`#…`, `<task>`, `TBD`, lorem ipsum). Un campo que la referencia manda dejar en blanco hasta que llegue el dato está en blanco a propósito, y el estado es el que nombra la referencia.
- No se añadió nada que este skill prohíbe. La referencia nombra qué se queda fuera.
- La respuesta nombra la carpeta, los archivos, el `N` y el estado. Si se aplicó una plantilla, la respuesta cierra con el bloque Assumed, una línea por plantilla, con el command que la cambia y el command que regenera esta pieza. Un blanco dejado a propósito nombra el command que lo llena.
