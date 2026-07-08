# Ireland decision and mission implementation prompt

Feature slug: `ireland_focus_tree`

Use this prompt with `hoi4-decisions-missions` after the focus path implementation is ready to wire decisions. Working labels are not final localisation.

## Required sources

Read the full Ireland spec package, especially:

- `specs/ireland_focus_tree_spec_part_5_decisions_missions.md`
- `specs/ireland_focus_tree_spec_part_6_reunification_formables.md`
- `specs/ireland_focus_tree_spec_part_7_mechanics_presentation.md`
- `matrices/ireland_focus_tree_decision_mission_matrix.md`

Follow `AGENTS.md`, `hoi4-decisions-missions`, `hoi4-focus-trees`, and `hoi4-events` if events are used.

## Must implement

- Constitutional Authority category with public order, reconciliation, constitutional campaign, emergency powers review, and route authority maintenance.
- Emergency Preparedness category with LOP, reserve, stockpile, port garrison, air warning, and G2 mission families.
- Ports and Coast category with transfer, port fortification, access rules, naval stores, and patrol decisions.
- Economic Recovery category with rural relief, native factory, Shannon grid, sugar beet, turf, port economy, and emergency stores projects.
- Foreign Access category with sponsor recognition, aid corridor, foreign liaison, anti dependency, and expose rival patronage decisions.
- Partition Settlement category with survey, committees, observer plebiscite, boundary commission, border incident, uprising, ultimatum, and occupation stabilization missions.
- Post Settlement Integration category with police transition, local administration, minority rights, frontier security, infrastructure integration, and constitutional integration.

## Cost and mission rules

Do not make the categories political power stores. Use dynamic costs and requirements based on equipment, manpower, trains, trucks, convoys, fuel, XP, command power, civilian factory burden, local support, legitimacy, state control, supplied divisions, foreign access, sponsor availability, and war state.

Use timed missions for state objectives. The player should place divisions, hold ports, build infrastructure, staff coastal posts, guard borders, run observer conditions, and complete integration work. Avoid passive checklist missions.

## Clutter and cleanup

Use phases, caps, route locks, target pools, and replacement decisions. Do not show every possible target at once. Cancel obsolete missions and clear temporary flags, variables, and event targets when route, war, sponsor, state owner, formation, or tag status changes.

## AI

Implement route aware AI. Historical AI balances preparedness. Opposition AI cooperates with Britain only when concessions or defence needs exist. Labour AI avoids Soviet dependency unless conditions justify it. Blueshirt and IRA AI choose violent Northern tools only under rare valid states.

## Localisation direction

Write final text during implementation from the design direction. Do not copy working labels as final text. Use icon first cost localisation. Use custom trigger tooltips for long requirements and readable names for state groups.

## Completion evidence

Return a matrix of implemented categories, decision families, mission families, costs, durations, state targets, success effects, failure effects, cleanup, and AI behavior. Report simplifications, missing localisation, missing assets, invalid routes, and any fallback.

## Canonical hidden path decision and mission addendum

Implement hidden path decision families from `specs/ireland_focus_tree_spec_part_10_hidden_paths.md` and `matrices/ireland_focus_tree_hidden_path_decision_matrix.md`.

Required families:

- civic cultural restoration: bilingual civil service, Gaeltacht service routes, rural school expansion, cross community contacts, minority guarantee charter, diaspora education links
- Emergency directorate: authority review, clean foreign cells, intercept couriers, centralise LDF, guard ports, civilian rule timetable
- Atlantic compact: sound out neutral observers, arbitrate shipping incident, host arbitration, deny permanent basing, invite small state observers, guarantee neutral port rights
- common platform settlement: minority guarantees, observer backed plebiscite, local service continuity, nonsectarian committee
- corrupted restoration failure: recovery and cleanup decisions that block the hidden capstone

Use concrete costs and requirements. Avoid political power stores. Hide invalid target decisions. Use cleanup when a route closes, a target no longer exists, Ireland joins a major faction, ports are lost, or a violent Northern route begins.

## Route-specific hidden overlay decision families

| Overlay | Required family | Cost direction | Success | Failure |
| --- | --- | --- | --- | --- |
| `hidden_constitutional_backchannel` | boundary document and liaison cap missions | trust, political capital, limited access pressure, no armed pressure | concession chance and compact reveal | nationalist patience loss and British hardening |
| `hidden_labour_independent_front` | worker guard, veteran integration, cooperative supply missions | equipment, union support, convoys, trains, authority | readiness and supply without client capture | militia capture, church backlash, employer pressure |
| `hidden_corporate_chambers_without_oduffy` | Guard discipline, chamber production, sponsor audit missions | equipment, command, legitimacy, worker backlash risk | institutional route survives leader crisis | coup scare, movement fracture, sponsor capture |
| `hidden_republican_reconciliation_backchannel` | amnesty, safehouse audit, arms surrender, border cell stand down missions | local support, authority, exposure risk, British reaction | underground pressure falls and civic route may reopen | martyr pressure, sabotage crisis, Army Council state |
