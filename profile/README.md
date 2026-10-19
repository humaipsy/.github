<h1 align="center">HumaiPsy</h1>

<p align="center">
  <strong>🔬 Open-source applications for running scientific human–AI-agent interaction experiments 🔬</strong>
</p>

<p align="center">
  <a href="https://github.com/humaipsy/humaipsy/blob/main/LICENSE"><img alt="License: AGPL v3" src="https://img.shields.io/badge/License-AGPL--3.0-blue.svg"></a>
  <a href="https://github.com/humaipsy/humaipsy/releases"><img alt="Latest release" src="https://img.shields.io/github/v/release/humaipsy/humaipsy?label=release&color=success"></a>
  <img alt="Platforms: Windows, macOS, Linux" src="https://img.shields.io/badge/platform-Windows%20%7C%20macOS%20%7C%20Linux-blue">
  <a href="https://humaipsy.github.io/humaipsy/"><img alt="Website" src="https://img.shields.io/badge/Website-humaipsy.github.io%2Fhumaipsy-blue"></a>
</p>

---

## What this organization is for

**HumaiPsy builds the instrumentation for studying people interacting with AI agents — software that treats the model as an experimental condition, not a black box.**

Experimental psychology, cognitive science and HCI can now ask questions that were impractical to operationalize a few years ago: how a person's reasoning shifts under a cooperative versus an argumentative interlocutor; whether confidence still tracks accuracy when that interlocutor is fluent and wrong; what someone's language reveals about trust in a system that answers instantly. Asking those questions well is a software problem, and the software is not a chat client with a transcript export bolted on. A language model is neither a questionnaire item nor a conventional stimulus: it varies between trials, it responds to how it is prompted, and it has to be held constant exactly where the design requires constancy. The difficult part is therefore the experimental part — counterbalanced conditions, sequenced and reproducible trials, prompts and model endpoints that are pinned rather than remembered, per-trial timing, and a record complete enough that the analysis can be re-derived months later by someone who was not in the room.

**Everything here is local-first, inspectable and free to run.** There is no telemetry, no account and no hosted service in the loop. An experiment talks to a model you point it at, writes its records to your disk, and can be run fully air-gapped. The code is AGPL-3.0, so a method published with it can be read, re-run and contested by anyone who wants to replicate or challenge the result — which is the only sense in which research tooling is genuinely scientific.

## Repositories

| Repository | What it is | Status |
| :--- | :--- | :--- |
| **[humaipsy](https://github.com/humaipsy/humaipsy)** | Cross-platform desktop application (Windows, Linux, macOS) for running multi-condition (e.g. Cooperative / Argumentative) chat experiments against a local or remote [Ollama](https://ollama.com) model, with a researcher-configurable number of trials per condition. Every trial is recorded to CSV, a mirrored JSONL audit-trail ledger and a local SQLite chat log, and a read-only browser dashboard can show a live view on a secondary screen. | Active · [latest release](https://github.com/humaipsy/humaipsy/releases/latest) |

## In the works

HumaiPsy is the first application in the set, not the set itself. The rest is being scoped in the order a study actually needs it:

- **Study design and counterbalancing** — conditions, trial order and assignment as a reproducible specification, rather than a spreadsheet convention passed between collaborators.
- **Stimulus presentation and timing** — controlled delivery of text, images and audio, at the timing precision a design can be held to.
- **Self-report instruments** — questionnaires and scales landing in the same record as the behavioural log, instead of a second file joined by hand.
- **Analysis and export** — from a finished session to a tidy dataset an analyst can open without reverse-engineering the tool that produced it.

None of the above has a promised date or a promised API. If one of them is what is blocking your study, [open an issue](https://github.com/humaipsy/humaipsy/issues) and describe the experimental requirement — a concrete requirement moves work faster than a feature request does.

## Principles

- **Reproducible by default.** Conditions, prompts and endpoints are pinned and recorded; running the same study twice produces comparable records.
- **Local-first, air-gap capable.** Participant data stays on the machine running the study, unless the researcher deliberately points it at a remote model.
- **Plain, durable formats.** CSV, JSONL and SQLite — readable in ten years without this software.
- **Open source under AGPL-3.0.** Fork it, re-run a published method, or audit what it actually does.
- **Built for real participants.** Vault-gated access and restrictive file permissions, alongside a [SECURITY.md](https://github.com/humaipsy/humaipsy/blob/main/SECURITY.md) that states plainly what is and is not protected.

## Get involved

Contributions are welcome from people who run experiments, and from people who write software for people who run experiments.

- **Questions, methods, ideas** — [open an issue](https://github.com/humaipsy/humaipsy/issues).
- **Building on the engine** — start with [ARCHITECTURE.md](https://github.com/humaipsy/humaipsy/blob/main/ARCHITECTURE.md) and the [contributor notes](https://github.com/humaipsy/humaipsy/blob/main/AGENTS.md); the engine has no UI dependency and is meant to be reused.
- **Running a study** — [releases](https://github.com/humaipsy/humaipsy/releases) carry an archive per platform plus a `SHA256SUMS.txt` manifest.
- **Handling participant data** — read [SECURITY.md](https://github.com/humaipsy/humaipsy/blob/main/SECURITY.md) before collecting any.

---

<p align="center"><em>Human–AI interaction as a measurable phenomenon.</em></p>
