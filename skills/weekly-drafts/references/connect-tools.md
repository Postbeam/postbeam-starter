# Connect optional tools

Steps for connecting the optional tools the user picked, by where they are running.

## Claude app (web, desktop, mobile, Cowork)

- If Postbeam Starter is installed as a plugin: Granola, Fireflies, Slack and Gmail are listed at Customize → Plugins → Postbeam Starter → Connectors. They select Add or Connect next to the tool.
- For any other tool, or without the plugin: Customize → Connectors, search for the tool, then Connect.

Outlook and Teams connect through the Microsoft 365 connector at Customize → Connectors (it is not one of the plugin's connectors), one connector that also covers calendar and files. On a work Microsoft account, their Microsoft admin may have to approve it once. If the app says they cannot add a connector at all, their workspace owner has to add it first.

## ChatGPT (web, desktop, mobile)

- They open Plugins in the sidebar, or go to `chatgpt.com/plugins`, search for the tool, select the plus button next to it and sign in.
- The plugins there are named Granola, Fireflies, Slack, Gmail, Outlook Email and Teams. Zoom has one too. Outlook and Teams are separate plugins, so they add only the one they want read.
- A tool with no plugin in the directory has no connector in ChatGPT.

## Claude Code

- Check `/mcp` first. It lists the tools that come with Postbeam Starter when it is installed as a plugin (`granola`, `fireflies`, `slack`, `gmail`) and the connectors already on their Claude account, including Microsoft 365 if they connected it in the Claude app. They pick the tool and authenticate. The ones they don't want can stay unauthenticated.
- For a tool that is not listed, they follow that tool's own MCP setup instructions and add it with `claude mcp add`.

## Cursor, Codex or something else

- They follow the tool's own MCP setup page for their agent. Do not make up an address. If you are not sure one exists, tell them to search for "<tool> MCP server".
- Some tools only offer a connector inside Claude, so theirs may have none for their agent.
