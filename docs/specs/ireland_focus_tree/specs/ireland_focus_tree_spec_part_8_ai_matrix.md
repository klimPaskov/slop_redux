# Ireland focus tree spec part 8, AI matrix

Working labels are internal handles only. They are not final localisation.

This part continues from part 7 and defines route aware AI behavior. It does not rewrite focus branch design. The implementation agent should convert these rules into national focus AI weights, strategy plans, decision `ai_will_do`, scripted triggers, scripted values, and cleanup helpers.

## AI design promise

Ireland should not use one generic neutrality plan with alternate ideology weights tacked on. AI Ireland must understand that sovereignty, ports, partition, domestic authority, and foreign access are linked. Foreign actors must also react to Ireland as a strategic Atlantic state, a contested neutral, a possible back door into Britain, and a partition claimant.

Every AI profile should evaluate four visible values from part 7.

| Value | AI reading | High value behavior | Low value behavior |
| --- | --- | --- | --- |
| `constitutional_authority_value` | Can the cabinet enforce law and keep route commitments | pursue negotiated routes, reforms, public order, observer missions | delay risky settlements, avoid coups, spend on authority missions |
| `emergency_preparedness_value` | Can Ireland survive air, sea, invasion, and supply pressure | hold strict neutrality, bargain from strength, garrison ports | prioritize coastal watch, reserves, stores, air defence |
| `partition_pressure_value` | How close Northern Ireland is to crisis or settlement | use settlement, border, or uprising actions by route | keep Northern actions quiet and reduce exposure |
| `foreign_access_pressure_value` | How much outside powers can demand or use Irish territory | refuse new sponsors, reduce leverage, close obsolete aid | seek limited aid only if survival risk is higher |

AI choices must be invalidated when the route, state, or sponsor is no longer valid. A route that requires Britain, Germany, the Soviet Union, the Vatican, or a Northern target cannot remain weighted if that actor is dead, capitulated without successor handling, unreachable, hostile beyond the route design, or already resolved by settlement.

## Ireland AI route profiles

### `ire_ai_historical_sovereign_neutrality`

Use as the default historical plan. The AI should keep de Valera aligned with constitutional sovereignty, recover the ports, pass the constitution, build Emergency defence, and avoid formal alliance entry unless Ireland is attacked or Britain collapses into a direct island security crisis.

Focus priority order:

1. Opening constitutional trunk through constitution, public order, civil war wound handling, and state legitimacy.
2. Treaty port recovery and coastwatching before deep industry if Europe is tense.
3. Emergency defence, LDF, air raid protection, port garrisons, and G2 counter intelligence.
4. Native industry, sugar beet, turf, Shannon grid, and supply projects.
5. Diplomacy that preserves neutrality, especially Washington and diaspora recognition if foreign access pressure is low.
6. Northern settlement only through border survey, observer channels, and delayed arbitration when authority and preparedness are high.

Decision and mission priorities:

- Take `staff_lop_chain` and `port_garrison_chain` when Britain or Germany is at war.
- Use `neutral_port_access_rules_family` to reduce access pressure after any temporary access concession.
- Use `public_order_enforcement_family` if IRA pressure rises, but prefer reconciliation if stability is poor.
- Use `observer_plebiscite_missions` only after legitimacy and British willingness are high.
- Use `anti_dependency_family` before accepting repeated foreign aid.

Invalid blockers:

- Do not start coercive Northern missions unless Ireland is already at war with Britain or a defensive protectorate condition is active.
- Do not accept German access, Axis volunteers, or IRA liaison actions.
- Do not join a faction while strict neutrality route flags are active.
- Do not form an Atlantic compact while the Emergency branch is incomplete and Britain remains a direct invasion threat.

Failure state response:

- If foreign access pressure is high, pause settlement and take access reduction missions.
- If emergency preparedness is low during war, delay political capstones and run emergency missions.
- If constitutional authority falls into the crisis band, stop Northern escalation and prioritize public order, reconciliation, and cabinet authority focuses.

Cleanup behavior:

- Clear temporary port access flags once a sponsor exits war or the access mission ends.
- Remove obsolete wartime missions after general peace unless postwar integration is still active.
- Close strict neutral decisions after Ireland joins any faction through invasion or player forced branch.

### `ire_ai_strict_neutral_watchtower`

Use for a more defensive alternate neutral AI. This profile should appear when the AI has high perceived threat, low industry, and no reason to pursue party change. It plays Ireland as a prepared neutral that refuses all permanent access.

Focus priority order:

1. Constitution and authority trunk.
2. Port return, coastwatching, G2, air defence, reserves, and stockpiles.
3. Turf, rail, supply hub, and domestic fuel projects.
4. Neutral diplomacy and limited recognition.
5. Northern settlement only after the world war is over or Britain is unable to resist and observer work is available.

Decision priorities:

- Highest priority to LOP, reserve, stores, and port garrison mission families.
- Medium priority to native factory decisions when no emergency missions are active.
- Low priority to diaspora recognition unless foreign access pressure is already controlled.
- No priority for aid corridor decisions unless Ireland is being invaded.

Invalid blockers:

- Refuse foreign access if `foreign_access_pressure_value` is already above the safe band.
- Refuse any sponsor action that creates a permanent access right.
- Do not pursue labour radicalisation, Blueshirt mobilisation, or IRA underground decisions.

War reactions:

- If Britain is at war with Germany, watch both sides and avoid access.
- If Britain is invaded or loses naval control near Ireland, raise coastal defence and prepare emergency protectorate decisions without taking full reunification war actions.
- If Germany owns western French ports, increase G2 and port defence priorities.

### `ire_ai_guarded_commonwealth_cooperation`

Use for the constitutional opposition route. This AI is not a Blueshirt route. It should restore a conservative constitutional government, bargain with Britain, and make Commonwealth linked cooperation conditional on autonomy, Northern safeguards, and avoidance of puppet dependency.

Focus priority order:

1. Constitutional opposition opener and legal government challenge.
2. Parliamentary restoration, opposition cabinet, and advisory board focuses.
3. Commonwealth liaison, British staff talks, and port rules.
4. Industry and army modernization that use British help but build Irish capacity.
5. Northern safeguards, arbitration, and all island settlement preparation.
6. Late game Atlantic compact only if Ireland remains sovereign and Britain has accepted limits.

Decision priorities:

- Use recognition and aid corridor decisions with Britain when foreign access pressure is low or moderate.
- Use anti dependency decisions after each major British aid stage.
- Use observer and minority safeguard missions before accepting Northern transfer or plebiscite results.
- Use constitutional campaign and reconciliation missions to keep authority high.

Invalid blockers:

- Do not choose Blueshirt paramilitary focuses after this route has taken legal opposition locks.
- Do not accept British conditions that would turn Ireland into a puppet unless the campaign explicitly enters a defeat or occupation outcome.
- Do not pursue coercive Northern settlement unless Britain is hostile or has collapsed and the route has shifted into emergency protectorate.

Failure state response:

- If foreign access pressure exceeds the risk band, delay further cooperation and take anti dependency missions.
- If unionist alarm is high, pause settlement and run minority safeguards.
- If Britain refuses cooperation, switch to armed neutrality support focuses and do not keep clicking failed British negotiations.

### `ire_ai_labour_democratic_social_reform`

Use for Labour routes where the AI keeps elections, parliamentary life, and trade union legitimacy. This route should not become a Soviet client by default.

Focus priority order:

1. Constitutional trunk and Labour legal route opener.
2. Labour cabinet, union law, rural relief, housing, social services, and worker representation.
3. Sugar beet, Shannon grid, native factories, and public works.
4. Citizen army or defence committee content only after cabinet authority is safe.
5. Northern labour links and cross border labour missions.
6. International labour diplomacy with Britain, United States, and small democracies before Soviet contact.

Decision priorities:

- Use rural relief, sugar beet, housing, and labour mediation decisions early.
- Use reconciliation missions over crackdowns unless authority is near collapse.
- Use Northern nationalist committee missions only when violence is controlled.
- Use aid corridors from democratic sponsors before Soviet options.

Invalid blockers:

- Do not take Soviet alignment if the democratic Labour subroute is locked.
- Do not use IRA uprising missions unless Labour has collapsed into a revolutionary crisis, which should be rare.
- Do not suppress unions through Blueshirt or emergency authoritarian tools after Labour route lock.

Failure state response:

- If strikes rise because industry costs are too high, reduce project frequency and take mediation decisions.
- If church backlash or rural resistance rises, slow radical social reform and use legitimacy missions.
- If Soviet sponsor pressure rises, use anti dependency actions before any further left sponsor work.

### `ire_ai_labour_social_republic`

Use as a rarer Labour path. It should represent a radical socialist republic that still grows from Irish labour politics. It can engage the Soviet Union, but it should resist simple client status unless authority is very low or the route chooses dependence.

Focus priority order:

1. Labour constitutional base or crisis election.
2. Factory councils, land and welfare reforms, and worker defence.
3. Public industry and supply reform.
4. Northern worker committees and anti sectarian missions.
5. Soviet recognition only after domestic institutions exist.
6. Anti dependency or balanced left diplomacy before capstone.

Decision priorities:

- Build industry through worker boards and public works rather than repeated free factories.
- Use `anti_dependency_family` after Soviet aid or arms.
- Use LDF conversion only when emergency preparedness is low or invasion risk is high.
- Use Northern labour settlement over armed uprising.

Invalid blockers:

- Do not join Comintern if foreign access pressure is high, Britain is likely to invade, and Ireland cannot defend ports.
- Do not accept Soviet basing in Irish ports unless the route has already abandoned strict sovereignty.
- Do not use coercive religious or Blueshirt suppression decisions.

Failure state response:

- If authority is low, pause foreign radical steps and build cabinet or council legitimacy.
- If British hostility rises, increase coastal defence and anti dependency before Northern action.
- If industry project strain hits crisis, move to relief decisions and postpone capstones.

### `ire_ai_blueshirt_corporatist_state`

Use rarely, with strong conditions. This path should split from Fine Gael legalism and represent a corporatist authoritarian route with Catholic, anti communist, paramilitary, and Spanish Civil War links. It must not be a generic fascist ladder.

Focus priority order:

1. Blueshirt revival and National Guard reorganization.
2. Legal opposition crisis or extra parliamentary route lock.
3. Corporate chamber, church or clerical support where justified, and anti communist mobilization.
4. National Guard integration and command obedience branch.
5. Spanish volunteer or Iberian contact content if Spain exists and civil war conditions allow it.
6. Coercive Northern settlement only after the regime has enough military readiness and has accepted international backlash.

Decision priorities:

- Use public order and paramilitary integration decisions to consolidate authority.
- Use reserve and officer decisions that convert Blueshirt cadres into state units, with legitimacy costs.
- Use Italian or Spanish contact only when Italy or Nationalist Spain exists and is not a direct puppet trap.
- Use coercive border incidents only when Britain is weak, hostile, or already at war with a major enemy.

Invalid blockers:

- Do not remain on the Fine Gael constitutional route after taking Blueshirt route locks.
- Do not choose Soviet or Labour social republic content.
- Do not take German IRA contact or Plan Kathleen content.
- Do not start Northern war if Ireland lacks supplied divisions near border states.

Failure state response:

- If constitutional authority collapses, expect coup, counter coup, or civil disorder events rather than clean focus progress.
- If British warning pressure rises above the danger band, pause Northern incidents and build defence.
- If Spain route is invalid, skip Spanish contact and use domestic corporatist consolidation.

### `ire_ai_ira_underground_republic`

Use very rarely for AI and only with permissive settings, high partition pressure, low authority, or major external crisis. This path should be unstable. German contact can provide opportunity, but it must increase exposure and dependency risk.

Focus priority order:

1. Underground republican route opener after state authority weakness.
2. Safehouse network, arms dumps, intelligence penetration, and cell discipline.
3. Northern operation preparation with state targets.
4. German contact only if Germany exists, is at war with Britain, and the route accepts exposure.
5. Uprising or border campaign only after safehouse and local support conditions are met.
6. Post victory civil authority conversion to avoid permanent underground governance.

Decision priorities:

- Use safehouse, arms dump, and local support missions before any uprising.
- Use G2 evasion or exposure reduction if counter intelligence pressure rises.
- Use German aid decisions only when the route has already accepted severe risk and has a clear Northern objective.
- Use post settlement integration quickly after any territorial success.

Invalid blockers:

- Do not take German contact if Germany is dead, no longer at war with Britain, has no access path, or Ireland has a strict neutral route lock.
- Do not start an uprising without minimum local support, supplied units or cells, and route flags.
- Do not form a stable all island identity instantly after irregular victory. Require integration decisions.

Failure state response:

- If exposure reaches crisis, trigger crackdown, informant purge risk, G2 success, or sponsor betrayal events.
- If German aid fails or becomes impossible, move to domestic arms and delay the campaign.
- If Britain reacts with overwhelming force, shift to survival missions and remove offensive weights.

### `ire_ai_late_game_atlantic_ambition`

Use after Ireland has solved its starting sovereignty and defence problems. This profile can appear from historical, constitutional, Labour democratic, or strict neutral routes. It should not be available to unstable IRA or high dependency Blueshirt routes without a recovery bridge.

Focus priority order:

1. Complete core route institutions.
2. Finish Emergency defence and industry enough to support a foreign policy.
3. Settle or freeze the Northern question through a chosen route.
4. Build Atlantic, small nation, diaspora, or postwar arbitration branch.
5. Form compact, arbitration office, or regional security identity only after minimum membership and recognition conditions.

Decision priorities:

- Use recognition missions, compact invitations, joint defence talks, and postwar reconstruction decisions.
- Use anti dependency before forming any faction if sponsor pressure is high.
- Use Northern integration and safeguards before claiming all island leadership.

Invalid blockers:

- Do not form a faction if Ireland is a puppet, occupied, in civil war, or has unresolved emergency occupation states.
- Do not use faction invitations on dead, hostile, or ideologically incompatible targets.
- Do not invite Britain if the compact is defined as a small nation neutral bloc unless a special British observer rule exists.

## Foreign actor AI matrix

### Britain and the United Kingdom

Britain is the most important foreign actor. Its AI should evaluate Ireland through access, Atlantic security, Northern stability, and current war danger.

Historical or cooperative response:

- Accept port transfer and treaty settlement if historical focuses are active and relations are not hostile.
- Offer limited intelligence and air or naval liaison when Germany threatens western approaches.
- Prefer diplomatic pressure over invasion when Ireland keeps neutrality and controls foreign access.
- Support constitutional opposition cooperation if Ireland grants limited staff talks and keeps autonomy rules.

Northern settlement response:

- Peaceful settlement is possible only when Ireland has high legitimacy, low violence, observer missions, and minority safeguards.
- Commonwealth linked settlement gets a higher British willingness score if Irish foreign access pressure is low and Ireland accepts defensive cooperation.
- Labour settlement gets cautious British review. Britain should prefer democratic Labour over Soviet linked Labour.
- Blueshirt coercion should trigger warnings, guarantees, troop readiness, and possible intervention.
- IRA uprising should trigger crackdown support, intelligence sharing, and high chance of British military response.

Access behavior:

- Ask for port or air cooperation only when Britain is at war with a naval or air threat and Ireland has moderate or low foreign access pressure.
- Stop demanding access if Ireland has passed strict neutrality laws and emergency preparedness is high.
- Increase pressure if Germany gets Irish access, IRA German liaison is exposed, or Ireland fails to police ports.

Invalid blockers:

- Britain should not offer Commonwealth cooperation if it is at war with Ireland, has lost the Home Islands without a government in exile rule, or Ireland is Axis aligned.
- Britain should not support all island transfer if Northern unionist crisis is high and no safeguards exist.
- Britain should not invade Ireland only because Ireland is neutral. Require German access, direct threat, or hostile route escalation.

Cleanup:

- Remove temporary access demands after peace.
- Clear Northern crisis warnings after settlement succeeds.
- Close British pressure decisions after Ireland joins Britain through valid route or after Ireland becomes hostile through war.

### Northern Ireland and unionist actors

Northern Ireland may be represented as state modifiers, decisions, hidden actors, or a release tag if implementation needs one. The AI logic should exist either way.

Default behavior:

- Resist Southern claims unless they are treaty based and include safeguards.
- Increase unionist alarm when Ireland runs border incidents, IRA safehouses, coercive propaganda, or armed concentration near the border.
- Lower alarm through observer missions, minority rights, cross border trade, labour links, and British endorsed arbitration.

Local group behavior:

- Unionist cabinet actors prioritize security, British guarantees, and avoidance of sudden transfer.
- Northern nationalist committees prioritize civil rights, local support, and low violence settlement.
- Northern labour groups support Labour routes when sectarian alarm is low and social reform is credible.
- Border communities respond to economic relief, rail links, and local security conditions.

Invalid blockers:

- Unionist actors should not accept settlement if Britain is hostile to it and Ireland lacks control or overwhelming leverage.
- Northern nationalist committees should not support IRA actions if exposure and violence have passed the failure band.
- Local labour support should not grow under Blueshirt coercive rule unless repression or fear logic is intentionally scripted.

Cleanup:

- Convert Northern local support into integration variables after settlement.
- Clear uprising cells after failed uprising, state transfer, or British occupation.
- Remove alarm missions after a final all island settlement or after Ireland abandons the Northern branch.

### Germany

Germany should see Ireland as an intelligence opportunity, a British flank, and a propaganda asset. It should not treat Ireland as a reliable ally by default.

Sponsor behavior:

- Offer covert contact only to IRA route or rare extreme anti British conditions.
- Prefer intelligence and disruption over large direct aid unless Britain is at war and sea access is plausible.
- Increase pressure for port access if Ireland accepts repeated aid.
- Abandon or expose contacts when German strategic situation is poor or Ireland has strong G2 pressure.

Plan Kathleen style behavior:

- The plan is treated as risky and amateur or unstable. Rewards should come with exposure, informants, British reaction, and foreign access pressure.
- Germany should not give clean invasion support without strong conditions, valid state targets, and high British war pressure.
- If Germany is losing, German aid should become less reliable and more dangerous.

Invalid blockers:

- No German contact if Germany has capitulated, is not at war with Britain, lacks naval or air access, or Ireland has strict neutral locks.
- No broad German alliance to historical or Labour democratic Ireland.
- No Northern invasion support if no Northern state target exists or Britain is already a friendly sponsor of Ireland.

Cleanup:

- Remove German liaison missions when Germany capitulates or peace with Britain occurs.
- Convert exposed contact into crackdown, diplomatic scandal, or route failure flags.

### Italy

Italy matters mainly for Blueshirt and Catholic corporatist routes. It should not dominate the Irish tree.

Behavior:

- Offer ideological prestige, corporatist advisors, or limited paramilitary inspiration to Blueshirt route.
- Support Spanish volunteer links if Italy and Nationalist Spain are aligned and the Spanish Civil War exists.
- Avoid heavy Irish military aid unless Ireland is already committed to Axis war or Britain is too weak to retaliate.

Invalid blockers:

- No Italian corporatist route support for Fine Gael legalism, Labour, historical neutrality, or IRA German path.
- No Italian mission if Italy has capitulated or has no route to influence Ireland.

Cleanup:

- Remove Italian liaison after Italy exits war or Spain route closes.

### Spain

Spain is route relevant only when the Spanish Civil War or post civil war Nationalist Spain exists. It should support Blueshirt identity, volunteer memory, and anti communist politics without becoming a generic sponsor.

Behavior:

- Nationalist Spain can receive Irish volunteer decisions from Blueshirt route.
- Republican Spain can be a Labour international solidarity question, but Labour democratic Ireland should prefer humanitarian or labour support over militarized commitment unless radicalized.
- Spain should not push Northern policy directly.

Invalid blockers:

- No Spanish volunteer branch if Spain has unified under an incompatible side before the route unlock.
- No support if Ireland lacks the route flag or cannot send volunteers due to neutrality law.

Cleanup:

- Close Spanish decisions after the Spanish Civil War ends.
- Convert volunteer memory into route specific officer or political modifiers only once.

### United States

The United States should matter through diaspora support, recognition, trade, neutrality, later Lend Lease style access, and postwar diplomacy. It should not become a simple factory button.

Behavior:

- Early game priority is low unless Ireland pursues diaspora diplomacy or Britain is under severe pressure.
- Support historical, constitutional, and Labour democratic routes with recognition and trade if Ireland avoids Axis access.
- Pressure Ireland against German contact and IRA escalation.
- Support postwar settlement or Atlantic compact if Ireland has stable institutions and low sponsor dependency.

Invalid blockers:

- No support to Blueshirt or IRA German routes unless the route has renounced extreme foreign contact and passed cleanup conditions.
- No major aid if Ireland grants hostile power port access.

Cleanup:

- Close wartime aid corridors after general peace.
- Convert diaspora aid into postwar recognition or investment only if dependency is controlled.

### Soviet Union

The Soviet Union is relevant to Labour radical routes and anti fascist diplomacy. It should not own the entire Labour tree.

Behavior:

- Offer recognition and limited industrial or military aid to Labour social republic route.
- Encourage anti fascist and anti Blueshirt actions.
- Treat democratic Labour as sympathetic but not automatically aligned.
- Increase sponsor pressure when aid is repeated or Ireland needs defence against Britain.

Invalid blockers:

- No Soviet aid to constitutional opposition, historical strict neutral, Blueshirt, or IRA German route.
- No Soviet port access unless the route has deliberately accepted high dependency.
- No Comintern entry if Ireland cannot defend itself and Britain is likely to invade unless the route is intentionally high risk.

Cleanup:

- Clear Soviet aid missions if the Labour route is lost, the Soviet Union capitulates, or Ireland joins a hostile faction.

### Vatican and Catholic actors

The Vatican should remain route relevant only when Catholic legitimacy, corporatist appeals, anti communist politics, or social reform backlash matters. It should not be a sponsor with military aid.

Behavior:

- Provide legitimacy pressure, moral caution, or mediation cues through events and decisions if the route uses Catholic institutions.
- Increase concern over radical anti clerical Labour choices.
- Give Blueshirt route a soft legitimacy opportunity only if violence is restrained, with high risk if paramilitary repression rises.
- Support peaceful settlement and minority safeguards in Northern integration when designed as moral mediation.

Invalid blockers:

- No military aid, port access, or direct state formation role.
- No support for IRA German contact or violent coercive settlement.
- No route lock that makes the Church the whole government unless a separate, fully planned route is accepted later.

Cleanup:

- Remove mediation decisions once settlement finishes or violence invalidates the mediation route.

## Internal actor AI rules

### Emergency cabinet

The Emergency cabinet is a hidden or scripted actor for historical, strict neutral, and constitutional routes.

- Prioritize authority and preparedness over ideology drift.
- Push port garrisons, LOPs, reserves, stores, and G2 when Europe is at war.
- Block Irish entry into faction unless Ireland is attacked, Britain collapses into a direct security crisis, or player route overrides it.
- Pause Northern settlement if preparedness is low.

### G2 and counter intelligence

G2 should react to foreign access pressure, IRA exposure, German contact, and port compromise.

- Increase counter intelligence missions when German contact is active or Britain reports intelligence risk.
- Support historical cooperation through limited information sharing without formal alliance.
- Raise constitutional authority on successful exposure reduction.
- Trigger failure if repeated ignored exposure reaches the crisis band.

### Local Defence Force

The LDF actor supports defensive mobilisation.

- High priority when Ireland is neutral in a general war.
- Low priority during peaceful early politics if equipment is scarce.
- Route variants alter unit shape: civic reserves for historical routes, labour defence committees for Labour, Guard formations for Blueshirt, and irregular integration or suppression for IRA route.
- Must not produce repeated free divisions. Unit growth uses equipment, manpower, state targets, and readiness thresholds.

### Constitutional opposition

The opposition actor represents Fine Gael legalism and non paramilitary conservatives.

- Prefer elections, parliamentary votes, Commonwealth cooperation, legal advisor unlocks, and British trust missions.
- Reject Blueshirt paramilitary escalation after route lock.
- Support Northern settlement only through safeguards and treaty work.
- Use anti dependency when British cooperation becomes heavy.

### Labour movement

The Labour actor should evaluate democracy, worker support, church backlash, industry burden, and sponsor risk.

- Prefer legal route if authority is stable and violence low.
- Consider social republic only under high unemployment, poor legitimacy, or failed cabinet crisis.
- Use social reform and industry missions before military radicalism.
- Avoid Soviet dependency unless democratic sponsors are impossible and route has moved left.

### Blueshirt organization

The Blueshirt actor should be dangerous, route locked, and failure prone.

- Attempts consolidation only when opposition has failed, authority is low, or anti communist pressure is high.
- Converts paramilitary strength into state command at the cost of legitimacy.
- Pursues coercive Northern actions only when readiness is high and Britain is constrained.
- Can trigger backlash or split if constitutional opposition remains strong.

### IRA underground

The IRA actor should pursue cells, arms, Northern pressure, and foreign contact only when state authority is weak or route chosen.

- Builds safehouses before open operations.
- German contact raises exposure and foreign access pressure.
- Failed missions empower G2, Britain, and unionist actors.
- Successful route must convert underground power into civil authority or risk permanent instability.

### Northern local groups

Northern local groups should be scoped to state variables or state modifiers.

- Nationalist committees grow through low violence missions and social aid.
- Unionist alarm grows through armed incidents, border units, and German contact.
- Labour links grow through social reform and low sectarian pressure.
- Integration cannot complete if alarm, violence, or foreign dependency remains high.

## War state reaction matrix

| Campaign state | Historical neutral | Commonwealth cooperation | Labour democratic | Labour social republic | Blueshirt | IRA underground |
| --- | --- | --- | --- | --- | --- | --- |
| Peace in Europe | constitution, industry, ports | opposition, legal route, British trust | reforms, relief, industry | councils, reforms, careful diplomacy | route consolidation if allowed | safehouses only if route chosen |
| Germany at war with Britain | Emergency defence and strict access | staff talks and port rules | defence committees and relief | anti fascist caution, no reckless Comintern | anti communist mobilization | possible German contact if rare path active |
| Britain under invasion threat | coast, reserves, stores | conditional support, no puppet acceptance | defence first, settlement delayed | defence first, avoid Soviet trap | opportunity only if Britain weak and readiness high | uprising temptation but high risk |
| Britain capitulated or exiled | emergency protectorate evaluation | Atlantic security bargain | humanitarian and settlement review | anti fascist legitimacy if Germany dominant | coercive route tempted | Northern operation tempted |
| United States joins war | diaspora and recognition | Atlantic cooperation | democratic support | reduce Soviet dependency if possible | lower Axis leaning | German contact becomes more dangerous |
| Soviet Union at war with Germany | neutral observation | low relevance | anti fascist solidarity | Soviet recognition possible | anti communist pressure | German contact risk rises |
| Ireland attacked | join defensive war, mobilize | seek British help if valid | mobilize civic defence | seek sponsors but protect autonomy | militarize state | survival uprising or state takeover |
| Northern violence crisis | pause if unprepared | safeguards and arbitration | labour mediation | worker committees if safe | crackdown and incidents | uprising if ready |

## Northern settlement AI thresholds

The implementation should tune exact values through constants, scripted values, or documented tuning. This design uses bands.

| Settlement action | AI required conditions | AI refusal conditions | Failure consequence |
| --- | --- | --- | --- |
| Border survey | route has Northern interest, authority safe | active civil crisis or foreign invasion | raises partition pressure if mishandled |
| Nationalist committee mission | violence low, legitimacy moderate | Blueshirt coercion active, IRA exposure high | repression or unionist alarm |
| Labour cross border committee | Labour route, social reform credibility, low sectarian alarm | high church backlash, low authority, violence | labour route loses Northern trust |
| Observer plebiscite | high legitimacy, British willingness, safeguards | Britain hostile, unionist alarm high, foreign access high | failed observer mission and settlement delay |
| Commonwealth settlement | opposition route, Britain valid, autonomy protected | puppet risk high, strict neutral lock | dependency pressure and route crisis |
| Coercive ultimatum | Blueshirt or defensive emergency, military readiness high | Britain strong and hostile, Ireland unprepared | British warning or intervention |
| IRA uprising | IRA route, cells ready, local support high, exposure controlled | Germany invalid after contact, G2 pressure high, no support | crackdown and route collapse |
| Emergency protectorate | Britain collapsed or Northern chaos, Ireland prepared | peacetime Britain intact, low authority | legitimacy loss and unionist resistance |

## Sponsor behavior and dependency limits

AI Ireland should treat sponsor aid as a risk. Aid gives tools, but repeated aid creates pressure.

- First aid stage can be accepted if the route needs it and access pressure is low.
- Second aid stage requires an anti dependency plan or high survival threat.
- Third aid stage should be rare and route defining.
- Any aid that grants port access should require war danger, clear duration, cleanup, and pressure growth.
- Sponsors should not give aid to routes that oppose their ideology or strategic interest unless the route has a special bridge.

## AI invalid route blockers

These blockers should be common scripted triggers reused across focuses and decisions.

| Blocker | Applies to | Rule |
| --- | --- | --- |
| `ire_ai_block_dead_sponsor` | foreign aid and access | target sponsor does not exist, has capitulated without exile handling, or is hostile |
| `ire_ai_block_wrong_route` | route decisions | country lacks matching route flag or has mutually exclusive route flag |
| `ire_ai_block_missing_northern_target` | Northern actions | required state group does not exist in current map or is already integrated |
| `ire_ai_block_unprepared_border_action` | coercive and uprising actions | no supplied units, no local support, or low preparedness |
| `ire_ai_block_high_dependency` | sponsor aid | foreign access pressure is in danger band and no anti dependency mission is active |
| `ire_ai_block_peace_obsolete_war_mission` | Emergency missions | general war has ended and no postwar cleanup target remains |
| `ire_ai_block_hidden_culture_bloat` | hidden cultural restoration | mechanic has not been accepted through final review and route lacks gameplay payoff |

## Cleanup and fallback rules

The AI package needs cleanup because Ireland can switch ideology, lose targets, form a unified identity, be invaded, or have sponsors disappear.

- Clear route specific strategy plans when a mutually exclusive political route locks.
- Cancel or hide obsolete decisions after all island settlement, failed uprising, general peace, sponsor capitulation, or Irish faction entry.
- Convert temporary Northern local variables into integration variables after a settlement.
- Clear sponsor access flags after war, expired treaty, or sponsor defeat.
- Replace IRA underground AI weights with integration or survival weights after successful territorial control.
- Replace Blueshirt border incident weights with occupation and integration weights after conquest.
- Prevent AI from collecting incompatible rewards by checking route flags before every late focus and decision.
- Keep a safe historical fallback only for AI behavior after invalidation. This fallback should pick defence, authority repair, and industry repair. It should not unlock new political content.
