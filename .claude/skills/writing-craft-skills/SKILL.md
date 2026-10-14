---
name: writing-craft-skills
description: >
  Create new personal craft skills to codify the writer's techniques and preferences.
  Activates when: the writer wants to document their approach to a specific aspect of
  screenwriting (action sequences, exposition, dialogue style, etc.) or when a
  repeating pattern in the writer's process should be formalized into a reusable skill.
---

# Writing Craft Skills

Script Doctor's built-in skills cover the process of screenwriting — how to develop a story, plan it, draft it, review it. But every writer also has personal craft techniques: how they write action sequences, how they handle exposition, their approach to opening images, their philosophy on voiceover.

This skill helps the writer codify those personal techniques into reusable skills that integrate with the Script Doctor workflow.

## When to Create a Craft Skill

- The writer has a specific technique they use repeatedly ("I always open with an image that mirrors the final image")
- A coverage note keeps recurring and the fix is always the same ("My exposition dumps always improve when I convert them to conflict scenes")
- The writer discovers a principle during drafting that they want to apply consistently
- The writer wants to document their approach to a genre-specific challenge (writing horror scares, comedy timing, courtroom procedure, etc.)

## Craft Skill Structure

Each craft skill is a SKILL.md file in its own directory:

```
skills/
├── [craft-skill-name]/
│   └── SKILL.md
```

The SKILL.md follows this format:

```markdown
---
name: [skill-name]
description: >
  [When this skill applies and what it does. Be specific about trigger conditions.]
---

# [Skill Name]

## When to Use
[Specific situations where this technique applies]

## The Technique
[Step-by-step description of the technique. Be concrete, not abstract.
Include examples from the writer's own work if available.]

## Verification
[How to check that the technique was applied correctly]

## Anti-patterns
[Common mistakes when applying this technique]
```

## Example Craft Skills

### Writing Action Sequences
A skill that describes how to write visually coherent, spatially clear action sequences: short sentences, new paragraph for each new shot, geography established before chaos, character stakes embedded in the physical action.

### Exposition Through Conflict
A skill for converting exposition dumps into scenes where the information emerges through disagreement, interrogation, or discovery — never through characters telling each other things they already know.

### Opening and Closing Images
A skill for the writer's approach to bookending a script with mirrored images that show the thematic change (or tragic lack of change) in visual form.

### Comedy Scene Structure
A skill for premise-escalation-blow comedy structure: establish the comic premise, escalate it through 3-4 beats with increasing absurdity, land the blow (the biggest laugh), and get out.

### Writing Silence
A skill for scenes where the most powerful moments happen without dialogue — using screen direction, physical behavior, and environmental sound to carry emotional weight.

### Dialogue Rhythm
A skill for the writer's specific dialogue preferences — average speech length, use of interruptions, how they handle overlapping dialogue, their approach to silence within dialogue scenes.

## Creating a New Craft Skill

1. **Name it specifically.** "Writing Better" is not a skill. "Converting Exposition to Conflict Scenes" is a skill.
2. **Describe the trigger.** When should this skill activate? Be specific about the drafting situation.
3. **Make it concrete.** Include do/don't examples. Abstract principles ("make it visual") are less useful than concrete techniques ("replace any sentence starting with 'feels' with a physical action").
4. **Include verification.** How does the writer know the technique was applied correctly?
5. **Document anti-patterns.** What does it look like when this technique goes wrong?

## Rules

- **Craft skills are personal.** They reflect the writer's voice and preferences, not universal rules. What works for one writer's action sequences won't work for another's.
- **Craft skills are optional.** Built-in Script Doctor skills (story development, coverage, etc.) are mandatory workflows. Craft skills are techniques the writer *chooses* to apply.
- **Craft skills evolve.** As the writer's craft develops, their skills should be revised. A technique that worked for early scripts may be superseded by a better approach.
- **Keep them short.** A craft skill that's longer than 2 pages is probably trying to do too much. Split it into multiple skills.

## Save Location

Personal craft skills live in: `skills/craft/[skill-name]/SKILL.md`

These are the writer's own tools. They can be shared with collaborators but they're not part of the core Script Doctor methodology.
