# Ric Flair Theme

WOOO! The Nature Boy has arrived in your terminal. This theme transforms your Claude Code spinner into a sixteen-time world champion of style and swagger.

## Sample Verbs

- **WOOO-ing** - The legendary cry
- **Stylin' and Profilin'** - The Nature Boy lifestyle
- **Limousine Ridin'** - First class travel only
- **Locking in the Figure Four** - The signature submission
- **Dirtiest Player Schemin'** - Always working an angle

## Files

- [ric-flair.json](./ric-flair.json) - JSON configuration (40 verbs)
- [ric-flair.md](./ric-flair.md) - Full documentation with verb references

## Usage

```bash
claude config set --project spinnerVerbs "$(cat ric-flair.json | jq -c '.spinnerVerbs')"
```

Whether you like it or not, your terminal is about to become the main event. WOOO!
