# Connect optional tools

Every tool here is optional. Help with the ones the user picked and nothing else. Give them only the section for where they are running. They sign in themselves.

## Claude app (web, desktop, mobile, Cowork)

- If you can show connector suggestions with a connect button, do that for the tools they picked.
- If Postbeam Starter is installed as a plugin: Granola, Fireflies, Slack, Gmail and Microsoft 365 are listed at Customize → Plugins → Postbeam Starter → Connectors. They select Add or Connect next to the tool.
- For any other tool, or without the plugin: Customize → Connectors, search for the tool, then Connect.

Outlook and Teams connect through Microsoft 365, one connector that also covers calendar and files. On a work Microsoft account, their Microsoft admin may have to approve it once. If the app says they cannot add a connector at all, their workspace owner has to add it first.

## ChatGPT (web, desktop, mobile)

- They open Plugins in the sidebar, or go to `chatgpt.com/plugins`, search for the tool, select the plus button next to it and sign in.
- The plugins there are named Granola, Fireflies, Slack, Gmail, Outlook Email and Teams. Zoom has one too. Outlook and Teams are separate plugins, so they add only the one they want read.
- If a tool has no plugin in the directory, use the fallback below.

## Claude Code

- Check `/mcp` first. It lists the tools that come with Postbeam Starter when it is installed as a plugin (`granola`, `fireflies`, `slack`, `gmail`, `microsoft365`) and the connectors already on their Claude account. They pick the tool and authenticate. The ones they don't want can stay unauthenticated.
- For a tool that is not listed, they follow that tool's own MCP setup instructions and add it with `claude mcp add`.

## Cursor, Codex and other agents

- They follow the tool's own MCP setup page for their agent. Do not make up an address. If you are not sure one exists, tell them to search for "<tool> MCP server".
- Some tools only offer a connector inside Claude. If theirs has none for their agent, use the fallback below.

## Everywhere

- No connector for a tool: they can paste notes or a transcript into the chat each week, or answer the interview questions for that part.
- A newly connected tool that does not show up yet: finish the setup with what is available, and tell them that running the setup again later adds it to the routine.
- An optional tool is never a condition for finishing.
