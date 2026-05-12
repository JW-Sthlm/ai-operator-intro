# Why CLI for partner work

> ⏱️ **Estimated time:** 10 min reading
> 🎯 **You'll be able to:** decide whether this course is for you, and what you can realistically do with the CLI in your job.

---

## The pitch in one sentence

You can talk to GitHub Copilot from your terminal. It can read files, search your inbox, query your repos, and produce real artefacts. Faster than chat.com. More flexible than the Copilot button inside Word.

That is the whole pitch. The rest of this lesson is "is that actually useful for *your* job?"

<details markdown="1">
<summary><strong>Why bother with a CLI at all? Don't I already have M365 Copilot?</strong></summary>

Quick analogy. M365 Copilot is the librarian. You ask, it finds, it reads back to you. Copilot CLI is the contractor. You give it a job, it goes off and does it.

M365 Copilot is great at what it sees: your email, your calendar, your Office files. Ask it about a thread, it summarizes. Ask it to draft a reply, it does. It lives inside the M365 surface and stays there.

Copilot CLI is a different shape. It runs on your laptop, in your terminal, and it actually does things. Reads any file you point at. Runs commands. Calls APIs. Ties tools together that don't normally talk to each other.

What the CLI gives you that M365 Copilot doesn't:

1. **Reach beyond M365.** Through MCP connectors you plug in anything that exposes one: GitHub, Notion, Atlassian, your own filesystem, public APIs. M365 Copilot is fixed to what Microsoft ships. The CLI is open.
2. **Execute, don't just retrieve.** *"Read this 12-page RFP, draft a one-pager for our exec sponsor, save to my Desktop."* Ask once, it runs the whole chain. M365 Copilot can summarize. The CLI can do the work.
3. **Speak every other command-line tool for you.** Git, GitHub CLI, npm, the Azure CLI. You don't need to remember syntax. Tell Copilot what you want and it picks the tool.
4. **Live where your real work happens.** Your files, your scripts, your terminal. No tab-switching, no re-uploading.

Set it up once. Use it for real work after.

> **A taste of what's possible:** *"Find the last three customer meetings I had with Contoso, pull the press release they published last week, summarize what they probably want to discuss next, then draft a follow-up email for me to review."* Calendar plus public web plus your own notes plus Copilot reasoning, chained in one prompt. That is the CLI.

</details>

---

## Who this is for

Business-side roles at a Microsoft partner. Account managers. Sellers. Engagement managers. Delivery managers. Marketing. Business development. The people who own the customer relationship and the commercial side of partner work.

If your job is reading documents, writing documents, summarizing meetings, prepping for the next conversation, qualifying opportunities, shaping proposals: this course is built for you.

If you write code for a living, your version of this course lives at **Frontier Consultancy**. Different audience, different examples, more depth on the technical side.

---

## What this can replace in your day

Examples that actually work for business-side partner roles:

| Today you... | With Copilot CLI you... |
|--------------|--------------------------|
| Read a 12-page customer RFP, then write a 1-page summary | Drop the RFP in a folder, ask "summarize for an account exec" |
| Open Outlook, scroll the last week, write an update for your manager | Ask "summarize my emails with Contoso this month" via the M365 MCP |
| Click through five tabs to pull a partner pre-call brief | Point the CLI at the customer's website and a recent deck, get a brief in 30 seconds |
| Draft the same proposal intro for the fourth time this quarter | Reuse a previous one as a template, change the names, change the angle |
| Cross-reference a long call transcript with a 30-page proposal | One CLI session, both files, "find the misalignments" |

The pattern is the same every time. You provide the context (files, links, what you're trying to do). Copilot provides the structured output. You review and ship.

---

<details>
<summary><strong>What this is NOT</strong>: common confusions, click to expand</summary>

⚠️

- **Not VS Code Copilot.** That is the assistant inside an editor. Copilot CLI is a separate tool that runs in your terminal. They share an account. They are different products.
- **Not chat.copilot.microsoft.com / M365 Copilot.** That is a chat product for documents and meetings. The CLI is more flexible (talks to your filesystem, runs commands, accepts MCP servers). M365 Copilot is more polished for everyday office work. You'll use both.
- **Not autonomous.** It does what you ask, step by step. You stay in the driver's seat. It never sends an email or modifies a file without your say-so.

</details>

<details>
<summary><strong>"I'm not a terminal person"</strong>: the terminal thing demystified</summary>

📖 Fine. You don't need to be.

The terminal here is just a text-input window where you type natural language and get answers back. The same way you'd type into a chat box. Differences:

- It can read files in the folder you're in
- It can run commands when you tell it to
- It remembers context within a session
- You can press ⬆️ to recall a previous prompt (this alone is a productivity win)

That is it. If you can use a chat box, you can use this terminal.

</details>

---

## ⚠️ Data boundaries: read this

You will be tempted to drop everything into the CLI. Customer NDA content. Confidential proposals. Internal partner strategy decks. Be deliberate.

**Safe by default:**
- Public docs, customer websites, press releases
- Your own drafts and notes
- Anything you'd post in your team chat without thinking twice

**Stop and think first:**
- Customer-confidential content under NDA. Fine for *summarization* you keep internal. Not for content you send back externally without review.
- Internal partner strategy documents. Same rule.
- Anything labeled Confidential or Highly Confidential at your company. Check your data policy first.

**Never:**
- Anything you'd be uncomfortable seeing in a screenshot of the CLI window
- Credentials, tokens, customer personal data

The CLI sends what you give it to a Copilot endpoint hosted by GitHub. Treat it the same way you treat M365 Copilot or any other AI tool your company has approved.

---

<details>
<summary><strong>"Will I break anything?"</strong>: the safety story</summary>

📖 No. This course never asks you to:
- Delete files you didn't create
- Run scripts you don't understand
- Touch production systems
- Modify your inbox or calendar without an explicit confirmation prompt

The CLI can *read* a lot. To *change* anything (send an email, update a file, move something) it asks you first. You stay in the driver's seat.

</details>

---

## ✅ Ready to move on if you can answer these

1. What is one thing the CLI does that M365 Copilot doesn't? *(reads any file you point at, runs commands, talks to MCP servers, lives in your terminal)*
2. Who is this course for? *(business-side roles at a Microsoft partner)*
3. Name two things this is NOT. *(VS Code Copilot; M365 Copilot; autonomous AI)*
4. What's one thing in your week you'd hand to the CLI first? *(your answer here)*
5. What's one thing you should think twice before pasting into the CLI? *(customer NDA content, credentials, personal data)*

---
