# Packagist (packagist)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
