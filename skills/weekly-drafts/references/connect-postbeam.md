# Connect Postbeam

Postbeam is a remote MCP server (HTTP) with sign-in. Its name is `postbeam` and its address is `https://app.postbeam.ai/mcp`.

Give the user only the section for where they are running. Every path ends with them signing in to Postbeam in a browser window, which you cannot do for them. When they say it is done, try `list_accounts` again.

## Claude app (web, desktop, mobile, Cowork)

- If Postbeam Starter is installed as a plugin: Customize → Plugins → Postbeam Starter → Connectors, then Connect next to Postbeam and sign in.
- If it is not: Customize → Connectors, search for "Postbeam", then Connect and sign in. Installing the Postbeam Starter plugin adds it too.
- If the app says they cannot add connectors, their workspace owner has to enable Postbeam first.

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

The Codex CLI, IDE extension and desktop app share this setup. In the desktop app the same thing is under Settings → MCP servers, with an Authenticate button.

## Something else

Tell them Postbeam is a remote MCP server that uses HTTP and sign-in (OAuth), with the name `postbeam` and the address `https://app.postbeam.ai/mcp`, and ask them to add it the way their agent adds MCP servers. Most agents need a restart afterwards.
