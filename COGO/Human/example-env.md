# Example environment variables

This file is a **scratchpad** for variable and secret **names** (and non-sensitive defaults). COGO may append or reorganize sections as the project grows.

**Do not commit real secrets.** Copy names and values into a real `.env` (gitignored), your host's secret manager, or CI secrets.

```bash
# --- Application ---
NODE_ENV=development
APP_NAME=
APP_URL=http://localhost:3000
PORT=3000
LOG_LEVEL=debug

# --- Database ---
DATABASE_URL=postgresql://USER:PASSWORD@localhost:5432/DBNAME

# --- Auth / sessions ---
SESSION_SECRET=GENERATE_A_LONG_RANDOM_STRING
JWT_SECRET=GENERATE_A_LONG_RANDOM_STRING
OAUTH_CLIENT_ID=
OAUTH_CLIENT_SECRET=
OAUTH_ISSUER_URL=

# --- Third-party APIs ---
API_KEY_EXTERNAL_SERVICE=

# --- Email ---
SMTP_HOST=
SMTP_PORT=
SMTP_USER=
SMTP_PASSWORD=

# --- Storage ---
S3_BUCKET=
S3_REGION=
AWS_ACCESS_KEY_ID=
AWS_SECRET_ACCESS_KEY=

# --- Payments (if applicable) ---
STRIPE_SECRET_KEY=
STRIPE_WEBHOOK_SECRET=

# --- Observability ---
SENTRY_DSN=
DATADOG_API_KEY=
```

## Usage

1. Duplicate relevant keys into `.env`, `.env.local`, or platform-specific secret UI.
2. Delete placeholder lines you do not need.
3. Rotate any secret that was ever pasted into chat or committed by mistake.
