<p align="right">Language:&emsp;<img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-on.svg" align="middle" style="vertical-align:middle"> <a href="casual.es.md" style="vertical-align:middle"><img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-off.svg" align="middle" style="vertical-align:middle"></a></p>

[🏠 Project Manager](../../../README.md) / [Write the use case](../SKILL.md)

# Casual use case

Source: Alistair Cockburn, *Writing Effective Use Cases*. The casual form keeps a readable story and drops the ceremony fields. The file type is `use-case`. The template id is `casual`.

## What it fixes

Who wants what, what is already true, the path on which they get it, another business way, and what is true when it works.

## Writing rules

These rules are the practice. A project template does not remove them.

- The title is the goal: a short active verb phrase, with the actor.
- The main flow has 3 to 9 numbered steps. Each step names who acts and a goal that succeeds. Write the intention, not the screen, the click, or the control.
- A step moves the story forward. One actor passes information, checks a condition, or changes state.
- No "if" inside the main flow. Another business way is an alternate, tied to the step it leaves (`2a`), written after the main flow.
- An alternate returns to a main step, ends in success, or stops. Say which.
- A system failure, an exception, or test data is named in one line and asked of `plugin-qa-engineer`. Do not write the test scenario.
- A precondition is already true before step 1. Do not repeat it as a step.
- Name data by a nickname. Field lengths, types, and validation stay out of the case.
- The system is a black box. Do not describe its internals, its modules, or its tables.
- Do not discover the business outcome. Cite an accepted file from `plugin-product` when one exists.

## Template

Headings, in this order. Translate them into the language of the request. Keep the template id.

## Actor

required. Who starts it, and the goal.

## Preconditions

required. What is already true. If nothing is known, the gap says so. Do not invent a login, a role, or a state.

## Main flow

required. Numbered steps, 3 to 9, each with the actor and a goal that succeeds.

## Business alternates

required. One block per alternate: the step it leaves, the business condition, the steps, and where it ends. If there is no alternate, write "None." An alternate that is a system failure is one line that asks `plugin-qa-engineer`.

## Postconditions

required. What is true when the goal is met. An alternate that stops says what is true instead.

## Done

- The five headings are present, in this order, in the language of the request. The template id `casual` is recorded in `notas`.
- The main flow has 3 to 9 steps. Each step names who acts. There is no "if" in the main flow. A business alternate sits under Business alternates and says where it ends.
- A system failure is one line that asks `plugin-qa-engineer`. The test scenario is not in this file.
- No screen, click, module, table, or field length was added. No outcome from `plugin-product` was invented.
- The state is `accepted` only when every required heading is filled from something the person said or from an accepted file. A heading that had to be guessed stays a gap and the file is `proposed`.
