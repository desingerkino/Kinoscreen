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
| 01 | scenes/01_metro.md | Act I | Вася у метро излагает «теорию покупки», спорит с Коляном на пиво, что возьмёт ботинки за семьсот | Draft |
| 02 | scenes/02_tamara.md | Act I | Вася «обыгрывает» Тамару в торге; пока он пересчитывает сдачу, коробку подменяют | Draft |
| 03 | scenes/03_luzha.md | Act II | Вскрытая коробка: плохие ботинки, подошва «открывает рот» в луже; пари он технически выиграл | Draft |
| 04 | scenes/04_vozvrat.md | Act II | Вася возвращается, Тамара обращает его же правила против него | Draft |
| 05 | scenes/05_kukhnya.md | Act II | Мама достаёт отцовские ботинки: «Как на тебя шили. А я не вру» | Draft |

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

Skills from script-doctor (`story-development`, `beat-sheet-planning`, `consistency-driven-drafting`, `scene-delegation`, `drafting-sprints`, `script-coverage`, `plot-hole-auditing`, `draft-branching`, `draft-locking`, `pre-submission-checklist`) describe one possible process: Story Bible, then beat sheet, then scene-by-scene drafting with acceptance criteria, then coverage notes. Use it when it helps; it is not obligatory and can be mixed with other skills. Commands: `/develop-story`, `/coverage`, `/submit-check`.

Where they disagree with this project, the project wins:

- Story Bible → `docs/script-doctor/story-bible.md`, beat sheet → `docs/script-doctor/beat-sheet.md`, coverage → `docs/script-doctor/coverage/` (as the skills say).
- Scenes are NOT written to `drafts/*.fountain`. They go to `scenes/NN_title.md` in the format above, and the scene table and change log in this file stay current.
- Fill the Project fields above (logline, genre, theme, characters) from the approved Story Bible.
- Format and AI-pattern rules in "Scene formatting" and "Working rules" apply to every draft.
- Draft branches use git branches; DOCX goes to `versions/` via the converter.

## How to use the skills

Skills are a toolbox, not a pipeline. Use them one after another or mixed together, whichever is more productive for the task in front of us. They complement each other: none has priority over another, and "mandatory", "always first" or "never skip" lines inside any skill (script-doctor especially) are not binding here.

1. **Pick by the problem, combine freely.** A dialogue fix may use `sw-dialogue`, `dialogue-craft` and `character-dialogue` at once; a new scene may start from the author's idea, from acceptance criteria, or from a character question. Take the useful part of each skill.
2. **Read the skill's SKILL.md before applying it** (and its `reference*.md` when depth is needed). Never apply a skill from the memory of its name. `sw-*` skills are written in Chinese: read them, answer in Russian.
3. **When two skills disagree**, say so in a sentence and choose what serves this scene and the author's intent, or ask the author. No skill overrides another by default.
4. **Match the weight of the task.** A one-line fix does not need a coverage pass. A big decision (structure, ending, who the hero is) deserves several skills and the author's input.
5. **The author's request decides the mode.** Wants a scene now: write it. Wants to talk through structure: do that. Missing information: ask one question at a time, not a list.
6. **Say what was applied** in one short line at the end ("Применил: sw-scene-craft + dialogue-craft"). No lectures about skills.
7. **Skip what is irrelevant:** series, sitcom, Chinese opera, Japanese/Korean/French and industry skills, unless asked. This is a fiction feature.
8. **Project rules in this file** (scene format, language, file locations, AI-pattern ban) beat any skill.

What each group is good for (suggestions, not stages):

| Task | Useful skills |
|---|---|
| Idea, logline, theme, Story Bible | `story-development`, `logline`, `theme-discovery`, `sw-premise-theme` |
| Characters and conflict | `sw-character-conflict`, `character-arcs`, `character-interview` |
| Structure and beat sheet | `beat-sheet-planning`, `sw-story-structure`, `story-structure`, `sw-genre-anatomy`, `sw-truby-anatomy` |
| Writing a scene | `consistency-driven-drafting`, `sw-scene-craft`, `scene-headings`, `action-description`, `drafting-sprints` |
| Dialogue | `sw-dialogue`, `dialogue-craft`, `character-dialogue` |
| Notes and diagnosis | `script-coverage`, `plot-hole-auditing`, `continuity-tracking`, `arc-check`, `story-check`, `scene-analysis`, `power-analysis` |
| Rewrite | `rewriting-methodology` plus the skill that matches the problem found |
| Experiments with structure | `draft-branching` (git branches) |
| Finishing and export | `pre-submission-checklist`, `draft-locking`, `title-page`, `page-estimation`, DOCX export from `screenplay-writer` |
| Stuck, second opinion | `sw-writers-room`, `chekhov-dramaturgy`, `sw-workflow` |

Text in the scenes always goes through `screenplay-writer` rules (format and `analytics/avoid-ai-writing-tells.md`).

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
| 2026-10-14 | Пробный черновик scenes 01–05 (Черкизон, 2002), ≈6 страниц; DOCX: versions/Vasya_v01.docx |
