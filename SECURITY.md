# Security policy

Everything in this repository is meant to be copied into other people's environments, so a
flaw here can propagate. Please report problems privately.

**How:** use GitHub's private vulnerability reporting on this repository (*Security* tab →
*Report a vulnerability*). You'll get an acknowledgement within 5 days and a fix or a
documented decision within 30 days.

**In scope:** any committed code, manifest, module, policy or documentation that recommends
an insecure configuration.

**Out of scope:** vulnerabilities in the third-party tools a module installs or scans
(report those upstream), and issues that require already holding the operator's credentials.

**Hygiene:** no credentials are committed; `.gitignore` excludes env files, tfvars, state and
keys; gitleaks runs in CI on every push and PR and locally via pre-commit.
