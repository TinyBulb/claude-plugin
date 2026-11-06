# TinyBulb

Make browser games feel finished and play well on phones, then publish them on [TinyBulb](https://tinybulb.com), where anyone can play them from a link.

## What's in the plugin

- **The `building-web-games` skill** teaches Claude what makes a browser game hold up: touch controls, phone layouts, loading screens, game feel, a complete loop from title to game over, testing at phone sizes, and cover art.
- **The TinyBulb connector** lets Claude publish a game for you. Its tools are `publish_game`, `update_game`, `get_game` and `read_bundle_format`. It needs no sign-in.

## How to use it

Ask Claude something like "Make a tap-to-jump game and publish it on TinyBulb". Claude builds the game and sends it to TinyBulb, which checks it. If something needs fixing, Claude gets each problem with how to fix it and tries again. When the game passes, Claude gives you a link: open it, play the game exactly as players will, and click Publish. You sign in with Google only at that step, and nothing is public before it.

To change a game later, ask Claude to update it.

## What it sends, and where

The plugin runs no code of its own. It sends data only when you ask Claude to publish or check a game:

- Your game's files go to TinyBulb, through the connector at `mcp.tinybulb.com` or, where Claude can run commands, to `api.tinybulb.com` with `curl`.
- Claude reads TinyBulb's publishing rules from `tinybulb.com`.
- Where Claude can run commands, it may open the game's link in your browser.

Read the [privacy policy](https://tinybulb.com/privacy) and [terms](https://tinybulb.com/terms). For help, see the [help pages](https://tinybulb.com/help) or write to support@tinybulb.com.
