# Troubleshooting

The eight most common stuck-points and how to get past them. If you're hitting something not on this list, open an issue at [github.com/JW-Sthlm/ai-operator-intro/issues](https://github.com/JW-Sthlm/ai-operator-intro/issues).

## 1. `winget` not found

You're on Windows but typing `winget` says "not recognized".

**Fix:** Open the Microsoft Store. Search for "App Installer". Install it. It includes `winget`. Then restart PowerShell and try again.

**If you can't install App Installer** (locked-down corporate laptop), use [GitHub Codespaces](https://github.com/features/codespaces) instead. Free tier includes 60 hours a month. Open a codespace from any repo and run `copilot` there. Everything in the course works the same way.

## 2. `copilot` command not found after install

You ran the install, it succeeded, but `copilot` doesn't work.

**Fix:** Close ALL PowerShell and terminal windows. Reopen a fresh one. The PATH only refreshes for new windows.

**Still missing?** Try reinstalling:

```
winget install GitHub.Copilot
```

**Last resort:** restart your computer. Sometimes Windows needs the reboot.

## 3. `/login` fails or times out

You ran `copilot`, typed `/login`, browser opened, but something broke.

**Possible causes:**

1. Your Copilot subscription isn't active.
2. A corporate proxy is blocking the device-code flow.
3. Your browser blocked the pop-up.

**Fix:**

- Verify your subscription at [github.com/settings/copilot](https://github.com/settings/copilot). If you don't see "Copilot Free is active" or one of the paid plans, activate Free there.
- Try the login on a personal network (home wifi, mobile hotspot). Corporate proxies sometimes block the device-code flow.
- Check your browser allowed the pop-up. Some browsers silently block them.

## 4. `gh auth login` shows `not_found` error

The browser shows `/login/device/failure?reason=not_found`.

**Cause:** You pasted a stale device code. Every new `gh auth login` invalidates all previous codes. Only the most recent one works.

**Fix:** Don't re-run `gh auth login`. Look at your terminal. The most recent code shown there is still valid. Go to [github.com/login/device](https://github.com/login/device) and paste that code.

## 5. MCP servers not showing in `/mcp`

You installed an MCP server (filesystem, M365, GitHub, whatever) but `/mcp` doesn't list it.

**Fix:** Did you run `/restart` after the install? MCP servers register when Copilot CLI starts. New ones don't appear until you restart.

```
/restart
```

**Still missing?** Ask Copilot directly. It can diagnose:

```
My MCP servers aren't showing up. Can you help me diagnose and fix this?
```

**If you want to look manually:** check that `~/.copilot/mcp-config.json` exists and is valid JSON. A typo there breaks everything.

## 6. M365 MCP install says "needs admin approval"

You tried to install the M365 MCP server. It failed with an admin-consent error.

**Cause:** Your Microsoft 365 tenant (your company's M365) blocks third-party app consent by default. This is normal corporate hygiene.

**Fix options:**

1. **Ask IT to approve the app.** They can grant tenant-wide consent for the M365 MCP server. Send them the GitHub Marketplace link.
2. **Skip M365 for now.** The course works fine without it. Use filesystem MCP and GitHub MCP instead. Every pattern in the course transfers.

## 7. Copilot gives wrong or irrelevant answers

The output doesn't match what you asked for.

**Tips that fix most cases:**

- **Be more specific.** "In the customer notes about Acme Retail's CFO concerns" beats "look at my notes".
- **Tell it what's wrong.** "That's not what I meant. The CFO isn't worried about cost, she's worried about timeline." Copilot adjusts.
- **Reset context.** If the conversation has been long, type `/compact` to summarize it. Or just close Copilot and restart.
- **Switch model.** Different models behave differently. Try `/model` and pick another one if the current one is off.

## 8. "Rate limit exceeded"

You hit your monthly Copilot request limit.

**Fix:** Wait until next month. Or upgrade to Copilot Pro at [github.com/settings/copilot](https://github.com/settings/copilot). Free includes a generous monthly allowance but heavy use can run through it.

## Still stuck?

1. **Ask Copilot first.** Type `I'm having trouble with [describe the problem]`. It can often help you diagnose.
2. **Search GitHub issues.** [github.com/JW-Sthlm/ai-operator-intro/issues](https://github.com/JW-Sthlm/ai-operator-intro/issues). Someone may have hit the same thing.
3. **Open a new issue.** Include your OS, what you typed, and the exact error. Screenshots help.
4. **Check the official docs.** [docs.github.com/copilot](https://docs.github.com/copilot) for everything that's not in this guide.
