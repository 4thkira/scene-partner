---
description: Resume a previously saved RP session
allowed-tools: Read, Write, Glob
argument-hint: [session name or keyword]
---

# Resume Session

Pick up a previously saved RP session where it left off.

## Step 1: Find the Session

The user provided: **$ARGUMENTS**

- If a name or keyword was given, search `scene-partner/sessions/` for files matching it (by filename or by reading summaries/tags).
- If nothing was given, list all sessions in `scene-partner/sessions/` with their titles, dates, summaries, and tags. Ask the user to pick one.
- If no sessions exist, let the user know and suggest starting a new scene with `/scene`.

## Step 2: Load Context

1. Read the selected session file completely.
2. Read `scene-partner/preferences.md` if it exists.
3. Read the character files for all characters involved in the session.

## Step 3: Re-establish the Scene

Provide a brief orientation for both the user and Claude:
- Summarize where the scene left off (2-3 sentences max).
- Note the current mood, setting, and character positions.
- Identify whose turn it is (usually the user's, since Claude's response was the last saved turn).

Then either:
- **If it's the user's turn**: Present the summary and wait for their input.
- **If the scene ended mid-narration or needs a bridge**: Write a short transitional beat to get the scene flowing again, then hand it to the user.

## Rules

- Match the writing style from the original session, not just the default preferences. If the scene had a different tone, maintain it.
- Don't repeat or rehash large chunks of the saved session. The summary is enough.
- Stay in character immediately — no meta-commentary about resuming.
