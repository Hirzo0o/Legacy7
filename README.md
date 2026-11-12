# Legacy7

Single-page product site for Legacy 7 | The Icon Series. Plain HTML, CSS and JavaScript with no build step.

## Checkout

`index.html` has a config block at the top of its script:

- `CHECKOUT_URL`: paste a Shopify or Stripe payment link to send "Order Now" to card checkout.
- While `CHECKOUT_URL` is empty, "Order Now" opens a pre-filled WhatsApp order to `WHATSAPP_NUMBER`.

## Deploy

`render.yaml` defines a Render static site that publishes the repo root.
If the site moves to a custom domain, update the URL in `index.html` (canonical, Open Graph, JSON-LD), `robots.txt` and `sitemap.xml`.
