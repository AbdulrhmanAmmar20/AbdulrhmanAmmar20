# Setup & Deploy Guide

Everything you need to make the new README render and animate on your GitHub profile.

## 1. Repo

Your profile README lives in a special repo named **exactly** after your username:

```
AbdulrhmanAmmar20/AbdulrhmanAmmar20   ← repo name must match your username
```

If you don't have it yet: create a new public repo called `AbdulrhmanAmmar20` and tick "Add a README".

## 2. File structure

Commit these files at the root of that repo:

```
AbdulrhmanAmmar20/
├── README.md                       ← the new profile README
├── assets/
│   ├── header.svg                  ← animated headline
│   └── neural-core-3d.svg          ← rotating 3D core
├── game/
│   └── index.html                  ← "Detect the Object" mini-game
└── .github/
    └── workflows/
        └── snake.yml               ← contribution snake generator
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

## 4. Snake animation (one-time wiring)

`snake.yml` is already in `.github/workflows/`. After you push it:

1. Repo → **Actions** tab → enable workflows if prompted.
2. Open **Generate Snake Animation** → **Run workflow** (runs on `main` push too).
3. It generates the snake SVG and pushes it to a new branch called `output`.
4. The README already points at:
   `.../AbdulrhmanAmmar20/output/github-contribution-grid-snake-dark.svg`

If Actions can't push, go to **Settings → Actions → General → Workflow permissions** and select **Read and write permissions**.

## 5. Quick checklist

- [ ] Repo named `AbdulrhmanAmmar20`
- [ ] `README.md`, `assets/`, `game/`, `.github/workflows/` committed
- [ ] GitHub Pages enabled (game link works)
- [ ] Snake workflow run once (snake image appears)
- [ ] Open your profile — header animates, typing line cycles, core spins

## Notes / tweaks

- **Email:** README keeps your `Abdulrhman.ar@outlook.com` link. Swap if you prefer `ammarkfupm22@gmail.com`.
- **Typing lines:** edit the `lines=...` part of the `readme-typing-svg` URL in README.md to change the rotating taglines.
- **Themes:** stats/graph use `radical` / `react-dark` to match your cyan-coral palette. Change the `theme=` query param to restyle.
- **Don't have a LinkedIn handle that matches?** Update the LinkedIn badge URL if needed.
