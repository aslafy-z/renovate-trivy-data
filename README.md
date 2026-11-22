# renovate-trivy-data

The central [renovate-trivy](https://github.com/aslafy-z/renovate-trivy) run
for my repositories.

- **`main`** (this branch): the [workflow](.github/workflows/renovate-trivy.yml)
  and the list of repositories it scans.
- **[`data`](../../tree/data)**: generated on every run. The Renovate preset,
  a [CVE report per repository](../../tree/data/repos) and the shared SBOM
  archive. A single commit, force-pushed: do not edit it.

Repositories take part by extending the preset, with the same line everywhere:

```json
"extends": ["github>aslafy-z/renovate-trivy-data:renovate-trivy#data"]
```

To scan another repository, add it to `repositories` in the workflow.
