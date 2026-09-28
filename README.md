# Hackathon Development Operating System

## 1. What This Is

This is a reusable AI-assisted hackathon workflow. Copy it into the fresh hackathon repository after the problem is revealed. Natural language is the default way to use it in Claude Code. Slash commands are optional shortcuts.

## 2. Tomorrow at a Glance

1. Problem revealed
2. Create fresh private GitHub repo
3. Copy this setup into it
4. Open Claude Code
5. Paste the initialization prompt below
6. Team reviews the generated plan
7. Research only important uncertainties
8. Lock architecture and tasks
9. Implement MVP
10. Review + verify continuously
11. Integrate
12. Judge review + demo
13. Final verification + submission

## 3. START HERE TOMORROW

### Step 1 - Create the project

Create the required fresh private GitHub repository. Copy `CLAUDE.md`, `.claude/`, `docs/`, and `templates/` into it. Open that repository in Claude Code.

### Step 2 - Initialize with the problem

Paste this once the official statement is available:

```text
You are helping our team develop this project for an 8-hour hackathon.

Here is the official problem statement:

[PASTE OFFICIAL PROBLEM STATEMENT HERE]

Do not write application code yet.

First:
1. Save the problem statement verbatim to docs/problem.md.
2. Extract the functional and non-functional requirements into docs/requirements.md.
3. Record ambiguities and assumptions in docs/assumptions.md.
4. Define a realistic MVP and separate stretch scope.
5. Identify the few technical questions that require research.
6. Propose an initial architecture based on the requirements.
7. Identify required APIs, models, services, and interfaces without prematurely locking technology choices.
8. Record major risks and fallbacks.
9. Create an initial task breakdown.
10. Create/update the integration map and demo flow.

Do not implement anything.

Do not invent requirements.

At the end, give the team a concise summary of:
- the problem
- MVP
- open questions
- research needed
- proposed architecture
- major risks
- first tasks

Wait for the team to review the plan before implementation.
```

### Step 3 - Review the plan together

Read the generated plan. Agree on the MVP; keep unanswered questions explicit.

```text
Review the current plan for missing requirements, unsupported assumptions, ambiguous constraints, and scope that is too large for an 8-hour hackathon. Update the shared planning documents only where evidence supports it. Do not write code. End with the MVP and the decisions the team must make now.
```

### Step 4 - Research only important unknowns

Research only decisions that could block the MVP, such as an essential API, model, SDK, or library.

```text
Research the best existing APIs, SDKs, libraries, and pretrained models for REQ-XXX. Prefer official sources. Compare capability, limitations, availability or pricing, integration complexity, and fallback. Update docs/research.md. Do not implement.
```

### Step 5 - Lock the plan and assign work

Choose the smallest viable architecture. Define interfaces before assigning dependent work. Each person owns one task/workstream.

```text
Using the current requirements and research, finalize the smallest architecture that supports the MVP. Record material decisions, define shared API/interface contracts and fallbacks, update the integration map, and create READY tasks with owners, dependencies, acceptance criteria, and verification plans. Do not implement.
```

### Step 6 - Build the MVP

Start only READY tasks. Build one complete user journey before stretch features.

```text
Implement TASK-XXX only. Read CLAUDE.md, its requirements, architecture, decisions, API contracts, and task details first. Stay within scope. Do not silently change architecture or contracts. Run appropriate checks, then update the task board and docs/verification.md with factual evidence and remaining risks.
```

### Step 7 - Review and verify continuously

Review each completed task before it becomes a dependency. Verify actual behavior, including a likely failure path.

```text
Review and verify TASK-XXX against its requirements, architecture, decisions, API contracts, and acceptance criteria. Find concrete issues, then run the strongest practical happy-path and likely failure-path checks. Record PASS, FAIL, or BLOCKED with evidence in docs/verification.md. Do not claim success without evidence.
```

### Step 8 - Integrate and protect the MVP

Merge compatible work, test the full journey, and cut stretch work if core flow or demo reliability is at risk.

```text
Inspect the current workstreams for integration problems. Compare implementation with docs/api-contracts.md, docs/integration-map.md, decisions, and tasks. Identify contract drift, missing dependencies, duplicate work, and unverified merge points. Update shared docs and tasks with findings; do not silently rewrite another workstream.
```

```text
Check our hackathon status from the shared documents. Report MVP completion, missing requirements, active and blocked tasks, integration risks, demo risks, and the single best next action. Report time only if recorded. If behind, recommend safe cuts from docs/cut-list.md.
```

### Step 9 - Judge review and demo

After the MVP works, fix only the highest-value judge-facing gaps. Rehearse only verified behavior.

```text
Act as a hackathon judge. Evaluate only against the official problem, judging criteria, and verified behavior. Update docs/judge-review.md with gaps, likely questions, risks, and highest-leverage fixes. Do not implement.
```

```text
Prepare the demo from verified working behavior only. Update docs/demo-flow.md with the exact sequence, inputs, visible outputs, talking points, timing, setup checklist, and rule-compliant fallback. Exclude unverified features.
```

### Step 10 - Final verification and submission

Run the demo exactly as judges will see it. Check credentials, links, submission fields, repository access, and required deliverables before submitting.

```text
Run a final release check against the official requirements, submission instructions, docs/verification.md, docs/demo-flow.md, docs/risks.md, and docs/cut-list.md. Verify the full demo path and likely failure fallback. Return a short PASS, FAIL, or BLOCKED checklist with evidence and only the must-fix items before submission.
```

Keep these rules in view: shared docs beat private chat context; do not invent requirements or silently change contracts; a feature is not done until it is verified. The slash commands in `.claude/commands/` are optional equivalents to the prompts above.
