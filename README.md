# Pre-hack workshop landing — Burning Token Workshop 1 demo

A static, responsive landing page built from a five-question intake. **Local preview only.**

## Run

```bash
npm install
npm run dev      # http://127.0.0.1:4321
npm run build    # production build → dist/
```

## Facts confirmed

- Built with Astro, statically rendered, no backend, no auth, no deploy.
- Brand wordmark (`stack.`) is a working placeholder — not a registered brand.
- Submission form, ranking mechanic, and the agent-readable feeds are visual previews only.
- No sponsor or organizer relationship is implied in this build.

## Facts that require written confirmation

- Sponsor tier pricing and structure (not published in this build).
- Sponsor credits or logos (none shown).
- Provider access for any deployment (none).
- Exact workshop format / capacity / platform access.

## Deploy to Railway (manual — runs on your account)

Nixpacks handles the Node build automatically. A `railway.toml` is included so
the start command is explicit: `astro preview --host 0.0.0.0 --port $PORT`.

```bash
cd /Users/mel/workspaces/frutero/projects/devrel/burning-token/code/pre-hack-workshop-landing

# 0. Railway CLI installed and authenticated
railway whoami

# 1. Init the project (creates the service in your active workspace)
railway init --name pre-hack-workshop-landing

# 2. First deploy (uploads current dir, triggers Nixpacks build)
railway up
```

Notes for the deploy:

- `railway.toml` pins the start command; Nixpacks auto-runs `npm install && npm run build`.
- Static-only output (`./dist`) is served by `astro preview`, which binds `$PORT` from Railway.
- No secrets, env vars, or external services are declared.
- The build does not declare any sponsor, organizer, or platform-access claims.

## Deploy to Render (alternative blueprint — not active)

A `render.yaml` blueprint is included as a reference if you ever switch providers
from Railway back to Render.

## Boundaries this build respects

- No API keys, deployment credentials, browser sessions, or secrets in source, screenshots, or prompts.
- No web research, Tavily, Render, Convex, authentication, or deploy steps.
- No testimonials, customer logos, or fabricated user data.
- No sponsor or organizer marketing claims.
