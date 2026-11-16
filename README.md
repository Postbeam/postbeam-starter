# Postbeam Starter

Get fresh LinkedIn drafts in [Postbeam](https://www.postbeam.ai) every week, written in your voice from what actually happened in your work.

Postbeam Starter is a plugin for Claude. It connects Claude to your Postbeam account and adds a guided setup that asks which of your work tools Claude may read, writes a first batch of drafts with you, and then schedules the routine so new drafts are waiting each week. Nothing is ever published or scheduled to LinkedIn by the routine. Every post waits in Postbeam as a draft until you approve it.

## What you need

A Postbeam account is the only requirement. Every other connector is optional, and you choose which ones to use during setup.

| Connector | Needed? | What the routine uses it for |
| :--- | :--- | :--- |
| Postbeam | Required | Reads your voice training and recent posts, saves the new drafts |
| Granola | Optional | Meeting notes and transcripts from the past week |
| Fireflies | Optional | Call transcripts from the past week |
| Slack | Optional | Decisions, customer questions and wins from work channels |
| Gmail | Optional | Threads with customers, prospects and partners |
| Microsoft 365 | Optional | Outlook email and Teams chats, for people who don't use Gmail or Slack |

On a work Microsoft account, your IT admin may need to approve the Microsoft 365 connector once before you can connect it.

Use a different call recorder? Fathom, Otter, Gong, Zoom and others work the same way. Connect the tool under **Customize**, then **Connectors**, and pick it during setup.

If you would rather not connect any of the optional tools, the routine asks you a few short questions about your week instead and drafts from your answers.

## Install

In Claude on the web or in the desktop app:

1. Open **Customize**, then **Plugins**.
2. Select **Add**, then **Add marketplace**, and enter `Postbeam/postbeam-starter`.
3. Add **Postbeam Starter**.
4. Open the plugin's **Connectors** tab and connect Postbeam. Connect any of the optional tools you want to use.

If Postbeam Starter appears under **Discover**, you can add it from there instead of adding the marketplace.

In Claude Code:

```
/plugin marketplace add Postbeam/postbeam-starter
/plugin install postbeam-starter@postbeam-starter
```

## Use it

Start a chat and say:

> Set up my weekly drafts

or pick `/postbeam-starter:weekly-drafts` from the slash menu. Claude then takes you through the setup:

1. Confirms Postbeam is connected and which account the routine is for.
2. Checks your Postbeam voice training.
3. Shows the optional tools and lets you pick any, all or none.
4. Proposes the routine: 3 drafts, Monday at 8am, looking back 7 days. Change whatever you like.
5. Runs it once with you. You approve the three moments before anything is written.
6. Schedules the weekly run, or hands you a prompt to reuse if your Claude has no scheduling.

Each week the routine picks moments worth posting about (a story from a call, an opinion you shared, a lesson from a deal or pitch, a question you keep getting asked), writes one draft per moment, saves them to Postbeam with a note on where each idea came from, and sends you a short summary.

To change the schedule, add a tool or stop the routine, run the setup again.

## Privacy and data

- The plugin contains only instructions and connector addresses. It runs no code and stores nothing itself.
- Claude reads only the tools you approve during setup, read-only, for the past week. Tools you decline are written into the routine as never to be read.
- Client names, private numbers and deal terms are left out of drafts unless they are already public.
- Drafts and their source notes are sent to your Postbeam account through `app.postbeam.ai`. Sign-in is OAuth, and the plugin ships no credentials.
- The optional connectors (Granola, Fireflies, Slack, Gmail and Microsoft 365) are not run by Postbeam. Connecting one signs you in to that connector under its own terms.
- Postbeam's [privacy policy](https://www.postbeam.ai/privacy-policy) covers what Postbeam does with your drafts and account data.

## Support

- Website: [postbeam.ai](https://www.postbeam.ai)
- Email: support@postbeam.ai

## License

MIT
