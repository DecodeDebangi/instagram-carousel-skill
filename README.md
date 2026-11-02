# Instagram Carousel Skill
   
A Claude skill that turns a topic, script or link into a ready-to-post
**Instagram carousel** (1080 × 1350) in one of five styles — plus captions in
English and Hinglish.

Built by [@decodedebangi](https://instagram.com/decodedebangi) for tech and AI
explainer posts.

## Styles

| Style | Vibe | Best for |
|---|---|---|
| **Editorial** | condensed orange headlines on cream graph paper | explainers, roadmaps, "how X works" |
| **Sticker** | grid paper, outlined pink type, die-cut sticker icons | playful tips, tool workflows |
| **Dark tech-news** | near-black, neon green, terminal prompts | weekly roundups, security news |
| **Minimal notebook** | ruled paper, highlighter, handwritten notes | study notes, concepts for students |
| **Bold pastel** | flat pastel blocks, giant grotesque type | hot takes, myths vs facts, big stats |

Open any file in `templates/` in a browser to see a cover and a content slide.

## What the skill does

1. Asks only for what's missing (style, slide count, language).
2. **Fact-checks** the script against its source and official docs, and flags
   when a source is promoting its own product.
3. Plans a jargon-free cover, one idea per slide, a "catch → fix" hook and a CTA.
4. Builds each slide at 1080 × 1350 with an **overflow budget** so text never
   collides with the footer.
5. Writes the caption in English and Hinglish, with the first-comment link.

## Install

**Claude (claude.ai / desktop):** zip the folder and upload it under
Settings → Capabilities → Skills, or add it from the repo.

**Claude Code:**

```bash
git clone https://github.com/DecodeDebangi/instagram-carousel-skill.git \
     ~/.claude/skills/instagram-carousel
```

Then ask: *"Make a carousel in the dark tech-news style about this week's AI news."*

## Structure

```
SKILL.md              workflow Claude follows
styles/<style>.md     tokens, components and cover recipe per style
templates/<style>.html  working cover + content slide per style
```

## Customise

Change the handle, colours or fonts in `SKILL.md` and `styles/`. To add a style,
copy any `styles/*.md` + `templates/*.html` pair and add a row to the table in
`SKILL.md`.

## License

MIT
