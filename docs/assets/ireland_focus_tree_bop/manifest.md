# Ireland Focus Tree BOP Achievement Asset Manifest

Asset lane: generated achievement icons only.

This package covers BOP achievements plus BOP/event and flavour achievement hooks not covered by the existing Ireland achievement asset set. No gameplay, localisation, focus, decision, `.gfx`, `.gui`, or spec files were edited.

## Package Paths

- Source PNGs: `docs/assets/ireland_focus_tree_bop/achievements/source_png/`
- Processed PNGs: `docs/assets/ireland_focus_tree_bop/achievements/processed_png/`
- Contact sheet: `docs/assets/ireland_focus_tree_bop/achievements/contact_sheets/ireland_bop_achievement_icons_contact_sheet.png`
- Final DDS files: `gfx/achievements/<achievement_id>{,_grey,_not_eligible}.dds`
- Handoff: `docs/assets/ireland_focus_tree_bop/gfx_handoff.md`

## Processing Notes

- Source mode: generated with Codex built-in `image_gen`.
- Target size: 64x64.
- Achievement alpha pattern: opaque 64x64, matching the existing Ireland achievement package.
- Variant coverage: completed, grey, and not eligible for every icon.
- Not-eligible variants use `.agents/skills/hoi4-feature-assets/assets/achievements/overlay.png`.
- No final icon uses readable text, slogans, real people, real movement emblems, or real state symbols.
- Rejected source: the first `ireland_bop_constitutional_mastery` copy was a wrong photographic port scene and was replaced before processing.
- Rejected source: the first `ireland_focus_tree_cabinet_over_emergency` source had a magenta matte block and was replaced before final processing.

## Icon Entries

| Achievement id | Id status | Source PNG | Processed PNG | Final DDS triplet | Direction |
|---|---|---|---|---|---|
| `ireland_bop_constitutional_mastery` | parent-provided | `achievements/source_png/ireland_bop_constitutional_mastery.png` | `achievements/processed_png/ireland_bop_constitutional_mastery.png` | `gfx/achievements/ireland_bop_constitutional_mastery{,_grey,_not_eligible}.dds` | constitutional book, seal, balance needle |
| `ireland_bop_thread_the_emergency` | parent-provided | `achievements/source_png/ireland_bop_thread_the_emergency.png` | `achievements/processed_png/ireland_bop_thread_the_emergency.png` | `gfx/achievements/ireland_bop_thread_the_emergency{,_grey,_not_eligible}.dds` | signal lamp and emergency cabinet seal |
| `ireland_bop_bargain_without_bases` | parent-provided | `achievements/source_png/ireland_bop_bargain_without_bases.png` | `achievements/processed_png/ireland_bop_bargain_without_bases.png` | `gfx/achievements/ireland_bop_bargain_without_bases{,_grey,_not_eligible}.dds` | coast defence phone and legal clause |
| `ireland_bop_congress_without_clientage` | parent-provided | `achievements/source_png/ireland_bop_congress_without_clientage.png` | `achievements/processed_png/ireland_bop_congress_without_clientage.png` | `gfx/achievements/ireland_bop_congress_without_clientage{,_grey,_not_eligible}.dds` | worker hall table and balance motif |
| `ireland_bop_guard_on_a_leash` | parent-provided | `achievements/source_png/ireland_bop_guard_on_a_leash.png` | `achievements/processed_png/ireland_bop_guard_on_a_leash.png` | `gfx/achievements/ireland_bop_guard_on_a_leash{,_grey,_not_eligible}.dds` | faceless guard sleeve under command chain |
| `ireland_bop_front_over_council` | parent-provided | `achievements/source_png/ireland_bop_front_over_council.png` | `achievements/processed_png/ireland_bop_front_over_council.png` | `gfx/achievements/ireland_bop_front_over_council{,_grey,_not_eligible}.dds` | civilian front table and hidden arms shadow |
| `ireland_bop_restore_civilian_rule` | parent-provided | `achievements/source_png/ireland_bop_restore_civilian_rule.png` | `achievements/processed_png/ireland_bop_restore_civilian_rule.png` | `gfx/achievements/ireland_bop_restore_civilian_rule{,_grey,_not_eligible}.dds` | ballot box returning over emergency seal |
| `ireland_bop_civic_revival_no_capture` | parent-provided | `achievements/source_png/ireland_bop_civic_revival_no_capture.png` | `achievements/processed_png/ireland_bop_civic_revival_no_capture.png` | `gfx/achievements/ireland_bop_civic_revival_no_capture{,_grey,_not_eligible}.dds` | schoolhouse, civic book, balanced seal |
| `ireland_focus_tree_cabinet_over_emergency` | parent-provided addendum | `achievements/source_png/ireland_focus_tree_cabinet_over_emergency.png` | `achievements/processed_png/ireland_focus_tree_cabinet_over_emergency.png` | `gfx/achievements/ireland_focus_tree_cabinet_over_emergency{,_grey,_not_eligible}.dds` | cabinet table, coast light, temporary powers ending |
| `ireland_focus_tree_no_one_commands_the_council` | parent-provided addendum | `achievements/source_png/ireland_focus_tree_no_one_commands_the_council.png` | `achievements/processed_png/ireland_focus_tree_no_one_commands_the_council.png` | `gfx/achievements/ireland_focus_tree_no_one_commands_the_council{,_grey,_not_eligible}.dds` | broken command seal, safehouse key, cut radio |
| `ireland_focus_tree_events_of_the_island` | parent-provided addendum | `achievements/source_png/ireland_focus_tree_events_of_the_island.png` | `achievements/processed_png/ireland_focus_tree_events_of_the_island.png` | `gfx/achievements/ireland_focus_tree_events_of_the_island{,_grey,_not_eligible}.dds` | event cards around island relief |
| `ireland_focus_tree_balanced_authority` | parent-provided addendum | `achievements/source_png/ireland_focus_tree_balanced_authority.png` | `achievements/processed_png/ireland_focus_tree_balanced_authority.png` | `gfx/achievements/ireland_focus_tree_balanced_authority{,_grey,_not_eligible}.dds` | scales, border bridge, civic seal |
| `ireland_focus_tree_flavour_coastwatch_without_scandal` | implemented parent id | `achievements/source_png/ireland_focus_tree_flavour_coastwatch_without_scandal.png` | `achievements/processed_png/ireland_focus_tree_flavour_coastwatch_without_scandal.png` | `gfx/achievements/ireland_focus_tree_flavour_coastwatch_without_scandal{,_grey,_not_eligible}.dds` | coastwatch chain without foreign access scandal |
| `ireland_focus_tree_flavour_schools_without_corruption` | implemented parent id | `achievements/source_png/ireland_focus_tree_flavour_schools_without_corruption.png` | `achievements/processed_png/ireland_focus_tree_flavour_schools_without_corruption.png` | `gfx/achievements/ireland_focus_tree_flavour_schools_without_corruption{,_grey,_not_eligible}.dds` | schools and folklore without corrupted restoration |
| `ireland_focus_tree_flavour_winter_fuel_limited_powers` | implemented parent id | `achievements/source_png/ireland_focus_tree_flavour_winter_fuel_limited_powers.png` | `achievements/processed_png/ireland_focus_tree_flavour_winter_fuel_limited_powers.png` | `gfx/achievements/ireland_focus_tree_flavour_winter_fuel_limited_powers{,_grey,_not_eligible}.dds` | winter fuel pressure with limited Emergency powers |
| `ireland_focus_tree_flavour_safeguards_without_coercion` | implemented parent id | `achievements/source_png/ireland_focus_tree_flavour_safeguards_without_coercion.png` | `achievements/processed_png/ireland_focus_tree_flavour_safeguards_without_coercion.png` | `gfx/achievements/ireland_focus_tree_flavour_safeguards_without_coercion{,_grey,_not_eligible}.dds` | Northern local safeguards without coercion |
| `ireland_focus_tree_flavour_merchant_marine_memory` | implemented parent id | `achievements/source_png/ireland_focus_tree_flavour_merchant_marine_memory.png` | `achievements/processed_png/ireland_focus_tree_flavour_merchant_marine_memory.png` | `gfx/achievements/ireland_focus_tree_flavour_merchant_marine_memory{,_grey,_not_eligible}.dds` | merchant marine memory after strict neutrality |

## Validation

- Source PNGs opened: 17.
- Processed PNGs verified: 51, all 64x64 RGBA with opaque alpha.
- Final DDS files verified: 51, all 64x64 uncompressed 32-bit DDS with the same pixel format header as the existing Ireland achievement DDS files.
- Magenta matte scan: 0 magenta-like pixels in processed PNG variants.
- Contact sheet reviewed after regeneration: no magenta matte cells and no blocked cells.

## Blockers

None for the generated asset package. The five flavour ids were adopted by the parent implementation and registered without renaming DDS triplets.
