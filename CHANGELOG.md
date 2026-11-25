# Changelog

Notable changes of this fork (`artemeey/php-openapi`). Upstream history is not duplicated here —
see [cebe/php-openapi releases](https://github.com/cebe/php-openapi/releases).

Versions follow [semver](https://semver.org/): patch releases carry bug and PHP compatibility fixes,
minor releases add features, major releases may break API. The PHP namespace (`cebe\openapi\*`) stays
the same as upstream, so switching between the fork and `cebe/php-openapi` needs no code changes.

## 1.8.1 — 2026-11-25

Based on `cebe/php-openapi` 1.8.0 (`893ab10`).

### Added

- PHP 8.4/8.5 support: implicit nullable parameter types are now explicit (`?Type $x = null`), which
  removes `E_DEPRECATED` notices on load in `SpecObjectInterface`, `SpecBaseObject`,
  `spec\Callback`, `spec\PathItem`, `spec\Paths`, `spec\Responses` and `spec\Reference`
  (`__construct()`, `resolve()`, `resolveReferences()`). Behaviour and accepted arguments are unchanged.
  Upstream patch: [cebe/php-openapi#259](https://github.com/cebe/php-openapi/pull/259).

### Changed

- Package renamed from `cebe/php-openapi` to `artemeey/php-openapi` for publishing on Packagist.
  This is a drop-in replacement: same namespace, same public API, only the Composer package name differs.
