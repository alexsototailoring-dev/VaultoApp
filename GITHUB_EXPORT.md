# Vaulto GitHub Export

This archive contains the Vaulto application source at stable rollback checkpoint `fc6b9ff8`: frontend, backend, database schema, tests, Docker/deployment configuration, assets, and lockfiles.

The export intentionally excludes `.git`, dependencies, build output, logs, real environment files, and `.manus/db` query artifacts. The query artifacts contained live user/account data and must not be uploaded to GitHub.

## Run locally

```bash
pnpm install
pnpm run dev
```

## Verify

```bash
pnpm test -- --run
pnpm run check
pnpm run build
```

## Environment

Copy `.env.aws.example` to `.env` and replace every placeholder with your own credentials. The Manus-specific OAuth, database, storage, Stripe, and Resend integrations require replacement configuration when hosted outside Manus. Never commit real secrets.

## Upload to GitHub

```bash
git init
git add .
git commit -m "Initial Vaulto project export"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
git push -u origin main
```
