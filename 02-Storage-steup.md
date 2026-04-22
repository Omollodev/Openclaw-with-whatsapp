# Key-Concept

During installation the workspace directory is the storgae location

    Workspace & Memory

![Workspace](/images/2.png)

    This is the config, credential, sessions live under:
```bash
    ~/.openclaw/.
```

See: [Agent workspace](https://docs.openclaw.ai/concepts/agent-workspace)

# [Github Recommended Private](https://docs.openclaw.ai/concepts/agent-workspace#git-backup-recommended-private)

Treat the workspace as private memory. Put it in a private git repo so it is backed up and recoverable.

## 1) Initialize the repo
If git is installed, brand-new workspaces are initialized automatically. If this workspace is not already a repo, run:
```bash
cd ~/.openclaw/workspace
git init
git add AGENTS.md SOUL.md TOOLS.md IDENTITY.md USER.md HEARTBEAT.md memory/
git commit -m "Add agent workspace"
```
​
## 2) Add a private remote (beginner-friendly options)
Option A: GitHub web UI

    Create a new private repository on GitHub.
    Do not initialize with a README (avoids merge conflicts).
    Copy the HTTPS remote URL.
    Add the remote and push:
```bash
git branch -M main
git remote add origin <https-url>
git push -u origin main
```
​
## 3) Ongoing updates
```bash
git status
git add .
git commit -m "Update memory"
git push
```
​
# Do not commit secrets
Even in a private repo, avoid storing secrets in the workspace:

    API keys, OAuth tokens, passwords, or private credentials.
    Anything under ~/.openclaw/.
    Raw dumps of chats or sensitive attachments.

If you must store sensitive references, use placeholders and keep the real secret elsewhere (password manager, environment variables, or ~/.openclaw/). Suggested .gitignore starter: