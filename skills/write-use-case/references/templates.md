<p align="right">Language:&emsp;<img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-on.svg" align="middle" style="vertical-align:middle"> <a href="templates.es.md" style="vertical-align:middle"><img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-off.svg" align="middle" style="vertical-align:middle"></a></p>

[🏠 Project Manager](../../../README.md) / [Write the use case](../SKILL.md)

# Use case templates

Source: Alistair Cockburn, *Writing Effective Use Cases*. A project adapts one of the two forms. It does not invent a third kind of use case.

This file chooses the template. It is not a use case.

## Shipped

| Id | Manual | Use when |
| --- | --- | --- |
| `casual` | [casual.md](casual.md) | The five fields are enough. This is the default. |
| `fully-dressed` | [fully-dressed.md](fully-dressed.md) | Scope, level, stakeholders, the trigger, and the guarantees have to be written. |

## Which file is read

The output folder is `adrenaline/project-manager/`, or the path `outputDirs["plugin-project-manager"]` in `.cursor/adrenaline.json` when that path is relative, has no `..`, and is not absolute. If `adrenaline/project-manager/` does not exist yet and `project-manager/` at the project root already has this plugin's `ORIGIN.json` or `STATUS.md`, use that folder.

1. The person names an id. Look for `<output>/templates/use-case/<id>.md`. If that file exists, it is the template. Read it. Do not also apply a shipped template on top of it.
2. If that file does not exist, and the id is `casual` or `fully-dressed`, read that shipped manual.
3. If the id is neither a project file nor a shipped id, write no use case. Name the shipped ids and every `<output>/templates/use-case/*.md` that was found. Say which command will write the case once they name one.
4. If they name no template, use `casual`. Record it under Assumed: template `casual`, because none was selected. Name `fully-dressed` and any project template that was found. Change it by naming the id in `/pm-use-case`. Regenerate the case with `/pm-use-case`.

A project template wins over the shipped id with the same name.

## A template the project owns

The person creates it in the project. It is not an `<NNN>` file and it has no row in `STATUS.md`.

Path: `<output>/templates/use-case/<id>.md`. `<id>` is English, lowercase, with hyphens. It is not `casual` or `fully-dressed`: those names stay the shipped ones. To change a shipped form, use another id and set `based_on`.

```markdown
---
id: acme-checkout
piece: use-case
based_on: casual
---

## Actor
required
Who starts it, and the goal as a short active verb phrase.

## Extra
optional
A heading this project adds. Once it is listed, a delivery fills it or leaves the gap this heading states.
```

`based_on` is `casual` or `fully-dressed`. The writing rules of that manual still apply. A project template cannot turn them off.

- A `required` heading of the base stays, with that base's meaning. The project file may rename the visible heading. The meaning stays.
- An `optional` heading of the base may be dropped.
- A new heading is allowed. It becomes required for every case that names this id.
- The heading text may be in the language the project writes. The artifact still follows the language of the request: translate the headings, keep the id.
- Instructions under a heading are for the writer. They are not copied into the use case.

When the person asks to create or change a project template, write only that file. Create the output folder if it is missing, and write `ORIGIN.json` beside `STATUS.md` if either is missing. Do not write a use case in that turn unless they also asked for one.

## Done

This file is not a situation. The delivery is the use case. Evaluate `## Done` in the manual this file selects. The template recorded on the case is the one selected here.
