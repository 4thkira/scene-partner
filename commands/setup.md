---
description: Set up your writing style and RP preferences
allowed-tools: Read, Write, Glob, AskUserQuestion
---

# Guided RP Setup

Walk the user through configuring their roleplay preferences. This creates a `preferences.md` file in `scene-partner/` that all other commands will reference.

## Step 1: Check for existing preferences

Look for `scene-partner/preferences.md` in the user's workspace. If it exists, read it and ask whether they want to update it or start fresh.

## Step 2: Ask about writing style

Use AskUserQuestion to walk through these choices one at a time. Keep the tone conversational and welcoming — this should feel like a creative partner getting to know them, not a form.

**Questions to ask (in order):**

1. **Point of view**: "What perspective do you like your scenes written in?"
   - Third-person limited (close to one character's perspective)
   - Third-person omniscient (narrator sees everything)
   - Second-person ("you walk into the room...")
   - First-person (narrator is the character)

2. **Prose style**: "What kind of writing style fits your scenes best?"
   - Atmospheric and sensory — rich descriptions, textures, the weight of a room
   - Fast-paced and punchy — short sentences, momentum, action-forward
   - Literary and introspective — internal monologue, metaphor, emotional depth
   - Casual and conversational — natural, relaxed, like telling a story to a friend

3. **Turn length**: "How long should each response roughly be?"
   - Short (1-3 paragraphs) — quick back-and-forth
   - Medium (3-6 paragraphs) — balanced detail and pacing
   - Long (5-8+ paragraphs) — immersive, detailed scenes

4. **Pacing**: "Should I match your energy, or keep a consistent style?"
   - Match me — if I write short, respond short; if I go detailed, follow
   - Stay consistent — keep the same style regardless of my turn length

5. **Session mode**: "How do you usually want characters set up?"
   - 1v1 — one character each, focused dynamic
   - Ensemble — multiple characters, I play some and you play the rest
   - Flexible — decide per scene

6. **Tone**: "Give me a few words that describe the vibe you usually go for. Examples: dark and intimate, lighthearted and funny, tense and dramatic, slow-burn romance, action-heavy, horror-tinged..."
   - (Free text response)

7. **Boundaries** (optional): "Anything you want me to always avoid or always lean into? No wrong answers — skip if you'd rather set this per scene."
   - (Free text response)

## Step 3: Save preferences

Create the `scene-partner/` directory if it doesn't exist. Write the preferences to `scene-partner/preferences.md` in this format:

```markdown
# Scene Partner Preferences
**Last updated:** YYYY-MM-DD

## Writing Style
- **POV:** [their choice]
- **Prose style:** [their choice]
- **Turn length:** [their choice]
- **Pacing:** [their choice]

## Session Mode
[their choice]

## Tone
[their keywords]

## Boundaries
[their notes, or "Set per scene"]
```

## Step 4: Confirm

Show the user their saved preferences in a brief summary and let them know they can run `/setup` again anytime to change things. Suggest they try `/character` next to create their first character.
