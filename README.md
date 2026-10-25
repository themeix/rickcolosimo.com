# RickColosimo.com – Jekyll & Tailwind CSS v4 Static Website

Rebuilt from the original WordPress website into a maintainable, high-performance static website powered by **Jekyll** and **Tailwind CSS v4**, deployed automatically to **GitHub Pages** via **GitHub Actions**.

---

## Content Management & Editing Guide

All website content is centrally organized in plain YAML data files and Markdown documents. You can edit any page, post, navigation item, or contact detail directly without touching template code.

### 1. Site Metadata, Contact Info & Footer Settings
**File:** `_data/settings.yml`
- Website title, tagline, description, and author.
- Contact section details (`email`, `phone`, `address`).
- Social links (`twitter_url`, `linkedin_url`, `facebook_url`).
- Footer credits and copyright information.

### 2. Header & Footer Navigation Menus
**File:** `_data/navigation.yml`
- **Main Header Menu:** Configure top-level navigation links and nested dropdown submenus (`children`).
- **Footer Links:** Update links across the three footer columns (`footer_director_services`, `footer_about_rick`, `footer_other`).

### 3. Creating & Editing Blog Articles
**Directory:** `_posts/`
- Naming format: `YYYY-MM-DD-slug.md` (e.g., `2026-10-25-my-new-article.md`)
- File structure:
  ```markdown
  ---
  layout: post
  title: "Your Article Title"
  date: 2026-10-25 10:00:00 -0400
  author: "Rick Colosimo"
  permalink: /your-article-slug/
  excerpt: "Short summary of the article..."
  categories:
    - five-minute-lawyer
  tags:
    - contracts
    - governance
  ---

  Write the article body here using standard Markdown formatting.
  ```

### 4. Creating & Editing Static Pages
**Directory:** `_pages/`
- Contains existing pages such as `about.md`, `my-approach.md`, `services.md`, `governance.md`, `finance.md`, `deals.md`, `tools.md`, etc.
- Front matter format:
  ```markdown
  ---
  layout: page
  title: "Page Title"
  permalink: /custom-url/
  ---

  Page content written in Markdown.
  ```

### 5. Media & File Assets
- Place images or downloadable files in `assets/uploads/`.
- Reference them in Markdown:
  ```markdown
  ![Alt description](/assets/uploads/your-image.png)
  ```

---

## Local Development & Build Commands

### 1. Install Dependencies
```bash
npm install
bundle install
```

### 2. Compile Tailwind CSS v4
```bash
npm run build:css
```

### 3. Run Development Server with Live Reload
```bash
bundle exec jekyll serve
```
Open `http://localhost:4000/` in your browser.

### 4. Full Production Build Test
```bash
npm run build
```

---

## Automated Deployment to GitHub Pages

This repository is configured with a GitHub Actions workflow (`.github/workflows/pages.yml`). Whenever you push changes to the `main` branch, the workflow automatically compiles Tailwind CSS v4, builds the Jekyll site, and deploys the static files to GitHub Pages.

```bash
git add .
git commit -m "Update site content"
git push origin main
```

---

## Custom Domain Configuration (`rickcolosimo.com`)

The repository includes a `CNAME` file pointing to `rickcolosimo.com`. To direct domain traffic to GitHub Pages, configure your DNS provider with the following records:

- **Apex Domain (`@` A Records):**
  - `185.199.108.153`
  - `185.199.109.153`
  - `185.199.110.153`
  - `185.199.111.153`
- **Subdomain (`www` CNAME Record):**
  - Name: `www`
  - Target: `<your-username>.github.io`
