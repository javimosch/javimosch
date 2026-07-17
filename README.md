# I build systems for autonomy in the age of AI.

📍 Savoie, France · Founder @ [Intrane.fr](https://intrane.fr)

---

## My stance

I treat AI as a **layer of control over execution, data, and decision-making.**
When intelligence and compute run through GAFAM's APIs, you're building on rented land.
Dependency is vulnerability.

The concern about AI making us dependent isn't wrong — it's the whole point.
The difference is I believe the answer is **ownership, not rejection.**
Self-hosted models. Portable data. Inspectable code.
A stack under your control is a stack that can't control you.

## What I build

- Self-hosted AI agent systems
- Developer CLIs and agent infrastructure
- **machin** — agent-native compiled language: no type annotations, one function per line, C-speed native binaries
- SaaS designed for ownership and portability

## Design principles

Own your data · Own your execution · Prefer self-hosted · Avoid irreversible lock-in

## What's shipping now

- **[machin-rag](https://github.com/javimosch/machin-rag)** — [agent-first local RAG](https://javimosch.github.io/machin-rag/): Qdrant + tiny hash embedder, one machin binary, no BYOK — retrieve half for offline agents next to colibri/bossless
- **[peage](https://github.com/javimosch/peage)** — [fiat pay-per-call for the agent economy](https://peage.intrane.fr): agents hold prepaid wallets, any API charges them with one HTTP call. No crypto, no subscriptions, no OAuth — signed receipts, caller-side spend caps, and a [public solvency proof](https://peage.intrane.fr/v1/solvency) recomputed on every request. The 402 web on rails you own; one ~110 KB machin binary
- **[relais](https://github.com/javimosch/relais)** — [an inbox your agent can block on](https://relais.intrane.fr): ephemeral/local agents have no public URL, so relais catches any HTTP for them (OAuth callbacks, webhooks, approvals) and offers a `/wait` long-poll they can block on until it arrives. Metered by peage
- **[portier](https://github.com/javimosch/portier)** — [SSO for your app in one redirect](https://sso.intrane.fr): add Login-with-Google/GitHub/any-OIDC without implementing OAuth. Pay-per-auth via peage (100 free, then 1 EUR/100), no per-seat tax
- **[machin-idp](https://github.com/javimosch/machin-idp)** — [an OIDC identity provider for the agent era](https://idp.intrane.fr): "Login with intrane" for humans **and** agents, headless login, EdDSA id_tokens in pure MFL (no RSA). Plugs into portier
- **supercli** — 10,000+ tools, one agent-friendly CLI
- **machin** — machine-first compiled language, native speed through C
- **[machin-terminal](https://github.com/javimosch/machin-terminal)** — a terminal emulator in pure machin (hosts vim/htop/tmux; tmux is the multiplexer)
- **[machin-hart](https://github.com/javimosch/machin-hart)** — [agent-first artifact host](https://hart.intrane.fr): any terminal agent publishes self-contained HTML/JSX and gets a live, versioned, sandboxed URL — with live-data dashboards, an operator view, and an MCP server for native agent tools. One self-hosted binary (CLI + daemon) — Claude Artifacts, unbundled and owned
- **[roam](https://github.com/javimosch/roam)** — leave an autonomous agent working on a remote box; it self-replicates over ssh, and you approve its risky moves from anywhere (one static machin binary, no Python on the target)
- **tau** — agent-first AI CLI in Zig
- **[remotecmd-cli](https://github.com/javimosch/remotecmd-cli)** — [execute commands on any machine](https://rcmd.intrane.fr): WebSocket relay + token auth, JSON output, fleet health checks. OSS self-hosted or €5/mo managed cloud
- **AutoMaintainer · mago** — autonomous engineering SaaS

## Connect

[![X/Twitter](https://img.shields.io/badge/-javimosch-000000?style=flat-square&logo=x&logoColor=white)](https://x.com/javimosch)
[![GitHub](https://img.shields.io/badge/-Follow-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/javimosch)
[![Website](https://img.shields.io/badge/-intrane.fr-22c55e?style=flat-square&logo=google-chrome&logoColor=white)](https://intrane.fr)

---

> If you don't own the stack, you are part of someone else's system.
