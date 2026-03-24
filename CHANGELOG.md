# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and this project adheres to [Semantic
Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added

- Added a reusable Node.js CI workflow for the RemNote repositories so shared quality and coverage steps now live in
  one public `robert7/workflows` workflow.

### Fixed

- Fixed reusable workflow validation on GitHub Actions by gating the Codecov upload step through `env.CODECOV_TOKEN`
  instead of referencing `secrets.*` directly inside the step condition.
