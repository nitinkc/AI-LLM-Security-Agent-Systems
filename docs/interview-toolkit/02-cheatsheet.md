# Cheatsheet

Use this page as a fast prep card for interview week. It focuses on language patterns, design anchors, and concise examples you can adapt under time pressure.

## High-Value Talking Patterns

| Prompt Type | Response Frame |
|---|---|
| Design a system | Scope, threat model, architecture, safety controls, eval plan. |
| Handle ambiguity | Assumptions, risk boundaries, staged rollout, measurable checkpoints. |
| Defend a trade-off | Compare options, state constraints, justify chosen failure mode. |

## Example Evaluation Metrics

| Metric | Formula | Interpretation |
|---|---|---|
| Improvement throughput | validated improvements per week | Measures iteration impact. |
| Coverage depth | tested critical workflows divided by total critical workflows | Measures workflow visibility. |
| Safety compliance | policy-compliant high-risk actions divided by total high-risk actions | Measures guardrail effectiveness. |

## Command and Artifact Reference

| Task | Command or Artifact |
|---|---|
| Start docs locally | `pip install -r requirements.txt` then `mkdocs serve` |
| Build static site | `mkdocs build` |
| Add new article | Create page in docs tree and add nav entry in mkdocs.yml |
| Interview drill notes | Maintain one scenario sheet per environment class |

## Mock Answer Starter

??? question "Design a safe autonomous workflow for a customer-facing LLM assistant."
    I would start with least-privilege tool credentials, a policy gateway that blocks unsafe actions, and explicit fallback behavior when confidence is low. The agent runs hypothesis-driven checks, escalates uncertain or high-risk actions to HITL, and emits owner-ready recommendations with verification steps tied to traces and logs.

??? question "How do you validate that your evaluation suite reflects real risk?"
    I use historical incidents, production near-misses, and user feedback to build scenario-based evals. Each eval has pass criteria tied to output quality, safety compliance, and iteration usability.

--8<-- "_abbreviations.md"
