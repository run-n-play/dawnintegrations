# Dawn Integrations — blog

A Jekyll blog served by GitHub Pages at **dawnintegrations.com**.

## Write a post
Drop a Markdown file in `_posts/` named `YYYY-MM-DD-title.md`:

```markdown
---
layout: post
title: "LinuxCNC on the 5-axis gantry: first motion"
date: 2026-09-28 09:00:00 -0400
tags: [linuxcnc, cnc]
excerpt: "One-line summary shown on the home page."
---

Post body in Markdown. Code blocks, images, the usual.
```

Commit and push — GitHub Pages rebuilds automatically.

## Edit the bio
`about.md`.

## Run it locally (optional)
Needs Ruby. Then:
```bash
bundle install
bundle exec jekyll serve
# http://localhost:4000
```

## Deploy (first time)
1. Create a new GitHub repo (e.g. `dawnintegrations`) and push these files to `main`.
2. Repo → **Settings → Pages** → Source: **Deploy from a branch**, branch `main`, folder `/ (root)`.
3. Under **Custom domain**, enter `dawnintegrations.com` and save. (The `CNAME` file already sets this.)
4. Set the Cloudflare DNS records (see below), wait for the green check, then enable **Enforce HTTPS**.

## Cloudflare DNS  (dawnintegrations.com → GitHub Pages)
Set proxy status to **DNS only** (grey cloud) so GitHub can issue its HTTPS cert.

| Type  | Name | Value                     |
|-------|------|---------------------------|
| A     | @    | 185.199.108.153           |
| A     | @    | 185.199.109.153           |
| A     | @    | 185.199.110.153           |
| A     | @    | 185.199.111.153           |
| AAAA  | @    | 2606:50c0:8000::153       |
| AAAA  | @    | 2606:50c0:8001::153       |
| AAAA  | @    | 2606:50c0:8002::153       |
| AAAA  | @    | 2606:50c0:8003::153       |
| CNAME | www  | run-n-play.github.io      |

Replace `run-n-play` in the CNAME target with your GitHub username if different.
