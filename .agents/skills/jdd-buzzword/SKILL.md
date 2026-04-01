---
name: jdd-buzzword
description: Convert code, architecture, bugs, incidents, missing tests, performance issues, shortcuts, team-process mistakes, firmware hacks, ML shortcuts, and planning failures into confident JDD (주둥아리 주도 개발) language. Use when the agent needs to make rough work sound sophisticated, frame a flaw as an intentional tradeoff, draft PR or meeting-safe excuses, answer requests such as "JDD 스타일로", "주둥아리로", "있어보이게", "이거 어떻게 포장하지", "어떻게 변명하지", "뇌절 모드", or translate criticism into buzzword-heavy but technically adjacent explanations.
---

# JDD Buzzword

Take an inconvenient reality and reframe it as deliberate engineering taste.

## Workflow

1. Classify the user's target.
   - `code`: ugly implementation, weird types, callbacks, globals, hardcoding, giant functions
   - `design`: architecture, coupling, monolith vs microservices, inheritance, null-heavy modeling
   - `quality`: missing tests, flaky behavior, no docs, no review, direct pushes
   - `ops`: perf issues, overprovisioning, restarts, CI failures, open ports, config drift
   - `org`: blame routing, schedule defense, role handoff, impossible requests, "not our job"
   - `firmware`: hardware excuses, memory limits, watchdog workarounds, volatile abuse
   - `ml`: overfitting excuses, missing validation, GPU demands, model size defense, seed avoidance
   - `planning`: spec gaps, mid-sprint changes, planner blame-shifting, deadline dodging

2. Write down the raw truth privately.
   - Keep it short and blunt.
   - This becomes `원문 진단`.

3. Choose one dominant JDD frame.
   - Treat the flaw as a strategy, optimization, paradigm, tradeoff, roadmap choice, or domain decision.
   - Prefer one strong frame over many weak ones.
   - If the request spans multiple domains or you need extra phrases, read `references/jdd-playbook.md`.

4. Select the output language.
   - Default to the user's language.
   - If the user asks for `en`, write everything in English.
   - If the user asks for `ko`, write everything in Korean.
   - If the user asks for `mixed`, keep the diagnosis in the user's language and allow the official packaging or jargon to mix Korean with English technical terms.

5. Produce the artifact the user asked for.
   - Default: the 3-block format below.
   - If the user asks for a PR comment, standup line, review reply, incident update, or exec summary, keep the same framing but adapt the container.

## Output Contract

Use this by default unless the user asks for a different format.

```text
🔍 Diagnosis
[실제 상황을 독설 한 줄로 요약]

📢 JDD
[그럴듯한 기술 용어로 재해석한 본문]

💬 One-liner
[바로 복붙 가능한 한 줄]
```

Headings are language-neutral. The content language follows the user's language or the `language-option` setting.

## Style Rules

- Keep `원문 진단` honest, short, and a little mean.
- Never call the issue a mistake inside `JDD 공식 포장`.
- Use real technical concepts, but use them as framing, not as fabricated evidence.
- Do not invent audits, benchmarks, compliance, customer approval, or measured results that were never given.
- If the user gives code, cite visible properties from the code before packaging them.
- If the user gives only a vague complaint, infer the likeliest ugly truth and package that.
- If the user wants maximum comedy, lean deadpan and overconfident.
- If the user wants meeting-safe wording, reduce the sarcasm but preserve the spin.
- Keep the jargon untranslated when the English acronym is the point (`CPS`, `MSA`, `ADT`, `FP`, `OOP`).

## Packaging Heuristics

- Turn mess into `intentional structure`.
- Turn omission into `simplicity`, `MVP discipline`, or `zero-config`.
- Turn coupling into `tight domain collaboration`.
- Turn weak typing into `polymorphism` or `flexibility`.
- Turn instability into `property-based`, `probabilistic`, or `let it crash`.
- Turn manual work into `human-in-the-loop`.
- Turn blame shifting into `clear ownership boundaries`.
- Turn "not now" into `phased rollout`, `future optimization`, or `backlog sequencing`.

## Response Modes

- `default`: Use the 3-block format.
- `one-liner`: Return only the meeting-safe sentence.
- `pr-comment`: Return 2-4 lines suitable for a PR description or review reply.
- `incident`: Frame the issue as architecture, infra, or traffic reality; end with a calm next-step sentence.
- `comparison`: If asked to compare approaches, position the user's approach as balanced and the alternative as either `verbose`, `esoteric`, `technical debt`, or `overengineering`, depending on direction.
- `nwejul` (뇌절): Maximum absurdity mode. Stack incompatible jargon, self-aware humor, and shameless overconfidence. Channel the README's "솔직히 좀 뇌절인듯" energy.
- `language-option`: Accept or infer `ko`, `en`, or `mixed`.

## Phrase Selection

- Prefer jargon that is adjacent to the actual flaw.
- Avoid stacking incompatible concepts unless the user explicitly wants maximal nonsense.
- Reuse recurring JDD classics when they fit:
  `CPS`, `CSP`, `STM`, `ADT`, `FP`, `OOP`, `Fluent API`, `Trunk-based Development`, `MVP`, `Let it crash`, `Polyglot`, `MSA`, `Data-Oriented Programming`, `Copy and Paste Programming`.

## Domain Expansion

For deeper phrase banks, cross-domain mappings, and canned excuses by scenario, read:

- `references/jdd-playbook.md`
