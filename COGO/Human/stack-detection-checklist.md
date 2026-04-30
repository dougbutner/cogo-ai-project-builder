# Stack Detection Checklist

Use during `/install-project`, `/rewrite-project`, or `/bootstrap-project` when inferring the stack from the repo.

## Order of inspection

1. **Repository root**: `package.json`, `pnpm-lock.yaml`, `yarn.lock`, `requirements.txt`, `pyproject.toml`, `go.mod`, `Cargo.toml`, `composer.json`, `Gemfile`, `Dockerfile`, `docker-compose.yml`, `Makefile`, `Justfile`.
2. **Monorepo signals**: `pnpm-workspace.yaml`, `turbo.json`, `nx.json`, `lerna.json`.
3. **Frontend**: `vite.config.*`, `next.config.*`, `nuxt.config.*`, `angular.json`, `svelte.config.*`, `index.html` + bundler hints.
4. **Backend**: framework-specific configs (Express/Fastify/Nest, Django/Flask/FastAPI, Rails, Spring, etc.).
5. **Mobile**: `android/`, `ios/`, Flutter, React Native.
6. **Database**: `prisma/schema.prisma`, `drizzle.config.*`, `migrations/`, ORM configs, `docker-compose` services.
7. **Auth**: OAuth/OIDC/SAML configs, NextAuth, Clerk, Auth0, Cognito, Supabase auth.
8. **CI/CD**: `.github/workflows/`, `.gitlab-ci.yml`, Buildkite, CircleCI, Cloud Build.
9. **Cloud / infra**: Terraform, Pulumi, SAM, Serverless, Kubernetes manifests, Fly/Railway/Vercel configs.

## If ambiguous

- Prefer listing **two hypotheses** and ask one question (e.g. "Is X the canonical deploy path?").
- Record the resolved stack in `COGO/Current-Project.md` under Recent Decisions.
