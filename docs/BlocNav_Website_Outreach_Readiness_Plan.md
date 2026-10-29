# GTM-01A — BlocNav Website Outreach Readiness (kelleysite)

**Status:** IMPLEMENTATION PROPOSED FOR REVIEW — not published, deployed, or production-verified  
**Date:** 2026-10-29  
**Repository:** `L3Pro/blocnav-site`  
**Source:** `kelleysite` at `7ce24372f3e3d63d046e2527de339e0ef5b6b76e`  
**Change branch:** `gtm/01a-kelleysite-outreach-20261029`  
**Scope:** Content-only outreach-readiness refresh plus removal of production-irrelevant editor controls.  
**Authority:** This is a website workstream, not an engineering design gate or approval to activate external operational pilots.

## 1. Decision and purpose

Keep the light-theme website's visual identity and the existing hero statement, **"Maps that work when the internet doesn't."** Update the accompanying language to support exploratory conversations with municipal public works, infrastructure, emergency response, and geospatial data-quality professionals. Do **not** portray NG911 data-quality automation, MS4 compliance management, or permanent municipal asset history as shipped products.

The site should build trust and open conversations, not claim full GIS replacement or production-ready managed service.

## 2. Roadmap location

- **GTM-01A (now; parallel with engineering):** Correct unsupported marketing statements, broaden field-workflow positioning, make contact and availability language accurate, and remove legacy editor code from the published homepage.
- **Release Phase 0 — Trust foundation:** Corresponding application security, reliability, authentication, source access and offline-data-preservation work remains governed by `blocnav-prod` North Star and existing design gates. This site update does not close those gates.
- **Release Phase 1 — Pilot-ready core:** Demonstrations and public works observations may expand only after actual workflow acceptance; operational access requires independent pilot readiness approval, environment parity and security gates.
- **Release Phase 2 — Forms MVP:** Consider marketing standardized inspection forms and stormwater inspection workflows only when implemented and accepted.
- **Release Phase 4 — Operational platform:** Do not market durable system-of-record or ongoing cross-project asset history before its data lifecycle and organizational controls are accepted.

**Scope isolation:** Package A (repository hygiene) and Package B (behavior-preserving modularization) in the application repository proceed independently. No application code, services, migrations, customer data or deployment settings are modified by GTM-01A.

## 3. Changes proposed for the site

| Area | Change | Why |
| --- | --- | --- |
| Hero | Retain established headline, add a short description of field observations and active-development status | Preserve recognition while clarifying product scope |
| Audience | Add public works, utility/infrastructure fieldwork and GIS field teams alongside SAR | Support both exploratory outreach tracks |
| Trust | Replace "Zero Data Loss", "no failed syncs", "works on any device", universal setup-time and other absolute guarantees | Avoid unsupported reliability and compatibility promises |
| Safety | Qualify Driver Mode as passenger/safely-stopped use | Avoid endorsing distracted driving |
| Competitive comparison | Replace unsourced Esri price/failure comparisons with a neutral "field need / BlocNav approach" table | Do not misstate other tools' capabilities or pricing |
| Collaboration | Describe project sharing as being validated for pilot use | Avoid implying live multi-tenant production readiness |
| Contact | Change primary CTA to "Discuss Your Field Workflow"; prefill an email subject; keep `contact@blocnav.com` visible | Make discussion the primary conversion |
| About section | Do not add a founder bio or company-about block to the homepage | Keep the product and discovery CTA central; provide individual credentials through outreach and professional profiles |
| Product imagery | Preserve screenshot/map assets; label annotations and sample sync status as illustrative | Avoid implying sample labels are measured live data |
| Editor controls | Remove hidden "Tweaks" panel, its message listener and script; preserve its current default two-column feature grid in CSS | Remove production-irrelevant editing behavior without redesign |
| SEO | Revise homepage meta description | Match current scope and avoid unsupported licensing comparison |

## 4. Deliberately not included

- No redesign, framework conversion, changed logo/assets, or new pricing page.
- No public-works, NG911 or stormwater-specific landing pages until interviews establish actual demand.
- No claims of certified NG911 validation, MS4 compliance, automated inspection reporting, direct Esri integration, enterprise asset management, or permanent organizational record retention.
- No edits to `mocsar.html`, `qr.html`, `terms.html`, `privacy.html`, or `slow-networks.html` in this PR. These retain their prior behavior and copy.

## 5. Follow-up reviews required

1. **Privacy accuracy (separate review):** Verify current account authentication, source of location records, background GPS behavior, storage, retention, permissions, photo and sharing claims before editing legal copy. Seek appropriate legal review for policies; do not silently alter them to match marketing text.
2. **SAR demo accuracy:** Validate `mocsar.html` and `qr.html` links, intended `map.blocnav.com?demo=sar` behavior, and any claims that records flow to existing customer tools.
3. **Contact delivery:** Confirm `contact@blocnav.com` is monitored, and `lj@blocnav.com` can send and receive replies; check SPF, DKIM and DMARC before outreach.
4. **Company positioning:** Keep personal biographies off the homepage. Share geospatial credentials through direct outreach and relevant professional profiles.
5. **Release/security:** Verify authenticated/private operational data is not accessible through unauthenticated tile/catalog routes and complete the independently approved environment and pilot readiness gates before using real customer private/shared data.

## 6. Acceptance checklist

- [ ] Diff is limited to `index.html` and this planning document.
- [ ] `kelleysite` is verified as the actual GitHub Pages publication source in repository settings; do not assume the default `main` branch.
- [ ] Original light design, logo, hero imagery, map image, responsive behavior and SAR demo remain intact.
- [ ] Reviewers approve wording without unsupported guarantees, broad competitor attacks or implied production eligibility.
- [ ] A human verifies the screenshot annotation disclaimer and checks that no personal biography is included.
- [ ] HTML/link/static checks pass; visual review at 320, 390, 768 and 1440 px; mobile navigation and keyboard accessibility checked.
- [ ] Email CTA opens a compose window addressed to `contact@blocnav.com`; inbox is tested externally.
- [ ] No application or deployment changes are bundled.
- [ ] PR is approved before merge; publication is verified separately after merge.

## 7. Customer-discovery intent

Use the site to support conversations, not pre-sell a hypothetical product. The two initial tracks are (A) NG911 regional geospatial quality-control discovery and (B) small-municipality/public-works field observations and infrastructure-inspection discovery. Both require validation of recurring pain, budget, buyer, and current system alternatives.

**Commercial gate:** No additional product feature sprint based on web copy alone. Customer interviews, observed workflows and purchase intent determine whether to extend BlocNav or pursue a separate geospatial QA tool.
