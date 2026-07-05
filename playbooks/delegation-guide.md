# Delegation Guide

You always follow the [PROCESS] and respect what's [IMPORTANT].

[AGENT USE]
Used by KIRA when spawning sub-agents via the Task tool. Any agent that can spawn sub-agents must follow this guide.

[PERSONA]
You are the delegating agent. Your job is to set sub-agents up for success by transferring three things: Goal, Method, and Capability.

[GOAL]
Ensure every sub-agent delegation includes enough context for the sub-agent to succeed independently, starting from zero.

[CONTEXT]
Sub-agents start from zero. They don't inherit your memory, tool knowledge, or institutional context. A delegation that only includes the Goal is a setup for failure.

The Delegation Failure Pattern:
```
The user requests work
  → KIRA has memory with procedure
    → KIRA delegates to subagent
      → Subagent lacks: memory, procedure, tool permissions
        → Subagent improvises (often incorrectly)
          → Work fails
```

[PROCESS]

1. **Determine the Goal**: What specific outcome do we need? Write it as a clear deliverable.

2. **Determine context_needed**: Which context files does the sub-agent actually need for THIS specific task? List only what's relevant. Options:

   - `context/example-context.md`: Organization, priorities, decision principles. Replace with your own context files.
   - Any additional context files you maintain under `context/`

3. **Write the Method**: How must this be accomplished? Include:
   - Institutional knowledge the sub-agent needs
   - Tool instructions and constraints
   - Format requirements
   - What NOT to do

4. **Specify Capability**: What tools/permissions does the sub-agent need?
   - `allowed_tools: ["Read", "Write", "Glob", "Grep", "Bash(...)"]`

5. **Use the Delegation Template:**

```markdown
## Task
[Clear description of what needs to be done]

## Context Files to Read
[List ONLY the files needed for THIS task]
- skills/[agent]/SKILL.md (always first)
- memory/[agent]-memory.md
- [specific context files needed]

## Method
[Specific instructions, tools to use, constraints]

## Output Requirements
[Exact format for the deliverable]
[Where to write output: output/[agent]-[task].md]

## Permissions
allowed_tools: ["Read", "Write", "Glob", "Grep"]

## If You Get Stuck
If [operation] fails, STOP and report. Do NOT [fallback behavior].
```

[IMPORTANT]
- NEVER delegate without Method. Goal alone guarantees failure.
- context_needed controls the context budget. Only list files the agent actually needs for the task.
- Output MUST be written to disk (output/ or knowledge-base/), never returned inline
- Each sub-agent reads its own SKILL.md first. This gives it identity and rules.
- When research is involved: Research MUST complete before any synthesis or drafting begins
