# SiteBazaar 🛒

**India's website marketplace** — apni website banao, list karo, aur WhatsApp se becho.

Single-file static storefront: catalog, pricing tiers, cart, WhatsApp order flow, order history aur owner dashboard. Koi backend nahi, koi payment gateway nahi — poora system ek `index.html` file me.

## Features

| Feature | Detail |
|---|---|
| 🛍️ Product Store | 14 website types — Business, Restaurant, Portfolio, E-commerce, Education, Real Estate, Branding, Custom |
| 📦 Packages | 4 pricing tiers (₹4,999 – ₹34,999) + 9 add-ons |
| 🛒 Cart | Quantity, remove, bulk discount (>₹20,000 पर 10% off) |
| 📩 WhatsApp Orders | Order message seedha owner ke WhatsApp par — koi payment data site par nahi |
| 📋 Order History | Order ID + live status tracking |
| 🔐 Owner Dashboard | Stats tiles, filter tabs, status management, WhatsApp reply link |

## Tech

Pure HTML + CSS + vanilla JS. Hash routing, `localStorage` persistence, Unsplash CDN images. No build step, no dependencies.

## Run locally

```bash
python -m http.server 8000
# then open http://localhost:8000
```

`file://` से भी चलेगा, लेकिन local testing के लिए a local server better है.

## Owner Panel

- URL: `#/admin`
- Demo password: `sitebazaar2026`

⚠️ यह password client-side ही check होता है — यह UI hide करता है, real security नहीं. Production me backend auth ज़रूरी है.

## Data

Sab data `localStorage` me — `sb_orders`, `sb_cart`, `sb_uid`. Order history per-device है (cross-device sync के लिए backend चाहिए).

## License

MIT
