# Packagist (packagist)

Packagist is the default package repository for Composer, the PHP dependency manager. It indexes
over 454,000 open-source PHP packages — versions, dependencies, maintainers, download statistics,
security advisories — and exposes them through a free public HTTP API plus a high-throughput static
Composer v2 metadata mirror at repo.packagist.org. Packagist is MIT-licensed open source (composer/packagist
on GitHub) and is operated by the Composer team, with funding from Private Packagist (the commercial
hosted/self-hosted sibling product at packagist.com) and infrastructure sponsorships from Bunny.net
and Aikido. Together with the Composer CLI, the SemVer library, the SPDX licenses helper, and the
Satis static repository generator, Packagist anchors PHP's modern software supply chain.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/packagist/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/packagist/refs/heads/main/apis.yml)

## Scope

- **Position:** Providing
- **Access:** 3rd-Party

## Tags

- Composer
- PHP
- Package Registry
- Dependency Management
- Open Source
- Developer Tools
- Software Supply Chain
- Security Advisories

## Timestamps

- **Created:** 2026-05-25T00:00:00.000Z
- **Modified:** 2026-05-25

## APIs

### Packagist API

The Packagist API exposes the public PHP Composer package registry — over 454,000 packages and
5.58 million versions backing more than 181 billion installs since 2012. Read endpoints (list,
search, popular, package detail, Composer v2 metadata, change feed, statistics, security advisories)
are anonymous; write endpoints (create-package, edit-package, update-package) authenticate with
SAFE or MAIN API tokens via Bearer `username:apiToken`. Static Composer v2 metadata is served from
a separate high-throughput mirror at repo.packagist.org.

- **Human URL:** [https://packagist.org/apidoc](https://packagist.org/apidoc)
- **Base URL:** `https://packagist.org`

#### Tags

- Composer
- PHP
- Packages
- Package Registry
- Dependencies
- Open Source

#### Properties

- [Documentation](https://packagist.org/apidoc)
- [Base U R L](https://repo.packagist.org/)
- [OpenAPI](openapi/packagist-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/packagist-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/packagist-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/packagist-package-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/packagist-security-advisory-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](json-structure/packagist-package-structure.json)
- [JSON-LD](json-ld/packagist-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Spectral Rules](rules/packagist-rules.yml)
- [Vocabulary](vocabulary/packagist-vocabulary.yml)
- [Examples](examples/packagist-search-example.json)
- [Examples](examples/packagist-get-package-example.json)
- [Examples](examples/packagist-security-advisories-example.json)

## Common Properties

- [Portal](https://packagist.org)
- [Documentation](https://packagist.org/apidoc)
- [Documentation](https://getcomposer.org/doc/)
- [About](https://packagist.org/about)
- [Statistics](https://packagist.org/statistics)
- [GitHub Organization](https://github.com/composer)
- [GitHub Repository](https://github.com/composer/packagist)
- [GitHub Repository](https://github.com/composer/composer)
- [GitHub Repository](https://github.com/composer/satis)
- [GitHub Repository](https://github.com/composer/semver)
- [GitHub Repository](https://github.com/composer/spdx-licenses)
- [GitHub Repository](https://github.com/composer/class-map-generator)
- [GitHub Repository](https://github.com/composer/ca-bundle)
- [GitHub Repository](https://github.com/composer/api-surface-check)
- [GitHub Repository](https://github.com/composer/docker)
- [Tool](https://getcomposer.org/)
- [Tool](https://github.com/composer/satis)
- [Documentation](https://getcomposer.org/doc/01-basic-usage.md)
- [Documentation](https://getcomposer.org/doc/04-schema.md)
- [Documentation](https://getcomposer.org/doc/articles/versions.md)
- [Documentation](https://packagist.org/about#how-to-update-packages)
- [Authentication](https://packagist.org/apidoc#authentication)
- [Sign Up](https://packagist.org/register/)
- [Login](https://packagist.org/login/)
- [A P I Keys](https://packagist.org/profile/)
- [Security Advisories](https://packagist.org/apidoc#list-security-advisories)
- [Security Advisories](https://github.com/FriendsOfPHP/security-advisories)
- [Mirror](https://packagist.org/mirrors)
- [Sandbox](https://packagist.com)
- [Privacy Policy](https://packagist.com/privacy)
- [Terms of Service](https://packagist.com/terms-of-service)
- [License](https://github.com/composer/packagist/blob/main/LICENSE)
- [Blog](https://blog.packagist.com/)
- [Forum](https://github.com/composer/packagist/discussions)
- [Issues](https://github.com/composer/packagist/issues)
- [Plans](plans/packagist-plans-pricing.yml)
- [Rate Limits](rate-limits/packagist-rate-limits.yml)
- [Features](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** info@apievangelist.com
**URL:** https://apievangelist.com
