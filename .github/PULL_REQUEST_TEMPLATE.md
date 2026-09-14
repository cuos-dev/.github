## What does this change, and why?

<!-- If it fixes an open issue, say "Fixes #123". -->

## How was it verified?

<!--
Say what you actually ran, and what you did not. "Built an rpi-arm64 image and
booted it on a Pi 4" and "reviewed only, not built" are both useful answers;
a checkbox that means neither is not.
-->

## Checklist

- [ ] Every commit is signed off (`git commit -s`) — see [DCO.txt](../DCO.txt).
      CI checks this and will fail the pull request otherwise.
- [ ] New shell scripts carry `# SPDX-License-Identifier: Apache-2.0`.
- [ ] `shellcheck --severity=warning` is clean, and any `*.test.sh` passes.
- [ ] The documentation matches the change — including any command in a README
      that this renames or removes.

<!--
Branch flow: where a repository has a `development` branch, pull requests go
there and not to `main`.
History is kept as it was made: no squashing, and no rebasing of a branch that
has already been pushed. Bring a branch up to date by merging `development`
into it.
-->
