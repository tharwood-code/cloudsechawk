# Contributing

Contributions that make a module more correct, more reproducible, or safer are welcome.

- **Never commit secrets.** CI runs gitleaks and will reject the PR. If you commit one by
  accident, rotate it first.
- **Keep modules self-contained.** Each one has its own README with prerequisites, a
  start-to-finish command sequence, and a cost/teardown note.
- **Least privilege.** New workflows get their own ServiceAccount and Role; new cloud
  resources get the narrowest IAM policy that works, written in the README.
- **One change per PR** with a sentence on what it fixes or teaches.

Local checks: `pip install pre-commit && pre-commit install`, then `pre-commit run --all-files`.

By contributing you agree your contributions are licensed under the Apache License 2.0.
