# Telegram Notes Skill

Collect all new messages from my Telegram bot, transcribe any voice messages, and classify everything into Ideas and Tasks.

## Setup check

Before starting, confirm:
1. The `.env` file exists in the project root with `TELEGRAM_BOT_TOKEN`
2. Whisper is available locally — if not, install it with `pip install openai-whisper`

## Instructions

### Step 1 — Check last processed message

Read the file `telegram-notes/.last_update_id` if it exists.
If it exists, only fetch messages with `update_id` greater than the saved value.
If it doesn't exist, fetch all messages.

### Step 2 — Fetch messages from Telegram

Use the Telegram Bot API `getUpdates` endpoint with the token from `.env`.
If a last update_id was found, add `offset = last_update_id + 1` to the request.

### Step 3 — Process each message

For **text messages**: use as-is.

For **voice or audio messages**:
1. Download the audio file using the Telegram file API
2. Transcribe it locally using Whisper (`whisper-1` model, use local execution)
3. Use the transcript as the message text

### Step 4 — Classify each message

Read each message and assign it to one of two types:

**IDEA** — an observation, insight, concept, or thing worth exploring later
**TASK** — something with a clear action that needs to be done

### Step 5 — Save results

**Ideas** → `telegram-notes/ideas.md`

Format per idea:
```
## [Date received]
**Main idea:** [1–2 sentence summary]
**Details:** [up to 8 sentences with all relevant context; brief external research is fine if it adds value]
**Source:** [text / voice]
```

**Tasks** → `telegram-notes/tasks.md`

Format per task:
```
## [Date received]
**Task:** [clear title]
**Assignee:** [if mentioned, otherwise "me"]
**Deadline:** [if mentioned, otherwise "not set"]
**Steps:**
- [step 1]
- [step 2]
```

Append new entries to existing files — do not overwrite previous content.

### Step 6 — Save progress

Write the highest `update_id` from this batch to `telegram-notes/.last_update_id`.

Tell me how many messages were processed and how many were ideas vs tasks.
