# Speaker Notes — Post 01: I Built an AI Agent to Stop Procrastinating

---

## Slide 1 — Title

Hi, I'm Anastasia. I'm a Business Analyst, and for about 6 months I was saying "I really should start writing about AI." Just saying it, not doing it. And last week an AI Agent finally made me stop talking and actually publish something. Today I want to show you exactly what I built and how it works — because if you've been procrastinating on something similar, this might help you too.

---

## Slide 2 — The Problem

So here's what was stopping me. It wasn't a lack of ideas. It was the format problem. Every week I wanted to post on LinkedIn, create slides for YouTube, AND write a script for recording — and doing all three from scratch every single week felt like too much. On top of that, whenever I tried using AI to help, the output just didn't sound like me. It was too polished, too generic. Not honest enough.

---

## Slide 3 — The Concept

So what I built is called a Claude Code Skill. Think of it like a briefing document you write once — and every time the agent runs, it already knows who you are before it does anything. It knows your voice, your audience, your tone. Instead of explaining yourself from scratch every week, you just describe your topic and share your story. The persona stays consistent automatically.

---

## Slide 4 — How It Works

The skill has three sections. The first is the Persona — it describes who I am, how I write, and who reads my content. That loads before any generation happens. The second section is "Before you start" — and this is important — before Claude writes anything, it asks me four questions. What's the topic, what number is this post, do I have a real story to share, and is there anything to avoid. That last question matters a lot, because it keeps the output specific, not generic. The third section is the Output — it defines exactly what to generate and where to save it.

---

## Slide 5 — Running It

Here's what actually running it looks like. I open my terminal in my project folder — I named it "AI girl Anastasia," which sounds a bit funny but honestly it makes me feel like I'm building something real. I run Claude Code, and I type `/weekly-content`. That's it. Claude reads the skill, asks me the 4 questions, and then generates three files — the LinkedIn post, the slides you're looking at right now, and the speaker notes I'm reading from. All saved to the right place automatically.

---

## Slide 6 — Before vs After

Before I had this: zero posts published, a lot of vague plans, and a pattern of "I'll start next week." After: I answer four questions, get three files, adjust maybe 10 to 20 percent, commit, push, done. The key shift isn't that AI does the work for me — I still review and edit everything. The key shift is that the hardest part, starting from a blank page, is gone.

---

## Slide 7 — How to Set It Up

If you want to try this yourself, it takes about 5 minutes to set up. You copy the skill folder into your Claude project, restart Claude Code, and the `/weekly-content` command is available. Then you just run it and answer four questions. Everything else is handled. I'll put the full setup guide and the skill files on GitHub — link is on the next slide.

---

## Slide 8 — Connect

That's it for today. The full skill, the folder structure, all the files — everything is on GitHub at AIgirlAnastasia. If you try it, I'd genuinely love to know how it goes. Come find me on LinkedIn or here on YouTube. This is week one for me. Let's see how consistent I can be.
