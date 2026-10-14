---
name: plot-hole-auditing
description: >
  4-phase root cause analysis for story logic issues. Activates when: something feels
  wrong in the script, a plot hole is identified, a character's behavior doesn't track,
  a payoff doesn't land, or the writer says "this doesn't work" or "something's off."
  Do NOT patch symptoms — trace back to the root and fix there.
---

# Plot Hole Auditing

This is the screenwriting equivalent of systematic debugging. When something doesn't work in a script, the instinct is to patch it where the symptom appears — add a line of exposition, insert a flashback, have a character explain their motivation. These patches almost always make the script worse. This skill traces the problem to its root and fixes it there.

## The 4-Phase Process

### Phase 1: IDENTIFY — Name the symptom precisely

Before you can fix anything, you have to articulate exactly what's wrong. "Something's off" is a starting point, not a diagnosis.

Translate the feeling into a specific, testable statement:
- ❌ "Act 3 doesn't work"
- ✅ "The audience won't believe Maria forgives David in Scene 30 because the forgiveness hasn't been earned"

- ❌ "The pacing is slow"
- ✅ "Pages 35-50 contain 6 scenes but only one new piece of information enters the story"

- ❌ "The villain is weak"
- ✅ "The antagonist's plan is never explained clearly enough for the audience to fear it"

- ❌ "It's confusing"
- ✅ "The audience doesn't know what Maria wants until page 25, so the first 25 pages have no dramatic engine"

Write the symptom as a clear statement before proceeding.

### Phase 2: TRACE — Work backward to the root

Starting from the symptom, trace backward through the script asking "why?" at each step:

**Example trace:**
```
SYMPTOM: Maria's forgiveness of David in Scene 30 feels unearned.
↑ Why? Because there's nothing between his betrayal (Scene 18) and the forgiveness (Scene 30) that shows David changing or Maria processing.
↑ Why not? Because scenes 19-29 are focused entirely on the B-plot (the investigation).
↑ Why? Because the beat sheet didn't account for the emotional throughline of the A-plot during the B-plot sequences.
↑ ROOT: The beat sheet has a 12-scene gap in the Maria/David relationship. The plan is missing beats, not the draft.
```

**Another example:**
```
SYMPTOM: The twist in Scene 45 doesn't land — it feels arbitrary.
↑ Why? Because the clues that should make it "inevitable in hindsight" aren't there.
↑ Why not? Because the plants were cut during a pacing revision of Act 1.
↑ ROOT: The Act 1 pacing revision damaged the plant/payoff chain. The plants need to be restored (possibly in different scenes that don't have the pacing problem).
```

Rules for tracing:
- **Go at least 3 levels deep.** The first "why" almost never reaches the root.
- **Look backward, not forward.** The fix is almost always earlier in the script than the symptom.
- **Check the beat sheet.** Is the problem in the execution (the drafted scenes) or the plan (the beat sheet itself)? If the beat sheet is missing beats, adding scenes to the draft without updating the plan will create new problems.
- **Check the Story Bible.** Is the problem even deeper — a character whose want/need/flaw don't create the right pressure? A thematic question that doesn't connect to the plot?

### Phase 3: FIX — Repair at the root, not the symptom

Based on where the trace ended, fix at that level:

**If the root is in the Story Bible:**
- Revise the character definition, thematic question, or world rules
- Cascade the change through the beat sheet
- Identify which drafted scenes are affected
- Re-draft affected scenes with updated criteria

**If the root is in the beat sheet:**
- Add, remove, or revise beats
- Update the dependency map
- Check for downstream beats that depend on the changed ones
- Re-draft only the scenes that changed

**If the root is in the draft:**
- Revise the specific scene(s)
- Run a new CRITERIA-DRAFT-POLISH cycle with updated or additional criteria
- Check continuity bridges to adjacent scenes

### Phase 4: VERIFY — Confirm the fix and check for collateral damage

After making the fix:

1. **Re-read the full sequence** from the earliest changed scene through the symptom scene. Does the symptom resolve?
2. **Check the dependency map.** Did the fix break any other plant/payoff chains?
3. **Read forward from the fix.** Do any downstream scenes now contradict the changed material?
4. **Run a targeted coverage pass** on the affected sections (invoke `script-doctor:script-coverage` on the changed pages).

If the fix introduced new problems, return to Phase 1 with the new symptom. Do not attempt to fix collateral damage without going through the full 4-phase process.

## Common Root Cause Patterns

### The Missing Beat
**Symptom**: A moment feels unearned or abrupt.
**Root**: The beat sheet is missing a transitional beat — a scene that bridges two emotional states. The audience needs to see the journey, not just the departure and arrival.

### The Severed Plant
**Symptom**: A payoff falls flat or feels random.
**Root**: The plant was cut during revision, or the plant scene was revised in a way that no longer sets up the payoff. Check revision history.

### The Wrong Character
**Symptom**: A scene feels flat despite good dialogue and structure.
**Root**: The wrong character is carrying the scene. The dramatic function belongs to someone else — someone with more at stake, more to lose, or a stronger connection to the thematic question.

### The Motivation Gap
**Symptom**: A character's choice doesn't make sense.
**Root**: The character's want or need (as defined in the Story Bible) doesn't actually drive this choice. Either the Story Bible definition is wrong, or the scene is asking the character to act out of character without earning it.

### The Exposition Band-Aid
**Symptom**: A scene is drowning in dialogue where characters explain things.
**Root**: Information that should have been dramatized earlier is being crammed in via exposition. The fix isn't better exposition — it's an earlier scene that shows instead of tells.

### The Pacing Sag
**Symptom**: A sequence feels slow.
**Root**: Multiple scenes in the sequence have the same dramatic function — they're all "showing things getting worse" without escalating. Each scene must do something the previous one didn't.

## Rules

- **Never patch.** Don't add a line of dialogue to explain a plot hole. Don't insert a flashback to justify a character choice. Don't have a character monologue about their feelings. These are all patches. Find the root.
- **Trace before fixing.** The impulse to fix immediately is strong. Resist it. A wrong fix at the wrong level creates two problems where there was one.
- **One symptom at a time.** If coverage identified 5 issues, audit them one at a time. They may share a root (in which case, one fix resolves multiple symptoms), but you can't tell until you trace each one.
- **Update all documentation.** If the fix changes the Story Bible, update it. If it changes the beat sheet, update it. Documentation drift is how new plot holes are born.
