# Ireland focus tree spec, part 5 decision and mission systems

This file defines the major decision and mission systems required by the Ireland focus tree. Working labels are internal handles only. They are not final decision names, mission names, event titles, option text, or localisation.

## Decision design rules

Ireland decisions should represent government work, military preparation, diplomacy, local organizing, or underground action. They should not become a political power store. Every major family should use concrete costs such as equipment, army XP, air XP, navy XP, command power, convoys, trains, fuel, manpower, civilian factory burden, stability, war support, local support, legitimacy, foreign access, or state objectives.

Important missions should require action. Good objectives include holding named states, placing supplied divisions in border states, building coastal defences, completing regional infrastructure, staffing Look Out Posts, stockpiling equipment, opening a foreign aid corridor, preventing foreign penetration, or maintaining observer conditions in Northern Ireland.

Every category must clean up obsolete missions after route changes, war ending, tag switch, annexation, formation, settlement failure, or invalid foreign sponsor state.

## Category map

| Working category | Main player question | Opens from focuses | Clutter control | Major values touched |
| --- | --- | --- | --- | --- |
| `ireland_constitutional_authority_category` | Who has public authority in the state | Opening trunk, political routes | Shows only current route authority tools | Constitutional Authority, armed movement pressure |
| `ireland_emergency_preparedness_category` | Can Ireland defend neutrality and coast | Emergency Skeleton, military branch | Active mission cap by region and phase | Emergency Preparedness, foreign pressure |
| `ireland_ports_and_coast_category` | Who controls and defends the ports | Port Question, Return of the Ports, Port Defence Commands | Hidden until port issue visible | Emergency Preparedness, Britain access |
| `ireland_economic_recovery_category` | How the state builds self sufficiency | Economic War Accounts, industry branch | Projects unlock by region and industry tier | trade dependence, rural distress, supply |
| `ireland_foreign_access_category` | Which foreign powers gain leverage | Diplomacy branch, route foreign focuses | Sponsor cards or target filters | Foreign Access Pressure by sponsor |
| `ireland_partition_settlement_category` | How Ireland pursues the Northern question | Border Survey and route variants | Separate peaceful, pressure, violent, integration phases | Partition Pressure, Northern support, unionist alarm |
| `ireland_route_crisis_category` | How route backlash is controlled | Blueshirt, IRA, Labour, Emergency Cabinet | Route locked and hidden when invalid | legitimacy, unrest, militia pressure |
| `ireland_post_settlement_integration_category` | How new territory becomes stable | Formation or settlement decision | Active missions by Northern state group | integration progress, resistance, legitimacy |

## Constitutional authority category

### Purpose

This category controls Dáil legitimacy, armed movement pressure, emergency executive reach, and public reconciliation. It should be visible from the opening trunk and should evolve by route.

### Decision families

| Decision family | Typical costs and requirements | Timers | Success effects | Failure effects | Cleanup and AI |
| --- | --- | --- | --- | --- | --- |
| `public_order_enforcement_family` | Political power only as a small part. Also command power, infantry equipment for police support, stability risk, and low armed pressure requirement for gentle actions. | 90 to 120 days for campaigns, shorter for urgent incident response. | Lowers armed movement pressure, raises legitimacy if proportionate, can reveal hidden route pressure. | Heavy hand can create martyrs. Weak action lets militia route pressure rise. | Hide after route becomes IRA takeover or corporatist state. Historical AI uses moderate enforcement. |
| `reconciliation_board_family` | Civilian factory burden, local support, manpower for veterans offices, high enough legitimacy. | 120 to 180 days by region. | Upgrades `Shadow of the Civil War`, lowers radical route costs, improves democratic Northern tools. | Failed boards raise old faction memory and can strengthen IRA or Blueshirt access. | AI uses if stability is not collapsing. Missions cancel after civil conflict or hard authoritarian route. |
| `constitutional_campaign_family` | Political power, public support, party popularity, low armed pressure, possible temporary campaign consumer goods burden. | 100 to 150 days before referendum or route lock. | Raises Dáil legitimacy, enables presidency and legal route modifiers. | Failed campaign causes legitimacy loss and opens crisis branches. | AI historical and democratic routes prioritize. Extremist routes do not. |
| `emergency_powers_review_family` | High war tension or war state, parliament support, legal route not collapsed. | 90 days recurring with cooldown. | Raises emergency reach without losing too much legitimacy. | Overuse lowers democratic trust and Labour support. Underuse keeps emergency tools weak. | AI uses when war threat is real and legitimacy is not too low. |
| `route_authority_maintenance_family` | Route specific costs. Labour uses worker support and factory output. Blueshirt uses command power and stability risk. IRA uses safehouses and exposure. Historical uses legitimacy and cabinet time. | 60 to 120 days. | Keeps chosen authority stable and changes cost of route decisions. | Failure raises route crisis and can unlock backlash missions. | Hidden when route not active. AI uses only valid route version. |

### Mission examples

| Mission | State or target logic | Objective | Success | Failure |
| --- | --- | --- | --- | --- |
| `veterans_board_county_mission` | Rotates through provinces or named state groups in the south and west. | Complete reconciliation work while local support stays above threshold. | Civil War idea improves and armed pressure falls. | Local radical pressure rises and route crisis event becomes possible. |
| `public_order_capital_mission` | Capital state and nearby urban state group. | Keep supplied divisions or police capacity present for the timer. | Reduces militia pressure without excessive legitimacy loss. | Street politics event raises IRA or Blueshirt route opening chance. |
| `constitutional_referendum_mission` | Country level. | Maintain legitimacy, keep armed pressure low, and complete campaign decisions. | Opens clean constitutional route lock. | Opens amended, disputed, or coercive constitution outcomes. |

## Emergency preparedness category

### Purpose

This is Ireland's main active defensive layer. It should not be one meter that rises from focuses only. Preparedness should be built through state missions, supply projects, reserve training, port defence, coast watching, air warning, and intelligence work.

### Component values

| Component | How it rises | What it affects | Failure symptom |
| --- | --- | --- | --- |
| `coast_watch_readiness` | LOP missions, support equipment, radio decisions, G2 branch | Sea and air incident response, landing warning | surprise incidents and foreign pressure |
| `reserve_readiness` | LDF missions, regular battalion focuses, equipment and manpower decisions | invasion response, border defence | weak emergency units and low deterrence |
| `supply_readiness` | emergency stores, fuel, trains, trucks, convoys, rationing decisions | long war endurance, mobilisation cost | ration crisis and foreign aid dependence |
| `port_readiness` | port transfer, coastal forts, garrisons, naval stores | port control and British pressure | demands for access and weak coastal defence |

### Decision and mission families

| Family | Costs and requirements | Duration | Success | Failure | AI |
| --- | --- | --- | --- | --- | --- |
| `staff_lop_chain` | support equipment, small manpower, coastal state control, sometimes civilian factory time for posts | 90 to 140 days by coast group | Raises coast watch, improves incident outcomes | Raises surprise risk and foreign pressure | AI prioritizes if coast watch below target and war exists nearby |
| `reserve_training_chain` | infantry equipment, army XP, manpower, local support | 90 to 180 days | Unlocks LDF or route reserve decisions, improves reserve readiness | Creates unreliable reserves or militia drift | AI uses when equipment stockpile is adequate |
| `emergency_stockpile_chain` | infantry equipment, support equipment, trucks, trains, convoys, fuel, civilian factory burden | 120 to 180 days | Raises supply readiness, reduces wartime shortage events | Rationing crisis, lower mobilisation speed | AI uses before joining any risky settlement or war route |
| `port_garrison_chain` | control of port state, divisions present, artillery or support equipment, construction slots | 120 to 180 days | Raises port readiness, adds forts or anti air, reduces access demands | Britain or Germany gains pressure argument | AI uses after ports returned |
| `air_warning_chain` | air XP, aircraft or purchase decision, airbase construction, fuel | 120 to 160 days | Better air incident response and preparedness | airspace incidents damage neutrality | AI uses if industry can support |
| `g2_counter_agent_chain` | legitimacy, intelligence exposure, command power, sometimes political power | 60 to 120 days | Lowers foreign access pressure and reveals spy incidents | Foreign sponsor gains leverage or IRA route exposure | AI uses if foreign access pressure high |

## Ports and coast category

### Purpose

The ports should start as a sovereignty and defence problem. After transfer, the category becomes a port defence and coastal command system. If access is negotiated or coerced, the category changes again.

### Port target groups

| Working state group | Intended scope | Notes |
| --- | --- | --- |
| `cobh_port_group` | Cork harbour and southern approaches | Key transfer and defence target. |
| `berehaven_port_group` | Berehaven and southwest coast | Important for Atlantic approaches and patrol logic. |
| `lough_swilly_port_group` | Lough Swilly and northwest approaches | Links to Northern pressure and British access. |
| `dublin_coast_group` | Dublin and east coast | Capital supply and shipping. |
| `western_coast_group` | Galway, Mayo, western seaboard | Coast watch and patrol depth. |

### Port decision families

| Family | Costs | Success | Failure | Cleanup |
| --- | --- | --- | --- | --- |
| `negotiate_port_transfer_family` | British trust, trade settlement progress, legitimacy, sometimes concession cost | Transfers port control stage, removes starting weakness, unlocks port defence | delayed transfer, higher British demands, war pressure | Hide after transfer, war loss, or hostile route |
| `port_fortification_family` | artillery, support equipment, civilian factory time, state control | Adds coastal forts, anti air, port readiness | construction delay and exposed port | Hide if state not controlled |
| `neutral_port_access_rules_family` | legitimacy, foreign access pressure checks, war state | Sets limited access, refusal, or inspection policy | sponsor anger, pressure gain | Replace after faction entry or route collapse |
| `naval_stores_family` | convoys, dockyard burden, fuel, trains | Improves naval service and port readiness | supply loss or dockyard delay | Reset after port lost |
| `coastal_patrol_family` | convoys, fuel, naval XP, patrol craft or dockyard time | Reduces smuggling, spy risk, and incident severity | convoy losses or smuggling exposure | Cooldowns and invalidation by war state |

## Economic recovery category

### Purpose

The economic decision layer should make industry geographically grounded. Focuses unlock project tiers. Projects should name or tooltip the relevant regions, and they should use construction capacity, tradeoffs, and local support rather than repeated factory rewards.

### Project families

| Family | Unlock | Target logic | Cost model | Outcome | Risk |
| --- | --- | --- | --- | --- | --- |
| `rural_relief_projects` | Tariff Scars, Civil War Wounds | rural state groups | civilian factory burden, political legitimacy, local support | rural distress falls, infrastructure or slots improve | if delayed, Labour or armed pressure rises |
| `native_factory_projects` | Native Manufactures | urban and port state groups | civilian factories, imports, trade dependence, industry advisor | factory or production line setup | sponsor dependence if imports needed |
| `shannon_grid_projects` | Shannon Power | Shannon, Limerick, midlands, west connectors | construction capacity, steel or import pressure, time | infrastructure and industrial capacity | wartime import shortage delays |
| `sugar_beet_projects` | Sugar Beet Belt | Carlow, Mallow, Tuam, Thurles style state groups | local support, civilian factory time, rural labour | rural factory, supply resilience, food security | overexpansion uses labour and trains |
| `turf_projects` | Turf and Bog Development | midlands and bog state groups | manpower, trains, infrastructure, civilian burden | fuel or supply resilience | productivity loss and limited efficiency |
| `port_economy_projects` | Port Led Recovery | port states | dockyard time, convoys, trade access | dockyards, repairs, convoys, trade | wartime shipping loss |
| `emergency_stores_projects` | Emergency Stores | country or regional depots | equipment, trucks, trains, fuel | supply readiness and ration resilience | if failed, ration crisis |

### AI economic behavior

Ireland AI should not start every project at once. It should use project phases. Early AI solves rural distress or trade settlement. Middle AI builds one main industry track and one supply track. Wartime AI prioritizes stores, ports, and LDF support. Labour AI prefers cooperative and rural projects. Opposition AI prefers trade and port recovery. Historical AI balances self sufficiency and trade. Blueshirt AI prioritizes disciplined factory and military supply projects. IRA AI prioritizes clandestine supply and border depots.

## Foreign access pressure category

### Purpose

Foreign access is a multi sponsor pressure system. It should not be a simple opinion modifier. Each sponsor can provide real help, but help creates leverage and can block other routes.

### Sponsor components

| Sponsor | Appears through | Useful support | Pressure risk | Route notes |
| --- | --- | --- | --- | --- |
| Britain | ports, trade, defensive cooperation, Northern settlement | trade, port transfer, defence access, guarantees | base demands, dependency, settlement veto | central to historical and opposition |
| Germany | IRA contact, spy incidents, rare diplomatic channel | equipment, intelligence, anti Britain leverage | exposure, legitimacy collapse, British intervention | risky and unstable |
| Italy and Spain | Blueshirt route, Catholic corporatist diplomacy | advisors, anti communist support, volunteer memory | democratic isolation, sponsor collapse | route locked |
| United States | diaspora, observers, trade, postwar diplomacy | recognition, aid, observer leverage | sponsor pressure and British suspicion | broad democratic access |
| Vatican | church diplomacy, conservative social legitimacy | domestic support, mediation, social legitimacy | Labour resistance, rights pressure | historical, opposition, Blueshirt, Labour conflict |
| Soviet Union | Labour radical route | anti fascist aid, advisors, volunteers | client pressure, church backlash, democratic suspicion | optional Labour radical |

### Decision families

| Family | Cost and requirement direction | Success | Failure | AI |
| --- | --- | --- | --- | --- |
| `recognition_mission_family` | legitimacy, diplomatic staff, low contradictory sponsor pressure | raises recognition and route legitimacy | rival sponsor leverage or embarrassment | AI uses when route needs arbitration or formable support |
| `aid_corridor_family` | convoys, access, relation threshold, foreign sponsor alive and not overextended | equipment or industry support, raises access pressure | convoy loss, dependency, rival reaction | AI balances support against dependency |
| `foreign_liaison_family` | political staff, route lock, war state, trust | advisors, intelligence, volunteer permission | spy exposure or public backlash | AI avoids if route incompatible |
| `anti_dependency_family` | high legitimacy, domestic industry, political cost | lowers sponsor pressure and preserves independence | sponsor anger and aid reduction | AI uses before capstone if pressure high |
| `expose_rival_patronage_family` | intelligence capacity, target sponsor pressure, evidence variable | reduces rival access and boosts own legitimacy | diplomatic incident | AI uses against rival sponsor only when safe |

## Partition settlement category

### Purpose

Partition is the expansion branch, but it must be objective driven. The category should move through survey, support, negotiation or pressure, settlement attempt, and integration.

### Values

| Value | Meaning | Raised by | Lowered or stabilized by |
| --- | --- | --- | --- |
| `partition_pressure` | How active the Northern question is | border agitation, war, British weakness, IRA or Blueshirt route | arbitration, restraint, cross border agreements |
| `northern_nationalist_support` | Local support for Dublin aligned settlement | committees, labour networks, observer missions | failed raids, repression, sectarian backlash |
| `unionist_alarm` | Resistance and mobilization against Dublin pressure | violent actions, poor safeguards, foreign sponsors | minority protections, restraint, Britain trust |
| `british_settlement_willingness` | London readiness to negotiate | Britain weakness, trust, Ireland cooperation, postwar pressure | Irish violence, Axis or Soviet dependency, unionist alarm |
| `integration_progress` | Post settlement administrative work | missions and state control | resistance, low legitimacy, rushed cores |

### Peaceful mission families

| Family | Duration | State targets | Requirements | Success | Failure |
| --- | --- | --- | --- | --- | --- |
| `border_survey_missions` | 90 to 120 days | border crossings and Northern state group | legitimacy and no active border war | reveals state requirements and lowers later cost | raises unionist alarm if mishandled |
| `nationalist_committee_missions` | 120 to 180 days | Belfast, Derry, border counties | political support, funds, low violent pressure | raises Northern support | repression and British suspicion |
| `observer_plebiscite_missions` | 180 to 365 days | Northern Ireland state group | high legitimacy, low armed pressure, British willingness | unlocks settlement decision or staged transfer | vote invalid, alarm rises, route cooldown |
| `boundary_commission_missions` | 180 days | border county groups | legal route, British trust or international support | claims or negotiation leverage | frozen border and legitimacy loss |
| `minority_rights_package_missions` | 120 days | country level and Northern state group | political route not extremist | lowers unionist alarm, improves integration | backlash and harder post settlement missions |

### Violent mission families

| Family | Duration | State targets | Requirements | Success | Failure |
| --- | --- | --- | --- | --- | --- |
| `border_incident_missions` | 60 to 120 days | border states | divisions present, equipment, route lock | raises pressure and may unlock ultimatum | British warning and unionist mobilization |
| `northern_uprising_missions` | 120 to 180 days | Belfast, Derry, border county groups | high local support, IRA route, safehouses, equipment | uprising or temporary control | crackdown, exposure, and loss of support |
| `ultimatum_preparation_missions` | 120 to 180 days | border, ports, capital | Blueshirt route, military readiness, Britain weakness | unlocks ultimatum decision | Britain guarantee and internal opposition |
| `occupation_stabilization_missions` | 180 days or more | newly controlled Northern states | garrisons, equipment, legitimacy or command | lowers resistance and opens integration | resistance and foreign condemnation |

## Route crisis category

### Labour crisis family

Labour crises should come from employer resistance, church pressure, strike discipline, and foreign suspicion. Decisions should balance production, legitimacy, and coalition cohesion. Costs should include factory output, stability, local support, and political capital. Failure should not simply remove stability. It should strengthen rival routes or reduce worker control.

### Blueshirt crisis family

Blueshirt crises should come from labour strikes, republican resistance, foreign isolation, and party moderates. Decisions should cost command power, equipment, stability, and legitimacy. Repression should work in the short term but raise long term unrest and international isolation.

### IRA crisis family

IRA crises should come from spy exposure, uncontrolled sabotage, German dependency, British counter pressure, and civil authority collapse. Decisions should require safehouse support, equipment, intelligence, and legitimacy. Failure can turn absorption into crackdown or hard takeover into collapse.

### Historical emergency crisis family

Historical crises should come from war incidents, shipping losses, belligerent aircraft, deserter issues, rationing, and foreign diplomatic pressure. Decisions should cost supply, legal authority, fuel, convoys, and legitimacy. Success preserves neutrality. Failure raises foreign access pressure and can open emergency cooperation or coercion paths.

## Post settlement integration category

### Integration rules

No Northern state should become a full core instantly through focus alone. A focus can prepare the settlement. The formation or settlement decision verifies control or agreement. Integration decisions and missions then grant staged claims, local administration, compliance, resistance reduction, and eventual cores.

### Integration families

| Family | Requirements | Cost model | Success | Failure | AI |
| --- | --- | --- | --- | --- | --- |
| `police_transition_family` | state control or settlement flag, low active war pressure | manpower, infantry equipment, support equipment, legitimacy | lower resistance and unlock administration | unrest and foreign criticism | AI uses first after settlement |
| `local_administration_family` | police transition started, civilian factories, local support | civilian burden, political legitimacy, time | integration progress and reduced costs | corruption or local backlash | AI uses when stability adequate |
| `minority_rights_family` | non extremist route or route specific safeguards | political capital, legal authority, possible stability cost | lowers unionist alarm and improves legitimacy | slows integration but prevents uprising | AI democratic routes prioritize |
| `frontier_security_family` | supplied divisions in border and Belfast or Derry groups | infantry equipment, command power, garrison objective | secure border and reduce sabotage | resistance and raids | AI uses during unrest |
| `infrastructure_integration_family` | controlled state, construction capacity, trains | civilian factories, trains, steel imports if needed | rail, infrastructure, supply hub, later core progress | supply penalties and resentment | AI uses when not in crisis |
| `constitutional_integration_family` | high legitimacy or route authority, peace | constitutional authority, political cost | staged cores and national idea upgrade | legitimacy loss and frozen claims | AI waits until resistance low |

## Cleanup rules

- Hide all sponsor decisions when the sponsor no longer exists, is capitulated beyond useful support, or is ideologically incompatible with the route.
- Cancel Northern peaceful missions when Ireland enters a violent Northern war, accepts extreme foreign dependency, or loses legitimacy below the route floor.
- Cancel violent Northern missions when Britain or Northern Ireland is already defeated, annexed, or settlement has been reached.
- Clear temporary selected targets after route changes, state owner changes, tag switching, civil war, or formation.
- Close port transfer decisions after all three ports are transferred, permanently leased, or lost through route failure.
- Replace early industry projects with stronger later project versions rather than showing all tiers at once.
- Keep active mission caps. Suggested caps are two emergency missions, two industry missions, one foreign sponsor mission, and two Northern missions unless a crisis demands otherwise.
