# Urable Walkthrough Library

Interactive, click-through walkthroughs of Urable workflows. Each guide is a self-contained
static page: one screenshot per step, a pulsing highlight on the exact click target, and
plain-English captions.

## Structure

- `index.html` — library landing page
- `<walkthrough>/` — one folder per walkthrough (`index.html` + `images/`)
- `scripts/<walkthrough>.json` — the structured step script each guide is generated from
  (`step → target → title → body → note`). These scripts are the source of truth: they're
  the future content files for in-app tours (Shepherd.js/driver.js) and the retrieval corpus
  for the AI assistant (RAG).

## Roadmap

1. **Library (now)** — shareable links, zero dev involvement
2. **Help-center embed** — one iframe pointing at these URLs
3. **Live in-app tours** — same scripts, CSS selectors instead of screenshot coordinates
4. **AI assistant** — MCP/API retrieval over `scripts/`

UI change? Re-capture screens, regenerate, push — Vercel redeploys automatically.

Maintained by Josh (BDR) with Claude. Deployed on Vercel.
