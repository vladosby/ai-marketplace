# Safety and pacing

- **Approval gate:** every save and every publish needs the user's explicit "yes" to the exact text shown.
- **Pacing:** wait a few seconds between navigations; do not open many pages in parallel.
- **Scope:** only the signed-in user's own profile and posts.
- **Stop conditions:** CAPTCHA, checkpoint, forced re-login, "unusual activity", rate-limit or restriction
  banners. Stop, tell the user, do not retry or work around it.
- **Secrets:** never read, print or store cookies, tokens or passwords. The browser profile directory
  holds the session; it must never be committed to git or shared.
- **Privacy:** profile data stays in the conversation; do not send it to other services.
