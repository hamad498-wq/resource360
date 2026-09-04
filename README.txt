Resource360 Client Portal — Supabase V3

This version replaces the old hard-coded demo login with Supabase Auth.

Configured:
- Supabase project URL
- Browser-safe publishable API key
- Email/password sign-in
- Session restoration
- Sign-out
- Protected clients-table profile lookup
- Existing RLS policy remains the database security boundary

Test:
1. Extract the ZIP.
2. Deploy the folder to a static HTTPS host (recommended) or run it from a local web server.
3. Open the site and click Client Login.
4. Sign in with client1@resource360.com and the password you created in Supabase.
5. Client 1 should load Demo Client.
6. client2@resource360.com can authenticate, but because no clients row exists for it, the portal should deny dashboard access.

IMPORTANT:
- Never place a Supabase secret/service_role key in this website.
- The publishable key is intentionally browser-side.
- Real client data should only be added to tables with appropriate RLS policies.
