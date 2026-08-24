# shoreline-landing-pages

Dedicated PPC/offer landing pages for Shoreline Pro Services — kept separate from the main site ([`shorelinepro-website`](https://github.com/shorelineproservices/shorelinepro-website)) so ad traffic lands on a focused, distraction-free page instead of the full homepage.

**Live:** https://shorelinepro-landing.netlify.app (not yet on a custom subdomain — fine for now since Google Ads campaigns aren't running yet; see the Google Ads Launch Kit artifact for the campaign plan).

**Pages:** `index.html` (the landing page + estimate form), `thank-you.html` (form success). Intentionally `noindex` — this page duplicates the homepage's messaging and isn't meant to compete with it in organic search.

**Form backend:** Netlify Forms — same setup as the main site (photo/video upload, honeypot, email notification to shorelineproservices@gmail.com, redirects to `/thank-you.html`).

**To update the live site:**
```bash
git add . && git commit -m "..." && git push   # history
netlify deploy --prod --dir=.                  # actually deploys — pushing alone does not
```

No CI/CD wired up yet, same as the main site.
