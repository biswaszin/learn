# Astro (static site framework)
**Track:** E-Web   **Status:** learning   **Last reviewed:** 2026-09-19

## In one line
A build-time framework for content sites: you write `.astro` components (HTML + a `---` JS fence), Astro compiles them into plain static HTML/CSS, and ships **zero JS by default**.

## Explanation (my words)
> TODO: fill this in after you actually port the site. Don't copy my words.

## How my site maps to Astro
- `index.html`                    → `src/pages/index.astro` (+ `src/layouts/BaseLayout.astro`)
- `css/style.css`                → `src/styles/style.css`, imported in the layout
- `images/`                      → `public/images/` (copied as-is, served at `/images/…`)
                                     **or** `src/assets/` (optimized via `<Image>`)
- navbar / hero / gears markup   → `src/components/*.astro`
- `href="#"` links               → real files: `src/pages/projects.astro` → `/projects`

## Gotchas / edge cases
- `.astro` files can't be opened by double-click — they need `npm run dev` / `npm run build`.
- A component's `<style>` is **scoped** to that component; global CSS must be imported or `is:global`.
- `public/` files are copied verbatim; `src/assets/` files get hashed/optimized by the bundler.
- Static output lands in `dist/`; that's what gets deployed (gitignore it).
- GitHub Pages **project** sites (`user.github.io/repo/`) need `site` + `base` in `astro.config.mjs`, else all absolute asset URLs 404.
- Requires Node toolchain. Adds a build step to a site that currently has none.

## Links
- docs: https://docs.astro.build/en/getting-started/
- official migration guide: https://docs.astro.build/en/guides/migrate-to-astro/
- images: https://docs.astro.build/en/guides/images/
- related: [web-html-css progress](../progress/web-html-css.md)
