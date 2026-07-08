# Ireland focus tree asset prompt for hoi4-feature-assets

Feature slug: `ireland_focus_tree`
Feature name: Ireland comprehensive national focus tree

This prompt is for the visual asset workflow. It is not a localisation file. Do not create final focus names, decision names, slogans, quotes, event prose, or achievement titles from these working labels.

Follow `hoi4-feature-assets` and `hoi4-frame-animation` where animation is requested. Inspect the relevant reference folders before creating assets:

- `.agents/skills/hoi4-feature-assets/assets/focuses`
- `.agents/skills/hoi4-feature-assets/assets/ideas`
- `.agents/skills/hoi4-feature-assets/assets/decisions`
- `.agents/skills/hoi4-feature-assets/assets/achievements`
- `.agents/skills/hoi4-feature-assets/assets/flags`
- `.agents/skills/hoi4-feature-assets/assets/news_event_images`
- `.agents/skills/hoi4-feature-assets/assets/report_event_images`

## Source mode rules

Use sourced asset work for real people, real historical flags, real party or movement symbols, real documents, and real photographed or archival scenes. Use generated art for focus icons, idea icons, decision icons, achievement icons, fictional flags, fictional route emblems, symbolic councils, UI panels, and alternate history scenes that do not depict a real event.

Do not generate real leader portraits. Do not invent historical flag status. Do not use historical symbols without source notes. Do not derive idea or decision icons by resizing focus icons.

## Required leader and advisor portraits

Sourced portraits are required if any of these figures appear as leaders, advisors, high command, or visible event figures:

| Working asset | Person | Use | Source mode | Notes |
| --- | --- | --- | --- | --- |
| `leader_eamon_de_valera` | Éamon de Valera | historical leader | sourced | Use contemporary or period suitable portrait. |
| `leader_douglas_hyde` | Douglas Hyde | president or cultural figure | sourced | Use if presidency is visible. |
| `advisor_sean_lemass` | Seán Lemass | industry and supplies | sourced | Industry branch. |
| `leader_wt_cosgrave` | W. T. Cosgrave | opposition route | sourced | Democratic opposition. |
| `advisor_sean_mac_eoin` | Seán Mac Eoin | opposition or military | sourced | Verify role before final implementation. |
| `leader_william_norton` | William Norton | Labour route | sourced | Labour democratic route. |
| `advisor_frank_ryan` | Frank Ryan | anti fascist advisor | sourced | Context sensitive. Use only if route includes him. |
| `leader_eoin_oduffy` | Eoin O'Duffy | Blueshirt route | sourced | Authoritarian route. |
| `advisor_daniel_mckenna` | Daniel McKenna | military and Emergency | sourced | Chief of Staff era. |
| `advisor_hugo_macneill` | Hugo MacNeill | military | sourced | Verify use. |
| `leader_sean_russell` | Seán Russell | IRA route | sourced | Dangerous route, context sensitive. |
| `leader_stephen_hayes` | Stephen Hayes | IRA route | sourced | Plan Kathleen context requires care. |

Generated or symbolic portraits are allowed for these collective bodies:

| Working asset | Body | Use | Source mode | Notes |
| --- | --- | --- | --- | --- |
| `leader_army_council_body` | Army Council | IRA hard route collective leader | generated | Institutional portrait, no personal random name. |
| `leader_corporate_chambers_body` | Corporate chambers | Blueshirt collective alternative | generated | Symbolic council or chamber, not a crowd. |
| `leader_labour_executive_body` | Labour executive council | Labour collective alternative | generated | Institutional portrait. |

## Flag and emblem assets

Final flag files must use HOI4 flag sizes and paths. Preserve the base Irish tricolour unless the implementation explicitly creates route cosmetic tags.

| Working asset | Use | Source mode | Notes |
| --- | --- | --- | --- |
| `flag_ireland_base` | base country | existing or sourced | Do not replace if already valid. |
| `flag_ireland_social_republic` | Labour capstone cosmetic | generated or sourced motif review | Must stay readable at 82x52, 41x26, 10x7. |
| `flag_ireland_corporate_state` | Blueshirt capstone cosmetic | sourced or generated synthesis | Historical symbols need source notes. |
| `flag_ireland_revolutionary_republic` | IRA capstone cosmetic | sourced or generated synthesis | Republican symbols need source review. |
| `flag_ireland_unified_constitutional` | all island formable if distinct | sourced or generated civic variant | Only if distinct from base. |
| `flag_ireland_cultural_epilogue` | rare ceremonial epilogue | generated or sourced cultural motif | No monarchy or occult theme. |
| `emblem_atlantic_compact` | rare neutral compact faction | generated | Faction emblem, not country flag. |

## Focus icon families

Every implemented focus needs an icon. Large families can share motifs, but final icons must be selected per focus and should not be left generic.

| Family | Target size | Source mode | Motifs |
| --- | --- | --- | --- |
| opening constitutional trunk | 94x86 | generated | Dáil chamber, constitution, ballot, public order, old ledgers, army review |
| historical neutrality | 94x86 | generated | constitution, port transfer, coast watch, neutral shipping, Emergency cabinet |
| opposition route | 94x86 | generated | parliament, legal restraint, London channel, defensive liaison, boundary office |
| Labour route | 94x86 | generated | union hall, cooperative factories, worker defence, anti fascist veterans, rural works |
| Blueshirt route | 94x86 | generated with historical symbol caution | paramilitary order, corporate chambers, anti communist cadres, frontier pressure |
| IRA route | 94x86 | generated with historical symbol caution | safehouses, border cells, sabotage files, courier risk, revolutionary council |
| industry branch | 94x86 | generated | Shannon power, sugar beet, turf, ports, native manufactures, emergency stores |
| military branch | 94x86 | generated | regular battalions, LDF, LOPs, port batteries, Air Corps, naval patrols, G2 |
| diplomacy branch | 94x86 | generated | League voice, London, Washington, Vatican, Berlin risk, Rome and Spain, Moscow |
| Northern settlement | 94x86 | generated | border survey, committees, observer ballots, frontier defence, integration office |
| late game | 94x86 | generated | all island settlement, Atlantic role, social republic, corporate state, revolutionary republic, cultural epilogue |

## Idea and national spirit icons

Target size: 64x64. Use generated icon art unless a specific historical symbol is required and sourced. Do not resize focus icons.

Required idea icon families:

- `idea_shadow_of_civil_war`
- `idea_economic_war_strain`
- `idea_treaty_ports_foreign_hands`
- `idea_small_army_long_coast`
- `idea_divided_island`
- `idea_trade_dependence`
- `idea_weak_air_naval_services`
- `idea_underground_republican_pressure`
- `idea_blueshirt_legacy`
- `idea_labour_discontent`
- `idea_emergency_powers`
- `idea_constitutional_authority`
- `idea_emergency_preparedness`
- `idea_foreign_access_pressure`
- `idea_integration_progress`

Each staged idea can use one base icon plus route variant overlays only if the final implementation confirms the game can cleanly reference variants. Otherwise produce distinct icons for major final forms.

## Decision icons and decision category icons

Decision icons target 32x32 unless repository pattern says otherwise. Decision category icons must match existing category size.

Required decision families:

- Constitutional Authority category icon.
- Emergency Preparedness category icon.
- Ports and Coast category icon.
- Economic Recovery category icon.
- Foreign Access category icon.
- Partition Settlement category icon.
- Post Settlement Integration category icon.
- Public order decisions.
- Reconciliation board decisions.
- Port transfer and port defence decisions.
- LOP and coast watch missions.
- LDF and reserve training decisions.
- Shannon grid, sugar beet, turf, and port economy projects.
- Sponsor aid, recognition, liaison, and anti dependency decisions.
- Border survey, plebiscite, observer, uprising, ultimatum, and integration decisions.

## Scripted GUI and animation assets

The Emergency Preparedness board is the main scripted GUI candidate.

| Working asset | Surface | Size | Source mode | Animation rules |
| --- | --- | --- | --- | --- |
| `ireland_emergency_board_background` | scripted GUI board | implementation defined | generated UI art | static |
| `ireland_emergency_component_card` | scripted GUI card | implementation defined | generated UI art | static variants for normal, selected, warning, complete |
| `ireland_emergency_meter_frame` | scripted GUI meter | implementation defined | generated UI art | static variants |
| `ireland_emergency_readiness_seal` | board header or category | likely 64x64 or category size | generated icon style | animated with real source frames, 6 to 8 frames, subtle signal lamp or coast watch glow |
| `ireland_emergency_warning_frame` | board warning overlay | implementation defined | generated UI art | animated only if useful, 6 to 8 frames, subtle pulse, static fallback required |
| `ireland_formation_seal` | all island formation decision or GUI | 64x64 or category size | generated seal | optional static only unless formation UI uses animation |

Every animated asset must follow `hoi4-frame-animation`. It needs source frames, processed frames, horizontal sheet PNG, sheet DDS, static fallback DDS, GIF preview for review only, manifest, and `gfx_handoff.md`. Do not create final motion from a transformed still.

## Report or news image needs

Only create report or news images if final implementation uses events for major public moments. Use direction only until implementation confirms event surfaces.

Possible presentation moments:

- Treaty Ports returned.
- Emergency coast watching network begins.
- All island settlement proclaimed.
- Violent Northern crisis or uprising if implemented as news.
- Atlantic compact conference if accepted.

Use sourced archival images for real historical events or real people. Use generated period documentary imagery for alternate history scenes or composite route outcomes.

## Achievement icons

Achievement icons target 64x64. Create completed icon first. Grey and not eligible variants follow achievement workflow.

The achievement prompt lists working achievement ids and icon direction. Use those ids for final achievement DDS names only after implementation confirms registry ids.

## Manifest and handoff requirements

For every asset, provide source PNG, processed PNG, final DDS or TGA where appropriate, status, source mode, prompt or source URL, license or uncertainty note for sourced assets, target size, intended use, sprite name proposal, and target `.gfx` handoff.

Write or update:

- `docs/assets/ireland_focus_tree/manifest.md`
- `docs/assets/ireland_focus_tree/gfx_handoff.md`
- contact sheets for large icon batches

Do not edit gameplay, localisation, GUI, or `.gfx` files unless the parent implementation prompt explicitly expands scope.

## Canonical hidden path asset addendum

`specs/ireland_focus_tree_spec_part_10_hidden_paths.md` makes hidden paths mandatory planned content. Older prompt lines that treat cultural restoration as only queued are superseded.

Required hidden path asset families:

| Hidden route | Asset needs | Source mode | Animation note |
| --- | --- | --- | --- |
| civic cultural restoration | focus icons for cultural threshold, presidential patronage, language administration, Gaeltacht development, common platform outreach, cultural diplomacy, capstone, plus idea and decision icons | generated gameplay icons, sourced review for real harp, presidential, constitutional, or Hyde material | capstone route seal can use a subtle animated glow with static fallback |
| Emergency directorate | warning seal, G2 files, LDF command, public order, directorate council, civilian restoration, permanent security fork, decision icons | generated unless real offices, real people, or real unit symbols are depicted | warning pulse optional with static fallback |
| Atlantic neutral compact | compact emblem, compass, convoy observer, arbitration office, no basing principle, member rules, decision icons | generated symbolic art | compact seal optional with static fallback |
| common platform settlement | minority guarantees, observer plebiscite, local service continuity, nonsectarian committee icons | generated symbolic icons | static preferred |
| hidden path achievements | icons for hidden route achievements added in Canonical | generated symbolic icons, source caution for historical motifs | static |

Do not put Gaelic text in generated images. Do not generate Douglas Hyde or other real people. Do not invent historical flag or symbol status.

## Route-specific hidden overlay assets

Add assets for the hidden overlays in part 10:

| Overlay | Required asset families | Source mode |
| --- | --- | --- |
| `hidden_constitutional_backchannel` | focus icons, decision icons, achievement icon, legal boundary motif | generated icons, sourced treaty or real document image only if used directly |
| `hidden_labour_independent_front` | focus icons, decision icons, idea icon, achievement icon, anti-fascist service motifs | generated icons, sourced portraits for real figures |
| `hidden_corporate_chambers_without_oduffy` | focus icons, decision icons, idea icon, chamber body portrait, achievement icon | generated symbolic chamber, sourced O'Duffy and real symbols if visible |
| `hidden_republican_reconciliation_backchannel` | focus icons, decision icons, idea icon, achievement icon, amnesty and arms surrender motifs | generated icons, source review for real IRA symbols or actors |

## Canonical consolidated hidden path asset addendum

The hidden paths in Part 10 are required asset surfaces. Add icon, idea, decision, achievement, emblem, and optional animation coverage for civic cultural restoration, Emergency directorate, Atlantic neutral compact, common platform Northern settlement, corrupted restoration failure, compromised republican network, cross border Labour Council, constitutional backchannel, corporate chambers without O'Duffy, republican reconciliation backchannel, neutral aftershock recovery, and Northern emergency protectorate.

Source mode rules remain strict. Real leaders, real flags, real unit symbols, real offices, real movement symbols, real cultural institutions, and attested emblems require sourced asset work. Generated assets are allowed for symbolic icons, fictional councils, alternate route emblems, compact seals, warning frames, and abstract UI states. Do not generate Douglas Hyde, O'Duffy, real IRA figures, real Aiséirghe figures, or historical symbols.

Animation candidates are the Emergency warning seal, compact seal, civic cultural capstone seal, and repaired beacon aftershock recovery. Every animation requires real source frames, a static fallback, sheet DDS, manifest, and handoff under the frame animation rules.
