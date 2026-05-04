# 🎮 Terminal Frenzy

[![Play Now](https://img.shields.io/badge/Play%20Now-GitHub%20Pages-7c3aed?style=for-the-badge&logo=github)](https://dubsopenhub.github.io/devrel-terminal-frenzy/)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Built with Copilot CLI](https://img.shields.io/badge/Built%20with-Copilot%20CLI-06b6d4.svg)](https://docs.github.com/en/copilot/github-copilot-in-the-cli)

**A retro arcade game starring GitHub's mascot characters.** Clear requests from Mona, Copilot, and Ducky, survive urgent terminal prompts, and keep the pipeline green for 60 seconds.

---

## ▶ Play Now

### 🌐 Browser (instant)

**[Play on GitHub Pages →](https://dubsopenhub.github.io/devrel-terminal-frenzy/)**

### 🎬 Game Preview

![Game Preview](preview.gif)


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
| **1** | Press the **key shown** on each mascot request card to clear it |
| **2** | Type the **Copilot CLI command** when urgent requests appear |

That's it. 60 seconds. How many can you clear?

### Scoring

- ✅ **Clear a request** → points × your pipeline multiplier
- ⭐ **Power-up cards** → double points, freeze timers, auto-clear requests
- 🔥 **Urgent requests** → type the shown Copilot CLI command for big bonuses
- ❌ **Wrong key** → lose points and break your combo
- 👑 **Final request** → Mona appears in the last 10 seconds. Type the full Copilot CLI command.

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

## 🐙 The Characters

GitHub's mascot characters — **Mona**, **Copilot**, and **Ducky** — now drive every card, urgent request, and animated title line. Mascot artwork is embedded directly in the single HTML file.

---

## 🛠️ Technical Details

- **Single HTML file** — no build step, no dependencies, no server
- **~2,000 lines** of HTML, CSS, and JavaScript
- **Web Audio API** — all sound effects synthesized in real-time
- **Canvas** — Matrix rain background and particle effects
- **GitHub mascot artwork** — embedded directly in `index.html`
- **localStorage** — high score persistence across sessions
- **Works offline** — mascot artwork ships inside the HTML file

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

This is a fun project! Ideas welcome:
- New mascot request phrases
- Visual effects and polish
- New urgent request commands
- Accessibility improvements

---

## 📄 License

[MIT](LICENSE) — play it, fork it, remix it.

---

🐙 Created with 💜 by [@DUBSOpenHub](https://github.com/DUBSOpenHub) with the [GitHub Copilot CLI](https://docs.github.com/copilot/concepts/agents/about-copilot-cli).

Let's play! 🎮✨
