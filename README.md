# Reverend Marius' Shepherd's Chapel &#10014;

A lovingly retro, 90s-style website for **Reverend Marius' Shepherd's Chapel** —
a steadfast refuge dedicated to gathering in reverence, grounding in truth, and
equipping for service.

Built as a static site (pure HTML + CSS + a dash of JavaScript), ready to host
on GitHub Pages.

## Pages

| File | Description |
|------|-------------|
| `index.html` | Home — welcome, mission statement, and pastor teaser |
| `about.html` | The Reverend — Marius Schmitz's full story ("My Unexpected Calling") |
| `expect.html` | What to Expect on your first visit |
| `guestbook.html` | A working 90s-style guestbook (saves entries in your browser) |
| `style.css` | Shared retro stylesheet |
| `images/` | Chapel and Reverend photos |

## Vibe

Marquees, ridge/outset borders, Comic Sans headings, a visitor counter, a
guestbook, and a proud "Best viewed in Netscape Navigator 4.0" footer. Come
exactly as you are! &#128231;

## Viewing locally

Just open `index.html` in any web browser, or serve the folder:

```sh
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Publishing with GitHub Pages

1. Push this repository to GitHub.
2. Go to **Settings → Pages**.
3. Under **Source**, choose your branch and the `/ (root)` folder.
4. Save — your chapel will be live at `https://<username>.github.io/<repo>/`.
