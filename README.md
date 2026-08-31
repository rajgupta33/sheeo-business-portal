# SheEO Business Portal

Standalone GitHub Pages deployment for the SheEO member portal at:

`https://members.sheeo-summit.com/portal/`

The repository root redirects to `/portal/`. The PWA manifest and service worker are scoped to `/portal/`, while public actions return visitors to `https://sheeo-summit.com`.

## GitHub Pages setup

1. In **Settings → Pages**, deploy from the `main` branch and the repository root.
2. Keep the custom domain set to `members.sheeo-summit.com`.
3. Enable **Enforce HTTPS** after GitHub verifies DNS.
4. In DNS, point the `members` CNAME to `rajgupta33.github.io`.

## Supabase

Apply `supabase/migrations/` in filename order and configure these authentication URLs:

- Site URL: `https://members.sheeo-summit.com/portal/`
- Redirect URL: `https://members.sheeo-summit.com/portal/reset-password.html`

Only the browser-safe Supabase publishable key belongs in `assets/js/config.js`. Never commit a service-role or secret key.
