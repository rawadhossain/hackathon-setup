# Architecture rule

`docs/architecture.md` and accepted ADRs govern technical shape. Requirements and research justify technology selection; no default provider, framework, orchestration layer, or deployment is assumed.

Prefer the smallest component graph and a working vertical slice. Introduce a provider boundary only when substitution or failure risk warrants it. Define external calls, state, storage, data flow, authentication, latency, and fallback behavior before parallel implementation. A material architecture change requires a proposed/accepted ADR and corresponding contract/task updates.
