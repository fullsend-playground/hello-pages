# hello-pages

Static web pages for [fullsend-playground](https://github.com/fullsend-playground), published to GitHub Pages.

## What's in this repo

| Path | Purpose |
| --- | --- |
| `index.html` | Site landing page |
| `pages/` | Additional HTML pages (add new routes here) |
| `assets/css/` | Shared stylesheets |
| `assets/js/` | Shared client-side scripts |
| `.github/workflows/` | CI/CD, including GitHub Pages deployment |

The project uses [Vite](https://vite.dev/) as a lightweight dev server with live reload and as the production build tool. Source files are plain HTML, CSS, and JavaScript — no framework required — so the repo stays easy to extend.

## Development

### Prerequisites

- [Node.js](https://nodejs.org/) 20 or newer
- npm (bundled with Node.js)

### Run the dev server

```bash
npm install
npm run dev
```

The dev server starts at [http://localhost:3000](http://localhost:3000) with live reload. Edit HTML, CSS, or JS and the browser refreshes automatically.

To preview the production build locally:

```bash
npm run build
npm run preview
```

The preview server runs on port `3001`.

## Adding a new page

1. Create an HTML file under `pages/`, for example `pages/about.html`.
2. Link shared assets with absolute paths (`/assets/css/site.css`).
3. Register the page in `vite.config.js` under `build.rollupOptions.input` so it is included in the build.
4. Run `npm run dev` and open `/pages/about.html`.

## Deployment

Pushes to `main` trigger the **Deploy GitHub Pages** workflow, which builds the site and publishes the `dist/` output to GitHub Pages.

After the first successful deploy, the site is available at:

`https://fullsend-playground.github.io/hello-pages/`

## License

Apache License 2.0 — see [LICENSE](LICENSE).
