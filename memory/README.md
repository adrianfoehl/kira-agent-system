# Memory

Each agent keeps exactly one memory file here: `[agent]-memory.md`. The real files are private and not part of this repository. `example-levi-memory.md` shows the shape with synthetic content.

## The rules that keep memory useful

1. **One file per agent, capped at 80 lines.** A memory file that grows without bound stops being read. When a file approaches the cap, compress: three similar entries become one pattern rule, completed project entries move to an archive.
2. **Memory stores decisions and patterns, not transcripts.** "Chose X over Y because Z" survives compression. Meeting notes do not belong here.
3. **Agents update their own file at the end of substantial sessions** (see `../system/feedback-loop.md`, Level 2). The orchestrator reads all memory files during retros and prunes.
4. **Memory is environment-specific.** Files are never synced between private and work environments. The mechanism is shared, the contents are not.

## Structure of a memory file

```markdown
## Current Focus        <- what this agent is working toward right now
## Active Projects      <- running threads with one-line status
## Patterns Recognized  <- compressed lessons, the highest-value section
## Open Items           <- loose ends the agent should not forget
```
