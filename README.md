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
2. ~~Set up MailerLite~~ — done. Form `199550384885204355` (group/account `2659458`) is wired into the `#list` section, restyled with the site's own CSS instead of MailerLite's default light theme. Its markup keeps the exact classes/IDs MailerLite's `webforms.min.js` depends on for the success-state toggle (`ml-form-embedContainer`, `.row-form`/`.row-success`, and the `ml_webform_success_46337644()` callback) — don't rename those without checking the embed still fires.
3. **Replace the "Coming Soon" Amazon button** in `index.html` with the real product link once the book is live, and remove `aria-disabled`.
4. **Replace the About section bio** with your own words — the current copy is a placeholder.
5. **Set up a MailerLite automation** to send `Bonus_Story_Steady_Lantern.md` (converted to PDF) automatically on signup, so delivering it isn't a manual step.

## Local preview

Just open `index.html` in a browser — no build step.
