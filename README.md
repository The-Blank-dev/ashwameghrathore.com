# ashwameghrathore.com

Personal single-page website for Ashwamegh Rathore. Plain HTML/CSS, no build step.

## Deploying with GitHub Pages

1. Push this repo to GitHub (e.g. `github.com/The-Blank-dev/ashwameghrathore.com`).
2. In the repo, go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to `Deploy from a branch`, branch `main`, folder `/ (root)`. Save.
4. GitHub will serve the site at `https://<username>.github.io/<repo>/` within a minute or two — confirm that works first.

## Pointing ashwameghrathore.com at it

The `CNAME` file in this repo already tells GitHub Pages to serve the custom domain. You still need to configure DNS with your domain registrar:

**Apex domain (`ashwameghrathore.com`)** — add these 4 `A` records pointing to GitHub Pages' IPs:
```
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

**`www` subdomain (optional, recommended)** — add a `CNAME` record:
```
www → <username>.github.io.
```

After DNS propagates (can take up to a few hours), go back to **Settings → Pages** in the repo, enter `ashwameghrathore.com` under **Custom domain**, and save. Once GitHub verifies it, enable **Enforce HTTPS**.

## Editing content

Everything lives in `index.html` — name, bio, experience entries, and contact links are plain HTML/CSS with no templating. Colors and spacing are controlled by CSS variables at the top of the `<style>` block, including automatic dark mode via `prefers-color-scheme`.
