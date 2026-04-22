# What is OpenClaw?

    OpenClaw is a self-hosted messaging gateway that connects WhatsApp, Telegram, Discord, and iMessage to AI coding agents.
        The gateway is a single long-running process on your machine that maintains persistent connections to messaging platforms (WhatsApp, Telegram, Discord, etc.).
        When a message arrives on any channel, the gateway routes it to an agent that can execute tools locally—file operations, shell commands, browser automation letting you self-host the entire stack: you own the connections, the config, and the execution environment.

How is OpenClaw different from Claude Code?

    OpenClaw is fully self-hosted on your machine, with many more supported integrations.

# Installation Process

Prerequisites

    Node ≥22 (node -v)

Installation & First Run
```bash
npm install -g openclaw@latest \
openclaw onboard --install-daemon
```
The --install-daemon flag installs the gateway as a background service (launchd on macOS, systemd on Linux). This means the gateway starts automatically on boot and keeps running—you don’t need a terminal open. The onboarding wizard walks you through config path, workspace location, and channel pairing.


See: Install, Onboarding Wizard
Useful Commands
```bash
openclaw status — Show channel health and recent sessions
openclaw health — Fetch health from the running gateway
openclaw security audit --deep — Audit config with live gateway probe
openclaw security audit --fix — Apply safe fixes to tighten security
openclaw doctor — Health checks and quick fixes for gateway
```
TUI Interface

    many helpful commands

Workspace & Memory
Key Concepts

    Config, credentials, sessions live under ~/.openclaw/.

See: Agent Workspace
Git backup

    Treat workspace as private memory; init git, add private remote, .gitignore secrets.

See: Git backup