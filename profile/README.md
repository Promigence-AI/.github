<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Promigence-AI/.github/main/profile/wordmark-dark.svg">
    <img alt="Promigence" src="https://raw.githubusercontent.com/Promigence-AI/.github/main/profile/wordmark-light.svg" height="44">
  </picture>
</p>

<h3 align="center">Production-grade sandboxes for AI agents</h3>
<p align="center">Ready in milliseconds, fast at scale, billed by the second.</p>

<p align="center">
  <a href="https://www.promigence.ai">Website</a> ·
  <a href="https://www.promigence.ai/docs">Docs</a> ·
  <a href="https://www.promigence.ai/docs/guides">Guides</a> ·
  <a href="https://www.promigence.ai/#pricing">Pricing</a> ·
  <a href="https://x.com/promigence">X</a> ·
  <a href="https://www.linkedin.com/company/promigence/">LinkedIn</a>
</p>

Promigence gives every AI agent its own isolated sandbox. Each one opens on your project, already installed and checked,
so the agent starts on the task instead of the setup. Run one sandbox by hand or a thousand at once, see the most a run
can cost before it starts, and pay by the second for what runs.

## What teams run on it

| Work | How it looks | Guide |
|---|---|---|
| Coding agents | Claude Code, Codex or OpenCode working on a copy of your repository | [Run them in a sandbox](https://www.promigence.ai/docs/guides/claude-code-and-codex) |
| CI | Your GitHub Actions jobs move with one line: `runs-on: promigence` | [A runner in two lines](https://www.promigence.ai/docs/guides/github-actions-runner) |
| Code your users' AI writes | One sandbox per user or session, network off unless you allow a host | [Run AI-written code safely](https://www.promigence.ai/docs/guides/run-ai-written-code-safely) |
| Evals and RL | A fresh copy of the environment for every task or episode | [Harbor](https://www.promigence.ai/docs/guides/harbor) · [Inspect](https://www.promigence.ai/docs/guides/inspect-evals) |
| Agents inside your app | Vercel AI SDK, Google ADK, Claude Agent SDK, an MCP execute tool | [All guides](https://www.promigence.ai/docs/guides) |

## Quickstart

```bash
npm i -g promigence
promigence signup          # in your browser: sign up, then authorize the CLI
promigence credits claim   # claim your free credit
promigence doctor
```

During the private beta, signing up needs an invite: ask at support@promigence.ai. The
[quickstart](https://www.promigence.ai/docs/quickstart) takes it from there: build a snapshot of your project, check
it, and start copies of it.

## Measured

| | Promigence | Conditions |
|---|---|---|
| Sandbox ready to run a command | 8 ms | p50, 2 vCPU / 4 GiB, n = 100 |
| 100 started at once, slowest 5% | 0.94 s | p95, every run completed, n = 400 |
| CI job, start to finish | 48.5 to 55.9 s | 4 vCPU / 16 GiB; the same job took 105.9 to 148.7 s on hosted CI runners |
| Agent step on a warm repository | 0.66 s | edit, then type-check, 4 vCPU, n = 30 |

Every figure, its date and its method: [promigence.ai/#numbers](https://www.promigence.ai/#numbers).

## Packages

| | Install |
|---|---|
| CLI and TypeScript SDK | `npm i -g promigence` · `npm i @promigence/sdk` |
| Python SDK | `pip install promigence` |
| Harbor | `pip install promigence-harbor` |
| Inspect | `pip install inspect-promigence` |
| Google ADK | `pip install promigence-google-adk` |
| Claude Managed Agents | `pip install promigence-claude-managed-agents` |
| Vercel AI SDK | `npm i promigence-ai-sdk-sandbox` |
| Claude Agent SDK | `npm i promigence-claude-agent-sdk` |

More framework adapters are on their way to npm and PyPI.

## Security

Each sandbox is fully isolated from every other, and nothing is shared with another customer. A sandbox can run with no
network at all or behind an allow-list of the hosts it needs. Secrets go only to the commands that name them, and they
are never written into a snapshot. More at [promigence.ai/security](https://www.promigence.ai/security).

## Talk to us

support@promigence.ai · Send us your repository and the command you run, and we will run it a thousand times and send
back a [validity report](https://www.promigence.ai/validity-report) with an exact price. Free, once.
