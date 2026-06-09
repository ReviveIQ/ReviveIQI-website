# ReviveIQI

**Where Revenue Intelligence Meets Real Execution.**

ReviveIQI is an AI-powered product suite covering the full revenue lifecycle — helping job seekers land faster and helping B2B sales teams diagnose where deals break, recover stalled pipeline, and close with clarity.

**Website:** [reviveiqi.com](https://reviveiqi.com)

---

## The suite

| Product | Status | What it does | URL |
|---|---|---|---|
| **ResumeIQ** | ✅ Live | AI-powered resume transformation + ATS optimization + Working With Me | [resumeiq.reviveiqi.com](https://resumeiq.reviveiqi.com) |
| **MyCareerIQ** | ✅ Live | AI job search pipeline — research, cover letters, outreach, tracking | [mycareeriq.reviveiqi.com](https://mycareeriq.reviveiqi.com) |
| **InboxIQ** | ✅ Live | Email inbox intelligence — surfaces hidden revenue opportunities | [inboxiq.reviveiqi.com](https://inboxiq.reviveiqi.com) |
| **Pipeline Diagnostics** | 🔜 In Development | B2B pipeline diagnostic and recovery tool | [diagnostic.reviveiqi.com](https://diagnostic.reviveiqi.com) |
| **DealForgeAI** | 🔜 In Development | B2B sales pipeline recovery and deal rescue | — |
| **ReviveIQI Core** | ✅ Live | B2B consulting — "Build With Me" revenue recovery engagements | [reviveiqi.com](https://reviveiqi.com) |

## Why it exists

The numbers are clear. According to the Ebsta × Pavilion 2024 B2B Sales Benchmark (4.2M opportunities, $54B in pipeline analyzed):

- **79%** of B2B pipeline never closes — not from competition, from process breakdown
- **17%** of reps generate 81% of revenue — the system is broken, not the people
- **38%** longer sales cycles vs 2021, win rates down 27% in the same period
- **21%** average B2B win rate — 4 in 5 deals are already lost before they start

ReviveIQI was built to fix this — starting at the individual level (resume, job search, inbox) and scaling to the team and organization level (pipeline diagnostics, deal recovery, B2B consulting).

## The founder

**Bryan Michael Greer** — Fort Lauderdale, Florida  
18 years in enterprise SaaS sales. SDR → multi-state regional leader. $7M+ ARR driven personally. Top 0.3% national performance ranking. After an unexpected reset, channeled that experience into building the tools he wished existed.

Contact: [bryan@reviveiqi.com](mailto:bryan@reviveiqi.com)  
Consulting: [calendly.com/bryan-greer1/reviveiqi-discovery-call](https://calendly.com/bryan-greer1/reviveiqi-discovery-call)

## Infrastructure

- **Hosting:** Railway (all products) + GitHub Pages (reviveiqi.com)
- **Database:** TiDB Cloud (pipeline-production cluster, gateway01.us-east-1)
- **Auth:** Custom JWT (ResumeIQ) · jose JWT (MyCareerIQ, InboxIQ)
- **AI:** OpenAI GPT-4o + GPT-4o-mini (separate keys per product)
- **Payments:** Stripe (live keys)
- **Email:** Resend (ResumeIQ, InboxIQ) · Gmail SMTP (MyCareerIQ)
- **GitHub org:** [github.com/ReviveIQ](https://github.com/ReviveIQ)

---

*ReviveIQI · Fort Lauderdale, FL · [reviveiqi.com](https://reviveiqi.com)*
