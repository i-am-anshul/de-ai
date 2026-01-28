# de-ai

A Claude Code skill that removes AI-generated writing patterns from text, making it sound natural and human-written.

## What it does

Detects and fixes common AI writing patterns:

- **Banned words** - delve, leverage, tapestry, utilize, etc.
- **Inflated significance** - "pivotal moment", "testament to", "rich history"
- **Promotional fluff** - "vibrant", "nestled", "breathtaking", "renowned"
- **Superficial analysis** - overuse of -ing words like "highlighting", "showcasing"
- **Vague attributions** - "experts say", "industry reports suggest"
- **Formatting tics** - em dash overuse, unnecessary boldface
- **Rule of three** - forced triple patterns ("X, Y, and Z")
- **Sycophantic tone** - "Great question!", "Excellent point!"
- **Chatbot artifacts** - "I hope this helps!", "Feel free to ask"

Also provides guidance on adding soul to writing: varied rhythm, real opinions, specific details.

## Installation

1. Clone this repo into your Claude skills directory:
   ```bash
   mkdir -p ~/.claude/skills
   git clone https://github.com/i-am-anshul/de-ai.git ~/.claude/skills/de-ai
   ```

2. Create the marketplace config at `~/.claude/skills/.claude-plugin/marketplace.json`:
   ```json
   {
     "name": "local-skills",
     "skills": {
       "de-ai": {
         "description": "Remove AI writing patterns from text",
         "version": "1.0.0",
         "path": "de-ai"
       }
     }
   }
   ```

3. Add to your Claude settings (`~/.claude/settings.json`):
   ```json
   {
     "enabledPlugins": {
       "de-ai@local-skills": true
     },
     "extraKnownMarketplaces": {
       "local-skills": {
         "source": {
           "source": "directory",
           "path": "~/.claude/skills"
         }
       }
     }
   }
   ```

4. Restart Claude Code.

## Usage

The skill activates automatically when you:
- Edit or review text for AI patterns
- Write resumes, cover letters, LinkedIn posts, or professional content
- Ask Claude to make text "sound more human" or "less AI-like"

You can also invoke it explicitly:
- "Use de-ai to clean up this paragraph"
- "Apply de-ai rules to my cover letter"

## Sources

- [Wikipedia: Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing)
