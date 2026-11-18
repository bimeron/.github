# Contributing to Bimeron

Thank you for helping improve Bimeron. This guide applies to every repository in the
[Bimeron Network organization](https://github.com/bimeron) unless a repository has its own
`CONTRIBUTING.md`. Build instructions and project-specific rules are in each repository's
README and `docs/` folder.

## Before you start

- **Security issues:** do not open a public issue. Follow the
  [security policy](SECURITY.md).
- **Bugs:** search existing issues first. If nothing matches, open a bug report in the
  repository where the problem appears. If you are not sure whether the problem is in an app or
  in Core, report it in the app's repository.
- **Substantial changes:** open an issue and agree on the approach before you write code. This
  includes new features, new upstream protocols, changes to the `.conf` profile format, the IPC
  protocol or public APIs, and new dependencies.
- **Small fixes** such as typos, broken links or obvious one-line bugs can go straight to a
  pull request.

## Making a change

1. Fork the repository and create a branch from the default branch.
2. Keep each pull request focused on one change.
3. Add or update tests for the behavior you change.
4. Update the documentation when behavior, options or formats change.
5. Run the checks described in the repository's documentation locally, and keep CI passing.

## Commit messages

Use [Conventional Commits](https://www.conventionalcommits.org/):

```text
fix(dns): forward queries over TCP when UDP relay is unavailable
feat: add TUIC v5 profile import
docs: describe kill switch limits on Linux
```

Use the same format for the pull request title.

## Pull requests

- Describe what changes and why, and link the related issue.
- Explain how you tested the change, including the operating system and, for network changes,
  the mode and upstream protocol.
- Do not include real server addresses, keys, passwords or unredacted logs.

A maintainer reviews every pull request. We may ask for changes or close a pull request that
does not fit the project's direction. Agreeing on the approach in an issue first avoids that.

## License

By contributing, you agree that your contribution is licensed under the license of the
repository you contribute to.
