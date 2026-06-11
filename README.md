# Surya Shankar Brahma — Portfolio

Single-file static site. No build step, no dependencies. Hosts free on GitHub Pages.

```
portfolio/
├── index.html          # the whole site (markup + styles + content)
└── profile.jpg      # your photo — swap to replace
```

---

## Host free on GitHub Pages

### Option A — Web UI (no command line)
1. Create a GitHub account, then create a **new public repo** named `portfolio` (or `<your-username>.github.io` for a root URL).
2. On the repo page → **Add file → Upload files** → drag in `index.html` **and** the `assets/` folder → **Commit**.
3. **Settings → Pages** → under *Build and deployment*, set **Source = Deploy from a branch**, **Branch = `main` / root** → **Save**.
4. Wait ~1 min. Your site is live at:
   - `https://<username>.github.io/portfolio/` (named repo), or
   - `https://<username>.github.io/` (if repo is `<username>.github.io`).

### Option B — Git CLI
```bash
cd portfolio
git init
git add .
git commit -m "portfolio"
git branch -M main
git remote add origin https://github.com/<username>/portfolio.git
git push -u origin main
# then enable Pages: Settings → Pages → Source: main / root
```

### Custom domain (optional, still free hosting)
Settings → Pages → **Custom domain** → enter your domain → add the DNS records GitHub shows (CNAME → `<username>.github.io`). Tick **Enforce HTTPS**.

---

## Customize

Everything is in `index.html`. Open it and edit two places only:

**Content** — find the `const DATA = {…}` block (section 14). Change text in quotes, add/remove array items (experience, projects, certs, etc.). No HTML needed.

**Theme** — find `:root{…}` at the top (section 1).
| Variable | Controls |
|---|---|
| `--accent` | accent colour (currently gold `#F5C451`) |
| `--bg`, `--surface` | background shades |
| `--font-display` / `--font-body` / `--font-mono` | typefaces (Google Fonts) |

**Photo** — replace `assets/profile.jpg` with any square-ish image of the same name.

**Other tweaks** — section spacing, cards, and layout live in the `<style>` block, each section labelled with a numbered comment.

---

Tip: open `index.html` locally in a browser to preview changes before pushing.
