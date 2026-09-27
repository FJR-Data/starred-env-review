# Starred repos vs. my environment

I run an automated "improvement watch" process that periodically pulls new GitHub
stars (among other discovery sources) and scores them against a specific
personal dev setup:

- Linux desktop, AMD GPU (Vulkan/ROCm), no cloud GPU
- Claude Code as the primary coding agent/CLI
- A self-hosted local LLM (served over an OpenAI-compatible API) used for
  cheap/background tasks
- A handful of home-grown automation processes (agent orchestration, memory,
  cron-style background jobs) that a candidate tool would need to fit into or
  compete with

This repo is a public-safe export of that scoring history, filtered down to
the items that actually got a real adopt/reject call — 11 repos total (2
adopted, 9 rejected). Items that were only seen or auto-scored, with no
decision ever made on them, are left out entirely.

## Scoring rubric

Each item gets a **tier** (1–3) and a **weighted score** (roughly 0–5) from an
automated pass that rates fit against the setup above on a few axes (dev
workflow value, integration effort, redundancy with what's already running).
Tier 1 / high score = looks like a strong fit worth adopting soon; tier 3 /
low score = weak fit or below the bar. Where no automated score exists, the
item is simply marked as **seen** — it showed up in the discovery feed but was
never run through the scorer or manually evaluated.

## Verdict values

- **adotado** — actually installed/used at some point (may since have been
  retired; see the reason column).
- **descartado** — evaluated and rejected, or installed and later removed.

A third bucket, **visto** (appeared in the starred list and/or got an
automated score, but no adopt/reject decision was ever made), exists
internally but is deliberately excluded from this export — it was the
largest bucket by far, and without a real decision behind it there was
nothing worth publishing.

## Files

- `REPORT.md` — the full table (repo, tier/score, verdict, reason,
  description).
- `data.json` / `data.csv` — the same rows, structured.

## What's deliberately left out

Descriptions and reasons here are written generically — no internal paths,
service/process names, host details, or any identifying detail about the
private setup beyond the generic profile described above.

## License

This content is licensed under the [Creative Commons Attribution 4.0
International (CC-BY-4.0)](LICENSE) license.
