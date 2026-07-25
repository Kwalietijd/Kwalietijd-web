# Deployment

## Hosting

The website is hosted on a Raspberry Pi.

Nginx serves the generated static files.

Cloudflare Tunnel provides secure public access.

## Deployment flow

```
Git push
    ↓
GitHub
    ↓
Webhook
    ↓
Raspberry Pi
    ↓
Build project
    ↓
Copy generated files
    ↓
Nginx serves updated site
```

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

* Automated deployments
* Preview deployments
* Analytics
* Contact form
* Performance monitoring
* Automated accessibility checks
