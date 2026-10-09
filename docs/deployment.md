# Deployment

## Hosting

The website is hosted as a static site on GitHub Pages at:

`https://kwalietijd.github.io/Kwalietijd-web/`

Astro's `base` setting includes the repository path so page assets load correctly on GitHub Pages.

## Deployment flow

The workflow in `.github/workflows/deploy.yml` runs on every push to `main` and can also be started manually from the Actions tab. It checks out the repository, installs dependencies with `npm ci`, builds the Astro site, uploads `dist/` as a Pages artifact, and deploys that artifact to GitHub Pages.

## One-time GitHub setup

In the repository settings, open **Pages** and select **GitHub Actions** as the build and deployment source. No SSH keys or Cloudflare Tunnel secrets are needed.

## Deployment philosophy

Production is static, fast, and rebuilt from source on each deployment. Avoid manual changes to generated production files.

## Future improvements

Potential future additions:

* Custom domain
* Analytics
* Contact form
* Performance monitoring
* Automated accessibility checks
