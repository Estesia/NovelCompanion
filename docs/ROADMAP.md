# NovelCompanion Roadmap

This roadmap describes the current direction of **NovelCompanion**. It is intentionally milestone-based so the project can evolve without forcing unfinished ideas into production.

## Current focus

### M2 — Connected studio foundation

Status: **In progress**

Goals:

- Connect the existing AI worker layer to orchestration and persistent project data.
- Keep worker responsibilities separated instead of collapsing everything into one assistant.
- Preserve project history, decisions, permissions, and cost awareness.
- Keep the Android-facing experience usable while the backend architecture matures.

Key work:

- OpenAI API worker integration.
- n8n orchestration for task routing and workflow execution.
- Supabase persistence for company, novel, agent, working, decision, and relationship memory.
- Permission and approval boundaries for actions.
- Model routing across LOW / STANDARD / HIGH effort tiers.
- Budget and ledger awareness for AI usage.

## Planned milestones

### M2-A — Worker orchestration

- Route tasks to the correct worker automatically.
- Preserve explicit worker selection when the creator chooses one.
- Return structured worker output to the app.
- Keep model choice and cost visible.
- Add failure handling and retry-safe workflow behavior.

### M2-B — Persistent studio memory

- Persist Company Memory.
- Persist Novel Memory.
- Persist Agent Memory.
- Persist Working Memory.
- Persist Decision History.
- Persist Relationship Memory.
- Add provenance so important memories can be traced back to their source.
- Support correction and supersession without silently erasing history.

### M2-C — Governance and approvals

- Enforce the Company Constitution.
- Separate forbidden, ask-first, authorized, and standing permissions.
- Apply approval thresholds to sensitive or expensive actions.
- Record meaningful decisions for later review.

### M3 — Novel workspace

- Project dashboard for active novels.
- Canon browser.
- Character, location, timeline, and relationship views.
- Task queue for workers.
- Draft and revision history.
- Novel health / consistency checks.

### M4 — Studio operations

- Marketing planning and content workflow.
- Finance and treasury views.
- Visual asset planning.
- Business strategy workspace.
- Scheduled and recurring studio tasks.

### M5 — Product polish

- Replace milestone ZIP packaging with a normal source tree.
- Formalize release builds.
- Improve observability and error reporting.
- Add migration discipline for persistent data.
- Harden permissions and secrets handling.
- Prepare public-facing documentation only when the product is ready.

## Principles that remain constant

1. The creator stays in control.
2. Canon and continuity are first-class data.
3. Workers have distinct responsibilities.
4. Decisions should be reviewable later.
5. Cost should be visible, not hidden.
6. Memory should preserve provenance.
7. Automation should reduce repetitive work without removing meaningful approval points.

---

Roadmap items may move between milestones as implementation reveals better boundaries.
