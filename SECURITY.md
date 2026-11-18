# Security policy

Bimeron handles network traffic and access credentials, so we treat security reports as a
priority. This policy applies to every repository in the
[Bimeron Network organization](https://github.com/bimeron) unless a repository has its own
`SECURITY.md`.

## Supported versions

All Bimeron releases are currently pre-releases. Security fixes go into the default branch and
the next release of the affected project. Older pre-releases do not receive backported fixes, so
update to the latest release before reporting a problem you found in an older one.

| Project | Supported |
| --- | --- |
| Bimeron Core | Latest release and the default branch |
| Bimeron Desktop | Latest release and the default branch |
| Bimeron Android | Default branch (no releases yet) |
| Bimeron Apple | Default branch (no releases yet) |

## Reporting a vulnerability

Do not report security vulnerabilities in public issues, pull requests or discussions.

Report them privately through GitHub:

1. Open the affected repository, for example
   [bimeron-core](https://github.com/bimeron/bimeron-core).
2. Go to **Security** → **Report a vulnerability**.
3. Describe the issue and submit the private report.

If you are not sure which repository is affected, report it in
[bimeron-core](https://github.com/bimeron/bimeron-core/security/advisories/new).

A useful report includes:

- the affected project, version or commit, and operating system;
- the profile mode (system VPN or SOCKS5 proxy) and the upstream protocol, if relevant;
- steps to reproduce, or a proof of concept;
- the impact you expect, for example a traffic or DNS leak, a kill switch bypass, privilege
  escalation through the Core service, or credential exposure.

Remove real server addresses, keys and passwords from profiles, logs and screenshots before you
attach them.

## What to expect

- We aim to acknowledge a report within 5 business days.
- We will confirm the issue, agree on a fix and a disclosure date with you, and keep you
  updated while we work on it.
- After the fix is released, we publish a GitHub security advisory. We credit you in it unless
  you ask us not to.

Please give us a reasonable time to release a fix before you disclose the issue publicly.

## Scope

In scope: code and release packages published in the Bimeron Network organization.

Out of scope: third-party VPN or proxy servers, the security of a particular upstream protocol
itself, and problems that require an already compromised device or administrator access that
an attacker could use directly.
