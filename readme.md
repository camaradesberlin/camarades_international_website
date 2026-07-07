# CAMARADES Website

This is a Quarto website. Source pages are `.qmd` files, and the rendered website is written to `docs/` for GitHub Pages.

## Table of Contents

1. [How to make changes to the website](#pull-the-repo-and-make-a-new-branch-in-rstudio)
2. [Add a new educational offering or workshop](#add-a-new-educational-offering-or-workshop)
3. [Edit or add a coordinating centre profile](#edit-or-add-a-coordinating-centre-profile)

## How to make changes to the website

To make changes, first clone or pull the repo and make a new branch in RStudio.

1. Clone the repository from GitHub:

```text
https://github.com/camaradesberlin/camarades_international_website
```

In RStudio, use **File > New Project > Version Control > Git**, paste the repository URL, and choose where to save the project locally.

2. Open the project in RStudio using `camarades_international_website.Rproj`.
3. In the **Git** pane, click **Pull** to get the latest changes.
4. Create a new branch from the RStudio Git pane:
   - Click the branch dropdown.
   - Choose **New Branch**.
   - Use a short descriptive name, such as `add-workshop-berlin` or `update-centre-germany`.
5. Make your edits.
6. Preview locally with:

```bash
quarto preview
```

7. Render the site before committing:

```bash
quarto render
```

8. Commit both the source changes and the updated `docs/` files.

## Add a new educational offering or workshop

Every `.qmd` file in `workshops/` is automatically listed on `education.qmd`.

1. Create a new file in `workshops/`, for example `workshops/intro-to-sr-online.qmd`.
2. Add front matter like this:

```yaml
---
title: "Workshop Title"
delivery: "Synchronous"
country: "Online"
date: "2026-05-01"
description: "One-line summary for the education listing."
---
```

3. Add a short description and any registration link:

```markdown
[{{< fa arrow-up-right-from-square >}} Info & Register](https://example.com){.btn .btn-secondary target="_blank"}
```

4. Put PDFs in `files/` and images in `images/`, then link them with site-relative paths such as `/files/handout.pdf`.
5. Run `quarto render` and check the Education page.

## Edit or add a coordinating centre profile

Centre pages live in `centres/`. The `about.qmd` page automatically lists them.

To edit an existing centre, update the relevant file, for example:

```text
centres/germany.qmd
```

To add a new centre:

1. Create a new file in `centres/`, for example `centres/france.qmd`. Ensure it ends in `e.qmd`. 
2. Add front matter like this:

```yaml
---
title: "France"
subtitle: "Institution or coordinating organisation"
description: "CAMARADES France is based at ..."
image: /images/CAMARADES_logo.jpg
---
```

3. Add centre details using the existing profile structure:

```markdown
## Contact

Institution  
Address  
[email@example.org](mailto:email@example.org)

## Educational Offerings

- Short description or link

## Ongoing projects

- Project name(s)

## Disease areas of interest

- Which disease areas of interest you are working on

## People and ORCID profiles

- Person Name: [{{< fa brands orcid label="ORCID" >}} 0000-0000-0000-0000](https://orcid.org/0000-0000-0000-0000){target="_blank"}
```

Use a centre-specific image if available. Otherwise use the standard CAMARADES logo:

```yaml
image: /images/CAMARADES_logo.jpg
```

Run `quarto render` and check both the centre page and the About CAMARADES listing.
