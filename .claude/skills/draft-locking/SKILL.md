---
name: draft-locking
description: >
  Verify, lock, and manage revisions of completed drafts. Activates when: a draft is
  declared complete, the writer says "I think this is done," transitioning between
  revision colors, or preparing a draft for submission or sharing.
---

# Draft Locking

When a draft is "done" — all scenes drafted, coverage notes addressed, plot holes audited — this skill runs the final verification pass, locks the draft, and manages the revision trail.

## Process

### Full Verification Pass

Before locking, run these checks against the complete draft:

1. **Beat sheet compliance**: Read the draft against the beat sheet. Every beat should be present and every acceptance criterion should pass. Flag any deviations — some may have been intentional changes made during drafting, but all must be acknowledged.

2. **Character arc completion**: For each major character, trace their arc from first appearance to last. Does the arc match the Story Bible? Does the character's final state answer the thematic question (even if the answer is tragic)?

3. **Plant/payoff audit**: Walk the dependency map. Every plant should have a payoff. Every payoff should have a plant. List any orphans.

4. **Continuity scan**: Check for continuity errors — time of day inconsistencies, characters who are in two places at once, objects that appear and disappear, information a character knows but shouldn't (or doesn't know but should).

5. **Page count check**: Total and per-act. Is the script in the right range for its format?

6. **Invoke script-coverage**: Run a full coverage pass if one hasn't been done on the complete draft.

### Lock the Draft

If verification passes (or the writer accepts the remaining issues as known):

1. Save the draft with a revision identifier:
   ```
   drafts/[project]/[project-name]-[color].fountain
   ```

2. Record the revision in the revision log:
   ```
   docs/script-doctor/revisions/revision-log.md
   ```

   Format:
   ```markdown
   ## [Color] Draft — [Date]
   - Pages: [count]
   - Known issues: [list or "none"]
   - Changes from previous: [summary]
   - Beat sheet version: [date of beat sheet used]
   - Story Bible version: [date of Story Bible used]
   ```

### Revision Color Order

Industry standard revision colors, in order:
1. **White** — First draft
2. **Blue** — Second draft
3. **Pink** — Third draft
4. **Yellow** — Fourth draft
5. **Green** — Fifth draft
6. **Goldenrod** — Sixth draft
7. **Buff** — Seventh draft
8. **Salmon** — Eighth draft
9. **Cherry** — Ninth draft
10. **Tan** — Tenth draft

If you're past Cherry, the script has bigger problems than color-coding.

After locking, the writer has four options:

- **Submit/share**: The draft goes out. Invoke `pre-submission-checklist` if not already done.
- **Start a new revision**: Create a new working copy at the next color. The locked draft is preserved.
- **Keep and continue**: Mark the draft as a milestone but continue working in the same file.
- **Discard and restructure**: The draft isn't working. Return to `story-development` or `beat-sheet-planning` for a fundamental rethink.

## Rules

- **The locked draft is read-only.** Once locked, changes go in a new revision color, not in the locked file. This preserves the ability to compare versions.
- **Verification is not optional.** Don't lock without running the full pass. Skipping verification is how scripts go out with orphaned plants and broken arcs.
- **Known issues are documented, not hidden.** If the writer decides to lock despite an unresolved issue, it goes in the revision log. The next revision knows what to fix.
- **Every revision gets a log entry.** Even small changes. The log is how you trace what changed when.

## Anti-patterns

- **Locking too early.** If coverage has identified critical issues, don't lock. Fix the critical issues first.
- **Never locking.** Endless revision without ever declaring a draft "done" is a form of avoidance. At some point, the draft is good enough for the next step (sharing with a trusted reader, submitting to a competition, showing to a producer). Lock it and get feedback from the real world.
- **Losing revision history.** Every locked draft should be preserved. Don't overwrite.
