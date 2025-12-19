# Operations Considerations

## Schema / Migration / Seed
- Current status: No database configuration or schema migrations exist.
- Observations:
  - `spring.datasource` is not configured in `application.yaml`.
  - No JPA entities or migration tooling (e.g., Flyway/Liquibase) are present.
- Decisions needed:
  - Choose migration tool (Flyway or Liquibase).
  - Define initial schema and seed strategy (dev/test seed vs. prod seed).

## Authentication / Authorization
- Current status: Not implemented.
- Observations:
  - No security dependencies (e.g., Spring Security) are included.
  - No auth/role model or token strategy is defined.
- Decisions needed:
  - Select auth method (JWT/OAuth2/session).
  - Define roles/permissions and access rules per endpoint.

## Rate Limit / Timeout
- Current status: Not configured.
- Observations:
  - No API gateway or rate-limit middleware settings are present.
  - No HTTP client/server timeout settings are defined.
- Decisions needed:
  - Define API rate-limit policy and enforcement layer.
  - Set request/response timeout defaults for server and any outbound calls.

## Deployment / Environment Variables / Secrets
- Current status: **Blocked — not defined.**
- Observations:
  - `application.yaml` only contains an app name. No environment variable or secret management approach exists.
- Blocker:
  - Without a defined deployment target (e.g., ECS/GKE/VM), secret store (e.g., AWS SSM/Secrets Manager, Vault), and env var strategy, production readiness cannot be assessed.
- Action required:
  - PM to specify deployment platform and secret management approach.

