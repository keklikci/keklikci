# README automation setup

The workflow in `workflows/readme-scribe.yml` renders `templates/README.md.tpl`
into the repository's `README.md`.

Before its first run, add a repository Actions secret named
`PERSONAL_GITHUB_TOKEN`. Use a classic GitHub personal access token with these
scopes:

- `read:user`
- `repo:status`
- `public_repo`

After adding the secret, run **Update README** from the Actions tab. Subsequent
runs happen daily at 00:00 UTC and commit only when the rendered README changes.
