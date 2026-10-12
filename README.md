# I build infrastructure for the commons — robust, open-source, built to last.

📍 Savoie, France · Founder @ [intrane.fr](https://intrane.fr)

---

## Why

We live in a world that fluctuates. Rather than chasing maximum performance, I build for robustness — the capacity to stay viable despite what we can't predict.

The living world doesn't optimize. It relies on diversity, cooperation, redundancy, margins of safety, and adaptation. What seems inefficient short-term is what makes it last. I apply the same logic to infrastructure.

AI is a tool I use — not the goal. The goal is **ownership and autonomy**: self-hosted, portable data, inspectable code. When intelligence and compute run through GAFAM's APIs, you're building on rented land. A stack under your control is a stack that can't control you.

## Values

- **Commons over platforms.** Open-source, not walled gardens.
- **Cooperation over dependency.** Teach several people rather than be the one expert who holds it all.
- **Diversity over uniformity.** Standard formats, interoperable systems, no lock-in.
- **Margins over optimization.** Don't exhaust resources chasing speed. Keep room for the unexpected.
- **Durability over novelty.** A thing that lasts 10 years beats one that ships fast and breaks on update.
- **Territory over cloud.** Local, anchored, serving real people in real places.

---

## The map — open source, self-hostable

The same map as [intrane.fr](https://intrane.fr): everything in this section is public source under an open license (MIT unless noted) and runs on your own machine. Many parts also have a hosted instance you can use today — that is what the link on the name points to.

### Own your execution
*The machine runs what you told it to, on hardware you chose.*

- **[machin](https://github.com/javimosch/machin)** — [a machine-first compiled language](https://javimosch.github.io/machin/): as terse as Python for an agent to write, compiles through C to one tiny native binary with HTTP, SQLite and crypto built in. Most of what follows is written in it.
- **the roam stack** — one story in three MIT binaries: **[roam](https://github.com/javimosch/roam)** ([live](https://roam.intrane.fr): leave an autonomous agent working on a remote box — budgets, sandbox, gated shell, no Python on the target) → **[roam-panel](https://github.com/javimosch/roam-panel)** (approve its risky moves from your phone with one-tap signed links) → **[roam-hub](https://github.com/javimosch/roam-hub)** ([hosted control plane](https://hub.roam.intrane.fr/llms.txt): schedule, meter, bill and report autonomous runs — metered LLM proxy with hard budgets and a kill switch, per-run péage billing, and [GitOps without k8s](https://blog.intrane.fr/gitops-for-people-with-three-vpses))
- **[remotecmd-cli](https://github.com/javimosch/remotecmd-cli)** — [run a command on any machine you own](https://rcmd.intrane.fr): WebSocket relay, token auth, JSON out, fleet health checks. Self-host free, or €5/mo on the managed relay
- **[mago](https://github.com/javimosch/mago)** — [cheap autonomous agents that run a company's backlog](https://mago.intrane.fr): an agent team takes your GitHub issues and ships pull requests. Stdlib-only Go, bring your own LLM harness · Apache-2.0
- **[tau](https://github.com/javimosch/tau)** — agent-first AI CLI in Zig: a non-interactive reimplementation of pi with tool-calling, goal mode and sessions
- **[machin-terminal](https://github.com/javimosch/machin-terminal)** — a terminal emulator in pure machin (hosts vim/htop/tmux)

### Own your data
*Your records are a file you can copy, read and carry away.*

- **[grange](https://github.com/javimosch/grange)** — [a document database built for agents](https://grange.intrane.fr): single binary, crash-safe WAL, O(1) aggregates, cold storage, an export endpoint that gives you everything
- **[bkn](https://github.com/javimosch/bkn)** — [a backend core in one binary](https://bkn.intrane.fr/llms.txt): document store, encrypted KV, auth, files (local or S3), event log, cron and signed webhooks over embedded SQLite, driven by an agent-first CLI with no admin UI. Nine domains of an 85k-line Node backend (superbackend) ported onto it as ~1,700 lines of scripts
- **[greffe](https://github.com/javimosch/greffe)** — [an append-only, signed register for associations and cooperatives](https://javimosch.github.io/greffe/): proof of authority on the machines the group already has, governance on-chain, no money, no mining — a node idles at ~5 MB. In production as the [public register](https://enbauges.fr/registre/ui) of a village [matériauthèque](https://enbauges.fr/materiautheque) in the Bauges
- **[poche](https://github.com/javimosch/poche)** — [an agent-first headless CMS over grange](https://javimosch.github.io/poche/): one machin binary, no UI
- **[machin-esetres](https://github.com/javimosch/machin-esetres)** — [a self-hosted S3 alternative](https://javimosch.github.io/machin-esetres/) with a real AWS SigV4 facade: `aws-cli`/`mc`/`rclone` point straight at it. One static binary, no MinIO, no Docker
- **[machin-vault](https://github.com/javimosch/machin-vault)** — backups you can verify and restore without the tool that wrote them
- **[blurd](https://github.com/javimosch/blurd)** — [face and plate redaction as a self-hosted API](https://blurd.intrane.fr): the original image is never stored, only the redacted bytes · AGPL-3.0

### Own your rails
*The plumbing an autonomous program needs — payment, identity, an address, a place to publish — without renting it from a platform.*

- **[peage](https://github.com/javimosch/peage)** — [fiat pay-per-call for agents](https://peage.intrane.fr): prepaid wallets, any API charges them with one HTTP call, signed receipts, caller-side spend caps and a [public solvency proof](https://peage.intrane.fr/v1/solvency)
- **[relais](https://github.com/javimosch/relais)** — [an inbox an agent can block on](https://relais.intrane.fr): catches OAuth callbacks, webhooks and approvals for programs with no public URL, with a `/wait` long-poll
- **[portier](https://github.com/javimosch/portier)** — [SSO for your app in one redirect](https://portier.intrane.fr): login-with-anything without implementing OAuth, priced per auth rather than per seat
- **[machin-idp](https://github.com/javimosch/machin-idp)** — [OIDC identity for humans and agents](https://idp.intrane.fr): humans join by invitation, agents are minted over an API and sign in with no browser
- **[machin-hart](https://github.com/javimosch/machin-hart)** — [agent-first artifact host](https://hart.intrane.fr): any terminal agent publishes self-contained HTML/JSX and gets a live, versioned, sandboxed URL. Claude Artifacts, unbundled and owned
- **[vigie](https://github.com/javimosch/vigie)** — [cookieless web analytics](https://vigie.intrane.fr) with no dashboard to log into — the numbers come to you as artifacts

### Own your tools
*Small, sharp, single-purpose. Adoptable in an afternoon and removable in ten minutes.*

- **[Agent-First CLI Specs](https://cli-specs.intrane.fr)** — seven small open specs that make any CLI legible to an agent: [output contract](https://github.com/javimosch/cli-output-spec), [guide](https://github.com/javimosch/cli-guide-spec), [feedback](https://github.com/javimosch/cli-feedback-spec), [self-update](https://github.com/javimosch/cli-update-spec), telemetry, daemon and trial. Each is adoptable on its own — [blog post](https://blog.intrane.fr/agent-first-cli-specs)
- **[supercli](https://github.com/javimosch/supercli)** — [10,000+ CLI tools, one CLI to reach them](https://javimosch.github.io/supercli/), zero configuration
- **[a2a-skill](https://github.com/javimosch/a2a-skill)** — [peer-to-peer messaging for agentic CLI sessions](https://javimosch.github.io/a2a-skill/) (claude, opencode, pi, …) over a shared SQLite bus. No central chain of command
- **[machin-secure](https://github.com/javimosch/machin-secure)** — a deterministic security auditor with no model inside it: it emits JSONL findings, your agent does the judging
- **[machin-rag](https://github.com/javimosch/machin-rag)** — [local retrieval in one binary](https://javimosch.github.io/machin-rag/): no keys to bring, nothing leaves the machine
- **[mtlm-router](https://github.com/javimosch/mtlm-router)** — [a 7M-parameter typed decision layer](https://mtlm-router.intrane.fr) in pure machin: routes natural-language requests in ~15ms on CPU, and says "escalate" instead of guessing · Apache-2.0
- **[bilan](https://github.com/javimosch/bilan)** — [a deterministic ledger and French tax radar](https://bilan.intrane.fr) for people with several activities
- **[machin-web-ui](https://github.com/javimosch/machin-web-ui)** — a component library and a Tailwind engine with no Node in the build
- **[machin-herald](https://github.com/javimosch/machin-herald)** — [a scheduled report mailer](https://javimosch.github.io/machin-herald/): run a command, email its stdout. A pipe, not a framework
- **[machin-feedback](https://github.com/javimosch/machin-feedback)** — an agent-first feedback relay: one inbox for every app's `feedback` command
- **[codebase-size](https://github.com/javimosch/codebase-size)** — [measure and classify a codebase by LOC](https://hart.intrane.fr/a/machin-loc/multi-assistant), published as self-contained hart reports

### For real places
*The point of all of it: infrastructure serving people in a particular valley, association or workshop.*

- **[creneau](https://github.com/javimosch/creneau)** — [machine booking for fablabs and makerspaces](https://creneau.intrane.fr): the laser, the CNC, the printers — one board, never double-booked
- **[matériauthèque](https://enbauges.fr/materiautheque)** — a shared materials library for the Cœur des Bauges, running on a [register](https://enbauges.fr/registre/ui) the commune can audit (built on greffe)

---

## Hosted products — closed source, paid

These are products, not parts of the map: their source is private and they cost money. They are what pays for the open work above.

- **[AutoMaintainer](https://automaintainer.intrane.fr)** — an agent fleet runs a verified build → verify → fix loop on your repos and opens merge-ready PRs, on your own provider keys
- **[grepapi](https://grepapi.intrane.fr)** — an affordable, agent-first alternative to SerpApi: web search results as JSON from one call or one CLI command
- **[crmd](https://crmd.intrane.fr)** — the CRM your agent runs
- **[chatsnip](https://chatsnip.intrane.fr)** — a chatbot for your micro-SaaS landing page, set up in five minutes
- **[Supergato](https://supergato.eu)** — a white-label AI agent platform: retrieval, tool calling, workflows and embeddable widgets
- **[La Chatière](https://lachatiere.fr)** — a French agent gateway for Mistral and other models, a white-label assistant for French teams
- **[crevisto](https://crevisto.com)** — a hundred ready-made AI image tools, paid per use, on the web and from [a command line whose client is MIT](https://github.com/javimosch/crevisto)
- **[comptoir](https://comptoir.intrane.fr)** — twelve UK and French tax calculators (stamp duty, take-home pay, capital gains, frais de notaire…), each one JSON call away
- **[DevCrew](https://devcrew.intrane.fr)** — your AI dev team lives in your chat: five agents that scope, build, review and prove work inside Slack, Teams or Telegram; your code never leaves your infra *(waitlist)*

## Connect

[![X/Twitter](https://img.shields.io/badge/-javimosch-000000?style=flat-square&logo=x&logoColor=white)](https://x.com/javimosch)
[![Website](https://img.shields.io/badge/-intrane.fr-22c55e?style=flat-square&logo=google-chrome&logoColor=white)](https://intrane.fr)
[![Blog](https://img.shields.io/badge/-blog.intrane.fr-3b4550?style=flat-square&logo=rss&logoColor=white)](https://blog.intrane.fr)

---

> If you don't own the stack, you are part of someone else's system. If it can't last, it won't liberate anyone.
