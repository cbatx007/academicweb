# Updating the Website

Most updates can be made directly in GitHub by opening a file, clicking the pencil icon, making the change, and committing it to `main`. GitHub Pages rebuilds the site automatically after each push.

## Add a Paper

Open `data/papers.yaml` and add a new entry:

```yaml
- title: "Paper Title"
  authors: ["Carlos Batallas"]
  year: 2026
  status: "working paper"
  venue: "Manuscript in preparation"
  link: "https://example.com"
  abstract: "One-sentence description."
  job_market_paper: false
  tags: ["International Humanitarian Law"]
```

Use `status: "published"` only after the piece has appeared in a venue. Other useful values are `"working paper"`, `"work in progress"`, `"under review"`, `"revise and resubmit"`, and `"accepted"`.

## Add a PDF

Upload the PDF to `static/files/`, then set the paper's `link` field to:

```yaml
link: "/files/paper-file-name.pdf"
```

## Update the Bio

Open `content/_index.md` and edit the paragraphs directly.

The short line under the name lives in `hugo.yaml` as `tagline`.

## Add Teaching

Open `data/teaching.yaml` and add:

```yaml
- course: "Course Name"
  role: "Instructor"
  institution: "IE University"
  term: "2026-present"
```

## Add a Presentation

Open `data/talks.yaml` and add:

```yaml
- title: "Talk Title"
  venue: "Conference or institution"
  date: "Month Year"
```

## Update the CV

Add the file as `static/files/cv.pdf`. Then open `hugo.yaml` and set:

```yaml
cv: "/files/cv.pdf"
```

This will add the CV link to the navigation and hero area.

## Change the Photo

Replace `static/images/photo.jpg` with the new image, keeping the same filename.

## Add a Blog Post

Create a folder such as `content/blog/my-post/index.md` and add:

```markdown
---
title: "Post Title"
date: 2026-06-24
description: "One-sentence summary."
tags: ["international humanitarian law"]
---

Write the post here.
```

Add a Blog link to `hugo.yaml` only when there are posts you want visitors to see.

## Mark a Paper as Published

In `data/papers.yaml`, change:

```yaml
status: "working paper"
```

to:

```yaml
status: "published"
venue: "Journal or outlet name"
```

## Add a Job Market Paper

Set this field on the relevant paper:

```yaml
job_market_paper: true
```

The homepage can then be adjusted to highlight it separately if needed.
