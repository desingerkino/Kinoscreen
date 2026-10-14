---
name: beat-sheet-planning
description: >
  Create a granular, scene-by-scene beat sheet with acceptance criteria for every beat.
  Activates after story-development has produced an approved Story Bible. Use when:
  transitioning from story to structure, user says "let's outline this," or an approved
  Story Bible exists and the user is ready to plan.
---

# Beat Sheet Planning

This skill takes the approved Story Bible and breaks it into a granular, scene-level plan. Every beat has enough specificity that a fresh agent — one who has never read the rest of the script — could draft the scene correctly from the beat entry alone.

## Prerequisites

An approved Story Bible must exist at `docs/script-doctor/story-bible.md` (or the user's preferred location). If it doesn't, invoke `script-doctor:story-development` first.

## Process Flow

```
Read the approved Story Bible
    ↓
Map the act structure into sequences
    ↓
Break sequences into individual beats/scenes
    ↓
Write acceptance criteria for each beat
    ↓
Identify dependencies between beats (plants/payoffs)
    ↓
Present the beat sheet in sequence-sized chunks for approval
    ↓
User approves?
    → No: Revise specific sequences
    → Yes: Save beat sheet document
    ↓
Ready for drafting (scene-delegation or drafting-sprints)
```

## Beat Entry Format

Every beat in the sheet follows this structure:

```markdown
### Beat [number]: [Short descriptive title]

- **Scene heading**: INT./EXT. LOCATION - TIME OF DAY
- **Characters present**: [list]
- **Dramatic purpose**: What changes in this scene. What is different at the end than at the beginning. Be specific — "Maria learns David lied" not "conflict happens."
- **Sequence**: [which sequence this belongs to, e.g., "Act 1 / Sequence 2: Establishing the world"]
- **Page target**: [approximate page count, e.g., "2-3 pages"]
- **Plants/setups**: What this scene establishes for later payoff. Reference the payoff beat number.
- **Payoffs**: What earlier plant this scene pays off. Reference the plant beat number.
- **Enters from**: [Brief note on the emotional/narrative state carrying in from the previous scene]
- **Exits to**: [What state this scene leaves the audience in, setting up the next scene]

**Acceptance criteria**:
- [ ] [Specific, testable requirement — e.g., "Maria discovers the lie through action, not dialogue"]
- [ ] [e.g., "Power dynamic shifts from David to Maria by scene's end"]
- [ ] [e.g., "Scene ends on a visual beat, not a line of dialogue"]
- [ ] [e.g., "Under 3 pages"]
- [ ] [e.g., "No exposition about backstory — the audience should feel the betrayal, not understand it yet"]
```

## Rules

### Granularity scales to format

- **Feature film**: Every scene gets a beat entry. A 100-page script might have 50-70 beats.
- **TV pilot (hour)**: Every scene, organized by act. Mark act breaks explicitly. 40-55 beats.
- **TV pilot (half-hour)**: Every scene. 25-35 beats.
- **Short film**: Every scene, but the beats may be very small (half-page scenes). 8-20 beats.

### Acceptance criteria are non-negotiable

Every beat MUST have acceptance criteria. This is what makes the drafting process work. Without criteria, the drafter has no way to verify their own work. Criteria must be:
- **Specific**: "The audience learns X" not "information is conveyed"
- **Testable**: You can read the drafted scene and unambiguously say yes or no
- **Functional**: About what the scene *does*, not how it *sounds* (craft is for polishing, not planning)

### Map dependencies explicitly

If Beat 34 only works because of a plant in Beat 12, say so in both entries. This creates a dependency graph that prevents revision damage — when you change Beat 12, you know to check Beat 34.

Common dependency types:
- **Plant → Payoff**: Object, information, or character trait introduced early, activated later
- **Promise → Delivery**: Tonal or structural promise (opening with a mystery promises a revelation)
- **Setup → Escalation**: Each scene in a sequence must escalate the previous one
- **Character state**: A character's emotional state at the end of one scene is the starting state for their next appearance

### Present in sequence-sized chunks

Don't dump 60 beats on the writer at once. Present one sequence at a time (typically 5-10 beats), get approval, then move to the next. If the writer wants to restructure a sequence, it's much easier to do it before the rest of the outline depends on it.

### The "could it be cut?" test

For every beat, ask: if this scene were removed, would the story still make sense? If yes, the scene needs to either gain a dependency (it must plant or pay off something) or be cut from the plan. No scenes exist for atmosphere alone — atmosphere is a byproduct of scenes that do real work.

Exception: a "breathing room" scene after a major climax can serve a pacing function, but it must still contain character work. The audience rests, but the character is processing.

### Page count budget

Track cumulative page count as you build the beat sheet. The total should land in the format's range:
- Feature: 95-115 pages (leave room for discovery during drafting)
- Hour pilot: 52-62 pages
- Half-hour pilot: 28-34 pages
- Short: 5-14 pages

If the beat sheet totals significantly over, identify beats to combine or cut before drafting begins. It's much cheaper to restructure an outline than a draft.

## Save Location

Write the completed, approved beat sheet to: `docs/script-doctor/beat-sheet.md`

## Transition

After the beat sheet is approved, the writer chooses their drafting approach:
- **scene-delegation**: Best for quality. Each scene gets a fresh context with tight instructions.
- **drafting-sprints**: Best for momentum. Batch-draft a sequence at a time with checkpoints.

Both approaches use `consistency-driven-drafting` for the actual scene writing.

## Anti-patterns

- **Vague dramatic purpose**: "They argue" is not a dramatic purpose. "Maria forces David to admit the lie, but David turns it around by revealing Maria's own secret" is a dramatic purpose.
- **Missing acceptance criteria**: Every beat must have them. "Write a good scene" is not a criterion.
- **Linear-only thinking**: Not every scene's only dependency is the scene before it. A plant in scene 3 might pay off in scene 45. Map these cross-links.
- **Over-prescribing dialogue**: The beat sheet describes what the scene does, not what people say. "Maria confronts David" is planning. "Maria says 'I know you lied'" is drafting. Don't draft in the outline.
- **Ignoring subplots**: Every subplot needs its own beat entries woven into the main beat sheet. If a subplot disappears for 20 pages, either add connective beats or cut the subplot.
