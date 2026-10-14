---
name: scene-delegation
description: >
  Dispatch a fresh context per scene with tight instructions and two-stage review.
  Activates when: drafting from a beat sheet, writing multiple scenes in sequence,
  or user wants high-quality scene-by-scene drafting. This is the preferred approach
  for quality over speed.
---

# Scene Delegation

Each scene gets drafted by a fresh context that receives only what it needs: the Story Bible, the beat entry for this specific scene, continuity notes from the previous scene, and the acceptance criteria. This prevents the accumulated drift that degrades quality over long drafting sessions.

## Why Fresh Context Per Scene

When a single context drafts scenes 1 through 50, several failure modes emerge:
- **Tonal drift**: The voice shifts gradually as the context window fills with prior scenes
- **Drift-fixing**: Later scenes subtly rewrite earlier decisions without the writer noticing
- **Fatigue patterns**: Dialogue becomes more generic, action lines more formulaic
- **Context pollution**: Details from Scene 12 bleed into Scene 40 in unintended ways

Fresh context per scene eliminates all of these. The tradeoff is speed — it's slower than continuous drafting. Use `drafting-sprints` if momentum matters more than per-scene quality.

## Process Flow

```
Read the beat sheet
    ↓
For each scene (in order):
    ↓
    Assemble the scene context packet:
        - Story Bible (full)
        - This scene's beat entry (with acceptance criteria)
        - Last 10-15 lines of the previous scene (continuity bridge)
        - Any relevant plant/payoff notes from the dependency map
        - Character voice signatures for characters in this scene
    ↓
    Dispatch to fresh context with consistency-driven-drafting
    ↓
    Receive drafted scene
    ↓
    Two-stage review:
        Stage 1 — Spec compliance (does it hit the beat?)
        Stage 2 — Craft quality (is it well-written?)
    ↓
    Pass both stages?
        → No: Return with specific notes, redraft
        → Yes: Accept scene, update continuity bridge for next scene
    ↓
    Checkpoint: Every 3-5 scenes, present progress to the writer
    ↓
Next scene
```

## The Scene Context Packet

The packet sent to the fresh drafting context contains exactly these pieces, no more:

### 1. Story Bible
The full Story Bible. This never changes between scenes. It provides the world rules, character definitions, tone references, and thematic question.

### 2. This Scene's Beat Entry
The specific beat entry from the beat sheet, including all acceptance criteria. This is the "assignment."

### 3. Continuity Bridge
The last 10-15 lines of the previously drafted scene. This provides:
- The emotional temperature entering this scene
- Any unfinished actions or dialogue
- The physical state of the world (time of day, location context)
- The last image the audience saw

For the first scene of the script, the continuity bridge is replaced with a brief note about the opening tone and first image strategy from the Story Bible.

### 4. Dependency Notes
If the beat sheet marks this scene as planting something or paying something off, include the relevant cross-reference:
- "This scene plants the ticking clock on the mantle. It pays off in Beat 47."
- "This scene pays off the lie established in Beat 12. The audience has been waiting 30 pages for this."

### 5. Character Voice Signatures
The voice signature entries from the Story Bible for every character who appears in this scene. This is redundant with the full Story Bible, but extracting it separately ensures the drafter focuses on voice differentiation.

## Two-Stage Review

After receiving a drafted scene, review in two passes:

### Stage 1: Spec Compliance
- Does the scene pass every acceptance criterion from the beat entry?
- Are the right characters present?
- Is the page count within the target?
- Does the plant/payoff land correctly?
- Does the scene heading match the beat entry?
- Does the scene's dramatic purpose actually occur?

**If Stage 1 fails: Return with specific failure notes. Do not proceed to Stage 2.**

### Stage 2: Craft Quality
- Does the dialogue differentiate characters? Read each character's lines in isolation.
- Is there subtext? Are characters saying what they mean, or is there a gap between text and intent?
- Are action lines lean and visual? No internal states, no camera direction, max 3 lines per paragraph.
- Is there visual storytelling? Could any dialogue beat be replaced with an image?
- Does the scene have rhythm? Varied line lengths, varied speech lengths, intentional pacing.
- Does the scene's opening earn the reader's attention for those specific pages?

**If Stage 2 fails: Return with specific craft notes. Indicate severity — some craft issues are polish-level (fix later) and some are structural (fix now).**

## Checkpoints

Every 3-5 scenes, present the accumulated draft to the writer:
- Show the new scenes in context (with the previous scene for continuity)
- Report any criteria that required multiple drafting passes
- Flag any emerging issues (a subplot that's running too long, pacing that feels off)
- Confirm the writer wants to continue with the current approach

The writer can adjust the beat sheet at any checkpoint without losing previously drafted scenes — but flagging any dependencies that might be affected.

## Context Isolation Principle

The drafting context receives ONLY the scene context packet. It does not receive:
- Previously drafted scenes (except the continuity bridge)
- Notes or feedback from other scenes' review passes
- The writer's stream-of-consciousness comments from earlier in the session
- Other scenes' acceptance criteria

This isolation is what makes the system work. Each scene is drafted as a standalone unit that happens to connect to its neighbors through the continuity bridge.

## Anti-patterns

- **Sending the full draft so far**: The drafter doesn't need 40 pages of prior script. They need 10 lines of continuity and the Story Bible. More context = more drift.
- **Skipping Stage 1 review**: "The dialogue is great, so the scene must work." No. Great dialogue in a scene that doesn't hit its beat is worse than mediocre dialogue in a scene that does — the great dialogue is harder to cut.
- **Combining scenes to save time**: Each scene is a separate CRITERIA-DRAFT-POLISH cycle. Combining two beats into one drafting pass means neither gets properly verified.
- **Ignoring continuity bridges**: If Scene 14 ends with Maria crying and Scene 15 opens with Maria laughing, the drafter needs to know whether that's a deliberate time cut or a continuity error. The bridge makes this explicit.
