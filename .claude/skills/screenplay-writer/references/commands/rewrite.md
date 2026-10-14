Rewrite a scene/block based on notes. Argument: $ARGUMENTS (scene number and notes, e.g. `05 sharpen conflict, cut exposition`).

## Step 1 — Preparation

1. Read CLAUDE.md — project type, characters, structure, Seed
2. Find the file in scenes/ by number
3. Read the scene in full
4. Read analytics/compass_artifact.md if it exists — genre systems
5. Read `references/avoid-ai-writing-tells.md` — forbidden patterns
6. Read the genre entry from the structural contracts:
   - Fiction: `references/compass/fiction/genre-mechanics.md`
   - Documentary: `references/compass/doc/genre-mechanics.md`

## Step 2 — Analyze the notes

Parse the notes from the argument. Common requests:
- "sharpen conflict" — raise stakes, add opposition
- "cut exposition" — show through action, not narration
- "trim" — remove repetition, get to the point
- "add subtext" — what goes unsaid
- "rewrite dialogue" — make it more alive, more individual
- Any other specific notes

## Step 3 — Rewrite

Rewrite the scene taking into account:
- The user's notes (top priority)
- Genre systems from compass_artifact.md
- Genre structural contract — don't violate **Forbidden**, serve **Must happen** where possible
- Forbidden AI patterns from avoid-ai-writing-tells.md
- Scene format for the project type (fiction/documentary)
- Seed from CLAUDE.md — if the scene can carry or echo the core image/metaphor without forcing it, do it

Save to the same file.

## Step 4 — Show the diff

Output the key changes: what was removed, what was added, what was reworked.

## Step 5 — Update CLAUDE.md

- Add an entry to "Change log"
- If the scene's key event changed — update the scenes table
