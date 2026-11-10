# Permit Desk

NYC permit and filing tracker (catalog → project slate → records, deadlines, data checks, reports).
Live at https://johnsochet19.github.io/permit-desk/

- The page is static and lives here (GitHub Pages). `supabase.js` is the Supabase browser library, vendored so the site doesn't depend on a CDN.
- Data, accounts and invites live in the Supabase project `permit-desk` (free plan). Everyone signs in with their own email and password; admins invite people under Settings → Users.
- The key in `index.html` is Supabase's *publishable* key: safe to be public. Row-level security only lets invited members read or change anything.
- `.github/workflows/keep-alive.yml` pings the database daily so the free project isn't paused for inactivity.
