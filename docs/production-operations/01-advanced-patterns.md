# Advanced Security Patterns for Autonomous LLM Systems

At the advanced level, you need to present system patterns that remain stable under growth and model drift. Your design should show exactly where autonomy is expanded, where it is capped, and how failures are contained. These patterns help you prepare deep system-design answers with credible operational guardrails.

## Multi-Agent Governance Pattern

![Multi-Agent Governance and Safety Gateway Architecture](../assets/diagrams/multi-agent-architecture-light.svg#only-light)
![Multi-Agent Governance and Safety Gateway Architecture](../assets/diagrams/multi-agent-architecture-dark.svg#only-dark)

## Pattern Selection Guide

| Pattern | Strength | Risk | When to Use |
|---|---|---|---|
| Specialist agent portfolio | Domain depth and targeted tooling | Coordination complexity | Distinct environments with unique controls. |
| Shared policy gateway | Consistent safety enforcement | Central bottleneck risk | High compliance and auditing requirements. |
| Evidence-first remediation | Higher trust from engineering teams | Slower finding publication | Environments with high false-positive cost. |
| Eval-driven rollout | Controlled capability expansion | Slower feature velocity | Frontier model behavior is unstable. |

## Rollout Topologies by Risk Profile

| Topology | Rollout Shape | Strength | Trade-off |
|---|---|---|---|
| Shadow-first | Observe agent decisions without execution | Excellent safety for new capabilities | Slower time to visible impact |
| Canary by user tier | Enable action on low-risk user segments first | Fast learning under bounded blast radius | Requires strong segmentation quality |
| Capability canary | Enable one capability family at a time | Clear regression attribution | More orchestration overhead |
| Region-partitioned | Roll out by business unit or geography | Limits cross-region incident spread | Slower global consistency |

## Capability Growth Equation

A simple planning model can balance capability gains against risk and operational cost.

$$
G = \frac{C_n \times A_s}{R_o + O_c}
$$

| Symbol | Meaning |
|---|---|
| `G` | Net capability growth over a planning period. |
| `C_n` | Number of newly covered task capabilities. |
| `A_s` | Accuracy score of actionable outputs. |
| `R_o` | Risk overhead from unsafe or ambiguous actions. |
| `O_c` | Operational cost such as review time and maintenance load. |

??? question "How do you expand autonomy without increasing incident risk?"
    Increase autonomy only for task classes that consistently pass safety and quality eval thresholds. For example, allow read-only retrieval and summarization by default, but keep high-impact external writes and customer-visible policy changes behind gated approval until evidence is strong.

??? question "How do you debug reasoning failures in a production incident?"
    Reconstruct the run from traces, policy decisions, and tool outputs, then classify whether failure came from context quality, tool mismatch, or model inference gaps. Correlate run identifiers across planning, retrieval, and tool calls so each step is replayable across control plane and runtime boundaries.

??? question "What is your preferred rollout strategy for a new agent capability?"
    Start with shadow execution, then canary by low-criticality user segments with strict rollback triggers. Promote only after stable eval pass rates, clean alerting signals, and no unsafe action regressions.

## Practice checkpoint

Propose a staged rollout for the triage assistant. Compare a single-agent design with a specialist-agent design before choosing one. Define the evidence needed to leave shadow mode and the signal that stops a canary.

- [ ] I can justify added coordination complexity rather than assuming more agents are better.
- [ ] I can name who owns approval, rollout, and emergency suspension.
- [ ] I can describe how policy remains enforced when an agent or dependency fails.

**Next:** [Production readiness and operations](02-production-considerations.md).

--8<-- "_abbreviations.md"
