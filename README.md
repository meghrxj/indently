# Indently website

Five self-contained pages. Each file carries its own styles and scripts, so there is nothing else to upload.

- index.html: home
- sourcing.html: for buyers, with the buyer dashboard demo
- selling.html: for suppliers, with the seller dashboard demo and WhatsApp flow
- manufacturing.html: for brands and manufacturers, with both demos
- solutions.html: procure-to-pay, order-to-cash, smart ordering, e-auctions, group buying and payments

## Deploy on Cloudflare Pages
1. Put these files in a GitHub repo, for example `indently-site`.
2. In Cloudflare, open Workers & Pages, then Create, Pages, Connect to Git, and pick the repo.
3. Build command: none. Output directory: `/`.
4. Add `indently.in` under Custom domains.

## Turn on the early access form (do this before launch)
In each HTML file, find `var FORM_ENDPOINT = '';` and set it to a Formspree, Getform or Cloudflare Worker URL.
Until it is set, the form shows a thank-you message but sends nothing.

## Real product photos
The dashboards use drawn illustrations. To use real photos:
1. Add a `products` folder next to the pages with these files: oil.jpg, bolt.jpg, brg.jpg, shoe.jpg, glv.jpg, cbl.jpg, mig.jpg, cut.jpg, film.jpg, ht.jpg.
2. In sourcing.html and selling.html, change `var PRODUCT_PHOTOS = false;` to `true`.
Any photo that is missing falls back to its illustration.

All dashboard screens show sample data. The app itself will live at app.indently.in.
