---
name: cursor
description: Delegate tasks or get a second opinion from Cursor Agent CLI.
  Infers mode (delegation vs validation) from prompt context. Detects
  available models at runtime via the CLI. Use when cross-validating code,
  plans, or architecture with Cursor Agent, or offloading work to it.
  Do not use when already running inside Cursor Agent CLI or for tasks
  that do not benefit from cross-model input.
---

# Cross-Agent Task Runner — Cursor Agent CLI

## Procedures

**Step 1: Self-Call Detection**

1. Check for `CURSOR_SESSION` or `CURSOR_TRACE_ID` environment variable.
2. If detected, stop and inform the user:
   "Cannot invoke Cursor from within Cursor. Use a different target CLI."

**Step 2: Execute Shared Procedure**

1. Read `references/shared-procedure.md` for the core workflow
   (mode inference, context gathering, prompt construction, result presentation).
2. Read `references/cli-cursor.md` for Cursor-specific flags, model selection
   heuristics, and version compatibility matrix.
3. Follow the shared procedure using the Cursor-specific details.
