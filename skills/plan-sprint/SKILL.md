---
name: plan-sprint
description: Writes the sprint plan, the goal, the selected items, and how they will be delivered. Use it when someone asks what this period will finish.
---

<p align="right">Language:&emsp;<img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-on.svg" align="middle" style="vertical-align:middle"> <a href="SKILL.es.md" style="vertical-align:middle"><img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-off.svg" align="middle" style="vertical-align:middle"></a></p>

[🏠 Project Manager](../../README.md)

# Plan the sprint

One sprint. The goal says why the period is valuable. The items are the ones the person selected. The plan points at the work, and it does not estimate it.

Source: Scrum Guide, 2020. Sprint Planning.

## Before writing

1. Read [sprint](references/sprint.md). Write that situation only.
2. Cite an accepted outcome from `plugin-product` when the person ties the goal to it. Do not write the outcome. Do not size the items.

## Delivery

The file is `<NNN>-sprint-<topic>.md` in `adrenaline/project-manager/`, or in `outputDirs["plugin-project-manager"]` when that path is valid. `<NNN>` is the next free number in that folder. The artifact follows the language of the request. The type id stays `sprint`. `STATUS.md` columns stay `N`, `archivo`, `estado`, `sustituye`, `notas`. `ORIGIN.json` sits beside it, with `suite` `ADRenaline-Suite`, `plugin` `plugin-project-manager`, `repository` `https://github.com/ADRenaline-Suite/plugin-project-manager`, and `convention` `adr-001`. It has no row in `STATUS.md`. A numbered file about one named project goes in `<subject>/`. A numbered file about the whole product stays at the output root. `<NNN>` is the next free number in the whole output folder. The `archivo` cell is `<subject>/<file>` when there is a subject (`doc/arch/adr-008-asunto-subcarpeta.md`).

## Example

The person says the next two weeks finish card payment, and names the use case they already have. The file records that goal, those dates, that file, and the cross-repository task if one exists. It does not add a second item and it does not write a story point.

## Done

Before you close, evaluate this list and the `## Done` list in the reference for this situation. A command fixes the situation: use the reference that command names. Every item is true, or you fix the delivery in this turn. Do not leave a file that fails an item. Do not mark it `accepted` while an item fails. A template the reference names is applied and recorded under Assumed; the delivery uses the state that reference names. A sprint with no timebox from the person is not a failed list: the reference leaves the file `proposed` and names the gap.

- The situation of this turn is the only one written, unless the request asked for two. Each delivery has its own `<NNN>`.
- Files are only in the output folder, named as Delivery says. `<NNN>` is not reused. `STATUS.md` matches the files and the state this situation allows. `ORIGIN.json` is in that folder, its four fields match this plugin, and it has no row in `STATUS.md`. A gap the reference leaves as `proposed` stays `proposed`.
- The artifact language matches the request. `STATUS.md` columns stay `N`, `archivo`, `estado`, `sustituye`, `notas`.
- Every field the template requires is filled. No placeholder remains (`#…`, `<task>`, `TBD`, lorem ipsum). A field the reference tells you to leave blank until data arrives is blank on purpose, and the state is the one the reference names.
- Nothing this skill forbids was added. The reference names what stays out.
- The reply names the folder, the files, the `N`, and the state. A blank left on purpose names the command that fills it.
