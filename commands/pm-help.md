---
name: pm-help
description: "ADRenaline. Help: catalog of plugin-project-manager (skills, rules, commands)."
---

# Help — ADRenaline Project Manager

Print this catalog as the reply. Do not run any skill or command. Do not invent entries that are not listed. If a component was added to the plugin and is missing here, add one line from its frontmatter `description` and say the catalog was refreshed.

When this help command is the first command in the message, every command, skill, or rule named after it is the subject of the help. Do not run those names. Do not print the full catalog. For each name, in the order given, print its catalog line (the linked id and the sentence). When the README has a heading for that command, also print the paragraphs under that heading, up to the next heading. A skill name uses the skill's catalog line and the README group that names that skill, up to its first command heading. A name that is not in this catalog is one line: it is not in this plugin. Do not invent what it does, and do not write a file.

Write the sentences in the language of the request. Keep command names, file ids, and every URL unchanged. Every id is a markdown link to the GitHub URL on its line. Do not print a repository `name` as the visible label of a plugin.

Keep the section headings, in this order: Plugin, Commands, Skills, Rules, then Agents, Hooks, and MCP when the plugin has them, then Output, then Not in this plugin. The title and the Plugin line show `ADRenaline` plus the `displayName`, then one sentence on what the plugin does. Under Commands, group the lines by the skill named in the line. Each group opens with that skill name linked to its SKILL.md. One line per item: the linked id, then the sentence. Output links this plugin's GitHub repository under that same label. A plugin under Not in this plugin uses `ADRenaline` plus its short name, and links to `https://github.com/<owner>/<other-plugin>` only when that repository exists.

## Plugin

- [**ADRenaline Project Manager**](https://github.com/ADRenaline-Suite/plugin-project-manager/blob/main/README.md) — Writes the use case, the cross-repository task, the progress report, the sprint plan, and the ordered backlog.

## Commands

- [**/pm-help**](https://github.com/ADRenaline-Suite/plugin-project-manager/blob/main/README.md) — This help (one-line catalog of the plugin).
- [**write-use-case**](https://github.com/ADRenaline-Suite/plugin-project-manager/blob/main/skills/write-use-case/SKILL.md) — Writes one use case from a Cockburn template, or from a template the project added.
- [**/pm-use-case**](https://github.com/ADRenaline-Suite/plugin-project-manager/blob/main/skills/write-use-case/references/templates.md) — Use case: who starts it and the path that meets the goal, in the casual or fully dressed template.
- [**track-cross-repo-task**](https://github.com/ADRenaline-Suite/plugin-project-manager/blob/main/skills/track-cross-repo-task/SKILL.md) — Writes one task that crosses repositories, with one result and the change in each repository.
- [**/pm-cross-repo-task**](https://github.com/ADRenaline-Suite/plugin-project-manager/blob/main/skills/track-cross-repo-task/references/cross-repo-task.md) — Cross-repository task: one result, and the change that belongs to each repository.
- [**report-progress**](https://github.com/ADRenaline-Suite/plugin-project-manager/blob/main/skills/report-progress/SKILL.md) — Writes a progress report from the status template, or from a template the project added.
- [**/pm-status**](https://github.com/ADRenaline-Suite/plugin-project-manager/blob/main/skills/report-progress/references/status-report.md) — Progress report: what finished this period, what is blocked, and what is next.
- [**plan-sprint**](https://github.com/ADRenaline-Suite/plugin-project-manager/blob/main/skills/plan-sprint/SKILL.md) — Writes the sprint plan: the goal, the selected items, and how they will be delivered.
- [**/pm-sprint**](https://github.com/ADRenaline-Suite/plugin-project-manager/blob/main/skills/plan-sprint/references/sprint.md) — Sprint plan: why this period is valuable, which items are in it, and how they will be delivered.
- [**order-backlog**](https://github.com/ADRenaline-Suite/plugin-project-manager/blob/main/skills/order-backlog/SKILL.md) — Writes the ordered delivery list.
- [**/pm-backlog**](https://github.com/ADRenaline-Suite/plugin-project-manager/blob/main/skills/order-backlog/references/backlog.md) — Ordered backlog: the delivery list, each item linked to a use case, a task, or a tracker id the person gave.

## Skills

- [**write-use-case**](https://github.com/ADRenaline-Suite/plugin-project-manager/blob/main/skills/write-use-case/SKILL.md) — Writes one use case from a Cockburn template, casual or fully dressed, or from a template the project added.
- [**track-cross-repo-task**](https://github.com/ADRenaline-Suite/plugin-project-manager/blob/main/skills/track-cross-repo-task/SKILL.md) — Writes one task that crosses repositories, with one result and the issue that belongs to each repository.
- [**report-progress**](https://github.com/ADRenaline-Suite/plugin-project-manager/blob/main/skills/report-progress/SKILL.md) — Writes a progress report from the status template, or from a template the project added.
- [**plan-sprint**](https://github.com/ADRenaline-Suite/plugin-project-manager/blob/main/skills/plan-sprint/SKILL.md) — Writes the sprint plan, the goal, the selected items, and how they will be delivered.
- [**order-backlog**](https://github.com/ADRenaline-Suite/plugin-project-manager/blob/main/skills/order-backlog/SKILL.md) — Writes the ordered delivery list, each item tied to a use case, a task, or a tracker id the person gave.

## Rules

- [**output-folder**](https://github.com/ADRenaline-Suite/plugin-project-manager/blob/main/rules/output-folder.mdc) — Every file goes in `adrenaline/project-manager/` (or in `outputDirs["plugin-project-manager"]` of `.cursor/adrenaline.json`). The artifact follows the language of the request.
- [**pm-boundary**](https://github.com/ADRenaline-Suite/plugin-project-manager/blob/main/rules/pm-boundary.mdc) — The diagram, the test, the opportunity, and the reader document stay in their plugins. The tracker is not replaced.

## Output

- Repository: [**ADRenaline Project Manager**](https://github.com/ADRenaline-Suite/plugin-project-manager).
- Folder: `adrenaline/project-manager/` (override via `.cursor/adrenaline.json`). An existing `project-manager/` at the project root keeps receiving files.
- Name: `<NNN>-<type>-<topic>.md`, with monotonic `<NNN>`. The prose follows the language of the request. The type stays the English piece id. A project template is `templates/<piece>/<id>.md` and has no `<NNN>`.

| Format | Description |
| --- | --- |
| `.md` | A use case, a cross-repository task, a progress report, a sprint plan, or an ordered backlog. |
| `templates/<piece>/<id>.md` | A project template for a use case or a progress report. Not an `<NNN>` file. |
| `STATUS.md` | State of each numbered file. Columns stay `N`, `archivo`, `estado`, `sustituye`, `notas`. |
| `ORIGIN.json` | Folder marker: `suite`, `plugin`, `repository`, `convention` `adr-001`. Not an `<NNN>` file. |

## Not in this plugin

- Use-case diagram → [**ADRenaline UML Diagrams**](https://github.com/ADRenaline-Suite/plugin-uml-diagrams).
- Test scenario → ADRenaline QA.
- Opportunity and business outcome → ADRenaline Product.
- Tutorial, how-to, reference, or explanation for a reader → ADRenaline Documentation.
- Opening or moving an issue in GitHub or Azure Boards → the tracker. A later write to the remote host goes through ADRenaline Action Confirmation.

In Claude Code, commands use the prefix `/plugin-project-manager:` (example: `/plugin-project-manager:pm-help`).

## Done

- With no names after this command, the reply is this catalog. Every id is a markdown link to the GitHub URL listed here. Commands are grouped by skill.
- With names after this command, the reply is only the help for those names, in that order: the catalog line and, when the README has it, the paragraphs under that heading. The other names were not run.
- No skill ran. No command ran. No file was written.
- No entry was invented. If a component exists in the plugin and is missing here, one line was added from its `description` and the reply says the catalog was refreshed.
