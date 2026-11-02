# Pairbook website

Static site for GitHub Pages: `index.html` (landing page), `privacy.html` (the policy App Store Connect and the
app link to), `support.html` (the support URL), and `demo-sticker.pdf` (App Review). No build step, no
JavaScript, no analytics or cookies (the app's "Data Not Collected" promise applies to the site too).

## Publish (about 5 minutes)

1. On GitHub, create a public repository named **`pairbook`** (the app links to
   `https://marktiddy.github.io/pairbook/privacy.html` and `.../support.html`, so the name matters).
2. In this folder:
   ```sh
   git init -b main
   git add .
   git commit -m "Pairbook website"
   git remote add origin git@github.com:marktiddy/pairbook.git
   git push -u origin main
   ```
3. On GitHub: the repository › Settings › Pages › Build and deployment › Source: **Deploy from a branch**,
   Branch: **main**, folder **/ (root)** › Save. The site appears at `https://marktiddy.github.io/pairbook/`
   within a minute or two.
4. Check both links open: `/privacy.html` and `/support.html`. Use them in App Store Connect (Privacy Policy URL,
   Support URL).

## Before launch

- [ ] Replace `support@example.com` in `support.html` with your real support address.
- [ ] When the app is live, change the hero button in `index.html` to the App Store link, and add the
      `apple-itunes-app` meta tag (commented in the `<head>`).
- [ ] If you use a different GitHub username or repository name, update `Monetisation.Links` in the app
      (`Packages/PairbookCore/Sources/PairbookStoreKit/Monetisation.swift`).

Images come from the app's sample home (`design/screenshots/capture.sh`), so they contain nothing real.
