# Setup & Deploy Guide

Everything you need to make the new README render and animate on your GitHub profile.

## 1. Repo

Your profile README lives in a special repo named **exactly** after your username:

```
AbdulrhmanAmmar20/AbdulrhmanAmmar20   ← repo name must match your username
```

## 2. File structure

```
AbdulrhmanAmmar20/
├── README.md                       ← the profile README
├── assets/
│   ├── header.svg                  ← animated headline
│   ├── neural-core-3d.svg          ← rotating 3D core
│   ├── dev-3d.svg                  ← animated 3D developer character
│   └── game-preview.svg            ← auto-playing game demo (inline)
└── game/
    └── index.html                  ← "Detect the Object" mini-game (playable)
```

> The README references assets with relative paths (`./assets/header.svg`). The animated SVGs (CSS + SMIL) **do animate** on GitHub when loaded this way — no extra hosting needed.

## 3. GitHub Pages (makes the game playable)

The "▶ PLAY NOW" button points to `https://abdulrhmanammar20.github.io/AbdulrhmanAmmar20/game/`. To turn it on:

1. Push the repo with the `game/index.html` file.
2. Repo → **Settings → Pages**.
3. Under **Build and deployment → Source**, choose **Deploy from a branch**.
4. Branch: `main`, folder: `/ (root)` → **Save**.
5. Wait ~1 min. Your game is live at the URL above.

> Username is lowercased in Pages URLs — that's already handled in the button link.
> The README also shows an inline auto-playing preview (`game-preview.svg`) so visitors see the game in motion without leaving the page. Real interactivity needs the Pages link, since GitHub READMEs can't run JavaScript.

## 4. Quick checklist

- [ ] Repo named `AbdulrhmanAmmar20`
- [ ] `README.md`, `assets/`, `game/` committed and pushed
- [ ] GitHub Pages enabled (Play link works)
- [ ] Open your profile — header animates, typing line cycles, core spins, dev waves, game preview loops

## Notes / tweaks

- **Email:** README keeps your `Abdulrhman.ar@outlook.com` link. Swap if you prefer `ammarkfupm22@gmail.com`.
- **Typing lines:** edit the `lines=...` part of the `readme-typing-svg` URL in README.md to change the rotating taglines.
- **Themes:** stats/graph use `radical` / `react-dark` to match your cyan-coral palette. Change the `theme=` query param to restyle.
- **LinkedIn:** update the LinkedIn badge URL if the handle changes.
