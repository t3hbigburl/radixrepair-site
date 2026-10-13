# Radix Industries — GitHub repository business website

Static business website files for **radixrepair.com**. Design based on the Radix WordPress theme, with the same brand, mobile navigation, service imagery, gallery, and quote intake. Built with HTML, CSS and JavaScript; no WordPress, database, or build process required. Commercial website hosting should use Cloudflare Pages or another suitable provider.

## Preview locally

Open `index.html` in a modern browser (or serve the folder locally using `python -m http.server 8000`). Explore the Services, Example Work, Coverage, About, Quote, Contact and Privacy pages. **Do not submit the quote form while previewing** unless you intend to send a real request.

## Recommended publishing: GitHub repository + Cloudflare Pages

**Important:** GitHub Pages is not intended/allowed as free hosting for sites used to run an online business or sites primarily facilitating commercial transactions. Because Radix Industries is a commercial services website with a quote form, use GitHub for source control and deploy through a hosting service that permits commercial websites, such as Cloudflare Pages. This changes **nothing** about the site design.

1. Create a GitHub repository named `radixrepair-site` and upload **the contents** of this ZIP to the repository root. The repository must have `index.html` at the top level.
2. Create a Cloudflare account, visit **Workers & Pages → Create application → Pages → Import existing Git repository**, and connect the repository.
3. Select branch **main**. For a plain static site: no framework preset; build command `exit 0` (or none if allowed), output directory `.` (repository root).
4. Deploy. Cloudflare creates a temporary `*.pages.dev` URL for previewing and automatically publishes updates when you push changes to GitHub.
5. To use **radixrepair.com**, open **Pages project → Custom domains → Set up a domain**, and follow Cloudflare's ownership/DNS instructions. For the domain apex `radixrepair.com` you must use a Cloudflare DNS zone and Cloudflare nameservers. Do not change DNS prematurely; first establish the Pages deployment.
6. Once the domain is active, confirm HTTPS, navigation, and the quote form activation.

Cloudflare docs: https://developers.cloudflare.com/pages/framework-guides/deploy-anything/
Custom domain docs: https://developers.cloudflare.com/pages/configuration/custom-domains/
GitHub Pages business-usage restrictions: https://docs.github.com/en/pages/getting-started-with-github-pages/github-pages-limits

You can still keep **everything in GitHub** as desired. GitHub remains the source-of-truth repository, with hosting handled by Cloudflare Pages. The GitHub connector in ChatGPT, if connected, can help manage the repository.

## Quote form — IMPORTANT FIRST-TIME SETUP

The public site submits to `https://formsubmit.co/radixrepair@gmail.com`. FormSubmit delivers the submitted data to that mailbox (a third-party service). **It must be activated/verified** the first time it is used. After publishing, make a test submission, find the FormSubmit verification email in **radixrepair@gmail.com**, follow its activation link, then submit a second test to verify delivery. Check spam/junk if needed. The button does **not** claim an email was delivered before FormSubmit confirms it.

The quote includes service, customer name, phone, email, call-back time, location, timing, emergency status and description. Urgent status prompts customers to call. Submitting is not a contract or an appointment. The site and repository do **not** store submission details. Do not put API keys, passwords or customer records in a public repository.

For a more advanced ticket workflow, replace FormSubmit later with a secure back-end endpoint; GitHub Pages cannot host PHP/WordPress or your self-hosted ticketing database.

## Customization

- Contact details live in each HTML page; current number: **814-590-8882**, email: **radixrepair@gmail.com**.
- Images in `assets/` are AI-generated **illustrative marketing concept scenes** (except original Radix logo). They must not be presented as documentary proof of completed work; replace with real customer photographs later when available.
- The service area map is a schematic, not an accurate drive-time boundary or precise 100-mile radius.
- `assets/css/site.css` holds all styles. `assets/js/site.js` handles mobile menu, gallery, form validation & urgent-call guidance.
- The site uses relative links, so it previews locally and on your Cloudflare Pages preview URL before custom domain activation.
- Review the sample privacy page for accuracy before publishing.

## What is **not** included

WordPress admin, PHP, email server, database, payment processing, remote monitoring, or ticket management. Those require a separate backend/hosting solution.
