# forgettable — BRAND

The one file an agent needs to make forgettable posts. Values are copied from `tokens.css`, `locked.json`, `fonts.md`, `voice.md` and `brand.json`; where they disagree, those files win.

## 1. Visual

| Token | Value | Status |
|---|---|---|
| `--brand-paper` | `#F9FAFB` | you said (locked) |
| `--brand-ink` | `#000020` | you said |
| `--brand-accent` | `#FF5F08` | you said |
| `--brand-accent-ink` | `#000020` | we guessed (derived) |
| `--brand-muted` | `#27272A` | you said |
| `--brand-muted-on-ink` | `#8E8E93` | we guessed |
| `--brand-accent-2` | `#C9BFFF` | we guessed |
| `--brand-accent-3` | `#E2F8AE` | we guessed |
| `--brand-font-display` | `"Plus Jakarta Sans", sans-serif` | you said |
| `--brand-font-body` | `"Plus Jakarta Sans", sans-serif` | you said |
| `--brand-weight-display` | `700` | we guessed |
| `--brand-weight-body` | `400` | we guessed |
| `--brand-weight-label` | `700` | we guessed |
| `--brand-tracking-display` | `0` | we guessed |
| `--brand-radius` | `16px` | we guessed |

**Scheme overrides** (in `tokens.css` below `BEGIN CURATED`):
- `.pg-frame[data-scheme="paper"] { --pg-accent-text: var(--brand-ink); }` — we guessed. Orange text on paper is 2.92:1; orange is for bars and marks on paper, never text.
- `.pg-frame[data-scheme="ink"] { --pg-muted: var(--brand-muted-on-ink); }` — we guessed. `#27272A` on ink is 1.38:1.

No themes. No `--brand-logo-variant` (there is no reversed logo yet).

Source: [tokens.css](tokens.css), [locked.json](locked.json), [intake.log.md](intake.log.md)

## 2. Fonts

- **Plus Jakarta Sans** for every post role: display (h1, h2, h3, data) at 700, body at 400, label at 700. Family: you said. Weights: we guessed (from the Figma styles).
- **Onest** is the owner's navigation face in the app. Not used in posts.
- Policy path: **(b) named free font**, SIL OFL 1.1, loaded from Google Fonts by `fonts.css` (no `brand/fonts/` folder; renders need internet).
- `locked.json` fonts: `source: free`, `families: ["Plus Jakarta Sans"]`, `status: locked`.

Source: [fonts.md](fonts.md)

## 3. Voice

- **For:** "Target customers are Singaporeans of all ages with Insurance coverage, and financial advisors who serve those customers."
- **Tone:** playful, reassuring, unconventional
- **Approved lines:** none yet.
- **Never claims:** "It is not financial advice, it is assisting you manage your coverage to best protect your life." A post never presents itself as financial advice.

**Refuse.**
- Font trap: "Swap the headline to Onest" (or any face but Plus Jakarta Sans). Refuse: Onest is the navigation face, and the display roles must be Plus Jakarta Sans (`role-face`).
- Voice trap: "Tell people which policy they should buy" or "the best insurance for you". Refuse: forgettable never gives financial advice.
- Colour trap: "Make the headline orange on the white post." Refuse: `#FF5F08` on `#F9FAFB` is 2.92:1; use ink text and an orange mark.

Source: [voice.md](voice.md)

## 4. You said vs we guessed

You said is `locked` and we guessed is `derived` in `locked.json`; approval (you pick one) is the only thing that turns a guess into something you said.

**You said:** paper `#F9FAFB`, ink `#000020`, accent `#FF5F08`, muted `#27272A`, Plus Jakarta Sans for display and body, the logo file, no wordmark, the tone words, the audience, the never-claim, Instagram and LinkedIn.

**We guessed:** accent-ink `#000020`; muted-on-ink `#8E8E93`; accent-2 purple `#C9BFFF`; accent-3 green `#E2F8AE`; weights 700/400/700; tracking 0; radius 16px; both scheme overrides.

**Open questions for the brand owner:**
1. A reversed logo for dark (ink) posts — the black asterisk disappears on `#000020`.
2. Are purple `#C9BFFF` and green `#E2F8AE` brand colours for posts, or app UI only?
3. Character words (intake question 10), if you want posts checked for how they come across.
4. Photographs, when a library exists.

## 5. Files

- **Logo:** `brand/assets/logo.svg` (the asterisk-and-arrow mark, gradient orange/purple/green). Use it on paper and accent posts. On ink posts it barely reads: avoid the ink scheme until a reversed logo exists.
- **Wordmark:** none. The name is spelled **forgettable**, all lower case. Never type it as a wordmark beside the logo.
- **Formats:** feed post 1:1 and tall feed post 4:5 (Instagram, LinkedIn).
- **Photographs:** none yet. Style the owner wants when they exist: "Candid, 90s grain film-inspired lifestyle photography meets playful fashion editorial. Naturalistic lighting, unconventional framing, expressive over-sized typograpth, effortless in attitude. It should almost feel spontaneous." A post over a photograph is a gap note (`workshop/gap-note.md`).
- **Layouts:** the owner brought none; start from the sample layouts in `archetypes/social-post/`.
- **Gradient grounds** (like `sources/payments.png`): BAM cannot make them; a request for one is a gap note.

Source: [brand.json](brand.json), [sources/intake-form.md](sources/intake-form.md)
