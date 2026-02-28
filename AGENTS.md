# AGENTS.md

## Cursor Cloud specific instructions

This is a static documentation site built with **Astro Starlight**, **Tailwind CSS v4**, and **TypeScript**. There is no backend, database, or Docker dependency.

### Running the dev server

```bash
yarn dev          # starts at http://localhost:4321
yarn dev --host 0.0.0.0  # if you need network access (e.g. from a browser on the VM desktop)
```

See `README.md` for the full command reference (`yarn build`, `yarn preview`, etc.).

### Gotchas

- **Search only works in production builds.** In dev mode the search modal shows "Search is only available in production builds." Use `yarn build && yarn preview` to test search.
- **Missing image warning during build:** The build emits `Image not found - /src/assets/doc-bg.png` on several pages. This is a pre-existing cosmetic issue and does not block the build.
- **Sitemap warning:** `[@astrojs/sitemap] The Sitemap integration requires the 'site' astro.config option. Skipping.` — also pre-existing and non-blocking.
- **No linter configured.** There is no ESLint or Prettier setup in this repo. `yarn build` (which runs `astro build`) is the primary correctness check.
