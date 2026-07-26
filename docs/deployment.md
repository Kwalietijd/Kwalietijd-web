# Deployment

## Hosting

The website is hosted on a Raspberry Pi.

Nginx serves the generated static files.

Cloudflare Tunnel provides secure public access.

## Deployment flow

```
Git push to main
    ↓
GitHub Actions
    ↓
Build Astro site (Node 22)
    ↓
rsync dist/ to Pi via Cloudflare Tunnel
    ↓
Nginx serves updated site
```

The deployment is automated via `.github/workflows/deploy.yml`.

On every push to `main`, GitHub Actions:
1. Checks out the code
2. Installs `cloudflared` for secure SSH access
3. Builds the Astro site
4. Deploys the `dist/` folder to the Pi via SSH through the Cloudflare Tunnel

## Required GitHub secrets

The following secrets must be configured in the repository settings:

| Secret | Description |
|--------|-------------|
| `SSH_PRIVATE_KEY` | Private key for SSH access to the Pi |
| `SSH_HOST` | hostname for Cloudflare Tunnel SSH access |
| `SSH_USER` | SSH username on the Pi |

## Deployment philosophy

Production should be:

* Static
* Reliable
* Fast
* Easy to recover
* Easy to rebuild from source

Avoid manual changes on the production server whenever possible.

## Future improvements

Potential future additions:

* Preview deployments
* Analytics
* Contact form
* Performance monitoring
* Automated accessibility checks
