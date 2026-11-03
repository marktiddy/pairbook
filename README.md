# Pairbook website

Static site for GitHub Pages: `index.html` (landing page), `privacy.html` (the policy App Store Connect and the
app link to), `support.html` (the support URL), and `demo-sticker.pdf` (App Review). No build step, no
JavaScript, no analytics or cookies (the app's "Data Not Collected" promise applies to the site too).

## Publish

The site is deployed by GitHub Actions (`.github/workflows/pages.yml`) on every push to `main`, or manually from
the Actions tab. There is no build step; the workflow uploads the repository root as the Pages artifact.

1. On GitHub: the repository › Settings › Pages › Build and deployment › Source: **GitHub Actions**.
2. Push to `main`. The site appears at `https://marktiddy.github.io/pairbook/` within a minute or two.
3. Check both links open: `/privacy.html` and `/support.html`. Use them in App Store Connect (Privacy Policy URL,
   Support URL).

The site lives at the repository root rather than in a `site/` folder because this repository contains only the
website. If the site is later moved into a subdirectory, update `path` in the workflow to match.

## Before launch

- [ ] Replace `support@example.com` in `support.html` with your real support address.
- [ ] When the app is live, change the hero button in `index.html` to the App Store link, and add the
      `apple-itunes-app` meta tag (commented in the `<head>`).
- [ ] If you use a different GitHub username or repository name, update `Monetisation.Links` in the app
      (`Packages/PairbookCore/Sources/PairbookStoreKit/Monetisation.swift`).

Images come from the app's sample home (`design/screenshots/capture.sh`), so they contain nothing real.
