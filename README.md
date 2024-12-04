# Docker image for running markdownlint-cli in Azure Pipelines container jobs

<!-- markdownlint-disable MD013 -->
[![License](https://img.shields.io/badge/license-MIT-blue.svg?style=flat-square)](https://github.com/swissgrc/docker-azure-pipelines-markdownlint/blob/main/LICENSE) [![Build](https://img.shields.io/github/actions/workflow/status/swissgrc/docker-azure-pipelines-markdownlint/publish.yml?branch=develop&style=flat-square)](https://github.com/swissgrc/docker-azure-pipelines-markdownlint/actions/workflows/publish.yml) [![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=swissgrc_docker-azure-pipelines-markdownlint&metric=alert_status)](https://sonarcloud.io/summary/new_code?id=swissgrc_docker-azure-pipelines-markdownlint) [![Pulls](https://img.shields.io/docker/pulls/swissgrc/azure-pipelines-markdownlint.svg?style=flat-square)](https://hub.docker.com/r/swissgrc/azure-pipelines-markdownlint) [![Stars](https://img.shields.io/docker/stars/swissgrc/azure-pipelines-markdownlint.svg?style=flat-square)](https://hub.docker.com/r/swissgrc/azure-pipelines-markdownlint)
<!-- markdownlint-restore -->

Docker image to run [markdownlint] commands in [Azure Pipelines container jobs].

## Usage

This container can be used to run markdownlint commands in [Azure Pipelines container jobs].

### Azure Pipelines Container Job

To use the image in an Azure Pipelines Container Job add the following task use it with the `container` property.

The following example shows the container used for linting the repository:

```yaml
- stage: Build
  jobs:
  - job: Lint
    steps:
    - bash: |
        markdownlint --output /markdownlint.json --json --config /.markdownlint.json /docs
      target: swissgrc/azure-pipelines-markdownlint:latest
```

### Tags

<!-- markdownlint-disable MD013 -->
| Tag      | Description                                                                                       | Base Image                 | Markdownlint-Cli | Size                                                                                                                                  |
|----------|---------------------------------------------------------------------------------------------------|----------------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| latest   | Latest stable release (from `main` branch)                                                        | node:22.11.0-bookworm-slim | 0.43.0           | ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/swissgrc/azure-pipelines-markdownlint/latest?style=flat-square)   |
| unstable | Latest unstable release (from `develop` branch)                                                   | node:22.12.0-bookworm-slim | 0.43.0           | ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/swissgrc/azure-pipelines-markdownlint/unstable?style=flat-square) |
| 0.31.1   | [markdownlint-cli 0.31.1](https://github.com/igorshubovych/markdownlint-cli/releases/tag/v0.31.1) | node:18.4.0-bullseye       | 0.31.1           | ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/swissgrc/azure-pipelines-markdownlint/0.31.1?style=flat-square)   |
| 0.32.0   | [markdownlint-cli 0.32.0](https://github.com/igorshubovych/markdownlint-cli/releases/tag/v0.32.0) | node:18.6.0-bullseye       | 0.32.0           | ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/swissgrc/azure-pipelines-markdownlint/0.32.0?style=flat-square)   |
| 0.32.1   | [markdownlint-cli 0.32.1](https://github.com/igorshubovych/markdownlint-cli/releases/tag/v0.32.1) | node:18.6.0-bullseye       | 0.32.1           | ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/swissgrc/azure-pipelines-markdownlint/0.32.1?style=flat-square)   |
| 0.32.2   | [markdownlint-cli 0.32.2](https://github.com/igorshubovych/markdownlint-cli/releases/tag/v0.32.1) | node:18.7.0-bullseye       | 0.32.2           | ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/swissgrc/azure-pipelines-markdownlint/0.32.2?style=flat-square)   |
| 0.33.0   | [markdownlint-cli 0.33.0](https://github.com/igorshubovych/markdownlint-cli/releases/tag/v0.33.0) | node:18.13.0-bullseye      | 0.33.0           | ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/swissgrc/azure-pipelines-markdownlint/0.33.0?style=flat-square)   |
| 0.34.0   | [markdownlint-cli 0.34.0](https://github.com/igorshubovych/markdownlint-cli/releases/tag/v0.34.0) | node:20.0.0-bullseye-slim  | 0.34.0           | ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/swissgrc/azure-pipelines-markdownlint/0.34.0?style=flat-square)   |
| 0.35.0   | [markdownlint-cli 0.35.0](https://github.com/igorshubovych/markdownlint-cli/releases/tag/v0.35.0) | node:20.3.0-bullseye-slim  | 0.35.0           | ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/swissgrc/azure-pipelines-markdownlint/0.35.0?style=flat-square)   |
| 0.36.0   | [markdownlint-cli 0.36.0](https://github.com/igorshubovych/markdownlint-cli/releases/tag/v0.36.0) | node:20.5.1-bookworm-slim  | 0.36.0           | ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/swissgrc/azure-pipelines-markdownlint/0.36.0?style=flat-square)   |
| 0.37.0   | [markdownlint-cli 0.37.0](https://github.com/igorshubovych/markdownlint-cli/releases/tag/v0.37.0) | node:20.7.0-bookworm-slim  | 0.37.0           | ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/swissgrc/azure-pipelines-markdownlint/0.37.0?style=flat-square)   |
| 0.38.0   | [markdownlint-cli 0.38.0](https://github.com/igorshubovych/markdownlint-cli/releases/tag/v0.38.0) | node:20.10.0-bookworm-slim | 0.38.0           | ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/swissgrc/azure-pipelines-markdownlint/0.38.0?style=flat-square)   |
| 0.39.0   | [markdownlint-cli 0.39.0](https://github.com/igorshubovych/markdownlint-cli/releases/tag/v0.39.0) | node:20.11.0-bookworm-slim | 0.39.0           | ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/swissgrc/azure-pipelines-markdownlint/0.39.0?style=flat-square)   |
| 0.40.0   | [markdownlint-cli 0.40.0](https://github.com/igorshubovych/markdownlint-cli/releases/tag/v0.40.0) | node:20.12.2-bookworm-slim | 0.40.0           | ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/swissgrc/azure-pipelines-markdownlint/0.40.0?style=flat-square)   |
| 0.41.0   | [markdownlint-cli 0.41.0](https://github.com/igorshubovych/markdownlint-cli/releases/tag/v0.41.0) | node:20.13.1-bookworm-slim | 0.41.0           | ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/swissgrc/azure-pipelines-markdownlint/0.41.0?style=flat-square)   |
| 0.42.0   | [markdownlint-cli 0.42.0](https://github.com/igorshubovych/markdownlint-cli/releases/tag/v0.42.0) | node:20.17.0-bookworm-slim | 0.42.0           | ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/swissgrc/azure-pipelines-markdownlint/0.42.0?style=flat-square)   |
| 0.43.0   | [markdownlint-cli 0.43.0](https://github.com/igorshubovych/markdownlint-cli/releases/tag/v0.42.0) | node:22.11.0-bookworm-slim | 0.43.0           | ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/swissgrc/azure-pipelines-markdownlint/0.43.0?style=flat-square)   |
<!-- markdownlint-restore -->

[markdownlint]: https://github.com/igorshubovych/markdownlint-cli
[Azure Pipelines container jobs]: https://docs.microsoft.com/en-us/azure/devops/pipelines/process/container-phases
