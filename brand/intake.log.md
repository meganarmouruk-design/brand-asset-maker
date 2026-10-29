# Intake log

Brand: forgettable. Intake run 2026-10-29. No engine: each step done by hand per `skills/bam--intake.md` "Without the engine".

## Doctor (by hand)

The owner handed in the intake form ([sources/intake-form.md](sources/intake-form.md)) with questions 1–9 answered. Question 10 (character words) is not on that form, so it is blank. Required items 1, 2 and 4 are present.

## Questions from the form (answers copied verbatim)

| # | Question | Answer | What we did with it |
|---|---|---|---|
| 1 | Logo and wordmark | "The logo is Forgettablelogo.svg, there is no text wordmark. It is spelled forgettable" | `assets/logo.svg` (bytes unchanged, sha256 7065b8a0…9d61), `locked`; `brand.json` wordmark `null`, name `forgettable`. No reversed logo supplied. |
| 2 | Primary colour | "FF5F08" | `--brand-accent: #FF5F08`, `locked` |
| 3 | Fonts | "We use Plus Jakarta Sans primarily for headers and copy, and then Onest in digital navigation" | Display and body = Plus Jakarta Sans, `locked`; Onest recorded as navigation only (not a post role). Policy path (b) free. |
| 4 | Who it is for | "Target customers are Singaporeans of all ages with Insurance coverage, and financial advisors who serve those customers." | `voice.md` |
| 5 | How it sounds | "playful, reassuring, unconventional" | `voice.md` tone words, `locked` |
| 6 | Never say | "It is not financial advice, it is assisting you manage your coverage to best protect your life." | `voice.md` never-claims; Refuse paragraph in `BRAND.md` |
| 7 | On-brand posts | three links (e27 article, forgettable.ai, an Instagram post) | Listed in `sources.md`. They are posts and a site, not layouts or templates, so no layouts to encode first. Not read into any value. |
| 8 | Photographs | "We dont have a library of photos yet, but the style is Candid, 90s grain film-inspired lifestyle photography meets playful fashion editorial. Naturalistic lighting, unconventional framing, expressive over-sized typograpth, effortless in attitude. It should almost feel spontaneous." | No photograph yet. Style recorded in `BRAND.md` Files. BAM has no photograph layout: a post over a photo is a gap note. |
| 9 | Where they run first | "Instagram and LinkedIn" | Formats 1:1 and 4:5 |
| 10 | Character words | (not asked on the form) | No `expression.json`. Ask later if wanted. |

## Figma

The Figma link is the Forgettable app UI, not a brand guide. Read with the Figma tools on 2026-10-29; variables, type styles and the card radius are saved verbatim in [sources/figma-export.md](sources/figma-export.md). Values read from it are `derived` unless the owner confirmed them.

## Questions asked in chat, 2026-10-29

| Id | Question | Owner's answer | Result |
|---|---|---|---|
| Q-ink | Which of the Figma blacks is the ink: #000020, #27272A or #010101 (logo)? | #000020 | `--brand-ink: #000020`, `locked` |
| Q-paper | Paper: #F9FAFB, #FFFFFF, or the purple→green gradient? | #F9FAFB | `--brand-paper: #F9FAFB`, `locked` |
| Q-muted | Figma grey #8E8E93 is 3.1:1 on paper (fails 4.5:1). What should muted be? | Use #27272A dark grey | `--brand-muted: #27272A`, `locked` |
| Q-fonts | Commit OFL font files to the public fork, or load from Google Fonts? | Load from Google Fonts | `fonts.css` imports Google Fonts; no `brand/fonts/` |

## Contrast table (WCAG 2.x, measured 2026-10-29)

| Pair | Ratio | 4.5:1 | 3:1 |
|---|---|---|---|
| ink #000020 on paper #F9FAFB | 19.68 | pass | pass |
| muted #27272A on paper #F9FAFB | 14.25 | pass | pass |
| accent #FF5F08 on paper #F9FAFB | 2.92 | fail | fail |
| accent #FF5F08 on ink #000020 | 6.75 | pass | pass |
| ink #000020 on accent #FF5F08 | 6.75 | pass | pass |
| white #FFFFFF on accent #FF5F08 | 3.05 | fail | pass |
| muted #27272A on accent #FF5F08 | 4.89 | pass | pass |
| muted #27272A on ink #000020 | 1.38 | fail | fail |
| grey #8E8E93 on ink #000020 | 6.31 | pass | pass |
| grey #8E8E93 on paper #F9FAFB | 3.12 | fail | pass |
| purple #C9BFFF on paper #F9FAFB | 1.62 | fail | fail |
| green #E2F8AE on paper #F9FAFB | 1.10 | fail | fail |

Derived from it:
- `--brand-accent-ink: #000020` (ink reads on orange; white does not at small sizes).
- Paper scheme: orange text falls back to ink (`--pg-accent-text`); orange stays for bars and marks.
- Ink scheme: muted becomes `--brand-muted-on-ink: #8E8E93` (Figma "Grays/Gray").
- Purple and green are surfaces only, never text on paper.

## Logo visibility (measured 2026-10-29, headless Chromium, logo as `<img>`)

Share of the logo's opaque pixels at 1.5:1 or more against the ground (BAM fails under 0.4):
- paper #F9FAFB: 0.95
- accent #FF5F08: 0.79
- ink #000020: 0.42 — the black asterisk (#010101) disappears; only the gradient arrow shows. Passes the number by a hair, but the mark does not read. **A reversed logo is needed for ink posts.**

## Photographs

No photograph yet.
