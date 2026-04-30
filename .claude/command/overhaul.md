# Website Overhaul — JT Vŕtanie studní

You are a **senior frontend engineer** with deep expertise in HTML, CSS, and responsive web design. You do **not** take shortcuts. Every section gets proper attention. Every pixel matters. You write production-quality code.

## Objective

Completely rebuild `index.html` using the **Spectral template** from `NEW-TEMPLATE/` as the structural and styling foundation, populated with real business content from `texts.md` and `.claude/materials/base-info.md`, and all gallery images from `assets/galery/`.

---

## Step 0 — Prepare Assets

1. Copy all template assets into the project root so paths work from `index.html`:
   - Copy `NEW-TEMPLATE/assets/css/` → `assets/css/` (overwrite if exists)
   - Copy `NEW-TEMPLATE/assets/js/` → `assets/js/` (overwrite if exists)
   - Copy `NEW-TEMPLATE/assets/webfonts/` → `assets/webfonts/`
2. Keep existing project assets intact:
   - `assets/galery/` — 5 gallery images (stroj.jpg, rura.jpg, vrtacia-hlavica-1.jpg, vrtacia-hlavica-2.jpg, well.jpg)
   - `assets/images/` — bg.jpg, overlay.png, pic01.jpg
   - `favicon-16x16.png`, `favicon-32x32.png`, `apple-touch-icon.png`
   - `.claude/materials/logo-rectangle.png` (company logo)

## Step 1 — Build index.html

Use `NEW-TEMPLATE/index.html` as the **exact structural skeleton**. Replace ALL placeholder content with real business content. The template's CSS classes, JS, and HTML structure must remain intact. Do NOT reinvent the wheel — use the template's built-in components (spotlights, features grid, banner, CTA, footer).

### Head Section
- Keep the Spectral template's `<head>` structure
- Update `<title>` to: `Vŕtanie studní Žilina | JT - Profesionálne vŕtanie studien`
- Add all SEO meta tags from the current `index.html`:
  - `<meta charset="utf-8">`, viewport meta
  - `<meta name="description">` with Slovak business description
  - Open Graph tags (og:type, og:url, og:title, og:description, og:locale)
  - Geo meta tags (geo.region, geo.placename, geo.position, ICBM)
  - Canonical URL: `https://jt-vrtanestudne.sk/`
  - Favicon links (`/favicon-32x32.png`, `/favicon-16x16.png`, `/apple-touch-icon.png`)
- Copy the full JSON-LD structured data block from the current `index.html` (LocalBusiness schema)
- Template CSS/JS paths must reference `assets/css/` and `assets/js/` (root-relative)

### Header / Navigation
- Brand name: `JT Vŕtanie studní` (or use the logo image from `.claude/materials/logo-rectangle.png`)
- Navigation menu links (anchor links to page sections):
  - Služby → `#services`
  - Postup → `#process`
  - Galéria → `#gallery`
  - Cenník → `#pricing`
  - Kontakt → `#contact`

### Banner (Hero)
- Use the `#banner` section from the template
- Heading: `JT Vŕtanie studní`
- Subheading (from texts.md intro): `Robíme vŕtané studne pre rodinné domy, chaty aj pozemky bez pripojenia na vodovod.`
- CTA button: `Kontaktujte nás` → links to `#contact`
- Keep the scroll-down arrow linking to first content section
- Use `assets/galery/stroj.jpg` as the banner background image (set via CSS or inline style on the banner section)

### Section: "Ako funguje vŕtaná studňa" (#how-it-works)
- Use template's `wrapper style1 special` pattern (the "One" section with icons)
- Heading from texts.md: `Ako funguje vŕtaná studňa`
- Body text: the explanation paragraph from texts.md about how drilled wells work
- Use 3 relevant FontAwesome icons (e.g., `fa-water`, `fa-mountain`, `fa-tint`) styled as `icons major`

### Section: Spotlight features (#services)
- Use template's `wrapper alt style2` spotlight pattern (the "Two" section)
- **Spotlight 1**: "Technológie" — use `assets/galery/vrtacia-hlavica-1.jpg` as image
  - Title: `Používané technológie`
  - Text: from texts.md technologies section (rotačné vŕtanie, výplachové vŕtanie, priemery 120–200 mm)
- **Spotlight 2**: "Konštrukcia studne" — use `assets/galery/rura.jpg` as image
  - Title: `Konštrukcia studne`
  - Text: from texts.md (pažnica, filtračná časť, štrkový obsyp, spodné zakončenie)
- **Spotlight 3**: "Výhody vŕtanej studne" — use `assets/galery/vrtacia-hlavica-2.jpg` as image
  - Title: `Výhody vŕtanej studne`
  - Text: from texts.md (stabilnejší zdroj, hlbšie vrstvy, menšie riziko vysychania)

### Section: Postup realizácie (#process)
- Use template's `wrapper style3 special` features grid pattern (the "Three" section)
- Heading: `Postup realizácie`
- Subtext: `Každý projekt riešime individuálne.`
- Create **5 feature items** (use the `ul.features` pattern with icons):
  1. Icon `fa-search` — **Obhliadka pozemku** — `Zhodnotíme miesto a podmienky pre vrt.`
  2. Icon `fa-drafting-compass` — **Návrh riešenia** — `Určíme vhodnú hĺbku, technológiu a umiestnenie vrtu.`
  3. Icon `fa-cog` — **Vŕtanie** — `Realizujeme vrt podľa geologických podmienok (rotačne alebo výplachovo).`
  4. Icon `fa-tools` — **Osadenie studne** — `Do vrtu sa osadí pažnica a filtračná časť určená pre kontakt s vodou.`
  5. Icon `fa-check-circle` — **Dokončenie** — `Studňa sa prečerpá, vyčistí a pripraví na používanie.`
- Add one more feature:
  6. Icon `fa-water` — **Čo ovplyvňuje množstvo vody** — from texts.md (geologické podložie, hĺbka vrtu, vodonosné vrstvy)

### Section: Galéria (#gallery)
- Create a NEW section using the spotlight or features grid pattern
- Display ALL 5 gallery images in a visually appealing grid:
  - `assets/galery/stroj.jpg` — Vŕtacie zariadenie
  - `assets/galery/rura.jpg` — Studničné rúry
  - `assets/galery/vrtacia-hlavica-1.jpg` — Vŕtacia hlavica
  - `assets/galery/vrtacia-hlavica-2.jpg` — Vŕtacia hlavica detail
  - `assets/galery/well.jpg` — Hotová studňa
- Each image should have a caption/label
- Style this section with `wrapper style1 special` or an appropriate built-in style

### Section: Cenník (#pricing) — CTA Pattern
- Use template's `wrapper style4` CTA pattern
- Heading: `Cenník`
- Text: from texts.md — `Cena závisí od hĺbky vrtu, typu podložia a prístupnosti pozemku.`
- Prominent price: `Orientačne: 60 – 80 € / meter` (also note base-info.md says `od 70Eur/m` — use the texts.md range but note the base)
- Additional info from base-info.md about what's included in the price:
  - Vystrojenie vrtu modrou atestovanou PVC studničnou rúrou
  - Obsyp dunajským štrkom 4/8
  - Utesnenie vrtu bentonitom
  - Zátka na ukončenie rúry vrtu
- CTA buttons:
  - `Kontaktujte nás` → `#contact`
  - `Viac o postupe` → `#process`

### Section: Kontakt (#contact)
- Use template's CTA or custom styled section
- Heading: `Kontakt`
- Text: `Ak máte záujem o studňu, kontaktujte nás. Prídeme sa pozrieť na pozemok a povieme vám, čo je reálne možné.`
- Phone numbers from base-info.md / current index.html structured data: `+421 905 485 627`, `+421 910 191 409`
- Keep the section visually prominent as a final call to action

### Footer
- Keep template footer structure
- Copyright: `© JT Vŕtanie studní`
- Keep `Design: HTML5 UP` credit (required by template license)
- Social icons: remove unused ones, keep phone and email icons only (or use `fa-phone` and `fa-envelope`)
- No fake social media links

### Scripts
- Keep all Spectral template scripts (jQuery, scrollex, scrolly, browser, breakpoints, util, main)
- Paths must point to `assets/js/`

---

## Step 2 — Custom CSS Overrides

Create or add to `assets/css/custom.css` and include it after `main.css` in the HTML:

1. **Banner background**: Set `assets/galery/stroj.jpg` as the banner background with proper cover sizing and overlay
2. **Color scheme**: Adjust to match the business brand (blues/water theme). Override CSS variables or Spectral's `$accent` color to a professional blue tone
3. **Typography**: Ensure Slovak diacritics render correctly. Consider adding a clean sans-serif font (the template already uses a good system font stack)
4. **Logo**: Style the header h1 to optionally show the logo image from `.claude/materials/logo-rectangle.png` alongside/instead of text
5. **Gallery grid**: Style the gallery section images with consistent sizing, hover effects, and captions
6. **Gallery section**: Use the spotlight or a CSS grid to show all 5 images attractively. If using spotlights (3 across), consider a 2+3 or 3+2 layout. All images must have `object-fit: cover` and consistent aspect ratios
7. **Responsive behavior**: Ensure the site works well at all 4 target resolutions (375x667, 768x1024, 1920x1080, 2560x1440). Content must fit without vertical scrolling at each resolution per the CLAUDE.md rules
8. **No vertical scrolling rule**: This is CRITICAL. All content MUST be visible within the viewport at each resolution. This means:
   - On mobile (375x667): You may need to simplify the layout, reduce spacing, use hamburger nav
   - On tablet (768x1024): Balance content density
   - On desktop (1920x1080): Full layout visible
   - On large desktop (2560x1440): Centered content with max-width
   - Consider reducing font sizes, padding, and image sizes on smaller viewports
   - The banner should be compact, not full-viewport-height if that would push content off screen

---

## Step 3 — Quality Checks

1. **All gallery images used**: Verify all 5 images from `assets/galery/` appear in the page
2. **All text content from texts.md**: Verify every section from texts.md has corresponding content on the page
3. **base-info.md details**: Ensure the specific technical details (PVC rúry, štrkový obsyp, bentonit, etc.) are included in the pricing/services sections
4. **SEO preserved**: All meta tags, structured data, and canonical URL must be present
5. **Favicons**: Working and linked correctly
6. **Template integrity**: Spectral's JS interactions (scroll animations, nav menu, parallax effects) must work
7. **No broken images**: All `src` paths must be correct
8. **No placeholder text**: Every piece of "Lorem ipsum" or template placeholder must be replaced with real content
9. **Slovak language**: `lang="sk"` on the html element, all content in Slovak
10. **Responsive**: Test conceptually at all 4 breakpoints
11. **Accessibility**: Images have alt text in Slovak, proper heading hierarchy, semantic HTML

---

## Source Files Reference

| Source | Purpose |
|---|---|
| `NEW-TEMPLATE/index.html` | HTML structure, CSS classes, JS integration pattern |
| `NEW-TEMPLATE/assets/css/main.css` | Core template styles (do not modify, override in custom.css) |
| `NEW-TEMPLATE/assets/css/noscript.css` | Fallback styles |
| `NEW-TEMPLATE/assets/js/*.js` | Template JavaScript (copy as-is) |
| `NEW-TEMPLATE/assets/webfonts/` | FontAwesome icons |
| `texts.md` | ALL text content for the page |
| `.claude/materials/base-info.md` | Additional business details (price, included services) |
| `.claude/materials/logo-rectangle.png` | Company logo |
| `assets/galery/*.jpg` | 5 gallery images (stroj, rura, vrtacia-hlavica-1, vrtacia-hlavica-2, well) |
| `assets/images/bg.jpg` | Background image option |
| Current `index.html` | SEO meta tags, structured data, contact info |

---

## Important Rules

- **Do NOT skip sections** — every piece of content from texts.md must appear
- **Do NOT use placeholder images** — only use images from `assets/galery/` and `assets/images/`
- **Do NOT modify `NEW-TEMPLATE/assets/css/main.css`** — override in a separate custom.css
- **Do NOT remove the HTML5 UP attribution** from the footer
- **Do NOT use any external CDN resources** that aren't already in the template (no Google Fonts unless already there, no external JS libraries)
- **Keep the page as a single `index.html`** — no multi-page setup
- **Preserve all existing SEO** from the current index.html (meta tags, structured data, favicons)
- **The page must be fully static** — no server-side code, no API calls
- **No vertical scrolling** — per `.claude/CLAUDE.md`, all content must fit in viewport at all resolutions
