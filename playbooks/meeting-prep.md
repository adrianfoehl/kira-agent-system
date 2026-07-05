# Meeting-Prep Playbook

You always follow the [PROCESS] and respect what's [IMPORTANT].

[AGENT USE]
Used by KIRA or directly by the user.

[GOAL]
Produce a 1-page meeting brief with context, agenda, talking points, and anticipated questions, so the user walks in prepared.

[INPUTS]
- meeting_type (required; which meeting?)
- attendees (optional; who will be there?)
- topics (optional; known agenda items)
- your_goals (optional; what does the user want from this meeting?)

[PROCESS]

1. **Identify the meeting**: What type? Who's attending? What's the political landscape?

2. **Check your stakeholder notes** (if you maintain stakeholder profiles in your context files). For each key attendee:
   - What do they care about?
   - What's their communication preference?
   - Any current tensions or alignments?

3. **Research if needed**: If it's an external meeting, consider spawning LEVI for a quick dossier on the person/company.

4. **Build the brief:**
   ```markdown
   # Meeting Prep: [Meeting Name]
   Date: [YYYY-MM-DD]
   Attendees: [List]

   ## Context
   [2-3 sentences on what's happening, what led to this meeting]

   ## Your Goals
   - [What the user wants from this meeting]

   ## Key Stakeholders & Their Angle
   - [Role]: [What they care about, potential concerns]

   ## Talking Points
   1. [Point 1: what to say and why]
   2. [Point 2]
   3. [Point 3]

   ## Anticipated Questions & Prepared Answers
   - Q: [Likely question]
     A: [Prepared response]

   ## Landmines to Avoid
   - [Topic/phrase that could derail the meeting]

   ## Success Looks Like
   [What a good outcome from this meeting is]
   ```

5. **Language**: The organization's language for internal meetings. English for external unless specified.

6. **Write to file.**

[DEFINITION OF DONE]
- [ ] Stakeholder angle included for every key attendee
- [ ] Landmines section filled (not empty)
- [ ] Max 1 page
- [ ] One clear key message identified
- [ ] Language matches audience

[IMPORTANT]
- The user reads this 5 minutes before the meeting. Keep it scannable.
- For leadership rounds: always include the Regulated-Industry Reality Check lens
- For CEO 1:1s: frame everything in terms of business impact, not AI features
