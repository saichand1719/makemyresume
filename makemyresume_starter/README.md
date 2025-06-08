# MakeMyResume – Starter Skeleton

**Generated:** 2025-06-08T20:07:21.566466 UTC

## What’s inside
```
.
├── .devcontainer/        # Codespaces config: Node 20, Python 3.10, ports 3000/8000
├── apps/
│   ├── api/              # FastAPI backend (health check only for now)
│   └── web/              # Front‑end placeholder – scaffold with Next.js
├── pnpm-workspace.yaml   # Monorepo glue
```

## Quick start (inside Codespaces)

```bash
# 🟢 1. back‑end deps
cd apps/api
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
uvicorn main:app --reload --port 8000
# Open forwarded port 8000 -> /health should return {"status":"ok"}

# 🟢 2. front‑end scaffold
cd ../../apps
npx create-next-app web --typescript --tailwind --eslint --src-dir --import-alias "@/"

# (Then in another terminal)
cd web
pnpm dev     # Codespaces auto‑forwards port 3000
```

## Next steps
1. Implement `/upload` route in `apps/api`.
2. Wire React upload component in `apps/web`.
