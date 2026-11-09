# Chain-Risk Governance

## 1. Purpose and principles

Chain-Risk is an evolving open-source initiative building tools for software
supply-chain security, dependency intelligence, and risk analysis.

Our governance aims to be lightweight, transparent, security-conscious, and
appropriate to the project's current size. Governance may evolve as the
organization and contributor community grow.

Our operating principles are:

- Security and user safety take priority over convenience.
- Technical decisions should be explainable and evidence-based.
- Contributions are evaluated on merit, quality, and project direction.
- Maintainers are accountable for review and project stewardship.
- Community participation should be respectful and inclusive.
- Project maturity and authority must be represented honestly.

## 2. Roles

### Organization owners

Organization owners administer GitHub organization settings, repository access,
teams, and organization-level security controls. They are responsible for
ensuring that administrative privileges are limited to trusted people.

### Maintainers

Maintainers are trusted contributors authorized to review and merge changes,
manage issues, coordinate releases, and guide technical direction in assigned
repositories.

Maintainers are expected to:

- Review contributions fairly and consistently.
- Enforce contribution and security policies.
- Protect credentials, signing keys, and privileged access.
- Explain significant technical decisions.
- Disclose relevant conflicts of interest.
- Avoid merging changes they authored without an independent review when
  practical, especially for security-sensitive changes.
- Participate in vulnerability handling on a need-to-know basis.

### Reviewers

Reviewers provide technical feedback and help assess correctness, maintainability,
testing, and security. Reviewers do not automatically have merge authority.

### Contributors

Contributors participate through code, documentation, testing, issue triage,
design feedback, security research, and community support.

Roles are based on demonstrated contribution, trust, and project needs, not
seniority, employer, or affiliation.

## 3. Decision-making

Routine decisions may be made by the maintainers responsible for the affected
repository, with discussion in the relevant issue or pull request.

Significant changes should be proposed publicly before implementation when
practical. Examples include:

- Architecture or public API changes.
- New security-sensitive capabilities or trust boundaries.
- Changes to supported platforms or compatibility guarantees.
- Major dependency or licensing changes.
- Release process changes.
- Changes to governance or contribution requirements.

A proposal should describe the problem, alternatives, security implications,
compatibility impact, and migration plan where relevant.

Maintainers seek consensus and should consider substantive, evidence-based
feedback. If consensus cannot be reached, the responsible maintainers make and
document the decision, including the rationale. Urgent security decisions may
need restricted discussion and expedited action.

## 4. Changes and approvals

Pull requests must follow `CONTRIBUTING.md` and the target repository's rules.
At minimum, changes must pass required CI checks and receive maintainer approval.

Security-sensitive, cryptographic, release, permission, or workflow changes
should receive additional scrutiny. Where practical, an author should not be
the only reviewer of a high-impact change.

Maintainers may request revisions, decline changes outside project scope, or
close inactive proposals with an explanation.

## 5. Becoming a maintainer

Maintainer invitations are based on sustained, high-quality contributions and
demonstrated judgement. Relevant evidence includes:

- Consistent technical contributions and reviews.
- Understanding of project architecture and security model.
- Constructive community participation.
- Responsible handling of confidential security information.
- Reliability and willingness to share maintenance responsibilities.

The existing maintainers or organization owners discuss and approve new
maintainers. Access should be limited to the repositories and permissions
required for the role and reviewed periodically.

## 6. Conflicts of interest

Maintainers and reviewers should disclose material conflicts that could affect
a decision, including employment, financial interests, or close involvement
with a vendor or project under review. A conflicted person may provide facts
but should not be the sole decision-maker.

## 7. Security and incident decisions

Vulnerability reports are handled privately according to `SECURITY.md`.
Information is shared only with people who need it to assess, fix, or coordinate
the issue. Public disclosure timing is coordinated with the reporter where
practicable.

Maintainers may take urgent protective action, including disabling a workflow,
withdrawing an artifact, or restricting access, when needed to protect users.
Such actions should be documented after immediate risk has been addressed.

## 8. Releases and project stewardship

Release authority rests with maintainers designated for the relevant repository.
Releases should be traceable to reviewed source, use protected credentials, and
publish clear version and change information.

The project should avoid making security, support, or compatibility promises
that it cannot operationally meet.

## 9. Changes to this governance

Changes to this document should be proposed through a pull request and reviewed
by organization owners and maintainers. Significant changes should include a
public rationale unless confidentiality is required for security reasons.

## 10. Current state

Chain-Risk is an evolving community. Roles and decision authority are those
currently assigned through the GitHub organization and repository permissions.
This document does not claim foundation affiliation, formal committee status,
or a larger governance structure that has not been established.
