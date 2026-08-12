# AIToolAtlas — Static Demo

> Discover the right AI for any task.

This is a **single-file static demo** of AIToolAtlas — pure HTML, CSS, and
vanilla JavaScript. No build step, no npm install, no database, no server.
Everything (search, trending tools, categories, comparison table) runs in
the browser against mock data baked into the page.

This is the demo/pitch version. For the real product — a database-backed
app with a real search API, ranking algorithm, and a submission queue — see
the separate `ai-tool-atlas` (Next.js + Postgres) project.

## What works here

- Hero search with a simulated "AI reasoning" loading sequence
- Keyword-based mock matching against 8 sample tools
- Trending tools, category browser, ChatGPT vs Claude vs Gemini comparison
- "Submit a tool" form — saves to `localStorage` only (not persisted anywhere else)

## Deploy it

### Option A — GitHub Pages (included, automatic)

This repo already has a GitHub Actions workflow
(`.github/workflows/deploy.yml`) that deploys `index.html` to GitHub Pages
on every push to `main`.

1. Push this repo to GitHub.
2. Go to **Settings → Pages** in your repo.
3. Under **Build and deployment → Source**, select **GitHub Actions**.
4. Push to `main` (or re-run the workflow from the **Actions** tab).
5. Your site will be live at `https://<username>.github.io/<repo-name>/`.

### Option B — Netlify Drop (no GitHub needed)

Go to [app.netlify.com/drop](https://app.netlify.com/drop) and drag
`index.html` into the browser. You get a live URL in seconds.

### Option C — Vercel

Import the GitHub repo at [vercel.com](https://vercel.com). No framework
will be detected, so it's served as a static site automatically.

## Local preview

Just open `index.html` directly in a browser — no server required. Or, for
a local dev server:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Limitations

- All tool data is hardcoded in `<script>` — nothing is fetched from a
  real API or database.
- The submission form only writes to browser `localStorage`; it is not
  visible to anyone else and clears if the user clears site data.
- Search "AI reasoning" is a scripted animation over simple keyword
  matching, not a real model call.

To make any of this real (persistent database, real ranking, multi-user
submissions), you need the full Next.js + Postgres project instead of this
static build.
