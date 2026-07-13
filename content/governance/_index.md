---
title: Governance
description: Contributors, project graduation, code of conduct, and security stance for the Cytomining community.
showDate: false
showAuthor: false
layout: simple
url: /governance/
aliases:
  - /people/
---

The Cytomining ecosystem is maintained by a distributed community of contributors across academia and industry.

## Contributors

- Browse contributors and maintainers in the [Cytomining GitHub organization](https://github.com/cytomining)
- See organization members directly in the [People directory](https://github.com/orgs/cytomining/people)
- Explore project-level contribution history in each repository's contributors graph

We welcome issues, bug reports, documentation improvements, and pull requests from the broader community.

## Governance

Cytomining uses a lightweight governance model centered on maintainers and public decision-making.
We keep policy concise and transparent.

- **Stewardship:** Repositories are maintained by designated maintainers in the [`Cytomining`](https://github.com/cytomining) organization.
- **Decision-making:** Day-to-day technical decisions happen in public issues, pull requests, and our public [Discord](https://discord.gg/dgEDz6xzfJ).
- **Consensus first:** Maintainers seek rough consensus from active contributors before merging impactful changes.
- **Escalation path:** When consensus is unclear, maintainers make a final call, document rationale, and revisit with new evidence.
- **Scope and ownership:** Changes are reviewed by maintainers closest to the affected project area, as defined by recent commits and other relevant ecosystem initiatives.
- **Openness:** Design direction, roadmap changes, and tradeoffs are discussed in public whenever possible.
- **Evolution:** Governance expectations are updated incrementally as the community and project complexity grow.

This reflects how the organization operates today and is intentionally compact so contributors can understand how decisions get made without navigating a large policy surface.

### Organizational structure

The Cytomining ecosystem currently spans two GitHub organizations with distinct roles.

The [**cytomining**](https://github.com/cytomining) organization hosts production-ready tools that have reached stable APIs, published documentation, test coverage, and community adoption.
Tools here are maintained collaboratively by contributors from the [Way Lab](https://www.waysciencelab.com/) at the University of Colorado Anschutz and the broader image-based profiling community.

The [**WayScience**](https://github.com/WayScience) organization serves as an incubator for next-generation tools under active development.
It is the primary home for roadmap work: tools here are experimental, may have unstable APIs, and have not yet graduated into [`Cytomining`](https://github.com/cytomining).

The two organizations are complementary.
[`WayScience`](https://github.com/WayScience) is where new ideas are prototyped and validated; [`Cytomining`](https://github.com/cytomining) is where they become community infrastructure.
Core production tools ([`Pycytominer`](/tools/pycytominer/), [`CytoTable`](/tools/cytotable/), [`coSMicQC`](/tools/cosmicqc/), [`copairs`](/tools/copairs/), [`DeepProfiler`](/tools/deepprofiler/), [`CytoDataFrame`](/tools/cytodataframe/)) live in [`Cytomining`](https://github.com/cytomining).
Roadmap tools ([`buscar`](/experimental/buscar/), [`OME-arrow`](/experimental/ome-arrow/), [`iceberg-bioimage`](/experimental/iceberg-bioimage/), [`ZEDprofiler`](/experimental/zedprofiler/)) live in [`WayScience`](https://github.com/WayScience) until they are ready to graduate.

### Graduation process

Projects typically begin in the [`WayScience`](https://github.com/WayScience) organization (or other organizations) while APIs, scope, and maintenance practices are evolving.
Once a project demonstrates stable releases, documentation, testing, active maintenance, and value to the broader Cytomining community, maintainers may propose transferring it to the [`Cytomining`](https://github.com/cytomining) organization through maintainer consensus.

A tool is considered ready to migrate from [`WayScience`](https://github.com/WayScience) (or any other repository from other organizations) into [`Cytomining`](https://github.com/cytomining) when it meets the following criteria:

- **Within scope** — the tool must be purpose-built for scientists who perform image-based profiling.
- **Stable API** — no breaking changes anticipated in the near term; a versioned release has been tagged
- **Documentation** — a published documentation site covering installation, usage, and API reference
- **Test coverage** — a CI-passing test suite with meaningful coverage (>80%) of core functionality
- **Publication or preprint** — a citable reference describing the tool's design and validation

## Code of Conduct

Participation in Cytomining spaces is expected to follow the organization-wide Code of Conduct:

- [Cytomining Organization Code of Conduct](https://github.com/cytomining/.github/blob/main/CODE_OF_CONDUCT.md)

All contributors and community members are expected to uphold a respectful, inclusive, and professional environment.

## Security Stance

We take security seriously across our software and community operations.

- [Cytomining Organization Security Policy](https://github.com/cytomining/.github/blob/main/SECURITY.md)
- If you discover a potential vulnerability, please report it responsibly through GitHub security reporting mechanisms where available
- Avoid opening public issues for unpatched security vulnerabilities
- We aim to triage and respond to credible reports quickly and transparently

For repository-specific security guidance, check each project's `SECURITY.md` (when present) and GitHub Security tabs.
