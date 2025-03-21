# workflows

This is a small project to experiment and demo setting up workflows with tagging for development, staging and production.

## Resources

- <https://github.com/marketplace/actions/git-auto-commit>

## Flow

**Protected Branches:**

- `develop`
- `staging`
- `main`

### Feature or Bug Development

Any features:

- `feature/<issue-nr-description>` -> `develop`
- Use `minor` label on PR

Any bugs:

- `bug/<issue-nr-description>` -> `develop`
- Use `patch` label on PR

Any small code changes with no build:

- `any` -> `develop`
- Use `no-build` label on PR

### Release Candidate

After some number of features and bugs, ready for release:

- `develop-into-staging` -> `staging`
- No labels needed

Any required hotfixes:

- `hotfix/<issue-nr-description>` -> `staging`
- Use `patch` label on PR

### Production

After staging release is ready, create PR into main:

- `staging-into-main` -> `main`
- No labels needed

### Update Development

After a production release, update development branch:

- `main-into-develop` -> `develop`
- No labels needed

Note: use `major` label only when required.
