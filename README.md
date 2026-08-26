# Echelon Commercial Site Engineering Portfolio

![Current Echelon Commercial storefront hero](assets/echelon-commercial-current.png)

A public overview of contributions to a commercial fitness e-commerce experience built on Shopify. The work combined front-end product experience, product-data operations, technical SEO and link auditing, documentation, runtime recovery, and production deployment discipline.

> Live experience: [echeloncommercial.com](https://echeloncommercial.com/)

## What I contributed

| Workstream | Representative contribution |
|---|---|
| Shopify front end | Maintained a React-powered commercial storefront and product-detail experience within a Shopify theme |
| Product information | Translated approved sell sheets and specification documents into consistent product descriptions, Features, Specs, warranties, and downloadable resources |
| PDP experience | Added direct spec-sheet downloads beside quote CTAs across a broad product catalog |
| Commercial UX | Organized equipment and market taxonomy, corrected navigation and product routing, and improved quote-oriented presentation |
| Forms and lead flow | Restored Market Segment capture, made it required, and routed the commercial quote flow to a hosted form endpoint |
| Quality assurance | Audited page routes, product handles, assets, PDFs, runtime behavior, and production bundle integrity |
| Incident recovery | Diagnosed and recovered from a JavaScript runtime regression, then established a verified stable baseline and rollback process |
| Documentation | Created repeatable update, validation, deployment, and recovery procedures |

## Selected outcomes

The work included updates across cardio, strength, Pilates, recovery, ThermaChill, sauna, and commercial wellness products. Product pages were aligned to approved source documents rather than relying on generic category copy. The process also introduced a stable-bundle workflow so future updates begin from a verified production baseline instead of an older experimental bundle. The August 2026 production pass added audience-specific market visuals, corrected active product-promotion language, removed an inactive search control, repaired stale destinations, and documented a route- and asset-level verification pass.

The quote experience now captures a required `Market Segment` selection using commercial categories such as Multifamily, Education, Corporate Wellness, Recreation, Government, Sports Performance, Fitness, Hospitality, Healthcare, Clubs, and Sports. The public portfolio intentionally describes the workflow without publishing private customer data or operational credentials.

## Tech Stack

| Layer | Technologies and usage |
|---|---|
| Storefront platform | Shopify Online Store theme architecture and Liquid templates |
| Front end | React with JavaScript and JSX, delivered through compiled production bundles |
| Markup and styling | HTML and CSS for Shopify theme structure, responsive layouts, product interfaces, and forms |
| Product experience | Shopify theme assets, CDN-hosted resources, product handles, PDP routing, and direct document downloads |
| Lead capture | Formspree for hosted quote-form submission and structured Market Segment data |
| Automation and QA | Python for source extraction, auditing, comparison, and deployment preparation; Node.js for JavaScript syntax validation |
| Version control and delivery | Git, GitHub, Shopify CLI, targeted theme-asset deployment, SHA-256 verification, and rollback procedures |

The portfolio intentionally does not claim a language or framework that was not confirmed in the available production artifacts. The focus is on the technologies directly evidenced by the storefront, deployment workflow, validation scripts, and public contribution record.

## Technical highlights

The implementation required working with minified production assets, React runtime compatibility, Shopify theme asset deployment, deterministic validation, and browser-level troubleshooting. A runtime regression caused by incompatible JSX helper calls was isolated through the stack trace, corrected by using the runtime already present in the bundle, and verified against the live asset after deployment.

The product-data workflow used source-document extraction, structured mapping, targeted bundle edits, syntax validation, deployment checks, and post-deployment verification. This reduced the risk of mismatched claims across product descriptions, Features, Specs, warranties, and downloadable sell sheets.

## Portfolio case studies

- [Production hardening and storefront audit ,  August 2026](case-studies/production-hardening-and-audit-2026-08.md)
- [Product information and PDP system](case-studies/product-data-operations.md)
- [Quote form, runtime recovery, and deployment discipline](case-studies/quote-form-and-runtime-recovery.md)

## Repository structure

| Path | Purpose |
|---|---|
| `assets/` | Public preview image used by this README |
| `case-studies/` | Summaries of representative work |
| `docs/` | Scope, disclosure, and reproducibility notes |

## Scope and disclosure

This repository is a sanitized portfolio, not the private source repository for the commercial site. It does not include proprietary sell sheets, production bundles, Shopify credentials, Formspree credentials, customer information, cookies, `.env` files, private screenshots, or internal access details. The public case studies focus on problem-solving, implementation approach, quality controls, and outcomes.

## Contact

For opportunities involving front-end engineering, e-commerce UX, Shopify implementations, product-data systems, technical operations, or production incident recovery, please reach out through my GitHub profile.
