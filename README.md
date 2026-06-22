# Technical Moves — Engineering & Environment landing page

A single-page landing site with a job grid, plus one HTML page per role.
Dark navy brand background (#152131), light job cards, left spine coloured by
discipline (teal = engineering, green = environment). Type is Lato, self-hosted.

## Files

```
index.html                 Landing page (intro + job grid)
style.css                  All styling — change colours/spacing here once
jobs/clerk-of-works.html   Live role (engineering / teal)
jobs/ecologist.html        DEMO role (environment / green) — replace or delete
jobs/_template.html        Copy this to add a new role
assets/                    Logos, discipline icons, photo
assets/fonts/              Lato (woff2, subset to Latin)
CNAME                      Subdomain for GitHub Pages (edit to your domain)
```

## Add a job (about two minutes)

1. Copy `jobs/_template.html`, rename it (e.g. `jobs/structural-engineer.html`).
2. Edit the spots marked `>>EDIT<<`; set `data-discipline` to `eng` or `env`,
   and point the corner icon at `icon-engineering.png` or `icon-environment.svg`.
3. Open `index.html`, copy one `<a class="card">…</a>` block, paste it, and update
   the title, summary, salary, location, link, discipline and logo.

Remove a job: delete its page and its card.

## Before it goes live — change these

- **Photo**: `assets/carl.jpg` is your headshot, masked to a circle by the CSS. To change it,
  drop a square image (≥ 400×400) in at the same path.
- **Ecology icon**: `assets/icon-environment.svg` is a placeholder leaf in the matching
  frame. Swap it when you have the proper discipline icon.
- **Dates / references**: placeholder values in the cards and title blocks.

Email and phone are already set to `carl.wright@technicalmoves.com` and `01223 603269`.

## Go live on GitHub Pages

1. Create a repo, upload this folder's contents to the root.
2. Repo **Settings → Pages → Build from branch → main → /(root)**.
3. It publishes at `https://<user>.github.io/<repo>/`.
4. For the subdomain: edit `CNAME` to your chosen host (e.g. `ee.technicalmoves.com`),
   then in your DNS add a CNAME record pointing that subdomain to `<user>.github.io`.
   Tick "Enforce HTTPS" once the certificate provisions.
