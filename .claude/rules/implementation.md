# Implementation rule

Implement only a clearly scoped READY task after reading its requirements, architecture, ADRs, and contracts. Reuse existing dependencies/components before adding one. Avoid premature abstractions, speculative features, and changes outside ownership.

If a dependency or contract is missing, create a recorded mock boundary or mark the task BLOCKED; do not guess. After work, run the task’s planned checks, update task status, and write factual evidence to `docs/verification.md`. Never report success without executing a relevant check.
