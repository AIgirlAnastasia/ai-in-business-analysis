# Telegram Notes Agent

Send yourself voice memos or text messages during the day. Run this skill at the end of the day — everything is classified into Ideas and Tasks, ready to review.

**Run with:** `/telegram-notes`

---

## What it does

| Step | Action |
|------|--------|
| TAKE | Fetches new messages from your Telegram bot via API |
| PROCESS | Transcribes voice messages (Whisper) → classifies into Ideas or Tasks |
| STORE | Saves to `telegram-notes/ideas.md` and `telegram-notes/tasks.md` |

No duplicates — tracks the last processed message automatically.

---

## Setup

### 1. Create a Telegram bot
1. Open Telegram → find `@BotFather`
2. Send `/newbot` → follow the prompts
3. Copy the token you receive

### 2. Add your token
Create a `.env` file in your project root:
```
TELEGRAM_BOT_TOKEN=your_token_here
```

### 3. Install Whisper (for voice messages)
```bash
pip install openai-whisper
```

### 4. Install the skill
Copy this folder to `.claude/skills/telegram-notes/` in your project.

### 5. Run it
```
/telegram-notes
```

---

## Example output

See [`example-output.md`](./example-output.md) for sample ideas and tasks.

---

## Tips

- Works with any language — Whisper supports 90+ languages
- Send rough voice notes — exact wording doesn't matter, the agent finds the meaning
- Run it once a day before you plan your next day
- The `.last_update_id` file is excluded from git — it's local state only
