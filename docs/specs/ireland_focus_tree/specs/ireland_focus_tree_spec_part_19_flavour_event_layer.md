# Ireland focus tree spec part 19, canonical flavour event layer

## Ruling

Flavour events are mandatory implementation content for Ireland. They are not passive colour text and they are not a small afterthought. Ireland should feel alive through ordinary institutions, ports, schools, shops, parish halls, radio rooms, coast posts, trains, farms, border markets, factories, relief committees, party offices, and local councils.

The major event suite in parts 12 and 13 covers public route turns, crises, foreign reactions, BOP breakpoints, Northern settlement stages, hidden reveals, and late game outcomes. This part adds the everyday event layer that makes those systems feel grounded. A campaign should fire a curated subset of the flavour pool based on route, state, pressure, war, season, BOP, focus progress, and mission state.

Working labels in this file and the flavour matrices are internal handles only. They are not final event titles, option text, report prose, news text, slogans, quotes, or cultural remarks.

## Design promise

Ireland should not play as a silent tree where only the biggest diplomatic shifts make noise. The player should see how national policy reaches ordinary life. A ration event should affect the Emergency supply system. A school event should affect civic cultural mobilisation or local support. A harbour event should affect coast watching, shipping, or foreign access. A parish hall event should affect route legitimacy. A border market event should affect Partition Pressure.

Each flavour event must do at least two meaningful things from this list:

- move Constitutional Authority, Emergency Preparedness, Partition Pressure, Foreign Access Pressure, BOP, local support, integration progress, compact cohesion, or route pressure
- open, modify, discount, strengthen, close, or replace a decision or mission
- create a targeted state task with named state group direction
- change an idea stage, national spirit stage, advisor availability, commander trust, or route actor confidence
- alter an AI strategy flag, sponsor willingness, or foreign reaction timer
- create cleanup, memory, or disqualifier logic that changes later events
- add or remove route risk such as corrupted restoration risk, directorate residue, guard overreach, Army Council pressure, or sponsor capture

Small stability, political power, war support, or tiny percentage changes are banned as the only result. A small value shift can support a larger effect package when tied to the live mechanic.

## Density target

The full Ireland event layer should now contain two bands:

| Band | Implementation target | Role |
| --- | --- | --- |
| major event suite | 130 to 170 events or merged dynamic equivalents | route commitments, crises, foreign reactions, Northern settlement, BOP extremes, formables, hidden reveals, news, report events |
| flavour event suite | 140 to 190 events or merged dynamic equivalents | ordinary historical texture with actual mechanic effects |

A practical full implementation target is 270 to 360 Ireland related events or merged dynamic equivalents. Merged dynamic events are acceptable only when the event preserves route specific text direction, historical anchor, trigger, choice logic, effects, AI behavior, and cleanup for every row it replaces.

## Frequency and clutter control

Flavour events should use a curated pool. The player should not be hit by every eligible event at once. Use route pools, state pools, seasonal pools, mission pools, and pressure pools.

Recommended rules:

- one ordinary flavour event can fire every 45 to 90 days in calm periods
- Emergency supply and coast events can fire faster during wartime pressure, but the system should cap visible active tasks
- Northern local flavour should fire around settlement work, integration missions, and local failures, not on a generic timer
- political route flavour should fire after route focuses, campaign decisions, and BOP movement
- hidden path flavour should stay rare until the hidden path is revealed, then become diagnostic and mechanical
- repeated failures should upgrade a pressure chain instead of repeating the same popup
- obsolete flavour pools must close after route change, tag switch, settlement completion, war end, or cleanup

## Historical background standard

Every flavour event needs a concrete historical or social anchor. The anchor can be an institution, industry, policy, place, public habit, transport problem, language question, supply problem, community dispute, or wartime administrative practice. It must not rely on invented drama.

Good anchors for Ireland include the 1937 Constitution, the Treaty Ports settlement, the Emergency Powers Act, coast watching, the LDF and LSF, G2, the Irish Red Cross, the Irish Folklore Commission and Schools Collection, Radio Athlone and Radio Éireann, Ardnacrusha, Aer Lingus, the Turf Development Board, sugar beet factories, creameries, rationing, customs, merchant shipping, border markets, local councils, parish halls, Gaeltacht policy, and postwar relief.

## Route coverage requirement

Every route must receive flavour events that feel different in play.

| Route or system | Flavour requirement |
| --- | --- |
| historical neutrality | ordinary neutrality, supply, coasts, shipping, cabinet discipline, coast posts, merchant marine memory |
| constitutional opposition | legal briefs, petitions, public meetings, backbench pressure, county council disputes, civil service rules |
| Labour | shop stewards, production truce, relief work, church concern, women organizers, cooperative and creamery boards |
| Blueshirt | march permits, discipline rows, corporate boards, right wing foreign channels, guard overreach, public order tests |
| IRA underground | prisoner petitions, safehouses, pamphlets, border smuggling, arms rumours, G2 evidence, family pressure |
| Emergency directorate | filing cabinets, public order success, restoration timetables, permanent security residue, civil policing conflict |
| civic cultural restoration | schools, folklore collectors, language exams, place names, minority guarantees, corrupted restoration safeguards |
| Atlantic compact | harbour diplomacy, member doubts, neutral shipping, observer visits, compact cohesion, public conference signs |
| Northern settlement | market days, rail tickets, local safeguards, policing inquiries, schools, transport, integration administration |
| industry and supply | Ardnacrusha, sugar beet, turf, fuel, public works, ports, aviation, rail, workshops, credit risk |
| late game | civil service integration, schoolbooks, merchant memory, Red Cross relief, demobilisation, neutrality review |

## Effect pacing

Flavour event effects should be felt, but they should not overwhelm focus rewards or major crises. The right pattern is medium weight, localized, staged, and connected.

Examples of acceptable effects:

- a school event creates a county target that reduces civic decision costs after completion
- a coast event lowers accidental air incident risk only after a supplied coast mission succeeds
- a shop queue event changes ration pressure and unlocks a black market response decision
- a border market event raises Partition Pressure and creates a customs mission unless handled quickly
- a party office event changes BOP and adds campaign cost escalation after repeated campaign decisions
- a hidden directorate event strongly lowers short term foreign access but starts a restoration deadline
- a Red Cross event opens a relief convoy decision that costs supplies, convoys, and diplomatic attention

Weak patterns are rejected:

- event fires and gives a small generic stability change
- event gives a few political power points
- event repeats the same equipment reward
- event has no follow up memory
- event has no trigger relation to route or state
- event cannot fail or change later content

## Flavour event catalogue

The canonical row level catalogue is in `matrices/ireland_focus_tree_flavour_event_catalogue_matrix.md`. It contains 169 working flavour event handles. The implementation can merge related rows into dynamic events, but the implementation report must map every working handle to a final event id, dynamic event variant, queued row, or rejected row with reason.

## Asset direction

Most flavour events should use existing route assets, shared report images, or category art. Do not create a unique news or report image for every ordinary event. Create asset families instead:

- civic school and folklore report image family
- coast watching and harbour report image family
- rationing and turf report image family
- rural industry and sugar beet report image family
- LDF and civil defence report image family
- border market and Northern community report image family
- radio and press public information image family
- humanitarian and Red Cross report image family

Every asset remains subject to `hoi4-feature-assets`. Real photographs, real leaders, real symbols, historical flags, and historically attested symbols need sourced asset work. Fictional or symbolic icons can be generated. No asset prompt may use invented historical images as if they were sourced.

## Text and audio boundary

The flavour layer needs stronger final writing than generic tooltips, but this spec does not supply final prose. Final event titles, descriptions, options, slogans, remarks, quotes, and audio cues remain implementation or research work.

Many flavour events can use plain in world prose without source dependent remarks. Where a cultural reference, period slogan, song, proverb, scripture, literary echo, or audio cue is desired, the text and audio research prompt must treat it as blocked until sourced.

## AI behavior

AI Ireland should receive the same flavour effects through weighted options, hidden variants, and route specific decisions. AI should not lose campaigns because ordinary flavour events stack without limits. Use caps and recovery decisions.

Foreign AI should react to flavour only when it changes a real pressure, such as foreign access, Northern settlement credibility, compact cohesion, shipping confidence, or sponsor exposure. Ordinary domestic texture should not wake every major power.

## Cleanup rules

Every flavour pool needs cleanup:

- clear state targets after mission completion or route closure
- remove obsolete decision discounts after route change
- close hidden path diagnostic events when the path is rejected or completed
- cancel supply flavour events after Emergency supply is solved or war ends
- close Northern local flavour after final integration or protectorate handback
- remove sponsor flavour after sponsor invalidation, defeat, or dependency resolution
- reset recurring event counters after tag switch or formable identity change

## Acceptance rule

Ireland is not implementation ready unless the flavour event layer is implemented or explicitly mapped to dynamic equivalents. A report that implements only the major suite while leaving ordinary flavour events absent should be treated as incomplete.
