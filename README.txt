LinkoraX — shared cross-browser portfolio setup

FILES
- LinkoraX_supabase_full.html: complete website HTML. Upload as link/index.html in your GitHub repository.
- LinkoraX_supabase_setup.sql: creates the shared portfolios/contact tables, RLS policies, and portfolio-media storage bucket in your existing Supabase project.

SETUP ORDER
1. In Supabase Dashboard, open SQL Editor > New query.
2. Paste the entire contents of LinkoraX_supabase_setup.sql and run it.
3. In Supabase Authentication > URL Configuration, set Site URL to:
   https://mubashir126muhammed126-cell.github.io/link/
   Add this URL to the Redirect URLs allow-list as well.
4. Confirm the admin user exists in Authentication > Users and its email is exactly the configured admin email in the HTML.
5. In GitHub, open the link folder and replace link/index.html with LinkoraX_supabase_full.html (rename it to index.html), then commit to main.
6. Open https://mubashir126muhammed126-cell.github.io/link/ and hard refresh.
7. Sign in. Add a portfolio and upload media. New projects start as drafts; use Publish to make them public.

SECURITY
- The HTML contains only the Supabase project URL and publishable key. Never add a service_role or secret key to client-side HTML.
- RLS policies restrict portfolio create/update/delete, contact updates, and storage uploads/deletes to the configured admin email. Public visitors can read only published portfolio rows and the public contact settings.
- The media bucket is public so public portfolio media can load without a visitor login. Do not upload private or sensitive files to it.
- Portfolio data previously stored in a browser's localStorage is not automatically migrated. Recreate those projects in the admin dashboard after setup, or export/import them separately.
- Supabase email delivery/reset settings are managed separately. The app will show the exact returned error if sign-in/reset fails.
