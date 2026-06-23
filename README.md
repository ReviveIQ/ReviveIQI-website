# ReviveIQI

**Where Revenue Intelligence Meets Real Execution.**

ReviveIQI is an AI-powered product suite covering the full revenue lifecycle — helping job seekers land faster and helping B2B sales teams diagnose where deals break, recover stalled pipeline, and close with clarity.

**Website:** [reviveiqi.com](https://reviveiqi.com)

---

## The suite

| Product | Status | What it does | URL |
|---|---|---|---|
| **ResumeIQ** | ✅ Live | AI-powered resume transformation, ATS optimization, Working With Me personality section | [resumeiq.reviveiqi.com](https://resumeiq.reviveiqi.com) |
| **MyCareerIQ** | ✅ Live | AI job search pipeline — research, cover letters, contact enrichment, outreach, tracking | [mycareeriq.reviveiqi.com](https://mycareeriq.reviveiqi.com) |
| **Pipeline Diagnostics** | ✅ Live | B2B pipeline intake and diagnostic tool | [diagnostic.reviveiqi.com](https://diagnostic.reviveiqi.com) |
| **InboxIQ** | 🔜 In Development | Application tracking layer — monitors inbox for replies, auto-advances pipeline stages, weekly digest | — |
| **DealForgeAI** | 🔜 In Development | B2B sales pipeline recovery and deal rescue | — |
| **ReviveIQI Core** | ✅ Live | B2B consulting — "Build With Me" revenue recovery engagements | [reviveiqi.com](https://reviveiqi.com) |

---

## Product detail

### ResumeIQ — [resumeiq.reviveiqi.com](https://resumeiq.reviveiqi.com)
AI-powered resume transformation. Upload any PDF or DOCX — get back a polished, ATS-optimized Word document in 60 seconds.

- GPT-4o parsing + narrative extraction + enhancement pipeline
- Before/after ATS score (pre-score grades original harshly; post-score rewards the transformation)
- Captures non-standard sections: Publications, Projects, Hobbies, Volunteer
- Post-conversion email delivers DOCX to inbox automatically
- Abandoned checkout recovery — "You were so close" email 1 hour after initiating checkout
- Optional "Working With Me" section synthesized from DISC, MBTI, PI, TKI, or 360 assessments
- Cross-product SSO → MyCareerIQ 7-day free trial after download

**Pricing:** Free (1 transform) · $14.99 Starter (3 transforms) · $19.99 Resume + Working With Me · $79.99 Career Launch Bundle

---

### MyCareerIQ — [mycareeriq.reviveiqi.com](https://mycareeriq.reviveiqi.com)
AI-powered job search pipeline. Researches open roles, enriches contacts, generates tailored cover letters, and tracks your full application pipeline.

- Greenhouse and Ashby ATS integrations — surfaces real open roles at target companies
- 30-day freshness filter — no stale postings
- Role-aware company discovery — suggests companies that actually hire for the candidate's role (admin → healthcare/gov/enterprise; sales → cross-industry)
- 60+ standardized industry categories
- Apollo contact enrichment (two-step: search → enrich) + Hunter.io fallback
- LinkedIn search URL fallback when Apollo finds a name but no profile URL
- Cover letter engine: 3-stage GPT pipeline (Narrative Brief → Letter → Quality Scoring)
- 6 cover letter modes, auto-selected from job title; first name salutation only
- Pipeline table sorted by date added, with relative timestamps
- 7-day free trial for ResumeIQ users via cross-product SSO

**Pricing:** 7-day free trial · $29.99/month · $299/year

---

### Pipeline Diagnostics — [diagnostic.reviveiqi.com](https://diagnostic.reviveiqi.com)
B2B sales pipeline intake and diagnostic tool. Captures deal-level data and generates executive summaries with recovery strategies.


---

### InboxIQ *(in development)*
The accountability layer for MyCareerIQ. Connects to Gmail/Outlook and watches what happens after you apply — so you never lose track of where things stand.

- Connects to Gmail and Outlook via OAuth
- Scans inbox for replies to applications and outreach messages
- Detects rejection emails automatically → advances pipeline stage to Rejected
- Detects interview invites → advances stage to Interviewing
- Surfaces stale applications: "You applied to ZoomInfo 8 days ago — no reply. Follow up?"
- Weekly digest email: open applications, pending replies, suggested follow-ups
- Keeps job search top of mind between MyCareerIQ sessions
- Shares TiDB pipeline — reads MyCareerIQ companies table to know which roles to watch for

**The problem it solves:** Most job seekers apply and go silent. InboxIQ closes the loop — turning MyCareerIQ's pipeline into a living, auto-updating record of where every application stands.

---

### ReviveIQI Core — [reviveiqi.com](https://reviveiqi.com)
B2B consulting engagements. "Build With Me" offer — diagnose broken pipeline, rebuild conversion systems, recover stalled revenue.

---

## Cross-product architecture

```
ResumeIQ → SSO handoff → MyCareerIQ (7-day trial, resume auto-synced)
```

All products share:
- TiDB Cloud cluster (`pipeline-production`, gateway01.us-east-1, database: `pipeline`)
- ReviveIQ GitHub org (`github.com/ReviveIQ`)
- Railway hosting with auto-deploy on `main` push
- Stripe (live keys, per-product checkout)
- `CROSS_APP_SECRET` for signed cross-product tokens (HMAC-SHA256)

ResumeIQ tables: `riq_users`, `riq_resumes`, `riq_sessions`, `riq_email_captures`, `riq_email_sends`
MyCareerIQ tables: `users`, `companies`, `researchConfig`, `applications`, `workspaces`, `subscriptions`

---

## Why it exists

The numbers are clear. According to the Ebsta × Pavilion 2024 B2B Sales Benchmark (4.2M opportunities, $54B in pipeline analyzed):

- **79%** of B2B pipeline never closes — not from competition, from process breakdown
- **17%** of reps generate 81% of revenue — the system is broken, not the people
- **38%** longer sales cycles vs 2021, win rates down 27% in the same period
- **21%** average B2B win rate — 4 in 5 deals are already lost before they start

ReviveIQI was built to fix this — starting at the individual level (resume, job search) and scaling to the team and organization level (pipeline diagnostics, deal recovery, B2B consulting).

---

## The founder

**Bryan Michael Greer** — Fort Lauderdale, Florida  
18 years in enterprise SaaS sales. SDR → multi-state regional leader. $7M+ ARR driven personally. Top 0.3% national performance ranking. After an unexpected reset, channeled that experience into building the tools he wished existed.

Contact: [bryan@reviveiqi.com](mailto:bryan@reviveiqi.com)  
Consulting: [calendly.com/bryan-greer1/reviveiqi-discovery-call](https://calendly.com/bryan-greer1/reviveiqi-discovery-call)

---

## Infrastructure

| Layer | Tool |
|---|---|
| Hosting | Railway (all products) · GitHub Pages (reviveiqi.com) |
| Database | TiDB Cloud (pipeline-production, gateway01.us-east-1) |
| Auth | Custom JWT (ResumeIQ) · jose JWT (MyCareerIQ) |
| AI | OpenAI GPT-4o + GPT-4o-mini |
| Payments | Stripe (live keys, per-product) |
| Email | Resend (ResumeIQ) · Gmail SMTP IPv4 (MyCareerIQ) |
| Storage | Cloudflare R2 (resumes, DOCX, cover letters) |
| Contact enrichment | Apollo.io · Hunter.io |
| DNS | Namecheap (reviveiqi.com) |
| GitHub | [github.com/ReviveIQ](https://github.com/ReviveIQ) |

---

## Repos

| Repo | Product | Deploy |
|---|---|---|
| `ReviveIQ/resumeiq` | ResumeIQ | Railway auto-deploy on main push |
| `ReviveIQ/mycareeriq` | MyCareerIQ | Railway auto-deploy on main push |
| `ReviveIQ/blueprint-iq` | Pipeline Diagnostics | Railway |
| `ReviveIQ/ReviveIQI-website` | reviveiqi.com | GitHub Pages |

---

*ReviveIQI · Fort Lauderdale, FL · [reviveiqi.com](https://reviveiqi.com)*
