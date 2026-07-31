# Daily Quote Bot 🤖

An n8n automation that sends a random inspirational quote to Telegram every day.

## How it works

1. **Schedule Trigger** — runs automatically once a day at a set time
2. **HTTP Request** — fetches a random quote from the [ZenQuotes API](https://zenquotes.io/api/random)
3. **Telegram** — sends the quote to a Telegram chat via a custom bot

## Workflow

## Setup

1. Import `daily-quote-workflow.json` into your n8n instance
2. Create a Telegram bot via [@BotFather](https://t.me/BotFather) and get your bot token
3. Get your Telegram Chat ID by messaging your bot, then visiting:
   `https://api.telegram.org/bot<TOKEN>/getUpdates`
4. Add your bot token as a credential in the Telegram node
5. Set your Chat ID in the Telegram node
6. Publish/activate the workflow

## Tech stack

- [n8n](https://n8n.io/) — workflow automation
- [ZenQuotes API](https://zenquotes.io/) — quote source
- [Telegram Bot API](https://core.telegram.org/bots/api) — message delivery

## Note

Credentials (bot token, chat ID) are **not** included in the exported JSON for security — you'll need to set these up yourself when importing.
