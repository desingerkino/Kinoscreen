---
name: drafting-sprints
description: >
  Batch execution through the beat sheet with sequence-level checkpoints. Activates
  when: the writer wants to power through drafting, prioritizes momentum over per-scene
  polish, or says "let's just get pages down." Faster than scene-delegation, trades
  some per-scene quality for drafting velocity.
---

# Drafting Sprints

Scene delegation produces the highest quality per scene, but it's slow. Drafting sprints trade some of that quality for momentum — drafting a full sequence (10-15 pages, 5-8 scenes) in one pass, then checkpointing with the writer before the next sequence.

## When to Use

- The writer wants to get a full draft down quickly
- The story and beat sheet are solid and the writer trusts the plan
- Revision will happen later — this is about getting the "clay on the wheel"
- The writer is losing motivation and needs forward progress

When NOT to use:
- The beat sheet is incomplete or has known structural issues (fix those first)
- The writer needs high per-scene quality (use scene-delegation instead)
- Key turning-point scenes (act breaks, climax) — these always deserve full scene-delegation treatment

## Process

### Sequence-Level Batches

Work through the beat sheet in sequence-sized batches:

```
Identify the next sequence (5-8 beats, ~10-15 pages)
    ↓
Draft all scenes in the sequence using consistency-driven-drafting
    (CRITERIA → DRAFT → POLISH for each, but at a faster tempo)
    ↓
Self-review the complete sequence:
    - Does the sequence build? (escalation, not repetition)
    - Are continuity bridges between scenes clean?
    - Are all acceptance criteria met?
    ↓
Checkpoint with the writer:
    - Present the sequence
    - Report page count (running total and this sequence)
    - Flag any beats that needed criteria adjustment
    - Flag any emerging issues (subplot drift, pacing concerns)
    ↓
Writer approves?
    → No: Revise specific scenes in the sequence
    → Yes: Move to next sequence
    ↓
Repeat until draft is complete
```

### Sprint Tempo

During a sprint, the CRITERIA-DRAFT-POLISH cycle runs faster:
- **CRITERIA**: Still mandatory. Read the beat entry, state the criteria. But don't agonize — the beat sheet already has them.
- **DRAFT**: Write to pass the criteria. Don't chase perfect dialogue. "Good enough to tell the story" is the bar.
- **POLISH**: One quick pass. Trim obvious bloat, catch any "we see" or camera direction that slipped in, ensure character names are consistent. Then move on. Deep polish is for revision.

### Checkpoint Protocol

At each checkpoint (every sequence):

1. **Page count report**: "[X] pages drafted. Running total: [Y] pages. Target: [Z] pages."
2. **Pacing assessment**: "This sequence covers [time period/story span]. Pacing feels [on track / slow / rushed]."
3. **Beat compliance**: "All beats hit" or "Beat [N] was adjusted — [brief explanation]."
4. **Emerging concerns**: Anything you noticed during drafting that the beat sheet didn't anticipate. New subplot that wants to emerge? Character who's asserting more presence than planned? A scene that revealed a better way to plant something?
5. **Decision point**: Does the writer want to continue, revise, or pause?

### Key Scenes Get Full Treatment

Even during a sprint, certain scenes always get the full scene-delegation treatment:
- **Opening scene**: First impression. It has to be right.
- **Act breaks**: The turns that define the structure.
- **Midpoint**: The revelation that reframes everything.
- **Climax**: The thematic question answered through action.
- **Final scene**: Last image. What the audience carries home.

These scenes are too important to sprint through. Slow down, assemble the full scene context packet, and draft with care.

## Rules

- **Don't skip criteria.** Sprint tempo means faster, not sloppier. Every scene still has criteria, and every draft still has to pass them.
- **Checkpoint every sequence.** Don't draft 40 pages without checking in. The writer needs to see the draft accumulating and flag problems early.
- **Track page count.** If the running total is significantly over or under target by the midpoint, stop and assess. Pacing problems compound.
- **Don't revise backward during a sprint.** If you notice that Scene 15 should have been written differently now that you've drafted Scene 25, make a note and keep going forward. Backward revision during a sprint kills momentum. Fix it in the revision pass.
- **Know when to stop sprinting.** If the quality is dropping noticeably — dialogue going flat, action lines getting generic, scenes feeling mechanical — stop the sprint. Take a break or switch to scene-delegation for the next sequence.

## Transition

After the sprint completes the full draft:
1. Invoke `script-doctor:script-coverage` for a full-draft coverage pass
2. Address critical and major issues via `script-doctor:plot-hole-auditing` and revision
3. When satisfied, invoke `script-doctor:draft-locking`
