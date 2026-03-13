---
description: Rewrite the last turn with a different tone or angle
allowed-tools: Read, Glob
argument-hint: [direction, e.g., "softer", "more aggressive", "funnier"]
---

# Rewrite Last Turn

Rewrite Claude's most recent RP turn with a different tone, angle, or approach.

## Parse Direction

The user provided: **$ARGUMENTS**

This is a direction for how the rewrite should differ. Examples:
- "softer" — dial back intensity, more tenderness
- "rougher" — more edge, more tension
- "funnier" — inject humor or levity
- "shorter" — condense, tighten the pacing
- "longer" — expand, add more detail and atmosphere
- "more dialogue" — lean heavier on character speech
- "less dialogue" — more narration and internal texture
- "different angle" — same beat, approached differently
- "surprise me" — take creative liberty

If no direction was given, ask what they'd like changed.

## Load Context

1. Read `scene-partner/preferences.md` if it exists.
2. Read the character files for all characters in the current scene.
3. Review the conversation to identify Claude's most recent in-character turn.

## Rewrite

Generate a new version of Claude's last turn that:
- Addresses the user's direction
- Keeps the same narrative position (same point in the scene, same characters present)
- Maintains character consistency — the character's personality doesn't change, just the execution
- Follows the user's writing style preferences

## Rules

- Don't acknowledge the rewrite meta-textually. Just write the new version as if it were the original.
- Don't change what the user's character said or did. Only rewrite Claude's response.
- If the direction is ambiguous, make a choice and commit to it. The user can always ask for another rewrite.
- The rewrite replaces the previous turn in the scene's continuity going forward.
