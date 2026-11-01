<p align="right">Language:&emsp;<img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-on.svg" align="middle" style="vertical-align:middle"> <a href="backlog.es.md" style="vertical-align:middle"><img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-off.svg" align="middle" style="vertical-align:middle"></a></p>

[🏠 Project Manager](../../../README.md) / [Order the backlog](../SKILL.md)

# Ordered backlog

Source: Scrum Guide, 2020. The Product Backlog is an ordered list of what is needed. The Product Owner is accountable for that order. In this suite the business outcome stays with `plugin-product`. This file is the delivery list. GitHub Issues, GitHub Projects, and Azure Boards stay the tracker. The file type is `backlog`.

## What it fixes

The order of the work, and the link from each item to a use case, a task, or a tracker id the person already has.

## How to do it

1. The order is the order the person gave. Do not sort by a value you inferred. If they gave no order, the list is a gap and the file stays `proposed`.
2. Each item has a name. When a use-case or task file exists, cite it. When it does not, the item stays one line and says the file is missing.
3. A GitHub issue URL or an Azure work-item id is written only when the person gives it. Do not create the issue and do not move a column.
4. When an accepted outcome from `plugin-product` exists, cite it once, above the list. Do not rewrite the outcome and do not reorder the list to match it unless the person says to.
5. One backlog file is one list. A later order is the next `<NNN>`, and the previous row becomes `superseded`, unless the person asks to amend the same file.

## Template

Headings, in this order. Translate them.

## Outcome

optional. The accepted `plugin-product` file, when one is cited. Omit the heading when none is cited.

## Items

required. A numbered list. Each item: the order, the name, the use-case or task file when it exists, and the tracker link when the person gave one.

## Done

- Items are numbered in the order the person gave, in the language of the request.
- No item, tracker link, or outcome was invented. A missing file is named as missing. No issue was opened.
- The state is `accepted` only when the order and at least one item came from the person. No order is a gap and the file is `proposed`.
