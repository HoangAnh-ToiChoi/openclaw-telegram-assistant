# OpenClaw Telegram Assistant

An AI assistant built with OpenClaw. It runs on an Ubuntu 24.04 server (AWS EC2) and is controlled through a Telegram bot.

## Features
- Chat with the AI assistant on Telegram (bot: @f8_openclaw_bot)
- Access control: only allowed Telegram users can chat (allowlist)
- Task 1: clone a GitHub repository to the server by sending a message
- Task 2: search the web and summarize the results
- Runs in the background as a systemd service and restarts automatically

## How to use
1. Open Telegram, find @f8_openclaw_bot and press Start.
2. Send a request in plain language. Examples:
   - Clone a repo: "Hãy clone repo https://github.com/octocat/Hello-World về server"
   - Web search: "Hãy tìm trên web các khóa học Pro của F8 và tóm tắt lại"
3. The assistant replies in the same chat with the result.

## Setup summary
- Server: Ubuntu 24.04 on AWS EC2 (non-root user "openclaw")
- Installed tools: GCC, Node.js, Homebrew, Google Cloud CLI, gog CLI, OpenClaw
- AI model: Google Gemini (API key is stored only on the server)
- Channel: Telegram bot created with @BotFather, with an allowlist of Telegram user IDs
- Gateway: OpenClaw gateway running as a systemd user service

## Notes
- Secrets (bot token, API keys, OAuth files) are NOT stored in this repository.
- Replies can take 10-30 seconds on a small server.
