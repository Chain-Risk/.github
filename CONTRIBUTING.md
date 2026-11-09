# Contributing to Chain-Risk

Thank you for helping improve Chain-Risk projects. We build open-source tools for
software supply-chain security and dependency risk analysis. Contributions are
expected to meet a high standard of correctness, reviewability, and security.

By participating, you agree to follow this guide and our
[Code of Conduct](CODE_OF_CONDUCT.md).

## 1. Before you start

- Search existing issues and pull requests before opening a new one.
- For substantial changes, open an issue or design discussion first.
- Keep changes focused. Separate refactoring from behavior changes where practical.
- Never include credentials, tokens, private keys, customer data, or real secrets
  in issues, pull requests, tests, fixtures, logs, or commits.
- Do not publish details of a suspected vulnerability in a public issue. Follow
  [SECURITY.md](SECURITY.md).

For repository-specific build, test, architecture, and release instructions, read
that repository's README and developer documentation. Repository-specific
instructions take precedence where they add detail, but may not weaken the
organization-wide security requirements without an explicit maintainer decision.

## 2. Required commit standards: signed commits and DCO

Every commit proposed for merging must satisfy **both** requirements:

1. **Cryptographic signature:** Each commit must be signed using a GitHub-supported
   signing method (SSH, GPG, or S/MIME) and display as **Verified** on GitHub.
2. **DCO sign-off:** Each commit must contain a `Signed-off-by` trailer identifying
   the contributor and attesting to the Developer Certificate of Origin.

These are separate controls. A `Signed-off-by` line is not a cryptographic
signature, and a cryptographic signature does not replace DCO sign-off.

Use both flags when creating commits:

```bash
git commit -s -S -m "type: describe the change"
```

For a multi-commit pull request, every commit must be signed and DCO-signed.
If you need to amend a commit, preserve both requirements:

```bash
git commit --amend -s -S
```

Configure a signing key and add its public key to your GitHub account before
submitting work. Follow GitHub's current documentation:
[About commit signature verification](https://docs.github.com/en/authentication/managing-commit-signature-verification/about-commit-signature-verification).

The DCO text is available at:
[Developer Certificate of Origin, Version 1.1](https://developercertificate.org/).

By adding `Signed-off-by: Full Name <email@example.com>`, you certify the DCO
statements for that commit. Use an email address associated with your Git
identity and follow the DCO wording. Do not sign off another person's work unless
you are authorized to make that certification.

**Pull requests containing unsigned or non-DCO-signed commits are not eligible
for merge.** Maintainers may ask you to re-sign/rebase and resubmit them.

## 3. Development workflow

1. Fork the relevant repository and create a focused branch.
2. Read its README, architecture notes, tests, and security guidance.
3. Make the smallest coherent change that solves the problem.
4. Add or update tests for behavior changes and bug fixes.
5. Run the repository's documented checks locally.
6. Review your own diff for secrets, generated files, unrelated edits, and
   accidental changes to permissions, workflows, dependencies, or release logic.
7. Create signed, DCO-signed commits.
8. Open a pull request using the provided template.

Do not commit build outputs, local environment files, credentials, generated
artifacts that the repository does not intentionally track, or unrelated changes.

## 4. Security-sensitive changes

Changes involving authentication, authorization, cryptography, parsing of
untrusted input, SBOM ingestion, dependency resolution, network access, process
execution, filesystem access, CI/CD, release workflows, or secret handling need
especially careful review.

For these changes:

- Explain the threat or failure mode the change addresses.
- Identify trust boundaries and assumptions.
- Validate inputs and handle errors safely.
- Avoid logging secrets or sensitive data.
- Prefer well-maintained, pinned dependencies and least-privilege permissions.
- Include negative tests and malformed-input tests where applicable.
- Document security-relevant behavior and compatibility implications.
- Do not weaken security checks merely to make CI pass.

Never introduce a known vulnerable dependency intentionally. If a dependency
change is necessary, explain why and identify the version/source.

## 5. Tests and quality

Pull requests should:

- Pass the repository's CI checks.
- Include tests for new behavior and regressions.
- Preserve deterministic tests; do not require network services or hosted LLMs
  unless the test is explicitly an integration test and is isolated accordingly.
- Avoid flaky timing, hidden external dependencies, and machine-specific paths.
- Update documentation when user-visible behavior, configuration, or commands
  change.

Do not claim a check passed unless it was actually run. Clearly identify checks
that could not be run locally and why.

## 6. Pull request expectations

A pull request should have:

- A clear problem statement and rationale.
- A concise description of implementation and design trade-offs.
- Tests and validation evidence.
- Documentation updates where needed.
- Security and compatibility impact, including migration notes if applicable.
- No unrelated formatting or refactoring.

Maintainers may request changes, additional tests, or a design discussion.
Review is based on technical merit, project scope, maintainability, and security;
it is not a promise of acceptance or a fixed review timeline.

## 7. Dependency and supply-chain changes

When adding or updating dependencies:

- Prefer established upstream projects and the smallest required dependency set.
- Explain why the dependency is needed and why the selected version is appropriate.
- Check license compatibility and known security advisories.
- Avoid unpinned remote scripts and opaque binary downloads.
- Preserve reproducible module metadata and checksums where the ecosystem supports it.
- Do not vendor or copy code without preserving its license and notices.

## 8. Reporting vulnerabilities

Do not open a public issue or pull request for an undisclosed vulnerability.
Use the private reporting instructions in [SECURITY.md](SECURITY.md).

## 9. Review and merge

All changes require successful required checks and maintainer approval under the
target repository's branch protection rules. Maintainers may request additional
review for high-impact or security-sensitive changes.

Maintainers retain responsibility for merge decisions and release readiness.
Submitting a pull request does not guarantee that it will be merged.

## 10. Questions

For general help, use the project's public issue tracker for reproducible bugs
and feature proposals, or see [SUPPORT.md](SUPPORT.md). Keep security reports
private.
