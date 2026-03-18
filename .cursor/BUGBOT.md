# amazon-ecs-deploy-task-definition — Repo-Specific BugBot Rules

> Org-wide rules are enforced via Cursor Team Rules.

## GitHub Action

- This is a GitHub Action for deploying ECS task definitions (forked from AWS). The action definition is in `action.yml` and the logic is in `index.js`.
- The bundled `dist/index.js` must be rebuilt after any changes to `index.js` or dependencies. PRs that modify source but not `dist/` are incomplete.

## Testing

- Tests are in `index.test.js`. Run tests before committing changes to the action logic.

## Change Management

- This action is consumed by many repos' CI pipelines. Breaking changes to inputs/outputs in `action.yml` affect all consumers — document in `CHANGELOG.md`.
