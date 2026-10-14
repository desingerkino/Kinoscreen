---
name: draft-branching
description: >
  Create isolated draft branches for structural experiments. Activates when: the writer
  wants to try an alternate structure, test a different opening, explore a non-linear
  approach, or try "what if" scenarios without destroying the working draft.
---

# Draft Branching

When a writer says "what if we opened in media res?" or "what if the whole thing were non-linear?", the wrong move is to start rewriting the working draft. Draft branching creates an isolated copy where the experiment can play out without risk.

## When to Branch

- Exploring a different structural approach (linear vs. non-linear, in media res, etc.)
- Testing an alternate ending
- Trying a major character change (what if the protagonist is the antagonist?)
- Experimenting with a different POV or voice
- Attempting a significant tonal shift (comedy version vs. drama version)
- Any change that would touch more than 5 scenes

If the change affects fewer than 5 scenes, it's probably a revision, not a branch. Just revise.

## Process

### Create the Branch

1. Copy the current working draft to a new directory:
   ```
   drafts/[project]/branches/[branch-name]/
   ```
   Use a descriptive name: `in-media-res`, `ellens-pov`, `dark-comedy-version`, `alt-ending-tragic`

2. State the **hypothesis** — what the branch is testing:
   ```
   HYPOTHESIS: Starting on page 30 of the current draft (the inciting incident)
   and restructuring Act 1 as flashbacks creates more immediate tension.
   ```

3. Decide the **scope**: Is this a full redraft or a targeted restructuring?
   - Full redraft: Revise the beat sheet for the branch, then re-draft affected scenes
   - Targeted: Rearrange, revise, or replace specific scenes without touching others

### Work the Branch

- All changes happen in the branch directory, never in the working draft
- The Story Bible remains the same unless the branch hypothesis explicitly changes story fundamentals
- Create a branch-specific beat sheet if the structure changes significantly: `docs/script-doctor/branches/[branch-name]-beat-sheet.md`
- Use the same CRITERIA-DRAFT-POLISH cycle for any new or revised scenes

### Evaluate the Branch

When the experiment is complete (or complete enough to evaluate):

1. Read the branch version start to finish. Does the hypothesis hold?
2. Compare directly with the working draft at the key points of difference
3. Ask the writer to evaluate — present both versions at the critical divergence points
4. Document what worked and what didn't, regardless of which version "wins"

### Resolve the Branch

Four options:

- **Merge**: The branch replaces the working draft. Copy the branch to the main draft directory. Update the beat sheet. Archive the old working draft as a branch (so it's recoverable).
- **Cherry-pick**: Specific scenes or structural choices from the branch are incorporated into the working draft. List exactly which scenes are being moved.
- **Keep**: The branch is preserved as an alternate version but the working draft continues as-is. The branch may be useful later.
- **Discard**: The experiment didn't work. Delete the branch directory. Document what was learned in `docs/script-doctor/revisions/branch-notes.md`.

## Rules

- **One active branch at a time.** Multiple simultaneous branches create confusion. Finish evaluating one before starting another.
- **Always state the hypothesis.** A branch without a hypothesis is aimless rewriting. Know what you're testing.
- **Don't let branches linger.** A branch that's been open for more than one session without evaluation is probably a procrastination tool. Evaluate it or discard it.
- **The working draft is sacred.** Never modify the working draft while a branch is active. All experimental changes go in the branch.
- **Document the outcome.** Even a discarded branch taught you something. Write it down.

## Anti-patterns

- **Branching instead of revising.** "I'll just try a different version" when the real issue is a fixable plot hole in the current draft. Use `plot-hole-auditing` first.
- **Infinite branching.** Creating branch after branch without finishing any of them. This is avoidance. Pick a direction and commit.
- **Merging without reading.** The branch must be read end-to-end before merging. Don't assume it works because the individual scenes seem good.
- **Losing the working draft.** Always archive before merging. You might want it back.
