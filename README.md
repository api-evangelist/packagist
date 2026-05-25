# Packagist (packagist)

Packagist is the default package repository for Composer, the PHP dependency manager. It indexes over 454,000 open-source PHP packages — versions, dependencies, maintainers, download statistics, security advisories — and exposes them through a free public HTTP API plus a high-throughput static Composer v2 metadata mirror at `repo.packagist.org`. Packagist is MIT-licensed open source (`composer/packagist` on GitHub) and is operated by the Composer team, with funding from Private Packagist (the commercial hosted/self-hosted sibling product at packagist.com) and infrastructure sponsorships from Bunny.net and Aikido. Together with the Composer CLI, the SemVer library, the SPDX licenses helper, and the Satis static repository generator, Packagist anchors PHP's modern software supply chain.

**URL:** [Visit APIs.json](https://raw.githubusercontent.com/api-evangelist/packagist/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=opensource-packagist&utm_content=repo)

## Tags

- Composer, PHP, Package Registry, Dependency Management, Open Source, Developer Tools, Software Supply Chain, Security Advisories

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## Registry Scale

| Metric | Value |
|---|---|
| Packages | 454,128 |
| Versions | 5,581,369 |
| Installs (since 2012-04-13) | 181,926,268,159 |

Source: [packagist.org/statistics](https://packagist.org/statistics).

## APIs

### Packagist API

The Packagist API exposes the public PHP Composer package registry. Read endpoints (list, search, popular, package detail, Composer v2 metadata, change feed, statistics, security advisories) are anonymous; write endpoints (create-package, edit-package, update-package) authenticate with SAFE or MAIN API tokens via Bearer `username:apiToken`. Static Composer v2 metadata is served from a separate high-throughput mirror at `repo.packagist.org`.

**Human URL:** [https://packagist.org/apidoc](https://packagist.org/apidoc)

**Base URLs:**

- `https://packagist.org` — application API (search, package detail, statistics, security advisories, writes)
- `https://repo.packagist.org` — static Composer v2 metadata mirror

**Operations:**

| Method | Path | Description |
|---|---|---|
| GET | `/packages/list.json` | List packages, optionally filtered by vendor or type |
| GET | `/search.json` | Search packages by name, tag, type |
| GET | `/explore/popular.json` | Top packages by weekly downloads |
| GET | `/packages/{vendor}/{package}.json` | Full package payload (12-hour cache) |
| GET | `/p2/{vendor}/{package}.json` | Composer v2 static metadata (preferred) |
| GET | `/p2/{vendor}/{package}~dev.json` | Composer v2 dev-branch metadata |
| GET | `/packages/{vendor}/{package}/stats.json` | Download statistics |
| GET | `/metadata/changes.json` | 24-hour rolling change feed |
| GET | `/statistics.json` | Registry-wide totals |
| GET | `/api/security-advisories/` | Security advisories for one or more packages |
| POST | `/api/create-package` | Submit a new package (MAIN token) |
| PUT | `/api/packages/{package}` | Edit package URL (MAIN token) |
| POST | `/api/update-package` | Trigger re-crawl (SAFE token) |

**Artifacts:**

- [Documentation](https://packagist.org/apidoc)
- [OpenAPI](openapi/packagist-api-openapi.yml)
- [JSON Schema — Package](json-schema/packagist-package-schema.json)
- [JSON Schema — Security Advisory](json-schema/packagist-security-advisory-schema.json)
- [JSON Structure — Package](json-structure/packagist-package-structure.json)
- [JSON-LD — Context](json-ld/packagist-context.jsonld)
- [Spectral Rules](rules/packagist-rules.yml)
- [Vocabulary](vocabulary/packagist-vocabulary.yml)
- [Example — Search](examples/packagist-search-example.json)
- [Example — Get Package](examples/packagist-get-package-example.json)
- [Example — Security Advisories](examples/packagist-security-advisories-example.json)
- [Naftiko Capability — Package Discovery](capabilities/package-discovery.yaml)
- [Naftiko Capability — Package Publishing](capabilities/package-publishing.yaml)
- [Naftiko Capability — Registry Change Feed](capabilities/registry-change-feed.yaml)
- [Naftiko Capability — Security Advisories](capabilities/security-advisories.yaml)
- [Naftiko Capability — Download Statistics](capabilities/download-statistics.yaml)

## Authentication

Write endpoints accept either bearer auth or `username` + `apiToken` query/POST parameters:

```
Authorization: Bearer <username>:<apiToken>
```

Token classes:

- **SAFE** — readonly + metadata refresh (`update-package` only).
- **MAIN** — full write surface, including `create-package` and `edit-package`.

API tokens are managed under your [Packagist profile](https://packagist.org/profile/).

## Operational Guidance

Packagist publishes operational guidance instead of a fixed RPS rate limit. The defaults that matter:

- **Concurrent requests:** 10 to `packagist.org`, 20 to `repo.packagist.org`.
- **Schedule off-peak:** avoid the top of the hour (`XX:00`) and midnight UTC.
- **Identify yourself:** send a `User-Agent` with a `mailto=` contact.
- **Use HTTP/2:** multiplexing is strongly recommended.
- **Change feed retention:** the `/metadata/changes.json` log is retained for 24 hours — poll within that window.

See [rate-limits/packagist-rate-limits.yml](rate-limits/packagist-rate-limits.yml) for the structured policy.

## Composer Organization

Packagist is the registry half of a wider Composer toolchain. The full open-source family ships under [github.com/composer](https://github.com/composer):

| Repository | Purpose |
|---|---|
| [composer/composer](https://github.com/composer/composer) | The Composer CLI / dependency resolver itself |
| [composer/packagist](https://github.com/composer/packagist) | This registry application (MIT, "not meant for re-use") |
| [composer/satis](https://github.com/composer/satis) | Static Composer repository generator |
| [composer/semver](https://github.com/composer/semver) | SemVer parsing and constraint logic |
| [composer/spdx-licenses](https://github.com/composer/spdx-licenses) | SPDX license list and validation |
| [composer/class-map-generator](https://github.com/composer/class-map-generator) | PHP class-map scanner |
| [composer/ca-bundle](https://github.com/composer/ca-bundle) | System CA bundle locator with Mozilla fallback |
| [composer/api-surface-check](https://github.com/composer/api-surface-check) | GitHub Action detecting public API surface changes |
| [composer/docker](https://github.com/composer/docker) | Official Composer Docker images |
| [composer/getcomposer.org](https://github.com/composer/getcomposer.org) | getcomposer.org website sources |

## Common Properties

- [Portal](https://packagist.org)
- [Documentation — apidoc](https://packagist.org/apidoc)
- [Documentation — Composer](https://getcomposer.org/doc/)
- [About](https://packagist.org/about)
- [Statistics](https://packagist.org/statistics)
- [GitHubOrganization](https://github.com/composer)
- [GitHubRepository — composer/packagist](https://github.com/composer/packagist)
- [GitHubRepository — composer/composer](https://github.com/composer/composer)
- [GitHubRepository — composer/satis](https://github.com/composer/satis)
- [License — MIT](https://github.com/composer/packagist/blob/main/LICENSE)
- [SignUp](https://packagist.org/register/)
- [Login](https://packagist.org/login/)
- [APIKeys — Profile](https://packagist.org/profile/)
- [Blog](https://blog.packagist.com/)
- [Forum — Discussions](https://github.com/composer/packagist/discussions)
- [Issues](https://github.com/composer/packagist/issues)
- [Mirrors](https://packagist.org/mirrors)
- [SecurityAdvisories — Endpoint](https://packagist.org/apidoc#list-security-advisories)
- [SecurityAdvisories — FriendsOfPHP](https://github.com/FriendsOfPHP/security-advisories)
- [Sandbox — Private Packagist (commercial)](https://packagist.com)
- [Plans / Pricing](plans/packagist-plans-pricing.yml)
- [Rate Limits](rate-limits/packagist-rate-limits.yml)

## Pricing

Packagist.org itself is free. The commercial sibling **Private Packagist** is offered as Cloud and Self-Hosted:

| Plan | Price | Notes |
|---|---|---|
| Packagist.org (Public) | Free | Unlimited public packages |
| Private Packagist Cloud (yearly) | €649/yr | 3 users + 3 suborganizations included |
| Private Packagist Cloud (monthly) | €54.08/mo | Same inclusions |
| Extra user | €15.58/mo | Beyond first 3 |
| Extra suborganization | €15.58/mo | Beyond first 3 |
| Self-Hosted | Contact sales | Air-gapped / on-prem |

A 14-day free trial and a 25% solo-user / non-profit discount are available. See [plans/packagist-plans-pricing.yml](plans/packagist-plans-pricing.yml) and [packagist.com/pricing](https://packagist.com/pricing).

## Artifacts

### OpenAPI

- [Packagist API](openapi/packagist-api-openapi.yml)

### JSON Schema

- [Package](json-schema/packagist-package-schema.json)
- [Security Advisory](json-schema/packagist-security-advisory-schema.json)

### JSON Structure

- [Package Structure](json-structure/packagist-package-structure.json)

### JSON-LD

- [Packagist Context](json-ld/packagist-context.jsonld)

### Spectral Rules

- [packagist-rules.yml](rules/packagist-rules.yml)

### Vocabulary

- [packagist-vocabulary.yml](vocabulary/packagist-vocabulary.yml)

### Capabilities (Naftiko)

- [Package Discovery](capabilities/package-discovery.yaml)
- [Package Publishing](capabilities/package-publishing.yaml)
- [Registry Change Feed](capabilities/registry-change-feed.yaml)
- [Security Advisories](capabilities/security-advisories.yaml)
- [Download Statistics](capabilities/download-statistics.yaml)

### Examples

- [Search](examples/packagist-search-example.json)
- [Get Package](examples/packagist-get-package-example.json)
- [Security Advisories](examples/packagist-security-advisories-example.json)

### Commercial artifacts

- [Plans / Pricing](plans/packagist-plans-pricing.yml)
- [Rate Limits](rate-limits/packagist-rate-limits.yml)

## Maintainers

**FN:** Kin Lane

**Email:** info@apievangelist.com
