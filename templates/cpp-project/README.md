# [C or C++ project name]

**Purpose:** [One engineering or programming problem]

**State:** Template; no source program or passing build is supplied by this template.

## Inputs and behavior

| Input | Type and unit | Accepted range | Invalid-input behavior |
| --- | --- | --- | --- |
| [Name] | [Type/unit] | [Range] | [Reject / report / defined fallback] |

**Output:** [Meaning, units, format, and precision]

**Mathematical model:** [Equation, assumptions, and references if applicable]

## Suggested layout

| Path | Purpose |
| --- | --- |
| `src/` | Implementation source |
| `include/` | Headers when the project actually needs them |
| `tests/` | Meaningful verification cases when needed |
| `examples/` | Small nonprivate input examples |
| `docs/` | Design explanations or output figures |
| `build/` | Local generated outputs; normally ignored |

Create only the directories the project uses. Do not add a framework before a simple compiler command becomes inadequate.

## Build

Record the actual compiler version and environment. For a single-file C++ program placed at `src/main.cpp`, this is an example command to adapt in MSYS2 UCRT64 or another environment with GCC:

```bash
mkdir -p build
g++ -std=c++20 -Wall -Wextra -Wpedantic -g src/main.cpp -o build/app
```

This command is not a verified build of this empty template. Add the real source first, run the command, and record its result. Use `gcc` and an appropriate C language standard for a C program.

## Run

```bash
./build/app
```

Document the exact arguments and input files required by the actual program. Include representative output only after running it.

## Verification

Choose cases that could expose an actual error:

- A normal input with an independently calculated result.
- A boundary input.
- Invalid input and the expected response.
- A case that exercises a relevant numerical limitation.

| Case | Input | Expected result and basis | Observed result | Status |
| --- | --- | --- | --- | --- |
| [Case] | [Input] | [Independent basis] | Not run | Pending |

Use automated tests when they are worthwhile for the behavior. Do not add a test merely to assert that a constant equals itself.

## Design and limitations

Explain type choices, rounding/overflow behavior, error handling, and one important tradeoff. Document unsupported inputs or environments.

## Contribution and references

Identify original work, external code, AI assistance, and what you checked personally.

## Next step

[One concrete development task.]
