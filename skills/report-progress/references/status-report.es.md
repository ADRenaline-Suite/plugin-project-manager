<p align="right">Idioma:&emsp;<a href="status-report.md" style="vertical-align:middle"><img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-off.svg" align="middle" style="vertical-align:middle"></a> <img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-on.svg" align="middle" style="vertical-align:middle"></p>

[🏠 Project Manager](../../../README.es.md) / [Reportar el avance](../SKILL.es.md)

# Reporte de estado

Fuente: *PMBOK Guide*, 7.ª edición, apartado 4.6.7. El reporte dice el estado actual y el avance desde el reporte anterior. Las previsiones de costo y de calendario entran solo cuando la persona da las cifras. El tipo de archivo es `status-report`. El id de plantilla es `status`.

La forma sigue la práctica de una página: las mismas secciones en el mismo orden, resultados y no actividad, y el estado y la decisión antes del detalle. Las notas de PMI sobre un reporte que alguien va a usar: que sea corto, que se quede objetivo y que no esconda un bloqueo.

## Qué fija

Dónde está el trabajo en este periodo, qué terminó, qué está bloqueado, qué sigue y si hace falta una decisión.

## Reglas de redacción

Una plantilla del proyecto no quita estas reglas.

- Los mismos encabezados, en este orden, en cada reporte. Quien lee aprende dónde mirar.
- El periodo es explícito: inicio y fin, o el nombre de un sprint ya escrito. Un reporte sin periodo es un hueco.
- El estado general es uno de `on track`, `at risk` u `off track`. Si no es `on track`, el resumen dice por qué en su primera frase.
- Informa resultados que terminaron. Una reunión, un porcentaje sin resultado y «casi listo» no son Hecho en este periodo.
- Hecho en este periodo y En curso van aparte. Un ítem está en uno de los dos.
- Un bloqueo nombra qué está esperando. Añade quién puede desbloquearlo, y desde cuándo, solo cuando la persona lo dijo.
- Siguiente es lo que estará terminado antes del próximo reporte. Cuando existe un reporte anterior de este asunto, compara el Hecho de este periodo con el Siguiente de aquel. Un ítem que no se cumplió se nombra. No se deja caer.
- Una fecha que dijo un reporte anterior sigue visible. Este reporte puede añadir una previsión nueva al lado. No sustituye la fecha anterior.
- Decisiones pedidas es lo que se pide, a quién y para cuándo. Cuando no hay petición, escribe «Ninguna». No inventes una decisión.
- Un costo, un presupuesto, una previsión, una fecha de línea base o el nombre de una persona entra solo cuando la persona lo da. No calcules uno.
- Cita un caso de uso o una tarea por el archivo que escribió este plugin, o por el nombre que la persona dio en este turno. No añadas trabajo de la nada.
- Esto no es un reporte de pruebas, una métrica de producto ni un documento Diátaxis. No los escribas.

## Plantilla

Encabezados, en este orden. Tradúcelos al idioma del pedido. Conserva el id de plantilla.

## Encabezado

obligatorio. El asunto, el periodo y la fecha de este reporte. El autor solo cuando la persona lo nombra.

## Estado general

obligatorio. `on track`, `at risk` u `off track`, y una línea. La línea es el motivo cuando el estado no es `on track`.

## Resumen

obligatorio. Hasta tres frases: dónde está, qué cambió en este periodo, qué decisión hace falta. Si no hace falta ninguna, la tercera frase lo dice.

## Hecho en este periodo

obligatorio. Resultados terminados, cada uno con el archivo o el nombre que cita. «Ninguno» cuando no terminó nada.

## En curso

obligatorio. Trabajo empezado y no terminado. «Ninguno» cuando no hay nada en curso.

## Bloqueos

obligatorio. Qué está esperando. «Ninguno» cuando nada está bloqueado.

## Siguiente

obligatorio. Qué estará terminado antes del próximo reporte.

## Decisiones pedidas

obligatorio. Lo que se pide, a quién y para cuándo. «Ninguna» cuando no hay petición.

## Cifras

opcional. Solo números y fechas que dio la persona: costo, calendario, línea base junto a la previsión. Omite el encabezado cuando no dio ninguno. No escribas «estimado».

## Done

- Los encabezados obligatorios están, en este orden, en el idioma del pedido. El id `status` queda en `notas`. Cifras aparece solo cuando la persona dio un número o una fecha.
- El estado general es una de las tres palabras. Un estado que no es `on track` da el motivo en la primera frase del Resumen.
- Hecho en este periodo contiene resultados terminados, no actividad. No comparte un ítem con En curso.
- El Siguiente de un reporte anterior se compara, y una fecha anterior no se sustituye.
- No se inventó un costo, una previsión, un nombre, una decisión ni una tarea. «Ninguno» o «Ninguna» es una sección llena. Un encabezado obligatorio sin hecho y sin un «Ninguno» honesto es un hueco, y el archivo queda `proposed`.
