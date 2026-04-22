# Channel Configuration of Openclaw

    OpenClaw can talk to you on any chat app you already use. Each channel connects via the Gateway. Text is supported everywhere; media and reactions vary by channel.

## Supported Channels

![channels](/images/3.png)

Chose the channel you want to communicate clawbot with via: whatsapp,discored,telegram

## Messaging platforms
### WhatsApp

Is the channel will use:

Install (on demand)

    Onboarding (openclaw onboard) and openclaw channels add --channel whatsapp prompt to install the WhatsApp plugin the first time you select it.
    openclaw channels login --channel whatsapp also offers the install flow when the plugin is not present yet.
    Dev channel + git checkout: defaults to the local plugin path.
    Stable/Beta: defaults to the npm package @openclaw/whatsapp.

Manual install stays available:
```bash
openclaw plugins install @openclaw/whatsapp
```

## Quick setup
### 1. Configure WhatsApp access policy
optional
```json
{
  channels: {
    whatsapp: {
      dmPolicy: "pairing",
      allowFrom: ["+15551234567"],
      groupPolicy: "allowlist",
      groupAllowFrom: ["+15551234567"],
    },
  },
}
```

### 2. Link WhatsApp (QR)
```bash
openclaw channels login --channel whatsapp

# For a specific account:

openclaw channels login --channel whatsapp --account work
```
### 3. Start the gateway
```bash
openclaw gateway
```
### 4. Approve first pairing request (if using pairing mode)
```bash
openclaw pairing list whatsapp
openclaw pairing approve whatsapp <COD>
```