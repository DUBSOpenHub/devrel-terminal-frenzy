# Security Policy

## Supported Versions

| Version | Supported |
|---------|-----------|
| 1.0.x   | ✅ Yes |

---

## Reporting a Vulnerability

**Do not open a public GitHub issue for security vulnerabilities.**

Please report vulnerabilities via [GitHub Security Advisories](https://github.com/DUBSOpenHub/devrel-cli-frenzy/security/advisories/new) or email the repository owner directly.

Include:
- A description of the vulnerability and its potential impact
- Steps to reproduce or a proof-of-concept
- Your preferred contact method for follow-up

**Expected response times:**

| Stage | Target |
|-------|--------|
| Acknowledgement | ≤ 48 hours |
| Initial triage | ≤ 5 business days |
| Fix / mitigation | ≤ 30 days |

---

## Security Posture

This is a **client-side only** HTML game with no server component, no authentication, and no data collection.

### What it does
- Loads team avatar images from `avatars.githubusercontent.com` (GitHub's public CDN)
- Stores a single high score value in the browser's `localStorage`
- Synthesizes audio using the Web Audio API
- Runs entirely in your browser tab

### What it does NOT do
- ❌ No server, no backend, no API calls (other than avatar images)
- ❌ No cookies, no tracking, no analytics
- ❌ No user accounts or authentication
- ❌ No data sent anywhere — everything stays in your browser
- ❌ No external JavaScript dependencies
- ❌ No service workers or background processes

### Content Security

- All game logic is inline in a single HTML file
- No external scripts are loaded
- Avatar images are loaded with `crossOrigin="anonymous"` from GitHub's CDN
- No user input is stored or transmitted — the game is stateless except for `localStorage` high score

### localStorage Usage

The game stores exactly two keys in `localStorage`:
- `copilot-frenzy-v2` — high score and achievement data (JSON)

This data never leaves the browser. Clearing browser data removes it entirely.

---

## Known Limitations

### No Content Security Policy header
Since the game is a local HTML file (or hosted on GitHub Pages), CSP headers are not set. If hosting on a custom domain, consider adding appropriate CSP headers.

### Avatar image loading
Team member avatars are loaded from `https://avatars.githubusercontent.com`. If this CDN is unreachable, the game still functions but cards will show placeholder images. A fallback timeout ensures the game starts within 5 seconds regardless.
