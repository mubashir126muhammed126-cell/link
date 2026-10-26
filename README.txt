LINKORAX — FULL GITHUB PAGES + SUPABASE PACKAGE

UPLOAD
1. Download and extract this ZIP.
2. Open your GitHub repository: mubashir126muhammed126-cell.github.io
3. Open the folder that serves your current LinkoraX page (your screenshot appears to show a page under /link/).
4. Replace that folder's existing HTML with this package's index.html. If your live URL is /link/, put index.html in the repository's link/ folder.
5. Commit changes and wait for GitHub Pages to publish.

SUPABASE AUTH
1. Supabase Dashboard > Project Settings > API (or API Keys).
2. The HTML already contains the Project URL and publishable key you provided.
3. Authentication > Providers: enable Email.
4. Authentication > Users: create/confirm admin user monumuhammed92@gmail.com.
5. Authentication > URL Configuration: add your exact GitHub Pages URL, including /link/ if that is the path, to allowed redirect URLs.
6. Test login and Forgot password.

IMPORTANT
- The page uses Supabase, not Firebase.
- Never put a password or Supabase service_role/secret key in HTML.
- The supplied publishable key is for browser use.
- This package enables Supabase authentication for the admin UI. Portfolio content is still browser-local; shared projects/uploads require Supabase database tables, RLS policies, and Storage buckets.
- This is static HTML. It does not create database tables or storage policies automatically.
