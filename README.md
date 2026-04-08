# TapKit Plugin Marketplace for Claude Code

Control a physical iPhone from Claude Code. Take screenshots, tap, swipe, type, and navigate apps — all through natural language.

## Installation

**Prerequisites:** [Claude Code](https://claude.ai/code), the TapKit Mac app running with a connected iPhone, and Switch Control enabled on the iPhone.

1. Add the marketplace in Claude Code:
   ```
   /plugin marketplace add Jootsing-Research/tapkit-plugins-claude
   ```
2. Run `/plugin`, open the **Marketplaces** tab, select `tapkit-plugins-claude`, browse plugins, and enable **tapkit**.
3. Run `/reload plugins`.
4. Run `/mcp`, select **TapKit**, and choose **Authenticate** to sign in via the browser.
5. Run `/exit` and restart Claude Code.

Verify by asking: *"Take a screenshot of my phone."*

Full instructions: [docs.tapkit.ai/integrations/claude-code](https://docs.tapkit.ai/integrations/claude-code)

## What You Get

The **tapkit** plugin connects Claude Code to a real iPhone via [TapKit](https://tapkit.ai). Once installed, you can tell Claude things like:

- "Take a screenshot of my phone"
- "Open Settings and turn on Do Not Disturb"
- "Order my usual from Uber Eats"
- "Check the weather in Tokyo"
- "Send a message on Telegram"

The plugin ships with the [TapKit MCP server](https://github.com/Jootsing-Research/tapkit-mcp) (gestures, screenshots, app control) plus a set of [skills](plugins/tapkit/skills) that teach Claude how to navigate specific apps.

## How It Works

```
Claude Code  →  TapKit MCP Server  →  Physical iPhone
   (you)        (mcp.tapkit.ai)        (your device)
```

Claude sees the phone screen through screenshots and interacts through tap/swipe/type commands. The core loop is always: **screenshot → look → act → screenshot to verify**.

## Requirements

- [Claude Code](https://claude.ai/code) CLI or desktop app
- A TapKit account at [tapkit.ai](https://tapkit.ai)
- A connected iPhone

## License

MIT
