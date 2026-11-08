# Nozzle and Beam

Custom 3D prints shop. Dark techy design + Stripe Checkout on Vercel.

## What’s included

- Brand name: **Nozzle and Beam**
- 3D printer hero that builds layers **upward**
- 30 products (size, color, personalization)
- Product photos: set `image: "/images/file.jpg"` on a product in `public/js/catalog.js`
- Cart + Stripe Checkout (`api/checkout.js`)
- Custom file request form

## New GitHub repo

1. Create an empty GitHub repo
2. Unzip this folder and upload **everything inside** `nozzle-beam/` (not the folder itself if you already named the repo)
3. Commit

You should see:

```
api/checkout.js
package.json
vercel.json
public/index.html
public/styles.css
public/js/...
```

## Deploy on Vercel

1. [vercel.com](https://vercel.com) → Add New → Project → import the GitHub repo
2. Framework: Other. Output directory is already set in `vercel.json` to `public`
3. Deploy

## Stripe

1. In Vercel → Settings → Environment Variables
2. Add `STRIPE_SECRET_KEY` = your `sk_test_…` (or live) key
3. Redeploy

Checkout posts to `/api/checkout` and redirects to Stripe.

## Product photos

Put files in `public/images/` and in `public/js/catalog.js`:

```js
image: "/images/keychain.jpg"
```

Leave `image` unset (or `null`) to keep the icon tile.
