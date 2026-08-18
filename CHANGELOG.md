# Changelog

Version history of the specifications and tools published in this repository.
Each specification also carries its own revision table in its final section.

## Unreleased

### Model CR2 — Specification
- Rev 1 (2026-09-01) — initial release, covering Serial API 1.1.

### Model CR2 — Tester / Emulator
- v1.01 — first public release.
- Favicon is now embedded in the file, so the tools have no external dependency and render correctly offline.

### Omni Platform — Specification
- Rev 1 (2026-09-01) — initial public release, covering Serial API 1.1 on the Omni Platform. Written as a companion to the Model CR2 specification, and derived from the internal document *WHILL Control System Protocol Specification for Omni Platform* Rev 6.
- `SetJoystick` (`0x03`), `SetSpeedProfile` (`0x04`), `SetMaxSpeedLevel` (`0x0B`) and `SetSpeedLevel` (`0x0C`) are documented as not supported: their acceleration profile is tuned for a rider being carried and is unsuitable for coordinated translation.
- `SetVelocity` (`0x08`) is documented with the Omni parameter range of −1500 … 1500 on both axes, widened from the Model CR2 so that the platform moves sideways and rotates as fast as it moves forward.


### Repository
- Restructured for publication: everything served from `docs/` via GitHub Pages.
- Laid out per product (`docs/cr2/`) with a product selector at the site root, so further products can be added as sibling directories on the same branch.
