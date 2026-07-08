# Ireland focus tree spec, part 1 core

## Feature promise

The Ireland tree should make a small neutral country feel politically tense, strategically exposed, and full of credible choices. The player begins with a state still shaped by the Civil War, the Anglo-Irish settlement, the economic war with Britain, partition, and a weak military position on a long coastline. The historical path should let Ireland build sovereignty through constitutional change, the return of the Treaty Ports, strict neutrality, emergency defence, and careful diplomacy. Alternate paths should come from pressures that already existed in Irish politics rather than from a generic ideology menu.

The tree should be playable as a layered national strategy. It should not be a collection of small modifiers. Every route should change how Ireland manages authority, neutrality, partition, industry, coastal defence, and foreign pressure.

## Design stance

This package uses path level focus planning. The implementation agent can choose exact focus count, coordinates, prerequisites, and final focus text, but the finished tree must preserve the route logic, branch payoffs, decision families, AI behavior, idea lifecycles, and historical constraints defined here.

The tree should support a large focus count because Ireland is the featured country. A likely implementation target is 170 to 220 focuses including shared support lanes, route locked branches, post formation branches, and hidden branch content. The number can change during implementation if the route depth remains intact.

## Main historical anchors

The historical route should begin before the 1937 constitution is fully settled, then move through sovereignty consolidation, the 1938 British Irish settlement, the transfer of the Treaty Ports, and the wartime Emergency. The plan should treat the 1937 constitution as a major sovereignty milestone, not a passive stability reward. It should treat the ports settlement as a strategic fork because possession of Cobh, Berehaven, and Lough Swilly changes neutrality, coastal defence, and British pressure.

The Emergency is the main military and diplomatic crisis. Ireland has to build coast watching, intelligence, local defence, rationing capacity, port security, and enough forces to deter pressure without becoming a normal major power. The military path should offer meaningful tools while keeping Ireland vulnerable if the player ignores preparedness.

Partition is the long term pressure. Reunification should never be a simple claim ladder. It should be managed through recognition, border politics, Northern nationalist networks, British leverage, unionist resistance, war conditions, and post settlement integration.

## Starting country condition

Ireland begins with a civilian government led by Éamon de Valera and Fianna Fáil. The player has legitimacy inside the Dáil, but the state still has rivals outside constitutional politics. The IRA can embarrass or challenge the government. The Blueshirt legacy can be folded into parliamentary opposition or pushed into a corporatist route. Labour and trade union politics can become a disciplined constitutional force or a more radical social republic. Fine Gael and Cumann na nGaedheal veterans can restore a stronger Commonwealth leaning constitutional opposition without becoming a fascist path by default.

The economy begins small, rural, and trade exposed. The player should care about the end of the economic war, industrial self sufficiency, electrification, sugar beet, turf, ports, and emergency supply. Industry rewards should place factories, infrastructure, railways, ports, airbases, anti air, and resources in relevant regions where possible.

The military begins too small for its coastline. The player can professionalize the regular army, raise the Local Defence Force, expand coast watching, build the Air Corps, create a modest naval service, or pursue route specific militia structures. Military growth should come from decisions, missions, equipment costs, training, mobilisation, and defensive state objectives rather than repeated free division focuses.

## Visible mechanics

### Constitutional authority

A visible value or national spirit family should measure whether the state governs through parliamentary legitimacy, emergency powers, party discipline, militia pressure, or underground coercion. It should affect political focuses, decision costs, internal crises, advisor availability, and route locks.

Recommended components:

- Dáil legitimacy, associated with elections, constitutional reforms, public order, and legal parties
- Armed movement pressure, associated with the IRA, Blueshirts, and later route militias
- Emergency executive reach, associated with wartime powers, censorship, rationing, and security measures
- Public reconciliation, associated with Civil War memory, amnesty, veterans, and cross party settlement

High legitimacy should reduce unrest, improve diplomatic recognition, and support negotiated reunification. High armed movement pressure should unlock violent routes and cheap paramilitary tools while risking crackdown events, loss of foreign trust, and splinter crises. High emergency reach should help during wartime but can damage democratic routes if overused.

### Emergency preparedness

This value measures ports, coast watching, reserves, supply stocks, air warning, communications, and trained local defence. It should affect invasion response, British pressure, German pressure, neutral credibility, and the chance of successful emergency missions.

Preparedness should increase through military, industry, and neutrality focuses. It should also rise from decisions that cost infantry equipment, support equipment, trucks, trains, fuel, civilian factory time, army XP, and state control objectives. If preparedness stays low during a major war, Ireland should suffer harder crises, harsher foreign pressure, and weaker starting units if attacked.

### Partition pressure

This value measures how active the Northern question is. It should be raised by border agitation, IRA actions, British weakness, war in Europe, unionist fear, and route propaganda. It should be lowered or stabilized by arbitration, diplomatic restraint, cross border economic agreements, and legal settlement work.

Partition pressure should unlock different reunification tools by route. The historical route can seek postwar arbitration or a neutral settlement. Fine Gael can seek Commonwealth backed review. Labour can support workers and trade unions across the border. IRA and corporatist routes can escalate pressure quickly, but they should provoke stronger British and unionist resistance.

### Foreign access pressure

Ireland should track how much leverage foreign powers gain over its neutrality. British access, German access, Italian or Spanish right wing ties, Soviet or International Brigade ties, American diplomatic support, and Vatican influence can all appear where route relevant. Foreign access is not only a diplomacy number. It should affect decisions, advisors, equipment aid, intelligence risk, faction entry, trade terms, and postwar legitimacy.

## Primary route families

### Historical sovereign neutrality

This route is the intended historical line. It strengthens de Valera, builds Éire through constitutional legitimacy, resolves the economic war, reclaims the ports, prepares for the Emergency, suppresses reckless underground activity, and keeps Ireland neutral. The route should not be boring. It should force the player to balance British pressure, German probes, Irish American opinion, coast defence, rationing, intelligence, and partition demands.

The route payoff is a sovereign neutral state with high preparedness, a reformed economy, and the option to pursue postwar reunification through arbitration or a rare major power settlement.

### Constitutional opposition and guarded Commonwealth cooperation

This route represents a parliamentary alternative built from Cumann na nGaedheal, Fine Gael, W. T. Cosgrave, and moderate opposition to Fianna Fáil. It should not be a copy of the fascist route. It preserves democracy, leans toward legalism, reassures Britain, and can enter a negotiated defence relationship if Europe descends into war.

The route payoff is a more pro Allied, more Commonwealth friendly Ireland that can bargain for partition concessions in exchange for cooperation. It should be possible to remain independent, to associate with the Allies, or to enter a limited defence pact if the world situation justifies it.

### Labour and social republic

This route grows from Labour, trade unions, Connolly memory, cooperative economics, and anti fascist internationalism. William Norton, trade union figures, and the legacy of Irish participation in the International Brigades should shape the route. It should be able to remain democratic socialist, become a stronger labour republic, or align with wider anti fascist forces.

The route payoff is a social republic that industrializes through cooperative boards, worker defence committees, and anti fascist diplomacy. It can seek all island labour solidarity, but it must manage Church opposition, employer resistance, and foreign suspicion.

### Blueshirt corporatist Ireland

This route must be route locked and politically costly. It grows from Eoin O'Duffy, the National Guard, Catholic corporatism, anti communism, Spain, Italy, and a desire to discipline the state after years of Civil War bitterness. It is not the normal Fine Gael route. The route should produce a National Corporate State style outcome only after the player empowers the militant right and weakens parliamentary checks.

The route payoff is a militarized corporatist Ireland with foreign right wing ties, anti communist military missions, and an aggressive Northern policy. It should gain manpower and command tools but lose democratic legitimacy, provoke internal opposition, and face serious diplomatic consequences.

### IRA underground republic

This route grows from the IRA's illegal status, the S-Plan, the Northern question, contacts with German intelligence, and the idea that the Dáil government has failed the republic. It should be powerful but unstable. It can either force the state to absorb and discipline the underground or let the Army Council overshadow civil government.

The route payoff is a high risk revolutionary republic that can escalate the border, sabotage British infrastructure, coordinate with foreign enemies of Britain, or create a state security crisis. Germany should not become a clean magic sponsor. Foreign support should bring intelligence exposure, dependence, and the risk of the player becoming a tool of another power.

### Hidden civic cultural restoration route

A hidden civic cultural restoration branch is accepted in part 10. It is not treated as ordinary historical inevitability, monarchy content, or fantasy kingship. It draws from constitutional language status, civic cultural institutions, public education, Gaeltacht development, presidential legitimacy, and non coercive Northern reconciliation.

The route requires rare public conditions, high Constitutional Authority, low armed pressure, low foreign dependency, and completed cultural or civic work. It should reveal through decisions, missions, and tooltips only after the player has earned it. Part 10 is the source of truth for this hidden route.

## Support lanes

### Economy and industry

This lane should support every route, with branch variants based on policy. Core historical themes include economic war recovery, state backed industry, sugar beet, native manufacturing, turf, ports, electrification, fisheries, railways, and emergency supply. The lane should build industry on the map and should unlock construction decisions rather than only granting passive modifiers.

### Military and emergency defence

This lane should build a defensive state. It includes army professionalization, reserve training, Local Defence Force, coast watching, port defence, air observation, air corps growth, naval patrols, intelligence, and supply stockpiles. Route variants decide whether defence remains constitutional, becomes militia heavy, leans to Allied cooperation, or becomes revolutionary.

### Diplomacy and neutrality

This lane defines Ireland's international posture. Historical neutrality should be difficult but rewarding. Pro Allied cooperation, anti fascist alignment, corporatist Catholic diplomacy, and IRA German links should each have different costs. The lane should also decide how Ireland treats the League, the Commonwealth, Washington, the Vatican, Berlin, Rome, Madrid, and Moscow.

### Reunification and settlement

This lane must be separate from politics and industry. It handles Northern Ireland, border commissions, plebiscites, pressure campaigns, armed routes, external guarantees, and post settlement integration. It should include several valid pathways, but every path needs diplomatic reaction, state control checks, local support, and resistance management.

## Route lock philosophy

The first two years should let the player prepare while revealing route pressures. The major political lock should come after the constitution, the opposition crisis, or a major public order confrontation. Historical neutrality, constitutional opposition, Labour, Blueshirt, and IRA routes should be mutually exclusive after the lock. Support lanes continue, but route identities alter their effects.

The implementation should avoid overusing mutually exclusive blocks for support branches. Economy, emergency defence, and many diplomacy support focuses should remain open unless a route explicitly contradicts them.

## Starting state groups for planning

Final state ids should be verified during implementation. This package uses geographic state group direction only.

- Dublin and eastern administration: Dublin, Wicklow, Kildare, Meath, and Louth where the map supports them
- Western ports and Atlantic coast: Galway, Mayo, Sligo, Donegal if held or claimed, Kerry, Clare, and western coastal states
- Treaty Port sites: Cobh and Cork harbour, Berehaven and Bantry Bay, Lough Swilly and Donegal approaches
- Industrial east and south: Dublin, Cork, Waterford, Limerick, Carlow, and surrounding industrial or port states
- Shannon and midlands development: Limerick, Clare, Offaly, Westmeath, Roscommon, Tipperary, and bog or hydro relevant regions
- Border counties: Donegal, Leitrim, Cavan, Monaghan, Louth, and any adjacent Northern states
- Northern Ireland settlement zone: Belfast, Derry, Armagh, Fermanagh, Tyrone, Antrim, Down, and border adjacent states if the map separates them

## What this tree should not do

- Do not make Ireland a normal great power through free factories.
- Do not make neutrality a passive waiting route.
- Do not reduce reunification to clicking claims.
- Do not turn Fine Gael into the Blueshirts by default.
- Do not make the IRA route a clean German alliance without internal cost.
- Do not make Labour a generic Soviet branch unless the player chooses that direction.
- Do not give every route the same industrial and military rewards.
- Do not let hidden routes crowd the historical and plausible alternate history paths.
