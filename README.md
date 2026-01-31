# Jackson Verbs

Custom verb themes for Claude Code's status line. Make your AI think with style.

## What's This?

Claude Code shows verbs like "Thinking..." while it works. This repo has themed verb packs you can drop into your config for a more entertaining experience.

## Installation

Add to `~/.claude/settings.json`:

```json
{
  "spinnerVerbs": {
    "mode": "replace",
    "verbs": ["Your", "Verbs", "Here"]
  }
}
```

Or use `"mode": "append"` to mix with the defaults.

## Themes

### [Star Wars](themes/star-wars/)

> A long time ago in a galaxy far, far away... Claude was processing.

Channeling the Force, Making the Kessel Run, Executing Order 66, Taking the High Ground, This is the Waying...

### [Samuel L. Jackson](themes/samuel-l-jackson/)

> "English, motherfucker, do you speak it?"

Demanding English Motherfucker, Tasting Big Kahuna Burgers, Striking with Great Vengeance, Staring Motherfuckerly, Not Granting Rank of Master...

### [Hulk Hogan](themes/hulk-hogan/)

> "Whatcha gonna do when Hulkamania runs wild on you?!"

Running Wild Brother, Dropping Leg Drops Brother, Hulking Up Brother, Slamming Giants Brother, Whatcha Gonna Do When Hulkamania Runs Wild on You Brother...

## Contributing

Got a theme idea? PRs welcome! Each theme needs:

```
themes/your-theme/
├── README.md           # Quick intro + sample verbs
├── your-theme.md       # Full verb list with references table
└── your-theme.json     # Raw JSON config
```

Aim for 30-45 verbs. Make them action verbs that work grammatically (present participles that read naturally with "for 30s" after them).

## License

MIT - Go wild, brother.
