# ReviveIQI Website

**Live at:** [reviveiqi.com](https://reviveiqi.com)  
**Hosted:** GitHub Pages · Auto-deploys from `main` branch  
**Domain Registrar:** Namecheap · DNS configured and verified

---

## What This Is

The official marketing website for **ReviveIQI** — an AI-powered revenue intelligence consulting firm founded by Bryan Michael Greer (Fort Lauderdale, FL). The site serves as the central hub for the ReviveIQI brand, consulting services, and AI product suite.

---

## Pages

| Page | Route | Status |
|------|-------|--------|
| Home | `/` | ✅ Live |
| ResumeIQ | `#resumeiq` (SPA) | ✅ Live |
| Job Search Pipeline | `#pipeline` (SPA) | ✅ Live |
| DealForge AI | `#dealforge` (SPA) | ✅ Live |

> The site is a single-page application (`index.html`). Navigation between pages is handled by JavaScript — no server routing required.

---

## Tech Stack

- **Pure HTML + CSS + Vanilla JS** — no build step, no dependencies
- **Fonts:** Syne (headings) + DM Sans (body) via Google Fonts
- **Animations:** CSS keyframes + IntersectionObserver scroll reveals
- **Background:** HTML5 Canvas particle network with mouse repulsion
- **Logo:** Inline SVG — geometric faceted diamond mark, no external assets

---

## Brand

| Token | Value |
|-------|-------|
| Navy (deep) | `#080f1e` |
| Navy (mid) | `#0f172a` |
| Navy (card) | `#1e3a5f` |
| Blue (primary) | `#2563eb` |
| Blue (mid) | `#3b82f6` |
| Blue (light) | `#60a5fa` |
| Blue (pale) | `#93c5fd` |
| Heading font | Syne 800 |
| Body font | DM Sans 300–500 |

**Tagline:** "Where Revenue Intelligence Meets Real Execution"

---

## Project Structure

```
ReviveIQI-website/
├── index.html      # Full site — all pages, styles, and scripts
├── CNAME           # GitHub Pages custom domain → reviveiqi.com
└── README.md       # This file
```

---

## Deployment

### GitHub Pages (current)
- Source: `main` branch · `/ (root)`
- Custom domain: `reviveiqi.com`
- HTTPS: Enforced via GitHub Pages SSL

### DNS (Namecheap → GitHub Pages)
| Type | Host | Value |
|------|------|-------|
| A Record | @ | 185.199.108.153 |
| A Record | @ | 185.199.109.153 |
| A Record | @ | 185.199.110.153 |
| A Record | @ | 185.199.111.153 |
| CNAME | www | ReviveIQ.github.io |

### To update the site
1. Edit `index.html`
2. Commit to `main`
3. GitHub Pages redeploys automatically in ~30 seconds

---

## AI Suite — Products Featured

### ✅ ResumeIQ (Live)
- **URL:** [resumeiq-production-d97e.up.railway.app](https://resumeiq-production-d97e.up.railway.app)
- **Repo:** `github.com/ReviveIQ/resumeiq`
- **Stack:** TypeScript · Deployed on Railway
- **What it does:** Transforms any resume into an ATS-optimized Word document with AI keyword gap analysis
- **Pricing:** $9.99 one-time · $29/mo unlimited

### ⚡ Job Search Pipeline (In Development)
- **Repo:** `github.com/ReviveIQ/SalesAEWorkflowHub`
- **What it does:** Adzuna job discovery + Apollo contact sourcing + Kanban application tracking + outreach sequence builder

### ⚡ DealForge AI (In Development)
- **Repo:** `github.com/ReviveIQ/SalesAEWorkflowHub`
- **What it does:** Takes real deal inputs and generates ready-to-use outreach, follow-up sequences, and stakeholder re-engagement assets

### 🧠 Pipeline Diagnostics Engine (Coming Soon)
- **What it does:** Upload your pipeline → AI-generated deal-by-deal breakdown with root cause analysis and reconnection strategy

---

## Roadmap

- [ ] Migrate to React + Vite + Tailwind as suite grows
- [ ] Add Calendly embed for direct booking on contact section
- [ ] Connect Pipeline Diagnostics Engine when live
- [ ] Add case studies / social proof section
- [ ] SEO meta tags + Open Graph images
- [ ] Analytics (Plausible or similar privacy-first)

---

## Contact

**Bryan Michael Greer**  
Founder · ReviveIQI  
📍 Fort Lauderdale, FL  
✉️ bryan@reviveiqi.com  
🌐 reviveiqi.com  
🐙 github.com/ReviveIQ
