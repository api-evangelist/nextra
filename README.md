# Nextra

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
