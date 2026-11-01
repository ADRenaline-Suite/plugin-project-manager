<p align="right">Idioma:&emsp;<a href="backlog.md" style="vertical-align:middle"><img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-off.svg" align="middle" style="vertical-align:middle"></a> <img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-on.svg" align="middle" style="vertical-align:middle"></p>

[🏠 Project Manager](../../../README.es.md) / [Ordenar el backlog](../SKILL.es.md)

# Backlog ordenado

Fuente: Scrum Guide, 2020. El Product Backlog es una lista ordenada de lo que hace falta. El Product Owner responde por ese orden. En esta suite el resultado de negocio se queda en `plugin-product`. Este archivo es la lista de entrega. GitHub Issues, GitHub Projects y Azure Boards siguen siendo el tracker. El tipo de archivo es `backlog`.

## Qué fija

El orden del trabajo, y el enlace de cada ítem a un caso de uso, una tarea o un id de tracker que la persona ya tiene.

## Cómo hacerlo

1. El orden es el que dio la persona. No ordenes por un valor que inferiste. Si no dio orden, la lista es un hueco y el archivo queda `proposed`.
2. Cada ítem tiene un nombre. Cuando existe un archivo de caso de uso o de tarea, cítalo. Cuando no existe, el ítem se queda en una línea y dice que el archivo falta.
3. Una URL de issue de GitHub o un id de work item de Azure se escribe solo cuando la persona lo da. No crees el issue y no muevas una columna.
4. Cuando existe un resultado accepted de `plugin-product`, cítalo una vez, encima de la lista. No reescribas el resultado y no reordenes la lista para encajar con él, salvo que la persona lo pida.
5. Un archivo de backlog es una lista. Un orden posterior es el siguiente `<NNN>`, y la fila anterior pasa a `superseded`, salvo que la persona pida enmendar el mismo archivo.

## Plantilla

Encabezados, en este orden. Tradúcelos.

## Resultado

opcional. El archivo accepted de `plugin-product`, cuando se cita. Omite el encabezado cuando no se cita ninguno.

## Ítems

obligatorio. Una lista numerada. Cada ítem: el orden, el nombre, el archivo de caso de uso o de tarea cuando existe, y el enlace al tracker cuando la persona lo dio.

## Done

- Los ítems están numerados en el orden que dio la persona, en el idioma del pedido.
- No se inventó un ítem, un enlace al tracker ni un resultado. Un archivo que falta se nombra como faltante. No se abrió un issue.
- El estado es `accepted` solo cuando el orden y al menos un ítem vinieron de la persona. Sin orden hay un hueco y el archivo queda `proposed`.
