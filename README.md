# TR Scroll Toggle Landing Page (Vue 2 + GSAP)

This project recreates the landing page and scroll-toggle interaction from **https://tr-scroll-toggle.webflow.io/** using **Vue 2 (Options API)**, **SASS (SCSS)**, and **GSAP** (ScrollTrigger).


## Section mapping
- Section 1: Scroll toggle (plan / design / build) with pinned visuals and counters
- Section 2: Photo zoom on scroll
- Etc: Thank you section

## Tech Stack
- Vue 2 (Options API) — Vue CLI project
- SASS / SCSS (no Tailwind)
- GSAP + ScrollTrigger (pinned section + scroll-bound animations)
- (Bonus) GSAP ScrollToPlugin for header checkpoint scrolling
- (Bonus) Lenis smooth scroll integrated with ScrollTrigger

## Folder Structure
```
src/
├── assets/
│   ├── images/
│   ├── fonts/
│   └── styles/
├── components/
│   ├── header.vue
│   ├── section-1.vue
│   ├── section-2.vue
│   └── etc.vue
├── pages/
│   └── index.vue
```

## System Requirements
- Node.js: **18 LTS** (recommended)
- npm: **9+** (or yarn classic)

## Local Setup
Install dependencies:
```bash
npm install
```

Run development server:
```bash
npm run serve
```

Build for production:
```bash
npm run build
```

Lint:
```bash
npm run lint
```

## Notes
- The main scroll-toggle interaction is implemented in `src/components/section-1.vue` using GSAP ScrollTrigger (pin + step switching).
- Smooth scroll is provided by Lenis and synced with ScrollTrigger in `src/main.js`.
- Images are located in `src/assets/images/` and kept lightweight for faster loading.
- Responsive behavior is implemented with media queries in component SCSS.
- Typography: Header tabs (plan/design/build) uses **Space Grotesk** loaded via Google Fonts (see `public/index.html`).

## Submission Checklist (GitHub)
1. Create a **public** GitHub repository.
2. Push an **initial commit**.
3. Finish the project, then push a **final commit**.
4. Share:
   - GitHub repository link
   - This README (with setup instructions)


## Animation Notes

See `docs/ANIMATIONS.md` for a short explanation of how Section 1 (scroll toggle) and Section 2 (zoom/reveal) are implemented with GSAP + ScrollTrigger, and how Lenis is synchronized.
