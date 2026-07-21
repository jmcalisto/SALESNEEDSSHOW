# Jack's Appointment — Discovery & Needs Analysis (Show)

A single self-contained HTML training activity (the "Discovery & Needs Analysis — Show section"
comic) for Wall Street English sales training. No build step, no dependencies beyond Google
Fonts — open `show_comic.html` directly in a browser to preview or deliver it.

## What it is

A narrated, comic-book-style playback of a complete Needs Analysis appointment between Ana (the
consultant) and Jack (a prospective student). The learner reads it panel by panel — either
tapping "Next" (or pressing Space / Enter / → ) to advance, or letting it play — while interlude
"Notice how…" cards call out the techniques Ana uses at key moments. It ends with a recap of the
lessons demonstrated.

## Localization

Everything a learner sees lives in two JavaScript objects near the top of the `<script>` block:

- `STR` — interface strings, screen copy, and the phase labels
- `LINES` — the dialogue itself, as a flat ordered array of `{who, phase, cap, t, audio}` lines
- `NOTICES` — the interlude "Notice how…" bullet lists, keyed by the line index they follow

To produce a new language version, translate the string values in these three objects and
re-host the file. Nothing else needs to change. Each line also supports an optional `audio`
field for a per-language voice clip; leaving it `null` keeps the activity text-only.

## Design system

This activity follows the comic/narrative "Show section" visual style used across Wall Street
English sales training activities — distinct from the multiple-choice "Do section" style. See
the companion style-guide repo for the full design tokens, component inventory, and a blank
template for building new activities in the same comic style.
