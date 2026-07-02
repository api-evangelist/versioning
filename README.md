# Versioning (versioning)
An index and topic collection covering API versioning patterns, schema evolution, and breaking-change detection across the API lifecycle. API versioning communicates change to consumers, while schema versioning and diff tooling makes those changes explicit, reviewable, and reversible. This collection brings together versioning approaches like SemVer and CalVer, registry-driven schema evolution platforms (Apollo, Buf, Apicurio, Confluent Schema Registry), spec-diff tools (oasdiff, Optic, Bump.sh, GraphQL Inspector), API documentation versioning (Stoplight, Scalar, Bump.sh), versioning headers and sunsetting practices (Stripe API Versioning, Sunset Header), and dependency-versioning automation (Dependabot, Renovate, Conventional Commits).

**URL:** [https://apievangelist.com](https://apievangelist.com)

## Tags:

 - API Versioning, SemVer, CalVer, Schema Evolution, Breaking Change, Deprecation, Schema Registry, Spec Diff, Conventional Commits, Sunset Header

## Timestamps

- **Created:** 2026-05-19
- **Modified:** 2026-05-19

## Common Properties

- [Portal](https://apievangelist.com)
- [GitHubOrganization](https://github.com/api-evangelist)
- [JSONSchema - API Version Schema](https://raw.githubusercontent.com/api-evangelist/versioning/refs/heads/main/json-schema/versioning-api-version-schema.json)
- [JSONSchema - Breaking Change Schema](https://raw.githubusercontent.com/api-evangelist/versioning/refs/heads/main/json-schema/versioning-breaking-change-schema.json)
- [JSON-LD](https://raw.githubusercontent.com/api-evangelist/versioning/refs/heads/main/json-ld/versioning-context.jsonld)
- [Vocabulary](https://raw.githubusercontent.com/api-evangelist/versioning/refs/heads/main/vocabulary/versioning-vocabulary.yaml)

## Features

| Name | Description |
|------|-------------|
| Semantic and Calendar Versioning | Established conventions like SemVer (MAJOR.MINOR.PATCH) and CalVer (YYYY.MM) give API and library producers a shared vocabulary for communicating compatibility and release cadence. |
| Breaking Change Detection | Spec-diff tools like oasdiff, openapi-diff, Optic, and GraphQL Inspector compare two versions of an API specification and classify changes as breaking, non-breaking, or unclassified. |
| Schema Registries and Evolution | Platforms like Apicurio, Confluent Schema Registry, Buf Schema Registry, and Apollo GraphOS track every version of a schema and enforce compatibility rules. |
| API Version Headers and Date-Based Versioning | Providers like Stripe and GitHub pin requests to a version via a header or date string, allowing the platform to ship new behavior without breaking existing integrations. |
| Deprecation and Sunsetting | The Deprecation and Sunset HTTP headers (RFC 8594 / RFC 9745) and platform-level deprecation policies give consumers structured advance notice. |
| Documentation and Changelog Versioning | Tools like Bump.sh, Stoplight, Scalar, LaunchNotes, and Keep a Changelog publish per-version API references and human-readable release notes. |
| Conventional Commits and Release Automation | Conventional Commits encodes change type directly in commit messages so SemVer bumps and changelogs can be generated automatically. |
| Dependency Version Management | Bots like Dependabot and Renovate continuously open pull requests to upgrade dependencies, respecting SemVer ranges and surfacing breaking changes. |

## Use Cases

| Name | Description |
|------|-------------|
| Pre-Merge Breaking Change Gate | Run oasdiff or Optic in CI on every pull request that touches the OpenAPI spec and block the merge if breaking changes are introduced without a major version bump. |
| Date-Pinned API Versions | Issue per-account or per-request API versions (e.g. Stripe's 2024-04-10 versioning) so customer integrations remain stable while the platform iterates behind the scenes. |
| Schema Registry Compatibility Enforcement | Producers and consumers of Kafka, gRPC, or GraphQL schemas register every revision in Apicurio, Confluent, Buf, or Apollo and the registry refuses incompatible changes. |
| Multi-Version API Documentation | Publish v1, v2, and v3 documentation simultaneously through Bump.sh, Stoplight, or Scalar so consumers on older versions still have authoritative reference material. |
| Deprecation and Sunset Notification | Emit Deprecation and Sunset HTTP headers from deprecated endpoints, then track consumer migration through analytics before fully removing the version. |
| Automated SemVer Release | Use Conventional Commits plus tools like semantic-release to compute the next SemVer version, generate a changelog, tag the repo, and publish a release from commit history. |
| Continuous Dependency Upgrades | Configure Dependabot or Renovate to open weekly PRs for dependency upgrades, with SemVer-aware grouping and automatic merge for non-breaking patches. |
| API Changelog and Release Notes | Publish a structured changelog through LaunchNotes, Beamer, or Keep a Changelog conventions so consumers can review what changed in every API release. |

## Integrations

| Name | Description |
|------|-------------|
| Oasdiff | Open-source CLI and library that compares two OpenAPI specifications and classifies every change as breaking or non-breaking. |
| Optic | API change-management platform that captures real traffic, generates OpenAPI, and gates pull requests on breaking changes. |
| Bump.sh | API documentation and changelog platform that publishes per-version OpenAPI and AsyncAPI references and surfaces diffs between releases. |
| Buf | Buf Schema Registry and CLI for Protocol Buffers, with first-class breaking-change detection and lint rules across proto versions. |
| Apollo GraphQL | Apollo GraphOS schema registry and Apollo Studio check every proposed GraphQL schema change against operations from real clients. |
| Apicurio | Open-source schema registry from Red Hat for Avro, JSON Schema, OpenAPI, AsyncAPI, and Protobuf, with pluggable compatibility rules. |
| Stripe | Stripe's date-based API versioning model pins every integration to a release date and provides a Versioning Stripe API reference for upgrading. |
| Dependabot | GitHub-native dependency-update automation that opens PRs for upgrades, respecting SemVer ranges and security advisories. |
| Renovate | Configurable dependency upgrade bot with SemVer-aware grouping, scheduling, and automerge across npm, Maven, Docker, and many other ecosystems. |
| Sunset Header | Standard HTTP response header (RFC 8594) for communicating the date at which a resource will become unavailable, used together with Deprecation (RFC 9745). |

## Artifacts

Machine-readable API specifications organized by format.

### JSON Schema

- [API Version Schema](json-schema/versioning-api-version-schema.json)
- [Breaking Change Schema](json-schema/versioning-breaking-change-schema.json)

### JSON Structure

- [API Version Structure](json-structure/versioning-api-version-structure.json)
- [Breaking Change Structure](json-structure/versioning-breaking-change-structure.json)

### JSON-LD

- [Versioning Context](json-ld/versioning-context.jsonld)

## Vocabulary

- [Versioning Vocabulary](vocabulary/versioning-vocabulary.yaml) — Unified taxonomy mapping resources, actions, workflows, and personas across API versioning, schema evolution, breaking-change detection, and deprecation.

## Network

This index references the following API versioning, schema evolution, and breaking-change tooling repositories:

- [Apicurio](https://github.com/api-evangelist/apicurio)
- [Apollo GraphQL](https://github.com/api-evangelist/apollo-graphql)
- [Axway](https://github.com/api-evangelist/axway)
- [Beamer](https://github.com/api-evangelist/beamer)
- [Buf](https://github.com/api-evangelist/buf)
- [Bump.sh](https://github.com/api-evangelist/bump-sh)
- [Changelog](https://github.com/api-evangelist/changelog)
- [CHANGELOG.md (Keep a Changelog)](https://github.com/api-evangelist/changelog-md)
- [Confluent](https://github.com/api-evangelist/confluent-the-data-streaming-platform)
- [Dapr](https://github.com/api-evangelist/dapr)
- [Dependabot.yml](https://github.com/api-evangelist/dependabot-yml)
- [GitHub](https://github.com/api-evangelist/github)
- [GitLab](https://github.com/api-evangelist/gitlab)
- [LaunchNotes](https://github.com/api-evangelist/launchnotes)
- [Liblab](https://github.com/api-evangelist/liblab)
- [Oasdiff](https://github.com/api-evangelist/oasdiff)
- [Optic](https://github.com/api-evangelist/optic)
- [Redpanda](https://github.com/api-evangelist/redpanda)
- [Renovate](https://github.com/api-evangelist/renovate-json)
- [Scalar](https://github.com/api-evangelist/scalar)
- [Schema Evolution](https://github.com/api-evangelist/schema-evolution)
- [Sentry](https://github.com/api-evangelist/sentry)
- [Spectral](https://github.com/api-evangelist/spectral)
- [Stoplight](https://github.com/api-evangelist/stoplight)
- [Stripe](https://github.com/api-evangelist/stripe)
- [Sunset Header](https://github.com/api-evangelist/sunset-header)
- [Versioning Protocols](https://github.com/api-evangelist/versioning-protocols)

## Maintainers

**FN:** Kin Lane

**Email:** kin@apievangelist.com
