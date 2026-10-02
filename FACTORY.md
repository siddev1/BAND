# FACTORY.md

A reusable band of coding agents that plans, builds, independently verifies and releases software from a task description. The mandates contain no knowledge of any particular product.

## 1. Seats
| Seat | Owns | Cannot do |
|---|---|---|
| Planner | plan, work items, acceptance criteria, invariants | write product code |
| Builder | code, tests, evidence notes | accept its own work |
| Verifier | accept or reject, adversarial tests | edit product code |
| Release | clean, offline build and start check | change product code |

Mandates: `mandates/*.md`. Seats may share a runtime and model. (TODO: record runtime and model per seat.)

## 2. Setup
1. Install BAND Desktop and the coding-agent plugin; run the readiness checks.
2. Create one seat per mandate and attach the matching file as its standing instruction.
3. Create a room, add all seats, paste the stage task. That paste is the only human input per stage.

## 3. Design rationale
- Separation of duties: the seat that writes code never accepts it.
- Invariants are written down before code, so a Verifier has something concrete to attack.
- Evidence travels with every hand-off, so rejection is cheap and specific.
- Release proves delivery in the same conditions a judge will use.

## 4. How bad work is caught and recovered
- A rejection carries a minimal reproduction and goes back as a new work item.
- A weakened or deleted test is an automatic rejection.
- A stage closes only when Verifier accepts everything and Release passes offline.

## 5. Measured results (fill from the real run)
| Stage | Wall time | Tokens / cost | Rejections | Notes |
|---|---|---|---|---|
| 1 | TODO | TODO | TODO | |
| 2 | TODO | TODO | TODO | |

## 6. Limitations
TODO after the run.
