# Glittering Gems

A hypothetical fine-jewelry brand website. Static site — plain HTML/CSS/JS, no build step, no dependencies (fonts are pulled from Google Fonts via CDN).

- `index.html` — page structure and copy
- `styles.css` — all styling and design tokens
- `script.js` — nav toggle, scroll reveal, demo signup form (front-end only, doesn't send anywhere)

Everything on the page (address, email, testimonial, "6–8 wks" stats) is placeholder content for a fictional brand — swap it for real details before using this for an actual business.

## Publish it on GitHub Pages

1. Create a new repository on GitHub (e.g. `glittering-gems`) — public, no need to initialize with a README since you already have one here.
2. From this folder, run:
   ```bash
   git init
   git add .
   git commit -m "Initial commit: Glittering Gems site"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<your-repo>.git
   git push -u origin main
   ```
3. On GitHub, go to your repo's **Settings → Pages**.
4. Under **Build and deployment**, set **Source** to "Deploy from a branch," pick the **main** branch and the **/ (root)** folder, then **Save**.
5. GitHub will publish it at `https://<your-username>.github.io/<your-repo>/` — it can take a minute or two to go live the first time.

## Customizing

- Colors and fonts are all defined as CSS variables at the top of `styles.css` under `:root` — change those to re-theme the whole site.
- The hero gem is a hand-built SVG in `index.html` (`#gemSvg`) — the facet shapes are plain `<polygon>` points, so you can nudge the coordinates to reshape it.
- The signup form in `script.js` is a front-end stub. To make it functional, point it at a real form backend (Formspree, Mailchimp, Netlify Forms, etc.) and swap out the `submit` handler.