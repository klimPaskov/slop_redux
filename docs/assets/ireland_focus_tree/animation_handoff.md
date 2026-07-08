# Ireland Focus Tree Animation Handoff

Status date: 2026-07-08

Scope: animation-only seal asset status for the Ireland focus tree. No `.gfx`, gameplay, focus, idea, decision, achievement, or localisation files were edited in this pass.

## Summary

| Seal | Status | Notes |
| --- | --- | --- |
| `ireland_emergency_readiness_seal` | Complete existing package | Existing source frames, processed frames, sheet PNG, static PNG, contact PNG, preview GIF, sheet DDS, and static DDS are present. |
| `ireland_foreign_access_pressure_seal` | Complete existing package | Existing source frames, processed frames, sheet PNG, static PNG, contact PNG, preview GIF, sheet DDS, and static DDS are present. |
| `ireland_northern_settlement_seal` | Complete existing package | Existing source frames, processed frames, sheet PNG, static PNG, contact PNG, preview GIF, sheet DDS, and static DDS are present. |
| `ireland_hidden_route_reveal_seal` | Complete existing package | Existing source frames, processed frames, sheet PNG, static PNG, contact PNG, preview GIF, sheet DDS, and static DDS are present. |
| `ireland_atlantic_compact_seal` | Complete | Accepted generated draft frames from the previous handoff, copied them into the workspace, removed the magenta matte, normalized to 64x64 transparent frames, and produced sheet/static PNGs, contact PNG, preview GIF, sheet DDS, and static DDS. |

## Shared Animation Settings

Existing completed seal packages use:

- Frame size: 64x64
- Frame count: 8
- Sheet size: 512x64
- Animation rate planned by briefs: 8 FPS
- Looping: yes
- Alpha: final sheet/static DDS files preserve alpha
- Suggested `.gfx` owner: parent implementation agent

## Existing Seal File Status

### `ireland_emergency_readiness_seal`

- Source frames: `docs/assets/ireland_focus_tree/animations/ireland_emergency_readiness_seal/source_frames/ireland_emergency_readiness_seal_000_source.png` through `_007_source.png`
- Processed frames: `docs/assets/ireland_focus_tree/animations/ireland_emergency_readiness_seal/processed_frames/ireland_emergency_readiness_seal_000.png` through `_007.png`
- Sheet PNG: `docs/assets/ireland_focus_tree/animations/ireland_emergency_readiness_seal/sheets/ireland_emergency_readiness_seal_sheet.png`
- Static PNG: `docs/assets/ireland_focus_tree/animations/ireland_emergency_readiness_seal/sheets/ireland_emergency_readiness_seal_static.png`
- Contact PNG: `docs/assets/ireland_focus_tree/animations/ireland_emergency_readiness_seal/previews/ireland_emergency_readiness_seal_contact.png`
- Preview GIF: `docs/assets/ireland_focus_tree/animations/ireland_emergency_readiness_seal/previews/ireland_emergency_readiness_seal_preview.gif`
- Sheet DDS: `gfx/interface/animated/ireland_emergency_readiness_seal.dds`
- Static DDS: `gfx/interface/animated/ireland_emergency_readiness_seal_static.dds`
- Proposed animated sprite: `GFX_ireland_emergency_readiness_seal`
- Proposed static fallback sprite: `GFX_ireland_emergency_readiness_seal_static`
- Visual review: contact sheet shows distinct drawn states with lighting/detail variation; no simple-shape placeholder or transform-only issue observed from contact inspection.

### `ireland_foreign_access_pressure_seal`

- Source frames: `docs/assets/ireland_focus_tree/animations/ireland_foreign_access_pressure_seal/source_frames/ireland_foreign_access_pressure_seal_000_source.png` through `_007_source.png`
- Processed frames: `docs/assets/ireland_focus_tree/animations/ireland_foreign_access_pressure_seal/processed_frames/ireland_foreign_access_pressure_seal_000.png` through `_007.png`
- Sheet PNG: `docs/assets/ireland_focus_tree/animations/ireland_foreign_access_pressure_seal/sheets/ireland_foreign_access_pressure_seal_sheet.png`
- Static PNG: `docs/assets/ireland_focus_tree/animations/ireland_foreign_access_pressure_seal/sheets/ireland_foreign_access_pressure_seal_static.png`
- Contact PNG: `docs/assets/ireland_focus_tree/animations/ireland_foreign_access_pressure_seal/previews/ireland_foreign_access_pressure_seal_contact.png`
- Preview GIF: `docs/assets/ireland_focus_tree/animations/ireland_foreign_access_pressure_seal/previews/ireland_foreign_access_pressure_seal_preview.gif`
- Sheet DDS: `gfx/interface/animated/ireland_foreign_access_pressure_seal.dds`
- Static DDS: `gfx/interface/animated/ireland_foreign_access_pressure_seal_static.dds`
- Proposed animated sprite: `GFX_ireland_foreign_access_pressure_seal`
- Proposed static fallback sprite: `GFX_ireland_foreign_access_pressure_seal_static`
- Visual review: contact sheet shows distinct drawn states with seal/rim/key detail changes; no simple-shape placeholder or transform-only issue observed from contact inspection.

### `ireland_northern_settlement_seal`

- Source frames: `docs/assets/ireland_focus_tree/animations/ireland_northern_settlement_seal/source_frames/ireland_northern_settlement_seal_000_source.png` through `_007_source.png`
- Processed frames: `docs/assets/ireland_focus_tree/animations/ireland_northern_settlement_seal/processed_frames/ireland_northern_settlement_seal_000.png` through `_007.png`
- Sheet PNG: `docs/assets/ireland_focus_tree/animations/ireland_northern_settlement_seal/sheets/ireland_northern_settlement_seal_sheet.png`
- Static PNG: `docs/assets/ireland_focus_tree/animations/ireland_northern_settlement_seal/sheets/ireland_northern_settlement_seal_static.png`
- Contact PNG: `docs/assets/ireland_focus_tree/animations/ireland_northern_settlement_seal/previews/ireland_northern_settlement_seal_contact.png`
- Preview GIF: `docs/assets/ireland_focus_tree/animations/ireland_northern_settlement_seal/previews/ireland_northern_settlement_seal_preview.gif`
- Sheet DDS: `gfx/interface/animated/ireland_northern_settlement_seal.dds`
- Static DDS: `gfx/interface/animated/ireland_northern_settlement_seal_static.dds`
- Proposed animated sprite: `GFX_ireland_northern_settlement_seal`
- Proposed static fallback sprite: `GFX_ireland_northern_settlement_seal_static`
- Visual review: contact sheet shows distinct drawn states with central settlement/hand/rim light changes; no simple-shape placeholder or transform-only issue observed from contact inspection.

### `ireland_hidden_route_reveal_seal`

- Source frames: `docs/assets/ireland_focus_tree/animations/ireland_hidden_route_reveal_seal/source_frames/ireland_hidden_route_reveal_seal_000_source.png` through `_007_source.png`
- Processed frames: `docs/assets/ireland_focus_tree/animations/ireland_hidden_route_reveal_seal/processed_frames/ireland_hidden_route_reveal_seal_000.png` through `_007.png`
- Sheet PNG: `docs/assets/ireland_focus_tree/animations/ireland_hidden_route_reveal_seal/sheets/ireland_hidden_route_reveal_seal_sheet.png`
- Static PNG: `docs/assets/ireland_focus_tree/animations/ireland_hidden_route_reveal_seal/sheets/ireland_hidden_route_reveal_seal_static.png`
- Contact PNG: `docs/assets/ireland_focus_tree/animations/ireland_hidden_route_reveal_seal/previews/ireland_hidden_route_reveal_seal_contact.png`
- Preview GIF: `docs/assets/ireland_focus_tree/animations/ireland_hidden_route_reveal_seal/previews/ireland_hidden_route_reveal_seal_preview.gif`
- Sheet DDS: `gfx/interface/animated/ireland_hidden_route_reveal_seal.dds`
- Static DDS: `gfx/interface/animated/ireland_hidden_route_reveal_seal_static.dds`
- Proposed animated sprite: `GFX_ireland_hidden_route_reveal_seal`
- Proposed static fallback sprite: `GFX_ireland_hidden_route_reveal_seal_static`
- Visual review: contact sheet shows distinct drawn states with revealed light/central emblem changes; no simple-shape placeholder or transform-only issue observed from contact inspection.

## Atlantic Compact Completed Package

`ireland_atlantic_compact_seal` is complete.

Final workspace outputs:

- Source frames: `docs/assets/ireland_focus_tree/animations/ireland_atlantic_compact_seal/source_frames/ireland_atlantic_compact_seal_000_source.png` through `_007_source.png`
- Processed frames: `docs/assets/ireland_focus_tree/animations/ireland_atlantic_compact_seal/processed_frames/ireland_atlantic_compact_seal_000.png` through `_007.png`
- Sheet PNG: `docs/assets/ireland_focus_tree/animations/ireland_atlantic_compact_seal/sheets/ireland_atlantic_compact_seal_sheet.png`
- Static PNG: `docs/assets/ireland_focus_tree/animations/ireland_atlantic_compact_seal/sheets/ireland_atlantic_compact_seal_static.png`
- Contact PNG: `docs/assets/ireland_focus_tree/animations/ireland_atlantic_compact_seal/previews/ireland_atlantic_compact_seal_contact.png`
- Preview GIF: `docs/assets/ireland_focus_tree/animations/ireland_atlantic_compact_seal/previews/ireland_atlantic_compact_seal_preview.gif`
- Sheet DDS: `gfx/interface/animated/ireland_atlantic_compact_seal.dds`
- Static DDS: `gfx/interface/animated/ireland_atlantic_compact_seal_static.dds`

Atlantic design constraints:

- Concept: Atlantic conference/faction compact seal, not a formable country.
- Target frame size: 64x64
- Frame count: 8
- Sheet size: 512x64
- Animation rate: 8 FPS
- Looping: yes
- Play on show: yes, proposed for parent wiring
- Alpha: processed frames, sheet PNG, static PNG, sheet DDS, and static DDS preserve transparent unused pixels.
- Animated sprite name: `GFX_ireland_atlantic_compact_seal`
- Static fallback sprite name: `GFX_ireland_atlantic_compact_seal_static`
- Final DDS paths expected by parent: `gfx/interface/animated/ireland_atlantic_compact_seal.dds` and `gfx/interface/animated/ireland_atlantic_compact_seal_static.dds`

Accepted generated draft files used as source inputs:

- `C:\Users\klimp\.codex\generated_images\019f42a0-e3b5-71e0-b3de-6d874745b118\ig_0efd2eb565e80dab016a4e7f8b2918819680b29a898902dbd1.png`
- `C:\Users\klimp\.codex\generated_images\019f42a0-e3b5-71e0-b3de-6d874745b118\ig_060e658eeb7cabbe016a4e7fc253b881968618bc904bc18f68.png`
- `C:\Users\klimp\.codex\generated_images\019f42a0-e3b5-71e0-b3de-6d874745b118\ig_0355f173a0101c0c016a4e80035e848193a5002483a19772e4.png`
- `C:\Users\klimp\.codex\generated_images\019f42a0-e3b5-71e0-b3de-6d874745b118\ig_0355f173a0101c0c016a4e804303b881938df1c0cc067bc298.png`
- `C:\Users\klimp\.codex\generated_images\019f42a0-e3b5-71e0-b3de-6d874745b118\ig_0355f173a0101c0c016a4e808117a8819397c1669a779a5eff.png`
- `C:\Users\klimp\.codex\generated_images\019f42a0-e3b5-71e0-b3de-6d874745b118\ig_0355f173a0101c0c016a4e80be2bb881939f65a7339c17ff90.png`
- `C:\Users\klimp\.codex\generated_images\019f42a0-e3b5-71e0-b3de-6d874745b118\ig_0355f173a0101c0c016a4e80f985808193b9c5f7d850358bae.png`
- `C:\Users\klimp\.codex\generated_images\019f42a0-e3b5-71e0-b3de-6d874745b118\ig_0355f173a0101c0c016a4e8133f0548193abeb74eed0bda26e.png`

Draft notes:

- The drafts were accepted because they are distinct generated source frames with a coherent Atlantic conference/faction seal motif: anchor/compass, laurel rim, green-gold metal, and sea-blue light states.
- They were not treated as final art until copied into `source_frames`, magenta matte removed, normalized, resized, assembled, converted to DDS, and visually inspected.
- Frame 001 is a stronger compass-state frame and frame 003 is the peak sea-blue state; both remain within the faction/conference seal concept and do not introduce a formable-country crest, flag, or territorial emblem.
- No draft was rejected. The original draft contact sheet remains only as review evidence at `docs/assets/ireland_focus_tree/animations/ireland_atlantic_compact_seal/previews/draft_review_contact.png`.
- Final visual compliance: one compact symbolic subject, no generated text, no fake checkerboard, no opaque square background in processed outputs, no simple-shape fallback, and no transform-only or recolor-only animation.

## Validation Notes

File-read validation performed with Pillow:

- `gfx/interface/animated/ireland_emergency_readiness_seal.dds`: readable, 512x64, RGBA alpha.
- `gfx/interface/animated/ireland_emergency_readiness_seal_static.dds`: readable, 64x64, RGBA alpha.
- `gfx/interface/animated/ireland_foreign_access_pressure_seal.dds`: readable, 512x64, RGBA alpha.
- `gfx/interface/animated/ireland_foreign_access_pressure_seal_static.dds`: readable, 64x64, RGBA alpha.
- `gfx/interface/animated/ireland_northern_settlement_seal.dds`: readable, 512x64, RGBA alpha.
- `gfx/interface/animated/ireland_northern_settlement_seal_static.dds`: readable, 64x64, RGBA alpha.
- `gfx/interface/animated/ireland_hidden_route_reveal_seal.dds`: readable, 512x64, RGBA alpha.
- `gfx/interface/animated/ireland_hidden_route_reveal_seal_static.dds`: readable, 64x64, RGBA alpha.
- `gfx/interface/animated/ireland_atlantic_compact_seal.dds`: readable, 512x64, RGBA alpha.
- `gfx/interface/animated/ireland_atlantic_compact_seal_static.dds`: readable, 64x64, RGBA alpha.

Preview validation:

- Existing four contact PNGs are present and readable at 384x184 with alpha.
- Existing four preview GIFs are present and readable at 64x64. They are review-only previews and do not carry final DDS alpha.
- Existing four sheet PNGs are present and readable at 512x64 with alpha.
- Existing four static PNGs are present and readable at 64x64 with alpha.
- Atlantic contact PNG is present and readable at 384x184 with alpha.
- Atlantic preview GIF is present and readable at 64x64. It is a review-only preview and does not carry final DDS alpha.
- Atlantic sheet PNG is present and readable at 512x64 with alpha.
- Atlantic static PNG is present and readable at 64x64 with alpha.

Visual inspection:

- Inspected the four existing contact sheets.
- The four existing seals appear to use distinct drawn frame states rather than simple geometry placeholders.
- No obvious transform-only failure was visible from the contact sheets.
- The Atlantic contact sheet was inspected after processing. It shows transparent 64x64 frames with distinct generated source states: calm anchor/compass, rising compass light, stronger gold/blue compact state, peak sea-blue state, and return-to-calm frames.

## Non-Edited Areas

Confirmed for this closeout pass:

- No `.gfx` file was edited.
- No gameplay file was edited.
- No localisation file was edited.
- No focus, idea, decision, achievement, or static icon lane was edited.

Note: repository status outside this handoff may already contain unrelated untracked or modified directories/files. This closeout intentionally only adds `docs/assets/ireland_focus_tree/animation_handoff.md`.
