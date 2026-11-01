---
name: report-progress
description: Writes a progress report from the status template, or from a template the project added. Use it when someone asks for a status report, a progress update, or a report template of their own.
---

<p align="right">Language:&emsp;<img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-on.svg" align="middle" style="vertical-align:middle"> <a href="SKILL.es.md" style="vertical-align:middle"><img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-off.svg" align="middle" style="vertical-align:middle"></a></p>

[🏠 Project Manager](../../README.md)

# Report progress

One progress report, in the template this turn selects. The sections stay in the same order every time. Outcomes are reported. A cost or a date is written only when the person gives it.

Source: *PMBOK Guide*, 7th edition, section 4.6.7.

## Before writing

1. Read [templates](references/templates.md) and only the manual it selects. The shipped manual is [status-report](references/status-report.md). A project file replaces it when the person names its id.
2. A request that names no template uses `status`.
3. A request to create or change a project template writes only `<output>/templates/status-report/<id>.md`, as [templates](references/templates.md) says. It does not write a report in that turn unless they also asked for one.
4. Cite use cases and tasks this plugin already wrote, or names the person gave this turn. Do not write a test report, a product metric, or a Diátaxis document.

## Delivery

The file is `<NNN>-status-report-<topic>.md` in `adrenaline/project-manager/`, or in `outputDirs["plugin-project-manager"]` when that path is valid. `<NNN>` is the next free number in that folder. The artifact follows the language of the request. Template headings are translated. The template id stays in English and is recorded in `notas`. `STATUS.md` columns stay `N`, `archivo`, `estado`, `sustituye`, `notas`. `ORIGIN.json` sits beside it, with `suite` `ADRenaline-Suite`, `plugin` `plugin-project-manager`, `repository` `https://github.com/ADRenaline-Suite/plugin-project-manager`, and `convention` `adr-001`. It has no row in `STATUS.md`. A numbered file about one named project goes in `<subject>/`. A numbered file about the whole product stays at the output root. `<NNN>` is the next free number in the whole output folder. The `archivo` cell is `<subject>/<file>` when there is a subject (`doc/arch/adr-008-asunto-subcarpeta.md`). A project template stays under `templates/` at the root.

## Example

The person says this week the card payment case was accepted, the receipt is still open, and they need a decision on the tax line by Friday. The report says `on track` only if they said the work is on track. Done this period cites the use-case file. The receipt stays under In progress. Decisions needed names that ask. No cost is added.

## Done

Before you close, evaluate this list and the `## Done` list in the reference for this situation. A command fixes the situation: use the reference that command names. Every item is true, or you fix the delivery in this turn. Do not leave a file that fails an item. Do not mark it `accepted` while an item fails. A template the reference names is applied and recorded under Assumed; the delivery uses the state that reference names. An unknown template id is not a failed list: follow the templates reference and write no report.

- The situation of this turn is the only one written, unless the request asked for two. Each delivery has its own `<NNN>`. A project template is not an `<NNN>` file.
- Files are only in the output folder, named as Delivery says. `<NNN>` is not reused. `STATUS.md` matches the files and the state this situation allows. `ORIGIN.json` is in that folder, its four fields match this plugin, and it has no row in `STATUS.md`. A gap the reference leaves as `proposed` stays `proposed`.
- The artifact language matches the request. `STATUS.md` columns stay `N`, `archivo`, `estado`, `sustituye`, `notas`.
- Every field the template requires is filled. No placeholder remains (`#…`, `<task>`, `TBD`, lorem ipsum). A field the reference tells you to leave blank until data arrives is blank on purpose, and the state is the one the reference names.
- Nothing this skill forbids was added. The reference names what stays out.
- The reply names the folder, the files, the `N`, and the state. If a template was applied, the reply ends with the Assumed block, one line per template, naming the command that changes it and the command that regenerates this piece. A blank left on purpose names the command that fills it.
