# setup-jacoco-cli

A GitHub Action that downloads and sets up [jacoco-cli](https://github.com/bgalek/jacoco-cli) for use in your workflows. It automatically detects the runner's OS and architecture, resolves the requested version, and adds `jacoco-cli` to `PATH`.

## Inputs

| Name      | Description                                              | Required | Default  |
|-----------|----------------------------------------------------------|----------|----------|
| `version` | Version of jacoco-cli to install (e.g. `1.0.0`).        | No       | `latest` |

## Usage

```yaml
steps:
  - uses: actions/checkout@v4
  - uses: bgalek/setup-jacoco-cli@v1
    with:
      version: latest
  - run: jacoco-cli report coverage.exec --classfiles build/classes --html report
```
