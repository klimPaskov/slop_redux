# Ireland Idea Icon Handoff

## Scope

This note covers only the Ireland idea and dynamic modifier icon lane for the Ireland focus tree asset package.

No gameplay, localisation, focus, decision, achievement, animation, flag, `.gfx`, or `.gui` files were edited.

## Source Mode

Source mode: `$imagegen` built-in image generation, using flat `#ff00ff` chroma-key backgrounds for local transparency extraction.

Reference folder inspected before processing:

- `.agents/skills/hoi4-feature-assets/assets/ideas`

Review and QA sheets:

- Generated candidate sheet: `docs/assets/ireland_focus_tree/generated_idea_variants_contact_sheet.png`
- Processed final idea sheet: `docs/assets/ireland_focus_tree/idea_icons_processed_contact_sheet.png`
- Reference sheet: `docs/assets/ireland_focus_tree/idea_reference_contact_sheet.png`
- The earlier placeholder review sheet was removed from the final asset package after the lane was replaced by generated painted icons.

Candidate indices below refer to `generated_idea_variants_contact_sheet.png`. Framed scenic variants, atlases, and unrelated UI-like compositions were rejected.

## Final Icons

| Icon | Sprite name | Selected candidate | Prompt subject | Source PNG | Processed PNG | Final DDS |
| --- | --- | ---: | --- | --- | --- | --- |
| `idea_ireland_shadow_of_civil_war` | `GFX_idea_ireland_shadow_of_civil_war` | 27 | Weapons and sealed envelope over dark green cloth, civil conflict memory | `docs/assets/ireland_focus_tree/source_png/idea_ireland_shadow_of_civil_war_source.png` | `docs/assets/ireland_focus_tree/processed_png/idea_ireland_shadow_of_civil_war.png` | `gfx/interface/ideas/idea_ireland_shadow_of_civil_war.dds` |
| `idea_ireland_economic_war_strain` | `GFX_idea_ireland_economic_war_strain` | 1 | Chain-bound ledger, coins, tariff pressure | `docs/assets/ireland_focus_tree/source_png/idea_ireland_economic_war_strain_source.png` | `docs/assets/ireland_focus_tree/processed_png/idea_ireland_economic_war_strain.png` | `gfx/interface/ideas/idea_ireland_economic_war_strain.dds` |
| `idea_ireland_treaty_ports` | `GFX_idea_ireland_treaty_ports` | 3 | Anchor, harbor key, rope | `docs/assets/ireland_focus_tree/source_png/idea_ireland_treaty_ports_source.png` | `docs/assets/ireland_focus_tree/processed_png/idea_ireland_treaty_ports.png` | `gfx/interface/ideas/idea_ireland_treaty_ports.dds` |
| `idea_ireland_small_army_long_coast` | `GFX_idea_ireland_small_army_long_coast` | 9 | Helmet, rifle, coastal watch post, wave | `docs/assets/ireland_focus_tree/source_png/idea_ireland_small_army_long_coast_source.png` | `docs/assets/ireland_focus_tree/processed_png/idea_ireland_small_army_long_coast.png` | `gfx/interface/ideas/idea_ireland_small_army_long_coast.dds` |
| `idea_ireland_divided_island` | `GFX_idea_ireland_divided_island` | 15 | Cracked stone island tablet | `docs/assets/ireland_focus_tree/source_png/idea_ireland_divided_island_source.png` | `docs/assets/ireland_focus_tree/processed_png/idea_ireland_divided_island.png` | `gfx/interface/ideas/idea_ireland_divided_island.dds` |
| `idea_ireland_trade_dependence` | `GFX_idea_ireland_trade_dependence` | 20 | Suspended shipping crate and dock tag | `docs/assets/ireland_focus_tree/source_png/idea_ireland_trade_dependence_source.png` | `docs/assets/ireland_focus_tree/processed_png/idea_ireland_trade_dependence.png` | `gfx/interface/ideas/idea_ireland_trade_dependence.dds` |
| `idea_ireland_emergency_powers` | `GFX_idea_ireland_emergency_powers` | 24 | Red emergency seal, crossed keys, shuttered apparatus | `docs/assets/ireland_focus_tree/source_png/idea_ireland_emergency_powers_source.png` | `docs/assets/ireland_focus_tree/processed_png/idea_ireland_emergency_powers.png` | `gfx/interface/ideas/idea_ireland_emergency_powers.dds` |
| `idea_ireland_authority` | `GFX_idea_ireland_authority` | 28 | Gavel over harp badge and legal papers | `docs/assets/ireland_focus_tree/source_png/idea_ireland_authority_source.png` | `docs/assets/ireland_focus_tree/processed_png/idea_ireland_authority.png` | `gfx/interface/ideas/idea_ireland_authority.dds` |
| `idea_ireland_partition_pressure` | `GFX_idea_ireland_partition_pressure` | 32 | Border milestone, cracked green shield, wire | `docs/assets/ireland_focus_tree/source_png/idea_ireland_partition_pressure_source.png` | `docs/assets/ireland_focus_tree/processed_png/idea_ireland_partition_pressure.png` | `gfx/interface/ideas/idea_ireland_partition_pressure.dds` |
| `idea_ireland_foreign_access` | `GFX_idea_ireland_foreign_access` | 35 | Guarded harbor gate, lock, diplomatic envelope | `docs/assets/ireland_focus_tree/source_png/idea_ireland_foreign_access_source.png` | `docs/assets/ireland_focus_tree/processed_png/idea_ireland_foreign_access.png` | `gfx/interface/ideas/idea_ireland_foreign_access.dds` |
| `idea_ireland_mechanics` | `GFX_idea_ireland_mechanics` | 37 | Brass and steel cogs around green harp badge | `docs/assets/ireland_focus_tree/source_png/idea_ireland_mechanics_source.png` | `docs/assets/ireland_focus_tree/processed_png/idea_ireland_mechanics.png` | `gfx/interface/ideas/idea_ireland_mechanics.dds` |

## Processing

Processing steps:

- Copied selected `$imagegen` outputs from `C:/Users/klimp/.codex/generated_images/` into `docs/assets/ireland_focus_tree/source_png/`.
- Removed the `#ff00ff` chroma-key background with the installed `$imagegen` chroma-key helper.
- Cropped each extracted subject to its visible alpha bounds.
- Normalized each icon to a transparent 64x64 RGBA PNG with centered subject and padding.
- Exported each final DDS through Pillow because `magick`, `texconv`, and `nvdxt` were unavailable on PATH.

## Validation Evidence

All 11 final processed PNGs and all 11 final DDS files reload successfully as 64x64 RGBA assets. All processed PNG corner alpha values are zero.

| Icon | Processed size | DDS size | Max corner alpha | Visible alpha pixels |
| --- | --- | --- | ---: | ---: |
| `idea_ireland_shadow_of_civil_war` | 64x64 RGBA | 64x64 RGBA | 0 | 1886 |
| `idea_ireland_economic_war_strain` | 64x64 RGBA | 64x64 RGBA | 0 | 1820 |
| `idea_ireland_treaty_ports` | 64x64 RGBA | 64x64 RGBA | 0 | 1116 |
| `idea_ireland_small_army_long_coast` | 64x64 RGBA | 64x64 RGBA | 0 | 1490 |
| `idea_ireland_divided_island` | 64x64 RGBA | 64x64 RGBA | 0 | 1151 |
| `idea_ireland_trade_dependence` | 64x64 RGBA | 64x64 RGBA | 0 | 896 |
| `idea_ireland_emergency_powers` | 64x64 RGBA | 64x64 RGBA | 0 | 1653 |
| `idea_ireland_authority` | 64x64 RGBA | 64x64 RGBA | 0 | 1766 |
| `idea_ireland_partition_pressure` | 64x64 RGBA | 64x64 RGBA | 0 | 1550 |
| `idea_ireland_foreign_access` | 64x64 RGBA | 64x64 RGBA | 0 | 1986 |
| `idea_ireland_mechanics` | 64x64 RGBA | 64x64 RGBA | 0 | 1863 |

## Blockers

No remaining blockers in this lane.

Conversion note: external DDS tools were unavailable, so final DDS files were exported with Pillow as requested by the continuation prompt.
