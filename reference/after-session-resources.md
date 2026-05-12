# After-session resources

> Where to go next if you want to keep learning.

## Build your first skill

[Exercise 3](../exercises/exercise-03-your-copilot-passport.md) walks you through turning a workflow you repeat into a reusable Copilot CLI skill. Once you have one skill that saves you 10 minutes a week, you'll see the pattern everywhere.

## Track-flavored exercises

If your work touches the [Frontier Consultancy](https://github.com/JW-Sthlm/frontier-consultancy) tracks, the track-specific exercise pushes deeper on the commercial side:

- **[Deal-shaping for a Cloud and AI Platform opportunity](../exercises/track-caip-deal-shaping.md)**. Pressure-test a CAIP deal end-to-end.

More track exercises (AIBS, Security) are on the backlog.

## Self-paced learning

| Resource | What it is | Time |
|----------|-----------|------|
| **[This course](../course/README.md)** | The four-lesson consultant version you're already in | 70 min |
| [Copilot CLI for Beginners (source)](https://gh.io/copilot-cli-course) | The original GitHub course this is adapted from. Developer-focused. Eight chapters. Python sample app. | ~2 hours |
| [Course repo (Codespaces-ready)](https://github.com/github/copilot-cli-for-beginners) | Code, exercises, and a sample app to practice with | Self-paced |

## Recommended next steps

Try these in your first week after the course:

1. **Run `/init` in a project folder.** Copilot scans the folder and generates instruction files (`AGENTS.md`, `.github/copilot-instructions.md`) tailored to your work there. This teaches Copilot the conventions of that folder so every future conversation starts with context.

2. **Try the beginner course chapter on agents.** It walks through creating a custom `.agent.md` file in `~/.copilot/agents/` for a task you repeat often. Chapter 5 covers skills. Chapter 6 covers MCP servers in detail.

3. **Build one custom skill.** Pick a workflow you do every week. Use Exercise 3 to wrap it in a skill. Use it once. Then improve it.

## Official documentation

| Resource | What it covers |
|----------|---------------|
| [GitHub Copilot CLI docs](https://docs.github.com/copilot/how-tos/copilot-cli) | Full documentation. Setup, usage, skills, MCP, agents. |
| [CLI command reference](https://docs.github.com/copilot/reference/copilot-cli-reference/cli-command-reference) | Every slash command and keyboard shortcut |
| [About agent skills](https://docs.github.com/copilot/concepts/agents/about-agent-skills) | How skills extend Copilot CLI |
| [Adding MCP servers](https://docs.github.com/copilot/how-tos/copilot-cli/customize-copilot/add-mcp-servers) | Connect Copilot CLI to external tools and APIs |
| [Custom instructions](https://docs.github.com/copilot/how-tos/copilot-cli/customize-copilot/add-custom-instructions) | Teach Copilot CLI your conventions |

## MCP ecosystem

The MCP catalog grows weekly. A few good starting points:

| Resource | What it is |
|----------|-----------|
| [Model Context Protocol homepage](https://modelcontextprotocol.io) | Official MCP project site |
| [MCP servers directory](https://modelcontextprotocol.io/servers) | Curated list of community and official MCP servers |
| [Filesystem MCP](https://github.com/modelcontextprotocol/servers/tree/main/src/filesystem) | The one we recommend installing first |
| [GitHub MCP (built in)](https://docs.github.com/copilot/how-tos/copilot-cli/customize-copilot/add-mcp-servers) | Already there, no install needed |

## Copilot plans

| Plan | Best for |
|------|----------|
| Free | Most of this course. CLI included. Generous monthly allowance. |
| Pro / Pro+ | Heavy users. More requests, more models. |
| Business / Enterprise | Provided by your employer. Admin controls and bigger quotas. |

More on plans: [github.com/features/copilot/plans](https://github.com/features/copilot/plans)

## From this course

| Material | What it is |
|----------|-----------|
| [Cheat sheet](cheat-sheet.md) | Quick reference. Commands, workflow shapes, shortcuts. |
| [Troubleshooting](troubleshooting.md) | Top eight stuck-points and fixes. |
| [The four lessons](../course/README.md) | The course itself, browsable. |
| [Exercises](../exercises/) | Hands-on practice. Customer briefing, scenario pick, build a skill. |

## Companion: Frontier Consultancy

If you build the solutions (architects, engineers, developers), the [Frontier Consultancy](https://github.com/JW-Sthlm/frontier-consultancy) materials cover the technical AI-first delivery tracks (CAIP, AIBS, Security). This course is the commercial counterpart.

## License and attribution

Adapted from [GitHub's Copilot CLI for Beginners](https://gh.io/copilot-cli-course) (MIT). Re-skinned for partner consultants in business-oriented roles. Community and partner enablement material. Not an official Microsoft or GitHub product.
