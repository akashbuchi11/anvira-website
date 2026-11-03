# Anvira website: static build

Open `index.html` in a browser, or upload this whole folder to any static host
(Netlify, Vercel, Cloudflare Pages, S3 + CloudFront, cPanel). There's no build step.
Keep the `assets` folder next to `index.html`.

## Editing content
Everything that changes lives in the `SITE` config block near the bottom of `index.html`:
- `legalName`: the line under the ANVIRA logo, the footer and the page title
- `salesEmail` / `salesPhone`: shown as "to be confirmed" while `null`
- `inquiryEndpoint`: where the enquiry form POSTs JSON. While `null`, the form prepares a copyable enquiry and says plainly that nothing was sent
- `showDraftNotice`: the "Preview" bar at the top. Set it to `false` at launch
- `commodities`: names, descriptions, typical buyers, spec lists and images. Set `enabled: false` to hide a product (this also updates the scrolling commodity strip)

## Before launch
1. Confirm the registered name: **Agri** (logo, card, invoices) or **Agro**. Update `legalName` and, if needed, commission a corrected logo.
2. Confirm an official sales email and a company phone line (not a personal mobile). Don't publish a street address until it's confirmed as an office.
3. Approve the product list. Maize is deliberately not listed.
4. Connect `inquiryEndpoint` to a company-owned form service, and add a privacy notice.
5. Don't add client names, logos, testimonials, GSTIN, LLPIN or certifications until each is verified and approved.

## Images
The photos are cropped from the approved mockup and upscaled 4x. They work well at the current sizes.
For launch, replace them with original high-resolution photos at the same file names and aspect ratios:
- product cards: about 2:1
- `hero-collage.webp`: the opening collage. It's a transparent WebP, so the gaps between photos show the page colour. Replace it with a new transparent PNG or WebP of the same shape
- About banner: about 2.8:1
