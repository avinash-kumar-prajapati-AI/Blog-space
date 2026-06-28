# blog_repo

Private content repository for SimpleBlogApp.

## Structure

```
articles/
  visibility.txt         → which categories are visible + 5 sidebar picks
  drafts.txt             → slugs of draft articles (format: category/slug)
  [category]/
    aboutcategory.txt    → description shown on category page
    [article-slug].md    → article content with frontmatter

media/
  images/
    articles/[slug]/     → thumbnail.png + content images
    assets/              → hero, 404, error graphics
    icons/               → site favicon
  docs/
    active-role.txt      → which job role to show on About page
    [job-role]/
      profile.json       → full resume data
      resume.pdf         → downloadable resume
```

## Article Frontmatter Reference

```yaml
---
id: "eng-001"
title: "Your Article Title"
description: "SEO meta description (150-160 chars ideal)"
tags: ["tag1", "tag2", "tag3"]
category: "engineering"
modified_date: "2025-06-01"
thumbnail: "media/images/articles/your-article-slug/thumbnail.png"
external_links:
  - label: "Visit Product"
    url: "https://your-link.com"
draft: false
---
```

## Adding a New Article

1. Create `articles/[category]/your-article-slug.md`
2. Add thumbnail to `media/images/articles/your-article-slug/thumbnail.png`
3. Push to `main` branch
4. GitHub Action auto-triggers Cloudflare rebuild
5. Live in ~30 seconds

## Making an Article a Draft

Add `category/article-slug` to `articles/drafts.txt`
