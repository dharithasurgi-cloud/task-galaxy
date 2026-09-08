# Security

## Deployment boundary

Deploy this app only over HTTPS, such as GitHub Pages. Do not distribute modified copies from unknown hosts. Browsers verify the HTTPS origin and service-worker scope before allowing installation.

## Data model

The planner stores tasks, categories, and theme preferences in browser `localStorage`. This is device-local data, not encrypted storage or cloud backup. Never enter passwords, financial information, access tokens, or other sensitive data into tasks or notes.

## App protections

- Content Security Policy limits scripts, connections, frames, objects, and forms to the app origin.
- No application secrets or authentication tokens are shipped in the client.
- The service worker caches only same-origin app files.
- The app does not make API calls or upload planner records.
- The app uses browser text APIs for user-created task content instead of injecting raw task text as HTML.

## Future cloud sync

Adding accounts, sharing, or synchronization requires a backend with authentication, authorization, HTTPS-only cookies or short-lived tokens, server-side input validation, rate limiting, encrypted storage, CSRF protection, audit logging, and a documented data deletion policy.
