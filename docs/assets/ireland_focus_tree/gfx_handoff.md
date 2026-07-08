# Ireland Focus Tree GFX Handoff

## Interface File

`interface/ireland_focus_tree.gfx` defines all Ireland sprites used by focuses, ideas, dynamic modifiers, decision categories, decisions, and animated route-state seals. The sprite names and paths are stable wiring targets for the final asset workflow.

## Animated Sprites

The Ireland animated seal package has five frame-based seals. Each has 8 frames, runs at 8 FPS, loops, and has a static fallback sprite:

- `GFX_ireland_emergency_readiness_seal`
- `GFX_ireland_foreign_access_pressure_seal`
- `GFX_ireland_northern_settlement_seal`
- `GFX_ireland_hidden_route_reveal_seal`
- `GFX_ireland_atlantic_compact_seal`

Final framesheets live under `gfx/interface/animated/` with matching `_static` fallback textures. The animation handoff at `docs/assets/ireland_focus_tree/animation_handoff.md` records source frames, processed frames, previews, dimensions, alpha validation, and frame-difference validation.

Final animation must not be a transform-only animation from one still, and it must not be built from simple shapes or diagram placeholders. The Atlantic Compact seal remains a conference or faction concept, not a formable-country emblem.

## Event and Flavour Picture Sprites

Major event generated report/news art has its detailed handoff at `docs/assets/ireland_focus_tree_events/gfx_handoff.md`.

Shared flavour generated report art has its detailed handoff at `docs/assets/ireland_focus_tree_flavour_events/gfx_handoff.md`.

Final DDS files live under `gfx/event_pictures/ireland_focus_tree/`. The event package proposes `GFX_news_ireland_*` and `GFX_report_ireland_*` sprite names; the flavour package proposes `GFX_flavour_report_*` sprite names. The main implementation pass should add sprite definitions to `interface/ireland_focus_tree.gfx` or to the established event-picture `.gfx` file if one has already been created.

## Achievement Icons

Custom achievements use icon files in `gfx/achievements/` with the achievement id as the base filename, plus `_grey` and `_not_eligible` variants. No `.gfx` spriteType is required for custom achievement icons.

## Cosmetic Flags

`IRE_ALL_ISLAND` uses vanilla-sourced Ireland tricolour files copied into the mod under `gfx/flags/`, `gfx/flags/medium/`, and `gfx/flags/small/`. Keep those filenames stable while `set_cosmetic_tag = IRE_ALL_ISLAND` remains wired in the settlement effect.

## Replacement Rules

If final art is replaced later, keep the existing sprite names and filenames stable so gameplay, localisation, achievements, and documentation do not need to change. Replacement art must follow `hoi4-feature-assets`; simple-shape placeholder art is not an accepted fallback.
