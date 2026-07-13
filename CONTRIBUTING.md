# Contributing to OpenActuarial

Contributions are welcome — issues, discussions, and pull requests alike.
This is a small project with a single maintainer, so please read this page
first; it is short and it is enforced by CI.

## Ground rules for changes

1. **Every behavior change needs a test.** Bug fixes add the test that
   would have caught the bug.
2. **Numerical changes need a reference.** Any PR that changes a published
   number — a fitted parameter, a factor, an interval, a projected value —
   must say *why the new number is right*: a citation (paper, textbook,
   regulatory formula), a closed-form derivation, or a cross-check against
   an independent implementation (SciPy, statsmodels, chainladder-python).
   This mirrors how the existing validation suite works; see the
   validation page of the documentation.
3. **Floors are tested, not aspirational.** CI runs the suite at the
   minimum declared dependency versions. If your change needs a newer
   pandas/numpy/scipy feature, raise the floor in `pyproject.toml` and say
   so in the changelog.
4. **Changelog entry required** under the unreleased/next heading,
   written for users, not for git archaeologists.
5. **Style is ruff's opinion** (`ruff check src tests examples`). No
   debates in review.

## Development setup

```bash
git clone https://github.com/OpenActuarial/<package>
cd <package>
pip install -e ".[dev]"
pytest
```

The CI that runs on your PR is the org-wide reusable workflow
(`OpenActuarial/.github`): lint, metadata consistency, the test matrix
(3 OS-Python combinations you can't easily run locally are normal to
fail-fix in the PR), minimum-dependency install, examples, coverage
floor, and a clean wheel install.

## Review and release authority

The maintainer reviews all changes and is the sole release authority;
releases are tag-driven through PyPI Trusted Publishing. If the project
grows additional maintainers, calculation code will require review by
someone other than its author — the CODEOWNERS mechanism is deferred
until there is more than one qualified reviewer, because a rule nobody
can satisfy is worse than none.
