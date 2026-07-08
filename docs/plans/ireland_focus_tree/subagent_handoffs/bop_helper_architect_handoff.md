# Ireland BOP Helper Architect Handoff

## Files changed

- `common/script_constants/ireland_bop_constants.txt`
- `common/scripted_triggers/ireland_bop_triggers.txt`
- `common/scripted_effects/ireland_bop_effects.txt`
- `docs/plans/ireland_focus_tree/subagent_handoffs/bop_helper_architect_handoff.md`

No focus, decision, localisation, interface, event, asset, or `common/bop` files were changed.

## Helper map

Scope for all scripted effects and triggers: country scope, intended for Ireland (`original_tag = IRE`) unless a parent call site deliberately checks a different scope first.

### Mode and lifecycle effects

| Helper | Inputs | Outputs and side effects | Intended call sites |
| --- | --- | --- | --- |
| `ire_bop_initialize_opening_state` | none | Clears BOP mode flags, sets `ire_bop_mode_opening_state`, initializes `IRE_state_authority_bop` with constitutional government left and armed political pressure right at `-0.10`. | Opening trunk focus or Ireland setup hook owned by parent. |
| `ire_bop_set_mode_opening_state` | existing BOP value | Sets opening side pair and clamps extreme inherited value to a moderate cap. | Route failure or recovery back to opening politics. |
| `ire_bop_set_mode_historical_emergency` | existing BOP value | Sets civilian cabinet versus emergency apparatus and clears conflicting mode flags. | Historical emergency route lock. |
| `ire_bop_set_mode_commonwealth_cooperation` | existing BOP value | Sets independent parliamentary review versus defence liaison cabinet and clears conflicting mode flags. | Commonwealth or Fine Gael route lock. |
| `ire_bop_set_mode_labour_republic` | existing BOP value | Sets Dail Labour cabinet versus workers congress and clears conflicting mode flags. | Labour route lock. |
| `ire_bop_set_mode_blueshirt_corporate` | existing BOP value | Sets parliamentary right and chambers versus Blueshirt guard and clears conflicting mode flags. | Blueshirt or corporate route lock. |
| `ire_bop_set_mode_republican_underground` | existing BOP value | Sets civilian republican front versus Army Council and clears conflicting mode flags. | Republican underground route lock. |
| `ire_bop_set_mode_civic_cultural` | existing BOP value | Sets civic institutions versus cultural mobilisation networks and clears conflicting mode flags. | Hidden civic cultural reveal. |
| `ire_bop_set_mode_emergency_directorate` | existing BOP value | Sets civilian restoration versus security directorate and clears conflicting mode flags. | Directorate reveal or crisis entry. |
| `ire_bop_cleanup_invalid_mode` | active side pair or missing BOP state | Rebuilds the mode flag from active sides, initializes opening mode when the BOP has invalid sides, or removes BOP and clears flags when scope is not Ireland. | Route cleanup, annexation cleanup, hidden route exit, war-end cleanup. |

Compatibility aliases are also present for the earlier internal names: `ire_bop_initialize_opening_effect`, `ire_bop_switch_to_*_effect`, `ire_bop_switch_to_commonwealth_effect`, `ire_bop_switch_to_ira_effect`, `ire_bop_switch_to_directorate_effect`, and `ire_bop_cleanup_invalid_mode_effect`.

### Shift effects

All shift helpers are concrete BOP moves using `add_power_balance_value`. Public generic shift magnitudes are small `0.10`, medium `0.16`, and large `0.24`. Left side means the first side in the active mode. Right side means the second side.

Public generic helpers:

- `ire_bop_shift_left_small`
- `ire_bop_shift_left_medium`
- `ire_bop_shift_left_large`
- `ire_bop_shift_right_small`
- `ire_bop_shift_right_medium`
- `ire_bop_shift_right_large`
- `ire_bop_shift_to_center_small`
- `ire_bop_shift_to_center_medium`

The generic left/right helpers do not set `tooltip_side`, because current active side cannot be injected dynamically into that static field without a larger meta-effect/scripted-localisation layer. The side-specific wrappers below set explicit tooltip sides.

Center shifts are feasible only as bounded correction helpers: they move right if the current value is less than `-0.15`, move left if the current value is greater than `0.15`, and do nothing inside the contested center band. They may slightly cross zero if called close to the center edge.

| Helper | Direction | Active mode guard |
| --- | --- | --- |
| `ire_bop_shift_constitutional_government_small` | left, constitutional government | opening |
| `ire_bop_shift_armed_pressure_small` | right, armed political pressure | opening |
| `ire_bop_shift_civilian_cabinet_small` | left, civilian cabinet | historical emergency |
| `ire_bop_shift_emergency_apparatus_small` | right, emergency apparatus | historical emergency |
| `ire_bop_shift_parliamentary_review_small` | left, independent parliamentary review | Commonwealth cooperation |
| `ire_bop_shift_defence_liaison_small` | right, defence liaison cabinet | Commonwealth cooperation |
| `ire_bop_shift_dail_labour_small` | left, Dail Labour cabinet | Labour republic |
| `ire_bop_shift_workers_congress_small` | right, workers congress | Labour republic |
| `ire_bop_shift_chambers_small` | left, parliamentary right and chambers | Blueshirt corporate |
| `ire_bop_shift_blueshirt_guard_small` | right, Blueshirt guard | Blueshirt corporate |
| `ire_bop_shift_republican_front_small` | left, civilian republican front | republican underground |
| `ire_bop_shift_army_council_small` | right, Army Council | republican underground |
| `ire_bop_shift_civic_institutions_small` | left, civic institutions | civic cultural |
| `ire_bop_shift_cultural_mobilisation_small` | right, cultural mobilisation networks | civic cultural |
| `ire_bop_shift_civilian_restoration_small` | left, civilian restoration | emergency directorate |
| `ire_bop_shift_security_directorate_small` | right, security directorate | emergency directorate |
| `ire_bop_add_constitutional_shift_effect` | left, constitutional government | opening |
| `ire_bop_add_armed_pressure_shift_effect` | right, armed political pressure | opening |
| `ire_bop_add_civilian_cabinet_shift_effect` | left, civilian cabinet | historical emergency |
| `ire_bop_add_emergency_apparatus_shift_effect` | right, emergency apparatus | historical emergency |
| `ire_bop_add_independent_review_shift_effect` | left, independent parliamentary review | Commonwealth cooperation |
| `ire_bop_add_defence_liaison_shift_effect` | right, defence liaison cabinet | Commonwealth cooperation |
| `ire_bop_add_dail_labour_cabinet_shift_effect` | left, Dail Labour cabinet | Labour republic |
| `ire_bop_add_workers_congress_shift_effect` | right, workers congress | Labour republic |
| `ire_bop_add_parliamentary_chambers_shift_effect` | left, parliamentary right and chambers | Blueshirt corporate |
| `ire_bop_add_blueshirt_guard_shift_effect` | right, Blueshirt guard | Blueshirt corporate |
| `ire_bop_add_civilian_front_shift_effect` | left, civilian republican front | republican underground |
| `ire_bop_add_army_council_shift_effect` | right, Army Council | republican underground |
| `ire_bop_add_civic_institutions_shift_effect` | left, civic institutions | civic cultural |
| `ire_bop_add_cultural_mobilisation_shift_effect` | right, cultural mobilisation networks | civic cultural |
| `ire_bop_add_civilian_restoration_shift_effect` | left, civilian restoration | emergency directorate |
| `ire_bop_add_security_directorate_shift_effect` | right, security directorate | emergency directorate |
| `ire_bop_add_institutional_shift_effect` | left side appropriate to current institutional mode | Commonwealth, Blueshirt, civic, or opening fallback |
| `ire_bop_add_civilian_shift_effect` | left side appropriate to current civilian mode | historical, republican, directorate, or opening fallback |
| `ire_bop_add_strong_left_shift_effect` | unguarded strong left | parent-only for major events or crisis resolution |
| `ire_bop_add_strong_right_shift_effect` | unguarded strong right | parent-only for major events or crisis escalation |

### Triggers

Mode triggers:

- `ire_bop_has_state_authority`
- `ire_bop_is_mode_opening_state`
- `ire_bop_is_mode_historical_emergency`
- `ire_bop_is_mode_commonwealth_cooperation`
- `ire_bop_is_mode_labour_republic`
- `ire_bop_is_mode_blueshirt_corporate`
- `ire_bop_is_mode_republican_underground`
- `ire_bop_is_mode_civic_cultural`
- `ire_bop_is_mode_emergency_directorate`
- `ire_bop_has_active_mode_trigger`
- `ire_bop_can_switch_route_mode_trigger`

Earlier internal trigger names with `_trigger` suffixes remain as aliases or implementation details.

Range triggers use expected BOP range ids that the parent must define in `common/bop/IRE_state_authority_bop`:

- `ire_bop_is_left_moderate_range_trigger`
- `ire_bop_is_left_high_range_trigger`
- `ire_bop_is_left_extreme_range_trigger`
- `ire_bop_is_right_moderate_range_trigger`
- `ire_bop_is_right_high_range_trigger`
- `ire_bop_is_right_extreme_range_trigger`
- `ire_bop_is_contested_center_range_trigger`
- `ire_bop_is_left_moderate_or_higher_trigger`
- `ire_bop_is_left_high_or_extreme_trigger`
- `ire_bop_is_right_moderate_or_higher_trigger`
- `ire_bop_is_right_high_or_extreme_trigger`
- `ire_bop_is_extreme_band_trigger`
- `ire_bop_is_left_high_or_extreme`
- `ire_bop_is_right_high_or_extreme`
- `ire_bop_is_center_contested`
- `ire_bop_is_stable_institutional`
- `ire_bop_is_pressure_dominant`

## Constants and tuning table plan

`ireland_bop_constants.txt` defines:

- `ireland_bop_values`: opening start and conservative mode translation caps.
- `ireland_bop_delta`: small, medium, large, standard, strong, and recovery left/right shift magnitudes.
- `ireland_bop_range_thresholds`: recommended parent BOP range boundaries from `-1.00` to `1.00`.
- `ireland_bop_mission_durations`: mission duration bands for public order, route stabilisation, port security, production truce, republican network audits, directorate restoration, and crisis response.

The effects file mirrors BOP deltas as file-local `@` constants because `set_power_balance` and `add_power_balance_value` are documented with literal decimal fields, not `constant:` support. Parent decision and mission files should use `constant:ireland_bop_mission_durations.*` where their fields support script constants; for timed flags or unsupported duration fields, assign to a variable first or use a file-local macro.

## Event target and cleanup plan

No event targets are created by this helper layer.

Cleanup is flag-based:

- `ire_bop_clear_mode_flags_effect` clears all mode flags.
- `ire_bop_clear_crisis_flags_effect` clears BOP crisis flags and the existing Ireland route crisis flags that overlap with BOP crisis routing.
- `ire_bop_cleanup_invalid_mode_effect` reconstructs the mode flag from active BOP sides, initializes opening mode for invalid active sides, or removes the BOP if the scope is no longer original Ireland.

If later decisions use global event targets for selected sponsors, selected Northern actors, or crisis sources, those systems must own `clear_global_event_target` calls in their own cleanup helpers.

## Migration plan from duplicated logic to helpers

1. Parent creates the single BOP object `IRE_state_authority_bop` in `common/bop`, with all side ids listed in the user task and range ids matching the trigger helpers.
2. Opening trunk calls `ire_bop_initialize_opening_state` once the BOP should become visible.
3. Route lock focuses call the matching `ire_bop_set_mode_*` helper.
4. Major focus, decision, mission, and event outcomes call the specific side shift helper instead of repeating `add_power_balance_value`.
5. Crisis and route failure flows call `ire_bop_cleanup_invalid_mode` after changing route flags or active sides.
6. Decision visibility and scripted localisation use mode and range triggers rather than raw side checks.

## Risks and syntax uncertainty

- The parent BOP object is not present in this change. Until it defines `IRE_state_authority_bop`, all effects/triggers are integration scaffolding.
- Range triggers rely on parent-defined range ids: `ire_bop_left_moderate_range`, `ire_bop_left_high_range`, `ire_bop_left_extreme_range`, `ire_bop_contested_center_range`, `ire_bop_right_moderate_range`, `ire_bop_right_high_range`, and `ire_bop_right_extreme_range`.
- `set_power_balance` and `add_power_balance_value` are documented with literal decimal fields. This helper uses file-local `@` constants in those fields and reserves `script_constants` for parent BOP ranges, durations, and fields documented or proven to accept `constant:`.
- `ire_bop_shift_left_small/medium/large` and `ire_bop_shift_right_small/medium/large` are intentionally unguarded and have no tooltip side. Prefer guarded side-specific wrappers for ordinary decisions when the tooltip side matters.
- `ire_bop_shift_to_center_small` and `ire_bop_shift_to_center_medium` are conservative correction helpers, not exact absolute setters. They cannot calculate the remaining distance to zero.

## Meaningful validation notes

Validation should focus on the final integrated BOP object and call sites:

- Confirm `IRE_state_authority_bop` exists once in `common/bop`.
- Confirm all side ids used by mode switch effects exist on that BOP object.
- Confirm all range ids used by trigger helpers exist on that BOP object and follow the threshold table.
- Confirm ordinary focus and decision call sites use guarded side-specific shift helpers.
- Confirm route and crisis cleanup calls do not erase still-needed route flags before follow-up events evaluate them.
