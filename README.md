# renovate-configuration

This repository contains a shared Renovate configuration for npm-based projects. It starts from Renovate’s recommended baseline, limits scanning to npm, runs on a weekly cadence, keeps the dependency dashboard available, and favors predictable updates over fast churn by waiting for releases to age, honoring package constraints, limiting pull request volume, and keeping commit messages in semantic-commit form.

Most of the policy lives in package rules instead of bespoke per-project tuning. Runtime, peer, and development dependencies are handled differently, non-major updates are generally grouped, lockfile maintenance stays on, and automerge is reserved for a narrow set of lower-risk cases such as selected trusted packages, some core tooling updates, maintenance work, and security fixes. The result is a conservative default for routine dependency upkeep with a faster path for changes that are usually safe or time-sensitive.
