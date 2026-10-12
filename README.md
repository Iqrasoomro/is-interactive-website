# IS Interactive — Static Website

A lightweight, responsive studio website for IS Interactive, featuring Polar Mills. Built with plain HTML, CSS, SVG and minimal JavaScript. No framework, build step, database, authentication or external font dependency is required.

## Preview locally

Open `index.html` in a browser. The privacy policy is at `privacy/polar-mills/index.html`.

For the most reliable local preview, run a local static server from this directory:

```bash
python -m http.server 8000
```

Then visit `http://localhost:8000` and `http://localhost:8000/privacy/polar-mills/`.

## Deploy to Netlify

1. Open Netlify and create a new site from a Git repository, or use its manual deploy flow.
2. For manual deploy, drag the **contents of this folder** into Netlify Drop.
3. No build command is needed. The publish directory is the repository root (`.`).
4. Verify the homepage and `/privacy/polar-mills/` directly in a private/incognito browser window.

## Deploy to Cloudflare Pages

1. Push the contents of this folder to a Git repository and create a Pages project from that repository.
2. Choose **None** / static HTML as the framework preset (or leave the framework preset unset).
3. Leave the build command blank. Set the output directory to `/` (repository root; if the UI requires `.` use `.`).
4. Deploy, then test both the homepage and `/privacy/polar-mills/` directly without signing in.

## Structure

- `index.html` — studio home page
- `styles.css` — responsive visual system
- `script.js` — mobile navigation and subtle section reveals
- `privacy/polar-mills/index.html` — draft game privacy policy
- `privacy/polar-mills/policy.css` — readable policy layout
- `assets/mark.svg` — favicon / studio mark

## Add another game

In `index.html`, duplicate the `article.game-card` element inside `#games`, then update the title, description, features and artwork. Keep a real store button disabled until an official store URL is available.

## Important before publishing the privacy policy

The Polar Mills privacy policy is deliberately labelled **Draft for review**. Check the final implementation of AdMob and Epic Online Services, data flows, consent and age targeting, then align the policy with Google Play Console's Data safety answers. Do not publish the draft as final until this review is complete.
