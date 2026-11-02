# Dark tech-news

Terminal-at-night: near-black dotted background, neon accent, condensed
white headlines, monospace prompts. Great for roundups and security news,
and for Hinglish headlines ("is hafte ki 5 badi khabrein").
Template: `templates/dark-tech.html`

## Tokens

| Token | Value |
|---|---|
| Background | `#0E1116` |
| Dots | `radial-gradient(#232A33 2px, transparent 2px)` every 36 px |
| Accent | `#3DF58A` (alts: `#5CC8FF`, `#FF5C7A`, `#FFC53D`) |
| Text | `#F4F6F8` |
| Muted | `#A9B4C0` |
| Chip | `#1C232C` fill, 2 px `#34404D` border |
| Warning | `#FFC53D` |

Fonts: **Anton** (headlines), **Fredoka** 600/700 (body), **JetBrains Mono** 500/700 (prompts, chips).

```css
background-color:#0E1116;
background-image:radial-gradient(#232A33 2px,transparent 2px);
background-size:36px 36px;
```

## Components

- **Prompt chip (header left):** 3 px accent border, accent text, radius 12, mono 30 px — `$ cat weekly_threats.log`.
- **Edition (header right):** muted mono 30 px — `week [##]` or `n/N`.
- **Headline stack:** Fredoka 700 72 px white lead-in → Anton 250 px accent → Anton 132 px white lines.
- **Topic chips:** `#1C232C` + `#34404D` border, mono 700 30 px, radius 999.
- **News item card:** `#161C24` fill, 2 px `#34404D` border, radius 24; mono 26 px accent
  label (`[01] breach`), Fredoka 600 40 px headline, Fredoka 500 32 px muted one-liner.
- **Icons:** shield/lock in accent outline, warning triangle in `#FFC53D`.
- **Code block:** `#161C24`, mono 30 px, accent line numbers.
- **Footer:** handle Fredoka 700 36 px left · accent pill "save karo" (bookmark icon) · "swipe →" right.

## Cover recipe

Prompt chip + edition → optional icon top-right → lead-in → huge accent number/word
→ two white Anton lines → 3 topic chips → footer.
Contrast: accent on `#0E1116` passes; never put muted text on chips.
