# Shokher Ghuri — ecommerce starter

A polished, responsive storefront UI for the Shokher Ghuri brand.

## Requirements
- Node.js 20.9+ recommended
- npm

## Run locally
```bash
npm install
npm run dev
```
Open http://localhost:3000

## What is included
- Bengali responsive homepage and product cards
- Category filtering and search
- Demo cart and coupon `SHOKH10`
- WhatsApp order message to the provided number, with customer name, phone, address and COD selection
- Starter styling for mobile and desktop

## Important: this is a UI starter, not a production store
The product data and cart currently live in browser memory. The WhatsApp button opens a prefilled message to 8801887711403 but does not create a verified order in a database. Admin link is a placeholder, and customer accounts, secure admin authorization, order tracking, persistent inventory, and live bKash/Nagad payments are not implemented yet.

Before taking real orders, connect:
1. Supabase database + Auth, with Row Level Security policies.
2. Server-side order creation and validation.
3. Protected admin routes and role checks.
4. Official bKash/Nagad merchant/payment gateway credentials and server-side payment verification.
5. Real WhatsApp Business phone number in the `wa.me` URL.
6. Delivery charge rules, stock checks, privacy/return policies, and backups.

Do not put service-role keys or payment secrets in `NEXT_PUBLIC_*` variables or browser code.

## Suggested next steps
- Replace sample product names, prices, emojis and colors with actual products/photos.
- Create a Supabase project and add `.env.local` values.
- Implement database tables: `profiles`, `products`, `orders`, `order_items`, `coupons`.
- Deploy by connecting the repository to Netlify. Next.js support is documented at https://docs.netlify.com/build/frameworks/framework-setup-guides/nextjs/overview/
