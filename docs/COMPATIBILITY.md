# EmDash Compatibility

## IntelCloud EmDash 0.36 Standalone Compatibility Set V0

Validated on: 2026-09-10

### Toolchain

- Node.js: 24.18.0 validated
- pnpm: 11.9.0

### Direct dependencies

- emdash: 0.36.0
- @emdash-cms/cloudflare: 0.36.0
- @emdash-cms/plugin-forms: 0.2.6
- @emdash-cms/plugin-webhook-notifier: 0.2.0
- astro: 7.0.0
- @astrojs/cloudflare: 14.0.0
- @astrojs/react: 6.0.0
- react: 19.2.4
- react-dom: 19.2.4
- @astrojs/check: 0.9.10
- @cloudflare/workers-types: 5.20260908.1
- wrangler: 4.130.0

### Cloudflare runtime

- compatibility_date: 2026-02-24
- compatibility_flags: nodejs_compat

### Cloudflare binding

D1 binding: DB
R2 binding: MEDIA
Worker Loader binding: LOADER
Cron: \* \* \* \* \*
Workers KV binding: none

### Validation

- pnpm install --frozen-lockfile
- typecheck
- build
- public runtime
- EmDash Admin
- seed/content
- media
- inline editing
- Table of Contents

### Compatibility adaptations

- category/[slug].astro: removed unsupported `includeCounts`
- tag/[slug].astro: removed unsupported `includeCounts`

### Upgrade rule

Do not upgrade EmDash, Astro, Cloudflare adapter, Wrangler, Node.js,
pnpm or other compatibility-sensitive direct dependencies as part of
unrelated feature work.

Upgrade through a dedicated branch and establish a new compatibility set.
