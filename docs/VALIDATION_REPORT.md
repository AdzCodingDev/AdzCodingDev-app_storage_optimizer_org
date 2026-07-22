# EchoSweep website validation report

Updated: 2026-07-06

## Scope

Static source validation of the public website implementation before GitHub Pages publication.

## Architecture

- plain HTML and CSS;
- no JavaScript;
- no package manager or build system;
- repository-root GitHub Pages layout;
- `.nojekyll` included;
- apex-domain `CNAME` included.

## Visual adaptation

The visual system was adapted from EchoSweep app screenshots without copying screen layouts or embedding the screenshots. The site uses a near-black background, graphite cards, lilac and pink highlights, restrained violet glow, rounded containers, and large readable controls.

## Static checks completed

- HTML files parse as documents;
- every public page has one visible `h1`;
- heading levels are structurally ordered;
- internal navigation targets exist in the source tree;
- stylesheet and icon references resolve in the source tree;
- canonical URLs use HTTPS and `echosweep.pl`;
- `robots.txt` points to the canonical sitemap;
- the sitemap contains all four public pages;
- `CNAME` contains exactly `echosweep.pl`;
- no `<script>`, iframe, form, external font, tracking pixel, analytics tag, or advertising resource is present;
- no HTTP asset URL is present;
- the contact email is consistently `privacy@adz-dev-coding.pl`;
- the publisher name is consistently `Adz Dev Coding`;
- responsive rules cover phone, tablet, and desktop layouts;
- keyboard-visible focus styles and skip links are present;
- reduced-motion preference is respected;
- decorative images use empty alternative text;
- semantic navigation, main content, sections, lists, and footer are used.

## External-resource audit

The pages automatically load only repository-hosted HTML, CSS, and SVG assets. External hyperlinks may be followed by the user, but the site does not automatically load third-party resources.

## Privacy-content boundary

The public text was reviewed against the documented EchoSweep product boundary and relevant Android source before publication preparation. Claims about universal runtime safety, exact release behavior, final Google Play Data safety answers, legal compliance, and successful publication are excluded or qualified.

## Not established by static source validation

- successful GitHub Pages deployment;
- current DNS propagation;
- TLS certificate issuance or HTTPS enforcement;
- live redirect behavior;
- rendered-browser and assistive-technology testing across target devices;
- professional legal review;
- behavior of the exact production Android artifact;
- Google Play acceptance.

## Publication gate

Before the site is treated as live:

1. merge the reviewed website change with explicit authorization;
2. make the website repository public if GitHub Free is used;
3. enable GitHub Pages from `main` and repository root;
4. configure and verify the custom domain and DNS;
5. enable HTTPS after certificate provisioning;
6. open and reread every live public page;
7. reconcile the privacy text with the exact release and final Google Play Data safety declaration.
