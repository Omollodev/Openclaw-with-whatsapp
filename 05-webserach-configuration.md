# Web Browser

## Browser (OpenClaw-managed)

OpenClaw can run a dedicated Chrome/Brave/Edge/Chromium profile that the agent controls. It is isolated from your personal browser and is managed through a small local control service inside the Gateway (loopback only). Beginner view:

    Think of it as a separate, agent-only browser.
    The openclaw profile does not touch your personal browser profile.
    The agent can open tabs, read pages, click, and type in a safe lane.
    The built-in user profile attaches to your real signed-in Chrome session via Chrome MCP.

**Note:** There are several types of broswer and you need to chose the easier to set-up 

**searXNG** 
    is one of the best web browser tool i need to use cause it's use to /plug -to-play tool.

### Quick start

```bash
openclaw browser --browser-profile openclaw status
openclaw browser --browser-profile openclaw start
openclaw browser --browser-profile openclaw open https://example.com
openclaw browser --browser-profile openclaw snapshot
```

