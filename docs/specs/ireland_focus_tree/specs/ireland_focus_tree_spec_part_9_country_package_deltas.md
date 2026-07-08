# Ireland focus tree spec part 9, country package deltas

Working labels are internal handles only. They are not final localisation.

This part defines the country package changes needed by the Ireland focus tree. It does not create final localisation text, final party descriptions, final focus titles, final slogans, or final quotes. Real historical leaders, real portraits, real flags, and historically attested symbols require sourced asset work.

## Country package design stance

Ireland should remain the main playable tag for most outcomes. Reunification, regime change, Commonwealth cooperation, Labour government, Blueshirt takeover, IRA underground rule, and late game compact leadership can be handled through cosmetic tags, leaders, party changes, laws, ideas, decisions, and focus route flags. A new Irish tag should be avoided unless implementation proves that a separate tag is required for a civil conflict, puppet transfer, or achievement.

Northern Ireland should usually be represented through state modifiers, hidden actors, decisions, and missions. A separate Northern Ireland tag can be created only if the implementation needs an active opposing country, a civil conflict, or a released subject. If created, it needs its own leader, flag, starting forces, AI, and cleanup. It cannot be a generic empty tag.

## Base Ireland package

| Surface | Baseline direction | Route changes |
| --- | --- | --- |
| Tag | Use existing Ireland tag if the repository already has one | avoid tag switch except rare implementation need |
| Tree id | `slopx_ireland_focus_tree` working tree id | route flags steer political branches |
| Capital | Dublin by default | no capital move unless a formable or occupation route later proves it useful |
| Public country identity | Ireland as the direct map name | cosmetic variants for all island settlement, commonwealth cooperation, social republic, corporatist regime, underground republic, and compact leadership |
| Starting government | Fianna Fáil led constitutional government | can shift to Fine Gael legalism, Labour cabinet, corporatist state, IRA military council, or route coalition |
| Starting head of government | Éamon de Valera as historical leader | alternate leaders and councils require sourced portraits or generated symbolic portraits as noted below |
| Head of state presentation | Douglas Hyde becomes relevant after the presidency is established | president should not replace government leader unless the repository uses separate presentation |
| Starting problems | civil war memory, weak defence, partition, small industry, port sovereignty, foreign access risk | each route mitigates or transforms these problems differently |

## Leader and portrait deltas

The list below is an implementation candidate set, not a final character file. The implementation agent should check existing repository characters before adding new ones.

| Working character role | Historical or fictional | Route use | Portrait source mode | Gameplay direction |
| --- | --- | --- | --- | --- |
| `ire_de_valera_leader` | real | historical sovereignty, strict neutrality, constitutional trunk | sourced real portrait | keeps sovereignty, neutrality, constitution, and Emergency authority central |
| `ire_douglas_hyde_president` | real | constitutional presidency and legitimacy events | sourced real portrait | boosts constitutional legitimacy and cultural respect without running cabinet policy |
| `ire_frank_aiken_security_or_defence` | real | defence, G2, Emergency cabinet | sourced real portrait | defence coordination, intelligence, neutrality enforcement |
| `ire_sean_lemass_industry` | real | native industry, state companies, public works | sourced real portrait | industrial development, production line, resource and tariff policy |
| `ire_wt_cosgrave_opposition` | real | Fine Gael constitutional opposition | sourced real portrait | legal opposition, Commonwealth negotiation, parliamentary legitimacy |
| `ire_william_norton_labour` | real | Labour democratic and social reform | sourced real portrait | trade union legitimacy, welfare, social reform, labour diplomacy |
| `ire_eoin_oduffy_blueshirt` | real | Blueshirt corporatist path | sourced real portrait | paramilitary route, corporatist chamber, Spanish volunteer link, high instability risk |
| `ire_ira_military_council` | symbolic or collective | IRA underground route | generated symbolic council portrait unless a real leader is selected and sourced | underground authority, safehouses, cell discipline, exposure risk |
| `ire_emergency_cabinet_body` | symbolic or collective | historical, strict neutral, wartime focus surfaces | generated symbolic institutional portrait only if needed | decision category or event art, not necessarily a country leader |
| `ire_labour_council_body` | symbolic or collective | radical Labour if no single leader should dominate | generated symbolic council portrait | route identity for worker councils if Norton remains parliamentary leader |
| `ire_unified_ireland_civic_body` | symbolic | post settlement all island civic identity if needed | generated symbolic civic portrait or no portrait | integration body for Northern settlement decisions |

Real leader portraits must not be generated. Generated council portraits should use institutional names, not random personal names.

## Party and ideology deltas

Final party localisation belongs to implementation. These are working identity handles and direction.

| Working party handle | Route | Ideology slot direction | Public direction |
| --- | --- | --- | --- |
| `ire_party_fianna_fail` | historical and neutral | democratic or neutrality aligned democratic slot depending repository ideology setup | constitutional republican government focused on sovereignty |
| `ire_party_fine_gael_constitutional` | constitutional opposition | democratic or conservative democratic slot | legal opposition, Commonwealth cooperation, parliamentary order |
| `ire_party_labour_democratic` | Labour democratic | democratic socialist slot if available, otherwise democratic | Labour cabinet, trade union law, welfare, public works |
| `ire_party_labour_social_republic` | Labour radical | communism or socialist revolutionary slot if the repository maps it there | worker councils and social republic, not automatic Soviet client |
| `ire_party_blueshirt_corporatist` | Blueshirt | fascism or authoritarian corporatist slot | National Guard, corporatist chamber, anti communist state |
| `ire_party_ira_underground` | IRA route | non aligned revolutionary or authoritarian republican slot, depending repository ideology model | underground military council seeking all island republic |
| `ire_party_emergency_cabinet` | wartime bridge | non aligned or democratic emergency law state | temporary authority state during invasion or collapse only |

The Fine Gael constitutional route and Blueshirt route must remain separate. Shared anti Fianna Fáil roots do not mean shared route identity.

## Cosmetic identity deltas

| Cosmetic identity handle | Unlock | Country name direction | Flag direction | Cleanup |
| --- | --- | --- | --- | --- |
| `ire_cosmetic_constitutional_ireland` | historical trunk after constitution and presidency | direct constitutional Ireland identity | base tricolour unless a sourced civic variant is justified | remains compatible with neutrality and peaceful settlement |
| `ire_cosmetic_commonwealth_cooperation` | Fine Gael cooperation path | direct Irish state identity with Commonwealth association implied by ideas and diplomacy, not a bloated map name | base tricolour or sourced constitutional variant | remove if Ireland becomes puppet or breaks with Britain |
| `ire_cosmetic_labour_republic` | Labour democratic or social republic capstone | direct social republic identity | generated Labour civic variant only if historical Labour symbols do not supply a sourced flag | remove if Labour loses power |
| `ire_cosmetic_corporatist_ireland` | Blueshirt route lock | direct Irish state identity under corporatist rule | sourced Blueshirt or corporatist symbol if historically attested, generated only for fictional synthesis | remove or replace after counter coup |
| `ire_cosmetic_underground_republic` | IRA route lock | direct republican identity with instability visible through ideas, not a long administrative name | sourced republican motifs required, no invented real symbol claims | convert after civil authority is restored |
| `ire_cosmetic_unified_civic` | all island peaceful settlement | direct unified Ireland identity | tricolour can remain, alternative all island civic flag only if sourced or clearly fictional cosmetic | remove obsolete partition modifiers |
| `ire_cosmetic_unified_coercive` | forceful settlement | direct all island identity under contested rule | route variant flag if justified | keep integration penalties until missions succeed |
| `ire_cosmetic_atlantic_compact_leader` | late game compact leadership | Ireland remains the map name unless a cosmetic all island identity exists | optional compact emblem, not necessarily a flag change | remove compact identity if faction dissolves |

Public names should stay short country names. Internal bodies such as cabinets, councils, chambers, and boards should be ideas, decisions, mechanics, or party names, not map names.

## Advisor and high command deltas

| Advisor family | Candidate roles | Route access | Reward style |
| --- | --- | --- | --- |
| Constitutional cabinet | legal reformer, public order minister, diplomatic negotiator | historical and opposition | authority gain, decision cost reduction, legitimacy, observer mission support |
| Emergency defence | defence coordinator, intelligence chief, reserve organizer | historical, strict neutral, commonwealth, emergency routes | LOP speed, G2 exposure reduction, LDF mission efficiency, port defence |
| Industry and supply | industry minister, Shannon engineer, beet board organizer, turf board planner | all non collapsed routes with branch modifiers | construction decisions, resource projects, supply and fuel resilience |
| Labour and welfare | trade union mediator, housing minister, public works planner | Labour democratic and social republic | strike control, labour support, public works mission effects |
| Commonwealth liaison | British staff liaison, Dominion negotiator, naval access officer | Fine Gael opposition and guarded cooperation | aid corridors, access pressure controls, British trust |
| Blueshirt and corporatist | Guard organizer, corporate chamber theorist, anti communist organizer | Blueshirt only | paramilitary integration, command obedience, legitimacy cost |
| IRA underground | safehouse organizer, arms contact, cell disciplinarian | IRA only | underground network, local support, exposure risk management |
| Northern settlement | observer envoy, minority safeguard negotiator, border survey board | settlement routes | plebiscite, integration, unionist alarm reduction |

Advisor unlocks should match branch identity. Avoid a single generic advisor list that every route buys.

## Starting ideas and lifecycle deltas

Part 1 and part 2 define the main idea lifecycle. Implementation should ensure the country package does not add extra passive spirits beyond those lifecycles.

| Idea family | Starting or unlocked | Route handling | Failure handling |
| --- | --- | --- | --- |
| `civil_war_memory_idea` | starting mixed or negative | historical and democratic routes mitigate through reconciliation, Blueshirt and IRA routes can weaponize it | authority loss, radical pressure, coup or underground growth |
| `weak_defence_forces_idea` | starting negative | Emergency, LDF, port garrison, and army modernization upgrade it | invasion vulnerability and low preparedness |
| `small_native_industry_idea` | starting negative or mixed | Lemass, Labour, Shannon, beet, turf, and native factory routes transform it | dependency, shortages, project delays |
| `partition_pressure_idea` | starting pressure | settlement routes convert pressure into claims, missions, integration, or stable settlement | unionist alarm, British warning, armed crisis |
| `foreign_access_pressure_idea` | hidden or visible mechanic spirit | diplomacy and anti dependency actions control it | sponsor leverage, invasion risk, loss of neutrality |
| `emergency_preparedness_idea` | unlocked by Emergency branch | becomes strong defensive identity after missions | weak if ignored, no free hidden bonus |
| `underground_cells_idea` | IRA route | can become civil authority after settlement | exposure, crackdown, German dependency |
| `corporatist_chamber_idea` | Blueshirt route | authoritarian economic and political identity | strikes, legitimacy loss, opposition crisis |
| `labour_reform_mandate_idea` | Labour route | democratic reform or social republic institutional base | church backlash, sponsor pressure, strike failure |

## Starting military package

The starting Ireland package should feel small, under equipped, and strategically exposed, but not empty. Exact division counts belong to implementation and should follow vanilla balance and repository patterns.

### Starting army concept

- A small regular army built from infantry battalion templates with limited artillery and support.
- Reserve manpower exists as a political and training resource, not as free divisions.
- Starting templates should include a regular infantry template, a smaller local garrison template, and a later LDF reserve template unlocked by focuses.
- Equipment stockpiles should be tight enough that repeated mobilization decisions require choices.
- The initial army should not be able to conquer Northern Ireland without route preparation, British weakness, or major player investment.

### Starting navy concept

- Coastal patrol and port control should matter more than capital ships.
- Use convoys, small patrol vessels, or minimal naval setup according to repository and HOI4 version support.
- Naval growth comes from port decisions, coastal patrol missions, and dockyard projects.
- Britain should react strongly to hostile foreign access in western ports.

### Starting air concept

- Air force starts weak or nearly absent.
- Air defence should be built through anti air, radar, observer posts, limited fighters, and foreign or domestic training decisions.
- No route should receive a large free air force. Foreign air support should increase access pressure.

## Military growth by route

| Route | Unit growth source | Requirements | Risks | AI use |
| --- | --- | --- | --- | --- |
| Historical neutral | LDF reserves, port garrisons, emergency infantry, coastal observers | infantry equipment, support equipment, manpower, state targets, preparedness | equipment shortage, weak training | high during war, moderate in peace |
| Strict neutral | deeper reserves, anti air detachments, coastal patrol | stores, local defence missions, ports controlled | slow industry and no sponsor aid | high if war spreads |
| Commonwealth cooperation | staff trained infantry, air defence, naval liaison, convoy escort | British trust, access limits, convoys, anti dependency | foreign access pressure, dependency | high if Britain at war and trust safe |
| Labour democratic | defence committees, public works logistics units, worker training | labour support, low violence, equipment, legitimacy | strike strain, church backlash | moderate, tied to defensive war |
| Labour social republic | worker defence corps and factory guards | council legitimacy, equipment, authority | Soviet pressure, employer resistance | rare, higher under invasion threat |
| Blueshirt corporatist | National Guard battalions, officer cadres, Spanish veteran memory | command obedience, equipment, route lock | legitimacy loss, coup backlash | rare, aggressive if Britain weak |
| IRA underground | flying columns, safehouse cells, arms dumps | local support, arms, exposure control | crackdown, German dependency, low regular strength | very rare, only route valid |
| Unified civic Ireland | integrated Northern local defence and police transition | settlement success, integration missions | unionist alarm, resistance | after settlement only |
| Atlantic compact | joint training missions and small nation reserves | compact cohesion, recognition, equipment | faction overreach | late game only |

Unit creation must not be a repeated free division loop. Every unit decision should consume equipment, manpower, state control, local support, or mission completion.

## Northern Ireland package if released

A released or active Northern Ireland package should be used only when the implementation needs an active country. Otherwise use state mechanics.

| Surface | Direction |
| --- | --- |
| Tag | reuse existing Northern Ireland tag if present, otherwise define a conflict free custom tag |
| Leader | James Craig for pre 1940, J. M. Andrews after succession if time logic is implemented, both real portraits sourced |
| Ruling party | Ulster Unionist direction |
| Starting ideas | unionist majority government, security apparatus, minority grievance, wartime vulnerability |
| Military | police auxiliaries, local garrisons, limited regular units, British support when valid |
| AI | defend union, ask Britain for guarantees, resist sudden settlement, accept observer settlement only under strict safeguards |
| Flags | source historical Northern Ireland government or Ulster banner handling according to legal and historical source rules |
| Cleanup | annexation, settlement, puppet, or integration must clear local crisis flags and convert state variables |

## Britain package deltas

Britain does not need a new country package, but it needs strategy hooks.

- Strategy plan for Irish port access demand.
- Strategy plan for accepting or rejecting all island settlement.
- Strategy plan for responding to German contact or IRA route.
- Strategy plan for Commonwealth cooperation and anti puppet clause.
- Event or decision hooks for Northern guarantees and unionist pressure.

## Foreign sponsor deltas

Germany, Italy, Spain, the United States, the Soviet Union, and the Vatican should not receive new full focus trees. They need route scoped decision AI, event responses, and possibly advisor or opinion modifiers.

| Actor | Required package delta |
| --- | --- |
| Germany | covert liaison decisions, exposure hooks, Plan Kathleen risk, no clean reward path |
| Italy | Blueshirt corporatist support and Spanish route tie, no broad Irish military aid by default |
| Spain | volunteer memory and civil war route checks only |
| United States | diaspora recognition, trade, postwar support, anti Axis access pressure |
| Soviet Union | Labour social republic recognition and aid with dependency risk |
| Vatican | mediation and legitimacy pressure only, no military sponsor behavior |

## Country package validation requirements

Implementation completion must prove the following.

| Surface | Required proof |
| --- | --- |
| Focus loading | Ireland loads `slopx_ireland_focus_tree` and route locks behave correctly |
| Leaders | every real leader uses sourced portrait or approved existing asset |
| Parties | route changes update ruling party and party popularity without mixing Fine Gael and Blueshirt routes |
| Ideas | starting ideas have lifecycle and route changes remove or transform obsolete forms |
| Forces | starting army, navy, air, and reinforcement route are not empty and not overpowered |
| Northern handling | state mechanics or released tag works without duplicate claims, instant cores, or stale crisis flags |
| Flags | base flags preserved unless route deliberately changes them, all variants have normal, medium, and small files |
| Advisors | route advisors match route identity and do not unlock for incompatible governments |
| AI | route strategy plans respect invalid blockers and cleanup |
