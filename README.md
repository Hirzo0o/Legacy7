# The Last Dance Collectibles

Storefront for three framed World Cup editions (CR7, Lionel Messi, Neymar Jr). Plain HTML and JavaScript with Tailwind from its CDN; no build step.

## Managing content

Open `/admin/` on the live site and choose **Sign in with Token** (a GitHub token with Contents read and write access to this repo). Saving commits to the `production-ready` branch, and Render redeploys in about a minute.

- **Editions** (`content/editions.json`): status (on sale, sold out, hidden), name, price and original price, headline (wrap words in `*stars*` for gold), story text, photos, video and the six cards for each edition. An edition with photos shows them; one without shows the illustrated frame.
- **Customer reviews** (`content/reviews.json`): reviews per edition. An edition with no reviews hides the reviews section.
- **Site settings** (`content/settings.json`): logo text, top bar message, WhatsApp number, footer phone number and browser tab icon.

Orders go through a pre-filled WhatsApp message listing the bag and total. `index.html` contains the same content as a fallback if a file fails to load.

## Deploy

`render.yaml` defines a Render static site that publishes the repo root.
If the site moves to a custom domain, update the URL in `index.html` (canonical, Open Graph, JSON-LD), `robots.txt` and `sitemap.xml`.

## Colours

The homepage uses Tailwind classes with the palette in the `tailwind.config` block of `index.html` (obsidian `#080808`, gold `#D4AF37`, champagne `#F3E5AB`). Headings use Cinzel and body text uses Plus Jakarta Sans, both self-hosted in `fonts/`. The policy pages use `pages.css` and `theme.css`.
