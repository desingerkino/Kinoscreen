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

## How to use the skills (mandatory)

There are many skills and they overlap. Using all of them at once gives mush. Rules:

1. **One driver per stage, plus at most 2–3 helpers.** The driver sets the process; helpers only add craft knowledge for a specific problem.
2. **Read the skill's SKILL.md before applying it** (and its `reference*.md` when the problem needs depth). Never apply a skill from memory of its name. Skills marked `sw-*` are written in Chinese: read them, answer in Russian.
3. **Follow stage order. Do not skip ahead.** No pages until the Story Bible is approved; no scene is drafted until its acceptance criteria are written.
4. **Approval gates.** After each stage show the result in short pieces and wait for the author's OK. The author decides; skills only propose.
5. **One question at a time** while developing the story. No lists of ten questions.
6. **Say what was applied**, in one short line at the end of the answer ("Применил: story-development + sw-premise-theme"). No lectures about the skills.
7. **Never use** the series, sitcom, Chinese opera, Japanese/Korean/French and industry skills for this film unless the author asks. This is a fiction feature.
8. Project rules in this file (scene format, language, file locations, AI-pattern ban) beat any skill.

| Stage | Driver | Helpers (pick only what the problem needs) |
|---|---|---|
| 1. Idea → Story Bible (logline, theme, characters, world, tone) | `story-development` | `logline`, `theme-discovery`, `sw-premise-theme`, `sw-character-conflict`, `character-arcs` |
| 2. Structure → beat sheet with acceptance criteria | `beat-sheet-planning` | `sw-story-structure`, `story-structure`, `sw-genre-anatomy`, `sw-truby-anatomy` |
| 3. Drafting a scene | `consistency-driven-drafting` (criteria → draft → polish); long runs: `drafting-sprints` | `sw-scene-craft`, `scene-headings`, `action-description`, `sw-dialogue`, `dialogue-craft`, `character-dialogue` |
| 4. Notes and review | `script-coverage` | `plot-hole-auditing`, `continuity-tracking`, `arc-check`, `story-check`, `scene-analysis`, `power-analysis` |
| 5. Rewrite | `rewriting-methodology` | the helper that matches the problem found in stage 4; `screenplay-writer` rewrite command |
| 6. Structural experiments | `draft-branching` | git branches |
| 7. Lock and export | `pre-submission-checklist` → `draft-locking` | `screenplay-writer` DOCX export, `title-page`, `page-estimation` |

Also always for writing text: `screenplay-writer` skill (format and AI-pattern rules, `analytics/avoid-ai-writing-tells.md`).

Stuck or want a second opinion on a hard decision: `sw-writers-room`, `chekhov-dramaturgy`, `sw-workflow` (project state).

## Story Systems skills

24 skills from story-systems-template (`logline`, `story-structure`, `character-arcs`, `dialogue-craft`, `continuity-tracking`, `rewriting-methodology`, `synopsis`, `pitch-worksheet`, `power-analysis`, `scene-analysis` and others) are installed as reference craft. They assume Fountain files and a `story-bible/` layout. Here the scene format stays Markdown in `scenes/` (see "Scene formatting"); use `fountain-syntax`, `format-export` and `title-page` only if a Fountain/PDF export is requested.

## Callbacks / Running gags

| Element | From → To |
|---------|-----------|

## Protected zones (no humor)

## Change log

| Date | Change |
|------|--------|
| 2026-10-14 | Project initialized (type: fiction, title: Вася) |
