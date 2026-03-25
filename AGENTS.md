# 🎮 DevRel Terminal Frenzy — Agent Architecture

## Overview

DevRel Terminal Frenzy is a single-file HTML5 arcade game built entirely by AI agents through a competitive tournament system called **Havoc Hackathon**. No human wrote any game code — all source was generated, judged, and refined by AI models orchestrated via GitHub Copilot CLI.

## Agent Topology

```
                    ┌─────────────────────┐
                    │   Human Orchestrator │
                    │   (Copilot CLI)      │
                    └──────────┬──────────┘
                               │
              ┌────────────────┼────────────────┐
              │                │                │
     ┌────────▼────────┐ ┌────▼─────┐ ┌────────▼────────┐
     │  Contestant Pool│ │  Judges  │ │  Refinement     │
     │  (8 models)     │ │  (3 models)│ │  (human-guided) │
     └────────┬────────┘ └────┬─────┘ └────────┬────────┘
              │               │                │
     Round 1: Build    Score & Rank      Polish & Ship
     Round 2: Upgrade
```

## Round 1 — Build Phase

Eight AI models each received the same prompt and independently built a complete retro NES-style game. Each model ran as an isolated `general-purpose` agent with full tool access (bash, file creation, web fetch).

**Models deployed:**
- Claude Opus 4.6, Claude Opus 4.5, Claude Sonnet 4.6
- GPT-5.4, GPT-5.2, GPT-5.1
- GPT-5.1 Codex Max
- Gemini 3 Pro Preview

## Round 2 — Upgrade Phase

The winning game concept ("Approve Frenzy") was given to 8 models to upgrade. Two additional agents received an extended prompt with Copilot CLI theming requirements.

## Judging System

Three independent judge models scored all entries on 5 weighted categories using sealed-envelope scoring (no judge could see another's scores):

- **Claude Sonnet 4.5** — Judge 1
- **GPT-5.3 Codex** — Judge 2
- **GPT-5.4 Mini** — Judge 3

Scores were stored in a session SQL database and weighted totals computed programmatically.

## Human Refinement Phase

After tournament selection, the winning entry went through ~40 iterations of human-guided refinement covering:
- Visual design (gradient orbs, frosted glass, Hoot/Dark Factory design language)
- Team roster verification (96 members cross-referenced with org data)
- Per-person typing phrases with avatar display
- Sound design (Web Audio synthesis)
- Difficulty balancing and anti-exploit measures
- Naming, tone, and copy review

## Key Design Decisions

| Decision | Rationale |
|----------|-----------|
| Single HTML file | Zero friction — double-click to play, host anywhere |
| Web Audio synthesis | No external audio files needed |
| GitHub avatar CDN | Always up-to-date team photos, CORS-enabled |
| localStorage only | No server, no accounts, no data collection |
| 8-key KEYSET (A,S,D,F,J,K,L,;) | Home row keys for touch-typing ergonomics |
| Wrong-key penalty (5% score) | Prevents button-mashing exploit |

## Agent Communication

All agents communicated through the filesystem (HTML files written to `~/hackathon/hk48/`). No inter-agent messaging was used. The human orchestrator read agent outputs and dispatched follow-up prompts.

## Model Performance Notes

- **GPT-5.2** won the CLI-themed upgrade round with near-perfect scores
- **Claude Opus 4.6** won Round 1 and placed 2nd in Round 2
- **Claude Sonnet 4.6** DNF'd in Round 2 (85+ minute timeout, never wrote file)
- **Codex Max** was fastest to finish but scored lowest on feature completeness
