# The Last Dance Collectibles

Single-page product site for The Last Dance Collectibles | The Icon Series. Plain HTML, CSS and JavaScript with no build step.

## Managing listings and the logo

Open `/admin/` on the live site and choose **Sign in with Token** (a GitHub token with Contents read and write access to this repo).

- **Product listings** edits `content/products.json`: title, prices, status, images and an optional card checkout link per product.
- **Site settings and logo** edits `content/settings.json`: header logo, footer logo, browser tab icon, product logo, WhatsApp number and phone.

The product marked Featured fills the main buy box; other visible products appear under "More from The Last Dance Collectibles".
A product with no checkout link takes orders through a pre-filled WhatsApp message.
Saving in the admin commits to the `production-ready` branch, and Render redeploys automatically.

## Deploy

`render.yaml` defines a Render static site that publishes the repo root.
If the site moves to a custom domain, update the URL in `index.html` (canonical, Open Graph, JSON-LD), `robots.txt` and `sitemap.xml`.

## Colours

All colours come from the `:root` palette at the top of the `<style>` block in `index.html` (frame black, gold foil and ivory, with crimson for the discount badge only). Headings use Cinzel and body text uses Plus Jakarta Sans, both self-hosted in `fonts/`. `theme.css` holds the colours and type and loads last. Change a value there to restyle the whole page.
