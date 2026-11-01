<p align="right">Language:&emsp;<img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-on.svg" align="middle" style="vertical-align:middle"> <a href="status-report.es.md" style="vertical-align:middle"><img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-off.svg" align="middle" style="vertical-align:middle"></a></p>

[🏠 Project Manager](../../../README.md) / [Report progress](../SKILL.md)

# Status report

Source: *PMBOK Guide*, 7th edition, section 4.6.7. The report states the current status and the progress since the previous report. Cost and schedule forecasts are included only when the person supplies the figures. The file type is `status-report`. The template id is `status`.

The shape follows the one-page practice: the same sections in the same order, outcomes rather than activity, and the status and the decision before the detail. PMI's notes on a report a reader will use: keep it short, stay objective, and do not bury a blocker.

## What it fixes

Where the work stands this period, what finished, what is blocked, what comes next, and whether a decision is needed.

## Writing rules

A project template does not remove these rules.

- The same headings, in this order, every report. A reader learns where to look.
- The period is explicit: start and end, or the name of the sprint already written. A report with no period is a gap.
- Overall status is one of `on track`, `at risk`, or `off track`. If it is not `on track`, the summary states why in its first sentence.
- Report outcomes that finished. A meeting, a percentage with no result, and "almost done" are not Done this period.
- Done this period and In progress are separate. An item is in one of them.
- A blocker names what it is waiting on. Add who can unblock it, and since when, only when the person said so.
- Next is what will be finished before the next report. When a previous report of this subject exists, compare this period's Done with that report's Next. A missed item is named. Do not drop it.
- A date that a previous report stated stays visible. This report may add a new forecast beside it. It does not replace the earlier date.
- Decisions needed is the ask, from whom, and by when. When there is no ask, write "None." Do not invent a decision.
- A cost, a budget, a forecast, a baseline date, or a person's name enters only when the person gives it. Do not compute one.
- Cite a use case or a task by the file this plugin wrote, or by the name the person gave this turn. Do not add work from nowhere.
- This is not a test report, a product metric, or a Diátaxis document. Do not write those.

## Template

Headings, in this order. Translate them into the language of the request. Keep the template id.

## Header

required. The subject, the period, and the date of this report. The author only when the person names one.

## Overall status

required. `on track`, `at risk`, or `off track`, and one line. The line is the reason when the status is not `on track`.

## Summary

required. Up to three sentences: where it stands, what changed this period, what decision is needed. If none is needed, the third sentence says so.

## Done this period

required. Finished outcomes, each with the file or the name it cites. "None." when nothing finished.

## In progress

required. Work started and not finished. "None." when nothing is in progress.

## Blockers

required. What it waits on. "None." when nothing is blocked.

## Next

required. What will be finished before the next report.

## Decisions needed

required. The ask, from whom, and by when. "None." when there is no ask.

## Figures

optional. Only numbers and dates the person gave: cost, schedule, baseline beside forecast. Omit the heading when they gave none. Do not write "estimated".

## Done

- The required headings are present, in this order, in the language of the request. The template id `status` is recorded in `notas`. Figures appears only when the person gave a number or a date.
- Overall status is one of the three words. A status that is not `on track` gives the reason in the first sentence of Summary.
- Done this period contains finished outcomes, not activity. It does not share an item with In progress.
- A previous report's Next is compared, and a previous date is not replaced.
- No cost, forecast, name, decision, or task was invented. "None." is a filled section. A required heading with no fact and no honest "None." is a gap, and the file is `proposed`.
