<p align="right">Idioma:&emsp;<a href="README.md" style="vertical-align:middle"><img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-off.svg" align="middle" style="vertical-align:middle"></a> <img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-on.svg" align="middle" style="vertical-align:middle"></p>

# Project Manager (`plugin-project-manager`)

Escribe el caso de uso, la tarea que cruza repositorios, el reporte de avance, el plan del sprint y el backlog ordenado. No dibuja el diagrama de casos de uso, no escribe la prueba y no descubre el resultado de negocio.

Las instrucciones están en inglés. El archivo que guarda el plugin sigue el idioma del pedido. Los archivos van en `adrenaline/project-manager/`.

## Caso de uso

`/pm-use-case` escribe un caso. Si no se nombra plantilla, usa `casual`. Nombra `fully-dressed` cuando hay que escribir el alcance, el nivel, los interesados, el disparador y las garantías. Un archivo del proyecto en `templates/use-case/<id>.md` se usa cuando se nombra ese id.

## /pm-use-case

Quién lo empieza, y el camino que cumple la meta. El flujo principal tiene de 3 a 9 pasos numerados. Otra vía de negocio queda al lado de ese flujo, no dentro de un «si». Un fallo del sistema se nombra y se pide a `plugin-qa-engineer`.

## Tarea entre repositorios

`/pm-cross-repo-task` escribe un resultado y el cambio que le toca a cada repositorio que nombra la persona.

## /pm-cross-repo-task

Un desenlace que se puede comprobar. Cada repositorio tiene su cambio. Un enlace a un issue se anota solo cuando la persona lo da. La tarea no abre el issue.

## Reporte de avance

`/pm-status` escribe el estado de este periodo. Si no se nombra plantilla, usa `status`. Un archivo del proyecto en `templates/status-report/<id>.md` se usa cuando se nombra ese id.

## /pm-status

El periodo, si el trabajo va en plazo, qué terminó, qué sigue abierto, qué está bloqueado, qué sigue y la decisión que hace falta. Un costo o una fecha se escribe solo cuando la persona lo da.

## Sprint

`/pm-sprint` escribe para qué vale este periodo, qué ítems entran y cómo se van a entregar.

## /pm-sprint

La meta del sprint, el periodo, los ítems elegidos y el plan de entrega. Cita un resultado de producto cuando ya hay uno accepted. No estima los ítems.

## Backlog

`/pm-backlog` escribe la lista de entrega en el orden que dio la persona.

## /pm-backlog

Cada ítem nombra un caso de uso, una tarea, o se queda en una línea hasta que ese archivo exista. Un id de GitHub o de Azure se anota solo cuando la persona lo da. El tablero se queda en el tracker.

## Una plantilla en el proyecto

Las plantillas de serie son `casual`, `fully-dressed` y `status`. El proyecto añade su archivo bajo `templates/` en la carpeta de salida. El id no reutiliza esos tres nombres. `based_on` nombra la forma de serie, y las reglas de redacción de esa forma siguen vigentes. El archivo no es una entrega numerada.

## Ayuda

## /pm-help

El catálogo de este plugin. No escribe un archivo.

## Para quién es

Quien quiere por escrito el caso de uso, la tarea entre repositorios, el reporte de avance, el sprint o el backlog. El diagrama se queda en `plugin-uml-diagrams`. La prueba se queda en `plugin-qa-engineer`. La oportunidad se queda en `plugin-product`. Un tutorial o un how-to se queda en `plugin-documentation`. Este plugin no copia sus skills.

## Qué incluye

Portable, para cualquier agente que siga [Agent Skills](https://agentskills.io/specification):

- `write-use-case` escribe el caso a partir de una plantilla.
- `track-cross-repo-task` escribe la tarea.
- `report-progress` escribe el reporte a partir de una plantilla.
- `plan-sprint` escribe el plan del sprint.
- `order-backlog` escribe la lista ordenada.

Cursor y Claude Code: los commands de arriba. En Cursor, `/pm-use-case`. En Claude Code, `/plugin-project-manager:pm-use-case`.

Solo Cursor: las rules `output-folder` y `pm-boundary`. Claude Code no carga rules. Las mismas restricciones están en los skills.

## Instalar

En Cursor, instala el plugin desde este repositorio en Customize.

En Claude Code:

```text
claude plugin marketplace add ADRenaline-Suite/plugin-project-manager
claude plugin install plugin-project-manager@plugin-project-manager
```

Para probar una copia local, arranca Claude Code con `claude --plugin-dir <ruta de este repositorio>`.
