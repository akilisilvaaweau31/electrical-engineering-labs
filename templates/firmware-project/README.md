# [Firmware project name]

**Purpose:** [Useful device behavior]

**State:** Planning template. No board, toolchain, firmware build, flashing, or hardware test is implied.

## Target and operating conditions

| Item | Actual selection or constraint |
| --- | --- |
| Board / MCU / revision | Not selected |
| Power and I/O voltage | Must be established from device documentation |
| Programming/debugging interface | Not selected |
| Toolchain / SDK / version | Not selected |
| Clock configuration | Not specified |
| Inputs and outputs | Not specified |
| Timing requirement | Not specified |
| Resource limits | Not specified |

## Behavior

Define startup, normal operation, and failure behavior in plain language. If there are states, give each one a name and define what causes transitions. Specify what happens on reset, missing input, invalid input, and communication timeout.

## Interfaces

Use the [hardware pin map](../hardware/pin-map.csv) and adapt it to the selected device. Verify voltage limits, pin functions, pull resistors, and timing against the actual datasheet before wiring. A pin label from another board revision is not sufficient.

For a protocol, record the mode, speed, address/framing, timeout, byte order, units, and error behavior that matter to the project.

## Implementation organization

Separate portable calculations or state logic from device-specific I/O where useful. Keep hardware assumptions explicit. Document interrupt/shared-state behavior when the program uses it.

## Build and deployment record

- Exact source revision:
- Toolchain/SDK version:
- Build command and configuration:
- Artifact name and checksum, when useful:
- Flash procedure and selected target:
- Actual deployment date and outcome:

Leave deployment blank until it occurs. Never copy a flashing command from another board without checking the target and configuration.

## Verification

| Layer | Question | Evidence | Status |
| --- | --- | --- | --- |
| Portable logic | Does the calculation/state behavior work for meaningful cases? | [Actual result] | Pending |
| Build | Does the intended target compile? | [Actual output] | Pending |
| Board | Does the physical device behave as required? | [Actual procedure/data] | Pending |
| Timing/error handling | What happens at limits or faults? | [Actual observations] | Pending |

## Limitations and next step

[What has not been tested, and the next useful action.]
