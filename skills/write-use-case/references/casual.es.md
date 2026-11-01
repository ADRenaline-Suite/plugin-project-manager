<p align="right">Idioma:&emsp;<a href="casual.md" style="vertical-align:middle"><img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-off.svg" align="middle" style="vertical-align:middle"></a> <img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-on.svg" align="middle" style="vertical-align:middle"></p>

[🏠 Project Manager](../../../README.es.md) / [Escribir el caso de uso](../SKILL.es.md)

# Caso de uso casual

Fuente: Alistair Cockburn, *Writing Effective Use Cases*. La forma casual conserva una historia legible y deja fuera los campos de ceremonia. El tipo de archivo es `use-case`. El id de plantilla es `casual`.

## Qué fija

Quién quiere qué, qué ya es cierto, el camino en el que lo consigue, otra vía de negocio, y qué es cierto cuando funciona.

## Reglas de redacción

Estas reglas son la práctica. Una plantilla del proyecto no las quita.

- El título es la meta: una frase corta con verbo de acción, con el actor.
- El flujo principal tiene de 3 a 9 pasos numerados. Cada paso nombra quién actúa y una meta que se cumple. Escribe la intención, no la pantalla, el clic ni el control.
- Un paso hace avanzar la historia. Un actor pasa información, comprueba una condición o cambia un estado.
- No hay un «si» dentro del flujo principal. Otra vía de negocio es una alternativa, atada al paso del que sale (`2a`), escrita después del flujo principal.
- Una alternativa vuelve a un paso principal, termina con éxito o se detiene. Di cuál.
- Un fallo del sistema, una excepción o un dato de prueba se nombra en una línea y se pide a `plugin-qa-engineer`. No escribas el escenario de prueba.
- Una precondición ya es cierta antes del paso 1. No la repitas como paso.
- Nombra el dato por un apodo. Las longitudes, los tipos y la validación se quedan fuera del caso.
- El sistema es una caja negra. No describas sus internos, sus módulos ni sus tablas.
- No descubras el resultado de negocio. Cita un archivo accepted de `plugin-product` cuando exista.

## Plantilla

Encabezados, en este orden. Tradúcelos al idioma del pedido. Conserva el id de plantilla.

## Actor

obligatorio. Quién lo empieza, y la meta.

## Precondiciones

obligatorio. Qué ya es cierto. Si no se sabe nada, el hueco lo dice. No inventes un login, un rol ni un estado.

## Flujo principal

obligatorio. Pasos numerados, de 3 a 9, cada uno con el actor y una meta que se cumple.

## Alternativas de negocio

obligatorio. Un bloque por alternativa: el paso del que sale, la condición de negocio, los pasos y dónde termina. Si no hay alternativa, escribe «Ninguna». Una alternativa que es un fallo del sistema es una línea que pide `plugin-qa-engineer`.

## Postcondiciones

obligatorio. Qué es cierto cuando la meta se cumple. Una alternativa que se detiene dice qué es cierto en su lugar.

## Done

- Los cinco encabezados están, en este orden, en el idioma del pedido. El id `casual` queda en `notas`.
- El flujo principal tiene de 3 a 9 pasos. Cada paso nombra quién actúa. No hay un «si» en el flujo principal. Una alternativa de negocio está bajo Alternativas de negocio y dice dónde termina.
- Un fallo del sistema es una línea que pide `plugin-qa-engineer`. El escenario de prueba no está en este archivo.
- No se añadió una pantalla, un clic, un módulo, una tabla ni una longitud de campo. No se inventó un resultado de `plugin-product`.
- El estado es `accepted` solo cuando cada encabezado obligatorio se llenó con algo que dijo la persona o con un archivo accepted. Un encabezado que hubo que adivinar sigue siendo un hueco y el archivo queda `proposed`.
