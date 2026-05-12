# Exercise 3: Build your first skill

> **Subtitle:** A reusable Copilot CLI workflow for your day-to-day
> **Time:** 20–25 min
> **Format:** Talk to Copilot. Let it create the files. Inspect only if you want to.
> **Goal:** Build a small reusable skill you can take back to your real work.

## Why this exercise

Copilot CLI has a few building blocks under the hood. **Instructions** describe how you work. **Skills** describe reusable workflows. **Agents** create scoped helpers. **MCP servers** connect tools. **Plugins** bundle the lot.

Building a skill is the fastest way to understand them. You don't hand-write JSON or learn a framework. You describe work you repeat often, ask Copilot CLI to turn it into a skill, and test that the right prompt triggers the right behavior.

## What you'll build, pick one

| Option | What it does | Best fit |
|--------|--------------|----------|
| **Customer briefing skill** | Pulls customer notes from a folder and produces a structured briefing. | Account managers, delivery leads, anyone running customer meetings |
| **Meeting prep skill** | Given a calendar event or rough notes, drafts an agenda with context and questions. | Anyone with recurring stakeholder meetings |
| **Status update skill** | Turns recent notes or messages into a weekly update for a manager, team, or customer. | Project leads, workstream owners, managers |

Pick work you already repeat. Small is good. A skill that saves 10 minutes every week beats an impressive demo you never use again.

## Build steps, talk to Copilot

### Step 1: Understand the shape of a skill

Paste this into Copilot CLI:

```
I want to build my first skill. Show me what files a skill needs, in plain language. Don't show me code yet. I'm not a developer, just someone who repeats the same kind of prompt every week.
```

**Expected outcome:** Copilot explains the main pieces. The `~/.copilot/skills/<your-skill-name>/` folder. The `SKILL.md` file. The trigger description that tells Copilot when to use the skill. Optional reference files for templates or examples.

Ask follow-up questions in plain English. `What's the minimum I actually need?` is a great one.

### Step 2: Scaffold your skill

Replace `<your-skill-name>` with a short, folder-style name like `customer-briefing`, `meeting-prep`, or `status-update`.

```
Scaffold a new skill called <your-skill-name> in ~/.copilot/skills/. Create the folder and a starter SKILL.md. Keep it minimal. Ask me only if you need a decision.
```

**Expected outcome:** A new folder appears at `~/.copilot/skills/<your-skill-name>/` with a starter `SKILL.md`.

If Copilot asks what the skill should do, answer like you'd brief a colleague.

### Step 3: Write the trigger and instructions

Use one of the prompts below as a starting point, then adapt it to your own work.

**Customer briefing example:**

```
Given a folder of customer notes (any .txt or .md file), write the SKILL.md trigger description and instructions for a Customer Briefing skill. The output should include: customer summary, real pain (not surface ask), buying group with each person's stake, deal-stopping risks, three sharp questions for the next call, and a recommended next step.

Keep the trigger description specific so it activates when I ask things like "build me a briefing on Acme Retail" but doesn't fire on every customer-related prompt.
```

**Meeting prep example:**

```
Given a calendar event description and any related notes in the current folder, write the SKILL.md trigger description and instructions for a Meeting Prep skill. The output should include: purpose, attendees (and what each cares about), proposed agenda, context to read first, and three questions I should ask.
```

**Status update example:**

```
Given recent notes, emails, or meeting summaries, write the SKILL.md trigger description and instructions for a Status Update skill. The output should include: headline, work completed this week, blockers, decisions needed, and what's planned next week.
```

**Expected outcome:** Copilot updates your `SKILL.md` with trigger phrases and step-by-step instructions.

Focus on the output you want. Sections, tone, and usefulness matter more than file structure.

### Step 4: Test that the skill activates

Reload Copilot CLI so it picks up the new skill:

```
Reload my skills so the new one is available.
```

Then try a natural trigger prompt. Example for a customer briefing skill:

```
Use my customer briefing skill on the notes in @customer-notes.txt.
```

**Expected outcome:** Copilot recognizes the skill, follows the instructions in `SKILL.md`, and produces the artifact you asked for.

If it doesn't trigger, ask:

```
Why didn't my new skill trigger? Review the SKILL.md trigger description and make it more explicit. What phrases would naturally activate it?
```

The test passes when the output is useful enough to improve your next real meeting or update.

### Step 5: Explain it and share it

Paste this:

```
What did we just build, and how would I share this skill with a colleague who's also using Copilot CLI?
```

**Expected outcome:** Copilot summarizes the skill in plain language and gives you a simple sharing path. Copy the skill folder. Send the `SKILL.md`. Package it as a plugin later if it becomes a team asset.

Practice the 30-second explanation: <em>"I built a skill that turns X into Y when I ask Z."</em>

## What good looks like

You're done when:

- The skill folder exists at `~/.copilot/skills/<your-skill-name>/`.
- The skill triggers on phrases you'd naturally use.
- The output is useful for real work, not just the workshop.
- You can explain to a peer what you built and when you'd use it.

## Stretch: turn it into a plugin

A skill is enough for personal use. If you want to share it as a packaged team asset, turn it into a plugin later. Add a `plugin.json`. Keep the skill under `skills/<name>/`. Document the install path.

The [GitHub Copilot CLI docs on agent skills](https://docs.github.com/en/copilot/concepts/agents/about-agent-skills) cover the structure if you want to go deep.

## What's next

- Use your skill once this week on real work.
- Share the folder with one colleague and ask whether the trigger makes sense to them.
- Keep the [cheat sheet](../reference/cheat-sheet.md) handy. Check [after-session resources](../reference/after-session-resources.md) for what to learn next.
