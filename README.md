# skylerbradley.dev

Static portfolio and technical notes site for Skyler Bradley. Built with Astro and deployed through GitHub Pages at `skylerbradley.dev`.

Pushes to `main` automatically build and deploy through `.github/workflows/deploy-pages.yml`.

## Local development

```bash
npm install
npm run dev
```

## Production build

```bash
npm run build
```

The deployable site is written to `dist/`.

## Hostinger deployment

1. Run `npm run build`.
2. In Hostinger File Manager, open the domain's `public_html` directory.
3. Preserve or download any existing files needed for rollback.
4. Remove the current parked-site files from `public_html`.
5. Upload the **contents** of `dist/`, not the `dist` directory itself.
6. Confirm these routes:
   - `/`
   - `/projects/secure-homelab/`
   - `/notes/`
   - `/sitemap-index.xml`
7. Confirm HTTPS is enabled and the domain redirects HTTP to HTTPS.

The generated site intentionally contains no `noindex` directive. `robots.txt` permits indexing after launch.

## Content model

- `src/pages/projects/` contains long-form case studies.
- `src/pages/notes/` contains durable technical articles.
- `src/styles/global.css` owns the design system and responsive rules.
- `public/images/` contains public-safe screenshots only.

## Before public launch

- Public contact email: `skylerbradley1@gmail.com`.
- LinkedIn uses the canonical public profile URL without mobile sharing parameters.
- Add a résumé only when a current public version is available.
- Never publish homelab addresses, hostnames, account names, service URLs, or exact security rules.
- Keep private projects, licensed assets, internal architecture, and sensitive infrastructure details out of the public repository.

## Publishing notes

Notes are intentionally infrequent. A post should demonstrate an original decision, experiment, failure, or result. Tutorial rewrites and posting for cadence alone do not belong here.
