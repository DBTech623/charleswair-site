# charleswair.com

Author site for Charles Wair / *Autonomous* (Malcolm Carter, Book One). Static HTML/CSS, hosted on GitHub Pages.

## Structure

- `index.html` — the whole site (single page: Home / Autonomous / About / Join the List)
- `styles.css` — styling; reuses the book's own Inter + IBM Plex Mono type system and the cover's dossier-placard motif
- `images/autonomous-cover.png` — front cover art
- `CNAME` — custom domain for GitHub Pages (charleswair.com)

## Still needed before this is fully live

1. ~~Buy the domain~~ — done, `charleswair.com` is registered (Cloudflare Registrar). Point its DNS at GitHub Pages:
   - Apex (`charleswair.com`): four `A` records to `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153` (optionally `AAAA` records too, to `2606:50c0:8000::153`, `2606:50c0:8001::153`, `2606:50c0:8002::153`, `2606:50c0:8003::153`)
   - `www`: a `CNAME` record to `dbtech623.github.io`
   - If DNS is on Cloudflare, set these records to **DNS only** (grey cloud, not proxied) until GitHub finishes issuing the HTTPS certificate — switch to proxied afterward if desired.
   - GitHub's current instructions: https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site
2. **Set up MailerLite** (free tier, up to 1,000 subscribers) and replace the placeholder form in `index.html`'s `#signup-form` with MailerLite's real embed code/action URL.
3. **Replace the "Coming Soon" Amazon button** in `index.html` with the real product link once the book is live, and remove `aria-disabled`.
4. **Replace the About section bio** with your own words — the current copy is a placeholder.

## Local preview

Just open `index.html` in a browser — no build step.
