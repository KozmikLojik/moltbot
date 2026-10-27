# MoltBot Workspace

A small workspace repository for configuring and experimenting with a MoltBot/Clawdbot-style assistant. The current repository contains agent guidance files and a standalone canvas bridge demo; it does **not** include the bot runtime, installation scripts, or deployment configuration.

## Repository layout

- `clawd/AGENTS.md` — workspace conventions, memory workflow, and safety guidance.
- `clawd/SOUL.md` — assistant behavior and boundaries.
- `clawd/IDENTITY.md` — template for the assistant's identity.
- `clawd/USER.md` — template for user preferences and context.
- `clawd/TOOLS.md` — local environment notes template.
- `clawd/HEARTBEAT.md` — optional periodic-check instructions; currently disabled.
- `clawd/BOOTSTRAP.md` — first-run identity setup conversation.
- `clawd/canvas/index.html` — interactive canvas bridge test page.

## Canvas demo

Open `clawd/canvas/index.html` in a browser to inspect the UI. The buttons send actions through the host application's `clawdbotSendUserAction` bridge. They will not perform bot actions in an ordinary browser without that bridge; the page reports when the bridge is missing.

## Setup notes

This repository only supplies workspace files. To use them, place the `clawd/` workspace in the directory expected by your installed bot runtime, following that runtime's official setup instructions. Runtime commands and supported configuration can differ by version, so verify them against the version you have installed.

## Security and privacy

- Do not commit API keys, access tokens, passwords, private keys, or session cookies.
- Keep personal long-term memory and daily logs out of this public repository unless you have deliberately reviewed and sanitized them.
- Review any user-specific details in `USER.md` and local machine details in `TOOLS.md` before publishing.
- Treat agent instructions and tool access as security-sensitive configuration. Require confirmation before actions that send messages, publish content, spend money, or modify external systems.
- Test integrations with dummy data and least-privilege credentials first.

## Current scope

This is currently a workspace/configuration starter, not a complete standalone chatbot application. A useful next milestone is to document the exact runtime/version this workspace targets and add a reproducible, safe setup checklist once that environment is confirmed.
