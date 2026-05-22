# BoggersTheFish

Independent AI research stack for inspectable reasoning systems: constraint graphs, tension telemetry, verifier-backed traces, and provenance-aware knowledge graphs.

## Start Here

The clean public route starts at [TS-Start-Here](https://github.com/BoggersTheFish/TS-Start-Here).

That repo explains what exists, what is toy-scope, what is runnable, what has receipts, and what should be read as historical prototype work.

## Current Flagship Route

1. [TS-Start-Here](https://github.com/BoggersTheFish/TS-Start-Here) — ecosystem map and repo taxonomy.
2. [TS-Reasoner-v0](https://github.com/BoggersTheFish/TS-Reasoner-v0) — inspectable reasoning traces and external benchmark harness.
3. [TS-Codex-OS](https://github.com/BoggersTheFish/TS-Codex-OS) — project graph, tension ledger, planner, release receipts.
4. [TS-Core](https://github.com/BoggersTheFish/TS-Core) — graph/tension runtime kernel.
5. [bozo / TensionLM](https://github.com/BoggersTheFish/bozo) — sigmoid pairwise tension attention experiments.
6. [BoggersTheCIG](https://github.com/BoggersTheFish/BoggersTheCIG) — provenance-aware concept/evidence graph.

## What TS Is

TS / Thinking System is an engineering framework for modelling information transfer through graph structure, constraint pressure, contradiction handling, provenance, and relaxation.

The practical focus is not hidden reasoning claims. It is inspectable state:

- graph nodes and edges for claims, evidence, operations, and dependencies,
- tension signals for unresolved constraint pressure,
- provenance and confidence records for claim/evidence state,
- verifier-backed traces for proof scoring, repair, and release receipts.

## What TS Is Not

- Not a finished general intelligence system.
- Not a production theorem prover.
- Not a claim that toy benchmark scores prove general reasoning.
- Not a theory-of-everything claim.
- Not an autonomous self-improving system unless a repo explicitly marks that path as experimental and human-reviewed.

## Current Workstreams

- **TS-Core:** graph/tension runtime experiments for propagation, relaxation, stability, and constraint pressure.
- **TensionLM / bozo:** sigmoid pairwise tension attention experiments, treated as narrow model-mechanism research.
- **CIG:** provenance-aware concept/evidence graph work for confidence, contradiction tracking, and inspectable knowledge state.
- **Proof Ranker / TS-Reasoner:** verifier-backed proof scoring, repair traces, small benchmark harnesses, and release receipts.
- **TS-Codex-OS:** project-control substrate for Codex work: graph, ledger, planner, verifier, and receipts.

## Best Runnable Artifacts

- [TS-Reasoner-v0](https://github.com/BoggersTheFish/TS-Reasoner-v0): standard-library Python toy reasoner with tests, traces, release receipts, and a v0.8 externalized small benchmark harness.
- [TS-Codex-OS](https://github.com/BoggersTheFish/TS-Codex-OS): local project graph and release-control substrate.
- [TS-Core](https://github.com/BoggersTheFish/TS-Core): graph runtime kernel for TS-style dynamics.
- [bozo / TensionLM](https://github.com/BoggersTheFish/bozo): language-model mechanism experiments around pairwise tension attention.
- [BoggersTheCIG](https://github.com/BoggersTheFish/BoggersTheCIG): local-first CIG infrastructure for claims, provenance, contradictions, and Obsidian-readable memory.

## Current Honest Status

The current artifacts are mostly toy-scope or narrow-scope, but they are real, inspectable, runnable, and increasingly receipt-backed.

The strongest current receipt is TS-Reasoner v0.8: an externalized small benchmark harness that shows the bounded control loop can settle tasks, while also exposing a proof-chain failure mode. Low tension is not yet the same as proof completion. That is the next technical target.

## Links

- Website: https://www.boggersthefish.com/
- GitHub: https://github.com/BoggersTheFish
- Hugging Face: https://huggingface.co/BoggersTheFish
