# Exercise 1: Build your customer briefing

> **Time:** ~8 min
> **Format:** Guided start, then explore on your own
> **Goal:** Use Copilot CLI to build a real customer briefing from notes you already have

> 💡 **Read-only by default.** The prompts below read files and synthesize output. They don't send emails, create CRM records, or modify anything. If Copilot ever proposes to create or change something, you'll see it before it runs. Review then approve.

The prompts are starting points. Rephrase them. Shorten them. Talk to Copilot like a colleague. There's no syntax to memorize.

## Before you start

You need a working folder and a notes file in it. Both are quick.

1. **Open a folder you can write to.** If you don't have one, ask Copilot:

   ```
   Create a folder called ai-operator-intro in my projects directory and open it.
   ```

   Any files Copilot reads (with `@`) or creates will live here.

2. **Add a notes file.** Save the block below as `customer-notes.txt` in your working folder, or use a real one of your own if you have it.

   ```
   Discovery call notes. Acme Retail, 12 Nov.

   - Mid-sized European retail chain, ~140 stores, ~3,400 employees.
   - Pain: Black Friday and Christmas peaks crash their on-prem analytics.
       Last year they couldn't ship a single promo dashboard in time.
   - CEO wants "real-time" sales visibility. Doesn't have a definition yet.
   - Tech estate: SQL Server on-prem, Power BI, some Azure (storage only).
       No data engineering team. Two analysts who live in Excel.
   - Budget signal: open to a 6-week pilot. Annual capex decision in Feb.
   - Buying group: CFO (sponsor), CIO (skeptic), Head of E-Com (champion).
   - Competition: another partner pitched a Snowflake migration last spring.
       Customer didn't buy. CFO said "too far, too fast."
   - Open question: what's the minimum we can show by end of Jan that
       proves real-time is real?
   ```

That's it. You have a folder and a file. Move on.

## Part A: Build the briefing, guided (4 min)

In your working folder, launch Copilot CLI:

```
copilot
```

Paste this prompt:

```
@customer-notes.txt Build me a structured customer briefing for an internal meeting tomorrow. Use this shape:

- One-line customer summary
- The real pain (not the surface ask)
- Buying group: who's in, what each cares about, who's the blocker
- Where this deal stops if we don't address something specific
- Three sharp questions we should ask in the next call
- A "minimum credible Jan demo" idea, given everything in the notes
- Risks I should flag to my account team before the meeting

Be opinionated. If the notes don't support a section, say so. Don't pad.
```

**What good looks like:** A briefing that reads like a senior colleague wrote it. Not a regurgitation of the notes. Calls out the CFO blocker. Names the Snowflake-shaped trauma. Picks a real Jan demo angle.

> ⚠️ **Common trap.** If you get back the notes reformatted as bullets, the prompt was too soft. Tell Copilot: <em>"That's just my notes restructured. I want analysis. Take a position."</em>

## Part B: Explore (4 min)

Try one or two follow-ups. Pick whatever's closest to your real work.

**Sharpen the Jan demo:**

```
Take the "minimum credible Jan demo" idea and turn it into a one-slide pitch I could send to the CIO. Plain language. No buzzwords. Make the value land in the first sentence.
```

**Pressure-test the deal:**

```
Play devil's advocate. What are the three reasons this deal does not close? Be honest. If you think we're underweight on something, say so.
```

**Draft the follow-up email:**

```
Draft a short follow-up email to the Head of E-Com (the champion). Reference the Jan demo idea. Propose a 30-minute working session to nail the scope. Warm tone, not pushy.
```

**Compare two customers:**

If you have notes on another customer in the same folder, try:

```
Now do the same briefing for @other-customer-notes.txt. How is the buying motion different from Acme? Where would I prioritize my time this week?
```

## What you just did

- ✅ Pointed Copilot at a real file with `@`. The file became context, not chat history.
- ✅ Asked for analysis, not a summary. Got back something opinionated.
- ✅ Iterated. Each follow-up sharpened the output, no setup required.

**The shape that matters:** This is the same pattern for an RFP, a partner deck, a meeting transcript, a customer email thread. Drop a file in, ask for the shape of output you want, iterate.

## What's next

➡️ [Exercise 2: Pick your scenario](exercise-02-pick-your-scenario.md) for more practice on your own data.

📋 Want a prompt reference? Open the [cheat sheet](../reference/cheat-sheet.md).

🔧 Something stuck? Check [troubleshooting](../reference/troubleshooting.md).
