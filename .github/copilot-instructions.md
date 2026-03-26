# Copilot Instructions — DevRel Terminal Frenzy

This repository contains a single-file HTML5 arcade game (`index.html`).

## Key facts
- The entire game is one self-contained HTML file (~2,000 lines)
- No build step, no dependencies, no server required
- All styling is inline CSS, all logic is inline JavaScript
- Sound effects are synthesized via Web Audio API (no audio files)
- Team avatars load from GitHub's CDN (`avatars.githubusercontent.com`)
- High scores persist via `localStorage`

## When making changes
- Keep everything in `index.html` — do not split into separate files
- Test changes by opening the file directly in a browser (`open index.html`)
- Check for JS syntax errors with: `node -e "const fs=require('fs');const h=fs.readFileSync('index.html','utf8');const m=h.match(/<script>([\s\S]*?)<\/script>/);try{new Function(m[1]);console.log('OK')}catch(e){console.log('ERROR:',e.message)}"`
- The game features 96 DevRel team members — roster changes require updating the `DEVREL` array AND the `TYPING_PHRASES_ALL` array
- All user-facing text should use "urgent request" (not "boss" or "manager")
- No `text-transform: uppercase` — use natural casing throughout

## Team roster
The `DEVREL` array contains GitHub usernames and avatar URLs for all team members. The `TYPING_PHRASES_ALL` array has a personalized phrase for each person. Both must stay in sync.

## Hosted at
- GitHub Pages: `https://dubsopenhub.github.io/devrel-cli-frenzy/`
