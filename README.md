# TestSprite Hackathon — Season 4 landing page

![Season 4 share card: Two Weeks. One Loop.](og-image.jpg)

Static, single-file landing page for Hackathon Season 4. No framework, no build step required: `index.html` plus a handful of image assets.

## Files

| Path | Purpose |
| --- | --- |
| `index.html` | The whole page: markup, CSS, and the small scripts (countdown, typing terminal, copy buttons, LOOP.md animation) |
| `painting.jpg` | Impressionist background used on the hero, CLI, timeline, and closing panels |
| `testsprite-logo.png` | Nav logo (rendered black via CSS filter) |
| `wordmark-outline.png` | Faint outlined wordmark under the footer |
| `og-image.jpg` | 1200×630 share card shown when the live URL is posted on Slack, Discord, X, etc. (referenced from `<meta property="og:image">`) |
| `favicon-32.png`, `favicon-512.png`, `apple-touch-icon.png` | Browser tab and home-screen icons |
| `events/` | Past-event posters (3) |
| `icons/` | Agent logos used in the LOOP.md card |
| `LICENSE` | © TestSprite, all rights reserved |

## Run locally

```bash
npm install
npm run dev        # http://localhost:5173
```

Or with no install at all: `npx vite`.

## Ship it

The page is static. Any of these work:

- **Copy into the site repo** — drop `index.html` and the asset files into the target route (e.g. `/hackathon`). Asset paths are relative, so keep the files together.
- **`npm run build`** — writes a `dist/` folder that can be handed to Vercel, Netlify, or S3.
- **Vercel** — import this repo; framework preset "Vite", default settings.

## Things to update before launch

- **Countdown target** — one line near the bottom of `index.html`:
  `var target = new Date("2026-09-14T09:00:00-07:00").getTime();`
- **Hero status chip** text ("Season 4 · Opens Sept 14 · $4,000 in prizes") once entries open.
- **`og:url`** in the `<head>` is set to `https://www.testsprite.com/hackathon`; change it if the page lives at a different path.
- **Brand marks** — the Discord and X buttons use generic icons; official SVGs can be pasted into the `<svg class="ico">` slots.
- **Fonts** load from Fontshare (Satoshi) and Google Fonts (Geist Mono, Source Serif 4). Self-host if the site's CSP requires it.

The Discord invite (`discord.com/invite/GXWFjCe4an`) and X handle (`@test_sprite`) are final.

## Source of truth

Copy and rules follow the internal "Online Hackathon Season 4 — Strategy & Execution (Draft v3)" doc. Dates are provisional until confirmed in Discord.
