# Task-Delegation Playbook

You always follow the [PROCESS] and respect what's [IMPORTANT].

[AGENT USE]
Used by KIRA every time she delegates to a sub-agent.

[GOAL]
Produce a complete delegation that sets the sub-agent up for success.

[INPUTS]
- task_description (required; what the user wants done)
- target_agent (required; which agent should handle this)
- urgency (optional; "now" or "when ready")

[PROCESS]

1. **Parse the Request**: What does the user actually need? What's the deliverable?

2. **Select Agent**: Match to the routing table. If ambiguous, ask the user.

3. **Determine context_needed**: List ONLY the context files the agent needs for THIS task. Don't load everything.

4. **Write the Delegation:**
   ```
   ## Task
   [What needs to be done: clear, specific deliverable]

   ## Context Files to Read
   - skills/[agent]/SKILL.md
   - memory/[agent]-memory.md
   - [only the context files needed]

   ## Method
   [How to do it: constraints, approach, institutional knowledge]

   ## Output Requirements
   [Format, length, where to write]
   Write to: output/[agent]-[task].md

   ## If You Get Stuck
   [Specific failure handling]
   ```

5. **Spawn** via Task tool.

6. **Track**: Note the delegation in `memory/kira-memory.md`.

[DEFINITION OF DONE]
- [ ] Goal + Method + Capability all included
- [ ] context_needed scoped to task (not everything loaded)
- [ ] Output location specified

[IMPORTANT]
- Goal alone guarantees failure. ALWAYS include Method.
- Research MUST complete before synthesis begins
- Output goes to disk, never inline
- If agent fails twice → Escalate to the user, don't lower quality
