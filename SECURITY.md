# Security Policy

Security is a primary design and maintenance priority for Chain-Risk projects.
We appreciate responsible reports that help protect users and the wider software
supply-chain ecosystem.

## Reporting a vulnerability

**Do not report suspected vulnerabilities in public issues, pull requests,
discussions, or social media.** Public disclosure before a fix is available can
put users at risk.

Preferred method:

1. Open the affected repository on GitHub.
2. Navigate to its **Security** tab.
3. Select **Report a vulnerability** to submit a private vulnerability report
   (GitHub Security Advisory), if private vulnerability reporting is enabled.

If that option is unavailable, do not publish exploit details. Contact the
Chain-Risk organization owners through
https://github.com/Chain-Risk and request a private reporting channel. Include
only enough information to establish contact until a private channel is agreed.

Do not send credentials, personal data, or unrelated sensitive information.

## What to include

A useful report may include:

- Affected repository, product, version, and commit if known.
- Vulnerable component and configuration.
- Preconditions and realistic impact.
- Reproduction steps or a minimal proof of concept.
- Potential mitigations, if known.
- Your preferred contact method and disclosure timeline.

Please avoid destructive testing, accessing data that is not yours, persistence,
or actions that could disrupt services or other users. Stop testing once the
issue is demonstrated.

## What to expect

Maintainers will make reasonable efforts to:

- Acknowledge reports as soon as practicable.
- Confirm whether the report is in scope and request clarification if needed.
- Assess severity, affected versions, and potential impact.
- Coordinate a fix, mitigation, and disclosure with the reporter.
- Credit the reporter where appropriate and with their consent.

Response and remediation times depend on severity, reproducibility, maintainer
availability, and release complexity. We do not promise a fixed response SLA.

Please do not disclose the vulnerability publicly until a coordinated disclosure
plan has been agreed, except where applicable law or an immediate safety need
requires otherwise.

## Scope

Reports are welcome for vulnerabilities in Chain-Risk-maintained code,
build/release workflows, official distribution artifacts, and project-operated
infrastructure.

Third-party dependencies should generally be reported to their respective
maintainers as well. If Chain-Risk's use or configuration creates additional
impact, include that context in the private report.

## Security-sensitive contributions

Changes affecting authentication, authorization, cryptography, parsing,
dependency resolution, SBOM handling, network access, process execution,
filesystem access, CI/CD, release artifacts, or secrets require explicit
security consideration and maintainer review.

## No safe harbour guarantee

This policy describes our preferred reporting process. It does not authorize
testing that violates law, contracts, platform terms, or another party's rights.
