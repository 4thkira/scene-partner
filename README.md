# Scene Partner

A turn-based roleplay and creative writing plugin for Claude. Create characters, define your writing style, and collaborate on scenes with Claude as your scene partner.

## Getting Started

1. **Run `/setup`** to configure your writing style — POV, prose style, pacing, and tone preferences.
2. **Run `/character`** to create your first character (and one for Claude to play).
3. **Run `/scene`** with a premise to start writing together.

## Commands

| Command | Description |
|---------|-------------|
| `/setup` | Guided setup for writing style, POV, pacing, and content preferences. |
| `/character [name]` | Create a new character or edit an existing one. Walks you through appearance, personality, voice, and more. |
| `/scene [premise]` | Start a new RP scene. Describe a setting, mood, or situation and Claude opens the scene in character. |
| `/save [title] [tags]` | Save the current session as a formatted markdown file with metadata and labeled turns. |
| `/resume [name]` | Resume a previously saved session. Lists available sessions if no name is given. |
| `/rewrite [direction]` | Rewrite Claude's last turn with a different tone (e.g., softer, funnier, more dialogue). |
| `/cast [character]` | Pull up a quick reference card for a character mid-scene. |

## How It Works

Scene Partner stores everything in a `scene-partner/` folder in your workspace:

- `preferences.md` — Your writing style choices
- `characters/` — Character files (one per character)
- `sessions/` — Saved RP sessions

Characters and preferences persist between sessions. You can edit character files directly as markdown, or use `/character` for a guided experience.

## Features

- **Flexible character roster** — 1v1 scenes or multi-character ensembles. You decide who plays whom.
- **Customizable writing style** — Choose your POV, prose style, turn length, and pacing. Change per-scene or set defaults.
- **Session management** — Save and resume scenes across conversations.
- **Mid-scene tools** — Rewrite turns that don't land right. Quick-reference characters without breaking flow.

## Tips

- You don't need to fill out every field when creating a character. Start minimal and add detail as they develop.
- `/rewrite` accepts natural language directions: "softer," "more sarcastic," "shorter," "surprise me."
- Your scene premise can be as detailed or vague as you like. Even just a mood works: `/scene something tense in the rain`.
- Characters grow over time. Edit their files to track arcs, new relationships, or changes.
