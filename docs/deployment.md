# Deployment

## Hosting

The website is hosted as a static site on GitHub Pages at:

`https://balansinkwalietijd.nl/`

Astro's `site` and `base` settings are configured for the custom apex domain. A `public/CNAME` file keeps the custom domain attached to each Pages deployment.

## Deployment flow

The workflow in `.github/workflows/deploy.yml` runs on every push to `main` and can also be started manually from the Actions tab. It checks out the repository, installs dependencies with `npm ci`, builds the Astro site, uploads `dist/` as a Pages artifact, and deploys that artifact to GitHub Pages.

## One-time GitHub setup

In the repository settings, open **Pages** and select **GitHub Actions** as the build and deployment source. Set `balansinkwalietijd.nl` as the custom domain. Configure the domain's DNS records with its DNS provider; no SSH keys or Cloudflare Tunnel secrets are needed.

## Deployment philosophy

Production is static, fast, and rebuilt from source on each deployment. Avoid manual changes to generated production files.

## Future improvements

Potential future additions:

* Custom domain
* Analytics
* Contact form
* Performance monitoring
* Automated accessibility checks
