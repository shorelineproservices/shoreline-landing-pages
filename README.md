# shoreline-landing-pages

Dedicated PPC/offer landing pages for Shoreline Pro Services — kept separate from the main site ([`shorelinepro-website`](https://github.com/shorelineproservices/shorelinepro-website)) so ad traffic lands on a focused, distraction-free page instead of the full homepage.

**Live:** https://get-estimate.shorelineproservices.com (migrated off Netlify to Cloudflare Pages 2026-08-29 — see the main site's README for why).

**Pages:** `index.html` (the landing page + estimate form), `thank-you.html` (form success). Intentionally `noindex` — this page duplicates the homepage's messaging and isn't meant to compete with it in organic search.

**Form backend:** Netlify Forms — a holdover from the old hosting, works standalone regardless of where the site itself is hosted. Photo/video upload, honeypot, email notification to shorelineproservices@gmail.com, redirects to `/thank-you.html`.

**To update the live site:**
```bash
git add . && git commit -m "..." && git push        # history
npx wrangler pages deploy . --project-name=shoreline-landing-pages --branch=main   # actually deploys
```

Check the Cloudflare dashboard (Workers & Pages → shoreline-landing-pages → Settings → Build & deployments) to see if Git-connected auto-deploy has been set up — if not, the `wrangler pages deploy` command above needs to be run manually after each push, same as before.
