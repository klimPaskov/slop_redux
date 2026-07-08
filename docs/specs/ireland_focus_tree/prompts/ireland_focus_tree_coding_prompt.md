# Ireland focus tree coding prompt

Feature slug: `ireland_focus_tree`
Feature name: Ireland comprehensive national focus tree
Working tree id: `slopx_ireland_focus_tree`

Implement the Ireland focus tree according to the full canonical spec package. Do not implement a simplified or fallback version without explicit approval.

## Required reading

Read all files under `docs/specs/ireland_focus_tree/`:

- `README.md`
- `ireland_focus_tree_planning_state.md`
- all files under `specs/`, especially parts 10, 12, and 13
- all matrices in `matrices/`
- all prompts in `prompts/`, including the event prompt
- research notes and bibliography in `research/`
- readiness and blocker reports in `reports/` and `plans/`

Also follow `AGENTS.md`, `hoi4-feature-planning`, `hoi4-focus-trees`, `hoi4-decisions-missions`, `hoi4-events`, `hoi4-feature-assets`, `hoi4-frame-animation`, `hoi4-text-audio-research`, `hoi4-improvement-loop`, and `hoi4-subagents`.

Before editing focus trees and events, read the offline Paradox wiki national focus, event, on action, trigger, effect, localisation, AI, decision, and relevant GUI pages. Inspect vanilla focus, decision, idea, AI, and country files. Inspect existing Slop Redux patterns. Do not rely on memory for syntax.

## Tree requirements

Create a bespoke Ireland national focus tree with a broad non linear structure. Use the spec path design instead of a vertical checklist. The final tree should include:

- opening constitutional trunk
- historical sovereign neutrality route
- constitutional opposition and guarded Commonwealth cooperation route
- Labour and social republic route with democratic and radical sub branches
- Blueshirt corporatist route separated from Fine Gael constitutional opposition
- IRA underground route with absorption and takeover sub branches
- industry and supply branch grounded in Ireland specific state building
- military and Emergency defence branch
- diplomacy and neutrality branch with sponsor pressure
- Northern settlement branch with peaceful, legal, Labour, coercive, and underground variants
- required hidden path architecture from part 10
- late game ambition branch with unified Ireland and route specific postwar outcomes
- required BOP integration from part 12
- required event suite from part 13

The implementation may choose final focus count and coordinates, but it must preserve route locks, branch interaction, support branch compatibility, route payoffs, idea lifecycle, AI behavior, decision hooks, hidden reveal logic, and cleanup.

## Required hidden paths

Hidden paths are required planned content. Implement revealable hidden content from part 10 and the hidden path matrices:

- civic cultural restoration
- Emergency directorate
- Atlantic neutral compact
- common platform Northern settlement
- corrupted restoration failure
- compromised republican network
- cross border Labour Council
- constitutional backchannel
- corporate chambers without O'Duffy
- republican reconciliation backchannel
- neutral aftershock recovery
- Northern emergency protectorate

Each hidden path needs reveal conditions, route blockers, focus groups, decisions or missions, AI behavior, failure states, cleanup, assets, and achievement hooks.

Civic cultural restoration stays peaceful, civic, educational, and constitutional. Aiséirghe inspired capture is dangerous authoritarian cultural pressure and a containment target for democratic routes. The Atlantic neutral compact remains a rare conference or limited faction concept, not a formable country. Northern emergency protectorate is temporary and must use British vulnerability checks, unionist safety, observer legitimacy, and legal settlement or handback outcomes.

## Mechanics and decisions

Implement visible mechanics for Constitutional Authority, Emergency Preparedness, Partition Pressure, Foreign Access Pressure, and the Ireland BOP layer. Use national spirit tooltips, decision headers, scripted localisation, BOP UI, and the planned Emergency scripted GUI board where feasible. Centralize thresholds, gains, durations, BOP range values, and AI weights in script constants or documented tuning helpers.

Implement all mapped decision families and mission families from parts 5, 6, 7, and 10. Use concrete costs and objectives. Do not default to political power or command power purchases. Use equipment, manpower, trains, trucks, convoys, fuel, XP, civilian factory burden, local support, legitimacy, state control, supplied divisions, foreign access, and timers where the spec calls for them.

Northern settlement must not become a claim ladder. Formation decisions must verify state control or settlement conditions before changing identity.


## Required event suite

Events are mandatory planned content. Implement the event suite from part 13 and `prompts/ireland_focus_tree_event_prompt.md`. Create country events, news events, report events, hidden runtime events, foreign reaction events, BOP threshold events, Northern settlement events, formable events, hidden path events, and cleanup events.

Events must connect focuses, decisions, missions, BOP bands, mechanic values, foreign actors, AI route behavior, leader or advisor changes, idea lifecycle, assets, achievements, and cleanup. Events are required implementation surfaces across all major routes and must never be reduced to passive presentation. Do not leave major routes silent.

Do not write final event localisation from working labels. Write final in world text from direction. Keep source dependent quotes, slogans, Gaelic wording, cultural remarks, movement phrases, lyrics, prayers, and audio blocked until researched.

## Country package, assets, and text research

Wire Ireland with correct focus loading, leaders, parties, starting ideas, advisor unlocks, starting force assumptions, force growth, AI strategies, flags, portraits, and localisation. Real leaders and real symbols require sourced assets. Generated portraits are allowed only for fictional or collective bodies.

Use the asset prompt for focus icons, idea icons, decision icons, achievement icons, flags, portraits, faction emblems, UI assets, hidden path assets, and animated assets. Do not leave visible assets missing or undocumented.

Use the text and audio research prompt for source dependent quotes, cultural remarks, slogans, allusions, or audio. Treat all unresearched source dependent wording as blocked. Write ordinary final localisation from the spec direction, not from working labels.

## AI, achievements, audits, and completion

Implement route specific AI for Ireland, Britain, Northern Ireland handling, Germany, Italy, Spain, the United States, the Soviet Union, Vatican influence where implemented, route actors, and hidden path actors. AI must respect route validity, sponsor existence, state control, Britain strength, war state, foreign access pressure, internal authority, hidden route blockers, and cleanup state.

Implement the achievement set from the achievement prompt with tracking flags, variables, unlock triggers, disqualifiers, localisation, icons, and docs. Hidden path achievements should not unlock from focus completion alone when decisions, missions, state control, trust, or cleanup are required.

Before claiming near completion, spawn `hoi4_improvement_loop_planner` with `fork_context=false` using the improvement loop prompt. Resolve the returned addendum by implementing it, folding it into specs, queueing it with reason, rejecting it with reason, or recording closure. If the tool is unavailable, record the blocker clearly.

Before final completion, run focus, event, decision, country package, localisation, asset, and completion audits as appropriate. Provide a route coverage table and a concrete completion report. Report every simplification, omission, missing asset, missing localisation, missing AI behavior, fallback, or blocker.


Additional canonical requirement, flavour event layer

Implement the comprehensive flavour event layer from parts 19, 20, and 21. The flavour layer is not filler. Every row in `matrices/ireland_focus_tree_flavour_event_catalogue_matrix.md` needs a final event, a dynamic variant, or a documented disposition. Flavour events must have concrete effects, historical anchors, AI behavior, and cleanup. They must interact with Constitutional Authority, Emergency Preparedness, Partition Pressure, Foreign Access Pressure, BOP, local support, integration, compact cohesion, route pressure, decisions, missions, ideas, or state targets.
