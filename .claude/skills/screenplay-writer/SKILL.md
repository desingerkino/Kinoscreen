---
name: screenplay-writer
description: Toolkit for writing and analyzing screenplays — feature films, TV pilots and series, and documentary AV-scripts (two-column VIDEO/AUDIO). Use when the user wants to start a screenplay project, write or rewrite a scene, split a draft into scenes, analyze structure, pacing, subtext or continuity, build a character sheet or bible, make a pitch or outline, check a script for AI-sounding writing, or export a script to DOCX. Triggers include сценарий, сцена, киносценарий, диалоги, логлайн, питч, персонаж, хронометраж, AV-скрипт, screenplay, scene, logline, beat sheet, script doctor.
---

# Screenplay Writer

Adapted for Claude web/desktop from the open-source `claude-screenplay-plugin` by Aslan Suleimenov (MIT, see `LICENSE`). The original is a Claude Code plugin driven by slash commands; here the same commands are triggered by plain requests.

All reference files live next to this file. Paths below are relative to this skill's folder.

## How it works

A screenplay project is a folder of plain files in the working directory:

```
CLAUDE.md                 project card: type, genre, logline, characters, scene table, rules, change log
scenes/NN_title.md        one file per scene (fiction) or block (documentary)
analytics/                reports, compass_artifact.md, character bible, pitch
versions/                 DOCX exports
```

`CLAUDE.md` here is just the project card (name kept for compatibility with the plugin's commands). Every command reads it first.

The project exists only in the current chat's workspace. Therefore:
- If the user attaches a project (zip, folder files, or a draft), unpack it into the working directory and continue from there.
- At the end of a work session, or when the user asks, send the updated files (or a zip of the project) with SendUserFile so nothing is lost. Tell the user to attach that zip at the start of the next chat to continue.

## Language

Reply in the language the user writes in. Write scene text in the project's working language (ask once if unclear, record it in the project card). The template says "Working language: English"; replace it with the real language when creating the card. `references/avoid-ai-writing-tells.md` covers both English and Russian AI-writing patterns.

## Commands → plain requests

When the user asks for one of these things, read the matching file in `references/commands/` and follow it. Where a file says `AskUserQuestion`, just ask in chat, one question at a time. Where it says "Save nothing, output only", do exactly that.

| User wants | Read |
|---|---|
| Start a project (optionally from a draft) | `commands/startproject.md` (card template: `references/project-CLAUDE-template.md`) |
| Split a draft into scenes | `commands/split.md` |
| Genre reference for this project (web research) | `commands/compass.md` |
| New scene or block | `commands/new-scene.md` |
| Rewrite a scene by notes | `commands/rewrite.md` |
| Analyze one scene or the whole script | `commands/analyze.md` |
| Character sheet | `commands/character-sheet.md` |
| Continuity check | `commands/continuity.md` |
| Research a topic for the script | `commands/research.md` |
| Beat sheet / outline | `commands/outline.md` |
| Renumber, delete, merge scenes | `commands/renumber.md`, `delete-scene.md`, `merge.md` |
| Stats: runtime, dialogue/action ratio | `commands/stats.md` |
| Export to DOCX | `commands/compile.md` |
| Full audit of the script | `commands/full-check.md` |
| Check that project type is set | `commands/type-check.md` |

## Agents → focused passes

`references/agents/` holds specialist passes. Run them when the user asks for the matching job, reading the agent file first and following it.

- Pipelines: `draft-polish.md` (analysis → scenes → logic → spelling → AI patterns), `script-doctor.md`, `proofread.md`
- Documents: `character-bible.md`, `pitch.md`, `unico.md` (UNICO starter pack)
- Audit checkers (used by `/full-check`, also usable one at a time): `action-line-checker`, `timeline-checker`, `structure-checker`, `scene-balance-checker`, `dialogue-ratio-checker`, `scene-continuity-checker`, `plot-thread-checker`, `tone-checker`, `character-ooc-checker`, `value-shift-checker`, `scene-hook-checker`, `scene-economy-checker`, `subtext-checker`, `visual-storytelling-checker`, `story-engine-checker`, `pilot-checker`; `deep-check.md` orchestrates them in order and builds the dashboard.

Run the passes one after another yourself. Use the Agent tool only if the user explicitly asks for subagents; a full audit is long, so offer to run a subset (for example scenes 1–20) first.

## Reference library

- `references/compass/INDEX.md`: map of genre theory. Fiction genre files (26), documentary types (7), character craft (`character/`: archetypes, wound-and-want, voice, antagonist), series and short-form formats (`format/`). Genre structural contracts, each with "Must happen" and "Forbidden", are in `compass/fiction/genre-mechanics.md` and `compass/doc/genre-mechanics.md`. Read only the sections for the project's genre.
- `references/avoid-ai-writing-tells.md`: read before writing or rewriting any scene. It overrides your default style.
- Soviet and Russian cinema is a valid reference set; the compass includes a cross-reference by genre.

## Hard rules that apply to every scene

- Write only what the camera sees: actions, not emotions. Strong verbs, specific details.
- Fiction format: `# Scene NN: Title`, plain-text slug line (`INT. PLACE — DAY`), character names in plain CAPS, one blank line between blocks, none between name and dialogue, no bold in scene files, no `CUT TO:` / `FADE OUT.`. Details in `scripts/converter_MD_DOCX/README.md`.
- Documentary format: `# Block NN: Title` plus a `| VIDEO | AUDIO |` table with V/O, SOT, SUPER, NAT SOUND, B-ROLL markers.
- Do not renumber files without an explicit request; when renumbering, use two-phase renames through temp names.
- After every added or changed scene, update the scene table and change log in the project card.
- After writing a scene, re-check the format and the AI-writing patterns before showing it. The plugin did this with hooks; here it is a manual step.

## DOCX export

1. Copy `scripts/converter_MD_DOCX/` into the project folder (the plugin does the same in `/startproject`).
2. `pip install python-docx --break-system-packages` if the module is missing (the package is `python-docx`, not `docx`).
3. From the project root run `python converter_MD_DOCX/md_to_docx.py [name]`. Output goes to `versions/<name>_vNN.docx`.
4. Deliver the DOCX with SendUserFile.

`pitch_to_docx.py` and `unico_to_docx.py` in the same folder export the pitch and UNICO documents.

Project type is read from the `**Type:**` line of the project card (`fiction` or `documentary`); the Russian `**Тип:**` (`художественный` / `документальный`) also works.
