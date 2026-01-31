# Claude Verbs Project

This repository contains custom verb themes for Claude Code's status line spinner.

## Project Structure

```
claude-verbs/
├── themes/                    # All verb themes
│   └── {theme-name}/
│       └── {theme-name}.json  # Theme configuration
├── README.md                  # Main documentation with theme count
└── .claude/                   # Claude Code configuration
```

## Theme File Format

Each theme is a JSON file with this structure:

```json
{
  "spinnerVerbs": {
    "mode": "replace",
    "verbs": [
      "Verb One-ing",
      "Verb Two-ing",
      "Another Action"
    ]
  }
}
```

### Verb Guidelines

- Use **present participle form** (ending in -ing)
- Verbs should read naturally as "Claude is [verb] for 30s"
- Aim for **35-45 verbs** per theme
- Reference catchphrases, quotes, and iconic moments from the source material
- Be creative with the -ing suffix (e.g., "YEEEAAAHHH-ing", "What's Going On-ing")

## Critical: Keeping Count in Sync

**ALWAYS update the theme count in README.md when adding or removing themes.**

The count appears in the first section:
```markdown
**35 themes** | Custom verb themes...
```

To get the current count:
```bash
ls -1 themes | wc -l
```

## Adding a New Theme

1. Create directory: `themes/{theme-name}/`
2. Create JSON file: `themes/{theme-name}/{theme-name}.json`
3. Add entry to README.md in the Themes section (alphabetical by category)
4. **Update the theme count** at the top of README.md
5. Commit with message format: `Add {N} new verb themes`

## Theme Entry Format for README

```markdown
### [Theme Name](themes/theme-name/)

> "Iconic quote from the source."

Sample Verb One, Sample Verb Two, Sample Verb Three, Sample Verb Four, Sample Verb Five...
```

## Validation Checklist

Before committing new themes:

- [ ] JSON is valid (no trailing commas, proper quotes)
- [ ] Directory name matches JSON filename (kebab-case)
- [ ] 35-45 verbs included
- [ ] Verbs are in present participle form
- [ ] README.md theme count updated
- [ ] README.md entry added for each new theme
- [ ] Commit message follows format

## Commands

```bash
# Count themes
ls -1 themes | wc -l

# Validate JSON syntax
for f in themes/*/*.json; do python3 -m json.tool "$f" > /dev/null && echo "OK: $f" || echo "FAIL: $f"; done

# List all themes
ls -1 themes

# Count verbs in a theme
jq '.spinnerVerbs.verbs | length' themes/{theme-name}/{theme-name}.json
```
