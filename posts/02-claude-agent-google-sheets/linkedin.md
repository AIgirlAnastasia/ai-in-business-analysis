# Post 02 — LinkedIn

---

You don't need to learn Python to analyze data anymore.

You need to learn how to ask the right question.

I've been a Business Analyst for years and always felt that gap — I can see what needs to be analyzed, but actually writing the code to do it? That's where I'd slow down or give up.

Then I found a pattern that changed this completely. 🙂

Here's the thing about LLMs: they're terrible at arithmetic. Ask Claude "what's the conversion rate in these 3,000 rows?" — it will confidently give you a wrong number.

But ask Claude to **write code that calculates** the conversion rate?

The code will be perfect. Every time.

This is what I call the **Module Pattern**:

→ **GET** — pull data from Google Sheets via MCP connection
→ **WRITE** — ask Claude to write the counting script
→ **RUN** — execute it, get exact numbers (zero hallucination possible)
→ **EXPLAIN** — paste the output back, ask Claude what it means

The split of responsibility is the key insight here 💡

Claude handles: understanding the question, writing the logic, interpreting the result
Code handles: the actual counting

You stay in the middle: asking the right questions.

I tested this on a real e-commerce dataset — 3,295 rows of user interactions. I asked Claude to write a formula directly into Google Sheets and a Python script for the deeper analysis. Setup took 10 minutes. The analysis I'd normally spend an hour on? Done in 5.

And I didn't write a single line of code.

This is what "AI for analysts" actually looks like in practice — not replacing the analyst, but removing the technical barrier that was always in the way.

Full breakdown + setup guide on GitHub (link in comments) 👇

Have you tried connecting Claude to your spreadsheets yet? Curious what you'd use this for 👀

#BusinessAnalysis #AI #DataAnalysis #GoogleSheets #ClaudeAI #NoCode #BusinessAnalyst
