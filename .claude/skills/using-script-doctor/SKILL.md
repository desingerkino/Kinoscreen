---
name: using-script-doctor
description: >
  Introduction to Script Doctor skills. Invoke BEFORE any screenwriting or script work
  to determine which skill applies. Activates when: user mentions screenplay, script,
  teleplay, pilot, scene, dialogue, story, beat sheet, coverage, draft, or any dramatic
  writing task.
---

# Using Script Doctor

Script Doctor is a set of composable skills for screenwriting. They are mandatory workflows, not suggestions.

## Skill Invocation Rules

Invoke relevant skills BEFORE any response or action. Even a 1% chance a skill might apply means you should invoke the skill to check. If an invoked skill turns out wrong for the situation, you don't need to use it.

## Routing

| User says...                                      | Invoke first               | Then...                       |
|---------------------------------------------------|----------------------------|-------------------------------|
| "Let's write a screenplay/script/pilot"           | story-development          | → beat-sheet-planning         |
| "I have an idea for a movie/show"                 | story-development          | → beat-sheet-planning         |
| "Help me outline/structure this story"             | story-development          | → beat-sheet-planning         |
| "Write scene X" / "Draft the next scene"          | consistency-driven-drafting | (within scene-delegation)     |
| "Something feels off about this scene/story"      | plot-hole-auditing         |                               |
| "Review this draft" / "Give me notes"             | script-coverage            |                               |
| "What if we tried a different structure?"          | draft-branching            |                               |
| "I think the draft is done"                       | pre-submission-checklist   | → draft-locking               |
| "Let's power through the next sequence"           | drafting-sprints           |                               |
| "Fix this plot hole" / "This doesn't work"        | plot-hole-auditing         |                               |

## Skill Categories

**Rigid skills** — follow exactly, don't adapt away the discipline:
- consistency-driven-drafting (CRITERIA-DRAFT-POLISH cycle)
- pre-submission-checklist (every item, no skipping)
- plot-hole-auditing (4-phase process, no shortcuts)

**Flexible skills** — adapt principles to the project's needs:
- story-development (Socratic approach, but the questions change per genre)
- beat-sheet-planning (granularity adapts to format — feature vs. pilot vs. short)
- script-coverage (depth adapts to draft stage)

## Key Principles

1. **Never jump to pages.** Story-development comes first. Always.
2. **Criteria before drafting.** Know what a scene must do before writing it.
3. **Fix at the root.** Never patch a problem with exposition. Trace back to where the problem started and fix it there.
4. **Every scene must turn.** Something must change — power, information, relationship, stakes. If nothing changes, it's not a scene.
5. **Fresh context per scene.** When delegating scene drafting, each scene gets only what it needs: the Story Bible, its beat entry, continuity from the previous scene, and its acceptance criteria. No accumulated drift.

## Format Awareness

Script Doctor is format-aware. Adapt to what the writer is building:

- **Feature screenplay**: 90-120 pages, three-act structure (or the writer's preferred structure), standard spec script format
- **TV pilot (hour)**: 55-65 pages, act breaks for commercial structure (if network), teaser + 4-5 acts typical
- **TV pilot (half-hour)**: 28-35 pages, cold open common, 2-3 acts
- **Short film**: Under 15 pages, compressed structure, often a single dramatic question
- **Limited series / miniseries**: Plan the full arc, outline per episode, draft as individual scripts
- **Sketch / comedy piece**: Premise-escalation-blow structure, tight page count

## Document Locations

- Story Bible: `docs/script-doctor/story-bible.md`
- Beat sheet: `docs/script-doctor/beat-sheet.md`
- Draft: `drafts/[project-name]/[draft-name].fountain` or `.md`
- Coverage notes: `docs/script-doctor/coverage/`
- Revision history: `docs/script-doctor/revisions/`

## Screenplay Format Reference

All drafts should use standard screenplay format:
- Scene headings: `INT./EXT. LOCATION - TIME OF DAY`
- Action lines: Present tense, lean prose, no camera direction in spec scripts
- Character names: ALL CAPS on first introduction, centered above dialogue
- Dialogue: Centered block under character name
- Parentheticals: Sparingly — only when the read would be wrong without them
- Transitions: Rarely needed; `CUT TO:` is implied

Fountain markup is preferred when writing to files. Markdown is acceptable for inline drafting.
