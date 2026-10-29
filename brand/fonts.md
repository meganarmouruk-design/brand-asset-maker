# Fonts

**Policy path: (b) a named free font** (`source: free` in `locked.json`).

Why: the owner named the fonts (intake question 3) and holds no font files. The owner chose on 2026-10-29 to load them from Google Fonts rather than commit files to the public fork, so there is no `brand/fonts/` folder and `fonts.css` imports the Google Fonts stylesheet (which carries the `@font-face` rules). Rendering needs an internet connection; if `font-loaded` fails offline, download the OFL files into `brand/fonts/` and point `fonts.css` at them.

Source: [intake-form.md](sources/intake-form.md) question 3: "We use Plus Jakarta Sans primarily for headers and copy, and then Onest in digital navigation"

| Family | Used for in posts | Weights | Licence | Source URL | Status |
|---|---|---|---|---|---|
| Plus Jakarta Sans | display (h1–h3, data) and body (body, label) | 400, 700, 800 | SIL Open Font License 1.1 | https://fonts.google.com/specimen/Plus+Jakarta+Sans | you said (locked) |
| Onest | not used in posts: the owner uses it in digital navigation only | — | SIL Open Font License 1.1 | https://fonts.google.com/specimen/Onest | you said (locked) for navigation |

Weights read from the Figma styles: Source: [figma-export.md](sources/figma-export.md) ("Title"/"Heading" Bold 700, "Subheading" ExtraBold 800, "Body" Regular 400, "Body emphasised" Bold 700). Which weight each role uses is **we guessed** (derived) until a post is approved.
