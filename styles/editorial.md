# Editorial

Magazine-style: big condensed orange headlines on warm cream graph paper,
white tags, black code pills. Calm, credible, explainer energy.
Template: `templates/editorial.html`

## Tokens

| Token | Value |
|---|---|
| Background | `#FBF6EF` |
| Grid | `#E6DACB`, 2 px lines every 54 px |
| Accent | `#D2552F` (alts: `#2F6FE4`, `#1E7A4C`, `#141414`) |
| Ink | `#141414` |
| Muted | `#6B625A` |
| Card | `#FFFFFF`, radius 24, shadow `0 10px 24px rgba(0,0,0,0.07)` |
| Divider | 4 px `#141414` (major), 2 px `#CFC5B9` (minor) |

Fonts (Google Fonts): **Anton** (headlines, ALL CAPS, line-height 0.98),
**Fredoka** 500/600/700 (body), **JetBrains Mono** 500 (pills, `// labels`, commands).

```css
background-color:#FBF6EF;
background-image:linear-gradient(#E6DACB 2px,transparent 2px),
                 linear-gradient(90deg,#E6DACB 2px,transparent 2px);
background-size:54px 54px;
```

## Components

- **Header:** handle centred at top 52 px, Fredoka 700 38 px, accent colour.
  Counter: 100 px circle, top 38 / right 52, `rgba(110,104,98,0.55)`, white 32 px bold `2/8`.
- **Section pill:** black `#141414`, white JetBrains Mono 32 px, radius 999, padding 12×30.
- **Headline:** Anton 104–132 px; line 1 ink, line 2 accent. Text-shadow `5px 5px 0 rgba(0,0,0,0.1)`.
- **Tag:** white box, Fredoka 700 44–72 px, radius 20–24, rotated −1.5°, soft shadow.
- **Layer number:** Anton 190–210 px accent ("01") beside an Anton 78–88 px title.
- **Big stat row:** 4 px ink top border, Anton 150–210 px accent number, Fredoka 40 px label.
- **Bullet:** accent `→` + Fredoka 500 38–42 px; key phrase in **bold**.
- **Comment label:** JetBrains Mono 28–30 px muted, `// what this is`.
- **Table:** rows with 2 px `#CFC5B9` dividers, framed by 4 px ink lines.
- **CTA block:** accent fill, radius 30, Anton 66–76 px white + black and white pills.
- **Footer:** bottom 50–60 / right 60 — Fredoka 700 48 px cue + 120×12 px accent bar.

## Cover recipe

Section pill → Anton line (accent, 124–200 px) → white tag → Anton line (accent)
→ Fredoka 46 px subline with ↓ → two black mono pills. Content block starts
~250–300 px from top.
