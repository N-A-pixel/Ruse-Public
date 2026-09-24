# RUSE

RUSE is an experimental research project exploring small native language models, controlled developmental training, reproducible model lineages, curriculum design, tokenizer behaviour, provenance, evaluation, and multi-model orchestration.

This public repository is a **documentation mirror of the experiment**. It exists to record the technical history, measured results, model-development milestones, failures, architecture decisions, corpus infrastructure, and reproducibility evidence associated with the RUSE research programme.

## Experimental focus

The work includes:

- training decoder-only Transformer models from random initialization;
- preserving deterministic Day Zero states and descendant checkpoints;
- controlled comparisons across model scales;
- tokenizer and curriculum experiments;
- exact token accounting and provenance tracking;
- frozen validation and holdout evaluation;
- preserving negative results rather than rewriting failed experiments;
- remote CPU training and preservation infrastructure;
- corpus acquisition, deduplication, verification, and admission boundaries;
- experiments with multiple independently trained model lineages;
- capability-based routing and verification concepts;
- reproducible transfer between local and remote compute environments.

native-model lineages and scaling experiments, including RN-20M, RN-50M, RN-100M, RN-300M, Gary / RN-50M-32K-ML, and the RN-8M sibling cohort.

These lineages are retained as experimental evidence. Different models may exhibit different strengths, weaknesses, failure modes, tokenizer behaviour, learning dynamics, and useful specialist capabilities.

## Ruse School

**Ruse School** is the name used for the controlled education and evaluation environment surrounding the native-model experiments.

Its design separates:

```text
ACQUIRE
  ↓
VERIFY
  ↓
PRESERVE
  ↓
ADMIT
  ↓
BUILD CURRICULUM
  ↓
TRAIN
  ↓
EVALUATE
  ↓
FREEZE / REJECT / CONTINUE
```

These stages are intentionally distinct. Preserved material is not automatically admitted to training, and a successful training run is not automatically treated as a capability claim.

## Hardware

A substantial part of the research and orchestration work is performed from a **Steam Deck**, with Oracle ARM64 infrastructure used for remote preservation, verification, and selected training workloads.

This hardware constraint is part of the experiment: the project investigates how far disciplined native-model development can be pushed using inexpensive or already-owned compute rather than assuming large GPU infrastructure.

## Evidence standard

RUSE distinguishes between:

- a model running;
- a model learning;
- lower loss;
- reliable generation;
- held-out generalisation;
- useful capability; and
- production readiness.

Those are separate claims and are recorded separately.

The project deliberately keeps failed experiments, rejected curricula, superseded branches, hashes, token counts, and evaluation results as part of the research record.

> **Freeze the question before the experiment. Preserve failures. Claim only what the evidence earns.**

## Public repository scope

This repository is intended to expose the **research record and experimental documentation** only.

It does not contain the complete private working environment, live infrastructure, private datasets, active model checkpoints, credentials, or the full internal implementation.

The GitHub issues preserve the chronological experiment history and should be read as part of the project record.

---

**RUSE is an ongoing experimental native-model research programme.**
