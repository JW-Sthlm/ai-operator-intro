# Copilot CLI cheat sheet

> For partner consultants. Print this or keep it open during and after the course.

## The #1 rule

**Just talk to it.** You don't need to memorize commands or syntax. Type what you want in plain English:

- `Help me prep for the meeting with Acme tomorrow`
- `What went wrong with that last command?`
- `How do I add a new MCP server?`
- `Explain what you just did`

The prompts and commands below are useful shortcuts. Natural language always works. If you're stuck, ask: `How do I...`

## The CLI mental model

| Piece | What it is | Why you care |
|-------|------------|--------------|
| **Copilot** | The AI that ties everything together | The thing you talk to |
| **MCP servers** | Adapters that plug Copilot into other systems | Reach: filesystem, GitHub, M365, Notion, your own |
| **Instructions** | Rules that shape every output automatically | Write once, always active |
| **Skills** | Reusable workflows that trigger on phrases | Same job, repeat reliably |
| **Agents** | Scoped helpers for specific kinds of work | A "writing reviewer" or "deal shaper" you can summon |

You don't need to understand every piece on day one. Start with Copilot plus one or two MCP servers. Skills and agents come naturally as you spot work you repeat.

## Essential commands

Inside Copilot CLI (after running `copilot`):

| Command | What it does |
|---------|-------------|
| `/mcp` | See your connected MCP servers |
| `/model` | Switch AI model |
| `/plan` | Create a structured plan before executing |
| `/research` | Deep investigation with web search + citations |
| `/resume` | Pick up a previous session with full context |
| `/compact` | Summarize the conversation to free up context |
| `/skills` | Browse your available skills |
| `/restart` | Reload Copilot CLI so new MCP servers or skills register |
| `/help` | Show all commands |
| `/exit` | Leave Copilot CLI |

## Referencing files and folders

The `@` symbol points Copilot at files. It reads the file and uses it as context for the conversation.

| Syntax | What it does | Example |
|--------|-------------|---------|
| `@file` | Single file | `@notes.txt analyze these workshop notes` |
| `@folder/` | All files in a folder | `@customer-notes/ give me an overview` |
| `@file1 @file2` | Multiple files | `@rfp.txt @capability.md draft a response` |
| `#number` | GitHub issue or PR | `#42 what is this about?` |
| `!command` | Run a shell command | `!dir` |

💡 You don't need `@` for everything. If you're asking a question or working with data from MCP tools, plain language works. Use `@` when you have a specific file you want Copilot to read.

## Reusable workflow shapes

### Customer briefing

```
@customer-notes.txt Build me a structured customer briefing:
- One-line customer summary
- Real pain (not surface ask)
- Buying group with each person's stake
- Deal-stopping risks
- Three sharp questions for the next call
- Recommended next step
Be opinionated. Don't pad.
```

### Document analysis

```
@document.txt You're a senior reviewer. Tell me:
- The three things that matter most
- The two things that will sink us if we ignore them
- The single sentence I should quote when I share this with my team
Take a position.
```

### Post-meeting recap

```
@meeting-notes.txt Build me a clean recap:
- Two-line factual summary
- Decisions and actions with owners and dates
- Open questions
- Relationship temperature (honest)
- A short follow-up email I can send today
```

### Pipeline review (on a CSV or notes)

```
@pipeline.csv Sort these opportunities by where they're stuck.
For each stuck deal:
- The one thing that unblocks it
- Whether I should kill, defer, or accelerate
- A specific next-step
```

## MCP power-up prompts (if you have these MCPs installed)

### Filesystem MCP

```
Read every .txt file in this folder and find the three biggest themes across all of them.
```

```
Find the most recent customer notes file in ~/Documents/customers and build me a briefing from it.
```

### GitHub MCP (built in)

```
Show me the open issues on JW-Sthlm/ai-operator-intro tagged "bug". For each, suggest a fix.
```

```
Read the README of microsoft/semantic-kernel and tell me, in 200 words, what this is and whether it fits a partner I'm working with.
```

### M365 MCP (optional, tenant-gated)

```
What meetings do I have today? For each, find any relevant emails from the past two weeks.
```

```
Draft a follow-up email to the people on yesterday's 14:30 call. Reference the action items we agreed.
```

## Four properties that make CLI different

| Property | What it means |
|----------|--------------|
| **Tool-connected** | Calls real systems through MCP servers. Not guesses. |
| **Repeatable** | Same workflow, different input. Reusable patterns. |
| **Inspectable** | Output is an artifact (file, plan, doc), not a chat bubble that scrolls away. |
| **Persistent** | `/resume` continues where you left off, across days. |

## Self-study resources

- **Beginner course (developer-leaning, ~2h):** [Copilot CLI for Beginners on Learning Hub](https://awesome-copilot.github.com/learning-hub/cli-for-beginners/)
- **Official docs:** [docs.github.com/copilot/how-tos/copilot-cli](https://docs.github.com/copilot/how-tos/copilot-cli)
- **MCP servers directory:** [modelcontextprotocol.io/servers](https://modelcontextprotocol.io/servers)
- **Source course repo:** [github.com/github/copilot-cli-for-beginners](https://github.com/github/copilot-cli-for-beginners)

## Keyboard shortcuts

| Shortcut | Action |
|----------|--------|
| `Shift+Tab` | Cycle modes (suggest → autopilot) |
| `Ctrl+C` | Cancel current action |
| `Ctrl+C` × 2 | Exit |
| `Ctrl+L` | Clear screen |

## See also

- 📚 [After-session resources](after-session-resources.md). Deeper material when you're ready.
- 🔧 [Troubleshooting](troubleshooting.md). Common issues and fixes.
