<p align="right">Language:&emsp;<img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-on.svg" align="middle" style="vertical-align:middle"> <a href="fully-dressed.es.md" style="vertical-align:middle"><img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-off.svg" align="middle" style="vertical-align:middle"></a></p>

[🏠 Project Manager](../../../README.md) / [Write the use case](../SKILL.md)

# Fully dressed use case

Source: Alistair Cockburn, *Writing Effective Use Cases*. Fully dressed is the casual story plus the fields a higher-ceremony case needs. The file type is `use-case`. The template id is `fully-dressed`.

## What it fixes

The same goal as the casual case, with the boundary, the level, who else cares, what starts it, and what is guaranteed if it works or if it stops.

## Writing rules

The casual rules apply: 3 to 9 steps, the actor in each step, intention not interface, no "if" in the main scenario, data by nickname, black box, no invented product outcome.

Also:

- Scope names the system under discussion. For a system requirement, that system is a black box: the case designs everything inside it and nothing outside it. A white-box business case is allowed only when the person says the case describes the organization, not a system to build.
- Level is one of `summary`, `user-goal`, or `subfunction`. The steps sit one level below the case. A user-goal case is not a summary of a whole business, and it is not a single click.
- Every stakeholder is named with the interest the system must satisfy. The primary actor is one of them.
- Preconditions are mandatory and already true. They are not checked again in the scenario.
- The success end condition satisfies the interests. The failed-end protection protects them when the goal is not met. Both are about the stakeholders, not about a stack trace.
- The trigger is the event that starts the case. It is not step 1.
- The main success scenario runs from the trigger to the success end condition.
- Each extension names the step it leaves (`4a`). Its handling returns to the main scenario, ends in another success, or fails under the failed-end protection.
- List the extension conditions before writing their steps. A system failure the system must detect is an extension condition in one line. Its handling is asked of `plugin-qa-engineer`. Do not write the test scenario.
- Priority, frequency, and channel are optional. Write them only when the person gives them.

## Template

Headings, in this order. Translate them. Keep the template id.

## Actor

required. Primary actor and the goal, as a short active verb phrase.

## Scope

required. The system under discussion. Say black box, unless the person asked for a white-box business case.

## Level

required. `summary`, `user-goal`, or `subfunction`.

## Stakeholders

required. Each name and the interest that must be satisfied. If a stakeholder was not named, the gap says who is missing. Do not invent a regulator, an owner, or a persona.

## Preconditions

required. Already true. Not rechecked in the scenario.

## Success end

required. What is true when every interest that this success covers is met.

## Failed end

required. What stays protected when the goal is not met.

## Trigger

required. The event that starts the case.

## Main success scenario

required. Numbered steps, 3 to 9.

## Extensions

required. Condition, the step it leaves, and the handling. A system failure is one line that asks `plugin-qa-engineer`. If there is no extension, write "None."

## Related

optional. Priority, frequency, or channel, and only the values the person gave. Omit the heading when they gave none.

## Done

- The required headings are present, in this order, in the language of the request. The template id `fully-dressed` is recorded in `notas`. Related appears only when the person gave a value.
- Level is one of the three names. Scope says whether the system is a black box.
- The main scenario has 3 to 9 steps, with no "if". Each extension names the step it leaves and where it ends.
- A system failure asks `plugin-qa-engineer` and does not contain the test scenario.
- No stakeholder, guarantee, trigger, or related value was invented. A required heading with no fact is a gap and the file is `proposed`.
