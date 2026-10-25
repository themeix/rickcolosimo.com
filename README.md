# RickColosimo.com – Jekyll & Tailwind CSS v4 Static Site

Rebuilt from the original WordPress website into a maintainable, high-performance static website powered by **Jekyll**, **Tailwind CSS v4**, and **Decap CMS**, deployed automatically to **GitHub Pages** via **GitHub Actions**.

---

## Tech Stack

- **Static Site Generator:** Jekyll 4.4+ (Ruby 3.3+)
- **Styling:** Tailwind CSS v4 (`@tailwindcss/cli`)
- **Content Management:** Decap CMS (`/admin/`)
- **CI/CD:** GitHub Actions (`.github/workflows/pages.yml`)
- **Hosting & Domain:** GitHub Pages with custom domain `rickcolosimo.com` (HTTPS enforced)
- **Search:** Client-side instant keyword search (`/search/`) with `search.json` index

---

## Project Structure

```text
rickcolosimo/
├── _config.yml               # Jekyll configuration and collection declarations
├── _layouts/                 # Site layouts
│   ├── default.html          # Main site wrapper with gradient background
│   ├── page.html             # Content page layout with 78/22 sidebar grid
│   ├── post.html             # Single article layout with taxonomy badges
│   └── archive.html          # Category and tag archive template
├── _includes/                # Modular components
│   ├── head.html             # SEO, fonts, stylesheets, favicons
│   ├── header.html           # Brand header with signature dual accent bands
│   ├── navigation.html       # Desktop dropdowns & mobile hamburger menu
│   ├── sidebar.html          # Search widget, Twitter CTA, and tag cloud
│   ├── post-card.html        # 4-card footer teaser cards
│   ├── pagination.html       # Numbered pagination (1..35)
│   └── footer.html           # Contact banner, directory links, copyright
├── _posts/                   # 140 migrated articles (2008 – 2022)
├── _pages/                   # Informational pages & interactive tools
├── _data/                    # Structured data for templates & Decap CMS
│   ├── navigation.yml        # Editable navigation structure
│   ├── settings.yml          # Site metadata, contacts, social URLs
│   ├── tags.yml              # Tag directory with article counts
│   └── categories.yml        # Category definitions
├── assets/
│   ├── css/
│   │   ├── input.css         # Tailwind v4 source & custom design tokens
│   │   └── main.css          # Compiled production stylesheet
│   ├── uploads/              # Preserved media assets & badges
│   └── tools/                # Interactive financial calculation apps
│       ├── SeriesA/          # Series A venture math calculator
│       ├── NoteConvert/      # Convertible note discount & cap calculator
│       └── NoteInterest/     # Promissory note simple interest calculator
├── admin/                    # Decap CMS browser manager
│   ├── index.html            # CMS loader
│   └── config.yml            # CMS collections schema
├── category/                 # 8 category archive endpoints
├── tag/                      # 114 tag archive endpoints
├── .github/workflows/
│   └── pages.yml             # GitHub Actions build and Pages deployment
├── CNAME                     # Domain pointer: rickcolosimo.com
├── robots.txt                # Robots rules and sitemap reference
├── package.json              # Node dependencies for Tailwind v4
└── Gemfile                   # Ruby gems for Jekyll
```

---

## Quick Start & Local Development

### 1. Prerequisites
- **Node.js**: v18 or higher (v20+ recommended)
- **Ruby**: v3.1 or higher (v3.3/3.4 recommended)
- **Bundler**: `gem install bundler`

### 2. Install Dependencies
```bash
# Install Node dependencies (Tailwind CSS v4 CLI)
npm install

# Install Ruby gems (Jekyll & plugins)
bundle install
```

### 3. Build & Serve Locally
```bash
# Compile Tailwind CSS v4
npm run build:css

# Run Jekyll development server with live reload
bundle exec jekyll serve

# Or run full build
npm run build
```
Navigate to `http://localhost:4000/` in your browser.

---

## Decap CMS Setup & Authentication

Decap CMS is installed at `/admin/`.

### Supported GitHub Authentication
Decap CMS uses the GitHub Git Gateway backend. To enable browser-based logins:
1. In your GitHub repository settings, register an OAuth App under **Developer Settings** -> **OAuth Apps**:
   - **Application name:** Rick Colosimo CMS
   - **Homepage URL:** `https://rickcolosimo.com/`
   - **Authorization callback URL:** `https://api.decapcms.org/callback`
2. Configure the OAuth Client ID and Secret in your authentication provider (or Netlify Identity / Cloudflare Worker OAuth proxy).
3. Update `repo:` in `admin/config.yml` to point to your repository (`<your-org-or-user>/rickcolosimo`).
4. Authors logging into `/admin/` will authenticate securely through GitHub and commit content directly to the `main` branch, triggering automated deployment via GitHub Actions.

---

## Domain & DNS Checklist for Launch

To switch DNS from WordPress hosting to GitHub Pages:
1. Ensure the `CNAME` file exists with `rickcolosimo.com`.
2. Configure DNS records at your domain registrar/DNS provider:
   - **Apex Domain (A records):**
     - `185.199.108.153`
     - `185.199.109.153`
     - `185.199.110.153`
     - `185.199.111.153`
   - **Apex Domain (AAAA records - IPv6):**
     - `2606:50c0:8000::153`
     - `2606:50c0:8001::153`
     - `2606:50c0:8002::153`
     - `2606:50c0:8003::153`
   - **WWW Subdomain (CNAME record):**
     - Host: `www` -> Points to: `<your-username>.github.io`
3. Under **GitHub Repository Settings -> Pages**:
   - Custom domain: `rickcolosimo.com`
   - Check **Enforce HTTPS** (GitHub provisions a free Let's Encrypt certificate automatically).
