---
description: Save the current RP session to a file
allowed-tools: Read, Write, Glob, Bash(date:*)
argument-hint: [title] [tags]
---

# Save Session

Save the current RP session as a formatted markdown file.

## Parse Arguments

The user provided: **$ARGUMENTS**

Expected format: `[title] [tags]` where tags are comma-separated (e.g., `Rooftop Standoff tension, action, rivalry`).

- If a title was given, use it.
- If no title was given, generate a short evocative one from the scene content (2-4 words).
- If tags were given, use them.
- If no tags were given, infer 3-5 tags from the scene's tone and themes.

## Compile the Session

Review the full conversation and assemble the session file. Include:

1. **Metadata header**:
   - Title
   - Date (today's date in YYYY-MM-DD format)
   - Characters involved (names and who played them)
   - Summary (1-2 sentences capturing the scene — enough to jog memory later, not a full recap)
   - Tags

2. **Scene content**:
   - Prologue (Claude's opening)
   - Each turn, clearly labeled with the character name
   - Epilogue if one was written

## Format

```markdown
# [Title]
**Date:** YYYY-MM-DD
**Characters:** [Name] (user), [Name] (Claude)
**Summary:** [Brief description]
**Tags:** tag1, tag2, tag3

---

## Prologue
[Opening narration]

## Turn 1
**[User's character]:** [User's input]
**[Claude's character]:** [Claude's response]

## Turn 2
...
```

## Save Location

Create `scene-partner/sessions/` if it doesn't exist. Save as:
```
scene-partner/sessions/YYYYMMDD_[Title in kebab-case].md
```

If a file with that name already exists, append a number (e.g., `_2`).

## Confirm

Tell the user the session was saved, show the title and tag line, and mention they can pick it back up later with `/resume`.
