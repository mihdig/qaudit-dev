# QAudit.dev - Product Roadmap TODO

> Based on Competitive Analysis December 2025
> Priority: P0 (Critical) → P1 (High) → P2 (Medium) → P3 (Nice to have)

---

## P0 - CRITICAL (Q1 2025)
> Blocking enterprise sales

### PDF Scanning
- [ ] PDF accessibility scanner (PDF/UA-1 standard)
- [ ] Missing tags detection
- [ ] Reading order validation
- [ ] Alt text for images in PDF
- [ ] PDF remediation suggestions
- [ ] Integration with main scan workflow

**Competitors:** Siteimprove, AudioEye, Deque
**Effort:** High | **Impact:** High

### Scheduled Monitoring
- [ ] Cron-based scan scheduler
- [ ] Daily/Weekly/Monthly options
- [ ] Email notifications on completion
- [ ] Score change alerts (regression detection)
- [ ] Dashboard for scheduled jobs

**Competitors:** All enterprise tools
**Effort:** Medium | **Impact:** High

### VPAT Generator
- [ ] VPAT 2.4 template
- [ ] Auto-populate from scan results
- [ ] WCAG 2.1/2.2 mapping
- [ ] Export to Word/PDF
- [ ] Accessibility Conformance Report (ACR)

**Competitors:** Deque, Siteimprove, Level Access, AudioEye
**Effort:** Medium | **Impact:** High

### SSO/SAML Authentication
- [ ] SAML 2.0 support
- [ ] Azure AD integration
- [ ] Google Workspace SSO
- [ ] Okta integration
- [ ] SSO configuration UI

**Competitors:** All enterprise tools
**Effort:** Medium | **Impact:** High

---

## P1 - HIGH PRIORITY (Q2 2025)
> Competitive parity

### Chrome Extension
- [ ] Browser extension scaffold
- [ ] Page scan from extension
- [ ] Overlay results on page
- [ ] Quick issue navigation
- [ ] Link to full report

**Competitors:** Deque axe, Evinced, Stark, WAVE
**Effort:** Medium | **Impact:** Medium

### Mobile Native App Scanning
- [ ] iOS app scanner (VoiceOver checks)
- [ ] Android app scanner (TalkBack checks)
- [ ] Touch target validation (44pt/48dp)
- [ ] React Native linting
- [ ] Mobile app report format

**Competitors:** Deque, Evinced, AudioEye
**Effort:** Very High | **Impact:** High

### Score Trending & History
- [ ] Historical scan storage
- [ ] Score over time charts
- [ ] Trend indicators (improving/declining)
- [ ] Compare scans side-by-side
- [ ] Export trend data

**Competitors:** Siteimprove, Pope Tech, AudioEye
**Effort:** Low | **Impact:** Medium

### Role-Based Access Control
- [ ] User roles (Admin, Editor, Viewer)
- [ ] Permission matrix
- [ ] Domain-level access control
- [ ] Invite team members
- [ ] Activity audit log

**Competitors:** All enterprise tools
**Effort:** Medium | **Impact:** Medium

### Accessibility Statement Generator
- [ ] Statement template
- [ ] Auto-populate from scans
- [ ] Compliance status
- [ ] Contact information
- [ ] Export HTML/PDF

**Competitors:** UserWay, Siteimprove
**Effort:** Low | **Impact:** Medium

---

## P2 - MEDIUM PRIORITY (Q3-Q4 2025)
> Market expansion

### WordPress Plugin
- [ ] WordPress plugin scaffold
- [ ] Dashboard widget
- [ ] Post/page scanning
- [ ] Admin settings page
- [ ] Gutenberg block checker

**Competitors:** accessiBe, UserWay, AudioEye, Siteimprove
**Effort:** Medium | **Impact:** Medium

### Shopify App
- [ ] Shopify app scaffold
- [ ] Theme scanner
- [ ] Product page checker
- [ ] Checkout flow audit
- [ ] App store listing

**Competitors:** accessiBe, UserWay, AudioEye
**Effort:** Medium | **Impact:** Medium

### Figma Plugin
- [ ] Figma plugin scaffold
- [ ] Contrast checker
- [ ] Touch target validator
- [ ] Focus order preview
- [ ] Design handoff annotations

**Competitors:** Stark, Evinced
**Effort:** High | **Impact:** Medium

### Legal Guarantee Program
- [ ] Define guarantee terms
- [ ] Partner with accessibility lawyers
- [ ] Insurance/coverage model
- [ ] Guarantee badge for sites
- [ ] Claim process

**Competitors:** accessiBe ($15-20K), AudioEye
**Effort:** Low (legal work) | **Impact:** Medium

### VS Code Extension
- [ ] VS Code extension scaffold
- [ ] Real-time linting
- [ ] Quick fixes
- [ ] Problem panel integration
- [ ] Settings configuration

**Competitors:** Deque axe Linter, Evinced
**Effort:** Medium | **Impact:** Low

### Full Site Crawler
- [ ] Automatic URL discovery
- [ ] Sitemap.xml parsing
- [ ] Robots.txt respect
- [ ] Crawl depth configuration
- [ ] Parallel scanning

**Competitors:** Siteimprove, Pope Tech
**Effort:** Medium | **Impact:** Medium

---

## P3 - NICE TO HAVE (2026)
> Differentiation & polish

### Color Blindness Simulation
- [ ] Protanopia filter
- [ ] Deuteranopia filter
- [ ] Tritanopia filter
- [ ] Achromatopsia filter
- [ ] Side-by-side comparison

**Competitors:** Stark, Siteimprove
**Effort:** Low | **Impact:** Low

### Training & Certification
- [ ] Video tutorials
- [ ] Written guides
- [ ] Certification exam
- [ ] Badges/certificates
- [ ] LMS integration

**Competitors:** Level Access, Deque University
**Effort:** High | **Impact:** Medium

### IntelliJ Plugin
- [ ] IntelliJ plugin scaffold
- [ ] Java/Kotlin support
- [ ] Android Studio integration

**Competitors:** Deque
**Effort:** Medium | **Impact:** Low

### Expert Manual Audit Service
- [ ] Partner network
- [ ] Booking system
- [ ] Audit workflow
- [ ] Report delivery
- [ ] Pricing model

**Competitors:** accessiBe, AudioEye, Level Access
**Effort:** High (ops) | **Impact:** Medium

### User Testing (Disabled Users)
- [ ] Tester network
- [ ] Test session management
- [ ] Video recording
- [ ] Feedback collection
- [ ] Report integration

**Competitors:** accessiBe, AudioEye, Level Access
**Effort:** Very High | **Impact:** Medium

---

## PROTECT & ENHANCE (Ongoing)
> Our unique advantages

### Tiered Contrast Scanner
- [ ] Performance optimization
- [ ] More gradient patterns
- [ ] Better text shadow detection
- [ ] APCA (WCAG 3.0) support
- [ ] Documentation & marketing

### Security + A11Y
- [ ] More OWASP rules
- [ ] Security score separate
- [ ] CVE database integration
- [ ] Security-specific reports

### Speed Optimization
- [ ] Maintain <1s scans
- [ ] Parallel rule execution
- [ ] Caching improvements
- [ ] CDN for assets

### Vision AI
- [ ] Better alt-text generation
- [ ] More fix suggestions
- [ ] Multi-language support
- [ ] Cost optimization

---

## COMPLETED
> Move items here when done

- [x] Landing page (qaudit.dev)
- [x] Competitor analysis document
- [x] Feature matrix document
- [x] MCP Server (basic)
- [x] CLI tool
- [x] 86 ACT rules
- [x] 5 report formats
- [x] Tiered Contrast Scanner
- [x] Security rules (OWASP)
- [x] Vision AI integration
- [x] GitHub repo setup

---

## METRICS TO TRACK

| Metric | Current | Q1 Target | Q2 Target |
|--------|---------|-----------|-----------|
| Rules count | 86 | 90 | 100 |
| False positive rate | <5% | <4% | <3% |
| Scan speed | <1s | <1s | <0.5s |
| WCAG 2.2 coverage | 95% | 98% | 100% |
| Enterprise features | 2/10 | 6/10 | 8/10 |

---

*Last updated: December 2025*
