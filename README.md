# OpenClaw Telegram Assistant

AI assistant built with OpenClaw, running on an Ubuntu 24.04 server (AWS EC2) and controlled through a Telegram bot.

## Features
- Chat with the AI assistant through Telegram (bot: @f8_openclaw_bot)
- Access control: only allowed Telegram IDs can chat (allowlist)
- Task example: clone a GitHub repo to the server by sending a message to the bot
- Runs as a background service (systemd), starts again after reboot

## How to use
1. Open Telegram and find @f8_openclaw_bot, then press Start.
2. Send a message, for example: "Hãy clone repo https://github.com/octocat/Hello-World về server".
3. The assistant replies with the result and the folder where the repo was cloned.

## Setup summary
- Server: Ubuntu 24.04 on AWS EC2, non-root user "openclaw"
- Tools: Node.js, Homebrew, gog CLI, OpenClaw
- Model: Google Gemini (API key stored on the server, not in this repo)
- Channel: Telegram bot created with @BotFather

## Notes
Secrets (bot token, API keys) are NOT stored in this repository.
