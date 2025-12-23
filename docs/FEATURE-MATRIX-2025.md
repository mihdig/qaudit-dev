# QAudit.dev - Complete Feature Matrix 2025

> Comprehensive comparison of all competitor features
> Last Updated: December 2025

---

## Executive Summary

### Legend
- ✅ = Full support
- ⚡ = Partial/Basic support
- 🚧 = In Development / Roadmap
- ❌ = Not available
- 🌟 = **QAudit Unique Feature**

### Quick Gap Analysis

| Category | QAudit Status | Priority Gap |
|----------|---------------|--------------|
| Core Scanning | ✅ Strong | - |
| Contrast Detection | 🌟 Best-in-class | - |
| Security | 🌟 Unique | - |
| PDF Scanning | ❌ Missing | **P0** |
| Mobile Native Apps | ❌ Missing | **P1** |
| Scheduled Monitoring | ❌ Missing | **P1** |
| Legal Guarantee | ❌ Missing | **P2** |
| Design Tool Plugins | ❌ Missing | **P2** |
| CMS Plugins | ❌ Missing | **P2** |

---

## 1. SCANNING CAPABILITIES

### 1.1 Web Page Scanning

| Feature | QAudit | Deque axe | Siteimprove | accessiBe | UserWay | AudioEye | Pope Tech | Evinced | TestParty |
|---------|--------|-----------|-------------|-----------|---------|----------|-----------|---------|-----------|
| Single page scan | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| Full site crawl | ⚡ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| Behind-login pages | ✅ | ✅ | ✅ | ❌ | ❌ | ✅ | ✅ | ✅ | ⚡ |
| JavaScript SPA support | ✅ | ✅ | ✅ | ⚡ | ⚡ | ✅ | ⚡ | ✅ | ✅ |
| Shadow DOM | ✅ | ✅ | ⚡ | ❌ | ❌ | ⚡ | ❌ | ✅ | ⚡ |
| iFrame scanning | ✅ | ✅ | ✅ | ⚡ | ⚡ | ✅ | ✅ | ✅ | ⚡ |
| Component-level scan | ✅ | ✅ | ❌ | ❌ | ❌ | ❌ | ❌ | ✅ | ⚡ |

**QAudit Status:** ✅ Strong
**Gap:** Full site crawl needs improvement (currently manual multi-URL)

---

### 1.2 Document & Media Scanning

| Feature | QAudit | Deque axe | Siteimprove | accessiBe | UserWay | AudioEye | Pope Tech | Evinced | TestParty |
|---------|--------|-----------|-------------|-----------|---------|----------|-----------|---------|-----------|
| **PDF Scanning** | ❌ | ✅ | ✅ | ❌ | ❌ | ✅ | ❌ | ❌ | ❌ |
| **PDF Remediation** | ❌ | ⚡ | ✅ | ❌ | ❌ | ✅ | ❌ | ❌ | ❌ |
| Word/Office docs | ❌ | ❌ | ✅ | ❌ | ❌ | ✅ | ❌ | ❌ | ❌ |
| Image alt-text audit | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| Video caption check | ⚡ | ✅ | ✅ | ⚡ | ⚡ | ✅ | ⚡ | ⚡ | ⚡ |
| Audio transcript | ⚡ | ⚡ | ✅ | ❌ | ❌ | ✅ | ⚡ | ❌ | ⚡ |

**QAudit Status:** ❌ Critical Gap
**Priority:** **P0 - PDF Scanning is table stakes for enterprise**

**Action Required:**
```
[ ] PDF accessibility scanner (PDF/UA-1 standard)
[ ] PDF remediation suggestions
[ ] Word document scanning (nice-to-have)
```

---

### 1.3 Mobile Scanning

| Feature | QAudit | Deque axe | Siteimprove | accessiBe | UserWay | AudioEye | Pope Tech | Evinced | TestParty |
|---------|--------|-----------|-------------|-----------|---------|----------|-----------|---------|-----------|
| Responsive web testing | ✅ | ✅ | ✅ | ⚡ | ⚡ | ✅ | ⚡ | ✅ | ✅ |
| Mobile viewport presets | ✅ | ✅ | ✅ | ❌ | ❌ | ✅ | ❌ | ✅ | ⚡ |
| Touch target detection | ✅ | ✅ | ✅ | ❌ | ❌ | ⚡ | ❌ | ✅ | ⚡ |
| **iOS Native App** | ❌ | ✅ | ❌ | ❌ | ❌ | ✅ | ❌ | ✅ | ❌ |
| **Android Native App** | ❌ | ✅ | ❌ | ❌ | ❌ | ✅ | ❌ | ✅ | ❌ |
| React Native | ❌ | ✅ | ❌ | ❌ | ❌ | ❌ | ❌ | ✅ | ❌ |

**QAudit Status:** ⚡ Partial (web only)
**Priority:** **P1 - Mobile native apps needed for enterprise**

**Action Required:**
```
[ ] iOS native app scanner (VoiceOver compatibility)
[ ] Android native app scanner (TalkBack compatibility)
[ ] React Native linting
```

---

## 2. CONTRAST & COLOR

### 2.1 Contrast Detection

| Feature | QAudit | Deque axe | Siteimprove | accessiBe | UserWay | AudioEye | Pope Tech | Evinced | Stark |
|---------|--------|-----------|-------------|-----------|---------|----------|-----------|---------|-------|
| CSS computed styles | ✅ | ✅ | ✅ | ⚡ | ⚡ | ✅ | ✅ | ✅ | ✅ |
| **Gradient backgrounds** | 🌟 | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ⚡ | ❌ |
| **Image backgrounds** | 🌟 | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ⚡ | ❌ |
| **Dual Screenshot** | 🌟 | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ |
| Semi-transparent overlay | 🌟 | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ⚡ | ❌ |
| Text shadow detection | 🌟 | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ |
| APCA (WCAG 3.0 draft) | ❌ | ⚡ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ✅ |

**QAudit Status:** 🌟 **UNIQUE ADVANTAGE - Tiered Contrast Scanner**

**Our Technology:**
```
TIER 1: CSS computed styles (~2ms)
TIER 2: Dual screenshot with/without text → pixel diff
TIER 3: Vision AI validation for edge cases
```

**No competitor has this capability!**

---

### 2.2 Color Tools

| Feature | QAudit | Deque axe | Siteimprove | Stark | accessiBe |
|---------|--------|-----------|-------------|-------|-----------|
| Contrast ratio calculator | ✅ | ✅ | ✅ | ✅ | ⚡ |
| Color blindness simulation | ❌ | ❌ | ✅ | ✅ | ✅ |
| Color palette analysis | ❌ | ❌ | ✅ | ✅ | ❌ |
| Suggested color fixes | ✅ | ✅ | ✅ | ✅ | ✅ |

**Gap:** Color blindness simulation would be valuable
**Priority:** P3

---

## 3. WCAG COMPLIANCE

### 3.1 Standards Coverage

| Standard | QAudit | Deque axe | Siteimprove | accessiBe | UserWay | AudioEye | Pope Tech |
|----------|--------|-----------|-------------|-----------|---------|----------|-----------|
| WCAG 2.0 A | ✅ | ✅ | ✅ | ⚡ | ⚡ | ✅ | ✅ |
| WCAG 2.0 AA | ✅ | ✅ | ✅ | ⚡ | ⚡ | ✅ | ✅ |
| WCAG 2.1 A | ✅ | ✅ | ✅ | ⚡ | ⚡ | ✅ | ✅ |
| WCAG 2.1 AA | ✅ | ✅ | ✅ | ⚡ | ⚡ | ✅ | ✅ |
| WCAG 2.2 AA | ✅ | ✅ | ✅ | ❌ | ❌ | ⚡ | ✅ |
| WCAG 2.2 AAA | ⚡ | ⚡ | ✅ | ❌ | ❌ | ❌ | ⚡ |
| Section 508 | ✅ | ✅ | ✅ | ⚡ | ⚡ | ✅ | ✅ |
| ADA | ✅ | ✅ | ✅ | ⚡ | ⚡ | ✅ | ✅ |
| EAA / EN 301 549 | ✅ | ✅ | ✅ | ❌ | ❌ | ⚡ | ⚡ |
| AODA (Canada) | ✅ | ✅ | ✅ | ⚡ | ⚡ | ✅ | ⚡ |

**QAudit Status:** ✅ Strong compliance coverage

---

### 3.2 Rule Coverage

| Metric | QAudit | Deque axe | Siteimprove | AudioEye | Pope Tech | WAVE |
|--------|--------|-----------|-------------|----------|-----------|------|
| Total rules | **86** | ~80 | 100+ | 32 | 100+ | 100+ |
| ACT-validated | ✅ | ✅ | Partial | ❌ | Partial | Partial |
| False positive rate | <5% | ~5% | ~8% | ~10% | ~15% | ~15% |
| Auto-detectable WCAG | ~55% | ~55% | ~60% | ~25% | ~55% | ~55% |

**QAudit Status:** ✅ Competitive rule coverage

---

## 4. SECURITY SCANNING

| Feature | QAudit | Deque axe | Siteimprove | accessiBe | UserWay | AudioEye | Evinced |
|---------|--------|-----------|-------------|-----------|---------|----------|---------|
| **OWASP Top 10** | 🌟 | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ |
| CSRF detection | 🌟 | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ |
| XSS vulnerability | 🌟 | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ |
| Mixed content | 🌟 | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ |
| External scripts audit | 🌟 | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ |
| Hidden secrets detection | 🌟 | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ |
| Inline event handlers | 🌟 | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ |
| HTTP security headers | 🌟 | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ |

**QAudit Status:** 🌟 **UNIQUE ADVANTAGE - Only tool combining A11Y + Security**

**Our Security Rules:**
- `security-csrf-token` - CSRF protection check
- `security-mixed-content` - HTTP/HTTPS mixing
- `security-external-scripts` - Third-party script audit
- `security-inline-handlers` - onclick/onload detection
- `security-hidden-secrets` - API keys, tokens in HTML

---

## 5. AI & AUTOMATION

### 5.1 AI Features

| Feature | QAudit | Deque axe | Siteimprove | accessiBe | UserWay | AudioEye | TestParty | Evinced |
|---------|--------|-----------|-------------|-----------|---------|----------|-----------|---------|
| **Auto alt-text generation** | ✅ | ❌ | ⚡ | ✅ | ✅ | ✅ | ✅ | ❌ |
| AI fix suggestions | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| **Auto code remediation** | ⚡ | ⚡ | ⚡ | ✅* | ✅* | ✅* | ✅ | ⚡ |
| Natural language chat | ✅ | ✅ | ✅ | ❌ | ❌ | ❌ | ❌ | ✅ |
| Issue clustering | ❌ | ⚡ | ✅ | ❌ | ❌ | ⚡ | ❌ | ✅ |
| Priority scoring | ✅ | ✅ | ✅ | ❌ | ❌ | ✅ | ⚡ | ✅ |
| Visual AI detection | ✅ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ✅ |

*overlay-based, not real code fixes

**QAudit Status:** ✅ Strong AI capabilities via Vision AI

**Our Vision AI:**
- Auto alt-text generation
- Fix suggestions in natural language
- Visual element detection
- Text-on-image analysis

---

### 5.2 Automation & CI/CD

| Feature | QAudit | Deque axe | Siteimprove | Pope Tech | Evinced | TestParty |
|---------|--------|-----------|-------------|-----------|---------|-----------|
| CLI tool | ✅ | ✅ | ❌ | ❌ | ✅ | ✅ |
| REST API | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| GitHub Actions | ✅ | ✅ | ⚡ | ❌ | ✅ | ✅ |
| GitLab CI | ✅ | ✅ | ⚡ | ❌ | ✅ | ✅ |
| Jenkins plugin | ❌ | ✅ | ⚡ | ❌ | ✅ | ⚡ |
| Jest integration | ✅ | ✅ | ❌ | ❌ | ✅ | ⚡ |
| Cypress integration | ⚡ | ✅ | ❌ | ❌ | ✅ | ⚡ |
| Playwright integration | ✅ | ✅ | ❌ | ❌ | ✅ | ⚡ |
| Selenium integration | ⚡ | ✅ | ❌ | ❌ | ✅ | ⚡ |

**QAudit Status:** ✅ Good CI/CD support

**Gap:** Official Cypress/Selenium SDKs need polish
**Priority:** P2

---

## 6. IDE & DEVELOPER TOOLS

### 6.1 IDE Integration

| Feature | QAudit | Deque axe | Evinced | TestParty | Stark |
|---------|--------|-----------|---------|-----------|-------|
| **MCP Server** | ✅ | ✅ | ✅ | ❌ | ❌ |
| VS Code extension | ❌ | ✅ | ✅ | ❌ | ❌ |
| IntelliJ plugin | ❌ | ✅ | ❌ | ❌ | ❌ |
| Chrome extension | ❌ | ✅ | ✅ | ❌ | ✅ |
| Firefox extension | ❌ | ⚡ | ❌ | ❌ | ✅ |
| Static code linting | ❌ | ✅ | ✅ | ⚡ | ❌ |

**QAudit Status:** ⚡ MCP only, needs browser extension

**Action Required:**
```
[ ] Chrome extension (P1)
[ ] VS Code extension (P2)
[ ] Static linter (P3)
```

---

### 6.2 MCP Server Comparison

| Feature | QAudit MCP | axe MCP Server |
|---------|------------|----------------|
| Claude Code support | ✅ | ✅ |
| Cursor support | ✅ | ✅ |
| VS Code support | ✅ | ✅ |
| GitHub Copilot | ⚡ | ✅ |
| Real-time scanning | ✅ | ✅ |
| Fix suggestions | ✅ | ✅ |
| Knowledge base | ⚡ | ✅ (Deque University) |
| **Tiered Contrast** | 🌟 | ❌ |
| **Security scanning** | 🌟 | ❌ |
| **Vision AI** | 🌟 | ❌ |
| Enterprise security | ⚡ | ✅ |

**QAudit Advantages over axe MCP:**
- Tiered Contrast Scanner
- Security scanning
- Vision AI capabilities

**axe MCP Advantages:**
- Deque University integration
- Enterprise security certifications
- Larger knowledge base

---

## 7. DESIGN TOOLS

| Feature | QAudit | Stark | Deque | Siteimprove | Evinced |
|---------|--------|-------|-------|-------------|---------|
| **Figma plugin** | ❌ | ✅ | ❌ | ❌ | ✅ |
| **Sketch plugin** | ❌ | ✅ | ❌ | ❌ | ❌ |
| Adobe XD plugin | ❌ | ✅ | ❌ | ❌ | ❌ |
| Design handoff | ❌ | ✅ | ❌ | ❌ | ✅ |
| Typography analysis | ❌ | ✅ | ❌ | ❌ | ❌ |
| Focus order preview | ❌ | ✅ | ❌ | ❌ | ❌ |
| Landmarks visualization | ❌ | ✅ | ❌ | ❌ | ❌ |

**QAudit Status:** ❌ No design tool integration
**Priority:** P2 - Figma plugin would expand market

**Action Required:**
```
[ ] Figma plugin (P2)
[ ] Design-to-code handoff (P3)
```

---

## 8. CMS & PLATFORM PLUGINS

| Platform | QAudit | accessiBe | UserWay | AudioEye | Siteimprove |
|----------|--------|-----------|---------|----------|-------------|
| **WordPress** | ❌ | ✅ | ✅ | ✅ | ✅ |
| **Shopify** | ❌ | ✅ | ✅ | ✅ | ⚡ |
| Wix | ❌ | ✅ | ✅ | ✅ | ❌ |
| Squarespace | ❌ | ✅ | ✅ | ✅ | ❌ |
| Webflow | ❌ | ✅ | ✅ | ⚡ | ❌ |
| Drupal | ❌ | ✅ | ✅ | ✅ | ⚡ |
| Magento | ❌ | ✅ | ✅ | ✅ | ⚡ |
| HubSpot | ❌ | ⚡ | ✅ | ⚡ | ✅ |
| BigCommerce | ❌ | ✅ | ✅ | ✅ | ❌ |

**QAudit Status:** ❌ No CMS plugins
**Priority:** P2 - WordPress/Shopify would capture SMB market

**Action Required:**
```
[ ] WordPress plugin (P2)
[ ] Shopify app (P2)
```

---

## 9. MONITORING & SCHEDULING

| Feature | QAudit | Siteimprove | accessiBe | UserWay | AudioEye | Pope Tech |
|---------|--------|-------------|-----------|---------|----------|-----------|
| **Scheduled scans** | ❌ | ✅ | ✅ | ✅ | ✅ | ✅ |
| **24/7 monitoring** | ❌ | ✅ | ✅ | ✅ | ✅ | ⚡ |
| Email alerts | ❌ | ✅ | ⚡ | ⚡ | ✅ | ✅ |
| Slack notifications | ✅ | ✅ | ❌ | ❌ | ⚡ | ❌ |
| Score trending | ❌ | ✅ | ❌ | ❌ | ✅ | ✅ |
| Regression detection | ❌ | ✅ | ❌ | ❌ | ✅ | ✅ |
| SLA monitoring | ❌ | ✅ | ❌ | ❌ | ✅ | ❌ |

**QAudit Status:** ❌ Critical gap for enterprise
**Priority:** **P1 - Scheduled monitoring is expected**

**Action Required:**
```
[ ] Scheduled scan jobs (daily/weekly/monthly)
[ ] Email notifications on score changes
[ ] Score history and trending charts
[ ] Regression alerts
```

---

## 10. REPORTING

### 10.1 Report Types

| Report Type | QAudit | Deque axe | Siteimprove | AudioEye | Pope Tech |
|-------------|--------|-----------|-------------|----------|-----------|
| JSON export | ✅ | ✅ | ✅ | ✅ | ✅ |
| HTML report | ✅ | ✅ | ✅ | ✅ | ✅ |
| PDF export | ⚡ | ✅ | ✅ | ✅ | ✅ |
| CSV export | ✅ | ✅ | ✅ | ✅ | ✅ |
| **Executive summary** | ✅ | ⚡ | ✅ | ✅ | ⚡ |
| **Developer report** | ✅ | ✅ | ✅ | ✅ | ✅ |
| **QA checklist** | ✅ | ⚡ | ⚡ | ⚡ | ⚡ |
| **Designer report** | ✅ | ❌ | ⚡ | ❌ | ❌ |
| EAA compliance report | ✅ | ⚡ | ✅ | ❌ | ❌ |

**QAudit Status:** ✅ Strong - 5 report formats

---

### 10.2 VPAT & Compliance Docs

| Feature | QAudit | Deque axe | Siteimprove | Level Access | AudioEye |
|---------|--------|-----------|-------------|--------------|----------|
| **VPAT generation** | ❌ | ✅ | ✅ | ✅ | ✅ |
| ACR (Accessibility Conformance Report) | ❌ | ✅ | ✅ | ✅ | ✅ |
| Accessibility statement | ❌ | ⚡ | ✅ | ✅ | ✅ |
| Compliance roadmap | ❌ | ⚡ | ✅ | ✅ | ⚡ |

**QAudit Status:** ❌ Missing compliance documentation
**Priority:** P1 - Enterprise requirement

**Action Required:**
```
[ ] VPAT generator (P1)
[ ] Accessibility statement template (P1)
[ ] ACR export (P2)
```

---

## 11. TEAM & GOVERNANCE

| Feature | QAudit | Siteimprove | Deque | Pope Tech | Level Access |
|---------|--------|-------------|-------|-----------|--------------|
| Multi-user support | ⚡ | ✅ | ✅ | ✅ | ✅ |
| Role-based access | ❌ | ✅ | ✅ | ✅ | ✅ |
| Team workspaces | ❌ | ✅ | ✅ | ✅ | ✅ |
| **SSO/SAML** | ❌ | ✅ | ✅ | ✅ | ✅ |
| Audit trail | ❌ | ✅ | ✅ | ✅ | ✅ |
| Task assignment | ❌ | ✅ | ⚡ | ✅ | ✅ |
| Jira integration | ✅ | ✅ | ✅ | ✅ | ✅ |
| Asana integration | ❌ | ⚡ | ❌ | ✅ | ⚡ |

**QAudit Status:** ❌ Needs enterprise governance features
**Priority:** P1 for enterprise tier

**Action Required:**
```
[ ] SSO/SAML authentication (P1)
[ ] Role-based access control (P1)
[ ] Audit logs (P1)
[ ] Team workspaces (P2)
```

---

## 12. LEGAL & SUPPORT

| Feature | QAudit | accessiBe | AudioEye | Level Access | UserWay |
|---------|--------|-----------|----------|--------------|---------|
| **Legal guarantee** | ❌ | ✅ ($15-20K) | ✅ | ✅ | ⚡ |
| Litigation support | ❌ | ✅ | ✅ | ✅ | ⚡ |
| Expert audits | ⚡ | ✅ | ✅ | ✅ | ✅ |
| User testing (disabled users) | ❌ | ✅ | ✅ | ✅ | ⚡ |
| Training/certification | ❌ | ⚡ | ⚡ | ✅ | ⚡ |

**QAudit Status:** ❌ No legal protection
**Priority:** P2 - Differentiator for risk-averse customers

**Action Required:**
```
[ ] Legal guarantee program (P2)
[ ] Partner with accessibility lawyers (P2)
[ ] Expert manual audit service (P2)
```

---

## 13. PERFORMANCE

| Metric | QAudit | Deque axe | Siteimprove | AudioEye | WAVE |
|--------|--------|-----------|-------------|----------|------|
| Single page scan | **<1s** | 2-5s | 3-5s | 2-3s | 3-5s |
| Full site (100 pages) | ~2min | ~5min | Hours | ~10min | N/A |
| API response time | **<500ms** | ~1s | ~2s | ~1s | N/A |
| CI/CD overhead | **Minimal** | Low | High | Medium | N/A |

**QAudit Status:** 🌟 **Fastest scanner in market**

---

## PRIORITY ROADMAP

### P0 - Critical (Q1 2025)

| Feature | Effort | Impact | Competitor Parity |
|---------|--------|--------|-------------------|
| PDF Scanning | High | High | Siteimprove, AudioEye, Deque |
| Scheduled Monitoring | Medium | High | All enterprise tools |
| VPAT Generator | Medium | High | All enterprise tools |

### P1 - High Priority (Q2 2025)

| Feature | Effort | Impact | Competitor Parity |
|---------|--------|--------|-------------------|
| iOS/Android Native | Very High | High | Deque, Evinced, AudioEye |
| SSO/SAML | Medium | High | Enterprise tools |
| Chrome Extension | Medium | Medium | Deque, Evinced, Stark |
| Role-based Access | Medium | Medium | Enterprise tools |
| Score Trending | Low | Medium | Siteimprove, Pope Tech |

### P2 - Medium Priority (Q3-Q4 2025)

| Feature | Effort | Impact | Competitor Parity |
|---------|--------|--------|-------------------|
| WordPress Plugin | Medium | Medium | accessiBe, UserWay |
| Shopify App | Medium | Medium | accessiBe, UserWay |
| Figma Plugin | High | Medium | Stark, Evinced |
| Legal Guarantee | Low (legal) | Medium | accessiBe, AudioEye |
| VS Code Extension | Medium | Low | Deque, Evinced |

### P3 - Nice to Have (2026)

| Feature | Effort | Impact |
|---------|--------|--------|
| Color blindness sim | Low | Low |
| IntelliJ Plugin | Medium | Low |
| Sketch Plugin | Medium | Low |
| Training/Certification | High | Medium |

---

## UNIQUE QAUDIT ADVANTAGES (PROTECT & PROMOTE)

### Features NO competitor has:

1. **Tiered Contrast Scanner**
   - Dual screenshot method
   - Gradient/image background detection
   - Text shadow analysis
   - **Marketing: "See contrast like humans do"**

2. **Security + A11Y Combined**
   - OWASP Top 10 in same scan
   - Single tool for both audits
   - **Marketing: "Complete audit, not just accessibility"**

3. **Scan Speed**
   - <1 second per page
   - 5-10x faster than competitors
   - **Marketing: "Fastest accessibility scanner"**

4. **Price/Feature Ratio**
   - Enterprise features at $149/mo
   - Competitors charge $500-28K for similar
   - **Marketing: "Enterprise power, startup pricing"**

---

## SUMMARY: WHAT TO BUILD NEXT

### Must Have (Blocking Sales)
1. ❌ PDF Scanning
2. ❌ Scheduled Monitoring
3. ❌ VPAT Generator
4. ❌ SSO/SAML

### Should Have (Competitive)
5. ❌ Chrome Extension
6. ❌ Mobile Native Apps
7. ❌ Score Trending
8. ❌ Role-based Access

### Nice to Have (Market Expansion)
9. ❌ WordPress Plugin
10. ❌ Figma Plugin
11. ❌ Legal Guarantee
12. ❌ VS Code Extension

---

*Document maintained by QAudit Product Team*
*Sources: Direct competitor website analysis, December 2025*
