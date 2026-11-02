---
name: decodedebangi-carousel
description: Create Instagram carousel posts (1080×1350) for a tech/AI creator page in one of five house styles — Editorial, Sticker, Dark tech-news, Minimal notebook, Bold pastel — plus an English and Hinglish caption. Use when the user gives a topic, script or link and asks for a carousel, slides or an Instagram post.
---

# Instagram carousel posts

Turn a topic, script or link into a ready-to-post Instagram carousel: a cover that
stops the scroll, 5–9 slides that each carry one idea, and a caption in English
and Hinglish. Built for a software-engineer creator page (tech news, AI updates,
engineering tips for students), but works for any tech topic.

## 0. Defaults (change if the user says otherwise)

| Setting | Default |
|---|---|
| Handle | `@decodedebangi` |
| Size | 1080 × 1350 px (Instagram portrait 4:5) |
| Slides | 6–9 (cover + content + CTA) |
| Style | the one the user names, else **Editorial** |
| Language | slides in English; captions in English **and** Hinglish |
| Photos | none unless the user supplies them — never leave empty photo placeholders on a final post |

Style files live in `styles/`. Read **only** the one you're using:

| Style | File | Best for |
|---|---|---|
| Editorial | `styles/editorial.md` | explainers, roadmaps, "how X works" |
| Sticker | `styles/sticker.md` | playful tips, tool workflows, "my setup" |
| Dark tech-news | `styles/dark-tech.md` | weekly roundups, security news, launches |
| Minimal notebook | `styles/minimal-notebook.md` | study notes, concepts for students, cheat sheets |
| Bold pastel | `styles/bold-pastel.md` | hot takes, myths vs facts, big single stats |

Each style file has tokens, components and layout rules; `templates/<style>.html`
has a working cover + content slide to copy from.

## 1. Intake

Start building once you have a topic or script. Ask (once, in one message) only
for what's missing and matters: style, number of slides, language. Don't ask
for photos — offer to add them later.

## 2. Research and fact-check (do not skip)

- **User pasted a script/post:** use their content, but read any link they give.
  Check every number, name and claim against the source before it goes on a slide.
- **Who is talking?** If the source is written by someone promoting their own
  product ("here's what I built"), say so to the user before building, and on
  the slides attribute claims and benchmarks to them ("their own test"), never
  present them as neutral fact. Ask whether the user wants a promo post or an
  explainer — they often want the explainer.
- **Product facts** (Claude Code, APIs, tools): get them from official docs, not
  memory. Commands, limits and features change.
- **Self-reported numbers** stay labelled as such. No invented stats, no filler.
- Illustrative examples (a fake error message, a sample path) are fine only if
  you tell the user they're examples.
- Flag mismatches between the user's script and the source (e.g. "the blog
  lists 7 layers, your cover says 6") instead of silently picking one.

## 3. Plan the slides

1. **Cover** — must be understandable by someone who has never heard the jargon.
   Lead with the reader's pain or curiosity ("why your AI agent forgets things"),
   not the technical term ("compaction is the wrong fix"). Test: could a
   2nd-year CS student tell what the post is about in 2 seconds?
   Offer 3–4 cover text options when the user is unsure; recommend one.
2. **Content slides** — one idea each: a headline (≤ 6 words, the slide's point)
   + 2–4 short points or one big number. Numbers that matter get the giant type.
3. **Middle hook** — a "the catch" / "the fix" pair keeps people swiping.
4. **CTA slide** — summary or cheat sheet + "link in the comments" + save/follow.
5. Footer cue on every content slide except the last: "swipe", or a teaser for
   the next slide ("the fix", "what survives?").

Introduce every product or proper noun the first time it appears ("Claude
Code, Anthropic's coding agent, …").

## 4. Build

**If a Design / canvas artifact type is available** (e.g. Claude's Design type):
create one canvas, one artboard per slide, each 1080 × 1350, laid out in a row
(80 px apart). Put each carousel in its own row with a title note above it.
Follow the type's own format rules; inline styles, fixed-size root.

**Otherwise:** one self-contained HTML file per slide (or one page with all
slides stacked), each slide a fixed `1080px × 1350px` box, fonts from Google Fonts.

Rules that apply in every style:

- Colours, fonts and components come from the style file. Don't mix styles
  within one carousel.
- A full-slide background goes inline on the root as `background-color` +
  `background-image` — **never** the `background:` shorthand on top of a class,
  it wipes out the grid/texture.
- Same header and footer on every slide; slide counter `n/N` must be correct.
- Icons: inline SVG. No emoji on slides.
- Minimum body text 30 px; headlines 96 px+. It's read on a phone.

### Overflow budget (the #1 bug)

Before writing each slide, add up its heights; the content must end ≤ 1180 px
from the top so it never touches the footer (footer sits at ~1240–1300).

Rough line heights: text height ≈ font-size × line-height × lines.
Lines ≈ characters ÷ (usable width ÷ char width).
Char width ≈ 0.5 × font-size (Fredoka/Inter), 0.6 × (JetBrains Mono),
0.42 × (Anton, uppercase). Usable width is ~920 px minus card padding.

If it's over: cut words first, then shrink the headline, then tighten gaps.
Never shrink body text below 30 px. Max ~4 cards or ~5 bullets per slide.

## 5. Caption

Write two versions — **English** and **Hinglish** (Roman-script Hindi mixed with
English, conversational, the way the creator talks in reels):

1. Hook question or bold line + 1 emoji
2. 2–3 short paragraphs: what's happening, the catch, the takeaway
3. 3–4 arrow (→) tips if the post is practical
4. "Swipe …" line, "link in the first comment 🔗", "save this …"
5. 5 hashtags, lowercase, relevant (no #viral, #fyp)

Give the exact link to put in the first comment. Use only facts that are on
the slides or in the source. If the post promotes someone's product, the
caption says whose it is.

## 6. Hand-off

- Tell the user what each slide says in one line, plus anything you assumed
  or couldn't verify.
- Export: **PNG 1×** per slide (1080 × 1350 is Instagram's native portrait size;
  2× gets downscaled anyway). Name files `01-cover.png` … in order.
- Offer: photos on the cover, a different style, or inner tweaks.
