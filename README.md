# EchoSweep website

Official static website and privacy-policy publication surface for the EchoSweep Android app.

## Publication model

- Hosting: GitHub Pages
- Canonical domain: `https://echosweep.pl`
- Source: repository root on `main`
- Technology: plain HTML and CSS; no build system; no JavaScript
- Tracking: no analytics, advertising, tracking pixels, external fonts, or third-party scripts

## Public pages

- `/` — EchoSweep overview
- `/privacy/` — canonical English Privacy Policy
- `/data-and-permissions/` — device data and Android permission explanation
- `/support/` — support and privacy contact

## Local preview

From the repository root:

```text
python -m http.server 8000
```

Then open `http://localhost:8000/`.

## Maintenance

Before publishing a policy change, reconcile the website with:

1. the exact EchoSweep release being documented;
2. the Google Play Data safety declaration;
3. current Android permissions and dependencies;
4. the current publisher and support-contact identity.

Operational documentation:

- `docs/DNS_AND_PAGES_GUIDE.md`
- `docs/VALIDATION_REPORT.md`

## Truth boundary

This repository documents the public website and policy text. Repository content alone does not prove runtime behavior of an Android release, legal compliance, Google Play acceptance, or successful DNS and HTTPS publication.
