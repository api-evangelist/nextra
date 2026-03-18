# Nextra

Nextra is an open-source, Next.js-based documentation framework for building fast, modern, and beautifully styled documentation sites. It extends Next.js with MDX support, file-system routing, built-in full-text search powered by Pagefind, syntax highlighting via Rehype Pretty Code, LaTeX rendering (KaTeX or MathJax), static image optimization, internationalization support, and two production-ready themes: a full-featured docs theme and a minimal blog theme.

- **Website:** https://nextra.site
- **GitHub:** https://github.com/shuding/nextra
- **Documentation:** https://nextra.site/docs

## Overview

Nextra is a JavaScript/TypeScript library consumed as an npm package. It is not a hosted service — there are no REST API endpoints, no webhooks, and no streaming event systems. Its programmable surface consists of:

1. **Next.js Plugin Configuration** — the `nextra()` plugin in `next.config.ts` accepts a `NextraConfig` object controlling MDX compilation, search, syntax highlighting, LaTeX, image optimization, and i18n behavior.
2. **File Convention APIs** — `_meta.js` files control sidebar ordering, titles, separators, dropdown menus, and per-page theme overrides.
3. **Server Utilities** — `getPageMap()`, `compileMdx()`, `fetchFilePathsFromGitHub()`, and related exports from the `nextra` package.
4. **Client Components and Hooks** — exported from `nextra/components` and `nextra-theme-docs`, including `useThemeConfig()` and `useConfig()`.

## Artifacts

| File | Type | Description |
|---|---|---|
| `json-schema/nextra-config-schema.json` | JSON Schema | Schema for the `NextraConfig` object passed to the `nextra()` Next.js plugin |
| `json-schema/nextra-theme-docs-config-schema.json` | JSON Schema | Schema for the `<Layout>` component props in `nextra-theme-docs` |
| `json-schema/nextra-meta-schema.json` | JSON Schema | Schema for `_meta.js` / `_meta.global.js` sidebar configuration files |
| `json-ld/nextra-context.jsonld` | JSON-LD Context | Linked data context mapping Nextra entities to schema.org and standard vocabularies |

## Packages

- **`nextra`** — Core plugin providing MDX compilation, page mapping, search, and utilities
- **`nextra-theme-docs`** — Full-featured documentation theme with sidebar, navbar, TOC, dark mode, and i18n
- **`nextra-theme-blog`** — Minimal blog theme with post listing, tags, dates, and RSS feed

## License

MIT — https://github.com/shuding/nextra/blob/main/LICENSE
