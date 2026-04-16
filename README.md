
# AI Job Parser — Autonomous Freelance Job Agent

An end-to-end autonomous system that monitors freelance job boards (Upwork, FL.ru), parses full vacancy descriptions, analyzes relevance using DeepSeek AI, and delivers structured results to a web dashboard.

## 🧠 Architecture

┌─────────────┐     ┌─────────────────┐     ┌──────────────┐
│  Gmail API  │────▶│  Orchestrator   │────▶│ UniversalParser│
│  (triggers) │     │ (upwork_pipeline)│     │  (headless)   │
└─────────────┘     └─────────────────┘     └──────┬───────┘
                                                     │
                                                     ▼
┌─────────────┐     ┌─────────────────┐     ┌──────────────┐
│  Web Admin  │◀────│   DeepSeek AI   │◀────│  Raw Job Data │
│  Dashboard  │     │  (relevance +   │     │   (JSON)      │
│   (Next.js) │     │   price calc)   │     │               │
└─────────────┘     └─────────────────┘     └──────────────┘

## 🛠 Tech Stack

| Component | Technology |
|:---|:---|
| **Orchestration** | Python 3.11+, Gmail API |
| **Browser Automation** | UniversalParser (Playwright + Chromium) |
| **AI Layer** | DeepSeek API (relevance scoring, auto-pricing) |
| **Dashboard** | Next.js 14, TypeScript, Tailwind CSS, Supabase |
| **Infrastructure** | Docker, Nginx, VPS (Armenia) |

## 🚀 Key Features

- **Hands-free job discovery:** Monitors Gmail for Upwork alerts, extracts job URLs.
- **Full job parsing:** Headless browser automation fetches complete descriptions, budgets, skills.
- **AI-powered relevance filter:** DeepSeek analyzes text against my tech stack (Python, n8n, AI APIs).
- **Smart pricing:** Automatically converts hourly rates to fixed-price estimates with 10% speed discount.
- **Centralized dashboard:** Pre-qualified jobs appear in Next.js interface with one-click apply links.

## 📸 Dashboard Preview

*(Screenshots coming soon)*

## 👤 Author

**Garik** — AI Automation Architect & Full-stack Developer.
- GitHub: [@baltazzar-lead](https://github.com/baltazzar-lead)
- Email: baltazzar009@ya.ru

---
*Processing 50+ vacancies/week with 90%+ relevance accuracy.*
