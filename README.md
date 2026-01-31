# Claude Verbs

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

### [Arnold Schwarzenegger](themes/arnold-schwarzenegger/)

> "I'll be back."

Getting to the Chopper, Being Back, Considering It a Divorce, Letting Off Some Steam, Hasta La Vista-ing Baby...

### [Bob Ross](themes/bob-ross/)

> "We don't make mistakes, just happy little accidents."

Beating the Devil Out of It, Adding Happy Little Trees, Making Happy Accidents, Finding Friends for Trees, Believing in the Magic...

### [Breaking Bad](themes/breaking-bad/)

> "I am the one who knocks."

Saying My Name, Knocking, Applying Science, Being the Danger, Cooking...

### [The Big Lebowski](themes/big-lebowski/)

> "The Dude abides."

Abiding, Marking It Zero, Entering a World of Pain, Tying the Room Together, Not Rolling on Shabbos...

### [Lord of the Rings](themes/lord-of-the-rings/)

> "Even the smallest person can change the course of the future."

Carrying the Ring, Speaking Friend and Entering, Not Simply Walking into Mordor, Keeping It Secret Keeping It Safe, Lighting the Beacons...

### [Pirate](themes/pirate/)

> "Yo ho ho and a bottle of rum!"

Swabbing the Deck, Seeking Buried Treasure, Hoisting the Jolly Roger, Searching for the Black Pearl, Shivering Timbers...

### [Noir Detective](themes/noir-detective/)

> "She walked in like trouble on two legs."

Following the Dame, Pouring Another Whiskey, Narrating Internal Monologue, Watching Rain Hit the Window, Lighting Another Cigarette...

## Creating New Themes

This repo includes a Claude Code skill for generating new themes. Copy `skills/verb-theme-creator/SKILL.md` to your `~/.claude/skills/` directory, then ask Claude to create a new verb theme.

The skill guides you through:
- Brainstorming verbs around your theme
- Converting quotes/references into action verb format
- Generating the required file structure

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
