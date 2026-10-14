# CLAUDE.md

## Project

- **Type:** fiction
- **Title:** Вася
- **Genre:** —
- **Logline:** —
- **Format:** —
- **Theme:** —
- **Seed:** —
- **Target audience:** —
- **Setting:** —
- **Period:** —
- **Currency and locale:** —
- **Runtime:** —
- **Story structure:** three-act (default)

Working language: **Russian**. All responses, comments and scene text in Russian.

## Characters

| Name | Age | Role | External goal | Inner need |
|------|-----|------|---------------|------------|

<!-- External goal: what the character is actively pursuing (visible, concrete)  -->
<!-- Inner need: what they must change or accept in themselves — often the opposite of what they want -->

## Structure

### Scenes

| # | File | Act/Loop | Key event | Status |
|---|------|----------|-----------|--------|

### Structural beats

---

## Scene formatting

Strictly per screenplay format. Quick rules:

```markdown
# Scene 01: Title

INT./EXT. LOCATION — TIME OF DAY

Action description. Present tense, third person. Max 4 lines per paragraph.

CHARACTER NAME
*(parenthetical)*
Dialogue text.
```

- ONE blank line between blocks; ZERO between name and dialogue
- Names — CAPS, plain text (no asterisks); no bold anywhere in scene files
- Slug line — plain text: `INT. LOCATION — DAY`
- First appearance: `NAME (age)` in caps within action text
- Do not use: `FADE OUT.`, `CUT TO:`, `CLOSE ON:`
- Numbers in dialogue — written out as words
- `---` — location change within a scene (converter skips it)
- `> **PALETTE:** ...` — visual note

## Working rules

- Do NOT renumber files without an explicit command
- When adding a scene — update the scenes table above and "Change log"
- Inserting scenes between existing ones → renumber subsequent scenes (whole numbers only, no letter suffixes)
- File renaming: two-phase rename via temp names (avoid collisions)
- AI writing patterns are forbidden — see `analytics/avoid-ai-writing-tells.md`
- Write only what the camera sees: actions, not emotions. Not "Мария грустит", but "Мария смотрит в окно, сигарета догорела нетронутой." Strong verbs, specific details.
- Craft skills `sw-*` (structure, dialogue, scene craft, character conflict, premise/theme, genre, workflow) live in `.claude/skills/`; use them for analysis and revision. Their text is in Chinese, answers stay in Russian.
- Skill `screenplay-writer` (`.claude/skills/screenplay-writer`) drives this project: new scenes, rewrites, analysis, character sheets, outline, `/full-check`-style audit, DOCX export. Read its SKILL.md first.
- Drafts: each significant revision is a git commit; DOCX exports go to `versions/`

## Script Doctor workflow

Skills from script-doctor (`story-development`, `beat-sheet-planning`, `consistency-driven-drafting`, `scene-delegation`, `drafting-sprints`, `script-coverage`, `plot-hole-auditing`, `draft-branching`, `draft-locking`, `pre-submission-checklist`) give the process: Story Bible first, then beat sheet, then scene-by-scene drafting with acceptance criteria, then coverage notes. Commands: `/develop-story`, `/coverage`, `/submit-check`.

Where they disagree with this project, the project wins:

- Story Bible → `docs/script-doctor/story-bible.md`, beat sheet → `docs/script-doctor/beat-sheet.md`, coverage → `docs/script-doctor/coverage/` (as the skills say).
- Scenes are NOT written to `drafts/*.fountain`. They go to `scenes/NN_title.md` in the format above, and the scene table and change log in this file stay current.
- Fill the Project fields above (logline, genre, theme, characters) from the approved Story Bible.
- Format and AI-pattern rules in "Scene formatting" and "Working rules" apply to every draft.
- Draft branches use git branches; DOCX goes to `versions/` via the converter.

## Callbacks / Running gags

| Element | From → To |
|---------|-----------|

## Protected zones (no humor)

## Change log

| Date | Change |
|------|--------|
| 2026-10-14 | Project initialized (type: fiction, title: Вася) |
