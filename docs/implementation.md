# Implementation Plan — Beta Website

**Target:** `beta.kwalietijd.nl`
**Stack:** Astro 7, Tailwind CSS v4, TypeScript, static generation
**Language:** Dutch

---

## Phase 1: Foundation

> Theme tokens, fonts, layout, static assets

- [x] Add brand colors as Tailwind v4 `@theme` tokens in `src/styles/global.css`
- [x] Add Montserrat font (Google Fonts, weights 400/500/600/700/800)
- [x] Set body font-family, background (cream), text color (charcoal)
- [x] Add `html { scroll-behavior: smooth; }`
- [x] Update `src/layouts/Layout.astro`: lang="nl", title, meta description, OG tags
- [x] Copy logos to `public/logo/`
- [x] Copy headshot to `public/photos/`
- [x] Verify: dev server runs, cream background, Montserrat renders

## Phase 2: Navigation

> Sticky nav with logo, anchor links, hamburger menu

- [x] Create `src/components/Navigation.astro`
- [x] Small logo linked to #hero
- [x] Anchor links: Werkwijze, Over mij, Ervaring, Contact
- [x] Mobile hamburger toggle (minimal JS)
- [x] Style: cream bg, deep slate text, terracotta hover
- [x] Verify: links scroll, hamburger works on mobile

## Phase 3: Hero Section

> Side-by-side hero with headline, intro, CTA, headshot

- [x] Create `src/components/Hero.astro`
- [x] Two-column layout (desktop), stacked (mobile)
- [x] H1: "Ruimte voor mens én werk."
- [x] Intro paragraph from content.md
- [x] CTA buttons: "Kennismaken" (primary), "Neem contact op" (secondary)
- [x] Headshot image, generous whitespace
- [x] Verify: responsive stacking, buttons link to #contact

## Phase 4: Content Sections

> All content sections with alternating backgrounds

- [x] Create `src/components/Intro.astro` — id="intro", white bg
- [x] Create `src/components/Services.astro` — id="diensten", cream bg
- [x] Create `src/components/Approach.astro` — id="werkwijze", white bg
- [x] Create `src/components/About.astro` — id="over-mij", cream bg
- [x] Create `src/components/Experience.astro` — id="ervaring", white bg
- [x] Create `src/components/Education.astro` — id="opleiding", cream bg
- [x] Verify: all text matches content.md, IDs work with anchors

## Phase 5: Contact & Footer

> Final sections

- [x] Create `src/components/Contact.astro` — id="contact", deep slate bg
- [x] Create `src/components/Footer.astro` — full logo, copyright, charcoal bg
- [x] Verify: contact section visually distinct, footer clean

## Phase 6: Page Assembly

> Wire everything together, clean up

- [x] Update `src/pages/index.astro` — import and render all components
- [x] Delete `src/components/Welcome.astro`
- [x] Delete `src/assets/astro.svg` and `src/assets/background.svg`
- [x] Verify: full page renders, no errors

## Phase 7: Responsive Design & Polish

> Test and refine across breakpoints

- [x] Test at 375px, 768px, 1024px+
- [x] Verify hero stacking, nav hamburger, text readability
- [x] Check font scaling, spacing, no horizontal overflow
- [x] Fine-tune line-heights, letter-spacing, padding

## Phase 8: Accessibility & SEO Audit

> Ensure accessibility and search-engine friendliness

- [x] Semantic HTML: nav, main, section, header, footer
- [x] Image alt text on all images
- [x] Color contrast: adjusted terracotta to #A85035 for WCAG AA compliance
- [x] Keyboard navigation: tab through all interactive elements
- [x] Meta tags: title, description, OG tags
- [x] Custom favicon from logo

## Phase 9: Build & Deploy Verification

> Confirm production build works

- [x] `npm run build` — static output in dist/
- [ ] `npm run preview` — test built site (manual step)
- [x] Verify all images, logos, fonts load
- [x] Check page size and performance

---

## Notes

- Terracotta color adjusted from `#C36A4B` to `#A85035` for WCAG AA contrast compliance
- Contact section placeholder links need real phone, email, and LinkedIn URLs
- Favicon is a simplified version of the scale icon
