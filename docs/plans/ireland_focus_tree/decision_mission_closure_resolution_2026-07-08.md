# Ireland Decision And Mission Closure Resolution

Date: 2026-07-08

## Purpose

This note resolves the improvement-loop finding that some closure-proof Ireland route actions still looked like short timed decisions instead of objective missions. It records which rows were converted into selectable missions and which rows intentionally remain ordinary decisions.

## Converted Selectable Missions

The following one-shot route, hidden-path, BOP, Northern settlement, protectorate, or achievement-proof rows now use `selectable_mission = yes`, `days_mission_timeout`, explicit completion flags, timeout flags or timeout effects, concrete cost/resource checks, and route-aware AI where relevant.

- Authority, Emergency, and hidden recovery proof: `ireland_hold_dail_confidence_mission`, `ireland_veterans_reconciliation_mission`, `ireland_emergency_stockpile_mission`, `ireland_coastwatch_posts_mission`, `ireland_constitutional_concession_test_mission`, `ireland_neutral_aftershock_recovery_mission`, `ireland_corrupted_restoration_recovery_board`, `ireland_restore_civilian_rule_mission`.
- Labour and republican route proof: `ireland_labour_cross_border_council`, `ireland_legal_worker_defence_mandate`, `ireland_republican_reconciliation_backchannel`, `ireland_safehouse_audit`, `ireland_courier_exposure_stage`, `ireland_arms_surrender_channel`, `ireland_border_cells_stand_down`.
- Northern settlement and integration proof: `ireland_border_survey_mission`, `ireland_international_observer_preparation`, `ireland_common_platform_table_mission`, `ireland_common_platform_unionist_alarm_containment`, `ireland_common_platform_minority_guarantee_charter`, `ireland_policing_transition_stage`, `ireland_service_continuity_stage`, `ireland_belfast_industry_stage`, `ireland_unionist_safeguards_stage`, `ireland_northern_emergency_protectorate`, `ireland_protectorate_temporary_administration`, `ireland_protectorate_observer_corridor`, `ireland_protectorate_policing_board`, `ireland_exit_emergency_protectorate_settlement`.
- BOP route proof: `ire_bop_coast_security_transfer`, `ire_bop_worker_production_truce`, `ire_bop_guard_discipline_case`, `ire_bop_civilian_rule_timetable_mission`, `ire_bop_northern_legitimacy_hearing_mission`.

## Ordinary Decisions Retained

These remain ordinary decisions because their job is to spend resources and apply a local project or pressure adjustment, not to prove route closure:

- Port and watch works: `ireland_secure_cobh_approaches`, `ireland_secure_berehaven_gate`, `ireland_lough_swilly_watch_rotation`.
- Routine BOP pressure levers: `ire_bop_public_confidence_drive`, `ire_bop_veterans_reconciliation_board`, `ire_bop_emergency_order_review`, `ire_bop_anti_basing_vote`, `ire_bop_defence_liaison_protocol`, `ire_bop_congress_mandate`, `ire_bop_cadre_mobilisation`, `ire_bop_civilian_front_conference`, `ire_bop_army_council_mandate`, `ire_bop_civic_institution_drive`, `ire_bop_public_cultural_mobilisation`.
- Local timed route actions whose success is a scoped costed project rather than a route-ending proof: `ireland_constitutional_backchannel_document_review`, `ireland_g2_counterespionage_review`, `ireland_turf_transport_priority`, `ireland_rail_and_road_repair_contract`, `ireland_ldf_training_cycle`, `ireland_london_channel_board`, `ireland_expose_german_courier_network`, `ireland_route_authority_review`, `ireland_labour_democratic_return_check`, `ireland_cooperative_supply_front`, `ireland_corporate_sponsor_containment`, `ireland_guard_leader_crisis`, `ireland_enforce_no_basing_principle`.

## Pressure Missions Retained As Auto Missions

`ireland_emergency_directorate_warning_mission` and `ireland_army_council_reconciliation_crisis` intentionally remain timeout pressure missions. They are meant to punish inaction or cancel when the player completes the matching corrective path; they are not player-completed project missions.

## Implementation Surfaces

- `common/decisions/ireland_focus_tree_decisions.txt`
- `common/decisions/ireland_bop_decisions.txt`
- `localisation/english/slop_redux_l_english.yml`
