# README automation setup

The workflow in `workflows/readme-scribe.yml` renders `templates/README.md.tpl`
into the repository's `README.md`.

Before its first run, or to replace a revoked or expired token, set the
repository Actions secret `PERSONAL_GITHUB_TOKEN` to a classic GitHub personal
access token with these scopes:

- `read:user`
- `repo:status`
- `public_repo`

After adding the secret, run **Update README** from the Actions tab. Subsequent
runs happen daily at 00:00 UTC and commit only when the rendered README changes.

## Contribution history chart

The template embeds a live chart from `commit-history.com` for `keklikci`. It
requires no additional workflow step or secret and tracks aggregate
contribution counts over time, including anonymized private contributions.
