# Worked example: ideal 12-bit ADC quantization

**Evidence type:** Analytical example written for this GitHub setup.

**Not performed:** Hardware measurement, device characterization, or simulator execution.

## Question

How does an ideal 12-bit converter represent an input from 0 to 3.3 V, and why do both 4,096 and 4,095 appear in ADC calculations?

## Predict

More bits should create more possible codes and narrower voltage intervals. Half the reference voltage should fall near the middle of the available codes. Quantization will prevent a single output code from specifying every possible input voltage exactly.

## Solve

Assume an ideal unipolar converter with `N = 12` and `Vref = 3.3 V`. This example uses a **floor/bin model**: divide `[0, Vref)` into equal bins and clamp the endpoint to the highest code. This is a declared mathematical convention; an actual ADC's transition levels, offsets, and transfer function must come from its datasheet.

The number of possible codes is:

`2^12 = 4,096`

The integer codes run from `0` through `4,095`, inclusive. The ideal bin width is:

`q = Vref / 2^N = 3.3 / 4,096 = 0.0008056640625 V`

That is approximately `0.805664 mV` per bin.

For an in-range input under this model:

`code = min(4,095, floor(Vin / q))`

This expression assumes `0 ≤ Vin ≤ Vref`. Out-of-range input handling is a separate requirement; do not infer a device's electrical tolerance from this mathematical clipping rule.

### Representative inputs

| Input voltage | Input / q | Code | Comment |
| --- | --- | --- | --- |
| 0 V | 0 | 0 | Lowest bin |
| 0.825 V | 1,024 | 1,024 | Quarter of the reference |
| 1.65 V | 2,048 | 2,048 | Half of the reference |
| 3.3 V | 4,096 | 4,095 | Endpoint clamped to highest code |

Under the declared floor model, an interior code `k` corresponds to the interval:

`kq ≤ Vin < (k + 1)q`

For code `2,048`, that is approximately `1.650000 V ≤ Vin < 1.650806 V`.

If the code is reconstructed as the bin midpoint, the estimate is:

`Vmid = (k + 0.5)q`

For code `2,048`, `Vmid = 1.65040283203125 V`. For an input inside its ideal bin, midpoint reconstruction has a quantization error of at most half a bin, approximately `0.402832 mV`, ignoring all real-device errors.

### Why 4,095 also appears

The endpoint mapping:

`Vdisplay = code × Vref / (2^N − 1)`

maps code `0` to 0 V and code `4,095` to 3.3 V. It is a common display/scaling choice, but it is not the same quantity as the ideal bin width `Vref / 4,096`.

For code `2,048`, endpoint mapping gives approximately `1.650403 V`. This happens to be close to the midpoint estimate here; the definitions still differ. Choose a conversion consistent with the actual ADC specification and your measurement/calibration goal.

## Engineering interpretation

An ADC code alone does not establish the true voltage to arbitrary precision. Real systems may also have reference error, offset, gain error, nonlinearity, noise, source impedance effects, and sampling constraints. None of those effects has been measured in this example.

## Software experiment to do next

Implement the declared model in a small C++ program. Handle invalid input explicitly and test zero, half scale, just below full scale, full scale, and out-of-range values. Decide and document how floating point inputs near bin boundaries are treated. Compare expected values with actual program output before recording software verification.

## Hardware experiment to do later

Select a real ADC/board, read its transfer function and input limits, then compare safe known inputs with recorded codes and an appropriate voltage measurement. Save the actual conditions and uncertainty; do not treat this ideal example as a calibration.

## Provenance

The values above follow directly from the stated ideal model and arithmetic. This is an educational reference created with AI assistance, not a claim that Akili completed a device test.
