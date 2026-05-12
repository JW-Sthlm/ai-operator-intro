# Exercise 2: Pick your scenario

> **Time:** ~8 min
> **Format:** Self-paced. Pick the scenario closest to your real work.
> **Goal:** Apply Copilot CLI to a consulting workflow you actually do

> 💡 **Read-only by default.** All four scenarios analyze and draft. Nothing is sent, posted, or saved to a CRM unless you do it yourself afterward. "Draft" prompts produce text for you to review.

The prompts are starting points. Rephrase them. If you're not sure what to type, describe what you want in plain English. Copilot understands.

## Before you start

You should already have Copilot CLI running in a working folder. If you completed Exercise 1, you're set. If not:

```
copilot
```

Pick **one** scenario from the four below. Run it on your real work where possible. Adjust customer or partner names to your own.

## Scenario A: RFP triage

*Best for: pre-sales, account managers, delivery managers, anyone who responds to RFPs*

Save an RFP (or any structured customer document) as `rfp.txt` or `rfp.pdf` in your working folder. If you don't have one to hand, use this stand-in:

```
RFP: Cloud Modernization, Northwind Retail

Section 1: Current state
- 47 internal applications, mostly Java + Oracle
- 2 data centers, end-of-life refresh in 18 months
- 800 employees, IT team of 42

Section 2: Required capabilities
- Migrate workloads to public cloud
- 99.95% availability SLA for tier-1 systems
- Zero-trust security model
- AI roadmap: chat assistant for customer service in year 1

Section 3: Evaluation criteria
- Demonstrated migration experience (case studies required)
- Total cost of ownership over 5 years
- Implementation timeline
- Local presence in DACH region
- AI/ML practice depth

Section 4: Submission requirements
- Executive summary
- Technical approach
- Team CVs
- Pricing
- 3 customer references
```

Save as `rfp.txt`. Then prompt:

```
@rfp.txt You're a senior bid manager helping me triage this RFP. Tell me:

1. The three things in this RFP that are easy wins for us (assume we're a mid-sized Microsoft partner with strong Azure and AI practices).
2. The two things that will sink us if we ignore them.
3. The single requirement that's a deal-shaper. If we nail this section, we likely win.
4. A draft executive summary, 200 words max. No buzzwords.
5. The honest "should we bid?" answer with reasoning.

Be direct. Don't hedge.
```

**Follow up:**

```
Rewrite the executive summary in the customer's voice. Pretend the buyer is reading it. Does it answer "why should I trust these people?"
```

## Scenario B: Deal narrative for a tough internal review

*Best for: account executives, sellers, anyone shaping a deal review*

Sketch the basics of a real or imagined opportunity in `deal.txt`:

```
Opportunity: Contoso Manufacturing
- $1.2M ARR target, year 1
- Currently using a competitor's cloud + analytics stack
- Internal champion: Head of Digital Transformation
- Detractor: CFO. Two failed digital projects in last 3 years.
- Timeline: decision by end of Q2
- Our differentiator: integrated AI + manufacturing operations toolkit
- Risk: customer wants 30 days of free POC. We have a 14-day standard.
- Open question: do we offer the extended POC or hold the line?
```

Then prompt:

```
@deal.txt You're prepping me for a deal review with my VP. Build me:

1. The "why we win" story in 90 seconds. Real reasons, not slogans.
2. The "why we lose" story. What kills this deal if it dies.
3. The CFO's actual objection. Not the one she'll say. The one she's holding.
4. Three sharp questions my VP is going to ask me. Draft my honest answers.
5. The POC decision: lay out the trade-off. Then take a side.

Channel a senior partner. Direct, no spin.
```

**Follow up:**

```
Now write the 30-second version I'd open the review with. Lead with the punch.
```

## Scenario C: Post-meeting recap and follow-up

*Best for: anyone running customer or partner meetings (everyone)*

Paste rough notes from a recent meeting into `meeting-notes.txt`. Don't clean them up. Real ugly notes are perfect.

If you need a stand-in:

```
30 min call with Litware (Maria, Per, Daniel) - Tue 14:30

- Maria opens: project is "fine" but quietly nervous
- Per (tech lead): integration test environment is broken since release 12.3
  Two weeks. Nobody on his team can fix without our help.
- Daniel (their PM): wants written commitment on the Jan 15 go-live
- I dodged the date. Said "let's see by Friday"
- Action: I'll get Sara to look at the test env tomorrow
- Action: Maria sending the dependency list
- Maria stayed on after the call - said board is "watching"
- Vibe: 6/10, was 8/10 last month. Trust slipping.
```

Then prompt:

```
@meeting-notes.txt Build me a clean post-meeting recap.

1. Two-line summary, factual.
2. Decisions and actions, with owners and dates.
3. Open questions.
4. A short read on the relationship temperature. Honest.
5. A follow-up email to Maria. Warm, but addresses the "board is watching" comment. Not panic-mode. Confidence-mode.

If anything in my notes is unclear or contradictory, flag it.
```

## Scenario D: Marketing campaign brief

*Best for: partner marketing, business development, anyone shaping go-to-market*

Sketch a campaign idea in `campaign.txt`:

```
Campaign idea: "AI in 30 Days"
- Target: mid-market customers (250-2000 employees)
- Sectors: financial services, manufacturing, retail
- Offer: a 30-day, fixed-price AI assistant pilot
- Goal: 20 qualified opportunities in Q1
- Channels: email, LinkedIn, partner events
- Asset gaps: case studies (have 2, need 4), pricing model (TBD)
- Open: should we co-brand with Microsoft or stand alone?
```

Then prompt:

```
@campaign.txt Help me turn this into a campaign brief I could hand to my agency.

1. The one-sentence value prop a customer would actually quote back.
2. The audience cut. Which sector lands fastest, and why.
3. The hero asset (the one thing they need to read or watch).
4. The honest co-brand call: stand alone or co-brand with Microsoft? Take a side, defend it.
5. The first email subject line. Optimize for open rate by being specific and human, not clever.

Be opinionated. Marketing briefs that try to please everyone die in the inbox.
```

## Tips that work across all four

- **Talk to it.** "Show me my projects that are behind schedule" works as well as carefully crafted prompts.
- **Ask it to explain itself.** "Why did you pick those?" or "What tool did you use?" Copilot will tell you.
- **Push back.** "That's not what I meant. The CFO isn't worried about cost, she's worried about timeline." Copilot adjusts.
- **Shorter follow-ups.** "Sharper." "Less corporate." "Plain English." "Cut a third." All work.
- **When it's wrong**, say so. "That didn't work. What went wrong?" is a valid prompt.

## Finished early?

Try a second scenario. Or invent your own. The pattern is the same: drop in context with `@`, ask for the shape of output you want, iterate.

## Reflect

When you wrap, think about:

- Could this become a workflow you run every week?
- Where's the delta vs. what M365 Copilot already does for you?
- Could a colleague run this same workflow if you wrote it down?

That third question is the gateway to skills (see [Exercise 3](exercise-03-your-copilot-passport.md)).

## What's next

📋 [The cheat sheet](../reference/cheat-sheet.md) has reusable prompt shapes and all key commands.

📚 [After-session resources](../reference/after-session-resources.md) point to deeper material when you're ready.

🔧 [Troubleshooting](../reference/troubleshooting.md) for the common stuck-points.
