# TinyBulb

Make browser games feel finished and play well on phones, then publish them on [TinyBulb](https://tinybulb.com), where anyone can play them from a link.

## What's in the plugin

- **The `building-web-games` skill** teaches Claude what makes a browser game hold up: touch controls, phone layouts, loading screens, game feel, a complete loop from title to game over, testing at phone sizes, and cover art.
- **The TinyBulb connector** lets Claude publish a game for you. Its tools are `publish_game`, `update_game`, `get_game` and `read_bundle_format`. It needs no sign-in.

## How to use it

After you add the plugin, open its **Connectors** tab and add TinyBulb. Then ask Claude for what you want, for example:

- "Make a tap-to-jump game and publish it on TinyBulb"
- "Make my game play well on phones"
- "Publish my game on TinyBulb"
- "What does a game need to go on TinyBulb?"

Claude builds the game and sends it to TinyBulb, which checks it. If something needs fixing, Claude gets each problem with how to fix it and tries again. When the game passes, Claude gives you a link: open it, play the game exactly as players will, and click Publish. You sign in with Google only at that step, and nothing is public before it.

To change a game later, ask Claude to update it.

## What it sends, and where

The plugin runs no code of its own. It sends data only when you ask Claude to publish or check a game:

- Your game's files go to TinyBulb, through the connector at `mcp.tinybulb.com` or, where Claude can run commands, to `api.tinybulb.com` with `curl`.
- Claude may read TinyBulb's published rules from `tinybulb.com`.
- Where Claude can run commands, it may open the game's link in your browser.

Read the [privacy policy](https://tinybulb.com/privacy) and [terms](https://tinybulb.com/terms).

## Troubleshooting

- **Claude can't reach TinyBulb:** open the plugin's **Connectors** tab and check that TinyBulb shows as connected.
- **Publishing takes a long time in a chat:** in a chat, Claude has to write the whole game into the upload, images included, so it's slow and suits small games. Claude Code uploads a zip file instead, so publish bigger games from there.
- **The link stopped working:** links expire. Ask Claude to send the game again for a new one.
- **Anything else:** see the [help pages](https://tinybulb.com/help) or write to support@tinybulb.com.
