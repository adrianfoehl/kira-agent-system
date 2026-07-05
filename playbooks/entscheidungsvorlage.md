# Entscheidungsvorlage Playbook

You always follow the [PROCESS] and respect what's [IMPORTANT].

[AGENT USE]
Used by KIRA. Delegate to LEVI for research or NILS for technical comparison if needed.

[GOAL]
Create a structured decision brief for leadership: max 1 page, clear recommendation.

[INPUTS]
- decision (required; what needs to be decided?)
- options (optional; if the user already has options in mind)
- deadline (optional; when must this be decided?)
- audience (optional; e.g. your manager / executive round; defaults to your manager)

[PROCESS]

1. **Frame the decision**: What exactly must be decided? What triggered this? What happens if we don't decide?

2. **Define options**: At least 2, max 4. For each:
   - What is it?
   - Effort (time, money, people)
   - Expected outcome
   - Risks
   - Compliance implications (CISO / works council / internal audit)

3. **Build the brief:**
   ```markdown
   # Decision: [Title]
   Date: [YYYY-MM-DD]
   Decision needed by: [Deadline]

   ## Context
   [2-3 sentences. What's the situation, why now]

   ## Options

   | | Option A | Option B | Option C |
   |---|---|---|---|
   | **What** | ... | ... | ... |
   | **Effort** | ... | ... | ... |
   | **Outcome** | ... | ... | ... |
   | **Risk** | ... | ... | ... |
   | **Compliance** | ... | ... | ... |

   ## Recommendation
   **Option [X]**: [Why in 2 sentences]

   ## Next Steps (if approved)
   1. [First action]
   2. [Second action]
   ```

4. **Language**: The leadership's working language. English if the user needs it for their own thinking first.

5. **Write to file.**

[DEFINITION OF DONE]
- [ ] Max 1 page
- [ ] At least 2 options compared
- [ ] Clear recommendation (not "it depends")
- [ ] Compliance implications assessed
- [ ] Next steps defined

[IMPORTANT]
- Leadership decides based on business impact, not technical elegance. Frame accordingly.
- Always include "What happens if we don't decide". Urgency must be clear.
- A recommendation is not optional. "Here are options" without a recommendation wastes leadership's time.
