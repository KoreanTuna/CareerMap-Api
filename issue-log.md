# Issue Log

## Docs submodule update
- Status: Blocked.
- Details: `docs` submodule clone failed due to network restriction (HTTP 403 from GitHub). This prevented scanning ERD/plan/storyboard assets in the docs repository.
- Action needed: Provide access to the docs repository or vendor the required ERD/plan/storyboard files into this repo.

## ERD / Plan / Storyboard scan
- Status: Not found in this repository.
- Details: No ERD/plan/storyboard files exist in the current repo tree, and the docs submodule could not be fetched.
- Action needed: Supply the missing artifacts or confirm their location.

## API / Domain scope confirmation
- Status: Missing.
- Details: There are no controllers, routes, or domain models in `src/main` yet. Current codebase only includes Spring Boot scaffolding.
- Questions for PM:
  - What are the core domain entities (e.g., user, career path, roadmap, milestones, assessments)?
  - What is the initial API surface (endpoints + verbs + payloads) required for MVP?

## Missing endpoints
- Status: Missing.
- Details: No REST controllers or API endpoints are implemented.
- Questions for PM:
  - Which endpoints are required for the first release? Please provide endpoint list + request/response schemas.

