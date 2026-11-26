# Electrical engineering portfolio index

This index separates the repository's established subject areas from new reference material. A folder or template does not imply a completed project.

## Existing subject areas

| Area | Home | Put here |
| --- | --- | --- |
| C and C++ | `c-programming/` | Original programs, small reusable functions, build instructions, and test evidence |
| Circuits | `circuits/` | Circuit analysis, schematics, measurements, and explanations |
| Digital logic | `digital-logic/` | Truth tables, Boolean reasoning, logic diagrams, and later HDL projects |
| Embedded systems | `embedded/` | Firmware and board-specific experiments when hardware is actually selected |
| LTspice | `ltspice/` | Editable simulation sources, model provenance, and selected results |
| PCB design | `pcb-design/` | Owned schematic/layout sources and fabrication decisions when work begins |
| Integrated projects | `projects/` | Projects combining several areas into one demonstrable result |

Repository inspection on 2026-11-25 found a README in each of these folders. This setup does not claim additional programs, simulations, or hardware builds existed at that inspection.

## New reference examples

| Item | Evidence type | Status |
| --- | --- | --- |
| [12-bit ADC quantization](examples/github-setup/adc-quantization.md) | Worked analytical example | Written for this setup; no hardware measurement |
| [RC step response](examples/github-setup/rc-step-response.md) | Worked analytical example | Written for this setup; simulation and measurement pending |
| [RC SPICE source](templates/spice-project/rc-step-reference.cir) | Reference source | Supplied for a future simulation; not run as part of this setup |

## Start a real project

1. Read [the start guide](docs/github-setup/START_HERE.md).
2. Choose one [template](templates/README.md).
3. Create a descriptively named subfolder inside the relevant existing subject area.
4. Add a row below only when an actual project has a README and evidence to review.

## Project register

| Project | Question or purpose | Current evidence | Next step | README |
| --- | --- | --- | --- | --- |
| No project entries added by this setup | Existing work must be inventoried before claiming completion | Unknown | Add verified projects individually | — |

Use explicit evidence descriptions such as “analytical calculation reviewed,” “simulation run saved,” or “bench measurements recorded.” Avoid a generic “complete” label that hides missing stages.
