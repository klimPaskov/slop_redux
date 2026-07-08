# Ireland BOP id registry

All ids are suggested implementation handles. The implementer may adapt them to the existing repository pattern, but must keep a mapping in docs if renamed.

## BOP object

| Id | Purpose |
| --- | --- |
| `IRE_state_authority_bop` | Single Ireland BOP object for all route specific visible side pairs. |

## Modes

| Mode id | Purpose |
| --- | --- |
| `ire_bop_mode_opening_state` | Constitutional government versus armed pressure before route lock. |
| `ire_bop_mode_historical_emergency` | Civilian cabinet versus emergency apparatus. |
| `ire_bop_mode_commonwealth_cooperation` | Independent parliamentary review versus defence liaison cabinet. |
| `ire_bop_mode_labour_republic` | Dáil Labour cabinet versus workers congress. |
| `ire_bop_mode_blueshirt_corporate` | Parliamentary right and chambers versus Blueshirt guard. |
| `ire_bop_mode_republican_underground` | Civilian republican front versus Army Council. |
| `ire_bop_mode_civic_cultural` | Civic institutions versus cultural mobilisation networks. |
| `ire_bop_mode_emergency_directorate` | Civilian restoration versus security directorate. |

## Side ids

| Side id | Mode use |
| --- | --- |
| `ire_bop_side_constitutional_government` | opening first side |
| `ire_bop_side_armed_political_pressure` | opening second side |
| `ire_bop_side_civilian_cabinet` | historical first side |
| `ire_bop_side_emergency_apparatus` | historical second side |
| `ire_bop_side_independent_parliamentary_review` | Commonwealth first side |
| `ire_bop_side_defence_liaison_cabinet` | Commonwealth second side |
| `ire_bop_side_dail_labour_cabinet` | Labour first side |
| `ire_bop_side_workers_congress` | Labour second side |
| `ire_bop_side_parliamentary_right_chambers` | Blueshirt first side |
| `ire_bop_side_blueshirt_guard` | Blueshirt second side |
| `ire_bop_side_civilian_republican_front` | IRA first side |
| `ire_bop_side_army_council` | IRA second side |
| `ire_bop_side_civic_institutions` | cultural first side |
| `ire_bop_side_cultural_mobilisation_networks` | cultural second side |
| `ire_bop_side_civilian_restoration` | directorate first side |
| `ire_bop_side_security_directorate` | directorate second side |

## Helper effect handles

| Effect handle | Purpose |
| --- | --- |
| `ire_bop_initialize_opening_effect` | Start opening mode and show BOP. |
| `ire_bop_switch_mode_effect` | Generic mode switch wrapper with cleanup. |
| `ire_bop_switch_to_historical_emergency_effect` | Switch to historical mode. |
| `ire_bop_switch_to_commonwealth_effect` | Switch to Commonwealth mode. |
| `ire_bop_switch_to_labour_effect` | Switch to Labour mode. |
| `ire_bop_switch_to_blueshirt_effect` | Switch to Blueshirt mode. |
| `ire_bop_switch_to_ira_effect` | Switch to republican underground mode. |
| `ire_bop_switch_to_civic_cultural_effect` | Switch to civic cultural mode. |
| `ire_bop_switch_to_directorate_effect` | Switch to Emergency Directorate mode. |
| `ire_bop_add_constitutional_shift_effect` | Opening side shift toward constitutional government. |
| `ire_bop_add_armed_pressure_shift_effect` | Opening side shift toward armed pressure. |
| `ire_bop_cleanup_invalid_mode_effect` | Remove old flags, missions, and decisions. |
| `ire_bop_handle_route_failure_effect` | Route failure cleanup and recovery setup. |

## Helper trigger handles

| Trigger handle | Purpose |
| --- | --- |
| `ire_bop_is_opening_mode_trigger` | Checks opening mode. |
| `ire_bop_is_route_mode_trigger` | Checks active route mode by parameter or specific helper. |
| `ire_bop_is_left_high_trigger` | Checks strong first side band. |
| `ire_bop_is_right_high_trigger` | Checks strong second side band. |
| `ire_bop_is_extreme_band_trigger` | Checks any extreme band. |
| `ire_bop_can_show_route_decisions_trigger` | Shared decision visibility logic. |
| `ire_bop_can_switch_route_mode_trigger` | Safety check for route mode changes. |
| `ire_bop_can_enter_directorate_trigger` | Directorate reveal gate. |
| `ire_bop_can_recover_civilian_rule_trigger` | Restoration gate. |
| `ire_bop_foreign_dependency_blocks_clean_route_trigger` | Anti dependency blocker. |

## Variable and flag handles

| Handle | Purpose |
| --- | --- |
| `ire_bop_current_mode` | Stored mode identifier if the implementation uses a variable pattern. |
| `ire_bop_last_major_shift_source` | Recent cause for dynamic tooltip. |
| `ire_bop_crisis_cooldown` | Prevents repeated crisis event spam. |
| `ire_bop_route_mode_locked` | Route mode has been initialized. |
| `ire_bop_in_recovery` | Recovery or restoration phase active. |
| `ire_bop_hidden_route_disqualified` | Used by hidden route cleanup where needed. |
