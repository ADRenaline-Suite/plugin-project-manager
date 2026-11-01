<p align="right">Idioma:&emsp;<a href="fully-dressed.md" style="vertical-align:middle"><img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-off.svg" align="middle" style="vertical-align:middle"></a> <img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-on.svg" align="middle" style="vertical-align:middle"></p>

[🏠 Project Manager](../../../README.es.md) / [Escribir el caso de uso](../SKILL.es.md)

# Caso de uso fully dressed

Fuente: Alistair Cockburn, *Writing Effective Use Cases*. Fully dressed es la historia casual más los campos que pide un caso de más ceremonia. El tipo de archivo es `use-case`. El id de plantilla es `fully-dressed`.

## Qué fija

La misma meta que el caso casual, con el límite, el nivel, a quién más le importa, qué lo dispara y qué queda garantizado si funciona o si se detiene.

## Reglas de redacción

Valen las reglas casuales: de 3 a 9 pasos, el actor en cada paso, la intención y no la interfaz, sin «si» en el escenario principal, el dato por un apodo, caja negra, sin inventar el resultado de producto.

Además:

- El alcance nombra el sistema del que se habla. En un requisito de sistema, ese sistema es una caja negra: el caso diseña todo lo de dentro y nada de fuera. Un caso de negocio de caja blanca solo vale cuando la persona dice que el caso describe la organización, no un sistema por construir.
- El nivel es uno de `summary`, `user-goal` o `subfunction`. Los pasos quedan un nivel por debajo del caso. Un caso de meta de usuario no es el resumen de un negocio entero, ni un solo clic.
- Cada interesado se nombra con el interés que el sistema tiene que satisfacer. El actor primario es uno de ellos.
- Las precondiciones son obligatorias y ya ciertas. No se vuelven a comprobar en el escenario.
- La condición de éxito satisface los intereses. La protección si falla los protege cuando la meta no se cumple. Las dos hablan de los interesados, no de un stack trace.
- El disparador es el suceso que empieza el caso. No es el paso 1.
- El escenario principal de éxito va del disparador a la condición de éxito.
- Cada extensión nombra el paso del que sale (`4a`). Su trato vuelve al escenario principal, termina en otro éxito o falla bajo la protección si falla.
- Lista las condiciones de extensión antes de escribir sus pasos. Un fallo del sistema que el sistema tiene que detectar es una condición de extensión en una línea. Su trato se pide a `plugin-qa-engineer`. No escribas el escenario de prueba.
- Prioridad, frecuencia y canal son opcionales. Escríbelos solo cuando la persona los da.

## Plantilla

Encabezados, en este orden. Tradúcelos. Conserva el id de plantilla.

## Actor

obligatorio. Actor primario y la meta, como una frase corta con verbo de acción.

## Alcance

obligatorio. El sistema del que se habla. Di caja negra, salvo que la persona haya pedido un caso de negocio de caja blanca.

## Nivel

obligatorio. `summary`, `user-goal` o `subfunction`.

## Interesados

obligatorio. Cada nombre y el interés que hay que satisfacer. Si un interesado no fue nombrado, el hueco dice a quién falta. No inventes un regulador, un dueño ni una persona.

## Precondiciones

obligatorio. Ya ciertas. No se vuelven a comprobar en el escenario.

## Fin con éxito

obligatorio. Qué es cierto cuando se cumple cada interés que cubre este éxito.

## Fin si falla

obligatorio. Qué queda protegido cuando la meta no se cumple.

## Disparador

obligatorio. El suceso que empieza el caso.

## Escenario principal de éxito

obligatorio. Pasos numerados, de 3 a 9.

## Extensiones

obligatorio. Condición, el paso del que sale y el trato. Un fallo del sistema es una línea que pide `plugin-qa-engineer`. Si no hay extensión, escribe «Ninguna».

## Relacionado

opcional. Prioridad, frecuencia o canal, y solo los valores que dio la persona. Omite el encabezado cuando no dio ninguno.

## Done

- Los encabezados obligatorios están, en este orden, en el idioma del pedido. El id `fully-dressed` queda en `notas`. Relacionado aparece solo cuando la persona dio un valor.
- El nivel es uno de los tres nombres. El alcance dice si el sistema es una caja negra.
- El escenario principal tiene de 3 a 9 pasos, sin «si». Cada extensión nombra el paso del que sale y dónde termina.
- Un fallo del sistema pide `plugin-qa-engineer` y no contiene el escenario de prueba.
- No se inventó un interesado, una garantía, un disparador ni un valor relacionado. Un encabezado obligatorio sin hecho es un hueco y el archivo queda `proposed`.
