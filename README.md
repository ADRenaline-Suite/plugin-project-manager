<p align="right">Language:&emsp;<img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-on.svg" align="middle" style="vertical-align:middle"> <a href="README.es.md" style="vertical-align:middle"><img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-off.svg" align="middle" style="vertical-align:middle"></a></p>

# Project Manager (`plugin-project-manager`)

Writes the use case, the task that crosses repositories, the progress report, the sprint plan, and the ordered backlog. It does not draw the use-case diagram, write the test, or discover the business outcome.

The instructions are in English. The file the plugin saves follows the language of the request. Files go in `adrenaline/project-manager/`.

## Use case

`/pm-use-case` writes one case. With no template named, it uses `casual`. Name `fully-dressed` when scope, level, stakeholders, the trigger, and the guarantees have to be written. A project file at `templates/use-case/<id>.md` is used when that id is named.

## /pm-use-case

Who starts it, and the path that meets the goal. The main flow is 3 to 9 numbered steps. Another business way sits beside that flow, not inside an "if". A system failure is named and asked of `plugin-qa-engineer`.

## Cross-repository task

`/pm-cross-repo-task` writes one result and the change that belongs to each repository the person names.

## /pm-cross-repo-task

One outcome that can be checked. Each repository has its change. An issue link is recorded only when the person gives it. The task does not open the issue.

## Progress report

`/pm-status` writes the status of this period. With no template named, it uses `status`. A project file at `templates/status-report/<id>.md` is used when that id is named.

## /pm-status

The period, whether the work is on track, what finished, what is still open, what is blocked, what is next, and the decision that is needed. A cost or a date is written only when the person gives it.

## Sprint

`/pm-sprint` writes why this period is valuable, which items are in it, and how they will be delivered.

## /pm-sprint

The sprint goal, the timebox, the selected items, and the delivery plan. It cites a product outcome when one is already accepted. It does not estimate the items.

## Backlog

`/pm-backlog` writes the delivery list in the order the person gave.

## /pm-backlog

Each item names a use case, a task, or stays one line until that file exists. A GitHub or Azure id is recorded only when the person gives it. The board stays in the tracker.

## A template in the project

The shipped templates are `casual`, `fully-dressed`, and `status`. A project adds its own file under `templates/` in the output folder. The id does not reuse those three names. `based_on` names the shipped form, and that form's writing rules still apply. The file is not a numbered delivery.

## Help

## /pm-help

The catalog of this plugin. It does not write a file.

## Who it is for

Someone who wants the use case, the task across repositories, the progress report, the sprint, or the backlog written down. The diagram stays with `plugin-uml-diagrams`. The test stays with `plugin-qa-engineer`. The opportunity stays with `plugin-product`. A tutorial or a how-to stays with `plugin-documentation`. This plugin does not copy their skills.

## What it includes

Portable, for any agent that follows [Agent Skills](https://agentskills.io/specification):

- `write-use-case` writes the case from a template.
- `track-cross-repo-task` writes the task.
- `report-progress` writes the report from a template.
- `plan-sprint` writes the sprint plan.
- `order-backlog` writes the ordered list.

Cursor and Claude Code: the commands above. In Cursor, `/pm-use-case`. In Claude Code, `/plugin-project-manager:pm-use-case`.

Cursor only: rules `output-folder` and `pm-boundary`. Claude Code does not load rules. The same restrictions are in the skills.

## Install

In Cursor, install the plugin from this repository in Customize.

In Claude Code:

```text
claude plugin marketplace add ADRenaline-Suite/plugin-project-manager
claude plugin install plugin-project-manager@plugin-project-manager
```

To try a local copy, start Claude Code with `claude --plugin-dir <path to this repository>`.
