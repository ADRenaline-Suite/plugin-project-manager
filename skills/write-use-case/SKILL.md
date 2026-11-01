---
name: write-use-case
description: Writes one use case from a Cockburn template, casual or fully dressed, or from a template the project added. Use it when someone asks for a use case, a casual or fully dressed case, or a use-case template of their own.
---

<p align="right">Language:&emsp;<img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-on.svg" align="middle" style="vertical-align:middle"> <a href="SKILL.es.md" style="vertical-align:middle"><img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-off.svg" align="middle" style="vertical-align:middle"></a></p>

[🏠 Project Manager](../../README.md)

# Write the use case

One use case, in the template this turn selects. The story is numbered steps. Another business way is an extension, not an "if" in the main path.

Source: Alistair Cockburn, *Writing Effective Use Cases*.

## Before writing

1. Read [templates](references/templates.md) and only the manual it selects: [casual](references/casual.md) or [fully-dressed](references/fully-dressed.md). A project file replaces that manual when the person names its id.
2. A request that names no template uses `casual`.
3. A request to create or change a project template writes only `<output>/templates/use-case/<id>.md`, as [templates](references/templates.md) says. It does not write a use case in that turn unless they also asked for one.
4. Do not draw the use-case diagram. Ask `plugin-uml-diagrams` when actors and boundaries have to be seen. Do not write the test scenario. Ask `plugin-qa-engineer` for a system failure. Do not discover the opportunity. Cite `plugin-product` when an accepted outcome exists.

## Delivery

The file is `<NNN>-use-case-<topic>.md` in `adrenaline/project-manager/`, or in `outputDirs["plugin-project-manager"]` when that path is valid. `<NNN>` is the next free number in that folder. The artifact follows the language of the request. Template headings are translated. The template id stays in English and is recorded in `notas`. `STATUS.md` columns stay `N`, `archivo`, `estado`, `sustituye`, `notas`. `ORIGIN.json` sits beside it, with `suite` `ADRenaline-Suite`, `plugin` `plugin-project-manager`, `repository` `https://github.com/ADRenaline-Suite/plugin-project-manager`, and `convention` `adr-001`. It has no row in `STATUS.md`. A numbered file about one named project goes in `<subject>/`. A numbered file about the whole product stays at the output root. `<NNN>` is the next free number in the whole output folder. The `archivo` cell is `<subject>/<file>` when there is a subject (`doc/arch/adr-008-asunto-subcarpeta.md`). A project template stays under `templates/` at the root.

## Example

The person says a buyer pays a confirmed order with a card, and can use a saved card instead. With no template named, the file is `casual`: the actor and the goal, the precondition they stated, the numbered main flow, the saved-card alternate tied to the step it leaves, and the postcondition. It does not describe the pay button and it does not write the declined-card test.

## Done

Before you close, evaluate this list and the `## Done` list in the reference for this situation. A command fixes the situation: use the reference that command names. Every item is true, or you fix the delivery in this turn. Do not leave a file that fails an item. Do not mark it `accepted` while an item fails. A template the reference names is applied and recorded under Assumed; the delivery uses the state that reference names. An unknown template id is not a failed list: follow the templates reference and write no use case.

- The situation of this turn is the only one written, unless the request asked for two. Each delivery has its own `<NNN>`. A project template is not an `<NNN>` file.
- Files are only in the output folder, named as Delivery says. `<NNN>` is not reused. `STATUS.md` matches the files and the state this situation allows. `ORIGIN.json` is in that folder, its four fields match this plugin, and it has no row in `STATUS.md`. A gap the reference leaves as `proposed` stays `proposed`.
- The artifact language matches the request. `STATUS.md` columns stay `N`, `archivo`, `estado`, `sustituye`, `notas`.
- Every field the template requires is filled. No placeholder remains (`#…`, `<task>`, `TBD`, lorem ipsum). A field the reference tells you to leave blank until data arrives is blank on purpose, and the state is the one the reference names.
- Nothing this skill forbids was added. The reference names what stays out.
- The reply names the folder, the files, the `N`, and the state. If a template was applied, the reply ends with the Assumed block, one line per template, naming the command that changes it and the command that regenerates this piece. A blank left on purpose names the command that fills it.
