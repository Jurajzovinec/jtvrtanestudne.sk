# VRTANE STUDNE


### SEO

This document outlines the technical SEO implementation for the JT Vŕtanie studní website.

#### Meta Tags

**Basic Meta Tags:**
- `charset`: UTF-8
- `viewport`: Responsive design with `user-scalable=no`
- `description`: Business description with key services and contact info (Slovak language)
- `keywords`: Targeted keywords for local search (vŕtanie studní, Žilina, geologický prieskum, etc.)
- `lang="sk"`: Document language set to Slovak

**Geo Meta Tags (Local SEO):**
- `geo.region`: SK-ZI (Žilina region)
- `geo.placename`: Žilina
- `geo.position`: 49.2231, 18.7397 (GPS coordinates)
- `ICBM`: 49.2231, 18.7397

#### Open Graph (Social Media)

- `og:type`: website
- `og:url`: https://jt-vrtanestudne.sk/
- `og:title`: Business name with service description
- `og:description`: Short description with pricing and contact
- `og:locale`: sk_SK

#### Canonical URL

- Canonical URL set to: `https://jt-vrtanestudne.sk/`
- Prevents duplicate content issues

#### Favicons

- 32x32 PNG
- 16x16 PNG
- 180x180 Apple Touch Icon

#### Structured Data (Schema.org)

Implements `LocalBusiness` schema with:
- Business name and alternate names (including diacritic variations)
- Description of services
- URL and telephone numbers
- Price range (Od 70€/m)
- Postal address (Žilina, Žilinský kraj, SK)
- Service area as GeoCircle with coordinates
- Opening hours (Mo-Su)
- Offer catalog with services:
  - Vŕtanie studní (well drilling)
  - Geologický prieskum (geological survey)
  - Drenážne vrty (drainage wells)

#### Robots.txt

Located at `/robots.txt`:
- Allows all search engines (`User-agent: *`)
- Allows crawling entire site (`Allow: /`)
- References sitemap location
- Crawl-delay: 1 second (prevents server overload)

#### Sitemap.xml

Located at `/sitemap.xml`:
- Homepage: priority 1.0
- Services section (#sluzby): priority 0.8
- Gallery section (#galeria): priority 0.6
- All URLs use HTTPS and include lastmod dates
- changefreq set to monthly

#### Content SEO

- Semantic HTML structure with `<header>`, `<main>`, `<article>`, `<footer>`
- H1: Main heading with primary keyword (Vŕtanie studní Žilina)
- H2/H3: Properly structured subheadings
- Alt text on images describing the content and including keywords
- Contact information in `<address>` element
- Clickable phone links (`tel:+421...`)

#### Keyword Strategy

Primary keywords (Slovak with diacritics and without):
- vŕtanie studní / vrtanie studien
- Žilina / Zilina
- geologický prieskum
- studne

Secondary keywords:
- drenážne vrty
- vŕtanie na kľúč
- vrtacky praca
- well drilling

#### Technical Notes

- Single-page application (SPA) with anchor navigation
- CSS-based responsive design
- Minimal JavaScript dependencies (jQuery)
- No vertical scrolling requirement at standard viewport heights

