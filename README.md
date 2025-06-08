# MakeMyResume – Minimal Test Project
**Generated**: 2025-06-08T20:14:53.671893+00:00

This is a self‑contained FastAPI application you can run directly in GitHub Codespaces (or locally)
to test the core résumé‑rewriter flow.

## Quick start (Codespaces)

1. Open this repo in a Codespace.
2. The dev‑container installs Python 3.10 and dependencies automatically.
3. Set your OpenAI key (optional) inside **Settings ▸ Codespaces ▸ Secrets**  
   ```
   OPENAI_API_KEY=sk‑...
   ```
   If you skip the key the app will still work with dummy rewrites.
4. Start the server:
   ```bash
   uvicorn main:app --reload --port 8000
   ```
5. Click the forwarded port **8000** ➜ upload a DOCX and a Job Description, press **Generate**.

## What it does

* Parses bullet‑style paragraphs from your DOCX résumé.
* Rewrites each bullet to align with the supplied Job Description  
  (uses OpenAI GPT‑4o if you provide a key; otherwise appends "‑tailored").
* Computes a naive “ATS” score (percentage of JD keywords found).
* Streams progress to the front‑end, lets you download the rewritten résumé.

## TODO

* Better ATS (embeddings)
* Layout freeze for non‑List bullets
* Deploy to Vercel/Fly
