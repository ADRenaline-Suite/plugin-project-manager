<p align="right">Idioma:&emsp;<a href="templates.md" style="vertical-align:middle"><img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-off.svg" align="middle" style="vertical-align:middle"></a> <img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-on.svg" align="middle" style="vertical-align:middle"></p>

[🏠 Project Manager](../../../README.es.md) / [Escribir el caso de uso](../SKILL.es.md)

# Plantillas del caso de uso

Fuente: Alistair Cockburn, *Writing Effective Use Cases*. Un proyecto adapta una de las dos formas. No inventa un tercer tipo de caso de uso.

Este archivo elige la plantilla. No es un caso de uso.

## De serie

| Id | Manual | Cuándo |
| --- | --- | --- |
| `casual` | [casual.es.md](casual.es.md) | Bastan los cinco campos. Es la de partida. |
| `fully-dressed` | [fully-dressed.es.md](fully-dressed.es.md) | Hay que escribir el alcance, el nivel, los interesados, el disparador y las garantías. |

## Qué archivo se lee

La carpeta de salida es `adrenaline/project-manager/`, o la ruta `outputDirs["plugin-project-manager"]` de `.cursor/adrenaline.json` cuando es relativa, no tiene `..` y no es absoluta. Si `adrenaline/project-manager/` aún no existe y `project-manager/` en la raíz ya tiene el `ORIGIN.json` o el `STATUS.md` de este plugin, se usa esa carpeta.

1. La persona nombra un id. Busca `<salida>/templates/use-case/<id>.md`. Si existe, es la plantilla. Léela. No apliques además una plantilla de serie.
2. Si no existe, y el id es `casual` o `fully-dressed`, lee ese manual de serie.
3. Si el id no es un archivo del proyecto ni un id de serie, no escribas el caso. Nombra los id de serie y cada `<salida>/templates/use-case/*.md` que haya. Di que `/pm-use-case` escribe el caso cuando nombren uno.
4. Si no nombran plantilla, usa `casual`. Regístralo bajo Assumed: plantilla `casual`, porque no se eligió ninguna. Nombra `fully-dressed` y cualquier plantilla del proyecto que se haya encontrado. Se cambia nombrando el id en `/pm-use-case`. Se regenera el caso con `/pm-use-case`.

Una plantilla del proyecto gana al id de serie que lleve el mismo nombre.

## Una plantilla del proyecto

La crea la persona en su proyecto. No es un archivo `<NNN>` y no tiene fila en `STATUS.md`.

Ruta: `<salida>/templates/use-case/<id>.md`. `<id>` va en inglés, en minúsculas y con guiones. No es `casual` ni `fully-dressed`: esos nombres siguen siendo los de serie. Para cambiar una forma de serie, usa otro id y pon `based_on`.

```markdown
---
id: acme-checkout
piece: use-case
based_on: casual
---

## Actor
required
Quién lo empieza, y la meta como una frase corta con verbo de acción.

## Extra
optional
Un encabezado que este proyecto añade. Si está en la lista, la entrega lo llena o deja el hueco que ese encabezado dice.
```

`based_on` es `casual` o `fully-dressed`. Las reglas de redacción de ese manual siguen vigentes. Una plantilla del proyecto no las apaga.

- Un encabezado `required` de la base se queda, con el significado de esa base. El archivo del proyecto puede cambiar el encabezado visible. El significado se queda.
- Un encabezado `optional` de la base se puede quitar.
- Un encabezado nuevo está permitido. Pasa a ser obligatorio en cada caso que nombre este id.
- El texto del encabezado puede ir en el idioma en que escribe el proyecto. El artefacto sigue el idioma del pedido: se traducen los encabezados y se conserva el id.
- Las instrucciones bajo un encabezado son para quien escribe. No se copian al caso de uso.

Cuando la persona pide crear o cambiar una plantilla del proyecto, escribe solo ese archivo. Crea la carpeta de salida si falta, y escribe `ORIGIN.json` junto a `STATUS.md` si falta alguno. No escribas un caso de uso en ese turno, salvo que también lo hayan pedido.

## Done

Este archivo no es una situación. La entrega es el caso de uso. Evalúa `## Done` en el manual que este archivo elige. La plantilla que queda anotada en el caso es la que se eligió aquí.
