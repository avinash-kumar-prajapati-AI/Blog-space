---
id: "proj-001"
title: "My Portfolio Website — Built with Astro and Cloudflare"
description: "How I built and deployed my personal blog and portfolio using Astro, GitHub as a CMS, and Cloudflare Pages — completely free."
tags: ["astro", "cloudflare", "portfolio", "static-site", "github", "open-source"]
category: "projects"
modified_date: "2025-06-15"
thumbnail: "media/images/articles/my-portfolio-website/thumbnail.png"
external_links:
  - label: "Visit Product"
    url: "https://github.com/avinash-kumar-prajapati/SimpleBlogApp"
draft: false
---

## What I Built

A personal blog and portfolio site that is fast, free to host, and easy to update by just pushing markdown files to GitHub.

## Why Astro

Astro outputs pure static HTML — no JavaScript sent to the browser unless needed. This means:

- Faster page loads
- Better SEO out of the box
- Lower hosting cost (zero)

## The Stack

| Layer | Tool |
|---|---|
| Framework | Astro |
| Content | Private GitHub repo (markdown) |
| Hosting | Cloudflare Pages |
| Database | None needed |
| Cost | Free |

## How Content Updates Work

```
I write article.md → push to blog_repo
→ GitHub Action fires
→ Cloudflare rebuilds site
→ Live in ~30 seconds
```

No CMS dashboard needed. Just a text editor and git.

## Key Learnings

- Static generation is underrated for blogs
- GitHub as a CMS works surprisingly well
- Cloudflare Pages free tier is genuinely generous

## What's Next

Adding an About page with my resume, improving search, and applying for Google AdSense once I hit 20 articles.

---

*Share this article if it helped you!*
