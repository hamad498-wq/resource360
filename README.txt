Resource360 Client Portal — Supabase V4

Adds public self-registration using Supabase Auth.

IMPORTANT DATABASE SETUP:
Run Resource360_signup_profile_trigger.sql once in Supabase SQL Editor before testing Sign Up.

Signup flow:
1. Visitor enters full name, email, and password.
2. Supabase Auth creates the user.
3. Database trigger creates public.clients row with membership_status = Pending.
4. Existing RLS policy keeps each client limited to their own row.
5. If email confirmation is enabled, the user confirms their email before signing in.

Never place a secret/service_role key in this website. The browser-safe publishable key is intentional.
