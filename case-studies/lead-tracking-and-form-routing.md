# Case Study: Lead Tracking and Safe Form Routing

## Context

The commercial storefront needed a reliable confirmation step for paid-lead measurement while retaining the existing hosted form workflow. The site used two Formspree-powered commercial lead forms: a React form on the main experience and a Contact page form.

## Challenge

The tracking handoff required a confirmation-page visit after a successful form submission, but the existing form destination and payload could not be disrupted. The implementation also had to preserve the required market segmentation field, the optional website field, and the production React runtime.

## Approach

I created and published a dedicated `/pages/thank-you` route with a short confirmation message. I then added a redirect only inside each form’s successful-response branch. Failed responses and network errors continue to use the existing error state, so a visitor is not redirected when the hosted submission fails.

The hosted form destination and existing payload structure were preserved. No dashboard migration or replacement form provider was introduced.

## Implementation details

| Area | Result |
|---|---|
| Confirmation route | Published `/pages/thank-you` in Shopify and routed the React application to it |
| Form coverage | Applied the post-success redirect to both existing commercial lead forms |
| Form behavior | Redirect occurs only after a successful hosted-form response |
| Data continuity | Preserved the required Market Segment field and optional Website field |
| Runtime safety | Validated the production React bundle with `node --check` and retained the existing runtime-compatible JSX output |
| Deployment scope | Pushed only the affected Shopify theme asset and Contact template |
| Verification | Downloaded the live files after deployment, compared hashes, and checked the public Contact and confirmation pages |

## Result

Commercial form submissions now have a stable confirmation destination suitable for conversion measurement, without changing the existing form provider, payload, or error handling. The implementation is documented separately from the public overview so the main README stays focused on the most relevant development work.

## Skills demonstrated

This work demonstrates conversion-flow implementation, hosted-form integration, safe changes to compiled React assets, Shopify theme deployment, regression prevention, post-deployment verification, and technical documentation.

## Confidentiality note

This public case study omits account identifiers, credentials, customer submissions, private endpoint configuration details, proprietary source code, and internal email correspondence. The private contributions repository contains the operational deployment record and dated production snapshots.
