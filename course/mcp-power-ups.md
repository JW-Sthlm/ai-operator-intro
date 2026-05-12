# MCP power-ups: GitHub, M365, and more

> ⏱️ **Estimated time:** 20 min
> 🎯 **You'll be able to:** install MCP servers, connect Copilot CLI to your inbox, calendar, and repos, and have it pull real data into your work.

---

<details>
<summary><strong>📖 "What MCP is, in plain English"</strong>: concept + table, click to expand</summary>

📖 An **MCP server** is a small program that gives Copilot access to a system. Instead of you copy-pasting from Outlook into the CLI, an MCP server lets the CLI **read your inbox directly** when you ask.

Think of it as a translator between Copilot and a system.

| MCP server | Gives Copilot access to | Why you care |
|------------|------------------------|--------------|
| **GitHub MCP** | Issues, PRs, repos | Pull a list of open repos into a status update. Comes built in. |
| **M365 MCP** | Your inbox, calendar, files in OneDrive | "What's on my calendar tomorrow with Contoso?" |
| **Filesystem MCP** | Any folder on your laptop | Read across many documents at once without copy-paste |
| **Notion / Atlassian / others** | Your internal notes and tickets | Same idea. Whatever system your team lives in. |

You don't write the MCP server. Other people do. You install and use it.

</details>

---

## ⚠️ The install prompt that confuses everyone

When you install an MCP server, Copilot CLI asks:

> Where do you want to configure these MCP servers?

You'll see a numbered menu. **Pick option 2: Copilot CLI.**

```text
Where do you want to configure these MCP servers?

  1. VS Code (Copilot Chat)
❯ 2. Copilot CLI
  3. GitHub Copilot Coding Agent (copilot-setup-steps.yml)
  4. Other
  5. Other (type your answer)
```

The other options install the MCP somewhere Copilot CLI can't find it (the VS Code workspace, GitHub-side runners, etc.) and it silently fails.

If you pick the wrong one and your MCP is missing later, re-run the install and pick option 2.

---

## 🚀 GitHub MCP comes built in

📖 GitHub MCP ships with Copilot CLI. No separate install. You can use it right now.

Open a CLI session:

```
> What are the latest issues on the github/docs repo?
```

Or:

```
> List my recent activity on GitHub.
```

It will fetch real data from your real GitHub account. No copy-paste.

**Verify what's connected:**

```text
> /mcp

Configured MCP servers:
  github   ✓ built-in   (47 tools)

Type a prompt to use them.
```

---

## 🚀 Install M365 MCP (your inbox + calendar + files)

📖 M365 MCP unlocks the "wow" use cases for business-side partner roles. Your real inbox. Your real calendar. Your real OneDrive files.

In a CLI session:

```
> Install the M365 MCP server.
```

Follow the prompts. When asked where to install, pick option 2 (Copilot CLI).

After install, try:

```
> What's on my calendar tomorrow?
> Summarize emails I got from Contoso this week.
> Find the most recent file I worked on with the word "QBR" in it.
```

⚠️ **First-time consent.** Microsoft will ask you to consent to the MCP reading your inbox. Read the consent screen. It will list permissions like `Mail.Read`, `Calendars.Read`. These are read-only by default. Don't grant write permissions you don't need.

⚠️ **Tenant gating.** Some companies block third-party app consent. If M365 MCP install fails with a consent error, that is your IT policy talking. Ask your admin, or skip this MCP and use file-drop context instead (lesson 3).

---

## 🚀 Optional: filesystem MCP for cross-document work

📖 The filesystem MCP lets Copilot read multiple folders without you `cd`-ing into each one.

```
> Install the filesystem MCP server with read access to my Documents folder.
```

Then:

```
> Look across my Documents folder. What customer briefs have I drafted in the last 30 days? Summarize the common themes.
```

Powerful for partner marketing roles and account managers who keep a library of past briefs and want to mine it.

---

<details>
<summary><strong>📖 "Combining MCP servers in one prompt"</strong>: the magic moment, click to expand</summary>

📖 Once you have multiple MCPs installed, the magic happens:

```text
> Look at my calendar next week. For every meeting with a customer name in the title,
> check my email for the latest thread with that customer. Draft a 3-bullet pre-meeting
> brief for each one.
```

Calendar plus email queried in one prompt. Briefs generated in batch. Try it. It feels like the future.

</details>

---

<details>
<summary><strong>🆘 "When MCP doesn't work"</strong>: troubleshooting, click to expand</summary>

| Symptom | Cause | Fix |
|---------|-------|-----|
| MCP not in `/mcp` list | Installed in wrong location | Reinstall, pick option 2 (Copilot CLI) |
| M365 says "no permissions" | Consent screen was declined | Reinstall, accept consent |
| M365 install errors with "admin approval required" | Your tenant blocks third-party app consent | Ask your IT admin, or use file-drop context instead |
| Slow / hangs | First-time auth bouncing through browser | Be patient, ~10 sec on slow networks |
| "Tool not available" | MCP not running | Restart Copilot CLI |

For deeper issues see [troubleshooting.md](../reference/troubleshooting.md).

</details>

---

## 🎯 Real-work test: a partner update from MCP

📖 Pick a customer you have an active engagement with. In Copilot CLI:

```
> Check my email for messages I've exchanged with anyone @ <customer domain> in the last 30 days.
> Then check my calendar for meetings with that customer in the same window.
> Draft a 5-bullet update for my manager: status, last meeting, blockers, next step, ask.
```

If this works, you just compressed 30 minutes of clicking into one prompt.

---

## ✅ You've cleared the value bar 📖

If you can:

- Use the built-in GitHub MCP without thinking about it
- Install at least one additional MCP and verify it shows in `/mcp`
- Combine MCP data with prompt context to produce a useful artefact

Then you've achieved the productivity bar. You can drive Copilot CLI for partner work end-to-end.

**Stop here. Ship some real work. Come back later if you want to go deeper.** This course intentionally ends at the point where you get value without writing code.

---
