# Seoyun Gallery

Responsive artist portfolio and purchase-inquiry storefront, based on the supplied gallery design and original artwork photos. English/Korean switch, artwork details with four photo views, and purchase inquiry drafting/copying. No dependencies or build required.

## Preview

Run `python3 -m http.server 8080` inside this directory and visit http://localhost:8080.

## Configure before sales

Edit `catalog.js`: set the real `contactEmail`, verified prices, dimensions and availability. The source attachment used an unverified example email; it has deliberately not been reused. The supplied four photos show one painting, so the catalog contains one original and three detail views. The supplied template's birthday painting was omitted because no matching photo was provided. Artwork title is retained from the supplied template; confirm the title and medium before launch.

Without a contact address, inquiries are draft-and-copy only and clearly say they have not been sent. With an email address configured, users can open their email application to send the inquiry. Optional HTTPS `checkoutUrl` per artwork supports an externally managed payment page. There is no integrated payment processing, order database, inventory locking, tax/shipping calculation, or automatic order email.

## Deploy

Import this repository into Vercel as an Other/static project, with no build command and output directory `.`. Or publish the root directory through GitHub Pages. All assets use relative paths.

## Push to GitHub

After creating a private repository named `seoyun` under your GitHub account:

```sh
git remote add origin https://github.com/bibibigbar-dev/seoyun.git
git push -u origin main
```

No credentials are stored in the project.
