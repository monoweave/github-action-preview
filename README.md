# github-action-preview

This GitHub action generates previews of NPM package version bumps and changelogs when used in conjunction with [Monoweave](https://github.com/monoweave/monoweave).

## Usage

```yaml
- uses: monoweave/github-action-preview@main
  with:
    token: ${{ secrets.GITHUB_TOKEN }}
```

## Workflow Permissions

You will need to grant GitHub Actions the ability to comment on pull requests, e.g.:

```
permissions:
  pull-requests: write
  issues: write
```

## Action Inputs

| Name | Description | Default |
| ---- | ----------- | ------- |
| `token` | `GITHUB_TOKEN` or PAT with ability to comment on pull requests. | `${{ github.token }}` |
| `monoweave-command` | The monoweave executable to run. | `yarn monoweave` |

## License

[BSD-3](./LICENSE)
