# GenPRD

AI-powered Product Requirements Document generator. Transform product ideas into production-ready PRDs in seconds.

🔗 **Live:** [genprd.se](https://genprd.se)

## 🎯 What It Does

**Input:** Product idea in plain text  
**Output:** Complete PRD with tech stack, data models, user flows, UI specs, and acceptance criteria

Built for founders, PMs, and developers who need professional PRDs fast.

## ✨ Features

### Free Tier
- 50 one-time credits
- Full PRD generation (1 credit/PRD)
- Iterative refinement (1 credit/iteration)
- Download as Markdown
- Email support

### PRO (299 SEK/mån)
- 200 credits/month (refills monthly)
- Priority generation queue
- Advanced templates
- Export to DOCX/PDF
- Priority support

## 🏗️ Architecture

**Single-File SaaS Pattern** - NordSym's proven architecture:
- **Frontend:** 195KB HTML (React + Tailwind + Supabase)
- **Backend:** n8n workflows
  - PRD Generation Agent (GPT-4o-mini)
  - Stripe Payment Handler
- **Database:** Supabase (PostgreSQL + Auth)
- **Payments:** Stripe live mode

### Tech Stack
```
Frontend:  React (UMD), Tailwind CSS, Supabase Auth
Backend:   n8n Cloud (nordsym.app.n8n.cloud)
AI:        GPT-4o-mini (temperature: 0.3)
Database:  Supabase PostgreSQL
Payments:  Stripe (checkout.session.completed)
Hosting:   GitHub Pages
```

## 📊 PRD Output Format

Every generated PRD includes:
1. **Executive Summary** - Product, goals, value prop
2. **Tech Stack** - Frameworks, libraries, infrastructure
3. **User Roles** - Permissions and access levels
4. **Data Model** - Tables, columns, relations, constraints
5. **Core Features** - Step-by-step user flows with UI copy
6. **UI/UX Specs** - Color palette (hex), typography, layout
7. **Out of Scope** - What's NOT in v1
8. **Success Criteria** - Testable acceptance criteria

### Why It Works
PRDs are **implementation-ready**:
- Hex color codes (#RRGGBB)
- Pixel-perfect sizing (px/rem)
- Exact button copy
- SQL-ready data types
- Complete error messages
- Specific validation rules

## 🚀 User Flow

1. **Sign Up** - Email/password or social auth (Supabase)
2. **Describe Product** - Free text input (no templates needed)
3. **Generate PRD** - AI creates complete PRD (5-10 seconds)
4. **Iterate** - Chat interface below PRD for refinements
5. **Download** - Export as Markdown (PRO: DOCX/PDF)

## 💳 Pricing Model

**Free:**  
- 50 credits (one-time)
- Full feature access
- Email support

**PRO Monthly:** 299 SEK/mån  
- 200 credits/month
- Refills on billing date
- Priority features

**PRO Yearly:** 2988 SEK/år (299 SEK/mån × 12)  
- Same as monthly
- Annual commitment

## 🎨 Design System

**Visual Identity:**
- Primary: Nordic minimalism
- Accent: Fox logo (genPRDfox.svg)
- Typography: System fonts (performance)
- Layout: Clean, spacious, mobile-first

**Screenshots:**
- Dashboard example: `DashboardGenPRDexample.svg`
- Login flow: `loginGenPRDExample.svg`
- Empty state: `NoPRDeample.svg`

## 🛠️ Development

### Local Testing
```bash
# Clone repo
git clone https://github.com/nordsym/genPRD.git
cd genPRD

# Open index.html in browser
# No build step required (single-file architecture)
```

### Deployment
Push to `main` → Auto-deploys via GitHub Pages → Live at genprd.se

### Backend Workflows
Located in n8n Cloud:
1. **PRD Generation:** `/webhook/genprd-generate`
2. **Stripe Handler:** `/webhook/genprd-stripe-payment`

## 📈 Business Model

**Lead Gen Engine** for NordSym custom development:
1. Users generate PRDs for their ideas
2. Realize complexity of implementation
3. Contact NordSym for 60-120k SEK custom builds

**Current Status:**
- Live since: Jan 2025
- MRR Target: 299 SEK (PRO conversions)
- Primary Goal: Lead generation > Direct revenue

## 🔗 Links

- **Live Site:** https://genprd.se
- **NordSym:** https://nordsym.com
- **Support:** info@nordsym.se
- **Stripe:** Live mode enabled

## 🧠 AI Configuration

**System Prompt (GPT-4o-mini):**
```
Expert PRD writer for AI implementation.
Output: Complete markdown PRD.
Include: Tech stack, data model, user flows, UI specs, success criteria.
Be EXTREMELY specific: hex colors, pixel sizes, exact copy, data types, error messages.
NO preamble or conclusion - markdown only.
```

**Temperature:** 0.3 (consistency > creativity)  
**Max Tokens:** 4000 (full PRD in one shot)  
**Response Time:** ~5-10 seconds

---

**Built by NordSym AB** | Stockholm | 559535-5768  
**Architecture:** Single-File SaaS Pattern | **Stack:** React + Supabase + n8n + GPT-4o
