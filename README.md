# Core Flows

Reusable GitHub Actions workflows for standardized CI/CD pipelines across multiple projects.

## Available Workflows

### NestJS CI/CD Pipeline (Yarn)

This workflow provides a complete CI/CD pipeline for NestJS applications using Yarn 1.22.22. It supports linting, testing, building, semantic versioning, and Docker image deployment to Amazon ECR.

#### Usage

```yaml
name: On Pull Request

on:
  pull_request:
    branches:
      - main

jobs:
  build-nestjs:
    uses: Stamper-Labs/core-flows/.github/workflows/yarn-nestjs-pipe.yml@main
    with:
      node-version: "20"
      release-mode: false
    secrets: inherit
```