# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and this project adheres to [Semantic
Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Changed

- Updated the reusable Node CI workflow to `actions/checkout@v5` and `actions/setup-node@v5` so GitHub Actions uses
  the Node 24-compatible action runtime while keeping the job's project runtime pinned to Node `20.19.0`.

## [0.1.0] - 2026-03-24

### Added

- Added a reusable Node.js CI workflow for the RemNote repositories so shared quality and coverage steps now live in
  one public `robert7/workflows` workflow.

### Fixed

- Fixed reusable workflow validation on GitHub Actions by gating the Codecov upload step through `env.CODECOV_TOKEN`
  instead of referencing `secrets.*` directly inside the step condition.
