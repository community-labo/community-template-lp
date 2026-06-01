# CLAUDE.md

This repository is a static landing page site for AIサロン. Use this file as the project-level working guide for Claude or other coding agents.

## Project Shape

- `index.html` is the top page.
- `contact.html`, `privacy.html`, `terms.html`, and `tokushoho.html` are lower-level legal/contact pages.
- `assets/` contains shared images.
- `scripts/fetch-peatix-dates.mjs` syncs event dates from Peatix.
- `.claude/skills/sync-peatix/SKILL.md` documents the Peatix date sync workflow.

## Editing Rules

- Keep the site as plain static HTML unless the user explicitly asks for a larger restructure.
- Prefer small, page-local edits. Do not introduce a build step for ordinary copy, layout, or link changes.
- Preserve existing Japanese copy style and brand terms such as `AIサロン`.
- Keep shared visible elements consistent across all pages, especially header, CTA links, footer links, copyright text, and legal page names.
- When adding a new lower-level page, copy the current lower-level header/footer structure and adjust only page-specific content.
- Keep assets in `assets/` with descriptive kebab-case English filenames.

## Footer Standard

Use the top page footer as the canonical footer:

- Logo text: `AIサロン`
- Catch copy: `AIを学び、活用し、仕事と暮らしをアップデートする。`
- Links:
  - `tokushoho.html`: `特定商取引法に基づく表記`
  - `privacy.html`: `プライバシーポリシー`
  - `terms.html`: `利用規約`
  - `mailto:info@ai-salon.jp`: `お問い合わせ`
- Copyright: `© 2026 AIサロン All Rights Reserved.`

On lower-level pages, the footer logo should link to `index.html#top`. On `index.html`, it should link to `#top`.

## Mobile CTA

The top page has a mobile-only floating CTA:

- Selector: `.sp-floating-cta`
- Display breakpoint: `max-width: 599px`
- Body bottom padding should exist only while the CTA is visible.
- Hide the CTA before it overlaps the footer, and remove the extra bottom padding at the same time.

## Common Values

- Service name: `AIサロン`
- Monthly price: `2,980円`
- Join CTA URL: `https://stripe.com/en-jp`
- Contact email: `info@ai-salon.jp`

## Verification

For simple HTML/CSS edits, inspect the changed files and run:

```bash
git diff --stat
```

For Peatix date changes, run:

```bash
npm run sync-peatix:dry
```

Only run the full Peatix sync when the user wants the LP date content updated.
