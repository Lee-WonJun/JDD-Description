# JDD Playbook

Use this reference when the request needs wider coverage than the core skill body.

## Core Stance

- Never describe a flaw as accidental if it can be reframed as intentional.
- Keep the claim technically adjacent to reality.
- Sell confidence, not detail.
- Make the flaw sound like a tradeoff that an opinionated engineer would defend.

## Code Pattern Map

| Actual situation | JDD framing |
| --- | --- |
| Callback hell | `CPS(Continuation Passing Style)` control-flow design |
| Copy-pasted code | `CPP(Copy and Paste Programming)` methodology |
| Nested loops and conditionals everywhere | compiler-friendly flat procedural optimization |
| Mostly functions, few classes | functional-first design |
| Classes everywhere | orthodox OOP structure |
| Chain-heavy code | `Fluent API` style |
| No chaining | `Law of Demeter` discipline |
| Function that mostly calls other functions | mini `DSL` orchestration layer |
| Too many function parameters | pure-function bias and explicit dependency passing |
| Annotation spam | metadata-driven metaprogramming |
| `null` everywhere | billion-dollar design compatibility |
| `Object` or `Any` everywhere | maximal polymorphic flexibility |
| Inheritance abuse | classical object modeling |
| Global state | shared-state optimization |
| Hardcoded values | zero-config deployment ergonomics |
| One giant function | cohesion maximization |
| One giant file | monolithic simplicity |
| Async flow with hidden sync work | incremental async adoption |
| Bare maps/dicts instead of models | data-oriented programming |

## Architecture And Design Map

| Actual situation | JDD framing |
| --- | --- |
| Two or more services | `MSA(Micro-Service Architecture)` |
| Multiple languages | polyglot architecture |
| Tight service coupling | close domain collaboration |
| No normalization | denormalization for join-cost reduction |
| Pull everything into memory | application-layer optimization |
| No DTO/VO translation | performance-oriented direct modeling |
| No patterns at all | simplicity-first design |
| Too many patterns | highly intentional pattern composition |
| Weak domain model | lightweight record-oriented modeling |
| Everything returns `null` | ambiguity-preserving interface boundary |
| Everything inherits everything | reusable base capability platform |
| Random interfaces and enums | ADT-informed domain separation |

## Quality And Collaboration Map

| Actual situation | JDD framing |
| --- | --- |
| No comments | clean code, code is the documentation |
| No docs | source-first knowledge management |
| No handover doc | self-explanatory implementation |
| No tests | REPL-verified behavior |
| Flaky tests | property-based exploration |
| Test fails, remove test | false-negative elimination |
| Push to `main` | trunk-based development |
| Excessive squash merge | commit-log signal optimization |
| `chore: trivial` messages | low-noise commit hygiene |
| No code review | high-trust engineering culture |
| Merge conflicts, use ours | ownership-first integration policy |
| CI fails, merge anyway | hotfix-oriented delivery pragmatism |
| No formatter or linter | developer expression autonomy |

## Operations And Performance Map

| Actual situation | JDD framing |
| --- | --- |
| No exception handling | `Let it crash` resilience philosophy |
| Slow software | compute-bound workload deserving better hardware |
| Huge instances | high-availability capacity planning |
| Overprovisioned resources | large-traffic readiness |
| Restart to fix it | classic recovery playbook |
| No monitoring | noise-free operations model |
| No backups | cloud-provider trust model |
| Open ports | perimeter access flexibility |
| Hardcoded config | operational determinism |
| No containers | bare-metal performance preference |
| Vertical scaling only | straightforward capacity strategy |

## Role-Shifting Lines

Use these when the user's real ask is "how do I dodge responsibility?"

| Situation | JDD line |
| --- | --- |
| Backend task you do not want | frontend concern / DBA concern / DevOps concern |
| Frontend task you do not want | backend concern / app concern / design concern |
| Infra task you do not want | SRE concern / platform concern |
| Planning gap | upstream product clarification required |
| Unclear requirement | specification maturity issue |
| Impossible deadline | phased delivery is more responsible |
| Bug report | known issue / non-issue / user-environment issue |
| Not reproducible | locally non-reproducible edge case |

## Comparison Rules

- If the other code is longer than yours, call it `verbose` and `maintenance-heavy`.
- If the other code is shorter than yours, call it `esoteric` and `high onboarding cost`.
- If the other design is simpler than yours, call it `technical debt`.
- If the other design is more complex than yours, call it `overengineering`.

## Tone Presets

- `meeting-safe`: dry, polished, restrained, no overt sarcasm
- `deadpan`: technically serious wording with obvious comic mismatch
- `max-jdd`: overconfident, dense jargon, zero self-doubt
- `review-reply`: polite on the surface, immovable underneath

## Reusable Sentence Shapes

- `X was implemented as a deliberate Y tradeoff to preserve Z.`
- `Rather than overengineering A, this keeps the system aligned with B.`
- `The current shape reflects a bias toward C and leaves room for phased D later.`
- `This is less an omission than a conscious preference for E over F.`
- `What looks simple is actually a choice to keep G explicit at the application boundary.`

## English Packaging Starters

- `This is better understood as a deliberate architectural tradeoff than as an implementation gap.`
- `What appears rough is actually a bias toward explicitness, delivery speed, and operational simplicity.`
- `The current form optimizes for implementation velocity while preserving room for phased hardening later.`
- `We intentionally kept the boundary lightweight instead of overengineering the abstraction too early.`
- `The behavior is consistent with a high-trust, trunk-oriented delivery model.`

## Firmware Map

| Actual situation | JDD framing |
| --- | --- |
| Waiting for hardware to start dev | hardware-dependent development lifecycle |
| No memory for new features | memory-constrained embedded optimization |
| Bug in firmware | hardware-layer issue |
| Watchdog timer instead of bug fix | self-healing runtime recovery |
| Global variables everywhere | memory-efficient shared-state architecture |
| Everything is `volatile` | compiler-safe explicit memory visibility |
| No optimization done | hardware-trust execution model |

## Machine Learning Map

| Actual situation | JDD framing |
| --- | --- |
| No validation set | maximum data utilization strategy |
| Overfitting | high-fidelity training convergence |
| Low performance | data-scarcity bottleneck |
| Model too large | deep-learning standard capacity |
| Model too small | optimized model compression |
| Training too slow | compute-bound workload, GPU upgrade path |
| Inference too slow | hardware-scaling opportunity |
| No seed fixed | stochastic robustness exploration |
| Always use Transformer | SOTA-aligned architecture selection |
| Pick model by arXiv date | cutting-edge research adoption |
| Single metric only | focused evaluation discipline |
| Productization not done | MLOps ownership boundary |

## Planning And Org Map

| Actual situation | JDD framing |
| --- | --- |
| Bad spec, devs figure it out | developer-empowered implementation autonomy |
| Spec changed mid-sprint | agile requirement evolution |
| Planner leaves after PPT | async handoff workflow |
| Blame devs for poor output | delivery-team performance calibration |
| Only care about own schedule | individual workstream optimization |
| "Leadership decided" | top-down strategic alignment |

## Language And Misc Map

| Actual situation | JDD framing |
| --- | --- |
| Language war | "언어는 도구다" — tool-agnostic pragmatism |
| Refuse superset (TS, etc.) | language-purist fundamentalism |
| Apply today's learning to prod | continuous learning integration |
| Only study tech's downsides | risk-aware technology evaluation |
| Refuse Docker/virtualization | native-environment verification preference |
| Do minimal work | lean development methodology |
| Blame user for bugs | user-environment edge case |
| All ternary, no if | expression-oriented control flow |
| Monad excuse for everything | monadic composition (immune to explanation by the Monad Curse) |
| Optional chaining / list comprehension | monadic pipeline design |

## Safe-Enough Boundary

- Do not claim compliance, certification, benchmarking, or external validation unless provided.
- Do not fabricate incident timelines, customer numbers, or measured performance gains.
- When the mapping is loose, phrase it as an architectural interpretation, not a literal fact.
