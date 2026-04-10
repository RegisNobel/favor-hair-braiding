# Favor Hair Braiding Static Website

Static marketing website for **Favor Hair Braiding** in **Stone Mountain, GA 30087**, built with plain HTML, CSS, and vanilla JavaScript.

## Current Site Status

The site is set up as a single-page static website with:

- local SEO-focused homepage content
- mobile-friendly navigation
- optimized gallery images
- call, Instagram, TikTok, and Facebook contact actions
- FAQ content
- LocalBusiness JSON-LD structured data
- Cloudflare Pages-friendly file structure

## Project Structure

- `index.html` - homepage markup, SEO metadata, schema, FAQ, and business content
- `styles.css` - mobile-first styling and responsive layout
- `script.js` - sticky header, mobile nav, and reveal-on-scroll behavior
- `assets/` - gallery photos and SVG icons for phone and social buttons

## Run Locally

You can open `index.html` directly, but a local server is better for testing navigation and asset loading.

Example:

```bash
python -m http.server 8000
```

Then open:

```text
http://localhost:8000/favor-hair-braiding/
```

## Deploy With Cloudflare Pages

### Pages Setup

1. Push this repository to GitHub.
2. Log in to Cloudflare and open **Workers & Pages**.
3. Click **Create application**.
4. Choose **Pages**.
5. Connect the GitHub repository.
6. For build settings:
   - **Framework preset**: `None`
   - **Build command**: leave empty
   - **Build output directory**: `favor-hair-braiding`
7. Click **Save and Deploy**.

### Custom Domain And DNS

If you want to use `favorhairbraidsandweaves.com` or another custom domain:

1. Open the deployed Cloudflare Pages project.
2. Go to **Custom domains**.
3. Click **Set up a custom domain**.
4. Enter your domain, for example:
   - `favorhairbraidsandweaves.com`
   - optionally `www.favorhairbraidsandweaves.com`
5. If the domain is already managed in Cloudflare DNS, approve the DNS records Cloudflare suggests.
6. If the domain is managed elsewhere, update DNS at your registrar using the records Cloudflare Pages provides.
7. Wait for SSL provisioning to complete.

Typical DNS setup:

- Apex/root domain:
  - Cloudflare usually provisions the required record automatically when the zone is managed in Cloudflare.
- `www` subdomain:
  - usually a `CNAME` pointing to the Cloudflare Pages hostname

After DNS is connected:

1. Confirm the custom domain shows as active in Cloudflare Pages.
2. Update the canonical URL and Open Graph URL in `index.html` if needed.
3. Test both the root domain and `www` variant.

## Update Business Information

Edit `index.html` to update:

- business name
- phone number
- location
- service wording
- social links
- FAQ content
- footer location and hours

Important areas:

- `<head>` for title, meta description, canonical URL, Open Graph tags, and schema
- `#about` for the top brand/trust section
- `#services` for gallery images and service-related copy
- `#faq` for common booking questions
- `#contact` for phone and social actions

## Update Images

Gallery images live in `assets/`:

- `gallery-1.jpg`
- `gallery-2.jpg`
- `gallery-3.jpg`
- `gallery-4.jpg`
- `gallery-5.jpg`
- `gallery-6.jpg`

If replacing photos:

- keep the same filenames to avoid changing HTML
- use optimized JPG images
- keep portrait orientation where possible for consistent layout
- update alt text in `index.html` when the subject changes

SVG button icons also live in `assets/`:

- `icon-phone.svg`
- `icon-instagram.svg`
- `icon-tiktok.svg`
- `icon-facebook.svg`

## Update SEO Content

SEO content is controlled mainly in `index.html`.

Review and update:

- `<title>`
- `<meta name="description">`
- `<link rel="canonical">`
- Open Graph tags
- JSON-LD structured data
- H1/H2/H3 text
- FAQ content
- image alt text

Current local SEO targeting includes natural phrasing around:

- `hair braiding Stone Mountain GA`
- `knotless braids Stone Mountain`
- `box braids near me`
- `kids braids Stone Mountain`
- nearby areas such as Lithonia, Decatur, Tucker, and Atlanta

## Session Changelog

Below is a summary of the changes made across this working session on **April 9, 2026** in **America/New_York** time.

### 2026-04-09 7:20 PM EDT to 7:45 PM EDT

- Created the initial static site structure in `favor-hair-braiding/`
- Added:
  - `index.html`
  - `styles.css`
  - `script.js`
  - `README.md`
  - initial local gallery assets
- Built the original responsive one-page marketing site

### 2026-04-09 7:45 PM EDT to 8:05 PM EDT

- Reworked layout and section order based on design feedback
- Removed the extra contact card
- Removed the navbar call button
- Combined services and gallery into a single image-led section
- Removed the original hero section when requested
- Simplified footer and contact layout

### 2026-04-09 8:10 PM EDT to 8:16 PM EDT

- Downloaded real gallery images to replace early placeholder artwork
- Added branded social icons and a phone icon for contact buttons
- Updated `gallery-6.jpg` with a kids braided hairstyle image

### 2026-04-09 8:20 PM EDT

- Replaced `gallery-2.jpg` with a kids braided hairstyle image

### 2026-04-09 8:25 PM EDT

- Replaced `gallery-1.jpg` with a corn rows hairstyle image

### 2026-04-09 8:26 PM EDT to 8:31 PM EDT

- Added local SEO improvements
- Added:
  - location-aware title and meta description
  - Open Graph metadata
  - canonical URL
  - LocalBusiness / HairSalon JSON-LD
  - FAQ section
  - stronger phone CTAs
  - service-area language for Stone Mountain, Lithonia, Decatur, Tucker, and Atlanta
- Resized gallery images to improve load performance
- Added lazy loading and async decoding to gallery images
- Updated README for deployment and maintenance guidance

### 2026-04-09 8:31 PM EDT to 8:35 PM EDT

- Removed the hero section again after the SEO refresh
- Removed the “Need an Appointment?” mid-page CTA band
- Removed the footer phone CTA
- Promoted the `Why Choose Us` section to the top with the only H1

### 2026-04-09 8:35 PM EDT to 8:40 PM EDT

- Reduced the visual size of the `Why Choose Us` section
- Removed the service tag/chip list under the gallery
- Updated README to include this full session changelog and Cloudflare Pages + DNS deployment guidance

## Production Notes

- The gallery images have already been resized for faster loading.
- Gallery images use `loading="lazy"` and `decoding="async"`.
- The website is fully static and does not require a build step.
- The current structure is suitable for Cloudflare Pages deployment.
