---
name: script-coverage
description: >
  Internal script coverage and notes generation. Activates when: reviewing a draft or
  portion of a draft, user asks for "notes" or "feedback," between drafting sequences,
  or when checking script quality. Generates structured coverage across four dimensions:
  structure, character, dialogue, and format.
---

# Script Coverage

This skill generates internal coverage — the same kind of analysis a professional script reader would produce, organized by category and severity. It does NOT produce a "coverage report" in the industry sense (with a PASS/CONSIDER/RECOMMEND rating). Instead, it produces actionable notes that feed back into revision.

## When to Invoke

- After completing a sequence of scenes (every 10-15 pages)
- When the writer asks for notes or feedback
- Before declaring a draft complete (pre-submission-checklist will invoke this)
- When something "feels off" but the writer can't identify why

## Coverage Dimensions

### 1. Structural Coverage

Read the draft against the beat sheet and evaluate:

- **Beat compliance**: Does each scene accomplish its stated dramatic purpose?
- **Pacing**: Are there sequences that drag? Scenes that rush? Is the page count balanced across acts?
- **Causality chain**: Does each scene follow logically from the previous one? Could you shuffle any scenes without the audience noticing? (If yes, the causality is too loose.)
- **Plant/payoff integrity**: Is every plant paid off? Is every payoff planted? Check the dependency map.
- **Act break strength**: Do the major turns actually turn? Is the Act 1 break a point of no return? Does the midpoint genuinely reframe the story? Is "all is lost" truly the lowest point?
- **Ticking clock**: Is there urgency? Does the audience know (or feel) that time is running out?

**Severity levels**:
- 🔴 **Critical**: A structural issue that breaks the story (missing payoff, broken causality, act break that doesn't turn). Block further drafting until fixed.
- 🟡 **Major**: A structural weakness that hurts the story but doesn't break it (pacing sag, soft midpoint). Fix in next revision pass.
- 🟢 **Minor**: A structural note that would improve the story (a scene that could be combined with another, a transition that could be smoother). Fix if time permits.

### 2. Character Coverage

For each major character, evaluate:

- **Arc tracking**: Is the character's arc progressing as defined in the Story Bible? Map their emotional state at each appearance.
- **Consistency**: Does the character behave consistently with their established traits? Inconsistency is only acceptable when it's the point of the scene (the character is lying, breaking down, or growing).
- **Agency**: Is the character driving events or being pushed around by the plot? Protagonists must make choices that have consequences.
- **Motivation clarity**: At every decision point, can you articulate why the character chose this? If not, the motivation is unclear.
- **Screen time distribution**: Is any major character disappearing for too long? Are minor characters eating screen time from major ones?
- **Relationship dynamics**: Are the key relationships changing over the course of the script? Static relationships are dead relationships.

### 3. Dialogue Coverage

Read ONLY the dialogue (ignore action lines) and evaluate:

- **Voice differentiation**: Cover the character names. Can you tell who's speaking from the dialogue alone? If you can't, the voices aren't differentiated.
- **Subtext**: How many lines mean exactly what they say? In a good script, most dialogue operates on two levels. Flag scenes where characters are saying what they mean — this is almost always a problem.
- **Exposition handling**: Is backstory delivered through conflict or through speeches? Flag any "maid-and-butler" dialogue (characters telling each other things they both know).
- **Line efficiency**: Flag dialogue that could be cut without losing meaning. If a character says in three sentences what could be said in one, note it.
- **Monologue check**: Flag any speech longer than 5 lines. Some are earned; most aren't. Each one needs to justify its length.
- **Dialect/period consistency**: If characters speak in a specific register (period dialogue, regional dialect, professional jargon), is it consistent throughout?

### 4. Format Coverage

Scan for technical screenplay format issues:

- **Scene heading format**: INT./EXT. LOCATION - TIME OF DAY. Every scene must have one.
- **Action line length**: No paragraph longer than 3 lines. Flag violations.
- **Camera direction**: Flag any "CLOSE ON," "WE SEE," "ANGLE ON," "CAMERA PANS" in spec scripts.
- **Character introduction**: Is every speaking character introduced in action lines (ALL CAPS) before their first dialogue?
- **Parenthetical overuse**: Flag scenes with parentheticals on more than 30% of dialogue lines.
- **Page count**: Is the total within format range? Is any individual scene significantly over its target?
- **Widows/orphans**: Scenes that start in the bottom 3 lines of a page or end in the top 3 lines of the next. (Cosmetic, but professional.)
- **Continued/more**: If scenes break across pages, are CONTINUED and MORE used correctly?

## Output Format

Present coverage as a structured note session, organized by severity within each dimension:

```
## Coverage Notes — [Draft Name], [Date]
### Pages reviewed: [range]

#### 🔴 Critical Issues (fix before continuing)
1. [STRUCTURE] Beat 23 plants the knife, but it's never paid off. ...
2. [CHARACTER] Maria's motivation for forgiving David in Scene 30 is unearned. ...

#### 🟡 Major Issues (fix in next revision)
1. [DIALOGUE] Jake and Elena sound identical in Scene 15-18. ...
2. [PACING] Act 2A drags — pages 35-50 could lose 5 pages. ...

#### 🟢 Minor Issues (polish-level)
1. [FORMAT] Camera direction on page 42 ("CLOSE ON the ring"). ...
2. [DIALOGUE] Maria's monologue on page 67 runs 8 lines — consider trimming. ...

#### ✅ Strengths
- [Brief note on what's working well — this matters for morale and for not breaking what works]
```

## Rules

- **Critical issues block progress.** Don't draft more scenes while critical issues exist upstream.
- **Be specific.** "The dialogue needs work" is not a note. "Jake's dialogue in scenes 15-18 uses the same vocabulary and cadence as Elena's — give him shorter sentences and more interruptions" is a note.
- **Strengths matter.** Always note what's working. The writer needs to know what NOT to change as much as what to change.
- **Don't rewrite.** Coverage identifies problems. It does not draft solutions. The fix comes through `plot-hole-auditing` (for structural issues) or another CRITERIA-DRAFT-POLISH cycle (for scene-level issues).
- **Severity is about story impact, not craft preference.** A clunky line of dialogue is minor. A protagonist who has no agency is critical. Don't inflate severity because you have a strong aesthetic preference.
