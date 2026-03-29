# Weekly Content Agent

The core agent. Give it a topic → it generates a LinkedIn post, a YouTube presentation, and speaker notes. One command, three files, ready to publish.

**Run with:** `/weekly-content`

---

## What it produces

| File | What it is |
|------|-----------|
| `linkedin.md` | Ready to copy-paste into LinkedIn |
| `slides.html` | Open in browser → share screen on YouTube |
| `speaker-notes.md` | What to say on each slide |

---

## How it works

1. Run `/weekly-content`
2. The agent asks you 4 questions about this week's topic
3. It generates all 3 files in `posts/[number]-[topic-slug]/`
4. Open `slides.html` in Chrome, go full-screen, start recording

---

## The output folder structure

Each week produces a folder like this:

```
posts/
└── 03-call-analysis-for-bas/
    ├── linkedin.md
    ├── slides.html
    └── speaker-notes.md
```

---

## Presentation design

The HTML slides are built for screen sharing:
- Sage green background (`#e8f5e2`), Montserrat font, teal accent (`#00c49a`)
- Large fonts readable at any resolution
- No external dependencies — works offline
- One idea per slide — clean, focused

---

## Tips

- The more specific your example, the better the output
- Share a real number ("saved 2 hours") rather than vague claims
- Run it, review it, adjust 20% — don't rewrite from scratch
- Commit and push after each week so the repo stays current
