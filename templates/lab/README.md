# [Project name]

**Question:** [What precise engineering question are you investigating?]

**State:** [Planned / analytical / software tested / simulated / measured; list all that actually apply]

**Date and revision:** [Date; commit or version when available]

**My contribution:** [What you did; distinguish source material and assistance]

## 1. Predict

Before calculating or running anything, predict the direction, approximate magnitude, and behavior. Explain why.

- Expected initial and final conditions:
- Expected trend when the input or a component changes:
- Approximate scale or order of magnitude:
- What observation would contradict the prediction:

## 2. Solve

Draw or link the circuit/system. Define every variable and its unit.

| Quantity | Symbol | Value | Unit | Origin or assumption |
| --- | --- | --- | --- | --- |
| [Quantity] | [Symbol] | [Value] | [Unit] | [Measured / specified / assumed] |

Show the governing equation, substitution, result, and a unit check. State the model's assumptions and the conditions where it may fail.

**Calculated result:** [Value, units, and appropriate precision]

**Independent sanity check:** [Limiting case, approximate calculation, conservation, or another suitable check]

## 3. Simulate

**Status:** [Not run / run on date]

- Source/model files:
- Simulator and version:
- Model origin, license or redistribution constraints, and revision:
- Analysis type, solver settings, time span, and step settings:
- Exact steps to reproduce:
- Output file or selected plot:

Compare the simulated output with the analytical result. Explain meaningful differences. Do not fill in simulated values until a simulation has actually run.

## 4. Measure

**Status:** [Not measured / measured on date]

- Equipment and instrument models:
- Relevant ranges, resolution, probe/loading settings:
- Calibration status, if known:
- Component identifiers and tolerances:
- Physical connections and supply conditions:
- Environmental conditions that materially matter:
- Procedure and repetitions:
- Raw observation file:

Use [measurements.csv](measurements.csv) as an optional starting form. Adapt its columns to the experiment and keep units explicit. Record unexpected observations rather than discarding them silently.

## 5. Compare and explain

| Quantity | Analytical prediction | Simulation | Measurement | Units | Notes |
| --- | --- | --- | --- | --- | --- |
| [Quantity] | [Value] | Pending | Pending | [Unit] | [Assumptions/conditions] |

When meaningful and the reference is nonzero:

`relative difference (%) = 100 × (observed − reference) / reference`

Identify the reference explicitly. Use an absolute difference when a relative comparison is undefined or misleading. A disagreement may reveal a model limitation, setup issue, component tolerance, or arithmetic error; investigate before choosing an explanation.

## 6. Uncertainty and limitations

Identify the main uncertainty contributors. Use [uncertainty-budget.csv](uncertainty-budget.csv) if a quantitative budget is appropriate. State assumptions behind any combined value.

- What the evidence supports:
- What remains unknown:
- Largest limitation of this setup/model:
- Conditions not tested:

## 7. Conclusion

Answer the original question in a short paragraph. Explain what changed in your understanding and what you would investigate next.

## Reproduce this work

1. [Required tools/files]
2. [Exact command or procedure]
3. [Expected observable result and tolerance]

## References and assistance

| Source | Version/date/section | Used for | Link |
| --- | --- | --- | --- |
| [Primary source] | [Identifier] | [Specific claim/model] | [URL] |

AI or collaborator contribution: [Describe or state none]

## Next step

[One concrete action; do not claim it is complete.]
