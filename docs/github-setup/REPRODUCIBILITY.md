# Reproducibility and evidence

A future reader should be able to understand your result and, when the required equipment is available, repeat it.

## Separate evidence types

| Label | What supports it | What it does not establish |
| --- | --- | --- |
| Analytical | Equations, assumptions, units, and calculations | Device behavior in a real circuit |
| Synthetic | Deliberately generated input or data | A real sensor or measured system |
| Software tested | Actual commands, inputs, expected behavior, and observed outputs | Hardware validation |
| Simulated | Saved model/source, simulator version, settings, and output | Bench performance |
| Measured | Instrument, conditions, raw observations, units, and procedure | Performance outside the measured conditions |
| Reviewed | Identified reviewer and review scope | Execution or physical testing unless included explicitly |

Write “not run,” “not measured,” or “unknown” where appropriate. Do not turn a prediction into a result by copying it into a table of observations.

## Minimum project record

- The engineering question and why it matters.
- The exact source files used, preferably identified by a commit.
- Assumptions and operating conditions.
- Relevant tool versions and commands or settings.
- Inputs, outputs, units, and acceptance criteria.
- A plain language explanation of the result and its limits.
- A citation for each external device/model/specification claim.

For a datasheet, record the manufacturer, part number, revision or date, URL, and page or section. Link to the vendor source. Do not redistribute a file just because it can be downloaded publicly.

## Measurement discipline

Record the instrument model, range, resolution, calibration information if known, loading or probe settings, and the method. “Calibration status unknown” is better than implying a calibration you cannot document.

Save raw observations before averaging or filtering. Keep processed data separate and document how it was produced. Use explicit units in column names, such as `input_voltage_V` and `elapsed_time_s`.

An uncertainty budget should name each contributor, its basis, distribution assumption, standard uncertainty, and sensitivity coefficient where applicable. Combining contributions by root sum of squares assumes the relevant contributions can be treated as independent; correlated contributions require a different treatment. If you cannot justify those assumptions, report the components or bounds instead of an unjustified precise combined value.

Repeatability, instrument resolution, tolerance, and systematic bias are different things. More decimal places do not create more accuracy.

## Reproducing software

Record exact build and run commands. Keep dependencies minimal. If dependencies are required, save the appropriate version/lock information and explain the supported environment. Do not claim a build is portable until another environment has actually been checked.

Small deterministic examples should state their expected result. Real algorithms should also explain tolerances and boundary behavior. A passing assertion only supports the case it exercises.

## AI assistance

Use the [AI assistance record](../../templates/ai-assistance.md) when AI made a substantive contribution. Describe which parts were generated, edited, or reviewed, and what you personally checked. Do not paste entire chat histories by default; keep the engineering decisions and relevant provenance.

AI assistance is not independent validation. An explanation you cannot yet defend belongs in your learning notes until you understand it.

## Before sharing a result

Check that links work, source and output match, units are clear, the result can be traced to evidence, and unsupported claims have been removed. Include one honest limitation and one useful next experiment.
