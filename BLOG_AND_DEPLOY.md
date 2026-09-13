# Blog and Deployment Notes

This website is currently a lightweight static GitHub Pages site. The homepage has a Writing section with a placeholder, but the Markdown blog renderer is not enabled yet.

## How to Add a Blog Post Later

Recommended future structure:

```text
blog/
  posts/
    2026-09-12-example-post/
      index.md
      hero.png
      figure-1.png
```

Each post should live in its own folder. Put the Markdown file and any related images in the same folder.

Suggested `index.md` format:

```markdown
---
title: "Example Post Title"
date: "2026-09-12"
description: "One short sentence for the blog index."
tags: ["systems", "training"]
---

# Example Post Title

Write the post here.

![Figure caption](figure-1.png)
```

When the blog is implemented, the homepage can show the newest few posts in the Writing section, and `/blog/` can show the full list. Until then, do not add real posts unless you are okay with them being stored but not displayed.

## How to Preview Locally

From this folder:

```bash
python3 -m http.server 8000
```

Then open:

```text
http://localhost:8000/
```

## How to Publish the Website

This repository is connected to:

```text
https://github.com/cdwang96/cdwang96.github.io.git
```

Because it is a `cdwang96.github.io` repository, GitHub Pages should publish the `master` branch automatically after you push.

Typical publish flow:

```bash
git status
git add index.html styles.css static/pdf/chendong-cv.pdf BLOG_AND_DEPLOY.md
git commit -m "Update homepage and CV"
git push origin master
```

Do not add `preview-v2/` unless you intentionally want to publish the old preview pages too.

After pushing, the public site should update at:

```text
https://cdwang96.github.io/
```

GitHub Pages can take a minute or two to refresh.

## Updating the CV

The homepage links to:

```text
static/pdf/chendong-cv.pdf
```

To update the CV, replace that file, commit it, and push.
