# QAudit.dev - Product Brief

> AI-Powered Accessibility & Security Compliance Platform

**Version:** 1.0
**Date:** December 23, 2024
**Status:** Planning → MVP Development

---

## Executive Summary

QAudit.dev is a B2B SaaS platform providing automated accessibility (WCAG 2.2/EAA 2025) and security (OWASP) audits. The platform targets SMB to Enterprise businesses, offering teaser reports for lead generation and API backend-as-a-service for developers.

**Company:** Registered in Moldova
**Domain:** qaudit.dev

---

## Market Opportunity

### EAA 2025 - Perfect Timing
- **June 28, 2025:** European Accessibility Act enforcement began
- **Standard:** EN 301 549 v3.2.1 (WCAG 2.1 AA minimum)
- **Scope:** All businesses serving EU customers
- **Penalties:** Up to €100,000+ per violation

### Competitive Landscape

| Competitor | Pricing | Weakness | Our Advantage |
|------------|---------|----------|---------------|
| Deque/axe | $5K-50K/yr | Enterprise only | SMB-friendly pricing |
| Siteimprove | €10K+/yr | Overkill for SMB | Right-sized solution |
| WAVE | Free | Outdated UX, no reports | Modern AI-powered |
| Pa11y | Free/OSS | No support, basic | Full platform + support |

**Our Position:** "Deque quality at Starter price with AI superpowers"

---

## Target Audience

### Primary: B2B

#### Segment 1: SMB (Small-Medium Business)
- 10-200 employees
- 1-5 websites/apps
- Budget: $50-500/month
- Pain: EAA compliance fear, no internal expertise
- Decision: Marketing/IT Manager

#### Segment 2: Digital Agencies
- Managing 20-100 client websites
- Need white-label solution
- Budget: $500-2000/month
- Pain: Manual audits don't scale
- Decision: Technical Director

#### Segment 3: Enterprise
- 500+ employees
- Complex web properties
- Budget: $2000-10000/month
- Pain: Compliance risk, audit fatigue
- Decision: CISO, Compliance Officer

### Secondary: Developers (PLG Entry)
- Free tier users
- Chrome extension users
- Convert to paid via company

---

## Product Vision

### Core Value Proposition
```
"Automated accessibility and security compliance in minutes, not months.
Stay compliant with EAA 2025, WCAG 2.2, and OWASP - effortlessly."
```

### Key Differentiators

1. **Tiered Contrast Scanner (UNIQUE)**
   - CSS analysis → Dual Screenshot → Vision AI
   - Catches gradients, image backgrounds, overlays
   - No competitor has this

2. **86 ACT Rules (W3C Validated)**
   - Industry-leading rule coverage
   - Can claim "W3C ACT Compliant"

3. **Vision AI Analysis**
   - AI sees what users see
   - Natural language explanations
   - Auto-fix code suggestions

4. **Combined A11Y + Security**
   - One platform, multiple compliance needs
   - WCAG + OWASP in single scan

5. **Teaser Report Engine**
   - Automated lead generation
   - Value-first outreach
   - Viral potential

---

## Feature Set

### MVP (4-Week Target)

| Feature | Priority | Status |
|---------|----------|--------|
| Landing page | P0 | In Progress |
| User auth (Supabase) | P0 | Planned |
| URL scan input | P0 | Planned |
| Basic scan (a11y-engine) | P0 | Ready (existing) |
| Results dashboard | P0 | Planned |
| PDF report export | P0 | Ready (existing) |
| Stripe payments | P0 | Planned |

### V1.1 (Post-Launch)

| Feature | Priority |
|---------|----------|
| Scheduled monitoring | P1 |
| Email notifications | P1 |
| API access | P1 |
| Jira integration | P2 |
| Slack alerts | P2 |
| White-label reports | P2 |

### V2.0 (Future)

| Feature | Priority |
|---------|----------|
| Mobile app scanning | P2 |
| Chrome extension | P2 |
| VS Code extension | P2 |
| Accessibility Statement generator | P2 |
| Competitive analysis | P3 |
| Chat with report (AI) | P3 |

---

## Pricing Strategy

### Subscription Tiers

| Tier | Price | Scans | Features |
|------|-------|-------|----------|
| **FREE** | $0 | 5/month | Basic report, watermark |
| **STARTER** | $49/mo | 100/mo | Full reports, 1 domain, email support |
| **PRO** | $149/mo | 500/mo | API access, 5 domains, priority support |
| **BUSINESS** | $399/mo | 2000/mo | White-label, 20 domains, Jira/Slack |
| **ENTERPRISE** | Custom | Unlimited | On-prem, SLA, dedicated CSM |

### API Usage (Addon)
- Pay-per-scan: $0.05/scan (after quota)
- Bulk packages: 10K scans = $300

### Annual Discount
- 20% off for annual payment
- 2 months free

---

## Revenue Projections

### Year 1 Target
```
Month 1-3:  10 customers × $100 avg = $1,000 MRR
Month 4-6:  50 customers × $120 avg = $6,000 MRR
Month 7-12: 150 customers × $150 avg = $22,500 MRR

Year 1 ARR Target: ~$270,000
```

### Break-Even Analysis
```
Fixed Costs: ~$125/mo infrastructure
Variable: Stripe 2.9% + compute

Break-even: ~3 Starter customers
```

---

## Technical Architecture

### Stack Decision

| Layer | Technology | Reason |
|-------|------------|--------|
| Frontend | SvelteKit | Already have dashboard-v2, fast |
| Hosting | Vercel | Easy deploy, edge functions |
| API | Hono/Cloudflare Workers | Fast, cheap, EU edge |
| Auth | Supabase Auth | Simple, proven |
| Database | Supabase PostgreSQL | All-in-one |
| Storage | Cloudflare R2 | Screenshots, PDFs |
| Queue | Inngest | Scheduled scans |
| Payments | Stripe | Industry standard |
| Scan Engine | Existing a11y-engine.js | Ready! |

### Existing Assets (Ready to Use)

```
scanners/
├── a11y-engine.js         ✅ Core scanner
├── rules/*.mjs            ✅ 86 ACT rules
├── lib/
│   ├── tiered-contrast-scanner.mjs  ✅ Unique tech
│   └── report-generator.mjs         ✅ 5 formats
└── mcp-server/            ✅ API foundation

workspace/dashboard-v2/    ✅ SvelteKit base
```

---

## Go-to-Market Strategy

### Phase 1: Soft Launch (Week 1-4)
1. Landing page live
2. Waitlist collection
3. 10 beta customers (free/discounted)
4. Iterate based on feedback

### Phase 2: Public Launch (Month 2)
1. ProductHunt launch
2. Dev.to / Hashnode articles
3. Twitter/LinkedIn presence
4. SEO content (blog)

### Phase 3: Outbound (Month 3+)
1. Teaser report campaigns
2. Cold email EU businesses
3. Partner with agencies
4. Conference presence

### Lead Generation Engine

```
Teaser Report Flow:
1. Scan target company website (automated)
2. Generate mini-report (5 top issues)
3. Send cold email with report attached
4. CTA: "See all 47 issues → Free account"
5. Nurture → Convert to paid
```

---

## Team Consensus (from Party Mode Review)

### Unanimous Agreement
- EAA timing is perfect
- Teaser reports = great lead gen
- Tiered Contrast Scanner = key differentiator
- B2B focus first, PLG for developers
- Need accuracy audit before launch

### Key Recommendations

**Sarah Chen (Product):**
- B2B SMB first, enterprise later
- Increase Business tier pricing
- Position against Siteimprove

**Erik Lindqvist (Architect):**
- Fly.io for scan workers
- Cloudflare for edge/API
- Supabase for simplicity

**Dr. Leonora Webb (Standards):**
- Don't call it "certification"
- Use "Compliance Assessment"
- Add multi-language reports

**Wilco van Braam (Rules):**
- Sampling for performance
- 20 elements per page for contrast
- Add timeout handling

**Simon Wu (AI):**
- AI fix suggestions = killer feature
- Natural language reports
- MCP integration for devs

**Julia Evans (Platform):**
- ~$125/mo infrastructure cost
- 99.9% uptime target
- GDPR: EU data residency

**Alan Richardson (QA):**
- Benchmark vs competitors before launch
- False positive audit required
- Test SPAs, Shadow DOM, iframes

**Stephanie Morillo (Docs):**
- Day 1: Landing + API docs
- SEO blog content plan
- Accessibility statement (eat own dogfood)

---

## Immediate Next Steps

### This Week
- [ ] Finalize landing page design
- [ ] Set up qaudit.dev hosting
- [ ] Create Supabase project
- [ ] Set up Stripe account

### Next Week
- [ ] Landing page live
- [ ] Auth flow working
- [ ] Basic scan endpoint
- [ ] Waitlist collection

### Week 3-4
- [ ] Dashboard MVP
- [ ] PDF reports
- [ ] Payment integration
- [ ] Beta launch

---

## Success Metrics

### MVP Success Criteria
- [ ] Landing page converts >5% to waitlist
- [ ] 50+ waitlist signups in week 1
- [ ] 10 beta customers onboarded
- [ ] <5% false positive rate
- [ ] <60s average scan time

### Month 3 Goals
- 100+ paying customers
- $5,000+ MRR
- <1% churn rate
- NPS >50

---

## Appendix

### Competitor Deep Dive
See: `docs/competitor-analysis.md` (to be created)

### Technical Specifications
See: `CLAUDE.md` for existing scanner documentation

### Brand Guidelines
See: `docs/brand-guidelines.md` (to be created)

---

*Document created: December 23, 2024*
*Last updated: December 23, 2024*
