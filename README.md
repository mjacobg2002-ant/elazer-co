# Elazer Co — Roofing / Siding / Gutters — Homepage Concept

A single-file, high-end homepage **concept/shell** for **Elazer Co**, a roofing, siding, and
gutter contractor that also offers skylight cleaning. Built as a static site — no build step, no
dependencies. Open `index.html` in any browser.

> This is a homepage shell, not the full production website. It is designed to look like the site
> of a serious professional exterior contractor and to make it easy to request an estimate.

---

## What's verified vs. placeholder

Everything on the page is grounded in the details provided by the client. Nothing was invented.

### ✅ Verified (used on the page)
- **Business name:** Elazer Co
- **Phone:** (484) 235-7821
- **Services:** Roofing (install / repair / replace), Siding, Gutters & gutter cleaning, Skylight cleaning
- **Segments:** Residential & commercial
- **Brand color:** green (drawn from the company logo)
- **Logo:** used in the header and footer (`public/images/elazer/logo.png`)

### ⚠️ Deliberately NOT included (unverified — left out on purpose)
Owner/founder name, exact city / service-area towns, business hours, years in business,
license/insurance numbers, certifications, warranties, pricing, "free estimate" claims, specific
response-time guarantees, customer reviews, and social profiles. Add these only once confirmed.
The Service Area section is intentionally generic — add Elazer Co's specific city/towns (see the
`TODO` comment in `index.html`).

### 🖼️ Placeholder imagery
All photos are **local, roofing-matched stock images** committed under `public/images/elazer-photos/`
(flagged in the HTML with `data-placeholder`). They depict relevant exterior work but are **not**
Elazer Co's own projects. **Replace them with authentic company photography** before launch. Siding
and skylight-cleaning photos are not yet represented — add them when available.

---

## Swapping in real assets

### Logo
The real logo is already in `public/images/elazer/logo.png` and used in the header/footer.

### Photos
Real photos go in the prepared folders under `public/images/elazer-photos/`
(`hero/`, `roofing/`, `repairs/`, `projects/`, `team/`, `gallery/`). Overwrite each file in place
with a real Elazer Co photo of the same subject and keep the `alt` text accurate.

To find every image to replace:
```bash
grep -n "data-placeholder" index.html
```

---

## Customizing

- **Colors** — edit the CSS custom properties in `:root` (charcoal base + a single green accent `--accent`).
- **Copy** — all text is inline in `index.html`.
- **Phone number** — search/replace `4842357821` and `(484) 235-7821`.
- **Service area** — fill in the specific city/towns (see the `TODO` comment near the `#area` section).
- **Estimate form** — currently a front-end shell. Wire it to email or a CRM (Formspree, a form
  service, or a backend endpoint) to receive real requests.

---

## Sections

Sticky header → Hero → Trust strip → Problem/intro → Roofing feature → What we do (Roofing / Siding /
Gutters / Skylight Cleaning) → Roof types → Repair feature → Before/After slider → Project gallery →
Craftsmanship → About → Why us → Service area → Contact CTA → Estimate CTA + form → Final CTA →
Footer, plus a mobile bottom action bar.

## Notes on quality
- Responsive from 320px up; mobile bottom action bar (Call / Get Estimate).
- Accessible: semantic landmarks, one `<h1>`, keyboard-operable before/after slider and menu, visible
  focus states, `prefers-reduced-motion` support, descriptive alt text.
- Performance: hero image prioritized, below-the-fold images lazy-loaded, minimal JS, no framework.

---

*Homepage concept. Verify all business details and replace placeholder imagery with authentic Elazer
Co photography before publishing.*
