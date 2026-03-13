---
description: Start a new RP scene
allowed-tools: Read, Write, Glob
argument-hint: [premise or scenario description]
---

# Start a New Scene

Open a new roleplay scene based on the user's premise.

## Step 1: Load Context

1. Read `scene-partner/preferences.md` if it exists. If not, use sensible defaults (third-person limited, atmospheric prose, 3-6 paragraphs, match user pacing).
2. List character files in `scene-partner/characters/`.
3. Read all relevant character files — any characters the user mentions in their premise, or all characters if there are only 2-3.

## Step 2: Parse the Premise

The user provided: **$ARGUMENTS**

If the premise is empty or vague, ask the user what they have in mind. Even a mood or a single image is enough — e.g., "something tense," "a first meeting," "rain."

From the premise, determine:
- **Setting**: Where and when does this take place?
- **Characters present**: Who's in the scene? Which does the user play, which does Claude play?
- **Starting mood/situation**: What's the emotional or physical context?
- **Tone**: Does this override the default preferences?

If any characters mentioned don't have files yet, offer to create quick ones or improvise from context.

## Step 3: Write the Prologue

Open the scene with:
- **Atmospheric scene-setting**: Establish the location through sensory details. Don't over-explain — let the environment suggest the mood.
- **Character positioning**: Where are the characters physically? What are they doing when the scene opens?
- **Opening action or dialogue**: Claude's character(s) should do or say something that invites the user to respond. Give them something to react to.

Follow the user's preferred POV, prose style, and turn length from their preferences.

## Rules

- Stay in character from the first line. No meta-commentary about starting the scene.
- Don't write the user's character's actions or dialogue. Set the stage, play Claude's character(s), and hand it to the user.
- The prologue should end at a natural pause that invites the user's first turn.
- If the user specified a tone that differs from their default preferences, honor the scene-specific tone.
