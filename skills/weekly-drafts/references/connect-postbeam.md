# Connect Postbeam

Postbeam is a remote MCP server (HTTP) with OAuth sign-in. Its name is `postbeam` and its address is `https://app.postbeam.ai/mcp`.

Every path ends with the user signing in to Postbeam in a browser window, which you cannot do for them.

## Claude app (web, desktop, mobile, Cowork)

- If Postbeam Starter is installed as a plugin: Customize → Plugins → Postbeam Starter → Connectors, then Connect next to Postbeam and sign in.
- If it is not: Customize → Connectors, search for "Postbeam", then Connect and sign in. Installing the Postbeam Starter plugin adds it too.
- If the app says they cannot add connectors, their workspace owner has to enable Postbeam first.

## ChatGPT (web, desktop, mobile)

1. They open Plugins in the sidebar, or go to `chatgpt.com/plugins`, and search for "Postbeam".
2. They select the plus button next to Postbeam, or open it if it is already added, and sign in to their Postbeam account when asked.
3. They come back to this chat. If the Postbeam tools still do not show up, they start a new chat and run the setup again.

In a company workspace, an admin may have to allow the plugin first.

## Claude Code

- Check `/mcp` first. If `postbeam` is listed, because Postbeam Starter is installed as a plugin or because Postbeam is already connected on their Claude account, they pick it and authenticate.
- If it is not listed, which is the usual case after `npx skills add`, they run this in a terminal:

  ```
  claude mcp add --transport http postbeam https://app.postbeam.ai/mcp
  ```

- Then they restart Claude Code, run `/mcp`, pick `postbeam` and authenticate.

## Cursor

1. They add Postbeam to `~/.cursor/mcp.json` (all projects) or `.cursor/mcp.json` (this project only). If the file already lists other servers, `postbeam` goes next to them inside `mcpServers`:

   ```json
   {
     "mcpServers": {
       "postbeam": { "url": "https://app.postbeam.ai/mcp" }
     }
   }
   ```

2. They restart Cursor and sign in to Postbeam when Cursor asks. If it does not ask, they open Customize in Cursor's sidebar, find `postbeam` and sign in from there.

## Codex

1. They run these two commands in a terminal. The second one opens the browser to sign in:

   ```
   codex mcp add postbeam --url https://app.postbeam.ai/mcp
   codex mcp login postbeam
   ```

2. They restart Codex.

The Codex CLI, IDE extension and desktop app share this setup. In the desktop app the same thing is under Settings → MCP servers, with an Authenticate button. They can also add the Postbeam plugin from the Plugins Directory there, as in ChatGPT.

## Something else

Give them the facts at the top of this file and ask them to add Postbeam the way their agent adds MCP servers. Most agents need a restart afterwards.
