# How-to-Report-n8n-Workflow-Errors-to-Telegram-
This guide shows you how to build a robust error-reporting system for your n8n workflows using Telegram. This setup is completely free if you are using the self-hosted version of n8n.
Prerequisites
n8n Instance: Either n8n Cloud (Trial/Paid) or Self-Hosted (Free).
Telegram Account: Free account to create the bot and receive messages.
Part 1: Set up your Telegram Bot
Before configuring n8n, you need a "mailbox" (Bot) and a "address" (Chat ID) to send the errors to.
1. Create the Bot
Open Telegram and search for @BotFather.
Start a chat and send the command /newbot.
Follow the prompts to name your bot (e.g., "My n8n Alerts").
Save the API Token given to you (it looks like 123456:ABC-DEF1234ghIkl-zyx57W2v1u123ew11).
2. Get your Chat ID
Search for your new bot username in Telegram and click Start (or send a message like "Hello").
Open your browser and visit this URL (replace <YOUR_TOKEN> with your actual token):
https://api.telegram.org/bot<YOUR_TOKEN>/getUpdates
Look for the "chat" object in the response. Copy the id number (e.g., 987654321).
Note: If the result is empty {"ok":true,"result":[]}, send another message to your bot and refresh the page.
