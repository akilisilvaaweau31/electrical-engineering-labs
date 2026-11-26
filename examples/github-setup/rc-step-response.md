# Worked example: RC step response

**Evidence type:** Analytical example written for this GitHub setup.

**Not performed:** SPICE execution, physical assembly, or bench measurement.

## Question

How quickly does an initially uncharged capacitor rise toward 3.3 V through a 10 kΩ resistor?

## Predict

The capacitor voltage should start at 0 V and approach the source voltage smoothly. A larger resistance or capacitance should make the response slower. The ideal capacitor voltage cannot jump instantaneously under a finite current.

## Model and assumptions

- Ideal 3.3 V step source at `t = 0`.
- Series resistor `R = 10,000 Ω`.
- Capacitor `C = 1 µF = 1 × 10^-6 F` from output to ground.
- Initial capacitor voltage `Vc(0) = 0 V`.
- No leakage, parasitics, source resistance beyond R, or instrument loading.
- Nominal component values are exact in this calculation; real tolerances are not included.

## Solve

Kirchhoff's current relation gives:

`C dVc/dt = (Vs − Vc) / R`

The time constant is:

`τ = RC = 10,000 × 1 × 10^-6 = 0.010 s = 10 ms`

For `t ≥ 0`:

`Vc(t) = Vs × (1 − exp(−t/τ))`

### Calculated values

| Time | Time constants | Calculated capacitor voltage | Fraction of final voltage |
| --- | --- | --- | --- |
| 0 ms | 0τ | 0.000000 V | 0.0000% |
| 10 ms | 1τ | 2.085998 V | 63.2121% |
| 20 ms | 2τ | 2.853394 V | 86.4665% |
| 30 ms | 3τ | 3.135703 V | 95.0213% |
| 40 ms | 4τ | 3.239558 V | 98.1684% |
| 50 ms | 5τ | 3.277765 V | 99.3262% |

To reach a fraction `p` of the final value:

`t = −τ ln(1 − p)`

Therefore, the calculated time to 90% is about `23.0259 ms`, and the time to 99% is about `46.0517 ms`. “Five time constants” means close to final voltage, not exactly equal to it.

## Sanity checks

At `t = 0`, `exp(0) = 1`, so the result is 0 V. As time grows, the exponential term approaches zero, so the result approaches 3.3 V.

The initial resistor current is:

`I(0+) = 3.3 V / 10,000 Ω = 0.00033 A = 330 µA`

The initial capacitor slope is:

`dVc/dt at 0+ = I/C = 330 V/s = 0.33 V/ms`

These are analytical predictions. They have not been measured.

## Simulate next

The [reference netlist](../../templates/spice-project/rc-step-reference.cir) is supplied for a future SPICE run. It uses a finite input rise time and a transient analysis through 50 ms. Record the actual simulator/version, settings, output, and any warnings. Compare `V(out)` near 10 ms and 50 ms with the analytical values above.

The netlist has not been executed during this setup. Simulator results must be recorded separately from this table.

## Measure later

For a suitable real circuit, record actual component values, source behavior, instrument input loading, probe settings, and timing resolution. Compare observations with the prediction and examine whether component tolerance or the measurement setup explains any difference.

Do not fill the measurement column with calculated numbers.

## Explain

The resistor limits current. As the capacitor voltage rises, the voltage across the resistor falls, so the charging current and voltage slope decrease. That feedback produces the exponential approach to the final voltage.

Changing R or C scales the time constant. The ideal final voltage is still 3.3 V under this model, provided there is no additional loading path.

## Provenance

This original educational example follows from the stated ideal circuit equations. It was created with AI assistance and is not a record of a completed Akili lab.
