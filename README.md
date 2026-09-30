# Diva Designer Boutique

A single-page boutique app for customers, tailors (staff) and the head.

- **Customers:** sign up, upload a 6×6 inch fabric photo, pick a style (blouse, modern, bridal, traditional, ethnic), choose one of 3 generated designs, and book a fitting with a tailor.
- **Staff:** enter measurements at the fitting, set the delivery date, and mark orders stitched and delivered.
- **Head:** see all orders, reassign tailors, change delivery dates.
- Everyone gets in-app notifications at each step.

## Tech
- One file: `index.html` (plain HTML/JS, no build step)
- Backend: [Supabase](https://supabase.com) (login, database, row-level security)
- Hosting: GitHub Pages

## Setup
1. Create a Supabase project and run the SQL for the `profiles`, `orders` and `notifications` tables with row-level security.
2. Put your project URL and **publishable** key in `index.html` (`SB` and `KEY`). Never commit the `service_role` key.
3. In Supabase → Authentication → URL Configuration, add the site address as the Site URL and Redirect URL.
4. Give roles in the `profiles` table: `customer` (default), `staff`, `head`.
5. Enable GitHub Pages: Settings → Pages → Deploy from branch → `main` / root.

Live site: https://rajshrid.github.io/diva-boutique/
