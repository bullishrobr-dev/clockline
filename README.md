# Clockline

Staff time clock for Zero Lines.

- **Clock (staff):** open the site, type your PIN, choose check in / start break / end break / check out. Staff never see hours.
- **Admin:** open the site with `#admin` on the end. Live status, reports for any period, Excel/CSV export, staff and PIN management.

Single static page (`index.html`). Data lives in Supabase (Zero Lines Academy project, `clockline_*` tables). All reads and writes go through database functions that check the worker PIN or the admin session; the tables themselves are not reachable from the browser. The key in `index.html` is Supabase's publishable key, which is meant to be public.
