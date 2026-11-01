<p align="right">Language:&emsp;<img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-on.svg" align="middle" style="vertical-align:middle"> <a href="templates.es.md" style="vertical-align:middle"><img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-off.svg" align="middle" style="vertical-align:middle"></a></p>

[🏠 Project Manager](../../../README.md) / [Report progress](../SKILL.md)

# Progress report templates

Source: *PMBOK Guide*, 7th edition, section 4.6.7. A status report is the same sections, in the same order, every time. PMI's practice notes add that it stays short, reports outcomes, and puts the bad news and the decision where a reader sees them. A project adapts the sections. It does not replace the report with a free essay.

This file chooses the template. It is not a report.

## Shipped

| Id | Manual | Use when |
| --- | --- | --- |
| `status` | [status-report.md](status-report.md) | The period, the status, what finished, what is blocked, and what is next. This is the default. |

## Which file is read

The output folder is `adrenaline/project-manager/`, or the path `outputDirs["plugin-project-manager"]` in `.cursor/adrenaline.json` when that path is relative, has no `..`, and is not absolute. If `adrenaline/project-manager/` does not exist yet and `project-manager/` at the project root already has this plugin's `ORIGIN.json` or `STATUS.md`, use that folder.

1. The person names an id. Look for `<output>/templates/status-report/<id>.md`. If that file exists, it is the template.
2. If that file does not exist, and the id is `status`, read [status-report.md](status-report.md).
3. If the id is neither a project file nor `status`, write no report. Name `status` and every `<output>/templates/status-report/*.md` that was found.
4. If they name no template, use `status`. Record it under Assumed: template `status`, because none was selected. Name any project template that was found. Change it by naming the id in `/pm-status`. Regenerate the report with `/pm-status`.

A project template wins over the shipped id `status` only when they give it another id. The shipped file is not edited from a project.

## A template the project owns

Path: `<output>/templates/status-report/<id>.md`. `<id>` is English, lowercase, with hyphens, and it is not `status`.

```markdown
---
id: acme-weekly
piece: status-report
based_on: status
---

## Header
required
Project, period, and the date of this report.

## Decisions needed
required
The ask, from whom, and by when. None, when there is no ask.
```

`based_on` is `status`. The writing rules in [status-report.md](status-report.md) still apply.

- A `required` heading of the base stays, with that base's meaning. The visible heading may be renamed.
- An `optional` heading of the base may be dropped.
- A new heading is allowed and becomes required for every report that names this id.
- Cost, a forecast, a baseline date, and a person's name are still written only when the person gives them. A new heading does not create permission to invent them.
- The artifact follows the language of the request. Translate the headings. Keep the id.
- Instructions under a heading are not copied into the report.

When the person asks to create or change a project template, write only that file. Create the output folder if it is missing, and write `ORIGIN.json` beside `STATUS.md` if either is missing. Do not write a report in that turn unless they also asked for one.

## Done

This file is not a situation. The delivery is the progress report. Evaluate `## Done` in the manual this file selects. The template recorded on the report is the one selected here.
