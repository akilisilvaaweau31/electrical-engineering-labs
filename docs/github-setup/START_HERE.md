# Start here: make the repository useful

Use this repository as a record of engineering work you can explain. The goal is a growing set of reproducible projects, each with a clear question and evidence.

## Your first session

1. Open the repository in GitHub Desktop or your existing Git workflow and confirm there are no unrelated changes to accidentally include.
2. Choose one small exercise. Good starting points are the [ADC example](../../examples/github-setup/adc-quantization.md) or [RC example](../../examples/github-setup/rc-step-response.md).
3. Copy the whole `templates/lab/` folder, including its [lab record](../../templates/lab/README.md) and blank CSV forms, into a new folder in the appropriate existing subject area. Example destinations: `circuits/rc-step-response/` or `c-programming/adc-conversion/`.
4. Fill in only what you actually did. Leave later stages marked pending.
5. Record the source files, the command or procedure, and the result. Commit the small coherent change and push it.
6. Add the project to [the portfolio index](../../PORTFOLIO_INDEX.md) when the project has real content.

You do not need to complete prediction, analysis, simulation, and measurement in a single sitting. The status should tell the truth about the work so far.

## What to save

| Save | Why |
| --- | --- |
| Original source code and small test inputs | Rebuild and understand the result |
| Editable schematics, simulation netlists, and owned board design sources | Preserve the engineering decisions |
| A short README per project | Explain the question, setup, result, and limitations |
| Small, selected measurement data with units and conditions | Support quantitative claims |
| A few useful plots or annotated photos | Make evidence easy to inspect |
| Decisions and error investigations | Show your reasoning and avoid repeating mistakes |
| Build/run instructions and tool versions | Let your future self reproduce the work |

Large raw simulation dumps, installers, copied textbooks, videos, credentials, and personal records need another home. Keep a pointer and checksum when an external artifact is necessary to reproduce the project.

## Use the existing folders

Do not reorganize everything before doing engineering. Put each new project in its closest existing category:

- `c-programming/`: C and C++ exercises, including math and data conversion tools.
- `circuits/`: analysis and measurement centered circuit projects.
- `digital-logic/`: combinational and sequential logic.
- `embedded/`: firmware and microcontroller experiments.
- `ltspice/`: simulation centered experiments.
- `pcb-design/`: schematic/layout projects when they begin.
- `projects/`: integrated builds spanning several categories.

Use a lowercase descriptive name such as `adc-quantization`, `rc-step-response`, or `button-debounce`. Keep a single canonical copy of a project. Link to it from other categories instead of duplicating its files.

## Useful reading

- [Everyday workflow](WORKFLOW.md)
- [Reproducibility and evidence](REPRODUCIBILITY.md)
- [Learning direction](LEARNING_ROADMAP.md)
- [Portfolio and résumé evidence](PORTFOLIO_GUIDE.md)
- [Templates](../../templates/README.md)

This directory is guidance added on 2026-11-25. It does not overwrite earlier project instructions or establish completed coursework, builds, or certifications.
