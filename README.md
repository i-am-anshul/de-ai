# de-ai

**Make AI-generated text sound human.**

A Claude Code plugin that detects and removes AI writing patterns from any text—resumes, cover letters, LinkedIn posts, documentation, emails, articles.

## Install

```bash
/plugin marketplace add i-am-anshul/de-ai
/plugin install de-ai
```

Works on **Windows**, **macOS**, and **Linux**. Requires [Claude Code](https://claude.ai/code).

## Before & After

**Before** (obvious AI):
> Delve into this comprehensive guide that unlocks the transformative power of effective communication. In the fast-paced world of modern business, leveraging these groundbreaking insights will elevate your professional journey.

**After** (human):
> This guide covers how to communicate clearly at work. Here's what actually helps.

## What It Catches

| Pattern | Example | Fix |
|---------|---------|-----|
| **Buzzwords** | delve, leverage, unlock, elevate | Use plain words |
| **Hype phrases** | "transformative power", "game-changer" | State the actual change |
| **Filler** | "In the fast-paced world of..." | Delete |
| **Vague claims** | "Experts say..." | Name the source or remove |
| **Promotional fluff** | vibrant, nestled, breathtaking | Use neutral language |
| **Sycophancy** | "Great question!" | Remove |
| **Chatbot artifacts** | "I hope this helps!" | Remove |
| **Em dash abuse** | multiple em-dashes per sentence | Use commas, periods |
| **Rule of three** | forced X, Y, and Z patterns | Use actual count needed |

See [SKILL.md](SKILL.md) for the complete detection rules and banned word list.

## Usage

The skill activates automatically when you:
- Ask Claude to edit or review text
- Write professional content (resumes, cover letters, LinkedIn)
- Request to make something "sound more human" or "less AI"

Or invoke directly:
```
Use de-ai on this paragraph
Apply de-ai to my cover letter
```

## Why This Exists

AI-generated text has tells. Recruiters spot them. Editors spot them. Readers spot them.

This plugin embeds the detection rules from [Wikipedia's "Signs of AI writing"](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing) plus additional patterns into Claude's workflow, so your text passes the human test.

## Keywords

`ai-writing-detection` `remove-ai-patterns` `humanize-text` `claude-code-plugin` `chatgpt-detection` `ai-content-detector` `writing-assistant` `deai`

## License

MIT
