# Your first conversations

> ⏱️ **Estimated time:** 20 min
> 🎯 **You'll be able to:** drive the CLI confidently for summarize, rewrite, and draft tasks. Know when to start a new session and when to keep going.

---

## The three modes you'll use

Copilot CLI has three modes. You'll use them all naturally. Helpful to know they exist.

| Mode | What it is | When to use |
|------|-----------|-------------|
| **Ask** (default) | Type a question, get an answer | "Summarize this." "What does this mean?" |
| **Agent** | It can run commands, edit files | "Find all PDFs in this folder." "Add a row to this CSV." |
| **Plan** | It explains what it would do *before* doing it | High-stakes tasks. Anything touching real files. |

You don't switch modes manually. The CLI picks based on what you ask. If it asks "want me to run this command?", that is agent mode asking permission.

⚠️ Always read what it is about to do. *Always.* Especially anything that says "delete" or "overwrite".

---

## 🚀 Hands-on: four conversations to try right now

Open a fresh PowerShell. Type `copilot`. Wait for the prompt. Now run these in order.

### 1. Summarize

📖 Paste this into the CLI:

> Imagine you advise a Microsoft partner on AI services. A customer asks: "what's the difference between Azure OpenAI and Microsoft Foundry?" Give me a 4-bullet answer for a non-technical exec.

**What you should get:** a structured 4-bullet response. Decent first draft.

What a session looks like in the terminal:

```text
PS C:\Users\you> copilot
✦ Copilot CLI · ready
> Imagine you advise a Microsoft partner on AI services...

  • Azure OpenAI Service: ...
  • Microsoft Foundry: ...
  • Where they overlap: ...
  • The exec takeaway: ...

> _
```

**Try one follow-up:**

> Now make it shorter. Two bullets. Same audience.

Notice the CLI remembers what you asked before. That is the conversation context.

### 2. Rewrite

📖 Paste this:

> Rewrite this in plain language for an exec audience: "We propose to leverage cross-functional synergies to drive accelerated value realization across the partner ecosystem through optimized workload distribution."

**What you should get:** something that doesn't sound like a robot wrote it.

### 3. Draft

📖 Paste this:

> Draft a 6-line email to a customer asking to schedule a 30-min call to align on their AI roadmap. Friendly tone, single ask, suggest two time slots next week.

**What you should get:** a usable draft. Tweak the times, send.

### 4. Reason about something

📖 Paste this:

> A customer is a mid-market retailer in the Nordics, around 800 employees. They currently use Dynamics 365 and want to add an AI use case. What three pilot use cases should they consider first and why?

**What you should get:** opinionated, not generic. Real reasoning. The CLI is good at this.

---

## How to keep a session productive

After 5 to 10 messages your session is full of context. Good when you are refining one thing. Bad when you switch topics.

**Rule of thumb:** start a new session when you switch tasks.

- Same customer, different angles. Keep going.
- New customer, new task. Exit (`/exit`), reopen (`copilot`), start fresh.

You'll get a feel for it. Costs nothing to start fresh.

⚠️ **Don't drag old context across topics.** If you ask about Customer A then Customer B in the same session, Copilot may bleed Customer-A details into the Customer-B answer. Embarrassing. Just `/exit` between customers.

---

## Useful slash commands

Type `/` inside copilot to see the menu. The ones you'll actually use:

| Command | Does |
|---------|------|
| `/exit` | Leaves the session |
| `/login` / `/logout` | Auth |
| `/help` | Lists everything |
| `/mcp` | Shows what MCP servers are connected (covered in lesson 4) |

⬆️ at the prompt brings back your previous prompts. Good for tweaking the same prompt with small variations.

---

<details>
<summary><strong>⚠️ Things that go wrong</strong>: quick reference, click to expand</summary>

📖

| What happens | Why | What to do |
|--------------|-----|------------|
| Answer is wrong or made up | Copilot doesn't actually know about your specific customer or product | Give it more context. Drop in the customer's website URL or a recent press release. |
| Answer keeps repeating | You're stuck in a context loop | `/exit` and start fresh |
| It refuses to do something | Safety filter triggered | Rephrase. If it is a legit ask, push back with context. |
| Suspiciously confident answer | LLMs hallucinate | Spot-check anything specific (numbers, names, dates) |

</details>

---

## 🎯 Try this on your real work

📖 **Pick one task you'll do this week** (a customer email, a status update, a meeting summary) and run it through Copilot CLI before doing it the old way.

Compare the time. Compare the quality. That is the only validation that matters.

---

## ✅ Ready to move on if

- You've had at least one useful conversation
- You know how to `/exit` and start fresh
- You can tell when a conversation has drifted and you should reset

---
