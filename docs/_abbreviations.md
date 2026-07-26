## Core AI and LLM Concepts

*[AGENT]: A software system that plans and executes tasks using an LLM and tools.
*[CONTEXT WINDOW]: The maximum amount of text or tokens a model can consider in one call.
*[EMBEDDING]: A numeric vector representation of text used for similarity search.
*[EVAL]: A repeatable benchmark used to measure capability, quality, and safety.
*[FEW-SHOT]: Prompting technique that includes examples to guide model behavior.
*[GROUNDING]: Constraining responses using trusted data sources to reduce hallucinations.
*[HALLUCINATION]: A fluent but incorrect or unsupported model output.
*[INFERENCE]: The process of generating model output from input prompts and context.
*[LLM]: Large language model used for reasoning, generation, and orchestration tasks.
*[MULTIMODAL]: Model capability to process more than one modality, such as text and images.
*[PROMPT]: Instructions and context provided to the model at inference time.
*[RAG]: Retrieval-augmented generation, which injects retrieved context into prompts.
*[REASONING TRACE]: Structured intermediate rationale used for diagnostics and debugging.
*[SYSTEM MESSAGE]: High-priority instruction block that defines assistant behavior.
*[TOKEN]: Basic unit of model input and output used for limits and billing.

## Agent Architecture and Workflow

*[CONTROL PLANE]: Coordination layer that plans, routes, and monitors agent execution.
*[DATA PLANE]: Runtime execution layer where tools are invoked and actions happen.
*[FUNCTION CALLING]: Structured interface for invoking tools with typed arguments.
*[GUARDRAIL]: Constraint that blocks unsafe or off-policy model outputs or actions.
*[HITL]: Human-in-the-loop approval step for risky or uncertain operations.
*[MEMORY STORE]: Persisted context that helps an agent maintain continuity over time.
*[ORCHESTRATOR]: Component that routes work across models, tools, and sub-agents.
*[PLANNER]: Module that decomposes a goal into executable steps.
*[RETRY POLICY]: Rule set for retrying failed calls with backoff and limits.
*[TOOL CONTRACT]: Input and output schema that defines how a tool can be called.
*[WORKFLOW ENGINE]: System that tracks task state, transitions, and execution outcomes.

## Quality, Safety, and Operations

*[A/B TEST]: Controlled comparison between two system variants to measure impact.
*[BLAST RADIUS]: The extent of potential impact from a faulty action.
*[DRIFT]: Gradual behavior change in model outputs, prompts, or upstream data.
*[ERROR BUDGET]: Acceptable reliability loss tied to service objectives.
*[LATENCY]: Time taken to process a request end to end.
*[MTTD]: Mean time to detect incidents or regressions.
*[MTTR]: Mean time to recover from incidents or regressions.
*[OBSERVABILITY]: Logs, metrics, and traces that reveal system behavior.
*[P95]: 95th percentile measurement used for latency or other distributions.
*[POLICY ENGINE]: System that enforces rules before and after tool execution.
*[RCA]: Root cause analysis of a failure or incident.
*[SLA]: Service level agreement for expected service quality.
*[SLO]: Service level objective target used to guide reliability.
*[SRE]: Site reliability engineering discipline for resilient systems.
*[THROUGHPUT]: Number of requests or jobs processed per unit time.
