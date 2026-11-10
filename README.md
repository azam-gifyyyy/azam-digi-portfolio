# AZAM DIGI — Dark Luxury Portfolio

React + Vite + Tailwind v4 build of `azam_digi_dark_luxury_portfolio.tsx` (the file only contained one
component, so it could not run on its own — this project is the surrounding app).

## Run it

```powershell
npm.cmd install
npm.cmd run dev
```

The dev server prints a local URL (this project currently uses **http://localhost:5174** because
Morrow Dental Studio already has 5173).

> Note: `npm` (the `.ps1` wrapper) is blocked by the PowerShell execution policy on this machine.
> Use `npm.cmd ...` or run the commands from Command Prompt.

## Build / preview

```powershell
npm.cmd run build
npm.cmd run preview
```

`build` outputs a static site in `dist/` — drag that folder into Netlify, or import the repo on
Vercel (framework preset: Vite).

## Where to edit content

Everything lives in `AZAM_CONFIG` at the top of `src/App.tsx`:

| Key | What it is |
| --- | --- |
| `websiteDemos` | The three website cards: title, tags, `previewUrl` (opens in the modal iframe), `image` |
| `aiUgcDemos` | The three Reels: `youtubeId`, `thumbnail`, `videoUrl`, client/stats |
| `contacts` | WhatsApp / Instagram / email — label, value and link |

The same file also holds the hero copy and section headings.

## Files

```
index.html            page shell, fonts, meta tags
src/main.tsx          React entry point
src/index.css         Tailwind import + base styles
src/App.tsx           the whole portfolio (canvas 3D engine, cards, modals)
```

## Deploy to Vercel

1. Push this folder to a GitHub repo.
2. Vercel → Add New Project → import the repo.
3. Framework: **Vite** (build `npm run build`, output `dist`). Deploy.
