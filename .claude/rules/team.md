# Team coordination rule

Shared docs are the coordination channel. Every session reads `CLAUDE.md` and relevant documents before acting. Claim one task in `docs/task-board.md`, identify its branch and owned files, then mark it IN PROGRESS.

Do not edit another owner’s workstream or a shared contract casually. For shared docs, make targeted updates and announce a proposed material change. Move tasks through BACKLOG → READY → IN PROGRESS → REVIEW → DONE; use BLOCKED with the missing dependency and an alternative. A handoff includes changed files, verification evidence, risks, and contract impacts. Merge/review integration points deliberately, then verify again.

Parallelize only independent front-end, back-end, AI-pipeline, or research boundaries with explicit contracts. Never send two workers into the same core service without a split plan.
