# Call Analysis Agent

Reads meeting transcripts and extracts everything a Business Analyst needs: decisions, open questions, problems, and action items.

**Run with:** `/call-analysis`

---

## What it does

| Step | Action |
|------|--------|
| TAKE | Reads all `.md` files from your `calls/` folder |
| PROCESS | Extracts decisions, open questions, problems, action items |
| STORE | Saves structured report to `report.md` |

---

## Setup

1. Create a `calls/` folder in your project
2. Add meeting transcripts as `.md` files (one file per meeting)
3. Install this skill → copy to `.claude/skills/call-analysis/`
4. Run `/call-analysis`

Your transcripts can be rough notes, copy-pasted Zoom transcripts, or anything written. The agent handles the structure.

---

## Example output

See [`example-output.md`](./example-output.md) for a sample report with anonymized data.

---

## Tips

- Name your transcript files by date: `2026-03-24_weekly-sync.md`
- Works best with 3–15 transcripts at once
- Run it before a status meeting to prep in 2 minutes instead of 30
