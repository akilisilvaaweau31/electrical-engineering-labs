# [SPICE experiment name]

**Question:** [What behavior does the simulation investigate?]

**State:** Template. The supplied RC reference netlist has not been simulated as part of this setup.

## Source of truth

Save the editable schematic or netlist. If both are present, identify which is authoritative and how the other was generated. Store a README with the assumptions and the simulator version used.

For LTspice work, place the project in an appropriately named subfolder under the existing `ltspice/` directory. Keep large generated raw outputs outside ordinary Git history unless there is a specific reason to retain them.

## Before running

- Predict the response and calculate one reference value.
- Confirm component values, units, ground, sources, and node labels.
- Identify model origins and any redistribution restrictions.
- Choose analysis settings that resolve the behavior of interest.

## Run record

| Setting | Actual value |
| --- | --- |
| Simulator/version | Not recorded |
| Source file/commit | Not recorded |
| Analysis | Not run |
| Time span and maximum step, if transient | Not recorded |
| Initial conditions | Not recorded |
| Parameter sweep | None specified |
| Output trace/expression | Not recorded |

## Selected evidence

Save a small useful plot with labeled axes and units, and a compact table of important values. Record exactly how those values were obtained. Keep run warnings and convergence problems in the project note.

## Reference circuit included

[`rc-step-reference.cir`](rc-step-reference.cir) supplies a simple 10 kΩ / 1 µF RC example with a 3.3 V pulse and a nominal 10 ms time constant. It is reference source, not a record of an executed simulation. Its input rise time is finite; the analytical reference assumes an ideal step. Compare that distinction when inspecting the result.

See [the analytical RC example](../../examples/github-setup/rc-step-response.md). If you copy this template into another folder, update this relative link or replace it with the project's own analytical record.

## Conclusion

Compare the actual simulated result with the predicted value. Explain any difference before calling it a model failure. State what remains unverified on hardware.
