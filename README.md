# Shared GitHub CI workflows

## Reusable Node CI

The default matrix tests supported Node.js LTS lines at their dependency-compatible floors: Node.js `22.13.0` and
Node.js `24`. Coverage uploads only from Node.js `24` so matrix jobs do not publish duplicate reports.

```yaml
jobs:
  quality:
    uses: robert7/workflows/.github/workflows/node-ci.yml@v0.4.0
    with:
      node_versions: '["22.13.0", "24"]'
      coverage_node_version: '24'
    secrets:
      codecov_token: ${{ secrets.CODECOV_TOKEN }}
```

Callers may override `node_versions` with any JSON array and select one matching entry for
`coverage_node_version`.
