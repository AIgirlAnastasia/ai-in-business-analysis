# Getting Started with Claude Code

Everything in this repo runs on **Claude Code** — a terminal-based AI agent by Anthropic. Here's how to get set up in about 10 minutes.

---

## Step 1 — Install Claude Code

You need Node.js installed first. Then run:

```bash
npm install -g @anthropic/claude-code
```

Check it works:
```bash
claude --version
```

---

## Step 2 — Set up your project folder

Create a folder for your project and navigate into it:

```bash
mkdir my-project
cd my-project
claude
```

Claude Code is now running inside your project.

---

## Step 3 — Install a skill from this repo

Pick a skill from the [`agents/`](../agents/) folder. For example, to install the call analysis skill:

1. Copy the `call-analysis` folder into `.claude/skills/` in your project:

```
your-project/
└── .claude/
    └── skills/
        └── call-analysis/
            └── SKILL.md
```

2. Restart Claude Code (`Ctrl+C`, then `claude` again)

3. Run the skill:
```
/call-analysis
```

---

## Step 4 — For the Telegram Notes skill

This skill needs one extra step — a Telegram bot token.

1. Open Telegram → search for `@BotFather`
2. Send `/newbot` and follow the steps
3. Copy your token
4. Create a `.env` file in your project root:

```
TELEGRAM_BOT_TOKEN=your_token_here
```

Then install and run `/telegram-notes` as above.

---

## Need help?

- [Claude Code docs](https://docs.anthropic.com/claude-code)
- Open an issue in this repo
- Find me on LinkedIn: [Anastasia Kalacheva](#)
