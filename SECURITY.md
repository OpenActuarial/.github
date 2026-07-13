# Security Policy

## Supported versions

Only the **latest release train** of the ecosystem receives fixes: the
newest release of each package, installed together (this is exactly what
the `openactuarial` meta-package pins). Older releases are not patched.

## Reporting a vulnerability

Use **GitHub private vulnerability reporting** on the affected repository
(Security tab -> "Report a vulnerability"). Do not open a public issue for
anything you believe is exploitable — this includes supply-chain concerns
about the release workflows, not just code.

You should get an initial response within a week. Fixes ship as a patch
release of the affected package(s) and, when the fix changes any published
number, a note in the validation documentation.

## Scope notes

- These packages execute no network calls and load no remote code at
  runtime; the main surfaces are input handling and the release pipeline.
- Release workflows use PyPI Trusted Publishing, reusable workflows pinned
  by tag under maintainer control, and third-party actions pinned to
  commit SHAs. Reports about weaknesses in that chain are in scope.
