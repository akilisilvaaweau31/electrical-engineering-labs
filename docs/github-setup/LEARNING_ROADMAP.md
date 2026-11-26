# Learning direction

This is a suggested project sequence, not a record of completed courses and not a replacement for a college education plan. Course prerequisites and transfer requirements must come from current college and university sources.

## Near-term foundation

| Focus | Small useful artifact | Evidence to keep | Readiness to move on |
| --- | --- | --- | --- |
| Units, algebra, vectors, calculus | A short engineering calculation with diagrams and units | Assumptions and a check of the answer | Explain the result without reading the solution |
| C/C++ fundamentals | A small program that handles numeric input and boundary cases | Source, build command, representative outputs | Explain the types, control flow, and failure cases |
| DC circuits | Divider, loading, or simple network analysis | Schematic, hand solution, simulation when run | Predict the direction of change before calculating |
| Transients | RC step-response study | Analytical solution, later simulation and measurement | Explain time constant and initial/final conditions |
| Digital logic | A truth table and implemented Boolean function | Derivation and exhaustive small-input checking | Explain each state or input combination |

Use the [ADC](../../examples/github-setup/adc-quantization.md) and [RC](../../examples/github-setup/rc-step-response.md) examples as starting points for your own explanations.

## After the foundation

| Direction | Useful project | What makes it worth showing |
| --- | --- | --- |
| Embedded systems | Read a physical input and report it reliably | Timing, calibration assumptions, error handling, and actual board evidence |
| Instrumentation | Capture and analyze a small set of measurements | Known source, traceable data, units, and honest uncertainty |
| Digital hardware | A small state machine or counter | State diagram, implementation, and verified behavior |
| Controls | Model a simple system and compare response | Clear model assumptions and quantitative error |
| Integrated project | A tool solving one real debugging or measurement problem | A demonstration another person can repeat |

Choose hardware and additional tools when a specific project requires them. Existing software can support a substantial amount of early analysis and programming work.

## Sustainable weekly pattern

Keep course work and fundamentals first. A useful portfolio session can be small: one derivation, one code improvement, or one measured observation with an explanation. Prefer a small finished result over several empty project folders.

At a weekly review, identify the strongest completed evidence, the most important unanswered question, and the next single project action. Move inactive ideas to a backlog so they do not compete with current studies.

## How this supports your career direction

Build evidence that transfers to embedded firmware, digital hardware, controls, and instrumentation: reasoning about signals, implementing reliable code, reading specifications, measuring correctly, and explaining tradeoffs. Your earlier practical experience can provide context without dictating the engineering specialty you pursue.
