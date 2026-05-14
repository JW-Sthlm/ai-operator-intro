# Track exercise: Deal-shaping for a Cloud and AI Platform opportunity

> **Time:** ~15 min
> **Format:** Self-paced, opinionated
> **Goal:** Use Copilot CLI to pressure-test and shape a CAIP (Cloud and AI Platform) opportunity end-to-end

This exercise pairs with the [Frontier Consultancy](https://aka.ms/frontierconsultancy) CAIP track. That track covers the technical delivery side. This one covers the commercial side. You can run both, or just this one if your role is account management, sales, or business development.

## What's a CAIP opportunity?

The Microsoft "Cloud and AI Platform" solution area. Customer wants to modernize infrastructure, migrate to Azure, build a foundation for AI workloads, or do all three. Typical signals: aging on-prem, end-of-life hardware refresh, a cloud-curious CTO, a board mandate for AI.

For this exercise you'll work a single opportunity from "first qualification" to "go/no-go recommendation".

## Setup

Save the block below as `opportunity.txt` in your working folder. Or use a real opportunity of your own.

```
Opportunity: Konsum Industries
Sector: industrial distribution, family-owned, ~€800M revenue, ~2,800 staff
Geography: Nordics, with a recent Polish acquisition (still integrating)

Trigger event:
- Q3 board meeting voted to "modernize the data platform". Vague mandate.
- New CFO (joined March) is asking what the IT estate actually costs
- The Polish acquisition runs SAP. Konsum runs Oracle EBS + custom apps.
  The CIO is six months into a hairball integration project that's late.

Stakeholders we know:
- CIO: knows we exist, polite but not pushy. Burned by a prior cloud project at her last company.
- Head of Analytics: a real champion. Wants out of Excel. Has a Power BI license but no data engineers.
- CFO: unknown to us. Joined from a manufacturing company that did a "Snowflake-first" play.
- CEO: family heir, second-generation. Tech-curious. Was at Slush last year and "saw what AI agents can do".

Competitive landscape:
- Snowflake reseller has been on-site twice. Pitched a data platform play.
- A Big Four firm is on the integration project for SAP-Oracle.
  They're rumored to be drafting a "cloud strategy" for the CIO.

Constraints:
- The CIO wants no decisions before the SAP-Oracle integration stabilizes (Q2 next year)
- The CFO wants visibility on cloud TCO now
- The board is impatient. Expects "AI traction" within 12 months.

Open questions:
- What do we lead with: data platform, AI proof-of-value, or full Azure migration?
- Do we engage the CFO directly or stay close to the CIO?
- Is this a CAIP-first deal or an AI Business Solutions (AIBS) play in CAIP clothing?
```

## Part A: First qualification (5 min)

Launch Copilot CLI in the folder, then paste:

```
@opportunity.txt You're a senior account executive helping me qualify this opportunity. I need you to take a position, not list options.

1. Is this a real opportunity or a wishlist? Honest assessment.
2. The "hidden buyer". Who actually decides this, regardless of titles. Make the case.
3. The deal shape. Is this CAIP, AIBS, or a mix? Why?
4. The minimum 3-month plan: what do we sell first, to whom, and how does it earn the second sale?
5. The single biggest risk that this deal evaporates.

Channel real-world consulting voice. No hedging. Take sides.
```

**What good looks like:** A piece of analysis that picks the CFO as hidden buyer (or makes a different case but defends it), names the AI-trauma risk, and proposes a wedge.

## Part B: Pressure-test against the competition (5 min)

```
Two competitors are circling. Snowflake reseller (data platform) and a Big Four firm (cloud strategy doc for the CIO).

For each one:
- What's their honest strength against us in this deal?
- What's their weakness we should exploit?
- What's the "they win this" scenario? What does the customer have to believe for us to lose?

Then: my counter-positioning, in one sentence each. Specific, not slogan-shaped.
```

**Follow-up:**

```
The CFO came from a Snowflake-first shop. How does this change the playbook? If she's the hidden buyer, are we toast unless we co-pitch with Snowflake?
```

## Part C: Build the go/no-go pack (5 min)

```
Build me a tight go/no-go pack to take to my regional VP. Format:

- Opportunity in 30 seconds (the elevator version)
- Why we win (3 reasons, real ones)
- Why we lose (2 reasons, brutal)
- The deal we should actually pursue (not the deal they think they want)
- The 6-week proof point that earns us the right to scale
- The ask: what do I need from the regional VP to move this forward?

The VP has 15 minutes and reads fast. No fluff.
```

## What you just did

- ✅ Took a messy real-world opportunity and forced structure on it.
- ✅ Used Copilot as a sparring partner, not a notepad. The "take a position" framing matters.
- ✅ Pressure-tested against named competitors. This is the part most account teams skip.
- ✅ Built a deal-review artifact you could actually send to a leader.

## Reflect

- Would the go/no-go pack survive a real VP review?
- Where did Copilot push back well? Where did it just agree with you?
- If you ran this on every CAIP opportunity in your pipeline, how much time would you save? How much sharper would your pipeline reviews be?

That third question is the door to building this as a skill (see [Exercise 3](exercise-03-your-copilot-passport.md)).

## What's next

- Pair this with the [Frontier Consultancy CAIP track](https://aka.ms/frontierconsultancy) when the technical proof point starts shaping up.
- Try the same flow on an AIBS opportunity (data, agents, Copilot Studio) or a Security opportunity (Defender, Sentinel, Entra).
- Build a `caip-deal-review` skill so this workflow runs on every opportunity, not just the ones you remember.
