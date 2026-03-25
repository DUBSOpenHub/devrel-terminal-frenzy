# 🎮 DevRel Terminal Frenzy

[![Play Now](https://img.shields.io/badge/Play%20Now-GitHub%20Pages-7c3aed?style=for-the-badge&logo=github)](https://dubsopenhub.github.io/devrel-terminal-frenzy/)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Built with AI](https://img.shields.io/badge/Built%20with-AI%20Agents-06b6d4.svg)](https://github.com/features/copilot)

**A retro arcade game for the GitHub DevRel team.** Approve PRs, survive urgent requests, and clear the review queue — all in 60 seconds. Featuring the faces and names of the entire DevRel org.

> **Built by 8 AI agents across 2 tournament rounds, scored by 3 independent judge models.** Zero human-written game code. Orchestrated via [GitHub Copilot CLI](https://docs.github.com/en/copilot/github-copilot-in-the-cli).

---

## ▶ Play Now

### 🌐 Browser (instant)

**[Play on GitHub Pages →](https://dubsopenhub.github.io/devrel-terminal-frenzy/)**

### 💻 From your terminal

```bash
# Clone and open
git clone https://github.com/DUBSOpenHub/devrel-terminal-frenzy.git
open devrel-terminal-frenzy/index.html
```

Or just download and double-click `index.html` — it's a single file with zero dependencies.

---

## 🎮 How to Play

| Step | What to do |
|------|-----------|
| **1** | Press the **key shown** on each card to approve it |
| **2** | Type the **Copilot CLI command** when urgent requests appear |

That's it. 60 seconds. How many can you clear?

### Scoring

- ✅ **Approve a card** → points × your pipeline multiplier
- ⭐ **Power-up cards** → double points, freeze timers, auto-approve
- 🔥 **Urgent requests** → type `/approve`, `LGTM`, `/ship-it`, or `/yolo` for big bonuses
- ❌ **Wrong key** → lose points and break your combo
- 👑 **Final request** → Martin Woodward appears in the last 10 seconds. Type LGTM three times.

### Ranks

| Score | Rank |
|-------|------|
| 0–399 | `$ exit 1` |
| 400–999 | Junior Dev |
| 1000–2499 | Senior Dev |
| 2500–4999 | Staff Engineer |
| 5000–7999 | Principal Engineer |
| 8000–11999 | VP of Vibes |
| 12000+ | 🤖 Copilot Singularity |

---

## 👥 The Team

All 96 members of the GitHub DevRel organization are featured in the game — their GitHub avatars appear on review cards, in urgent requests, and in the animated title screen. Each person has a custom typing phrase that cycles on the home screen.

---

## 🏗️ How It Was Built

This game was built entirely by AI agents competing in a **Havoc Hackathon** — a multi-model tournament system that pits AI models against each other:

### Round 1: 8 Models, 8 Games
Eight AI models each independently built a complete retro game from scratch:

| Model | Game | Score |
|-------|------|-------|
| Claude Opus 4.6 | Copilot Approve Frenzy | **90.33** 🥇 |
| GPT-5.2 | DevRel Rush | 82.67 🥈 |
| GPT-5.1 Codex Max | Retro Copilot Chaos | 81.00 🥉 |
| Claude Sonnet 4.6 | Copilot Chaos | 80.67 |
| Claude Opus 4.5 | Copilot Catch | 80.00 |
| GPT-5.4 | Copilot Party | 77.00 |
| GPT-5.1 | Copilot Cartridge | 74.00 |
| Gemini 3 Pro | DevRel Panic | 65.67 |

### Round 2: Upgrade Tournament
The winning concept was given to 8 models to upgrade with CLI theming, all 96 team faces, manager requests, power-ups, and polish:

| Model | Score |
|-------|-------|
| GPT-5.2 (CLI Edition) | **95.33** 🏆 |
| Claude Opus 4.6 (CLI Edition) | 86.00 |
| GPT-5.2 | 64.67 |

### Judging
Three independent AI judge models scored each game on:
- **Fun Factor** (3× weight)
- **Copilot CLI Theme** (3× weight)
- **Upgrade Quality** (2× weight)
- **Visual Polish** (1× weight)
- **Code Quality** (1× weight)

Judges: Claude Sonnet 4.5, GPT-5.3 Codex, GPT-5.4 Mini

### Human Refinement
After the tournament winner was selected, the game went through extensive human-guided iteration on:
- Title screen design (Hoot/Dark Factory visual language)
- Team roster accuracy (96 members verified against internal org)
- Typing animation with per-person phrases
- Sound design (victory jingle, buzzer effects)
- Difficulty tuning and anti-mash penalties
- Naming and tone ("DevRel Terminal Frenzy")

---

## 🛠️ Technical Details

- **Single HTML file** — no build step, no dependencies, no server
- **~2,000 lines** of HTML, CSS, and JavaScript
- **Web Audio API** — all sound effects synthesized in real-time
- **Canvas** — Matrix rain background and particle effects
- **GitHub Avatars** — loaded directly from `avatars.githubusercontent.com`
- **localStorage** — high score persistence across sessions
- **Works offline** — once avatar images are cached

---

## 📁 Repository Structure

```
devrel-terminal-frenzy/
├── index.html          # The entire game (single file)
├── README.md           # This file
├── AGENTS.md           # AI agent architecture
├── SECURITY.md         # Security policy
├── LICENSE             # MIT License
└── .github/
    └── copilot-instructions.md
```

---

## 🤝 Contributing

This is a team fun project! Ideas welcome:
- New typing phrases for team members
- Visual effects and polish
- New urgent request commands
- Accessibility improvements

---

## 📄 License

[MIT](LICENSE) — play it, fork it, remix it.

---

<sub>🎮 DevRel Terminal Frenzy — built by AI, played by legends.</sub>
