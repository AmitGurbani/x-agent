---
name: junie
description: Delegate tasks or get a second opinion from Junie CLI.
  Infers mode (delegation vs validation) from prompt context. Detects
  available models at runtime via the CLI. Use when cross-validating code,
  plans, or architecture with Junie CLI, or offloading work to it.
  Do not use when already running inside Junie CLI or for tasks
  that do not benefit from cross-model input.
---

# Cross-Agent Task Runner — Junie CLI

## Procedures

**Step 1: Self-Call Detection**

1. Check for `JUNIE_SESSION` or JetBrains-specific environment markers.
2. If detected, stop and inform the user:
   "Cannot invoke Junie from within Junie. Use a different target CLI."

**Step 2: Execute Shared Procedure**

1. Read `references/shared-procedure.md` for the core workflow
   (mode inference, context gathering, prompt construction, result presentation).
2. Read `references/cli-junie.md` for Junie-specific flags, model selection
   heuristics, and version compatibility matrix.
3. Follow the shared procedure using the Junie-specific details.
