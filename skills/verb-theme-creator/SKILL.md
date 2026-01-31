---
name: verb-theme-creator
description: Use when creating new Claude Code spinner verb themes for the jackson-verbs repository. Guides brainstorming verbs around a theme, formatting them as natural action verbs, and generating the required file structure (README.md, theme.md, theme.json).
---

# Verb Theme Creator

Create themed verb packs for Claude Code's status line spinner.

## Overview

Claude Code displays verbs like "Thinking..." while processing. This skill guides creation of themed verb collections users can add to their `~/.claude/settings.json`.

## When to Use

- User wants to create a new verb theme
- User asks about adding themes to jackson-verbs
- User wants to customize Claude Code spinner verbs

## Theme Requirements

**Verb Count:** 30-45 verbs per theme

**Verb Format:** Present participles (action verbs ending in -ing) that:
- Read naturally with "for 30s" appended (e.g., "Channeling the Force for 30s")
- Capture the theme's essence through actions, not raw quotes
- Reframe famous quotes into action format

**Reframing Examples:**
| Raw Quote | Action Verb |
|-----------|-------------|
| "Do or do not" | Trying Not (There is No Try) |
| "Say what again" | Asking What Again |
| "Whatcha gonna do" | Asking Whatcha Gonna Do |

## File Structure

Each theme requires three files in `themes/[theme-name]/`:

```
themes/theme-name/
├── README.md           # Quick intro + sample verbs + file links
├── theme-name.md       # Full verb list with reference table + JSON block
└── theme-name.json     # Raw JSON config for copy/curl
```

## Creation Process

### 1. Understand the Theme

Ask clarifying questions:
- What's the source material? (movies, person, franchise, era)
- What's the vibe? (serious, comedic, nostalgic, intense)
- Any specific references to include or avoid?

### 2. Brainstorm Raw Material

List 50+ potential references:
- Catchphrases and quotes
- Character actions
- Iconic moments
- Running jokes
- Signature moves/behaviors

### 3. Convert to Action Verbs

Transform each reference into a present participle that:
- Starts with an -ing verb
- Reads naturally as a status message
- Keeps the reference recognizable

### 4. Curate to 30-45

Select the strongest verbs:
- Mix of well-known and deep-cut references
- Variety in verb length (short punchy + longer descriptive)
- No repetitive patterns

### 5. Create Files

**theme-name.json:**
```json
{
  "spinnerVerbs": {
    "mode": "replace",
    "verbs": [
      "Verb One",
      "Verb Two"
    ]
  }
}
```

**theme-name.md:**
```markdown
# Theme Name Verbs

> "Iconic quote from theme" - Attribution

Brief theme description.

## The Verbs

| Verb | Reference |
|------|-----------|
| Verb One | Source/context |
| Verb Two | Source/context |

## Quick Copy

\`\`\`json
{
  "spinnerVerbs": {
    "mode": "replace",
    "verbs": [...]
  }
}
\`\`\`
```

**README.md:**
```markdown
# Theme Name

> "Iconic quote"

Brief description. [X] verbs of [theme essence].

**Sample verbs:** Verb One, Verb Two, Verb Three...

## Files

- [theme-name.md](theme-name.md) - Full verb list with references
- [theme-name.json](theme-name.json) - Raw JSON for your config
```

## Quality Checklist

- [ ] 30-45 verbs total
- [ ] All verbs are present participles (-ing)
- [ ] Verbs read naturally with "for Xs" appended
- [ ] Reference table explains each verb's origin
- [ ] Mix of famous and deep-cut references
- [ ] JSON is valid and properly formatted
- [ ] All three files created in correct structure

## Common Mistakes

| Mistake | Fix |
|---------|-----|
| Forced -ing ("Do or Do Not-ing") | Reframe as action ("Trying Not") |
| Raw quotes as verbs | Convert to action format |
| Too many similar verbs | Ensure variety |
| Missing references | Add context for each verb |
| Under 30 verbs | Brainstorm more source material |
