# Ireland BOP Achievement Handoff

## Files changed

- `common/achievements/ireland_focus_tree_achievements.txt`
- `docs/plans/ireland_focus_tree/subagent_handoffs/bop_achievement_worker_handoff.md`

## Achievement ids added

- `ireland_bop_constitutional_mastery`
- `ireland_bop_thread_the_emergency`
- `ireland_bop_bargain_without_bases`
- `ireland_bop_congress_without_clientage`
- `ireland_bop_guard_on_a_leash`
- `ireland_bop_front_over_council`
- `ireland_bop_restore_civilian_rule`
- `ireland_bop_civic_revival_no_capture`

## Gameplay surface changed

Added achievement definitions for the canonical Ireland state-authority BOP package. Each achievement uses the existing Ireland achievement style with a compact `possible` gate and route-specific `happened` conditions.

The new definitions combine route or hidden-route flags with BOP helper triggers and existing mechanic variables:

- BOP helpers: `ire_bop_has_state_authority`, `ire_bop_is_mode_historical_emergency`, `ire_bop_is_mode_commonwealth_cooperation`, `ire_bop_is_mode_labour_republic`, `ire_bop_is_mode_blueshirt_corporate`, `ire_bop_is_mode_republican_underground`, `ire_bop_is_mode_civic_cultural`, `ire_bop_is_mode_emergency_directorate`, `ire_bop_is_stable_institutional`, `ire_bop_is_center_contested`, and `ire_bop_is_pressure_dominant`.
- Variables: `ireland_constitutional_authority`, `ireland_emergency_preparedness`, `ireland_partition_pressure`, and `ireland_foreign_access_pressure`.
- Route and outcome flags: historical neutrality, constitutional opposition, Labour republic, Blueshirt corporatist, IRA republic, civic reveal, directorate reveal, restored civilian rule, permanent security state, corrupted restoration failure, compromised republican network, anti-basing vote, Guard discipline, and Republican front conference flags.

## Before and after behavior

Before this patch, the Ireland achievement file contained general Ireland route achievements but no definitions for the canonical BOP-specific achievement ids.

After this patch, the BOP achievement ids are defined and require concrete route, BOP mode, BOP range, and pressure or authority state. The conditions avoid trivial flag-only unlocks and disqualify captured, security-state, or dependency outcomes where the achievement theme requires institutional control.

## Validation notes

- Checked the new achievement ids are unique within `common/achievements/ireland_focus_tree_achievements.txt`.
- Checked the new definitions only reference BOP helpers already present in `common/scripted_triggers/ireland_bop_triggers.txt`.
- Checked the new conditions do not use unsupported comparison operators.

## Parent resolution

The parent implementation resolved the handoff needs:

- All eight BOP achievement ids have `_NAME` and `_DESC` localisation in `localisation/english/slop_redux_l_english.yml`.
- All eight BOP achievement ids have completed, grey, and not-eligible DDS triplets under `gfx/achievements/`.
- The BOP/event achievement addendum ids and five flavour mastery ids were also registered with matching localisation and DDS triplets.
