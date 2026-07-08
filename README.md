<p align="center">
  <img src="https://bothive.cloud/bothive-ai-logo.svg" alt="Bothive" width="72" />
</p>

<h1 align="center">Bothive</h1>

<p align="center">
  <strong>Build agents. Ship them. Let them run.</strong><br/>
  HiveLang, a hosted runtime, integrations, and a marketplace — one place to go from idea to deployed agent.
</p>

<p align="center">
  <a href="https://bothive.cloud">bothive.cloud</a> ·
  <a href="https://bothive.cloud/docs">Docs</a> ·
  <a href="https://bothive.cloud/hivestore">Hivestore</a> ·
  <a href="https://bothive.cloud/changelog">Changelog</a>
</p>

---

## What is Bothive?

Bothive is a platform for **creating, running, and distributing AI agents**.

You define behavior in **HiveLang**, test locally with the **CLI**, deploy to a **hosted runtime**, and connect agents to Slack, GitHub, Notion, and the rest of your stack. **HiveMind** helps you scaffold bots from a conversation. **Hivestore** is where teams discover and install agents built by others.

No duct-taping models, cron jobs, OAuth flows, and deployment pipelines yourself.

---

## What's in the box

| | |
|---|---|
| **HiveLang** | Declarative language for bots — instructions, tools, memory, workflows. Readable in git, friendly to LLMs. |
| **Pulse Engine** | Sandboxed execution with guardrails, logging, and integration adapters. |
| **HiveMind** | Describe what you need; get a bot, code, and a path to deploy. |
| **Hivestore** | Marketplace for production-ready agents. |
| **Integrations** | Connect once per workspace — every agent can use them. |

---

## Quick start

```bash
npm install -g @bothive/cli

bothive init my-agent
bothive dev
bothive login && bothive push
```

Embed in your own app:

```bash
npm install @bothive/sdk
```

```typescript
import { BothiveClient } from "@bothive/sdk";

const client = new BothiveClient({ apiKey: process.env.BOTHIVE_API_KEY });
const session = client.createSession({ botId: "your-bot-id" });

await session.send("Draft a reply to this support ticket");
```

→ [API docs](https://bothive.cloud/docs/api)

---

## HiveLang in 30 seconds

```hivelang
bot SupportAgent {
  instructions {
    You are a concise, helpful support agent.
  }

  capabilities {
    slack.send
    notion.search
  }

  react on "help *" with maxSteps 5
}
```

→ [HiveLang guide](https://bothive.cloud/docs/hivelang)

---

## Repo structure

```
bothive/
├── bothive/          # Platform — dashboard, API, runtime, UI
├── packages/
│   ├── cli/          # @bothive/cli
│   ├── sdk/          # @bothive/sdk
│   └── hivelang/     # HiveLang parser & runtime
└── ...
```

---

## Links

- [Documentation](https://bothive.cloud/docs)
- [Integrations](https://bothive.cloud/integrations)
- [Pricing](https://bothive.cloud/pricing)
- [Contact](https://bothive.cloud/contact)
- [X / Twitter](https://x.com/bothive_ai)

---

<p align="center">
  <sub>Agents that do the work — not just answer the prompt.</sub>
</p>
