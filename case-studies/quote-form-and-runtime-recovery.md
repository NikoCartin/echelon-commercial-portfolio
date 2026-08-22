# Case Study: Quote Flow, Runtime Recovery, and Safe Deployment

## Context

A commercial website needs a dependable path from buyer interest to a qualified sales conversation. The quote form must collect useful segmentation data, submit reliably, and remain compatible with the front-end runtime used by the production bundle.

## Challenge

The quote flow had lost its Market Segment field and was reporting failed submissions. A subsequent UI patch introduced JSX helper calls that were incompatible with the runtime already present in the minified production bundle, resulting in a blank application and the error `TypeError: m.jsx is not a function`.

## Approach

I first isolated the issue from the browser stack trace and preserved the last known working bundle. I then restored the stable runtime pattern, reintroduced Market Segment as a required field, mapped the approved commercial categories, configured the hosted form destination, and validated the live asset after deployment.

The recovery process included a clear separation between experimental files and the verified baseline. Each change was syntax-checked before deployment, and the live bundle was fetched again after deployment to confirm the expected runtime markers and form fields.

## Implementation details

| Area | Result |
|---|---|
| Market Segment | Required field with approved commercial categories |
| Form destination | Hosted Formspree endpoint configured by the site owner |
| Payload | Segment submitted under a stable `market_segment` field |
| Runtime compatibility | Removed incompatible `m.jsx` and `m.jsxs` calls from the live bundle |
| Recovery | Re-established a verified stable bundle after the blank-screen incident |
| Deployment control | Targeted Shopify asset pushes and post-deployment verification |
| Reproducibility | Stable baseline, SHA-256 records, and rollback instructions |

## Result

The application returned to a working state, the quote form retained the commercially important segmentation field, and the update process gained a safer baseline and rollback discipline. The same validation pattern can be applied to future form, navigation, and bundle changes.

## Skills demonstrated

This work demonstrates incident diagnosis, browser-console analysis, React runtime compatibility, form integration, data capture design, Shopify deployment, asset integrity verification, rollback planning, and technical documentation.

## Confidentiality note

This public case study intentionally omits private endpoint configuration details, credentials, customer submissions, proprietary code, and internal operational data. It focuses on the engineering problem and the method used to resolve it.
