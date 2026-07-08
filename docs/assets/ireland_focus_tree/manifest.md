# Ireland Focus Tree Asset Manifest

## Generated Package

Registered during the Ireland focus tree asset workflow. The current sprite paths are stable wiring targets; final artwork must be generated, sourced, or processed under `hoi4-feature-assets` and must not be simple-shape placeholder art.

- Source PNGs: `docs/assets/ireland_focus_tree/source_png/`
- Processed PNGs: `docs/assets/ireland_focus_tree/processed_png/`
- Focus icon contact sheet: `docs/assets/ireland_focus_tree/focus_icons_contact_sheet.png`
- Focus icon handoff: `docs/assets/ireland_focus_tree/focus_icon_handoff.md`
- Idea icon contact sheet: `docs/assets/ireland_focus_tree/idea_icons_processed_contact_sheet.png`
- Decision icon contact sheet: `docs/assets/ireland_focus_tree/processed_png/ireland_decision_icons_contact_sheet.png`
- Achievement icon contact sheet: `docs/assets/ireland_focus_tree/achievement_icons_contact_sheet.png`
- Animation handoff: `docs/assets/ireland_focus_tree/animation_handoff.md`

Final game assets:

- Focus icons: `gfx/interface/goals/*.dds`
- Ideas and dynamic modifier icons: `gfx/interface/ideas/*.dds`
- Decision icons: `gfx/interface/decisions/*.dds`
- Decision category icons: `gfx/interface/decisions/categories/*.dds`
- Achievement icons: `gfx/achievements/*.dds`, with `_grey.dds` and `_not_eligible.dds` variants
- Animated seal framesheets and static fallbacks: `gfx/interface/animated/ireland_*_seal*.dds`
- All-island cosmetic flag files: `gfx/flags/IRE_ALL_ISLAND_*.tga`, `gfx/flags/medium/IRE_ALL_ISLAND_*.tga`, and `gfx/flags/small/IRE_ALL_ISLAND*.tga`
- Major event generated report/news art: `gfx/event_pictures/ireland_focus_tree/*.dds`, with package manifest at `docs/assets/ireland_focus_tree_events/manifest.md`
- Shared flavour generated report art: `gfx/event_pictures/ireland_focus_tree/*.dds`, with package manifest at `docs/assets/ireland_focus_tree_flavour_events/manifest.md`

Wiring file:

- `interface/ireland_focus_tree.gfx`

## Event and Flavour Art Packages

The Ireland major event and shared flavour report/news art package was generated as final-source period documentary art, not placeholder art.

- Major event package manifest: `docs/assets/ireland_focus_tree_events/manifest.md`
- Major event package handoff: `docs/assets/ireland_focus_tree_events/gfx_handoff.md`
- Major event contact sheet: `docs/assets/ireland_focus_tree_events/contact_sheets/ireland_event_images_contact_sheet.png`
- Flavour report package manifest: `docs/assets/ireland_focus_tree_flavour_events/manifest.md`
- Flavour report package handoff: `docs/assets/ireland_focus_tree_flavour_events/gfx_handoff.md`
- Flavour report contact sheet: `docs/assets/ireland_focus_tree_flavour_events/contact_sheets/ireland_flavour_report_images_contact_sheet.png`

These packages add 7 final news images at `397x153` and 18 final report images at `210x176`. The handoff documents propose sprite names and final DDS paths for the main implementation pass. The generated scenes intentionally avoid readable fake text, real people, real flags/symbols, real documents, and historically attested insignia.

## Icon Coverage

Focus family sprites:

- `GFX_goal_ireland_opening`
- `GFX_goal_ireland_authority`
- `GFX_goal_ireland_constitutional`
- `GFX_goal_ireland_neutrality`
- `GFX_goal_ireland_labour`
- `GFX_goal_ireland_blueshirt`
- `GFX_goal_ireland_ira`
- `GFX_goal_ireland_industry`
- `GFX_goal_ireland_military`
- `GFX_goal_ireland_ports`
- `GFX_goal_ireland_emergency`
- `GFX_goal_ireland_diplomacy`
- `GFX_goal_ireland_foreign_access`
- `GFX_goal_ireland_partition`
- `GFX_goal_ireland_late`
- `GFX_goal_ireland_route_choice`
- `GFX_goal_ireland_support_lanes`
- `GFX_goal_ireland_hidden_civic`
- `GFX_goal_ireland_hidden_directorate`
- `GFX_goal_ireland_hidden_atlantic`
- `GFX_goal_ireland_hidden_common`

Idea sprites:

- `GFX_idea_ireland_shadow_of_civil_war`
- `GFX_idea_ireland_economic_war_strain`
- `GFX_idea_ireland_treaty_ports`
- `GFX_idea_ireland_small_army_long_coast`
- `GFX_idea_ireland_divided_island`
- `GFX_idea_ireland_trade_dependence`
- `GFX_idea_ireland_emergency_powers`
- `GFX_idea_ireland_authority`
- `GFX_idea_ireland_partition_pressure`
- `GFX_idea_ireland_foreign_access`
- `GFX_idea_ireland_mechanics`

Decision category sprites:

- `GFX_decision_category_ireland_authority`
- `GFX_decision_category_ireland_emergency`
- `GFX_decision_category_ireland_ports`
- `GFX_decision_category_ireland_economy`
- `GFX_decision_category_ireland_foreign_access`
- `GFX_decision_category_ireland_partition`
- `GFX_decision_category_ireland_crisis`
- `GFX_decision_category_ireland_integration`

Decision icons are defined for every `GFX_decision_ireland_*` token used by `common/decisions/ireland_focus_tree_decisions.txt`.

Achievement icon production uses painted source icons for every Ireland achievement and writes colour, grey, and not-eligible DDS variants under `gfx/achievements/`. See `docs/assets/ireland_focus_tree/achievement_icon_handoff.md` and `docs/assets/ireland_focus_tree/achievement_icons_contact_sheet.png`.

## Source Notes

The icon filenames and sprite names are stable implementation targets. Any final icon replacement must use generated, sourced, or user-provided artwork under the asset skill; simple shapes, diagrams, geometric stand-ins, and transform-only animations are not acceptable final assets.

The focus icon lane was refreshed from the generated `goal_ireland_<token>_source.png` files. The final focus PNG and DDS outputs preserve the existing Ireland focus package dimensions (`96x96`) and registered sprite paths in `interface/ireland_focus_tree.gfx`; see `docs/assets/ireland_focus_tree/focus_icon_handoff.md` for validation details.

## Animated Seal Entries

The final animated package contains five frame-based seals:

- `ireland_emergency_readiness_seal`
- `ireland_foreign_access_pressure_seal`
- `ireland_northern_settlement_seal`
- `ireland_hidden_route_reveal_seal`
- `ireland_atlantic_compact_seal`

Each seal has source frames, processed frames, a `512x64` DDS framesheet, a `64x64` static DDS fallback, a contact sheet, and a preview GIF. See `docs/assets/ireland_focus_tree/animation_handoff.md` for the full file list and validation notes.

### `ireland_atlantic_compact_seal`

- Related feature slug: `ireland_focus_tree`
- Asset type: animated symbolic route-state seal
- Intended in-game use: Atlantic Compact conference/faction seal for parent-owned Ireland focus tree UI wiring
- Source mode: `$imagegen` draft frames from the previous animation handoff, accepted and processed in this pass
- Source PNGs: `docs/assets/ireland_focus_tree/animations/ireland_atlantic_compact_seal/source_frames/ireland_atlantic_compact_seal_000_source.png` through `_007_source.png`
- Processed PNGs: `docs/assets/ireland_focus_tree/animations/ireland_atlantic_compact_seal/processed_frames/ireland_atlantic_compact_seal_000.png` through `_007.png`
- Sheet PNG: `docs/assets/ireland_focus_tree/animations/ireland_atlantic_compact_seal/sheets/ireland_atlantic_compact_seal_sheet.png`
- Static PNG: `docs/assets/ireland_focus_tree/animations/ireland_atlantic_compact_seal/sheets/ireland_atlantic_compact_seal_static.png`
- Contact sheet: `docs/assets/ireland_focus_tree/animations/ireland_atlantic_compact_seal/previews/ireland_atlantic_compact_seal_contact.png`
- Preview GIF: `docs/assets/ireland_focus_tree/animations/ireland_atlantic_compact_seal/previews/ireland_atlantic_compact_seal_preview.gif`
- Final sheet DDS: `gfx/interface/animated/ireland_atlantic_compact_seal.dds`
- Final static DDS: `gfx/interface/animated/ireland_atlantic_compact_seal_static.dds`
- Target frame size: 64x64
- Frame count: 8
- Sheet size: 512x64
- Frame timing: 8 FPS
- Loop behavior: looping, `play_on_show = yes` proposed
- Anchor point: center
- Animated sprite name: `GFX_ireland_atlantic_compact_seal`
- Static fallback sprite name: `GFX_ireland_atlantic_compact_seal_static`
- Suggested `.gfx` file: `interface/ireland_focus_tree.gfx`
- Notes: Atlantic Compact remains a conference/faction concept, not a formable country. The final frames use transparent unused pixels and distinct generated source states; no transform-only, recolor-only, simple-geometry, or fallback animation was used.
- Asset status: complete

The asset package does not invent leader portraits, slogans, quotes, or audio. Real leader portraits are reused from vanilla character assets. The all-island cosmetic identity uses the vanilla Ireland tricolour copied from `C:/Program Files (x86)/Steam/steamapps/common/Hearts of Iron IV/gfx/flags/IRE_*.tga`, with matching medium and small flag variants, because the accepted source direction preserves the base Irish national flag unless a later sourced route variant is approved.

Unresearched quotes, slogans, cultural remarks, allusions, and audio remain blocked pending the text and audio research workflow.
