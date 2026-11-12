# Perch & Seed: bird feeding picks site

Static site for GitHub Pages (Settings > Pages > Deploy from branch `main`, folder `/`).

- `index.html` forwards to `picks/` and keeps `?src=`. The old waitlist page is in git history.
- `picks/index.html` is the picks page (paid links, budget / mid-range / premium, no prices). Seed-packet style since 2026-11-12, built by /mnt/project-files/ps-seed-packet/build.py (project files). Animations: GSAP + ScrollTrigger + Lenis, self-hosted in `picks/vendor/`. Photo credits: `assets/CREDITS.md`. Every pick has a product picture slot that loads `assets/products/<ASIN>.jpg` and shows a drawing of the feeder until that photo exists.
- `picks/kit.js` (same file on all three picks sites) runs the email sign-up and the cookie-free counting:
  - Sign-up posts straight to MailerLite account 2745570, form 202478167777085313 ("Up close site"), double opt-in, with `signup_source` = the `?src=` value.
  - GoatCounter code `perchseed` counts visits (source = `?src=`), clicks on "See it on Amazon" (`out/<ASIN>`) and sign-ups (`signup`). Nothing is fetched from Amazon.

## Tracking ID
Amazon links use `perchandseed-20` (Sam created it 2026-11-11). The older `perchseed-20` is also in Sam's account, so old links with it still credit Sam.
