# de-ai Skill

Remove AI writing patterns from text. Make your writing sound human.

## What it does

de-ai detects and fixes common AI-generated writing patterns:
- Banned words (delve, leverage, tapestry, etc.)
- Inflated significance ("pivotal moment", "testament to")
- Promotional language ("vibrant", "nestled", "breathtaking")
- Superficial -ing analyses ("highlighting", "showcasing")
- Vague attributions ("experts say", "industry reports")
- Em dash and boldface overuse
- Rule of three patterns
- Sycophantic tone ("Great question!")
- Chatbot artifacts ("I hope this helps!")

It also teaches how to add soul: varied rhythm, opinions, specificity.

## Installation (already done)

The skill has been installed globally with this structure:

```
~/.claude/skills/
├── .claude-plugin/
│   └── marketplace.json    # Registers skills as a local marketplace
└── de-ai/
    ├── SKILL.md            # Main skill instructions
    └── README.md           # This file
```

Settings added to `~/.claude/settings.json`:
```json
{
  "enabledPlugins": {
    "de-ai@local-skills": true
  },
  "extraKnownMarketplaces": {
    "local-skills": {
      "source": {
        "source": "directory",
        "path": "/Users/Anshul/.claude/skills"
      }
    }
  }
}
```

## Usage

The skill triggers automatically when Claude detects you're:
- Editing or reviewing text for AI patterns
- Writing resumes, cover letters, or professional content
- Asking to make text "sound more human" or "less AI"

You can also explicitly reference the skill:
- "Use de-ai to clean up this text"
- "Apply de-ai rules to my cover letter"

## Adding more skills

To add more custom skills to this local marketplace:

1. Create a new skill folder in `~/.claude/skills/` (e.g., `my-skill/`)
2. Add a `SKILL.md` with proper frontmatter
3. Register it in `~/.claude/skills/.claude-plugin/marketplace.json`
4. Enable it in settings: `"my-skill@local-skills": true`

## Source

Based on:
- [Wikipedia: Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing)
- Custom Rules.md writing guidelines
