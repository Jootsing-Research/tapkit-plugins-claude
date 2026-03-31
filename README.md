# TapKit Plugin Marketplace for Claude Code

Control a physical iPhone from Claude Code. Take screenshots, tap, swipe, type, and navigate apps — all through natural language.

## Installation

```bash
# Add the marketplace
/plugin marketplace add Jootsing-Research/tapkit-plugins-claude

# Install the tapkit plugin
/plugin install tapkit@tapkit-plugins-claude
```

## What You Get

The **tapkit** plugin connects Claude Code to a real iPhone via [TapKit](https://tapkit.ai). Once installed, you can tell Claude things like:

- "Take a screenshot of my phone"
- "Open Settings and turn on Do Not Disturb"
- "Order my usual from Uber Eats"
- "Check the weather in Tokyo"
- "Send a message on Telegram"

### MCP Tools

The plugin provides these tools through the TapKit MCP server:

| Tool | Description |
|------|-------------|
| `screenshot` | Capture the current screen |
| `tap` | Tap at coordinates |
| `double_tap` | Double-tap at coordinates |
| `long_press` | Long press at coordinates |
| `swipe` | Swipe between two points |
| `drag` | Drag from one point to another |
| `hold_and_drag` | Hold then drag |
| `copy_text_to_phone` | Copy text to the phone's clipboard for pasting |
| `open_app` | Open an app by name |
| `spotlight` | Search via Spotlight |
| `press_home` | Go to the home screen |
| `lock` / `unlock` | Lock or unlock the device |
| `volume_up` / `volume_down` | Adjust volume |
| `activate_siri` | Trigger Siri |
| `run_shortcut` | Run a Siri Shortcut |
| `list_phones` / `select_phone` | Manage connected devices |
| `get_phone_info` | Get device details |
| `escape` | Dismiss modals and keyboards |
| `enable_switch_control` | Enable Switch Control accessibility |

### Skills

The plugin includes 11 skills that teach Claude how to navigate specific apps and workflows:

| Skill | Description |
|-------|-------------|
| **tapkit** | Core iPhone control — gestures, screenshots, typing, and navigation patterns |
| **clock** | Set alarms, timers, stopwatch, and world clocks |
| **facebook** | Browse feed, Marketplace, Reels, groups, and messaging |
| **hinge** | Browse profiles, send likes and roses, message matches |
| **instagram** | Browse feed, Reels, stories, DMs, and profile management |
| **linkedin** | Browse feed, connect with people, search jobs, and messaging |
| **telegram** | Send messages, browse chats, join groups, and interact with bots |
| **tiktok** | Browse For You feed, like and comment on videos, follow creators |
| **twitter** | Browse feed, compose posts, create threads and polls |
| **uber-eats** | Search restaurants, browse menus, and place delivery orders |
| **weather** | Check forecasts, air quality, UV index, and manage saved cities |

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

## Author

[Jootsing Research](https://jootsing.ai) — tj@jootsing.ai
