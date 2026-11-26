# Next session

## Read first

1. [AGENTS.md](AGENTS.md)
2. [STATUS.md](STATUS.md)
3. [DECISIONS.md](DECISIONS.md)
4. [The ADC analytical reference](examples/github-setup/adc-quantization.md)

Inspect the current working tree and project directory before changing anything. If the work below has already been completed, update this handoff instead of duplicating it.

## Suggested task: an ideal ADC conversion exercise

**Goal:** Create a small original C++ exercise that implements and explains the declared ideal 12-bit, 3.3 V floor/bin model.

**Proposed home:** `c-programming/adc-quantization/`.

**Current state:** The analytical reference exists. This setup does not supply or claim a compiled C++ implementation.

### Work to do

1. Explain why 12 bits produce 4,096 codes and why the highest integer code is 4,095.
2. Specify accepted input and out-of-range behavior. Keep the mathematical model separate from any real device's electrical limits.
3. Implement the calculation in a small understandable program. Keep the input/reference units explicit.
4. Build with the actual local compiler and save its version and exact command in the project README.
5. Check meaningful inputs: zero, quarter scale, half scale, a value just below full scale, full scale, and invalid values.
6. Explain floating point and rounding choices near bin boundaries.
7. Save the actual run results and add an accurate entry to [PORTFOLIO_INDEX.md](PORTFOLIO_INDEX.md).

Use [the C++ documentation template](templates/cpp-project/README.md) as needed. Add tests only when they help verify the implemented behavior; independent expected values matter more than the size of a test suite.

### Success evidence

- Original source in the project folder.
- A README explaining the model, input handling, build command, and limitations.
- Actual compiler and run results, with expected values based on the analytical model.
- An explanation Akili can discuss in his own words.

No hardware is required for this software exercise. Completing it would establish a tested mathematical program, not physical ADC accuracy.

## Handoff after the session

Update the project README and [STATUS.md](STATUS.md). Replace this next task with the next useful action. Record what actually changed and what remains unverified.
