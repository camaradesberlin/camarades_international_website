 # Contribute Workshops

  Help keep the Education page fresh by adding your workshops here. Every `.qmd` in `workshops/` is auto-listed on `education.qmd`, so new files appear on
  the site without extra wiring.

  ## How to add a workshop

  1. Copy the starter below into `workshops/your-workshop-name.qmd`.
  2. Update the front matter:
     - `title`: clear workshop name
     - `date`: ISO format `YYYY-MM-DD` (used for sorting)
     - `delivery`: e.g., `Synchronous`, `Asynchronous`, `Hybrid`
     - `country`: city/country or `Online`
     - Optional: `categories` or `description` if helpful
  3. Write a short summary and include a registration/info button link.
  4. Place any PDFs in `files/` and images in `images/`; link with site-relative paths (e.g., `/files/your-handout.pdf`).
  5. Preview with `quarto render education.qmd` (or `quarto render` for the whole site) to confirm it lists correctly.

  ### Starter template

  ```yaml
  ---
  title: "Workshop Title"
  delivery: "Synchronous"
  country: "Online"
  date: "2025-05-01"
  # categories: ["Meta-analysis", "Training"]   # optional tags
  # description: "One-line summary for listings" # optional
  ---
  ```

  Add a short intro paragraph, key bullets (language, location, credits, etc.), and a call-to-action button:

  ```markdown
  ::: button
  [{{< fa arrow-up-right-from-square >}} Info & Register](https://example.com){.btn .btn-secondary target="_blank"}
  :::
  ```

  Run 'quarto render' and commit your changes to the main branch and it will show up on the Education page automatically. 
