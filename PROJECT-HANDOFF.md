# Virgil Digital Project Handoff

Last updated: 22 October 2026

## Project

- Repository: `https://github.com/VIP-oss-bit/virgil-digital.git`
- Local path: `/home/free2b/Downloads/virgil-digital`
- Working branch: `redesign-399`
- Preview: `https://redesign-399.virgil-digital.pages.dev`
- Stack: Astro, static deployment via Cloudflare Pages
- Latest local commit: `5dbc861 Refine mobile menu icon`

Push the latest commit if it is not visible on the preview:

```bash
cd /home/free2b/Downloads/virgil-digital
git push
```

## Business decisions

- Core new-business website offer: **£399**.
- Existing website refresh: **from £499**.
- Website care: **£19/month**.
- Do not describe £399 as a temporary reduction from £499 unless that pricing policy genuinely exists.
- Bristol-based, but service is available UK-wide.
- Positioning: fast, fixed-price, direct contact, no agency handoff.
- Keep Rufus.taxi out of public case studies until there is enough completed work.
- Mealwright and StaySafe Guide are Virgil's own products/projects, not client work.
- Family clients have granted permission to use testimonials and project evidence.

## Completed website work

- Modernised homepage with animated hero/browser preview.
- Project carousel using real project screenshots, including Mealwright.
- Carousel timing is approximately 2.8 seconds with opacity transitions and reduced-motion support.
- Coral calls to action and mint featured-work accents are now visible.
- Added featured work, case-study links, testimonials and guide links.
- Added a compact accessible mobile hamburger icon with `aria-expanded` and dropdown navigation.
- Mobile header hides while scrolling down and returns while scrolling up.
- Improved Virgil Digital wordmark with a custom `V` mark.
- Redesigned footer with CTA, navigation links, contact details and coral top border.
- Build passes with `npm run build`.

## Public pages

`/`, `/about/`, `/services/`, `/work/`, `/work/alterations-by-nicole/`, `/work/marvel-desserts/`, `/work/staysafe-guide/`, `/work/mealwright/`, `/guides/`, `/guides/social-media-vs-website/`, `/guides/what-is-seo/`, `/faq/`, `/process/`, `/contact/`.

The guides explain social media versus owned websites, SEO and search visibility. FAQ and process pages explain scope, timelines, revisions and workflow.

## Evidence and assets

Project assets live in `public/work/`, including desktop/mobile screenshots and portfolio images. Cloudflare Analytics snapshots are written as dated context, not guarantees:

- Alterations by Nicole: 1.79k unique visitors, 22.2k requests
- Marvel Desserts: 873 unique visitors, 12.12k requests
- StaySafe Guide: 3.07k unique visitors, 32.42k requests
- Mealwright: 821 unique visitors, 12.39k requests

Marvel testimonial, attributed to Naz: “Huge thanks to Virgil for his guidance and clear explanations throughout the website project. The service was amazing and the price was fair. I couldn't be happier and would highly recommend him.”

## Known issues

- Carousel needs previous/next controls, keyboard support, clickable indicators and pause-on-hover/focus.
- `src/pages/index.astro` contains duplicate/dead carousel CSS to clean carefully.
- Web3Forms access key is currently client-side; add protected handling, spam controls and rate limiting.
- Privacy policy, terms and analytics/cookie consent review are still needed.
- Check the mobile carousel and footer after the latest deploy.
- Do not publish raw analytics screenshots; use dated written metrics with context.

## Recommended next steps

1. Push `5dbc861`, then check the preview on mobile and desktop.
2. Confirm hamburger behaviour, menu close behaviour, scroll-hide header, footer spacing and carousel readability.
3. Add accessible carousel controls and pause behaviour.
4. Add a clear `/process/` link to the homepage and service/FAQ sections.
5. Add an existing-website-refresh guide covering audit, access, backup, redesign, testing and launch.
6. Add `/privacy/` and `/terms/`; review UK analytics, cookies, contact handling and consent.
7. Harden the contact form with protected handling and rate limiting.
8. Set up Google Search Console and Bing Webmaster Tools; submit `https://virgildigital.co.uk/sitemap.xml`.
9. Complete and verify the Google Business Profile.
10. Create a repeatable manual audit template and research an initial list of about 25 prospects with weak or missing websites.
11. Publish useful guides targeting real business-owner questions; avoid thin location doorway pages.
12. Define customer intake and template-selection before automating Astro generation.
13. Keep generated sites in isolated Git branches with preview deployments and human approval before production.
14. Track API costs, hosting, domains, email, support time, revisions and lead-acquisition cost before changing prices.

## Production launch checklist

Use this order for the first public launch of the redesigned site. Do not submit the sitemap until the live domain shows this version.

- [ ] Confirm the working tree is clean and the latest branch is pushed.
- [ ] Confirm the production branch in Cloudflare Pages; do not merge or change it until identified.
- [ ] Review the homepage on desktop and mobile: navigation, carousel, buttons, images, footer and spacing.
- [ ] Test every public route: About, Services, Work, all case studies, Guides, FAQ, Process, Contact, Privacy and Terms.
- [ ] Send one live contact-form test and confirm delivery to `hello@virgildigital.co.uk`.
- [ ] Check external links, email links, sitemap, canonical URLs and page titles.
- [ ] Merge or deploy `redesign-399` to the confirmed production branch using the existing Cloudflare workflow.
- [ ] Confirm `https://virgildigital.co.uk` serves the redesigned site on desktop and mobile.
- [ ] Confirm `https://virgildigital.co.uk/sitemap.xml` lists the new public pages.
- [ ] Submit `sitemap.xml` in Google Search Console.
- [ ] Request indexing for the homepage and the key `/services/`, `/work/`, `/process/` and `/contact/` pages.
- [ ] Record the launch date and production commit in this document.

## Safe rollback workflow

Work on feature branches, commit small changes and push branches before deployment testing. Use `git log --oneline` to inspect history. Do not reset or delete work without confirming the exact target. Generated `.astro/`, `dist/` and `node_modules/` remain ignored.
