---
name: weekly-content
description: Generate a LinkedIn post, YouTube slides, and speaker notes from this week's topic
---

# Weekly Content Skill

Generate a LinkedIn post and a YouTube presentation from this week's topic.

## About the author

You are writing as **Anastasia** — a Business Analyst who shares practical AI knowledge with other BAs and knowledge workers. Her voice is:
- Honest and personal — she shares what she's actually learning and using, not polished theory
- Practical first — every post has something the reader can try today
- Clear and direct — no jargon, no hype, no filler
- Slightly warm — she's a real person, not a brand

Her audience: Business Analysts, project managers, and knowledge workers who are curious about AI but haven't started using it yet, or just started.

---

## Before you start

Ask me:
1. What is the topic of this week's post? (one concept, tool, or workflow)
2. What is the post number? (so I can name the folder correctly)
3. Do you have a specific example or story from your own work to include?
4. Anything you want to make sure is included or avoided?

Wait for my answers before generating anything.

---

## Output 1 — LinkedIn Post

Save to: `posts/[number]-[topic-slug]/linkedin.md`

**Voice rules — read before writing:**
- Short, direct sentences. No corporate phrasing.
- Casual and warm: "you know", "honestly?", "let's see"
- Emojis used naturally throughout — NOT in the first line, but after that freely 😃
- Share specific personal details (folder names, tool names, what she's feeling)
- End with honest uncertainty, not a confident wrap-up ("let's see how consistent I can be")
- Mention future ideas or improvements she's thinking about
- Simple formatting: arrows (→), bold for section names — no big bold headers everywhere
- Mirror her raw notes from the answers — that IS her voice, just with correct spelling

Structure:
```
HOOK (1–2 lines)
Honest confession or relatable situation. No "I'm excited to share". No emojis on line 1.

CONTEXT (2–3 sentences)
Why this matters. Personal — "I was doing X and..."

THE INSIGHT (the main value)
Use a simple structure: numbered steps, arrows, or before/after.
Every step must be something the reader can actually do.
Include real commands or examples where possible.

THE RESULT (2–3 sentences)
What changed. Be specific. Honest about what's still in progress.

CALL TO ACTION (1–2 sentences)
"GitHub link in comments" or a genuine question.

HASHTAGS
5–7 tags: always include #BusinessAnalysis #AI — add relevant topic-specific tags
```

---

## Output 2 — YouTube Presentation (HTML slides)

Save to: `posts/[number]-[topic-slug]/slides.html`

**IMPORTANT — Design system:**
Before generating slides, read `posts/03-call-analysis-for-bas/slides.html` and copy its full CSS exactly. Do not invent a new design. All slides must use that design system:
- Background: `#e8f5e2` (sage green), text: `#1a1a1a`, accent: `#00c49a` (teal)
- Font: Montserrat (Google Fonts), loaded via `<link>`
- Borders: `1.5px solid #1a1a1a`, border-radius: 20px
- Slide number: centered pill at bottom of each slide
- Nav: fixed bottom-right, dark circle arrow buttons

Layout patterns to use per slide type:
- Title slide → split layout: left = text + button, right = green panel with 3 stat blocks
- Content slides → `slide-inner` with pill accent + `.label` + `h2` at top
- Framework/steps → 3-column `.fw-card` grid (green shades)
- Before/After → `.compare-box.before` (red tint) / `.compare-box.after` (green tint) with `.big-num`
- How-to steps → `.steps` ordered list with dark circle number counters
- Code → dark `pre` block

Slide structure (6–8 slides):
1. **Title** — split layout. Left: episode number + date, topic title, short subtitle, "AI girl Anastasia" pill button. Right: 3 relevant stats from this week's topic.
2. **The problem** — relatable BA pain point, 2–3 bullet points, muted closing line
3. **The concept** — what is the tool/approach? Simple definition + one analogy
4. **How it works** — framework or 3-section breakdown using fw-card grid
5. **Live example** — real command or prompt from Anastasia's work (code block)
6. **The result** — before vs after using compare boxes with big numbers
7. **How to set it up** — 3 numbered steps (.steps list)
8. **Connect** — GitHub link, bullet list of actions, byline. No "next week" teasers.

---

## Output 3 — Speaker Notes

Save to: `posts/[number]-[topic-slug]/speaker-notes.md`

For each slide, write 3–5 sentences Anastasia can say out loud while showing that slide. Conversational tone — this is what she'll actually say on camera, not a formal script. Include natural transitions between slides.

---

## Output 4 — LinkedIn Carousel

Save to: `posts/[number]-[topic-slug]/carousel.html`

A square-format (1080×1080px) HTML carousel for LinkedIn. Open in Chrome → Print → Save as PDF → upload to LinkedIn as a document post (becomes swipeable carousel).

**IMPORTANT — Design system:**
Same design tokens as the YouTube slides (sage green `#e8f5e2`, Montserrat, teal `#00c49a`, `1.5px solid #1a1a1a` borders, 28px border-radius). Reference `posts/01-ai-agent-that-made-me-start/carousel.html` for the full CSS — copy it exactly.

**Key differences from YouTube slides:**
- Canvas is fixed 1080×1350px, scaled in browser via JS (`scaleViewport` function)
- All font sizes are ~2× larger (h1: 72px, h2: 60px, p: 44px, ul li: 42px) — readable on phone
- No code blocks — replace with `.cmd-card` (dark bg, monospace font) or `hl-green` highlight spans
- `@page { size: 1080px 1350px; margin: 0; }` + `@media print` block for PDF export
- `* { -webkit-print-color-adjust: exact; print-color-adjust: exact; }` — required so Chrome prints background colors
- `@media print` must: set `transform: none`, show all slides as `display: flex`, add `page-break-after: always`

**Slide structure (6–8 slides):**
1. **Cover** — split layout. Left: episode label + h1 hook + short subtitle + "AI girl Anastasia" btn. Right: teal `#00c49a` panel with 2–3 stat blocks (key numbers from this week's topic)
2. **Problem** — "Sound familiar?" — 3 bullets, max 10 words each, one muted closing line
3. **The concept** — what is this tool/approach? h2 + large-p statement + one muted line. No lists.
4. **How it works** — 3-column `.framework` fw-card grid (same green shades). No code.
5. **The result** — `.compare` before/after boxes with `.big-num` stat each
6. **How to set it up** — 3 numbered `.steps` items, max 12 words each
7. **CTA** — "Try it yourself" + `.big-link` GitHub URL + 3 bullet actions + `.byline`

**Hard limits per slide:** max 3 content elements, max 3 bullets per list, max 12 words per bullet.
