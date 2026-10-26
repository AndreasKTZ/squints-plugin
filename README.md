# Squints for Claude Code

Point at an element in the browser with [Squints](https://chromewebstore.google.com/detail/aapcfeiigjccdealkigbpnjdpanpfolb), and Claude knows exactly which one you mean: its selector, styles, the design tokens its values match, and the component that rendered it.

- **"Make this 24px."** Select an element with Squints' Inspect tool and say "this". Shift-click several and say "these".
- **"Which card do you mean?"** When more than one element could fit, Claude asks you in the browser instead of guessing. Squints outlines each candidate on the page and you confirm one, or click the one you meant.
- **`/squint`** always uses your selection, e.g. `/squint make these cards the same height`.

## Install

In Claude Code:

```
/plugin marketplace add AndreasKTZ/squints-plugin
/plugin install squints@squints
```

Then start a new session, and open Squints on your page (Alt+S). It connects within a few seconds.

You need the [Squints extension](https://chromewebstore.google.com/detail/aapcfeiigjccdealkigbpnjdpanpfolb) for Chrome and Node.js 20 or later.

## What Claude can see

Only pages you share. Local development sites (localhost, 127.0.0.1, `*.localhost`, `*.test`) are shared automatically; any other site only after you turn it on in Squints' Settings. Everything stays on your machine: the plugin runs a small local server that only the Squints extension can connect to. No screenshots are sent.

To pause sharing, turn off **Share with agents** in Squints' Settings. To remove the plugin, run `/plugin uninstall squints@squints`.

## Other agents

Cursor, Codex, VS Code and other MCP clients can use the same server through npm:

```
npx -y squints-mcp
```
