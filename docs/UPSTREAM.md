# EmDash Upstream

## Source acquisition

Generated with:

pnpm create emdash .

CLI produced a template referencing EmDash 0.37.0.

IntelCloud subsequently established EmDash 0.36.0 as the
validated compatibility baseline because the 0.37.0 artifact
was not usable on the Windows development environment at the
time of validation.

Selected:

- Deployment: Cloudflare Workers
- Template: Blog
- Package manager: pnpm
- Install dependencies: No

Generated date: 2026-09-10

## Important provenance note

The generated Blog template initially referenced:

- emdash: ^0.37.0
- @emdash-cms/cloudflare: ^0.37.0

Therefore this repository is not treated as a byte-for-byte historical
EmDash 0.36 Blog template.

IntelCloud intentionally established EmDash 0.36.0 as the compatibility
baseline and applied the minimum source adaptations required for that API.

## IntelCloud compatibility adaptations

1. emdash changed to exact 0.36.0.
2. @emdash-cms/cloudflare changed to exact 0.36.0.
3. Removed unsupported `includeCounts: false` from:
   - src/pages/category/[slug].astro
   - src/pages/tag/[slug].astro

No framework refactor was performed as part of these adaptations.
