# Evolution Decisions

Decision log: what was changed in the system, when, and why. Updated during retros.

> Transparency note: the entries before July 2026 were reconstructed from working notes when preparing this public release. The mechanism (log every structural change during retros) existed from day one. The discipline of filling it in real time did not. That gap is itself one of the more useful lessons in this repository, see the README.

Format:
```
## [YYYY-MM-DD]: [Change Title]
**What changed:** [Description]
**Why:** [Reasoning]
**Decided by:** user / retro
**Affected agents:** [List]
```

---

## 2026-03-07: System created (Phase 0 + Phase 1)
**What changed:** Initial build of 7 MVP agents (KIRA, LEVI, THEO, VERA, SARA, MAX, EMMA) plus system files and 5 priority playbooks.
**Why:** Replace ad-hoc prompting with a persistent team: stable roles, stable quality bars, reusable workflows.
**Decided by:** user
**Affected agents:** All

## 2026-03-16: Dual-environment split
**What changed:** The system was split into three content layers: personal-sensitive, personal-universal, and work. Export skills depersonalize the universal layer so the same mechanics can run in a work environment without carrying private content. Values and priorities were split into separate files along the same boundary.
**Why:** One system, two environments. Private context must be structurally unable to leak into work outputs, not just filtered by convention. The boundary lives in the file layout, not in prompts.
**Decided by:** user
**Affected agents:** All (context loading), KIRA (routing)

## 2026-04: Bench grows to 9 agents
**What changed:** Two additional specialists were added after recurring work kept landing between existing scopes, including a dedicated enablement/training persona (HANNA).
**Why:** Rule of thumb that emerged: add an agent only when a recurring kind of work has its own quality bar that existing agents keep missing. Not before.
**Decided by:** user / retro
**Affected agents:** New personas, KIRA routing table

## 2026-06-15: Lead-plus-specialists recognized as a single-user pattern
**What changed:** While designing an organization-wide agent system inspired by this one, a red-team review (run by THEO, one of this system's own agents) concluded that copying the KIRA topology, one lead plus named specialists, would be an anti-pattern at organizational scale. The org design became a single generic agent with permission scopes and shared skills instead. This system keeps its topology for single-user use, where it works.
**Why:** Named personas encode one person's preferences and trust levels. An organization needs role-based access and shared governance, not a cast of characters.
**Decided by:** retro (THEO review), confirmed by user
**Affected agents:** None here, but the insight shaped the sibling org system

## 2026-07-05: Public release
**What changed:** The mechanism layer (orchestrator, skills, playbooks, feedback loop, memory schema) was exported to this public repository. Context and memory contents were replaced with synthetic examples. This log was reconstructed from working notes, see the transparency note above.
**Why:** The system is more useful shared than private, and the private substance was never needed to explain the mechanics.
**Decided by:** user
**Affected agents:** None (content-identical export, private layers removed)
