# Security notes

## Environment files

- Keep credentials in local-only env files such as `.env` or `.env.local`.
- This repository ignores `.env` and `.env.*` by default and allows only `.env.example` as a committed template.
- Never put real secrets in `.env.example`.

## Frontend key visibility

- This project is a Vite + React frontend. Values shipped to browser builds are observable by users.
- Do not treat frontend API keys as private secrets.
- Keep private credentials on a backend/server-side service and call that service from the frontend.

## If a credential is exposed

- Revoke/rotate it immediately at the provider.
- Remove the credential from source control and update local/deployment configuration.
