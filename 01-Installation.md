# Installation Process

## Prerequisites

    Node ≥22 (node -v)


### Installation & First Run

following the documentation from openclaw website link: 
    [openclaw-docs](https://docs.openclaw.ai/install)


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