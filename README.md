# Free Gift Studio website

This repository is the shared GitHub Pages root for Free Gift Studio:

- Repository: <https://github.com/Isthatok74/isthatok74.github.io>
- Live site: <https://freegiftstudio.ca>

It owns the developer landing page, the `freegiftstudio.ca` custom-domain
configuration, and root-level files shared by the studio's projects. Individual
project websites may be maintained in separate repositories and published below
this domain, such as <https://freegiftstudio.ca/paper-volleyball/>.

## Shared root files

The source copies of root-level static files live in `public/` so Vite includes
them unchanged in `docs/` during a production build.

- `public/CNAME` assigns the GitHub Pages site to `freegiftstudio.ca`.
- `public/app-ads.txt` is the single authorized-sellers file shared by every app
  whose store listing uses this developer domain.

Update `public/app-ads.txt` when an app needs another authorized seller or AdMob
publisher account. Do not place app-specific copies at project paths such as
`/paper-volleyball/app-ads.txt`; app-store crawlers resolve the file from the
developer website's domain root.

## Local development and publishing

Install dependencies and run the development server:

```bash
npm install
npm run dev
```

Build the production site:

```bash
npm run build
```

The Vite build writes the deployable site to `docs/`. GitHub Pages publishes
that directory from this repository. Commit the source changes and regenerated
`docs/` output together when publishing an update.

Project repositories are responsible for their own source and project-page
deployment. They should link back to this repository when documenting ownership
of the shared domain, `CNAME`, or `app-ads.txt`.
