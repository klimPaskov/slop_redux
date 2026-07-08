# Ireland Focus Tree BOP Achievement GFX Handoff

Asset lane: generated achievement icons only.

Custom achievement icons use root `gfx/achievements/` files named after the achievement id. No `.gfx` `spriteType` entries are required for these icons.

## Final DDS Paths

Each entry has completed, grey, and not-eligible variants:

```text
gfx/achievements/<achievement_id>.dds
gfx/achievements/<achievement_id>_grey.dds
gfx/achievements/<achievement_id>_not_eligible.dds
```

## Parent-Provided BOP Achievement IDs

- `ireland_bop_constitutional_mastery`
- `ireland_bop_thread_the_emergency`
- `ireland_bop_bargain_without_bases`
- `ireland_bop_congress_without_clientage`
- `ireland_bop_guard_on_a_leash`
- `ireland_bop_front_over_council`
- `ireland_bop_restore_civilian_rule`
- `ireland_bop_civic_revival_no_capture`

## Parent-Provided BOP/Event Achievement IDs

- `ireland_focus_tree_cabinet_over_emergency`
- `ireland_focus_tree_no_one_commands_the_council`
- `ireland_focus_tree_events_of_the_island`
- `ireland_focus_tree_balanced_authority`

## Implemented Flavour Achievement IDs

These stable ids were adopted by the parent implementation and are registered in `common/achievements/ireland_focus_tree_achievements.txt` with matching localisation:

- `ireland_focus_tree_flavour_coastwatch_without_scandal`
- `ireland_focus_tree_flavour_schools_without_corruption`
- `ireland_focus_tree_flavour_winter_fuel_limited_powers`
- `ireland_focus_tree_flavour_safeguards_without_coercion`
- `ireland_focus_tree_flavour_merchant_marine_memory`

## Handoff Notes

- Achievement registry surface: `common/achievements/ireland_focus_tree_achievements.txt`.
- Localisation surface: `localisation/english/slop_redux_l_english.yml`.
- Suggested `.gfx` file: none; achievement icons are resolved by root achievement DDS filenames.
- Source PNGs and processed previews live under `docs/assets/ireland_focus_tree_bop/achievements/`.
- Contact sheet for review: `docs/assets/ireland_focus_tree_bop/achievements/contact_sheets/ireland_bop_achievement_icons_contact_sheet.png`.

No `.gfx` entries are needed for achievement icons. The parent implementation wired all listed achievement ids after this asset pass.
