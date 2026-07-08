# Ireland focus tree spec, part 7 mechanic presentation

This file chooses presentation surfaces for the four Ireland mechanics. Working labels are internal handles only. They are not final GUI labels, decision category text, tooltip text, or localisation.

## Presentation principles

The player should understand basic cause and effect. Future route surprises can stay hidden, but the player must know why a visible value rose or fell and what broad kind of action can change it.

The four mechanics should be visible without forcing the player into a large custom window for every action. Use scripted GUI only where visual management makes the mechanic easier to read than normal decision categories.

Colour identity should be consistent in final localisation and scripted localisation.

| Mechanic | Recommended colour identity | Main presentation | Secondary presentation | Animation need |
| --- | --- | --- | --- | --- |
| Constitutional Authority | blue for legitimacy, orange for armed pressure, grey for emergency reach, green for reconciliation | national spirit tooltip plus decision category header | focus tooltips and route lock tooltips | static is enough, optional warning pulse only if authority near collapse |
| Emergency Preparedness | green for ready, yellow for strained, red for exposed | compact scripted GUI board opened from decision category | decision category header and national spirit | useful animated warning or readiness seal with static fallback |
| Partition Pressure | red for pressure, green for Northern support, purple for unionist alarm, blue for British willingness | decision category header with state target tooltips | targeted missions and formable progress tooltips | static state icons are better than heavy animation |
| Foreign Access Pressure | purple for sponsor leverage, blue for Britain, grey for Germany, red for right wing sponsors, green for US or diaspora, dark red for Soviet pressure | sponsor summary in diplomacy decision category | national spirit tooltip and decision effects | optional subtle sponsor card glow if scripted GUI is used |

## Constitutional Authority

### Best presentation

Use a staged national spirit family with a detailed scripted localisation tooltip and a decision category header. Do not build a full scripted GUI for this value. Constitutional Authority is a status and route gating mechanic, not a board full of independent targets. A large window would add clutter.

### Components

| Component | Meaning | Raised by | Lowered by | Gameplay use |
| --- | --- | --- | --- | --- |
| `dail_legitimacy` | Trust in parliamentary and constitutional rule | Dáil focuses, elections, constitution, reconciliation, fair settlement | armed routes, coercive emergency, foreign dependency | lowers decision costs, enables peaceful settlement, blocks hard routes |
| `armed_movement_pressure` | Power of IRA, Blueshirt, and route militias outside ordinary law | militia tolerance, failed public order, border violence, economic distress | policing, reconciliation, regularization | opens IRA and Blueshirt routes, weakens foreign trust |
| `emergency_executive_reach` | State capacity to act during war | Emergency cabinet, rationing, censorship, security | parliamentary restraint, crisis failure | helps wartime missions but can harm democratic routes |
| `public_reconciliation` | Civil War wounds and cross party trust | amnesty, veterans boards, coalition, fair integration | repression, failed amnesty, coercive settlement | improves stability and integration, reduces backlash |

### Threshold behavior

| Band | Direction | Gameplay effects |
| --- | --- | --- |
| `authority_low` | The state is contested or coercive | peaceful Northern decisions blocked, route crisis decisions visible |
| `authority_mixed` | The state can govern but faces pressure | normal decisions available with higher costs or risks |
| `authority_stable` | constitutional or route authority is credible | lower costs, better integration and diplomacy |
| `authority_exceptional` | rare clean legitimacy | peaceful all island route, cultural epilogue, strict neutral achievement hooks |

### Player readable tooltip direction

The tooltip should show component values, current band, main recent cause, and two to four available action families. It should not list hidden future route unlocks. It can say that armed movements are gaining public space or that parliamentary authority is stable, but it must not reveal secret crisis events.

### AI use

AI should treat low authority as a reason to fix public order before taking foreign or Northern gambles. Route AI can exploit low authority only if it is intentionally choosing IRA or Blueshirt paths.

## Emergency Preparedness

### Best presentation

Use a compact scripted GUI board that opens from the Emergency Preparedness decision category. The board should have four meters or cards: coast watch, reserves, supply, and ports. It should show state mission status and broad danger band. This is the only mechanic in the Ireland package that clearly benefits from a custom scripted GUI because the player needs to manage several defence components at once.

### GUI concept

Working GUI label: `ireland_emergency_board_gui`. This is an internal handle, not final text.

Recommended display:

- Top summary status for overall preparedness band.
- Four component cards with static icons and numeric or band display.
- Active mission slots showing coast, border, port, or supply tasks.
- Warning frame when world war is active and preparedness is low.
- Button to show or hide regional emergency missions.
- Tooltip showing what focuses and decisions can raise each component.

### Animated presentation

Use one small animated state asset if final asset capacity allows it:

| Asset working label | Surface | State logic | Animation direction | Static fallback |
| --- | --- | --- | --- | --- |
| `ireland_emergency_readiness_seal` | Emergency board header or decision category | active when preparedness changes or low during war | subtle signal lamp or coastal watch glow, built from real source frames through frame animation rules | static seal with same silhouette |
| `ireland_emergency_warning_frame` | scripted GUI board | visible in low preparedness during nearby major war | subtle warning pulse, not flashing clutter | static warning frame |

Animation should clarify danger, not decorate every card. Do not fake animation by pulsing one still image.

### Component thresholds

| Component | Low band consequences | High band consequences |
| --- | --- | --- |
| coast watch | higher surprise, more spy incidents, weaker neutrality incident outcomes | better warning, counter espionage, shipping event outcomes |
| reserves | weaker emergency units, harder border missions | cheaper LDF and faster invasion response |
| supply | ration crisis, slower mobilisation, foreign aid pressure | resilient mobilisation and better strict neutrality |
| ports | foreign access demands, weak coastal defence | port command decisions, naval patrols, lower coercion pressure |

### AI use

AI should target minimum preparedness before risky paths. Historical AI should keep all four components balanced. Opposition AI can substitute British liaison for part of air or naval weakness, but that raises foreign access. Labour AI can use worker defence and cooperative supply. Blueshirt AI can use cadres and discipline. IRA AI can use clandestine supply but should suffer more exposure.

## Partition Pressure

### Best presentation

Use a decision category header with dynamic values and targeted missions. Do not build a full scripted GUI initially. The Northern problem is best played through state objectives, observer missions, support missions, and integration projects. A large board would risk looking like a claim menu.

### Values

| Value | Display | Meaning |
| --- | --- | --- |
| `partition_pressure` | red pressure band | urgency and escalation of the Northern issue |
| `northern_nationalist_support` | green support band | ability to run peaceful or uprising missions |
| `unionist_alarm` | purple alarm band | resistance and British reaction difficulty |
| `british_settlement_willingness` | blue diplomacy band | chance of talks, plebiscites, or concession routes |
| `integration_progress` | green or blue progress stage | post settlement administration state |

### Presentation by phase

| Phase | What the player sees | Main actions |
| --- | --- | --- |
| survey | state group tooltip and first pressure band | border survey, committee contacts |
| peaceful campaign | support, alarm, and observer conditions | plebiscite, arbitration, rights guarantees |
| pressure campaign | pressure and military readiness | border defence, incidents, ultimatum prep |
| settlement | decision verifies state control or agreement | formation or partial transfer |
| integration | stage by state group | police transition, administration, rights, infrastructure, cores |

### State target clarity

All missions must name the relevant region in localisation. If exact state ids are hidden inside scripted triggers, the tooltip should still print a readable region name such as Belfast area, Derry area, border counties, Northern ports, or full Northern Ireland state group. The implementation should avoid raw state id exposure.

### Animation decision

Keep this mechanic mostly static. Use icons and warning colour instead of animated frames. Animation can be reserved for the final formation seal in the asset prompt, not for every Northern mission.

## Foreign Access Pressure

### Best presentation

Use the diplomacy decision category header and a national spirit tooltip. If the implementation creates many sponsor actions, use a small sponsor summary panel or target filter pattern. Do not create a huge foreign influence board unless decision density becomes too high.

### Sponsor tracking

| Sponsor component | What it measures | Helpful actions | Dangerous actions |
| --- | --- | --- | --- |
| `british_access_pressure` | base, port, defence, trade leverage | port transfer, defensive contingency, settlement talks | coerced access, dependency without concessions |
| `german_access_pressure` | Abwehr, IRA contacts, anti Britain leverage | counter espionage if exposed and rejected | Plan Kathleen style contact, arms for dependency |
| `right_wing_access_pressure` | Italy, Spain, corporatist diplomacy | anti communist advisors and limited aid | sponsor collapse and democratic isolation |
| `american_access_pressure` | diaspora, recognition, observers, trade | observer support, aid, postwar leverage | sponsor dependence and British suspicion |
| `vatican_access_pressure` | church diplomacy and social legitimacy | mediation and conservative legitimacy | Labour backlash and rights pressure |
| `soviet_access_pressure` | Labour radical support | anti fascist aid and volunteers | client pressure and church backlash |

### Sponsor bands

| Band | Gameplay use |
| --- | --- |
| low | sponsor can offer limited help without dependency |
| useful | sponsor actions stronger, but rival reactions begin |
| dependent | route identity threatened and some neutral or peaceful outcomes blocked |
| compromised | crisis or failure state, anti dependency missions required |

### Player readable direction

The player should see which sponsor has leverage, what action recently raised it, and what kind of action can reduce it. The tooltip should avoid revealing hidden spy follow ups before they fire.

### AI use

AI should avoid having one sponsor dominate unless route identity demands it. Historical AI should balance or refuse leverage. Opposition AI accepts some British access if it gains concrete defence or Northern concessions. Labour AI can accept Soviet pressure only under threat and should later reduce dependence. Blueshirt AI accepts right wing pressure but must not ignore internal crisis. IRA AI accepts German pressure only under rare dangerous route conditions.

## Presentation through ideas

The starting idea lifecycle should visually carry the mechanics.

| Idea family | Presentation role | Changed by |
| --- | --- | --- |
| `shadow_of_civil_war_family` | authority and reconciliation | trunk, Labour, opposition, IRA, Blueshirt |
| `economic_war_strain_family` | economy and foreign trade pressure | settlement, industry, trade decisions |
| `treaty_ports_family` | ports and foreign access | port transfer, access agreements, port defence |
| `small_army_long_coast_family` | preparedness | military, LDF, coast watching, air, naval |
| `divided_island_family` | partition pressure | Northern branch and formation decisions |
| `foreign_access_family` | sponsor pressure | diplomacy and route foreign support |

Idea icons must be distinct from focus icons and decision icons. They should be designed for 64x64 readability and not derived by resizing focus art.

## Tuning and constants direction

Important thresholds, gains, losses, duration bands, AI weights, and sponsor pressure values should be centralized in script constants or a documented tuning file during implementation. The spec does not provide exact constants, but it requires these groups:

- Constitutional Authority component gains and losses.
- Emergency Preparedness component thresholds.
- Partition Pressure, support, alarm, and British willingness bands.
- Foreign Access Pressure sponsor bands.
- Mission duration bands for easy, medium, and hard objectives.
- AI willingness weights for peaceful, cooperation, radical, coercive, and strict neutral routes.
- Integration stage thresholds and resistance penalties.

## Mechanic failure and recovery states

| Mechanic | Recovery path | Runaway failure |
| --- | --- | --- |
| Constitutional Authority | reconciliation, legal reforms, route authority maintenance | armed route crisis, coercive state, or civil authority collapse |
| Emergency Preparedness | stockpile missions, LDF, ports, coast watch, foreign liaison | coerced foreign access, weak invasion response, ration crisis |
| Partition Pressure | arbitration, observer missions, support work, rights package | border violence, failed uprising, British crackdown |
| Foreign Access Pressure | anti dependency missions, domestic industry, balanced diplomacy | client state, exposed spy network, compromised route capstone |

## Localisation handoff direction

Final localisation should describe public action and visible consequence. It should not expose future hidden branches, route variables, or secret event chains. It should mention dynamic actors, sponsors, and state groups where helpful. It must not use unresearched quotes, slogans, song fragments, literary references, or final cultural remarks.
