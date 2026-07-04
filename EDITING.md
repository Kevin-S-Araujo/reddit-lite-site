# Editing the Reddit Lite landing page

Live site: **https://kevin-s-araujo.github.io/reddit-lite-site/**
Repo: **https://github.com/Kevin-S-Araujo/reddit-lite-site**
Local clone: `C:\Users\20sdk\OneDrive\Área de Trabalho\Apps\reddit-lite-site\`

GitHub Pages serves the `main` branch automatically. Every push to `main` deploys within ~60 seconds — no build step, no CI.

---

## File structure

```
index.html      The entire site — all CSS and JS are inline in this one file.
EDITING.md      This file.
```

There are no external dependencies, no npm, no framework. Edit `index.html` and push.

---

## Making a change

```powershell
cd "C:\Users\20sdk\OneDrive\Área de Trabalho\Apps\reddit-lite-site"

# Edit index.html however you like, then:
git add index.html
git commit -m "describe what changed"
git push
```

The live site updates within a minute of the push.

---

## Things still left TODO in index.html

Search for `TODO` in the file to find these three placeholders:

1. **Firefox Add-ons URL** — the `href` on the "Add to Firefox" button (search `firefox.com/addon`).
2. **Chrome Web Store URL** — the `href` on the "Add to Chrome" button (search `chrome.google.com/webstore`).
3. **Lemon Squeezy checkout URL** — the `href` on the "Get Pro" button (search `lemonsqueezy.com`).

Replace each placeholder with the real URL once the store listings are live.

---

## Layout overview (index.html sections in order)

| Section | What it is |
|---------|-----------|
| `<nav>` | Top bar with logo and CTA button |
| `#hero` | Headline, sub-copy, two install buttons |
| `#features` | Six benefit cards (free features) |
| `#comparison` | Free vs Pro table |
| `#cta` | "Get Pro" call-to-action block |
| `<footer>` | Links row + copyright |

CSS variables at the top of the `<style>` block control the color palette:

```css
--accent: #ff4500;   /* Reddit orange */
--pro:    #a78bfa;   /* Pro purple */
--bg:     #0d0d0e;   /* Page background */
```

Animations (gradient text, ambient blobs, scroll-reveal cards) respect `prefers-reduced-motion` and are safe to leave as-is.

---

## Briefing a new AI session to edit the site

Paste this into a new Claude Code session:

> The Reddit Lite landing page lives at `C:\Users\20sdk\OneDrive\Área de Trabalho\Apps\reddit-lite-site\index.html`.
> It's a single self-contained HTML file — all CSS and JS are inline. The live site is at
> https://kevin-s-araujo.github.io/reddit-lite-site/ and deploys automatically when you push to `main`.
> See `EDITING.md` in that folder for the full layout and TODO list.

That's all the context needed to make edits and push them.
