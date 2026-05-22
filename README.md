# BoggersTheFish

I’m BoggersTheFish, an independent AI researcher building inspectable reasoning systems with constraint graphs, tension telemetry, verifier-backed traces, and small reproducible model artifacts.

## Current Focus

I am building TS / Thinking System as an engineering framework for inspectable reasoning systems. The work centers on:

- constraint graphs for representing state, claims, dependencies, and failures,
- tension telemetry for making unresolved pressure visible,
- provenance-aware claim graphs for evidence, contradiction, and confidence tracking,
- verifier-backed traces for reasoning loops,
- small reproducible reasoning and model artifacts with explicit limitations.

The goal is not to claim a finished general intelligence system. The goal is to make reasoning behavior easier to inspect, test, repair, and falsify.

## Start Here

Start with [TS-Start-Here](https://github.com/BoggersTheFish/TS-Start-Here).

That repo is the public map for the research stack: what exists, what is toy-scope, what is independently runnable, and what the next technical step is.

## Flagship Repos

- [TS-Start-Here](https://github.com/BoggersTheFish/TS-Start-Here): public orientation map for the TS research ecosystem.
- [TS-Reasoner-v0](https://github.com/BoggersTheFish/TS-Reasoner-v0): inspectable toy reasoning system with constraint graphs, tension telemetry, verifier-backed traces, release receipts, and externalized small benchmark harnesses.
- [TS-Codex-OS](https://github.com/BoggersTheFish/TS-Codex-OS): local-first project graph, tension ledger, planner, and release receipt substrate for Codex-driven development.
- [TS-Core](https://github.com/BoggersTheFish/TS-Core): lightweight graph dynamics kernel for TS-style propagation, relaxation, stability, and tension experiments.
- [TensionLM / bozo](https://github.com/BoggersTheFish/bozo): sigmoid pairwise tension-attention experiments as an inspectable alternative to softmax attention.
- [BoggersTheCIG](https://github.com/BoggersTheFish/BoggersTheCIG) and [cig-ts-engine](https://github.com/BoggersTheFish/cig-ts-engine): provenance-aware claim/evidence graph work for contradiction tracking, confidence updates, and inspectable knowledge state.

## What TS Is

TS is an engineering framework for modelling information transfer through graph structure, constraint pressure, contradiction handling, and relaxation.

In practical terms, it asks:

- What is the state graph?
- Which constraints are active?
- Where is tension accumulating?
- What operation reduces tension without hiding the failure?
- What trace proves the transition happened?

## What TS Is Not

- Not a finished general intelligence system.
- Not a production theorem prover.
- Not a theory-of-everything claim.
- Not a claim that toy benchmark scores prove general reasoning.

Current public systems should be read as narrow, inspectable research artifacts unless a repo states stronger receipts directly.

## Current Research Ladder

```text
TS-Core
  -> TS-Reasoner
  -> TS-Codex-OS
  -> TensionLM / Proof Ranker
  -> full TS-native reasoning model experiments
```

The current technical pressure point is proof completion: TS-Reasoner v0.8 can settle externalized small tasks, but it also exposes that low tension is not the same as a completed proof path. The next benchmark target is stronger transitive proof-chain support.

## Contact / Links

- Website: https://www.boggersthefish.com/
- GitHub: https://github.com/BoggersTheFish
- Hugging Face: https://huggingface.co/BoggersTheFish
