# Changelog

Notable changes of this fork (`artemeey/php-openapi`). Upstream history is not repeated here — see
[cebe/php-openapi releases](https://github.com/cebe/php-openapi/releases).

Versions follow [semver](https://semver.org/): patch releases carry bug and PHP compatibility fixes,
minor releases add features, major releases may break the API. The `cebe\openapi\*` namespace is the
same as upstream, so switching between the fork and `cebe/php-openapi` needs no code changes.

## 1.8.1 — 2026-11-25

First release of the fork; based on upstream `893ab10` (one commit after the `1.8.0` tag).

### Fixed

- PHP 8.4/8.5 deprecation notices: implicit nullable parameter types are now explicit
  (`?Type $x = null`) in `SpecObjectInterface`, `SpecBaseObject`, `spec\Callback`, `spec\PathItem`,
  `spec\Paths`, `spec\Responses` and `spec\Reference` (`__construct()`, `resolve()`,
  `resolveReferences()`). Accepted arguments and behaviour are unchanged, so the fix is not a BC break.
  Upstream patch: [cebe/php-openapi#259](https://github.com/cebe/php-openapi/pull/259).

### Changed

- Package renamed from `cebe/php-openapi` to `artemeey/php-openapi` for publishing on Packagist.
  Drop-in replacement: same namespace, same public API, only the Composer package name differs.
