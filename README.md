<div align="center">

# 📓 personal-notes

<p>Personal notes repository for <a href="https://github.com/Aniket886"><code>@Aniket886</code></a> — powered by an automated GitHub Actions workflow that writes factual journal entries and idea lines to this repo every day.</p>

![GitHub last commit](https://img.shields.io/github/last-commit/Aniket886/personal-notes?style=flat-square&color=6e40c9)
![GitHub commit activity](https://img.shields.io/github/commit-activity/m/Aniket886/personal-notes?style=flat-square&color=238636)
![Workflow](https://img.shields.io/badge/workflow-GitHub%20Actions-2088FF?style=flat-square&logo=github-actions&logoColor=white)
![AI](https://img.shields.io/badge/AI-Groq%20%7C%20llama--3.3--70b-orange?style=flat-square&logo=lightning&logoColor=white)
![Timezone](https://img.shields.io/badge/timezone-IST%20%28Asia%2FKolkata%29-blue?style=flat-square)

</div>

---

> The project started as a simple auto-commit repo, but was intentionally reshaped into something that looks and behaves more like a real personal notes workspace. Instead of appending obvious counter lines, the workflow now writes short reflections, project notes, and quote-style ideas based on approved profile facts. The goal is to keep the repository activity looking like a believable personal workspace instead of a mechanical streak bot.

---

## 📋 Overview

This repository does four things:

| # | Action |
|---|--------|
| 1 | Schedules a daily workflow run at `00:05 IST` |
| 2 | Chooses how many commits to create for that run |
| 3 | Generates note content for each commit |
| 4 | Commits those note updates back to `main` |

---

## ⚙️ Current Behavior

### 🔄 Automatic daily run
- Runs every day at `00:05 IST`
- Uses GitHub cron `35 18 * * *` because GitHub Actions schedules are stored in UTC
- Chooses a random number of commits between `3` and `20`
- Uses Groq AI for the note text
- The lower cap keeps the workflow within the model's request-rate limits

### 🖐️ Manual run
- Triggered from the `Actions` tab
- Accepts an optional `commit_count`
- Manual range is `3` to `800`
- If you provide a value, that exact number is used
- Manual runs do not call Groq
- Manual runs use the local factual template generator only, so larger counts do not hit the AI API

### 📄 Content output

Each commit writes one new line into one of these files:

| File | Purpose |
|------|---------|
| `public/notes/journal.md` | Short work-log reflections, project thoughts, and learning notes |
| `public/notes/ideas.md` | Short quote-like lines, prompts, and project principles |

---

## 🗂️ Repository Structure
