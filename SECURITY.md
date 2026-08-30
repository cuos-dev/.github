# Security Policy

## Reporting a vulnerability

**Please do not open a public issue for a security problem.**

Report it through **GitHub's private vulnerability reporting**: go to the
affected repository, open the *Security* tab, and choose *Report a
vulnerability*. That keeps the report private to you and the maintainers until
a fix is available, and gives you a thread to follow it in.

If you cannot use that — no GitHub account, or the repository does not offer
it — email **contact@simonwalz.de** with `CuOS security` in the subject.

Please include:

- which component and version (`cuos version` on a running system, or the tag
  or commit you built from)
- what an attacker can do, and what access they need to start
- steps to reproduce, and any logs — **with credentials removed**

### What happens next

| | |
|---|---|
| We acknowledge the report | within **5 working days** |
| We tell you whether we can reproduce it, and our assessment | within **10 working days** |
| We agree a disclosure date with you | once a fix or a mitigation exists |

If you do not hear from us in that time, please chase us — a missed
notification is more likely than silence on purpose.

We will credit you in the release notes unless you would rather stay anonymous.
We have no bug bounty.

## Which versions get fixes

CuOS is **pre-1.0 and has no long-term support branches**. Security fixes go
into the current release; there are no backports to older tags. If you run a
pinned version, expect to move forward to take a fix.

Every CuOS image reference is pinned by digest and a mismatch is fatal, so
updating means changing the pin deliberately rather than drifting onto a new
image by accident.

## What is in scope

The four repositories of this organisation: the operating system and its update
mechanism (`cuos`), the build tooling (`cuos-release`), the IaC manager, WebUI
and fleet components (`cuos-iac`), and these org-wide files.

Out of scope: vulnerabilities in application containers you run **on** CuOS,
which belong to their own projects; and the consequences of a configuration that
deliberately weakens the system — an unprivileged report that CuOS is insecure
when run with `os_root_password` set to a known value tells us nothing.

## Hardening your own deployment

- Pin images by digest and update deliberately.
- Keep registry credentials out of images and out of `system.json` files you
  share; use the config encryption in `cuos-release`.
- Sign your IaC repository's commits and set `iac_repo_signing_keys`, so a
  device only applies configuration it can verify.
- Give the application container only the privileges it needs.
