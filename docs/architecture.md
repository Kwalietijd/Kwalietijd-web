# Architecture

## High-level architecture

```
GitHub Repository
        │
        ├── Local development (Mac)
        ├── AI coding agent (Docker Sandbox)
        └── Raspberry Pi deployment
```

The Git repository is the source of truth.

## Development

Local development:

* Node.js 22+
* Astro
* Tailwind CSS
* TypeScript

The AI coding agent runs inside Docker sandboxes. Those sandboxes are considered disposable and should not require any machine-specific configuration.

The project itself should define everything required to build it.

## Production

Infrastructure:

```
Internet
    │
Cloudflare
    │
Cloudflare Tunnel
    │
Nginx
    │
Static files
```

No Node.js application is expected to run in production for the website itself.
