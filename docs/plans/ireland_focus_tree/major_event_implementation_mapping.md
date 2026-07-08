# Ireland Major Event Implementation Mapping

Source package: `docs/specs/ireland_focus_tree/` and the canonical event matrices.

Implemented files:

- `events/ireland_focus_tree_events.txt`: opening, historical trunk, BOP threshold, and BOP recovery events `slopx_ireland_focus.1` through `.29`.
- `events/ireland_focus_tree_major_events.txt`: route, industry, military, diplomacy, Northern settlement, hidden path, late game, and hidden runtime events `slopx_ireland_focus.30` through `.150`.
- `common/scripted_effects/ireland_major_event_effects.txt`: major-event cooldown, hidden maintenance pulse, and reusable payload helpers.
- `common/on_actions/ireland_focus_tree_on_actions.txt`: Ireland-only daily hook for hidden maintenance, not a world iteration.
- `interface/ireland_focus_tree.gfx`: generated Ireland event/news/flavour report sprites.

## Coverage Summary

| Family | Event ids | Visible events | Hidden runtime | Failure or overreach | Mechanical connections |
| --- | --- | ---: | ---: | --- | --- |
| Opening and historical trunk | `.1-.18` | 18 | 0 | Emergency sunset, internment dispute, first public order test | authority, preparedness, ports, coastwatch, G2, LDF, BOP init |
| BOP warning and recovery | `.19-.29` | 11 | 0 | overcentralisation, armed pressure, apparatus, sponsor, congress, guard, army council, civic capture, directorate rule | `IRE_state_authority_bop`, authority/preparedness/partition/foreign access |
| Fine Gael constitutional opposition | `.30-.37` | 8 | 0 | defence consultation backlash, base request pressure | legal authority, liaison caps, Northern reassurance, BOP parliamentary review/liaison |
| Democratic Labour | `.38-.47`, `.102`, `.126` | 12 | 0 | workers congress overreach, church tension, sponsor warning | democratic Labour, union councils, cross-border council, BOP Dail Labour/workers congress |
| Blueshirt corporatism | `.48-.57`, `.119`, `.127` | 12 | 0 | march crisis, O'Duffy confidence, guard overreach, corporate sponsor alarm | corporate chambers, O'Duffy split, guard pressure, BOP chamber/guard |
| IRA underground crisis | `.58-.68`, `.117`, `.128` | 13 | 0 | compromised network, Plan file exposure, uprising deadline, dependency crisis | civilian front, army council, courier exposure, reconciliation backchannel, BOP republican front/army council |
| Industry and supply | `.69-.76` | 8 | 0 | ration trust strain, foreign contract pressure | Shannon/grid, sugar beet, turf, ports, rail, stores, self-sufficiency |
| Emergency defence and military | `.77-.85` | 9 | 0 | drill incidents, air/naval shortages | army establishment, port batteries, LOPs, LDF, air warning, naval patrol, G2 |
| Diplomacy and foreign access | `.86-.95`, `.116`, `.125`, `.129` | 13 | 0 | foreign access threshold, sponsor dependency backlash, aftershock recovery | British/German/US/Soviet/Vatican channels, neutral conference, Atlantic compact |
| Northern settlement and integration | `.96-.108`, `.120-.124` | 18 | 0 | integration backlash, protectorate review, settlement failure | prepared settlement, state-control verification, safeguards, staged integration, all-island identity |
| Hidden paths | `.109-.120` | 12 | 0 | corrupted restoration failure, mobilisation overreach, directorate entrenchment, protectorate extension | civic restoration, directorate, common platform, constitutional/republican backchannels, corporate chambers without O'Duffy |
| Hidden cleanup and achievement hooks | `.131-.150` | 0 | 20 | integration failure check, route crisis cleanup, corrupted restoration cleanup | hidden reveal rewards, backchannel cleanup, foreign crisis recovery, protectorate exit, integration advance/failure, achievement flags |

## Runtime Pattern

Visible major events are ordinary MTTH events. Each event is gated by:

- `original_tag = IRE`
- a route focus, route flag, pressure trigger, or settlement trigger
- `NOT = { has_country_flag = ireland_major_event_cooldown }`
- a one-shot `ireland_major_seen_*` flag

Visible options use `ai_chance` and call concrete payloads: authority/preparedness/partition/foreign-access helpers, BOP shifts, state-settlement helpers, achievement flags, or cleanup flags.

Hidden maintenance is separate:

- `slopx_ireland_major_event_pulse` runs only from `on_daily_IRE`.
- It schedules hidden root `.131` only when `ireland_major_cleanup_cooldown` expires.
- Root `.131` dispatches `.132-.150` only when the relevant focus, pressure, route, state-control, or achievement condition is already true.

## Asset Wiring

Every visible event in `events/ireland_focus_tree_events.txt`, `events/ireland_focus_tree_major_events.txt`, and `events/ireland_flavour_events.txt` uses generated Ireland sprites registered in `interface/ireland_focus_tree.gfx`.

Major news sprites:

- `GFX_news_ireland_ports_return`
- `GFX_news_ireland_commonwealth_liaison`
- `GFX_news_ireland_labour_congress`
- `GFX_news_ireland_corporate_chambers`
- `GFX_news_ireland_northern_settlement`
- `GFX_news_ireland_unified_identity`
- `GFX_news_ireland_atlantic_compact`

Major report sprites:

- `GFX_report_ireland_coastwatch`
- `GFX_report_ireland_g2_intercept`
- `GFX_report_ireland_safehouse_network`
- `GFX_report_ireland_integration_commission`
- `GFX_report_ireland_emergency_directorate`
- `GFX_report_ireland_civic_cultural_route`
- `GFX_report_ireland_bop_warning_authority`

Shared flavour report sprites:

- `GFX_flavour_report_civic_life`
- `GFX_flavour_report_press_radio`
- `GFX_flavour_report_language_school`
- `GFX_flavour_report_turf_rationing`
- `GFX_flavour_report_rural_industry`
- `GFX_flavour_report_power_transport`
- `GFX_flavour_report_ports_coast`
- `GFX_flavour_report_civil_defence`
- `GFX_flavour_report_g2_internment`
- `GFX_flavour_report_border_life`
- `GFX_flavour_report_relief`

## Validation Targets

- Event ids `.1-.150` are unique by definition across the two focus event files.
- Visible major-event localisation references resolve in `localisation/english/slop_redux_l_english.yml`.
- No visible Ireland focus, major, or flavour event still points at a generic vanilla event picture.
- All generated `GFX_news_ireland_*`, `GFX_report_ireland_*`, and `GFX_flavour_report_*` references are registered in `interface/ireland_focus_tree.gfx`.
