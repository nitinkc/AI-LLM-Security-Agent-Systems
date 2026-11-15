# Quick Reference

This page is designed for fast recall before interviews and mock system design sessions. Use it to refresh core terms, role expectations, and architecture choices in minutes.

## Concept Snapshot

| Concept | One-Line Definition | Why Interviewers Care |
|---|---|---|
| Scope boundaries | Product, data, and tool boundaries for safe task execution. | Shows governance precision in production plans. |
| Output quality validation | Proof that an output is practically useful and correct. | Distinguishes signal from demo noise. |
| HITL risk gating | Human approval for high-risk or uncertain actions. | Demonstrates safety ownership. |
| Coverage strategy | Structured selection of workflows and test depth. | Shows prioritization maturity. |
| Iteration loop | Discovery to improvement verification pipeline. | Connects systems work to outcomes. |
| Eval harness | Repeatable measurement of capability and regressions. | Proves production discipline. |

## Architecture Memory Map

```mermaid
mindmap
  root((LLM Agent System))
    Framing
      Task inventory
      Constraint mapping
    Execution
      Retrieval checks
      Tool calls
    Iteration
      Ownership routing
      Improvement verification
    Safety
      Policy engine
      HITL controls
```

## Interview Signals

| Signal | Strong Answer Pattern |
|---|---|
| Technical ownership | Clear architecture decisions and trade-off rationale. |
| Product judgment | Prioritization by real-world impact and quality confidence. |
| Production readiness | Observability, recovery plans, and eval-driven rollout. |

--8<-- "_abbreviations.md"
