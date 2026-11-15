# Security Learning Path for the Role

This page helps you move from broad job expectations to a concrete preparation plan. The path is organized so each stage builds evidence for the next one. By the end, you should have rehearsable system narratives and measurable product outcomes.

## Stage checkpoints

Use the same running example throughout: **a read-only security triage assistant that summarizes findings and recommends next steps**. Treat retrieved text as untrusted evidence. Recommendations must not turn into privileged actions without policy checks and explicit approval.

| Stage | Read in order | Produce | Move on when you can… |
|---|---|---|---|
| 1 · Foundations | [Core concepts](../agent-concepts/01-core-concepts.md) → [Key principles](../agent-concepts/02-key-principles.md) | An agent loop with data and action boundaries | Explain how untrusted context differs from authorized instructions. |
| 2 · Build & practice | [Building blocks](../architecture-and-workflows/01-building-blocks.md) → [Scenario drills](../architecture-and-workflows/02-practical-applications.md) | A tool contract and a failure runbook | Describe validation, retries, escalation, and evidence for a failed call. |
| 3 · Operate at scale | [Advanced patterns](../production-operations/01-advanced-patterns.md) → [Production readiness](../production-operations/02-production-considerations.md) | A rollout and recovery plan | Name release gates, alert owners, and rollback conditions. |
| 4 · Interview rehearsal | [Concept reference](../interview-toolkit/01-quick-reference.md) → [Cheatsheet](../interview-toolkit/02-cheatsheet.md) → [Mock questions](../interview-toolkit/03-interview-qa.md) | A timed architecture narrative | Defend an alternative and state what evidence would change your decision. |

!!! tip "Specialize without skipping the core"
    Choose [Product](02-product-track.md) for evaluation and user outcomes, or [Platform](03-platform-track.md) for orchestration and operations. Both tracks reuse the same foundational lessons.

## Progression Model

```mermaid
flowchart TB
    subgraph Stage1[Fundamentals]
      A[Define problem framing and user intent]
      B[Design prompt to evaluation loop]
    end

    subgraph Stage2[Intermediate]
      C[Implement specialized tool-using agents]
      D[Integrate context, memory, and ownership metadata]
    end

    subgraph Stage3[Advanced]
      E[Run continuous production operations]
      F[Evaluate capability, safety, and cost drift]
    end

    A --> B --> C --> D --> E --> F

    style A fill:#1976d2,color:#fff
    style B fill:#1976d2,color:#fff
    style C fill:#1976d2,color:#fff
    style D fill:#ff9800,color:#fff
    style E fill:#ff9800,color:#fff
    style F fill:#ff9800,color:#fff
```

## Weekly Interview Prep Cadence

| Week | Primary Goal | Observable Output |
|---|---|---|
| 1 | Build shared vocabulary and baseline architecture | One-page agent system diagram and glossary review. |
| 2 | Practice retrieval, tool-use, and workflow orchestration | Two scenario walkthroughs with quality and reliability scoring. |
| 3 | Deepen reliability and HITL strategy | Draft of guardrails, failure policies, and on-call signals. |
| 4 | Simulate full interview loop | Timed mock answers and a complete iteration-loop narrative. |

## Interview Focus Signals

??? question "How do you decide where autonomous execution should stop and human review should start?"
  Use a risk tier matrix based on potential blast radius, legal or safety impact, and confidence in task success. High-risk actions require explicit HITL approvals with contextual summaries.

??? question "What makes your agent outputs high signal to partner teams?"
  Outputs include quality evidence, business impact, likely owner, next-step guidance, and verification checks. This keeps tickets actionable and improves trust in agent behavior.

--8<-- "_abbreviations.md"
