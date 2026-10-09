# Kwalietijd Website

Professional one-page website for **Kwalietijd**, the independent practice of a bedrijfsmaatschappelijk werker.

## Quick Start

### Prerequisites

- Git
- mise

### Installation

```bash
git clone <repository>

cd Kwalietijd-web

mise install

npm install

npm run dev
```

The development server will be available at:

http://localhost:4321

## Purpose

This website is intended to establish trust and professionalism for potential clients. It should communicate experience, reliability, and approachability without feeling overly commercial.

The primary audience consists of:

* HR professionals
* Managers
* Employers
* Organizations looking for bedrijfsmaatschappelijk werk
* People referred through existing professional networks

The website is intentionally simple and focused on quality over quantity.

## Goals

* Build trust within the first few seconds
* Clearly explain the services offered
* Present professional experience and qualifications
* Make it easy to get in touch
* Load quickly on all devices
* Be accessible and easy to maintain
* Remain mostly static with minimal operational complexity

## Non-goals

This project is **not** intended to become:

* A large marketing website
* A CMS
* A blog platform (unless added later)
* An authenticated web application

## Technology

Current planned stack:

* Astro
* TypeScript
* Tailwind CSS
* Static site generation
* GitHub Pages

## Repository structure

```text
assets/        Raw design assets (logos, original photos)
docs/          Project documentation
public/        Static assets served by Astro
src/           Astro source code
```

## Development principles

* Keep dependencies minimal.
* Prefer static generation over server-side rendering.
* Prioritize accessibility.
* Mobile-first design.
* Focus on readability and trust.
* Keep JavaScript to a minimum.

## Deployment

Development happens locally.

Production is hosted on GitHub Pages.

Every push to `main` builds and deploys the site through GitHub Actions. The deployment process is documented in `docs/deployment.md`.

## Future ideas

* Testimonials
* Contact form
* Privacy policy
* Blog/articles
* English version (if ever needed)
