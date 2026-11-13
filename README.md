# Luisa Orozco webpage

This site uses Hugo and the `hugo-profile` theme.

## Preview locally

Install Hugo Extended (on macOS, `brew install hugo`). From the repository root, run:

```sh
hugo server
```

Open the address Hugo prints, usually <http://localhost:1313/>. The preview updates when you edit the site.

## Build locally

To make the same production build used in CI, run:

```sh
HUGO_ENV=production hugo --minify
```

Hugo writes the generated site to `public/`. You do not need to upload this directory yourself.

## Deployment

GitHub Actions builds and deploys the site through [the deploy workflow](.github/workflows/deploy.yml). Pull requests run the build without deploying. A push to `main` builds the site and publishes `public/` to the `gh-pages` branch for GitHub Pages. You can also run the workflow manually; it deploys when run on `main`.
