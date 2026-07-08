# Ireland Major Event Suite Worker Handoff

Main implementation update: this handoff records the first `.1-.29` event tranche as delivered by the subagent. The final implementation has since integrated localisation, replaced the generic picture keys with generated Ireland event sprites, and added the expanded `.30-.150` major-event suite. Use `docs/plans/ireland_focus_tree/major_event_implementation_mapping.md` and the current event files as the final source for event/art coverage.

Scope: first implementation tranche for `slopx_ireland_focus` events in `events/ireland_focus_tree_events.txt`.

Write set used:
- `events/ireland_focus_tree_events.txt`
- `docs/plans/ireland_focus_tree/subagent_handoffs/major_event_suite_worker_handoff.md`

## Event ID Map

| Event id | Handle | Surface | Current picture key |
| --- | --- | --- | --- |
| `slopx_ireland_focus.1` | `opening_dail_mandate` | country event | `GFX_report_event_generic_sign_treaty1` |
| `slopx_ireland_focus.2` | `constitution_public_authority` | country event | `GFX_report_event_generic_sign_treaty1` |
| `slopx_ireland_focus.3` | `presidency_and_public_symbol` | country event | `GFX_report_event_generic_sign_treaty1` |
| `slopx_ireland_focus.4` | `civil_war_memory_returns` | country event | `GFX_report_event_generic_rifles` |
| `slopx_ireland_focus.5` | `first_public_order_test` | country event | `GFX_report_event_generic_rifles` |
| `slopx_ireland_focus.6` | `route_convention_opens` | country event | `GFX_report_event_generic_sign_treaty1` |
| `slopx_ireland_focus.7` | `authority_bop_initialized` | country event | `GFX_report_event_generic_research_lab` |
| `slopx_ireland_focus.8` | `first_northern_question_hearing` | country event | `GFX_report_event_generic_sign_treaty1` |
| `slopx_ireland_focus.9` | `ports_handover_public_relief` | news event | `GFX_news_event_generic_sign_treaty3` |
| `slopx_ireland_focus.10` | `treaty_ports_military_assessment` | country report event | `GFX_report_event_usa_destroyers` |
| `slopx_ireland_focus.11` | `emergency_powers_debate` | country event | `GFX_report_event_generic_sign_treaty1` |
| `slopx_ireland_focus.12` | `coastwatch_service_expands` | country report event | `GFX_report_event_usa_destroyers` |
| `slopx_ireland_focus.13` | `neutral_ship_incident` | country report event | `GFX_report_event_usa_destroyers` |
| `slopx_ireland_focus.14` | `internment_policy_dispute` | country event | `GFX_report_event_generic_rifles` |
| `slopx_ireland_focus.15` | `g2_counter_espionage_report` | country report event | `GFX_report_event_generic_research_lab` |
| `slopx_ireland_focus.16` | `ldf_public_mobilisation` | country report event | `GFX_report_event_generic_rifles` |
| `slopx_ireland_focus.17` | `neutrality_survives_first_test` | news event | `GFX_news_event_generic_sign_treaty3` |
| `slopx_ireland_focus.18` | `emergency_powers_sunset_review` | country event | `GFX_report_event_generic_sign_treaty1` |
| `slopx_ireland_focus.19` | `opening_bop_center_contested` | country event | `GFX_report_event_generic_sign_treaty1` |
| `slopx_ireland_focus.20` | `constitutional_overcentralisation` | country event | `GFX_report_event_generic_sign_treaty1` |
| `slopx_ireland_focus.21` | `armed_pressure_extreme` | country event | `GFX_report_event_generic_rifles` |
| `slopx_ireland_focus.22` | `emergency_apparatus_overreach` | country report event | `GFX_report_event_generic_research_lab` |
| `slopx_ireland_focus.23` | `liaison_cabinet_dependency` | country report event | `GFX_report_event_usa_destroyers` |
| `slopx_ireland_focus.24` | `workers_congress_pushes_past_dail` | country event | `GFX_report_event_generic_factory` |
| `slopx_ireland_focus.25` | `blueshirt_guard_state_capture` | country event | `GFX_report_event_generic_rifles` |
| `slopx_ireland_focus.26` | `army_council_state_capture` | country event | `GFX_report_event_generic_rifles` |
| `slopx_ireland_focus.27` | `civic_cultural_capture` | country event | `GFX_report_event_generic_dancing` |
| `slopx_ireland_focus.28` | `security_directorate_permanent_rule` | country report event | `GFX_report_event_generic_research_lab` |
| `slopx_ireland_focus.29` | `bop_recovery_settlement` | country event | `GFX_report_event_generic_peaceful_annexation` |

All events are `is_triggered_only = yes`. No on_actions, focus hooks, decisions, localisation, interface, assets, scripted effects, scripted triggers, achievements, or AI files were edited.

## Localisation Drafts

These keys are not integrated in this tranche. Add them to the Ireland localisation file with UTF-8 BOM encoding and without `:0`.

```yaml
slopx_ireland_focus.opening_dail_mandate.t: "Opening Parliamentary Mandate"
slopx_ireland_focus.opening_dail_mandate.desc: "The government presents its opening programme as a test of public authority. Ministers need either a clear cabinet mandate or a wider consultation before the work can move."
slopx_ireland_focus.opening_dail_mandate.a: "Let the cabinet carry the mandate."
slopx_ireland_focus.opening_dail_mandate.b: "Keep the mandate under consultation."

slopx_ireland_focus.constitution_public_authority.t: "Public Authority and the Constitution"
slopx_ireland_focus.constitution_public_authority.desc: "The constitutional settlement gives the state clearer instruments, but its public meaning remains contested. The chamber must decide whether authority comes first or whether hearings temper the settlement."
slopx_ireland_focus.constitution_public_authority.a: "Confirm the authority of the institutions."
slopx_ireland_focus.constitution_public_authority.b: "Open public hearings before the next step."

slopx_ireland_focus.presidency_and_public_symbol.t: "The Presidency as a Public Symbol"
slopx_ireland_focus.presidency_and_public_symbol.desc: "The new office can steady public life if it is presented as a constitutional symbol rather than a factional prize. Officials prepare a careful programme of ceremony, appointments, and civic contact."
slopx_ireland_focus.presidency_and_public_symbol.a: "Present continuity through the office."
slopx_ireland_focus.presidency_and_public_symbol.b: "Build a wider civic programme around it."

slopx_ireland_focus.civil_war_memory_returns.t: "Old Divisions Return to Public Life"
slopx_ireland_focus.civil_war_memory_returns.desc: "Debate over the state programme brings old bitterness back into meetings, newspapers, and local committees. The government can answer with reconciliation or with a firmer public order line."
slopx_ireland_focus.civil_war_memory_returns.a: "Hold the line through reconciliation."
slopx_ireland_focus.civil_war_memory_returns.b: "Prepare the security services for disorder."

slopx_ireland_focus.first_public_order_test.t: "The First Public Order Test"
slopx_ireland_focus.first_public_order_test.desc: "A political confrontation gives the government its first visible test of restraint. Police reports warn that a weak answer may invite further pressure, while a heavy answer may deepen mistrust."
slopx_ireland_focus.first_public_order_test.a: "Restraint will show confidence."
slopx_ireland_focus.first_public_order_test.b: "The state must show it can act."

slopx_ireland_focus.route_convention_opens.t: "The Route Convention Opens"
slopx_ireland_focus.route_convention_opens.desc: "Delegates, ministers, and party organisers gather to define the next political course. Each bloc arrives with a different answer to authority, neutrality, labour organisation, and security."
slopx_ireland_focus.route_convention_opens.a: "Keep the route anchored in parliamentary neutrality."
slopx_ireland_focus.route_convention_opens.b: "Give civic bodies a stronger place."
slopx_ireland_focus.route_convention_opens.c: "Let labour committees shape the programme."
slopx_ireland_focus.route_convention_opens.d: "Prepare emergency committees for hard choices."

slopx_ireland_focus.authority_bop_initialized.t: "State Authority Balance Opened"
slopx_ireland_focus.authority_bop_initialized.desc: "The contest over public authority is no longer abstract. Cabinet, parliament, security offices, and organised movements all expect the next decisions to move the balance of power."
slopx_ireland_focus.authority_bop_initialized.a: "Put the balance before the government."

slopx_ireland_focus.first_northern_question_hearing.t: "The First Northern Question Hearing"
slopx_ireland_focus.first_northern_question_hearing.desc: "The first formal hearing on partition pressure brings legal, local, and security arguments into the same room. A careful answer can lower tension, but a border-first answer will harden expectations."
slopx_ireland_focus.first_northern_question_hearing.a: "Keep the matter in legal hearings."
slopx_ireland_focus.first_northern_question_hearing.b: "Prioritise local safeguards."
slopx_ireland_focus.first_northern_question_hearing.c: "Order a border security review."

slopx_ireland_focus.ports_handover_public_relief.t: "The Treaty Ports Return"
slopx_ireland_focus.ports_handover_public_relief.desc: "The transfer of the ports brings visible relief across the country. The government treats the moment as both a public confirmation of sovereignty and the beginning of a harder defence burden."
slopx_ireland_focus.ports_handover_public_relief.a: "Sovereignty brings new duties."

slopx_ireland_focus.treaty_ports_military_assessment.t: "Military Assessment of the Ports"
slopx_ireland_focus.treaty_ports_military_assessment.desc: "The staff assessment is sober. The ports are valuable, exposed, and in need of a programme that can defend them without making Ireland dependent on outside arrangements."
slopx_ireland_focus.treaty_ports_military_assessment.a: "Prioritise batteries and harbour works."
slopx_ireland_focus.treaty_ports_military_assessment.b: "Build patrol routines under Irish control."
slopx_ireland_focus.treaty_ports_military_assessment.c: "Accept limited repair liaison."

slopx_ireland_focus.emergency_powers_debate.t: "Debate on Emergency Powers"
slopx_ireland_focus.emergency_powers_debate.desc: "War abroad presses the government to prepare extraordinary measures. The dispute is not over danger itself, but over which offices may act and how the powers will be reviewed."
slopx_ireland_focus.emergency_powers_debate.a: "Set civilian limits from the start."
slopx_ireland_focus.emergency_powers_debate.b: "Build the emergency apparatus."
slopx_ireland_focus.emergency_powers_debate.c: "Attach a sunset review."

slopx_ireland_focus.coastwatch_service_expands.t: "The Coastwatch Service Expands"
slopx_ireland_focus.coastwatch_service_expands.desc: "Reports from the coast show gaps in observation, communications, and local response. The service can grow as a military screen, a civil defence network, or a controlled liaison channel."
slopx_ireland_focus.coastwatch_service_expands.a: "Expand the observation posts."
slopx_ireland_focus.coastwatch_service_expands.b: "Bind the service to local defence."
slopx_ireland_focus.coastwatch_service_expands.c: "Keep a guarded naval channel."

slopx_ireland_focus.neutral_ship_incident.t: "Incident Involving a Neutral Ship"
slopx_ireland_focus.neutral_ship_incident.desc: "A shipping incident tests the limits of neutrality in public view. The cabinet must answer without letting either belligerent turn Irish policy into a precedent."
slopx_ireland_focus.neutral_ship_incident.a: "Protest and organise escort routines."
slopx_ireland_focus.neutral_ship_incident.b: "Seek information through guarded channels."
slopx_ireland_focus.neutral_ship_incident.c: "Restrict the most exposed sailings."

slopx_ireland_focus.internment_policy_dispute.t: "Dispute Over Internment Policy"
slopx_ireland_focus.internment_policy_dispute.desc: "Security offices argue that detention powers are needed before threats become public crises. Legal and political critics warn that unreviewed powers will weaken the authority they are meant to protect."
slopx_ireland_focus.internment_policy_dispute.a: "Require judicial review."
slopx_ireland_focus.internment_policy_dispute.b: "Approve security detention."
slopx_ireland_focus.internment_policy_dispute.c: "Review each case before action."

slopx_ireland_focus.g2_counter_espionage_report.t: "Counter-Espionage Report"
slopx_ireland_focus.g2_counter_espionage_report.desc: "The intelligence report identifies foreign contacts, courier routes, and local intermediaries. Acting too soon may expose only part of the network, but waiting carries political risk."
slopx_ireland_focus.g2_counter_espionage_report.a: "Break the network at once."
slopx_ireland_focus.g2_counter_espionage_report.b: "Watch the contacts longer."
slopx_ireland_focus.g2_counter_espionage_report.c: "Take the case into public prosecution."

slopx_ireland_focus.ldf_public_mobilisation.t: "Public Mobilisation of the Local Defence Force"
slopx_ireland_focus.ldf_public_mobilisation.desc: "The local defence effort draws volunteers, county officials, and military staff into a visible programme. Its value depends on equipment, discipline, and the public trust that it remains under civilian authority."
slopx_ireland_focus.ldf_public_mobilisation.a: "Prioritise equipment and stores."
slopx_ireland_focus.ldf_public_mobilisation.b: "Organise county drills."
slopx_ireland_focus.ldf_public_mobilisation.c: "Emphasise civilian primacy."

slopx_ireland_focus.neutrality_survives_first_test.t: "Neutrality Survives Its First Test"
slopx_ireland_focus.neutrality_survives_first_test.desc: "The first serious pressure on Irish neutrality passes without a formal break. The result steadies the cabinet, but it also proves that the next test may arrive with less warning."
slopx_ireland_focus.neutrality_survives_first_test.a: "Strict neutrality remains the policy."
slopx_ireland_focus.neutrality_survives_first_test.b: "Readiness must come first."

slopx_ireland_focus.emergency_powers_sunset_review.t: "Emergency Powers Sunset Review"
slopx_ireland_focus.emergency_powers_sunset_review.desc: "The review of emergency powers forces the cabinet to account for detention, censorship, communications control, and intelligence authority. The machinery can be narrowed, supervised, or allowed to harden."
slopx_ireland_focus.emergency_powers_sunset_review.a: "Let the strongest powers lapse."
slopx_ireland_focus.emergency_powers_sunset_review.b: "Retain powers under a review board."
slopx_ireland_focus.emergency_powers_sunset_review.c: "Let the directorate retain the machinery."

slopx_ireland_focus.opening_bop_center_contested.t: "The Centre of Authority Is Contested"
slopx_ireland_focus.opening_bop_center_contested.desc: "The opening balance of authority comes under pressure before a stable settlement forms. Parliament, public order committees, and armed intermediaries all expect recognition."
slopx_ireland_focus.opening_bop_center_contested.a: "Rebuild confidence through parliament."
slopx_ireland_focus.opening_bop_center_contested.b: "Negotiate a public order compromise."
slopx_ireland_focus.opening_bop_center_contested.c: "Accept talks under armed pressure."

slopx_ireland_focus.constitutional_overcentralisation.t: "Constitutional Authority Overreaches"
slopx_ireland_focus.constitutional_overcentralisation.desc: "Central authority has moved faster than public consent. The cabinet can review the settlement, impose discipline, or concede hearings that slow the programme."
slopx_ireland_focus.constitutional_overcentralisation.a: "Open a decentralising review."
slopx_ireland_focus.constitutional_overcentralisation.b: "Enforce cabinet discipline."
slopx_ireland_focus.constitutional_overcentralisation.c: "Concede public hearings."

slopx_ireland_focus.armed_pressure_extreme.t: "Armed Pressure Reaches an Extreme"
slopx_ireland_focus.armed_pressure_extreme.desc: "Armed organisers test whether the government will treat them as a political force or a security problem. Each answer carries costs for public authority and partition tension."
slopx_ireland_focus.armed_pressure_extreme.a: "Offer disarmament under civilian terms."
slopx_ireland_focus.armed_pressure_extreme.b: "Contain the pressure through security."
slopx_ireland_focus.armed_pressure_extreme.c: "Negotiate a temporary ceasefire."

slopx_ireland_focus.emergency_apparatus_overreach.t: "Emergency Offices Overreach"
slopx_ireland_focus.emergency_apparatus_overreach.desc: "Emergency offices begin acting ahead of the cabinet's public mandate. The government must decide whether to investigate, ratify, or move the dispute into the courts."
slopx_ireland_focus.emergency_apparatus_overreach.a: "Order a civilian review."
slopx_ireland_focus.emergency_apparatus_overreach.b: "Ratify the operational mandate."
slopx_ireland_focus.emergency_apparatus_overreach.c: "Let the courts define the limit."

slopx_ireland_focus.liaison_cabinet_dependency.t: "Cabinet Dependency on Liaison Channels"
slopx_ireland_focus.liaison_cabinet_dependency.desc: "Foreign liaison has become too useful for some ministers to discard. The cabinet can make a public anti-basing stand, accept the channel, or audit it under strict Irish control."
slopx_ireland_focus.liaison_cabinet_dependency.a: "Force an anti-basing vote."
slopx_ireland_focus.liaison_cabinet_dependency.b: "Keep the liaison channel open."
slopx_ireland_focus.liaison_cabinet_dependency.c: "Audit the channel under cabinet control."

slopx_ireland_focus.workers_congress_pushes_past_dail.t: "The Workers' Congress Pushes Past Parliament"
slopx_ireland_focus.workers_congress_pushes_past_dail.desc: "Labour organisers argue that production committees have earned authority beyond parliamentary schedules. The cabinet can reassert its mandate, trade autonomy for output, or let the congress move further."
slopx_ireland_focus.workers_congress_pushes_past_dail.a: "Reassert the cabinet mandate."
slopx_ireland_focus.workers_congress_pushes_past_dail.b: "Accept a production truce."
slopx_ireland_focus.workers_congress_pushes_past_dail.c: "Let the congress manage its own work."

slopx_ireland_focus.blueshirt_guard_state_capture.t: "Guard Influence Reaches the State"
slopx_ireland_focus.blueshirt_guard_state_capture.desc: "Uniformed organisers press for influence over public order and political ceremony. The state can route them through lawful chambers, discipline them, or cut them away from public authority."
slopx_ireland_focus.blueshirt_guard_state_capture.a: "Bind them to chamber legality."
slopx_ireland_focus.blueshirt_guard_state_capture.b: "Discipline the guard under state command."
slopx_ireland_focus.blueshirt_guard_state_capture.c: "Ban their public role."

slopx_ireland_focus.army_council_state_capture.t: "Army Council Influence Reaches the State"
slopx_ireland_focus.army_council_state_capture.desc: "An armed council claims that the state must accept its discipline and networks. The government can restore a civilian front, audit the hidden structure, or allow direct armed influence."
slopx_ireland_focus.army_council_state_capture.a: "Restore a civilian front."
slopx_ireland_focus.army_council_state_capture.b: "Audit the safehouse network."
slopx_ireland_focus.army_council_state_capture.c: "Accept direct council discipline."

slopx_ireland_focus.civic_cultural_capture.t: "Civic Institutions Capture the Programme"
slopx_ireland_focus.civic_cultural_capture.desc: "Civic and cultural bodies begin shaping policy faster than ministers can supervise it. Their strength can steady local life, but it can also move authority outside the cabinet."
slopx_ireland_focus.civic_cultural_capture.a: "Put schools under civic boards."
slopx_ireland_focus.civic_cultural_capture.b: "Set local charters for the programme."
slopx_ireland_focus.civic_cultural_capture.c: "Use their mobilisation networks."

slopx_ireland_focus.security_directorate_permanent_rule.t: "The Security Directorate Seeks Permanence"
slopx_ireland_focus.security_directorate_permanent_rule.desc: "The security directorate argues that its wartime machinery should remain in place. Ministers must decide whether to schedule civilian restoration, keep the command, or expose its record to public inquiry."
slopx_ireland_focus.security_directorate_permanent_rule.a: "Set a civilian timetable."
slopx_ireland_focus.security_directorate_permanent_rule.b: "Keep the emergency command."
slopx_ireland_focus.security_directorate_permanent_rule.c: "Open a public inquiry."

slopx_ireland_focus.bop_recovery_settlement.t: "Settlement After the Authority Crisis"
slopx_ireland_focus.bop_recovery_settlement.desc: "The crisis has burned through public trust and administrative slack. A settlement can restore the centre, absorb the route consequences, or review the emergency machinery before the next programme begins."
slopx_ireland_focus.bop_recovery_settlement.a: "Restore the centre of authority."
slopx_ireland_focus.bop_recovery_settlement.b: "Accept a route settlement."
slopx_ireland_focus.bop_recovery_settlement.c: "Review all emergency machinery."
```

## Existing Ireland Helpers Used

- `slopx_ireland_initialize_mechanics`
- `slopx_ireland_gain_authority_small`
- `slopx_ireland_gain_authority_medium`
- `slopx_ireland_lose_authority_small`
- `slopx_ireland_gain_preparedness_small`
- `slopx_ireland_gain_preparedness_medium`
- `slopx_ireland_reduce_partition_pressure_small`
- `slopx_ireland_raise_partition_pressure_small`
- `slopx_ireland_reduce_foreign_access_small`
- `slopx_ireland_raise_foreign_access_small`
- `slopx_ireland_cleanup_crisis_flags`

## Expected BOP Helpers Called

These helpers are intentionally called as parent-owned integration points. They are expected in BOP/scripted effect work outside this worker write set.

- `ire_bop_initialize_opening_effect`
- `ire_bop_add_constitutional_shift_effect`
- `ire_bop_add_armed_pressure_shift_effect`
- `ire_bop_switch_to_historical_emergency_effect`
- `ire_bop_shift_civic_compromise_small`
- `ire_bop_shift_civic_institutions_small`
- `ire_bop_shift_independent_parliamentary_review_small`
- `ire_bop_shift_dail_labour_cabinet_small`
- `ire_bop_shift_emergency_apparatus_small`
- `ire_bop_shift_defence_liaison_cabinet_small`
- `ire_bop_shift_civilian_cabinet_small`
- `ire_bop_shift_security_directorate_small`
- `ire_bop_shift_civilian_republican_front_small`
- `ire_bop_shift_army_council_small`
- `ire_bop_shift_workers_congress_small`
- `ire_bop_shift_parliamentary_right_chambers_small`
- `ire_bop_shift_blueshirt_guard_small`
- `ire_bop_shift_civilian_restoration_small`
- `ire_bop_shift_cultural_mobilisation_networks_small`
- `ire_bop_recover_to_center_effect`
- `ire_bop_handle_route_failure_effect`
- `ire_bop_cleanup_invalid_mode_effect`

## Required Assets

Current script references only confirmed vanilla generic keys:
- `GFX_report_event_generic_sign_treaty1`
- `GFX_report_event_generic_rifles`
- `GFX_report_event_generic_research_lab`
- `GFX_news_event_generic_sign_treaty3`
- `GFX_report_event_usa_destroyers`
- `GFX_report_event_generic_factory`
- `GFX_report_event_generic_dancing`
- `GFX_report_event_generic_peaceful_annexation`

Recommended Ireland-specific replacement keys for asset follow-up:
- `GFX_news_event_slopx_ireland_ports_handover_public_relief`
- `GFX_report_event_slopx_ireland_treaty_ports_military_assessment`
- `GFX_report_event_slopx_ireland_coastwatch_service`
- `GFX_report_event_slopx_ireland_neutral_ship_incident`
- `GFX_report_event_slopx_ireland_g2_counter_espionage`
- `GFX_report_event_slopx_ireland_ldf_public_mobilisation`
- `GFX_report_event_slopx_ireland_authority_bop_warning`
- `GFX_report_event_slopx_ireland_workers_congress`
- `GFX_report_event_slopx_ireland_civic_cultural_capture`
- `GFX_report_event_slopx_ireland_bop_recovery_settlement`

## Follow-Up Blockers

- Localisation is not wired because localisation files were outside the write set. The draft English text above avoids real quotes, slogans, Gaelic, exact headlines, prayers, songs, cultural allusions, and audio references.
- BOP helpers are expected integration points and are not defined in this tranche. The parent-owned BOP/scripted effect pass must provide them before these events are load-complete.
- Focus, decision, BOP threshold, and report/news firing hooks are not wired here because those files were outside the write set.
- Events `.9` and `.17` are `news_event` surfaces without `major = yes`; every option carries Ireland gameplay effects, so a global observer version should be implemented as a paired flavour/news surface or with safe observer-only options in a later parent pass.
- Final Ireland-specific event art is not created or registered here because interface and asset files were outside the write set. The script uses confirmed vanilla generic keys until those replacements are ready.
