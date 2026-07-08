# Ireland focus tree spec part 10, hidden paths

This file is the canonical hidden path specification. It supersedes earlier notes that treated hidden cultural restoration as queued or rejected by default. The user has ruled that hidden paths are required. The Ireland package includes planned hidden paths with discovery rules, route locks, gameplay loops, AI limits, assets, achievements, and failure states.

All focus labels in this file are working labels only. They are not final localisation.

## Hidden path design ruling

Hidden paths are accepted design surfaces. They must not be random prizes, unmarked cheat routes, or cosmetic rewards. A hidden path becomes valid only when the player has created the public conditions that make it believable.

A hidden path should reveal itself through visible country behavior:

- completed public focuses that point toward the route without naming the final secret
- mechanic thresholds that the player can read and manage
- decisions or missions that ask for concrete work
- an event, report, or focus reveal only when the state of the country makes the reveal earned
- AI strategy that keeps rare routes rare and blocks impossible choices

Hidden does not mean unsupported. Every hidden route needs asset direction, decision or mission hooks, AI behavior, cleanup, achievement tracking, and disqualifiers.

## Hidden route families

| Hidden family | Route role | Entry condition | Main payoff | Main risk | AI access |
| --- | --- | --- | --- | --- | --- |
| `hidden_civic_cultural_restoration` | cultural and constitutional identity route | high Constitutional Authority, cultural branch progress, low armed pressure, low foreign dependency | civic cultural republic identity, language institutions, Northern reconciliation tools, diplomatic prestige | cultural overreach raises Partition Pressure and lowers authority | very rare, only historical or democratic high legitimacy AI |
| `hidden_emergency_directorate` | crisis state and security route | Constitutional Authority collapse risk, high Emergency Preparedness, war pressure, foreign access danger | stronger neutral survival, LDF and G2 control tools, invasion resilience | democratic damage, unionist alarm, armed pressure | rare crisis AI only |
| `hidden_atlantic_neutral_compact` | late diplomacy and conference route | strict neutrality, ports controlled, low sponsor dependency, high preparedness, war pressure around Atlantic | neutral conference or faction concept with member goals, shared observation, shipping protections | compact seen as a major power proxy or weak talk shop | rare, state validated, no formable country |
| `hidden_common_platform_settlement` | Northern civic settlement variant | cultural route or Labour legal route, low coercion, high local support, outside observers | settlement path that lowers unionist alarm without war | sectarian framing or pressure failure blocks the path | player favored, AI very rare |
| `hidden_corrupted_restoration_failure` | trap and failure branch | cultural route attempted with low authority or high armed pressure | blocks fantasy route abuse, creates emergency correction work | cultural institutions become propaganda shells and raise crisis pressure | AI disabled |

## Discovery and reveal rules

Hidden paths use a reveal ladder rather than a single event. The implementation should avoid showing hidden focus names or secret end states before the player earns them.

| Reveal stage | What the player sees | Required public action | Hidden state effect |
| --- | --- | --- | --- |
| Stage 0, dormant | ordinary cultural, emergency, or neutrality tooltips | none | hidden route flags are absent |
| Stage 1, suggested | a decision category hint or spirit tooltip notes a possible institutional direction | completes public focus family and reaches a relevant value band | sets hidden candidate flag |
| Stage 2, testing | targeted missions appear with practical requirements | player spends resources, holds states, lowers pressure, or proves neutrality | route progress variable begins |
| Stage 3, reveal | hidden focus group or decision family appears | progress threshold met and disqualifiers absent | branch becomes visible |
| Stage 4, commitment | route lock focus or decision asks for a public commitment | final threshold, cost, and risk check | route commitment flag set |
| Stage 5, capstone | identity, faction, emergency cabinet, or settlement payoff | route missions completed | cleanup removes obsolete actions |

Reveal text should explain public action and visible consequence. It must not reveal secret follow ups in ordinary tooltips.

## Hidden path one, civic cultural restoration

### Playable promise

This route turns the cultural revival thread into a real civic state project. It should draw from constitutional language status, the presidency, cultural organizations, Gaeltacht policy, public education, and cross community cultural work. It must not become occult content, a meme monarchy, or a high kingship power fantasy.

The route is strongest when it stays civic and constitutional. A player earns it by keeping parliamentary authority high, controlling foreign access, solving or calming Partition Pressure, and investing in cultural institutions without letting armed groups claim the revival.

### Historical anchors

The route may use the 1937 constitutional language status as a legal anchor. Article 8 identifies Irish as the national language and first official language, with English recognized as a second official language. The route may also use Douglas Hyde and Gaelic League history as civic anchors. Source review is required before any final wording, slogan, quote, or cultural remark is written.

The National Library of Ireland notes that Hyde chaired the foundation meeting of the Gaelic League in 1893, that Eoin MacNeill convened it, and that Hyde became first president. It also describes the organization as non political and non sectarian. This is useful for a hidden Northern civic branch, but the implementation must source exact wording before using any direct language.

### Entry gate

The route can be revealed when all of these public conditions are true:

- Ireland has completed the constitutional trunk and preserved or restored high Constitutional Authority.
- Ireland has not committed to Blueshirt corporatism, Army Council rule, German dependency, Soviet dependency, or permanent foreign basing.
- Armed pressure is low or has been absorbed into legal institutions.
- Emergency law is not in a directorate or permanent authoritarian state.
- The cultural policy opener, presidency focus, or public education focus group has been completed.
- Partition Pressure is below crisis level or the player has started a non coercive Northern settlement path.

Optional strengthening conditions:

- Douglas Hyde is visible as president or cultural figure.
- The player has completed Gaeltacht, education, or civil service decisions.
- The player has kept strict neutrality or finished a peaceful settlement.
- Labour or Fine Gael constitutional routes can enter if they preserve constitutional rule and avoid extremist patronage.

Disqualifiers:

- Blueshirt corporate state capstone.
- IRA Army Council takeover.
- emergency directorate entrenched beyond its temporary recovery path.
- high Foreign Access Pressure from any sponsor.
- violent Northern war before reconciliation missions are complete.
- Constitutional Authority below the restoration floor.

### Focus architecture

| Working focus group | Purpose | Unlocks | Route lock | Reward direction | Linked decisions or missions | AI behavior | Failure state | Asset direction |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| `irl_hidden_cultural_threshold` | hidden reveal gate | reveals cultural candidate decisions | requires high authority and low dependency | shows hidden path hint through spirit tooltip | none at first | AI can satisfy but rarely reveals | if authority falls, hint disappears | no special icon until revealed |
| `irl_presidential_cultural_patronage` | connect presidency to cultural legitimacy | cultural patronage advisor slot, Hyde related source asset if used | incompatible with authoritarian takeover | improves authority component and lowers cultural mission cost | `cultural_patronage_program` | historical AI rare if stable | if president removed by coup, route closes | sourced portrait, state book, civic harp motif |
| `irl_first_official_language_program` | legal language administration | bilingual civil service missions | constitutional route only | upgrades Constitutional Authority tooltip and opens admin projects | `build_bilingual_civil_service` | AI uses if high stability | overreach raises public strain | sourced constitutional book or generated symbolic icon after source review |
| `irl_gaeltacht_development_board` | link culture to industry and rural development | rural infrastructure and school projects | compatible with Labour and historical routes | adds map work in western states, rural factories, transport, education support | `gaeltacht_service_routes`, `rural_school_expansion` | AI uses if civilian capacity exists | failed projects raise rural disappointment | idea icon direction: road, schoolhouse, coast |
| `irl_civic_revival_without_a_crown` | define civic, non monarchical route identity | cultural restoration route lock | blocks mythic monarchy branch | changes cosmetic identity only if implementation supports it, with no tag switch | closes fantasy overreach decisions | AI historical and democratic only | if armed pressure rises, route can corrupt | focus icon direction: open constitution and harp, source review for harp |
| `irl_common_platform_outreach` | connect cultural route to Northern reconciliation | cross community missions and observer work | requires low coercion | reduces unionist alarm and opens hidden settlement variant | `cross_community_language_contacts`, `minority_guarantee_charter` | AI very rare, only peaceful | failure raises Partition Pressure | decision icon direction: two hands and schoolbook, no slogans |
| `irl_cultural_diplomacy_abroad` | use culture as small state diplomacy | diaspora and neutral observer tools | requires low sponsor dependency | improves recognition and lowers foreign access pressure | `invite_cultural_observers`, `diaspora_education_links` | AI uses if compact candidate | sponsor overuse creates dependency | focus icon direction: island, book, Atlantic line |
| `irl_civic_restoration_capstone` | finish hidden route | final civic cultural state package | mutually exclusive with directorate, corporate state, Army Council | upgrades cultural idea, unlocks achievement tracking, improves peaceful integration | closes unfinished cultural missions | AI rare closure only | if Partition Pressure high, capstone blocked | animated route seal optional, static fallback required |

### Decision and mission loop

The civic cultural route must have a decision loop. It cannot be a set of focuses that only grant legitimacy.

| Decision or mission family | Type | Cost or requirement | Success | Failure | Cleanup |
| --- | --- | --- | --- | --- | --- |
| `build_bilingual_civil_service` | staged decision | civilian factory burden, administration time, high authority | upgrades cultural idea and reduces future integration costs | raises public strain if authority is weak | hidden after capstone or authoritarian route |
| `gaeltacht_service_routes` | timed mission | build or improve infrastructure in western state group, spend trains or trucks if used | adds rural development and raises cultural progress | lowers rural trust and delays capstone | removes after development board completion |
| `rural_school_expansion` | decision pool | civilian capacity, stability floor, local support | improves manpower recovery and education related research bonus direction | raises strain if repeated too quickly | replaced by stronger late projects |
| `cross_community_language_contacts` | Northern mission | low Partition Pressure, observer access, no border war | lowers unionist alarm and unlocks common platform settlement | exposes cultural route as nationalist pressure and raises alarm | cancelled by violent route |
| `minority_guarantee_charter` | decision | high authority, low armed pressure, Northern local support | opens hidden settlement variant and integration protections | authority hit and Partition Pressure gain if failed | completed or cancelled after settlement |
| `diaspora_education_links` | diplomacy decision | convoys or civilian capacity, US or diaspora contact, low dependency | improves recognition and reduces foreign access pressure | sponsor leverage rises if overused | ends if major sponsor dependency occurs |

### Idea lifecycle

| Idea | Start or unlock | Role | Upgrade path | Failure path | Final form direction |
| --- | --- | --- | --- | --- | --- |
| `cultural_revival_networks` | hidden cultural opener | positive but fragile network | presidency and language program | propaganda capture if authority low | civic cultural institutions |
| `bilingual_administration_program` | language program | administrative capacity and integration tool | civil service missions | public strain and local resistance | bilingual service corps |
| `gaeltacht_development_board` | development branch | rural industry and infrastructure | service route missions | rural disappointment | rural cultural economy |
| `common_platform_contacts` | Northern outreach | settlement support | minority charter success | unionist alarm | cross community settlement office |

Do not create a new idea for every focus. Use staged upgrades and decision hooks.

### Northern settlement interaction

The cultural route can unlock `hidden_common_platform_settlement` only if it avoids sectarian pressure. It should not bypass the main Northern settlement requirements. It can reduce costs, lower unionist alarm, and unlock observer missions, but state control, treaty acceptance, or plebiscite requirements still need decision verification.

The common platform variant should support:

- minority guarantee decisions
- cross border school or civil society missions
- observer backed local administration
- slower but safer integration
- no instant cores
- failure states when local trust collapses

### Country identity and formable limits

This route may allow a civic cosmetic identity for Ireland or unified Ireland. It must not create a separate formable country unless a later accepted improvement loop addendum proves a map control and identity reason.

Allowed identity changes:

- cosmetic name direction that emphasizes civic cultural renewal after source review
- flag remains the state tricolour by default unless a sourced and justified route variant is approved
- president or cultural patron visible through sourced portraits if used
- party names and institutions can change only through constitutional route logic

Forbidden identity changes:

- no invented high kingship state as a normal payoff
- no occult or mythic government
- no ethnic exclusion mechanics
- no Gaelic slogan or motto without text research
- no instant all island cores through cultural focus alone

## Hidden path two, Emergency Directorate

### Playable promise

This is a crisis route, not an ideology route. It appears when parliamentary authority is strained, foreign access pressure is dangerous, and the Emergency apparatus is strong enough to take control. It gives Ireland survival tools under invasion or major war pressure, but it damages democratic legitimacy and makes Northern settlement harder.

The route must remain separate from Blueshirt corporatism and the IRA route. It is a state security path based on Emergency cabinet powers, G2, LDF, coast watching, port defence, and military discipline.

### Entry gate

The directorate candidate can appear when:

- Emergency Preparedness is high or critical.
- Constitutional Authority is below a crisis threshold or falling quickly.
- Ireland faces invasion risk, nearby major war, foreign espionage, or port pressure.
- G2, LDF, coast watch, or port defence focus groups are developed.
- Ireland has not already become Blueshirt, Army Council, or a foreign client.

It should never appear as an easy shortcut in a stable peaceful campaign.

### Focus architecture

| Working focus group | Purpose | Unlocks | Route lock | Reward direction | Linked decisions or missions | AI behavior | Failure state | Asset direction |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| `irl_emergency_directorate_warning` | hidden crisis gate | directorate warning missions | authority low and emergency high | opens temporary emergency decisions | `emergency_authority_review` | AI checks invasion risk | if ignored, armed pressure rises | warning seal, static only |
| `irl_g2_central_files` | intelligence consolidation | counter espionage and sponsor cleanup tools | no foreign client route | lowers Foreign Access Pressure and raises emergency reach | `clean_foreign_cells`, `intercept_couriers` | AI uses against Germany or IRA danger | overuse lowers authority | generated file cabinet and radio icon |
| `irl_ldf_command_transfer` | LDF under central command | reserve command missions and emergency units | directorate candidate | improves defence, ties down manpower | `centralise_ldf_units`, `guard_ports_with_ldf` | AI uses if invasion threat | poor supply causes readiness loss | LDF armband style requires source review if real |
| `irl_emergency_public_order` | public order policy | censorship and public order decisions | incompatible with Labour civil liberty route | lowers armed pressure but hurts authority | `temporary_public_order_controls` | crisis AI uses | high use triggers restoration demand | generated emergency notice icon without readable text |
| `irl_directorate_commitment` | route lock | temporary directorate government package | locks democratic cultural route while active | stronger survival, worse diplomacy | activates directorate cleanup chain | AI rare crisis only | if war threat fades, legitimacy crisis | institutional council portrait generated if leader changes |
| `irl_restore_civilian_rule` | recovery fork | return path to constitutional government | requires threat reduced | restores authority and closes directorate | `civilian_rule_timetable` | AI prefers after threat | failed timetable entrenches route | ballot and emergency seal icon |
| `irl_permanent_security_state` | harsh fork | authoritarian neutral state | high foreign access and low authority | stronger internal control, worse Northern settlement | security integration missions | AI nearly never | route can isolate Ireland | darker council icon, no real fascist symbols |

### Decision and mission loop

| Decision or mission family | Type | Costs and requirements | Success | Failure | Cleanup |
| --- | --- | --- | --- | --- | --- |
| `emergency_authority_review` | timed mission | stabilize authority within a deadline | prevents directorate commitment and restores normal route | directorate commitment becomes available or forced by crisis | removed after authority recovered |
| `clean_foreign_cells` | decision | G2 progress, command power, intelligence exposure, stability risk | lowers Foreign Access Pressure and exposes sponsor actions | raises diplomatic backlash if abused | hidden after sponsor pressure solved |
| `intercept_couriers` | mission | supplied units or police in port and border state groups | blocks Plan Kathleen style escalation | compromised event chain advances | cancelled after IRA or Germany invalid |
| `centralise_ldf_units` | decision | manpower, infantry equipment, command power, local support | strengthens LDF idea and raises preparedness | lowers authority if used for politics | replaced by regular reserve law after recovery |
| `guard_ports_with_ldf` | timed objective | supplied divisions in port state group | raises port readiness and reduces invasion risk | port vulnerability rises | removed when war threat ends |
| `civilian_rule_timetable` | recovery mission | authority above recovery floor, threat reduced | returns to constitutional route and removes directorate penalties | entrenched security state branch opens | one time |

### Balance and failure

The directorate must help survival enough to matter. It can improve port defence, counter espionage, reserve coordination, and temporary public order. It must also create visible costs:

- lower democratic legitimacy
- higher Partition Pressure if public order actions are heavy
- worse Labour and cultural route compatibility
- higher unionist alarm
- risk of a permanent security state if the player refuses recovery

This route should not generate repeated free divisions. It should create emergency units through LDF decisions with manpower, equipment, supply, and state placement requirements.

## Hidden path three, Atlantic neutral compact

### Playable promise

This path lets a strict neutral or high credibility Ireland build a late wartime or postwar compact for small state observation, shipping protection, arbitration, and anti basing principles. It is a conference or faction concept. It is not a formable country and must never become an Atlantic state tag.

The compact is earned through high neutrality credibility, port control, low sponsor dependency, and diplomatic restraint. It should appeal to players who want Ireland to shape the war without joining a major faction.

### Entry gate

The compact can be revealed when:

- Ireland has recovered and controls the Treaty Ports.
- Ireland has high Emergency Preparedness and coast watch coverage.
- Ireland is not in a major faction.
- Foreign Access Pressure is low or balanced.
- Ireland has completed neutral observer, Washington, London, Vatican, or small state diplomacy branches without becoming a client.
- A major war or postwar conference state makes small state neutrality relevant.

The compact must require at least two eligible partners or observers before faction creation. If there are not enough eligible partners, it remains a conference decision set rather than a faction.

### Focus architecture

| Working focus group | Purpose | Unlocks | Route lock | Reward direction | Linked decisions or missions | AI behavior | Failure state | Asset direction |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| `irl_hidden_neutral_conference_gate` | reveal candidate | compact conference decisions | strict neutral credibility | opens diplomacy category hint | `sound_out_neutral_observers` | AI rare if stable | no eligible partners hides it | simple compass icon |
| `irl_atlantic_shipping_observers` | shipping observation | convoy and coast watch liaison | no permanent foreign bases | shared convoy incident missions | `arbitrate_shipping_incident` | AI uses if convoy threat high | sponsor anger raises pressure | binoculars and convoy icon |
| `irl_small_state_arbitration_office` | arbitration institution | diplomatic missions with members | low dependency | raises recognition and compact cohesion | `host_arbitration_session` | AI uses with trust | weak session lowers cohesion | office seal, no readable text |
| `irl_neutral_basing_principle` | anti base rule | shared no basing guarantee | incompatible with Allied basing route | reduces foreign access pressure and blocks base deals | `deny_permanent_basing_requests` | AI historical if strict neutral | refusal may anger majors | locked harbour and scale icon |
| `irl_compact_member_rules` | member logic | member invite pool and refusal logic | requires two eligible partners | creates compact cohesion value if faction exists | `invite_small_state_observer`, `guarantee_neutral_port_rights` | AI target checks strict | no members downgrades to conference | faction emblem generated |
| `irl_atlantic_compact_capstone` | final compact or conference | faction or persistent conference modifier | cannot form country | shared defensive observation, arbitration, achievement | closes obsolete observer decisions | AI very rare | collapse creates diplomatic embarrassment | animated compact seal optional |

### Member and observer logic

Eligible partners should be checked dynamically. The implementation can use nearby neutral or small state actors when valid. It must avoid inviting non existing countries, puppets without autonomy, countries at war in a way that makes neutrality nonsensical, or major faction leaders who would turn the compact into a proxy.

Potential target groups:

- neutral European states that remain independent
- Latin American or Atlantic observers only if diplomacy justifies it
- the United States as observer only before direct faction alignment or when it fits route state
- Britain as a limited observer only when Irish sovereignty and port control remain intact
- the Vatican only as a diplomatic observer if route relevant, not as a military member

The compact should have a cohesion or credibility value if implemented as a faction mechanic. Low cohesion blocks shared action. High cohesion unlocks arbitration, observer, or maritime support decisions. Member count must matter.

### Decisions and missions

| Decision or mission family | Type | Costs and requirements | Success | Failure | Cleanup |
| --- | --- | --- | --- | --- | --- |
| `sound_out_neutral_observers` | targeted decision | diplomatic capital, relations, low dependency | creates candidate observer | target refusal raises cooldown | hidden if target invalid |
| `arbitrate_shipping_incident` | timed mission | convoy access, coast watch coverage, no sponsor dependency | raises compact credibility and lowers foreign access pressure | incident worsens and major pressure rises | closes after war or target invalid |
| `host_arbitration_session` | decision | civilian factory burden, high authority, member count | raises cohesion and recognition | low attendance damages credibility | cooldown and member validity check |
| `deny_permanent_basing_requests` | decision response | no basing principle active | blocks base access and raises neutral credibility | angers requesting major | obsolete if Ireland joins faction |
| `invite_small_state_observer` | targeted decision | member rules focus, target neutrality | adds observer or member | refusal cooldown | invalid target cleanup |
| `guarantee_neutral_port_rights` | mission | hold ports and maintain readiness | strengthens compact and coast defence | port loss collapses route | removed if ports lost or Ireland joins faction |

## Hidden path four, common platform settlement

### Playable promise

This is a hidden settlement variant, not a separate ideology. It appears when Ireland has built cultural legitimacy, Labour legal support, or constitutional opposition trust while keeping coercion low. The route should use civic guarantees and observer work to make a peaceful Northern settlement more plausible.

The route should make the Northern path more demanding in time and missions, but less likely to produce resistance after success.

### Entry gate

Required conditions:

- low armed pressure
- low coercive route flags
- Northern local support progress
- observer access or London talks progress
- common platform outreach or Labour cross border support
- no border war and no IRA uprising route

### Settlement package

| Settlement element | Purpose | Gameplay effect | Failure |
| --- | --- | --- | --- |
| `minority_guarantee_charter` | reassure unionist and Protestant communities | lowers unionist alarm and integration costs | failure raises Partition Pressure |
| `observer_backed_plebiscite` | verify legitimacy | lets a peaceful settlement decision count more strongly | failed vote locks peaceful path for a period |
| `local_service_continuity` | avoid administrative shock | reduces post settlement resistance | high cost in civilian capacity and time |
| `cultural_nonsectarian_committee` | keep cultural route from becoming sectarian | unlocks common platform achievement | if armed groups dominate, route closes |

This path should never hand over Northern states for free. It changes the difficulty curve by replacing war preparation with diplomacy, local support, observer conditions, and integration missions.

## Hidden failure branch, corrupted restoration

### Purpose

This branch prevents hidden cultural content from becoming an exploit or fantasy route. If the player tries to force cultural restoration while authority is low, armed movements are strong, or foreign pressure is high, the cultural route can corrupt into a failure state.

### Trigger conditions

- cultural restoration candidate flag exists
- Constitutional Authority falls below the failure floor
- armed pressure rises above the failure threshold
- violent Northern action or foreign dependency occurs before civic route commitment
- emergency directorate or extremist route uses cultural institutions as propaganda

### Effects

The failure branch should:

- lock civic cultural capstone
- worsen cultural idea into a propaganda or public strain form
- raise Partition Pressure
- lower foreign trust
- open recovery decisions that can return to normal routes but not to the hidden capstone
- create achievement disqualifier flags

It should not create a powerful extremist cultural state. It is a failure and recovery route.

## Hidden path AI rules

| AI actor | Cultural restoration | Emergency directorate | Atlantic compact | Common platform settlement | Invalid route blockers |
| --- | --- | --- | --- | --- | --- |
| historical Ireland AI | very rare, only if high authority and peaceful | crisis only if invasion risk and authority low | rare if strict neutral and ports safe | rare if Northern pressure low | no extremist route, no sponsor dependency |
| democratic opposition AI | possible if stable and Hyde or cultural path active | avoids unless war threat severe | possible with Allied trust but no basing | possible through London talks | blocks if Blueshirt route active |
| Labour AI | possible as civic cultural support, not as nationalist fantasy | avoids unless civil order collapse | possible if independent from Soviet pressure | possible through worker and observer missions | blocks if Soviet dependency high |
| Blueshirt AI | blocked from civic restoration | may try permanent security only through its own route, not directorate | blocked or very low | blocked | corporate state capstone blocks cultural route |
| IRA AI | blocked from civic restoration | may trigger security reaction as opponent, not user | blocked | blocked if uprising route active | Army Council takeover blocks civic route |
| strict neutral AI | possible if high authority | temporary crisis only | strongest valid AI for compact | possible if low pressure | faction entry blocks compact |
| Britain AI | reacts positively to common platform if trust high | wary of directorate | may observe compact if no bases | supports only if unionist alarm low | blocks if German access or IRA violence |
| unionist actors | can accept civic guarantees only under low pressure | alarm rises against directorate | indifferent unless compact affects ports | core target actor | blocks violent route or weak guarantees |
| Germany | tries to spoil compact and exploit IRA if allowed | infiltrates under high access pressure | opposed | no support | invalid if Germany defeated or no access |
| United States | observer support if low dependency | wary of authoritarian directorate | possible observer | supports peaceful settlement | blocks if Ireland is Axis aligned |
| Soviet Union | may support Labour but not cultural route | wary of security state | low interest | supports Labour variant only if not dependent | blocks if anti communist route active |

AI should never choose hidden paths because a hidden focus is visible by accident. Each route needs explicit validity checks and route weights that consider authority, pressure values, war state, state control, sponsor pressure, and current ideology.

## Asset direction for hidden paths

| Asset family | Needed assets | Source mode | Animation |
| --- | --- | --- | --- |
| civic cultural restoration focus icons | constitution, schoolhouse, civil service, rural route, nonsectarian contact, cultural diplomacy, capstone | generated icons, with source review for harp or state symbols | capstone seal may animate with static fallback |
| civic cultural ideas | cultural networks, bilingual administration, Gaeltacht development, common platform contacts | generated idea icons, no resized focus icons | static |
| Douglas Hyde and real cultural figures | portrait if visible | sourced only | static unless sourced portrait overlay is later justified |
| cultural route symbols | harp, presidential seal style, constitutional book | source review if historically attested | optional animated seal after source review |
| emergency directorate icons | G2 files, LDF command, public order, directorate council, civilian restoration | generated icons unless real symbol used | warning seal optional |
| emergency directorate portrait | institutional council or emergency cabinet if leader changes | generated if fictional collective, sourced if real named figures | static preferred |
| Atlantic compact icons | compass, convoy observer, arbitration office, no basing principle, member rules | generated icons | compact seal optional with static fallback |
| common platform settlement icons | guarantees, observer plebiscite, service continuity, nonsectarian committee | generated icons | static |
| achievements | hidden path achievement icons | generated symbolic icons, source caution for historical motifs | static |

Do not use Gaelic text inside generated images. Do not use real flags or real movement emblems without source documentation.

## Text and audio research gates

Hidden routes need source research only for major reveal moments or final achievement text. Ordinary focus and decision text can be written by implementation from direction.

Research required before final wording for:

- constitutional language status references
- Douglas Hyde and Gaelic League references
- non political and non sectarian cultural work references
- any Gaelic wording, slogan, motto, or cultural phrase
- Atlantic conference or neutrality references
- Emergency directorate language if based on real offices or laws
- achievement title allusions
- any audio cue

No unresearched Gaelic line, slogan, prayer, poem, lyric, or quotation should appear in localisation.

## Achievement hooks

| Working id | Route | Unlock direction | Disqualifiers | Icon direction |
| --- | --- | --- | --- | --- |
| `ireland_focus_tree_restoration_without_a_crown` | civic cultural restoration | complete the hidden civic route while staying democratic, independent, and non coercive | Blueshirt route, IRA takeover, emergency security state, violent Northern war | constitution, harp, and open civic book |
| `ireland_focus_tree_common_platform` | common platform settlement | settle the Northern question through observer backed guarantees without war | border war, uprising route, high unionist alarm | bridge, schoolbook, and observer seal |
| `ireland_focus_tree_watchmen_of_the_west` | Emergency directorate recovery | enter the directorate under invasion danger, defend ports, then restore civilian rule | permanent security state, port loss, foreign basing | coast watch post and emergency seal |
| `ireland_focus_tree_conference_of_neutrals` | Atlantic compact | create compact or conference with enough valid observers while refusing permanent bases | faction entry, sponsor dependency, insufficient members | compass and small state circle |
| `ireland_focus_tree_no_crown_no_courier` | hidden route mastery | complete civic restoration and expose foreign courier danger in the same campaign | German dependency, Army Council rule, cultural corruption | civic book and intercepted radio map |

## Prompt update requirements

Implementation prompts, asset prompts, achievement prompts, decision and mission prompts, and goal prompts must treat hidden paths as mandatory planned content. Older files that say hidden cultural restoration is queued or rejected are superseded by this Part 10 addendum.

## Cleanup rule

The improvement loop planner must review this hidden path addendum. It may recommend trimming, but it must not revert hidden paths to unplanned status. If the planner rejects a hidden route, the final package must record the rejection and provide another hidden path of similar depth or a clear user approved reason.

## Route-specific hidden overlays

The five primary hidden paths above are the core hidden architecture. The following route-specific overlays are also mandatory. They prevent the main alternate routes from having only visible paths while the historical route receives all hidden depth.

| Overlay working label | Parent route | Reveal condition | Main play role | Hard blockers |
| --- | --- | --- | --- | --- |
| `hidden_constitutional_backchannel` | Fine Gael constitutional opposition | British trust, low armed pressure, controlled defence liaison, concession chance | legal backchannel that can lead into Northern civic settlement or guarded association | Blueshirt route, puppet status, high foreign dependency |
| `hidden_labour_independent_front` | Labour democratic socialist | Labour government, fascist or corporatist threat, worker defence regularised, Soviet pressure below client band | anti-fascist and cooperative security branch without Soviet capture | Soviet client route, militia capture, failed civil rights commitments |
| `hidden_corporate_chambers_without_oduffy` | Blueshirt corporatist | Blueshirt route active, Guard command crisis, O'Duffy failure or overreach, corporate institutions survive | authoritarian consolidation through institutions, not a one-man cult | Fine Gael constitutional route, no corporate institutions, foreign sponsor capture above hard band |
| `hidden_republican_reconciliation_backchannel` | IRA absorption or legal state under IRA pressure | underground pressure high but foreign dependency cut, amnesty or absorption decisions active | hard route out of civil conflict through controlled reintegration | Army Council state, active German liaison dependency, unresolved courier scandal |

### `hidden_constitutional_backchannel`

This overlay gives Fine Gael constitutional opposition a hidden route that is legalistic and diplomatic. It should reveal only when the player has kept armed pressure low, built British trust, and avoided becoming a dependent ally.

Focus groups:

| Working group | Purpose | Unlocks | Reward direction | Decisions or missions | AI behavior | Failure |
| --- | --- | --- | --- | --- | --- | --- |
| `boundary_files_reopened_group` | Reopen legal and diplomatic material on partition. | Backchannel missions and British response checks. | Raises concession chance and lowers radical pressure. | Document review, observer request, public restraint mission. | Democratic AI uses if Britain is friendly. | Nationalist patience falls if Britain refuses. |
| `limited_liaison_safeguards_group` | Define military cooperation without dependency. | Defence liaison decisions with caps. | Improves warning and supply, raises foreign access if abused. | Liaison cap, port access review, anti dependency audit. | AI uses only when danger is high. | Dependent ally outcome blocks clean compact. |
| `constitutional_concession_test_group` | Convert trust into a Northern settlement test. | Northern civic settlement reveal. | Opens guarantee or plebiscite missions. | British response, local guarantee, observer preparation. | AI uses when success chance is real. | Failure hardens British reaction. |

### `hidden_labour_independent_front`

This overlay keeps Labour from becoming only a Soviet route. It uses democratic worker defence, trade union logistics, cooperative supply, and anti-fascist service under law.

Focus groups:

| Working group | Purpose | Unlocks | Reward direction | Decisions or missions | AI behavior | Failure |
| --- | --- | --- | --- | --- | --- | --- |
| `worker_defence_under_law_group` | Keep defence committees disciplined and state controlled. | Worker guard missions and reserve conversion. | Readiness rises without militia capture. | Equipment, training, and authority missions. | Labour AI uses if stable. | militia politicisation raises authority crisis. |
| `anti_fascist_service_board_group` | Use anti-fascist volunteers and veterans without foreign capture. | Advisor or cadre decisions after source review. | Adds training and defence cadres through costs. | veteran integration and anti dependency checks. | AI uses under fascist threat. | foreign pressure or church backlash rises. |
| `cooperative_supply_front_group` | Build war supply through cooperatives. | Convoy, rail, and welfare supply missions. | Improves logistics and public support. | support equipment, convoys, trains, civilian burden. | AI uses if equipment exists. | economic strain and employer backlash. |

### `hidden_corporate_chambers_without_oduffy`

This overlay prevents the Blueshirt route from depending only on one leader. It should reveal when the movement survives O'Duffy failure, overreach, scandal, or replacement, and when corporate chambers become the real governing mechanism.

Focus groups:

| Working group | Purpose | Unlocks | Reward direction | Decisions or missions | AI behavior | Failure |
| --- | --- | --- | --- | --- | --- | --- |
| `guard_leader_crisis_group` | Resolve or exploit O'Duffy overreach. | replacement, chamber rule, or Guard hardening. | Changes leader or creates collective body. | Guard discipline, loyalty review, public order mission. | AI rare. | coup scare or movement fracture. |
| `corporate_chamber_state_group` | Make corporate rule institutional. | production boards and union suppression risks. | Industry control improves with legitimacy cost. | factory coordination, labour containment, sponsor review. | AI uses only on route. | labour backlash and foreign pressure. |
| `right_contact_containment_group` | Keep foreign right aid from becoming ownership. | exposure and dependency decisions. | Aid can be accepted only with visible risk. | sponsor audit, public scandal, arms channel. | AI avoids full capture. | dependency or diplomatic isolation. |

### `hidden_republican_reconciliation_backchannel`

This overlay gives Ireland a hard but playable exit from underground pressure without making the IRA path a clean conquest route. It can appear for a legal government that has high underground pressure, or for an IRA absorption route that has cut foreign dependency.

Focus groups:

| Working group | Purpose | Unlocks | Reward direction | Decisions or missions | AI behavior | Failure |
| --- | --- | --- | --- | --- | --- | --- |
| `amnesty_channel_group` | Offer a controlled path out of underground politics. | amnesty and arms surrender missions. | Reduces underground pressure and raises authority if trusted. | safehouse audit, arms surrender, prisoner review. | Historical AI can use moderate version. | martyr pressure if heavy handed. |
| `civil_authority_restoration_group` | Restore civilian control after absorption. | leader or idea lifecycle repair. | Reopens civic routes if foreign links were cut. | council discipline, public order review, local support check. | AI prefers this over Army Council rule. | Army Council state if failed. |
| `border_cells_stand_down_group` | Prevent Northern cells from sabotaging settlement. | stand down or integration missions. | Lowers partition pressure and British reaction. | border cell stand down, local guarantee, observer support. | AI uses if settlement possible. | sabotage crisis and frozen border. |

## Route-specific overlay assets and research

- Constitutional backchannel needs legal and boundary icon families, plus treaty and defence liaison research.
- Labour independent front needs worker defence, cooperative supply, and anti-fascist service icons. Real figures require sourced portraits.
- Corporate chambers without O'Duffy needs Guard crisis, chamber body, and right contact exposure icons. O'Duffy and real symbols require sourced work.
- Republican reconciliation backchannel needs amnesty, arms surrender, civil authority, and border cell stand down icons. Real IRA symbols and actors require source review.

These overlays should also receive achievement checks and AI blockers. They are hidden subpaths with required gameplay content.

## Route specific hidden overlays added for full coverage

The hidden path rule applies across major route families. The core hidden paths above cover cultural, emergency, neutral, and Northern settlement content. The following overlays extend hidden planning into IRA, Labour, constitutional, and radical right routes so hidden content is not concentrated in one branch.

These overlays are not independent country formables. They are revealable branch overlays that add focus groups, missions, decisions, AI rules, assets, achievements, and cleanup to an existing route when the public route has created the right conditions.

### `hidden_compromised_republican_network`

Purpose:

This overlay belongs to the IRA hard route when foreign contact, courier exposure, or Plan Kathleen style logic has gone too far. It exists to keep the IRA path risky. It should never make German contact a clean source of power.

Reveal conditions:

- IRA hard route or underground pressure is active.
- Foreign Access Pressure is high through German or other hostile sponsor channels.
- G2 has failed or delayed courier interception.
- Britain is at war and treats Ireland as a security concern.
- The player has accepted risky courier, sabotage, or foreign liaison actions.

Focus and decision groups:

| Working group | Purpose | Unlocks | Reward direction | Failure state |
| --- | --- | --- | --- | --- |
| `compromised_courier_chain` | reveal foreign handler risk | courier exposure missions | short term sabotage reach, high exposure | British pressure and G2 crackdown |
| `dependency_purge_cells` | let IRA route try to escape sponsor control | purge missions and safehouse audits | lower foreign pressure and regain authority | purge failure creates faction split |
| `republic_without_handlers` | hard route recovery capstone | route lock away from foreign dependency | revolutionary route survives without puppet pressure | failure leaves compromised republic idea |
| `british_countermove` | make outside reaction active | border and port security crisis | forces preparation and tradeoff | British intervention or demands |

Decision and mission requirements should use exposure values, safehouse networks, equipment loss, local support, and G2 pressure. The route may create irregular units only through unsafe network decisions with reliability problems. It must not hand out clean elite divisions.

AI behavior:

IRA AI can reveal this overlay only under rare high risk conditions. German AI can push it only when at war with Britain and when Irish G2 is weak. Britain and G2 should react aggressively once exposure rises. Historical Ireland AI should treat it as a threat, not a route.

Asset direction:

Use generated courier, radio, safehouse, and broken chain icons. Real IRA symbols, real leaders, and any German contact imagery require source review. No slogans or final button text are approved.

### `hidden_cross_border_labour_council`

Purpose:

This overlay strengthens the Labour route without turning it into a Soviet branch. It creates a democratic socialist all island channel through unions, port workers, cooperative industry, anti fascist defence, and local rights.

Reveal conditions:

- Labour democratic route active.
- Soviet dependency below danger threshold.
- Partition Pressure managed through local support rather than violence.
- Worker defence or cooperative industry branch complete.
- Unionist alarm is low enough for cross border labour contact.

Focus and decision groups:

| Working group | Purpose | Unlocks | Reward direction | Failure state |
| --- | --- | --- | --- | --- |
| `border_workers_committee` | build a cross border social route | worker contact and port solidarity missions | local support, supply, Labour legitimacy | unionist alarm or employer backlash |
| `popular_defence_front` | defend democracy without Soviet client logic | worker defence integration and militia regularization | reserve units, anti fascist preparedness, no free army loops | permanent militia government risk |
| `labour_settlement_congress` | connect Labour to Northern settlement | observer and rights missions | federal or common platform settlement support | Soviet dependency blocks trust |
| `return_to_elections` | keep route democratic | election and cabinet mission after crisis | removes militia pressure, achievement hook | hard left split or public fatigue |

Costs should include support equipment, infantry equipment, civilian factory burden, legitimacy, local support, and timed election deadlines. Political power is not enough by itself.

AI behavior:

Labour democratic AI can use this overlay when fascist threat is high, dependency is low, and local support exists. Labour radical AI should not get the clean democratic payoff if Soviet dependency is high. Britain can tolerate it if it is democratic and non violent. The Soviet Union may try to influence it, but the route should reward resisting dependency.

Asset direction:

Generated icons can use worker, port, reserve badge, ballot, and cooperative industry motifs. Real Labour figures and trade union symbols need source review. No unresearched slogans.

### `hidden_constitutional_backchannel`

Purpose:

This overlay lets constitutional opposition, historical neutrality, or guarded Commonwealth cooperation use discreet legal diplomacy without becoming a British client. It is a hidden path for players who keep sovereignty high while using London or Washington channels carefully.

Reveal conditions:

- Constitutional Authority high.
- Foreign Access Pressure balanced and below dependency.
- Treaty review, London channel, or arbitration branch complete.
- No permanent foreign bases.
- No extremist route active.

Focus and decision groups:

| Working group | Purpose | Unlocks | Reward direction | Failure state |
| --- | --- | --- | --- | --- |
| `quiet_london_channel` | create legal diplomacy without full alignment | backchannel and guarantee decisions | relations, observer support, lower settlement cost | dependency pressure if overused |
| `washington_listener_network` | use American attention without basing | recognition and aid screening missions | aid without base concessions | sponsor backlash |
| `neutrality_law_review` | keep cooperation constitutional | legal review and Dáil oversight | authority and low dependency | opposition scandal |
| `backchannel_settlement_note` | support Northern federal or common platform settlement | observer backed settlement aid | British willingness and local trust | unionist alarm if seen as secret deal |

AI behavior:

Constitutional AI can use this overlay under low war danger and high authority. Britain and the United States should support it only if Ireland resists Axis access and does not demand unrealistic concessions. Germany should treat it as a threat to courier operations.

Asset direction:

Use generated legal, diplomatic pouch, observer, and chamber icons. Any real document image or portrait needs source review.

### `hidden_corporate_chambers_without_oduffy`

Purpose:

This overlay prevents the Blueshirt route from depending only on one leader. If O'Duffy is unavailable, discredited, or removed, a corporate council path can appear. It is still authoritarian and remains separate from Fine Gael constitutional opposition.

Reveal conditions:

- Blueshirt corporatist route active.
- O'Duffy path blocked, removed, or compromised.
- Corporate chamber focuses developed.
- Constitutional Authority damaged.
- Labour and IRA pressure present or rising.

Focus and decision groups:

| Working group | Purpose | Unlocks | Reward direction | Failure state |
| --- | --- | --- | --- | --- |
| `corporate_chamber_collective` | replace personal leader route with council rule | chamber body leader or advisor group | industry discipline and command obedience | legitimacy collapse |
| `union_discipline_statutes` | suppress labour opposition | public order and factory control missions | short term production control | strikes and underground growth |
| `provincial_order_boards` | regionalize the corporatist state | provincial administration decisions | local control with resistance | state level backlash |
| `right_wing_foreign_arbitrage` | seek Italy or Spain support without dependency safety | sponsor pressure decisions | limited aid and diplomatic posture | foreign access spike |

AI behavior:

Blueshirt AI can use this only if its normal leader path is invalid. It should avoid war with Britain unless Ireland is prepared and Britain is weak. It blocks civic cultural restoration and compact diplomacy.

Asset direction:

Generated symbolic council portrait is allowed if the leader is a fictional collective body. Real O'Duffy portrait and real Blueshirt symbols require sourced assets.

### `hidden_republican_reconciliation_backchannel`

Purpose:

This overlay gives non IRA routes a way to absorb lower level republican networks without enabling Army Council takeover. It supports the historical and constitutional routes by turning underground pressure into legal reserve, policing, or amnesty work.

Reveal conditions:

- IRA pressure exists but has not become a takeover.
- Constitutional Authority is high enough for amnesty.
- G2 or public order route has mapped safehouse networks.
- Foreign courier pressure is low or has been exposed.

Focus and decision groups:

| Working group | Purpose | Unlocks | Reward direction | Failure state |
| --- | --- | --- | --- | --- |
| `arms_surrender_channel` | disarm part of the underground | surrender and amnesty missions | lowers armed pressure and raises authority | hardliners split |
| `frontier_service_offer` | convert legal volunteers into border service | reserve integration decision | route specific small units with limits | infiltration risk |
| `amnesty_under_watch` | keep reconciliation from becoming naivety | monitored reintegration | manpower and legitimacy | G2 scandal if abused |
| `hardliner_crackdown` | contain cells that reject settlement | targeted mission | lowers sabotage risk | public backlash |

AI behavior:

Historical and constitutional AI can use this when authority is high and foreign pressure is low. IRA hard AI resists it. Britain reacts favorably if it lowers sabotage, but may demand stronger measures after failures.

Asset direction:

Generated amnesty, arms surrender, frontier service, and monitored reserve icons. Real IRA imagery requires source review.

### `hidden_neutral_aftershock_recovery`

Purpose:

This overlay appears after a neutrality failure, port crisis, compact collapse, or foreign access scandal. It lets the player repair a damaged neutral state instead of losing the entire neutrality route to one disaster.

Reveal conditions:

- Strict neutrality or historical neutrality route active.
- A port, shipping, foreign access, or compact mission fails.
- Ireland remains independent and not a client.
- Emergency Preparedness can still be rebuilt.

Focus and decision groups:

| Working group | Purpose | Unlocks | Reward direction | Failure state |
| --- | --- | --- | --- | --- |
| `repair_the_beacons` | restore coast watch and public confidence | coast watch repair missions | preparedness recovery | repeated failure closes compact |
| `port_scandal_inquiry` | handle foreign access failure | inquiry and cleanup decisions | lowers dependency and restores authority | scandal damages government |
| `neutrality_reaffirmed` | rebuild strict neutral identity | no base doctrine and observer reset | compact can reopen later | impossible if bases accepted |
| `emergency_lessons_board` | turn failure into better defence | updated LDF and port missions | stronger future readiness | cost burden |

AI behavior:

Historical and strict neutral AI should use this after a failure if Ireland is still independent. It should not use it to erase deliberate foreign basing or Axis collaboration.

Asset direction:

Generated repaired beacon, inquiry, port ledger, and neutral seal icons. Optional animated beacon recovery can be planned only if the implementation has an Emergency board or compact UI.

### `hidden_northern_emergency_protectorate`

Purpose:

This overlay handles severe wartime Northern crisis without turning it into annexation. It represents temporary administration, corridors, observers, policing, and exit settlement when Britain cannot secure a Northern state group or asks for Irish support under pressure.

Reveal conditions:

- Britain is unable or unwilling to secure a Northern crisis area.
- Ireland has high Emergency Preparedness and low foreign dependency.
- No German dependency or IRA takeover.
- Britain is friendly, exhausted, or under direct threat.
- Ireland can hold named border and corridor objectives.

Focus and decision groups:

| Working group | Purpose | Unlocks | Reward direction | Failure state |
| --- | --- | --- | --- | --- |
| `border_emergency_conference` | start temporary administration under pressure | conference mission with Britain and local actors | temporary access and observer authority | British refusal or unionist alarm |
| `humanitarian_corridors` | make route practical and non annexationist | supply and refugee missions | local support and legitimacy | supply crisis |
| `temporary_policing_authority` | secure areas without full integration | shared policing and garrison missions | resistance reduction | abuse raises alarm |
| `protectorate_exit_settlement` | decide return, federalize, or integrate later | exit decision verified by control and support | converts to common platform or partial settlement | frozen administration |

AI behavior:

Ireland AI can use this only under severe valid conditions. Britain AI can request or accept it only if it is losing control or needs border stability. Unionist actors resist unless guarantees and policing missions succeed. Germany tries to exploit it if Ireland has weak G2.

Asset direction:

Generated corridor, observer, temporary administration, and emergency border icons. No new country flag unless implementation creates a temporary cosmetic identity with clear source rules.

## Consolidated hidden path acceptance list

The accepted hidden path set for implementation planning now includes:

- civic cultural restoration
- Emergency directorate
- Atlantic neutral compact
- common platform Northern settlement
- corrupted restoration failure branch
- compromised republican network
- cross border Labour Council and popular defence front
- constitutional backchannel
- corporate chambers without O'Duffy
- republican reconciliation backchannel
- neutral aftershock recovery
- Northern emergency protectorate

The improvement loop planner may recommend trimming or merging specific overlays, but it must not treat hidden path planning as optional. Any rejected hidden overlay needs a clear reason and an accepted replacement or explicit user approved cut.
