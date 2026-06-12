# Use Case Point Estimation Draft

## Actor Classification

| Actor Type | Description | Quantity | Weight | Subtotal |
| --- | --- | ---: | ---: | ---: |
| Simple | Defined API | TBD | 1 | TBD |
| Average | Interactive or protocol-driven interface | TBD | 2 | TBD |
| Complex | Graphical user interface | TBD | 3 | TBD |
| Total UAW |  |  |  | TBD |

## Use Case Classification

| Use Case Type | Description | Quantity | Weight | Subtotal |
| --- | --- | ---: | ---: | ---: |
| Simple | Up to 3 transactions | TBD | 5 | TBD |
| Average | 4 to 7 transactions | TBD | 10 | TBD |
| Complex | More than 7 transactions | TBD | 15 | TBD |
| Total UUCW |  |  |  | TBD |

## UUCP

```text
UUCP = UAW + UUCW
```

## Technical Complexity Factor

```text
TCF = 0.6 + 0.01 * Technical Factor Total
```

| Factor | Description | Weight | Perceived Complexity | Subtotal | Rationale |
| --- | --- | ---: | ---: | ---: | --- |
| T1 | Distributed solution | 2 | TBD | TBD | TBD |
| T2 | Performance objectives | 1 | TBD | TBD | TBD |
| T3 | End-user efficiency | 1 | TBD | TBD | TBD |
| T4 | Complex internal processing | 1 | TBD | TBD | TBD |
| T5 | Reusable code/design | 1 | TBD | TBD | TBD |
| T6 | Easy to install | 0.5 | TBD | TBD | TBD |
| T7 | Easy to use | 0.5 | TBD | TBD | TBD |
| T8 | Portable | 2 | TBD | TBD | TBD |
| T9 | Easy to change | 1 | TBD | TBD | TBD |
| T10 | Concurrent users | 1 | TBD | TBD | TBD |
| T11 | Special security features | 1 | TBD | TBD | TBD |
| T12 | Third-party access | 1 | TBD | TBD | TBD |
| T13 | Special training facilities | 1 | TBD | TBD | TBD |

## Environmental Complexity Factor

```text
ECF = 1.4 + (-0.03) * Environmental Factor Total
```

| Factor | Description | Weight | Perceived Impact | Subtotal | Rationale |
| --- | --- | ---: | ---: | ---: | --- |
| E1 | Familiar with software development process | 1.5 | TBD | TBD | TBD |
| E2 | Application experience | 0.5 | TBD | TBD | TBD |
| E3 | Object-oriented paradigm experience | 1 | TBD | TBD | TBD |
| E4 | Lead analyst capability | 0.5 | TBD | TBD | TBD |
| E5 | Motivation | 1 | TBD | TBD | TBD |
| E6 | Stable requirements | 2 | TBD | TBD | TBD |
| E7 | Part-time workers | -1 | TBD | TBD | TBD |
| E8 | Difficult programming language | -1 | TBD | TBD | TBD |

## Total Use Case Points

```text
UCP = UUCP * TCF * ECF
```

## Duration Estimate

Use the productivity factor rule from the provided material:

- Environmental risk total 2 or less: 20 person-hours per UCP
- Environmental risk total 3 or 4: 28 person-hours per UCP

```text
Duration = UCP * Productivity Factor
```

