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



To make any of this real (persistent database, real ranking, multi-user
submissions), you need the full Next.js + Postgres project instead of this
static build.
