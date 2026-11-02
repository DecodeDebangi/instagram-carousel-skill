# Sticker (playful)

Scrapbook energy: grid paper, chunky rounded type, outlined pink words,
die-cut sticker icons, brutalist cards with hard black shadows.
Template: `templates/sticker.html`

## Tokens

| Token | Value |
|---|---|
| Background | `#FBFAF7` |
| Grid | `#ECEAE4`, 1.5 px lines every 54 px |
| Blue (accent) | `#2F6FE4` |
| Raspberry | `#C2335A` (outline stroke `#B8264F`, fill `#F9C9DA`) |
| Orange | `#F06A2B` |
| Yellow | `#FFD45C` |
| Pastel fills | pink `#F9C9DA`, mint `#C7F0D8`, butter `#FFE7A3`, sky `#CFE0FF` |
| Ink | `#1B1B1F` |
| Card | white, **4 px ink border**, radius 30, shadow `10px 10px 0 #1B1B1F` |

Font: **Fredoka** 500/600/700 for everything (Google Fonts).

## Components

- **Outlined word:** Fredoka 700, `color:#F9C9DA; -webkit-text-stroke:14px #B8264F; paint-order:stroke fill;`
- **Hero box:** blue fill, radius 30, padding 14, inner 5 px dashed white border radius 20, white 200 px text.
- **Dashed pill:** white, 4 px dashed raspberry border, radius 999, Fredoka 600 42 px.
- **Stickers:** inline SVG 130–150 px, each shape with an 8 px white stroke and
  `filter:drop-shadow(0 6px 0 rgba(0,0,0,0.12))`, rotated ±6–12°. Use simple
  shapes: terminal window, bug, asterisk, folder, check circle, bookmark.
  Place 2 on each side of the cover headline, never over text.
- **Number badge:** 96–110 px circle, blue fill, white Fredoka 700 60 px.
- **Stat card:** pastel fill + brutalist border/shadow, 120 px number.
- **Counter:** black pill, white Fredoka 600 32 px, top-right.
- **Cover bottom bar:** 5 px blue line across; on it three pills — white handle,
  yellow "save for later" with bookmark SVG, white "swipe →".
- **Footer (content slides):** "swipe →" Fredoka 600 36 px bottom-right.

## Cover recipe

Small line (78 px, one word blue) → blue hero box → outlined pink line (104–120 px)
→ dashed pill → (optional) photo cards only if the user gave photos → bottom bar.
