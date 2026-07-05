# Self-Learning Feedback System

**Read by every agent on startup.** These are the system-wide rules for learning and improvement.

## The 3 Learning Levels

### Level 1: Immediate Learning (Within a Session)
When the user provides feedback (explicit or implicit), update your Lessons Learned IMMEDIATELY before repeating the task.

**Explicit feedback signals:**
- "That's not what I wanted"
- "Too long / too short / wrong focus"
- "Exactly like that! Remember this."
- Direct corrections

**Implicit feedback signals:**
- The user ignores output and does it themselves
- The user rephrases the same request
- The user corrects output manually

**Action:** Append to your SKILL.md `## Lessons Learned` section using the structured format:
```
### [Category: Output Preferences | Mistakes I Won't Repeat | What Worked Well]
- [YYYY-MM-DD]: [What happened] → [What I learned]
```

### Level 2: Cross-Session Learning (Memory Files)
At the end of every substantial interaction, update your memory file (`memory/[agent]-memory.md`) with:
- Key decisions made
- Patterns recognized
- Open questions

### Level 3: System Evolution (Weekly Retrospective)
KIRA runs a retro on request ("KIRA, retro"): reads all memory files and Lessons Learned, identifies patterns, and recommends system changes.

## Hard Rules for Self-Modification

1. **Append-only to Lessons Learned**: Never delete or rewrite existing lessons
2. **Max 15 lessons per agent**: When you hit 15, flag to KIRA for compression during next retro
3. **Structured format required**: Date + What happened + What I learned
4. **Memory files capped at 80 lines**: When approaching the cap, compress older entries (keep patterns, drop specifics)
5. **No changes to Identity, Scope, or Routing sections**: Only the user or KIRA (during retro with the user's approval) can modify these
6. **Lessons override generic instructions**: When a lesson conflicts with a general approach, the lesson wins

## Memory Pruning Protocol
During weekly retros, KIRA:
1. Reviews all memory files approaching 80-line cap
2. Compresses: 3+ similar entries → 1 pattern rule
3. Archives: Move completed project entries to `knowledge-base/`
4. Preserves: Active projects, recognized patterns, open improvements

## Feedback Log
All feedback events are logged to `system/feedback-log.md` in chronological order:
```
[YYYY-MM-DD HH:MM] [AGENT] [LEVEL] [DESCRIPTION]
```
