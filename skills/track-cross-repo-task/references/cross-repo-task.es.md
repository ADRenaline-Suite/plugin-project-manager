<p align="right">Idioma:&emsp;<a href="cross-repo-task.md" style="vertical-align:middle"><img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-off.svg" align="middle" style="vertical-align:middle"></a> <img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-on.svg" align="middle" style="vertical-align:middle"></p>

[🏠 Project Manager](../../../README.es.md) / [Seguir la tarea entre repositorios](../SKILL.es.md)

# Tarea entre repositorios

Fuente: *PMBOK Guide*, 7.ª edición, la actividad como un trabajo con un resultado. El tracker que guarda el issue no es este archivo. El tipo de archivo es `cross-repo-task`.

## Qué fija

Un resultado comprobable, y qué repositorio hace qué parte.

## Cómo hacerlo

1. Una tarea, un resultado. El resultado es algo que una persona puede comprobar, no una lista de reuniones.
2. Nombra cada repositorio que nombró la persona, y el cambio que le toca. No añadas un repositorio que no nombró.
3. Una URL de issue o un id de work item se escribe en ese repositorio solo cuando la persona lo da. No abras el issue.
4. La tarea termina cuando el cambio de cada repositorio está hecho. Dilo como condición de cierre.
5. Un caso de uso que esta tarea lleva a cabo se cita por archivo cuando existe. No escribas el caso de uso aquí.

## Plantilla

Encabezados, en este orden. Tradúcelos. Conserva el id de tipo.

## Resultado

obligatorio. El único desenlace que cierra la tarea.

## Repositorios

obligatorio. Un bloque por repositorio: el nombre, el cambio que le toca y el enlace al issue cuando la persona lo dio.

## Cierra cuando

obligatorio. Todos esos cambios están hechos.

## Done

- Los tres encabezados están, en este orden, en el idioma del pedido.
- Hay un resultado. Cada repositorio lo nombró la persona. No se inventó un issue y no se abrió ninguno.
- El estado es `accepted` solo cuando el resultado y al menos un repositorio vinieron de la persona. Una lista de repositorios que falta es un hueco y el archivo queda `proposed`.
