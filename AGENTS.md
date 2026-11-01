# plugin-project-manager

Writes the use case, the task that crosses repositories, the progress report, the sprint plan, and the ordered backlog. The procedure is in the skills under `skills/`.

Files go in `adrenaline/project-manager/` at the project root, or in the path `.cursor/adrenaline.json` sets under `outputDirs["plugin-project-manager"]`. If `adrenaline/project-manager/` does not exist yet and `project-manager/` at the project root already has this plugin's `ORIGIN.json` or `STATUS.md`, keep writing there and say so. A use-case diagram is asked of `plugin-uml-diagrams`. A test scenario is asked of `plugin-qa-engineer`. The opportunity stays with `plugin-product`. A project template lives in `templates/` inside the output folder and is not an `<NNN>` file.
