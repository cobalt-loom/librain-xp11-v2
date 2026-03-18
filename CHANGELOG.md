# Changelog

All timestamps in this file are recorded in local time.

## 2026-03-18 06:56:01 +03:00

- Changed the public project identity to `Librain XP11 v2`.
- Changed plugin metadata to present the branch as an XP11-focused VR plugin.
- Changed the README opening to reflect the current XP11-only, VR-first
  direction and to credit `skiselkov/librain` and `toadlife/librain`
  explicitly.
- Changed the public project description to reflect a renderer that consumes a
  broader weather state than the predecessor, including precipitation, wind,
  temperature, icing, wetness, visibility, and related atmospheric context.
- Changed the branch baseline to a clean forward path built from the current
  `toadlife` fork `master` line rather than continuing inside the older dirty
  local tree.
- Changed the public API in `src/librain.h` to add a generalized override
  interface for externally supplied weather and VR state.
- Changed `src/librain.c` to support override-driven precipitation intensity,
  precipitation type, wind, gusts, ambient temperature, local glass
  temperature, icing ratio, VR mode selection, and precipitation smoothing.
- Changed droplet and thermal behavior inputs to read from the override layer
  when present while preserving the original simulator-driven path as fallback.
- Changed `plugin/plugin.c` to expose override datarefs under
  `librain/override/*` for external control.
- Changed `plugin/plugin.c` to load optional override values from
  `librain.cfg` at plugin startup.
- Changed the long-term packaging direction away from the fork's Windows
  `libacfutils` DLL redist model and toward a self-contained plugin with
  `libacfutils` folded into the final binary.
