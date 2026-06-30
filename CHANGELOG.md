# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.2.0] - 2026-06-30

### Added

- `set_linked_cel_with` and the `LinkedCelOptions` struct for configuring linked cels.

### Changed

- **Breaking (`tiny-skia` feature):** bumped the optional `tiny-skia` dependency
  from `0.11` to `0.12`. The `Pixels` ⇄ `Pixmap` conversions expose `tiny_skia`
  types in their signatures, so consumers using the `tiny-skia` feature must also
  move to `tiny-skia` 0.12.

### Internal

- Adopted `rustfmt` and enforce formatting in CI.
- Bumped the `criterion` dev-dependency from `0.5` to `0.8` (no effect on downstream users).

## [0.1.0] - 2026-03-26

### Added

- Initial release: read and write Aseprite `.ase`/`.aseprite` files with
  byte-perfect round-trip fidelity. Supports RGBA, grayscale, and indexed color
  modes; normal, group, and tilemap layers; animation tags; slices; user data
  with typed properties; tilesets; and linked cels.
