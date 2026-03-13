---
description: Create or edit a character for roleplay
allowed-tools: Read, Write, Glob, AskUserQuestion
argument-hint: [character name]
---

# Character Creation & Editing

Guide the user through creating a new character or editing an existing one.

## Check Arguments

The user provided: **$ARGUMENTS**

- If a name was given, check if `scene-partner/characters/[name].md` exists.
  - If it exists, read it and ask what they want to change.
  - If it doesn't exist, start creating a new character with that name.
- If no name was given, list existing characters from `scene-partner/characters/` and ask whether they want to create a new one or edit an existing one.

## Creating a New Character

Read the character template from `${CLAUDE_PLUGIN_ROOT}/skills/rp-engine/references/character-template.md` for the full structure and question flow.

Walk through character creation conversationally using AskUserQuestion where appropriate. Ask questions one or two at a time — don't dump the whole template at once.

**Required fields** (must ask):
1. Name and role
2. Who plays them (user or Claude)
3. Appearance (at least 2-3 details)
4. Core personality
5. Voice and speech patterns

**Optional fields** (offer but don't push):
6. Background
7. Abilities / skills
8. Dynamics with other characters
9. Notes

After gathering responses, assemble the character file and show it to the user for review. Ask if they want to adjust anything before saving.

## Saving

Create `scene-partner/characters/` if it doesn't exist. Save as `scene-partner/characters/[kebab-case-name].md`.

The filename should be the character's name in kebab-case (e.g., "Detective Voss" becomes `detective-voss.md`).

## Editing an Existing Character

Read the existing file, show the current content, and ask what they want to change. Apply the edits and show the updated version for confirmation before saving.

## After Saving

Confirm the character was saved and suggest next steps:
- Create another character with `/character`
- Start a scene with `/scene`
- Set up preferences with `/setup` if they haven't yet
