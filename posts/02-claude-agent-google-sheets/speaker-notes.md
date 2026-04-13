# Speaker Notes — Episode 02
## Data Analysis No Longer Requires Coding

---

### Slide 01 · Title

Hey, welcome back. This week I want to challenge something that I think stops a lot of BAs from using AI for data work — the idea that you need to know how to code. You don't. What you need is a specific pattern. And once I learned it, I stopped spending hours in Excel and started spending minutes with Claude. Let's go through it.

---

### Slide 02 · The problem

So here's the mistake I made when I first tried this. I had 3,295 rows of data, I asked Claude directly: "what's the conversion rate?" It gave me a number, it sounded confident, it was wrong. And this is actually a known thing — LLMs are not built to count. They're built to predict the next likely word. So when you ask them to do arithmetic on large datasets, they'll give you something that sounds plausible. The fix is surprisingly simple.

---

### Slide 03 · The concept

The pattern is called: code counts, LLM interprets. You don't ask Claude for the answer. You ask Claude to write code that finds the answer. And then you run the code. The code is deterministic — it doesn't hallucinate, it doesn't estimate. It counts every row. Claude's job becomes writing the logic and then explaining what the numbers mean. Your job is asking the right question. That's it. You never have to write a single line of Python.

---

### Slide 04 · Framework

Four steps, same every time. Step one: GET — connect Google Sheets via MCP, Claude reads the sheet directly. Step two: WRITE — you describe what you want to know, Claude writes the formula or the script. Step three: RUN — the code executes, you get exact numbers. Step four: EXPLAIN — you paste the output back to Claude and ask what it means. This loop takes about 5 minutes for most analyses. And the more you use it, the faster you get at asking the right question in step two.

---

### Slide 05 · Formula in the sheet

So here's what step two actually looks like. I said to Claude: "Write a formula into cell E1 that counts the total number of purchases." Claude used the MCP connection to insert `=COUNTIF(C:C,"purchase")` directly into my Google Sheet. The sheet calculated: 855 purchases. I didn't touch a keyboard for that formula. Then I said: "Now I want a monthly breakdown" — and that's when the simple formula wasn't enough, so Claude wrote a script instead. Same pattern, bigger question.

---

### Slide 06 · The script

This is the script Claude wrote for the monthly breakdown. I wrote none of this. I described what I wanted — "break down interactions by month, show me purchases per month" — and Claude produced this. Then I ran it with one command and got a complete monthly breakdown of 3,295 rows in about 5 seconds. The interesting thing is: you don't need to understand this code. You need to understand the output.

---

### Slide 07 · Result

So what did the script find? Three things. One — 71.5% of the product catalog was never purchased. Not once. That's huge if you're managing inventory or marketing spend. Two — January and October through December are clear peaks. Classic seasonal pattern, found automatically. Three — February to September is flat. Possible marketing gap. I didn't go looking for any of this. I asked a question, ran the script, asked Claude to explain the output, and these patterns surfaced. That's the interpret step in action.

---

### Slide 08 · Setup

OK so how do you actually set this up? One command — you install the MCP server, Claude opens the Google OAuth flow, you authenticate in about two minutes, and then you're done. From that point, you just point Claude at any sheet URL and describe your question. The full setup guide, the dataset from this demo, and the script are all on GitHub — link is on screen. Give it a try on your own data and let me know what you find. See you next week.

---
