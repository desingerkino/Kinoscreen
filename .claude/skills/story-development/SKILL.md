---
name: story-development
description: >
  Socratic story exploration and Story Bible creation. Activates BEFORE any page-writing.
  Use when: user wants to write a screenplay, has a movie/show idea, wants to develop a
  premise, or mentions wanting to "figure out the story." Do NOT skip to drafting.
---

# Story Development

This skill replaces the impulse to start writing pages immediately. The agent explores the story through questions, surfaces alternatives, and builds a Story Bible that becomes the source of truth for everything that follows.

## Process Flow

```
Explore the premise
    ↓
Ask clarifying questions (one at a time)
    ↓
Identify genre, tone, world, themes
    ↓
Develop characters (want, need, flaw, arc)
    ↓
Propose 2-3 structural approaches
    ↓
Present Story Bible sections for approval
    ↓
User approves Story Bible?
    → No: Revise specific sections
    → Yes: Write Story Bible document
    ↓
Spec self-review (check for contradictions, vagueness, missing pieces)
    ↓
User reviews written Story Bible
    ↓
Transition to beat-sheet-planning
```

## Rules

### One question at a time
Don't overwhelm. Ask a single focused question, listen to the answer, then build on it. The conversation should feel like a writers' room, not an interrogation.

### Push back on first answers
The first idea is rarely the best idea. When the writer says "it's about a cop who..." ask "what if the cop isn't actually a cop?" or "what's the version of this where the antagonist is right?" This isn't being difficult — it's doing the work of story development.

### Explore alternatives
Always propose 2-3 structural approaches before settling. The writer might not know that their thriller premise works better as a character study until you show them the shape of both.

### YAGNI ruthlessly
Remove subplots, characters, and world-building that don't serve the central dramatic question. A lean story is a strong story. If a character doesn't challenge the protagonist or embody the theme, they probably don't need to exist.

### Incremental validation
Present the Story Bible in sections. Get approval on each before moving to the next. The sections, in order:

1. **Logline** — One sentence. Who is the protagonist, what do they want, what's in their way, and what's at stake? If the logline doesn't work, nothing works. Spend time here.

2. **Thematic question** — What is this story asking? Not answering — asking. "Can a person be good in a corrupt system?" The theme is a question the story explores, and reasonable people should be able to disagree about the answer.

3. **Genre and tone** — What does this feel like? Name 2-3 reference works (films, shows, books) that live in the tonal neighborhood. Be specific: "The Coen Brothers' *No Country for Old Men* meets *Hell or High Water*" gives more direction than "dark thriller."

4. **World rules** — What does the audience need to know about how this world works? What's different from reality? What are the unspoken rules of the society? This is especially critical for sci-fi, fantasy, and period pieces, but every story has a world.

5. **Character map** — For each major character:
   - **Want**: What they're pursuing consciously (the plot goal)
   - **Need**: What they actually need to grow (the thematic goal)
   - **Flaw**: The specific trait that prevents them from getting what they need
   - **Arc**: How the flaw is challenged and whether it changes (tragic = it doesn't)
   - **Voice signature**: 2-3 sentences describing how this character speaks differently from every other character. Speech patterns, vocabulary level, verbal tics, what they avoid saying.

6. **Structural shape** — What's the architecture?
   - Three-act structure (classical)
   - Five-act structure (TV, Shakespeare)
   - Sequence approach (8 sequences)
   - Non-linear / fragmented
   - Bottle episode / unity of time and place
   - Braided narrative / parallel timelines
   - Writer's own preferred structure

7. **Rough act breaks** — Where are the major turns? Don't over-detail — just the seismic shifts. For a three-act feature:
   - End of Act 1 (~p.25-30): The protagonist commits to the journey
   - Midpoint (~p.55): A revelation that reframes everything
   - End of Act 2 (~p.85): All is lost / dark night of the soul
   - Climax (~p.100-110): The thematic question is answered through action

### Save the Story Bible

Write the completed, approved Story Bible to: `docs/script-doctor/story-bible.md`

Commit it. This document is the source of truth. Every subsequent skill references it.

### Self-review before handoff

Before asking the user to review the saved Story Bible, do a quick self-check:
- Are there any placeholder phrases like "TBD" or "something like..."?
- Do any character arcs contradict each other?
- Is the thematic question actually explored by the plot, or is it bolted on?
- Does the logline still accurately describe what the story has become?
- Could you hand this to a stranger and they'd understand the story?

Fix any issues inline before the user sees the document.

### Transition

After the Story Bible is approved, invoke `script-doctor:beat-sheet-planning`. Do NOT invoke any other skill. Beat sheet planning is always the next step.

## Anti-patterns

- **Starting with "What's your screenplay about?"** — Too vague. Start with something the writer can grab: "Tell me about the moment that made you want to write this." Or "Who's the person in this story, and what's the worst thing that could happen to them?"
- **Accepting a premise without pressure-testing** — "A detective investigates a murder" is not a story. What makes this detective different? Why this murder? What's the cost of solving it?
- **Building the world before the character** — World-building is seductive but secondary. The world exists to pressure-test the character. Build the character first, then ask: "What world would put maximum pressure on this person's specific flaw?"
- **Skipping the thematic question** — A screenplay without a thematic question is just a sequence of events. It might be entertaining, but it won't resonate. Insist on finding the question.
- **Over-engineering the Story Bible** — The Story Bible is a working document, not a novel. If a section runs longer than a page, it's too detailed for this stage. Save the detail for the beat sheet.
