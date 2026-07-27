# EchoSweep website validation report

Updated: 2026-07-27

## Scope

Static source validation of the public website implementation and later bounded content and responsive-layout updates.

## Architecture

- plain HTML and CSS;
- no JavaScript;
- no package manager or build system;
- repository-root GitHub Pages layout;
- `.nojekyll` included;
- apex-domain `CNAME` included.

## Visual adaptation

The visual system was adapted from EchoSweep app screenshots without copying screen layouts or embedding the screenshots. The site uses a near-black background, graphite cards, lilac and pink highlights, restrained violet glow, rounded containers, and large readable controls.

## Mobile and large-text polish checkpoint

The responsive layout was tightened after reviewing operator-supplied Android Chrome screenshots from a Motorola razr 60 ultra used with large system text and browser zoom. Navigation remains horizontally compact where space permits and switches to a stable 2×2 grid at the narrowest effective viewport, preventing active-item scrolling and left-edge clipping while preserving large touch targets.

## App-version identity checkpoint

The home page now states that the product is maintained as two distinct Android app variants:

- `EchoSweep` — stable;
- `EchoSweep Dev` — development and testing.

The public wording deliberately does not claim current availability, exact version numbers, specific Google Play tracks, rollout state, or installed-artifact identity. Those values may change independently and require separate release evidence.

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
- privacy contact remains `privacy@adz-dev-coding.pl`;
- support contact is `support@echosweep.pl`;
- the publisher name is consistently `Adz Dev Coding`;
- the home page names `EchoSweep` and `EchoSweep Dev` as separate app variants;
- responsive rules cover phone, tablet, desktop, large-text, and zoom-sensitive layouts;
- keyboard-visible focus styles and skip links are present;
- reduced-motion preference is respected;
- decorative images use empty alternative text;
- semantic navigation, main content, sections, lists, and footer are used.

## External-resource audit

The pages automatically load only repository-hosted HTML, CSS, and SVG assets. External hyperlinks may be followed by the user, but the site does not automatically load third-party resources.

## Privacy-content boundary

The public text was reviewed against the documented EchoSweep product boundary and relevant Android source before publication preparation. Claims about universal runtime safety, exact release behavior, final Google Play Data safety answers, legal compliance, and successful publication are excluded or qualified.

## Not established by static source validation

- current GitHub Pages deployment completion for the latest commit;
- cross-network cache propagation;
- rendered-browser and assistive-technology testing across all devices, font scales, and zoom levels;
- professional legal review;
- behavior of the exact production Android artifact;
- current Google Play track or rollout state;
- Google Play acceptance.

## Publication maintenance gate

After a website change is merged:

1. wait for GitHub Pages to deploy the resulting `main` commit;
2. open and reread the affected live pages;
3. check large-text and zoom behavior on the operator device where relevant;
4. reconcile privacy and release wording with the exact Android release artifact and final Google Play declarations before irreversible submission.
