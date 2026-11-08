# MBA Bros Private Cloud — Showcase & Support Portal

[![Deploy to GitHub Pages](https://github.com/mbabros/mbabros.github.io/actions/workflows/deploy.yml/badge.svg)](https://github.com/mbabros/mbabros.github.io/actions/workflows/deploy.yml)

The official documentation, showcase portal, and engineering blog for the **MBA Bros Private Cloud**—an enterprise-grade, zero-trust hybrid self-hosted infrastructure.

Live Site: **[https://mbabros.github.io/](https://mbabros.github.io/)**

---

## 🌟 Tech Stack

* **Framework:** [Astro](https://astro.build/) (v5)
* **Documentation System:** [Starlight](https://starlight.astro.build/)
* **Blog Extension:** [starlight-blog](https://github.com/HiDeoo/starlight-blog)
* **Search Engine:** Pagefind (Zero-config, client-side, offline-first full-text search)
* **Package Manager:** `pnpm`
* **Deployments:**
  * **GitHub Pages:** Automated build & deployment via GitHub Actions (`.github/workflows/deploy.yml`)
  * **GitLab Pages:** Compatible via `.gitlab-ci.yml`
  * **Coolify / Docker:** Production multi-stage `Dockerfile` and `docker-compose.yml`

---

## 📂 Repository Layout

```text
├── .github/workflows/deploy.yml # GitHub Actions deployment to GitHub Pages
├── .gitlab-ci.yml               # GitLab CI configuration for GitLab Pages
├── Dockerfile                   # Multi-stage production container build
├── docker-compose.yml           # Compose specification for Coolify / Docker
├── nginx.conf                   # Static HTTP server configuration
├── astro.config.mjs             # Starlight & blog plugin configuration
├── package.json                 # Project dependencies & scripts
├── pnpm-lock.yaml               # Deterministic dependency lockfile
├── tsconfig.json                # TypeScript compiler configuration
└── src/
    ├── assets/                  # Optimized vector assets and diagrams
    ├── content.config.ts        # Astro content collection definitions
    └── content/
        └── docs/
            ├── index.mdx        # Showcase portal landing page
            ├── showcase/        # Topology, port maps, and service inventory
            ├── guides/          # Blueprints (OCI, Caddy, Tailscale, Coolify)
            ├── support/         # Runbooks, troubleshooting, and FAQs
            └── blog/            # Engineering blog posts
```

---

## 🚀 Local Development

1. **Install dependencies:**
   ```bash
   pnpm install
   ```

2. **Start the development server:**
   ```bash
   pnpm dev
   ```
   Open `http://localhost:4321` in your browser.

3. **Build for production:**
   ```bash
   pnpm build
   ```

4. **Preview the production build locally:**
   ```bash
   pnpm preview
   ```

---

## ✍️ Authoring Content

### Adding Documentation Guides
Create a new Markdown (`.md`) or MDX (`.mdx`) file in `src/content/docs/guides/` or `src/content/docs/support/`.

Update the sidebar configuration in `astro.config.mjs` to include your new slug:
```javascript
{ label: 'New Guide Title', slug: 'guides/new-guide' }
```

### Writing Blog Posts
Create a new Markdown file in `src/content/docs/blog/` (e.g. `2026-11-09-my-post.md`):

```markdown
---
title: Post Title
date: 2026-11-09
authors: mbabros
tags: ["homelab", "networking"]
excerpt: Brief summary of the post.
---

Post content goes here...
```

---

## 📜 License
MIT License. Created by the MBA Bros Homelab Engineering Team.
