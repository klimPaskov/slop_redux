# Ireland focus tree text and audio gate handoff

Date: 2026-07-08
Owner: `hoi4_quote_remark_researcher`
Scope: quote, cultural remark, slogan, allusion, and audio-gate research for Ireland focus tree implementation.

## Canonical inputs read

- `docs/specs/ireland_focus_tree/prompts/ireland_focus_tree_text_audio_research_prompt.md`
- `docs/specs/ireland_focus_tree/prompts/ireland_focus_tree_event_prompt.md`
- `docs/specs/ireland_focus_tree/prompts/ireland_focus_tree_flavour_event_prompt.md`
- `docs/specs/ireland_focus_tree/research/*.md`
- `docs/specs/ireland_focus_tree/specs/ireland_focus_tree_spec_part_10_hidden_paths.md`
- `docs/specs/ireland_focus_tree/specs/ireland_focus_tree_spec_part_13_event_suite.md`
- `docs/specs/ireland_focus_tree/specs/ireland_focus_tree_spec_part_19_flavour_event_layer.md`
- `.agents/skills/hoi4-text-audio-research/SKILL.md`

## Implementation rule

Plain in-world prose is the default approved writing mode. Implementation may write ordinary focus, decision, event, news, report, tooltip, and option text from the spec direction without direct quotation, slogans, prayers, song or poem fragments, exact newspaper headlines, invented Gaelic phrases, or audio cues.

Source-dependent wording is blocked unless listed under `Accepted source-dependent wording`. Working labels are not final localisation.

## Accepted source-dependent wording

Use these as short institutional anchors, title-like references, or background terms. Do not build long quotations around them.

| Surface | Accepted wording or term | Source | Confidence | Copyright and risk note | Implementation use |
| --- | --- | --- | --- | --- | --- |
| Constitution, language, civic restoration | `first official language`; `second official language` | Irish Statute Book, Constitution of Ireland, Article 8. https://www.irishstatutebook.ie/en/constitution/index.html | High | Official legal source; quote only these short fragments if needed. | Safe for tooltips, event prose, or focus descriptions about language administration. Prefer prose like "Irish-language administration" instead of quoting full Article 8. |
| Constitution milestone | `Enacted by the People 1st July, 1937`; `In operation as from 29th December, 1937` | Irish Statute Book, Constitution of Ireland front matter. https://www.irishstatutebook.ie/en/constitution/index.html | High | Official legal source; use only dates or a short reference. | Safe to say the constitution was enacted on 1 July 1937 and came into operation on 29 December 1937. |
| Treaty Ports | `Treaty Ports`; `harbour defences`; `Cobh`; `Berehaven`; `Lough Swilly` | Documents on Irish Foreign Policy, transfer records. https://www.difp.ie/volume-5/1938/transfer-of-treaty-ports/2338/ | High | Proper names and short document terms. DIFP page carries Royal Irish Academy copyright; avoid long direct extracts. | Safe for ports return, port defence, and report-event text. Use plain prose for ceremony and negotiations. |
| Emergency law | `Emergency Powers Act, 1939`; `public safety`; `preservation of the State`; `public order`; `supplies and services` | Irish Statute Book, Emergency Powers Act 1939. https://www.irishstatutebook.ie/eli/1939/act/28/enacted/en/html | High | Official legal source; quote only short fragments. | Safe for Emergency powers debate, directorate warning, public order, rationing, and supply-control prose. |
| Coast watching | `Marine and Coast Watching Service`; `Look Out Posts`; `LOPs`; `Local Defence Force`; `LDF`; `Coastwatchers` | Military Archives, Lookout Post Logbooks. https://www.militaryarchives.ie/en/reading-room-collections/lookout-post-logbooks | High | Proper institutional terms; safe as terms. | Safe for Emergency/coastwatch/G2 events and reports. It is also safe to mention 83 LOPs and the September 1939-June 1945 logbook collection. |
| Civic cultural restoration | `non-political and nonsectarian` | National Library of Ireland, Douglas Hyde, Eoin MacNeill, and the Gaelic League. https://www.nli.ie/1916/exhibition/en/content/stagesetters/culture/hyde-macneill/ | High for NLI wording | Modern NLI text; exact phrase is short, but prefer paraphrase. | Safe direction: "civic, non-sectarian cultural work." Avoid making this a slogan. |
| Civic cultural flavour | `Schools' Collection`; `Irish Folklore Commission`; `National Folklore Collection` | UCD National Folklore Collection. https://www.ucd.ie/irishfolklore/en/collections/schoolscollectionduchas/ | High | Proper institutional terms. | Safe for schoolhouse, folklore collector, archive, and cultural administration events. |
| Labour and anti-fascist route context | `International Brigades`; `Republican Congress`; `Frank Ryan` as a historical actor | Queen's University Belfast Frank Ryan project. https://www.qub.ac.uk/sites/frankryan/InterpretativeResources/HistoricalContext/FrankRyanArevolutionarylife/ | Medium-high secondary academic context | Do not quote Ryan or songs. Use names and plain prose only. | Safe to ground events in anti-fascist veteran memory, democratic worker defence, and the risk of later German contact controversy. |
| Blueshirt/O'Duffy route context | `Blueshirts`; `National Guard`; `corporate state`; `National Corporate Party`; `Irish Brigade` | History Ireland, Eoin O'Duffy's Blueshirts and the Abyssinian crisis. https://historyireland.com/eoin-oduffys-blueshirts-and-the-abyssinian-crisis/ | Medium-high secondary scholarly context | Do not quote fascist or corporatist rhetoric. Avoid slogans and salutes. | Safe for uneasy authoritarian prose, leader crisis, chamber-state mechanics, and foreign-right contact risk. |
| IRA/German contact context | `Plan Kathleen`; `Hermann Goertz`; `Stephen Hayes`; `Seán Russell`; `IRA foreign contact`; `Abwehr` | The Irish Story, Hermann Goertz. https://www.theirishstory.com/2019/05/13/herman-goertz-a-german-spy-in-wartime-ireland/ | Medium secondary context; use with caution | Do not quote Goertz, IRA slogans, or Nazi-linked wording. | Safe to frame Plan Kathleen as exposure, dependency, amateur/incompetent planning risk, and a counter-intelligence crisis. |

## Considered quote and allusion candidates

No full main quote is selected for implementation. The safest package is a no-quote recommendation with short institutional anchors above.

| Candidate | Package | Status | Reason |
| --- | --- | --- | --- |
| Constitution Article 8 language fragments | constitution, civic cultural restoration | Accepted only as short legal fragments | Strong official source and exact wording. Useful but should not become dramatic quote text. |
| Constitution preamble religious language | constitution, civic cultural restoration, flavour church surfaces | Blocked | Prayer-like and too loaded for ordinary UI. It risks over-defining route theology and is not needed for mechanics. |
| Constitution Article 1 sovereignty wording | constitution, all-island, diplomacy | Needs review | Official source, but long and rhetorically broad. Use plain prose unless a future quote pass approves a very short fragment. |
| Original 1937 Articles 2 and 3 national-territory language | all-island settlement, Northern route | Blocked for direct use | Period-relevant but politically charged and not directly available in the current Irish Statute Book consolidated text. Use plain settlement/guarantee prose instead. |
| `non-political and nonsectarian` Gaelic League wording | civic cultural restoration, common platform | Accepted as a short source note; prefer paraphrase | Good fit for civic cultural restoration and common platform. Do not make it a motto. |
| `Look Out Posts` / `LOPs` | Emergency/coastwatch | Accepted | Proper institutional term from Military Archives. Strong fit and low risk. |
| `transfer of harbour defences` | Treaty Ports | Accepted as document-style terminology | Good fit for ports handover and report events. Avoid copying the DIFP draft press notice. |
| Labour/Connolly slogans or quotations | Labour route | Blocked | Not researched in this pass and may misframe the 1930s Labour route as Connolly memorial rhetoric rather than democratic government. |
| Frank Ryan direct quotations, ballad fragments, or Spanish Civil War songs | Labour/anti-fascist route | Blocked | Copyright and attribution risk; also politically charged. Use plain prose about anti-fascist veterans and International Brigade memory. |
| O'Duffy, Blueshirt, corporate-state, or foreign-fascist slogans | Blueshirt/corporatist route | Blocked | Extremist rhetoric risk and not needed for gameplay. Use uneasy authoritarian prose. |
| IRA slogans, republican song fragments, prisoner songs, or Plan Kathleen wording | IRA route | Blocked | Attribution, copyright, and extremist-romanticization risk. Use plain prose about exposure, cells, couriers, raids, and dependency. |
| Gaelic phrases, mottoes, prayers, proverbs, folklore titles, or Irish-language button text | civic, flavour, cultural epilogue, achievements | Blocked unless separately approved | The implementation prompt explicitly blocks Gaelic wording without source checks. Proper names of institutions are allowed only when sourced. |
| Exact newspaper headlines, radio announcements, or diaspora letters | flavour events, report/news events | Blocked | Requires separate source check and copyright review. Use invented in-world summaries, not exact headlines. |
| Audio cues from Irish songs, hymns, marches, ballads, folk recordings, or anthem material | all audio surfaces | Blocked pending audio researcher | Composition and recording rights are separate. No audio is safe from this handoff. |

## Package gate table

| Package or surface | Plain in-world prose | Source-dependent wording gate |
| --- | --- | --- |
| `constitution_sovereignty_package` | Safe. Use sober legal/state-building prose, dates, presidency, referendum, cabinet, courts, and constitutional authority. | Short Article 8 fragments are safe. Preamble, prayers, Article 1 quote, and old Article 2/3 quote remain blocked. |
| `ports_return_package` | Safe. Use ports, evacuation, local handover, stores, batteries, training cadre, and defence responsibility. | Treaty Ports place names and "harbour defences" are safe. Do not copy DIFP press notices or ceremony wording beyond short terms. |
| `emergency_watch_package` | Safe. Use coast posts, LDF manning, incident logs, shipping and aircraft reports, and coastal defence. | `Marine and Coast Watching Service`, `Look Out Posts`, `LOPs`, `LDF`, and 83 posts are safe. No invented watchmen mottoes. |
| `neutrality_crisis_package` | Safe. Use restrained prose about pressure, ports, shipping, internment, and diplomatic risk. | Direct de Valera neutrality quotes, speeches, or newspaper lines are blocked. |
| `labour_social_republic_package` | Safe. Use democratic Labour, trade unions, cooperatives, worker defence under law, anti-fascist veteran memory, and International Brigade context. | Frank Ryan direct quotes, Connolly quotes, songs, Spanish Civil War slogans, and Soviet movement phrases are blocked. |
| `blueshirt_corporatist_package` | Safe. Use authoritarian risk, public order, chamber institutions, leader overreach, foreign-right exposure, and anti-communist mobilisation. | O'Duffy quotes, Blueshirt slogans, salutes, fascist/corporatist slogans, and real movement imagery wording are blocked. |
| `ira_underground_package` | Safe. Use safehouses, arms caches, couriers, G2 files, Plan Kathleen exposure, British reaction, and foreign dependency. | IRA slogans, song lines, prisoner rhetoric, Goertz quotes, Nazi-linked phrases, and clean victory language are blocked. |
| `all_island_settlement_package` | Safe. Use legal settlement, guarantees, observers, local administration, safeguards, integration work, and British/unionist reaction. | Direct constitutional territorial claims, proclamation language, slogans, and triumphalist phrases are blocked. |
| `violent_northern_crisis_package` | Safe. Use severe plain prose about ultimatum, local danger, supply, policing, and backlash. | Coercive slogans, jokes, sectarian phrasing, and triumphalist allusions are blocked. |
| `atlantic_compact_package` / `atlantic_neutral_compact_package` | Safe. Use small-state conference, neutral shipping, observation, arbitration, no-basing principles, and member doubts. | No "conference of neutrals" as a sourced title unless treated as an invented in-world title. Audio and period conference quotations remain blocked. |
| `hidden_civic_cultural_restoration_package` / `cultural_epilogue_package` | Safe. Use civic institutions, schools, civil service, Hyde as cultural anchor if sourced elsewhere, Gaeltacht development, and non-sectarian outreach. | Gaelic mottoes, folklore lines, songs, prayers, high-kingship wording, and occult/mythic allusions are blocked. The NLI "non-political and nonsectarian" phrase is safe only as a short reference or paraphrase. |
| `common_platform_settlement_package` | Safe. Use guarantees, observers, minority protections, schools, local policing, shared civic work, and non-coercive settlement. | Direct legal charter language, all-island slogans, or exact cross-community quotations remain blocked. |
| `emergency_directorate_package` | Safe. Use survival tradeoff, public order, G2 records, LDF command, restoration timetable, and democratic cost. | Real office slogans, speeches, decrees, or exact emergency notices are blocked except short Emergency Powers Act fragments above. |
| `achievement_reference_package` | Safe only with invented/plain achievement text that does not imply a sourced allusion. | Working labels such as `restoration_without_a_crown`, `watchmen_of_the_west`, `conference_of_neutrals`, and `no_crown_no_courier` are not approved as final allusions. They need a separate title pass if implementation wants clever sourced titles. |
| Flavour event cultural surfaces | Safe. Use concrete ordinary prose about schools, parish halls, radio rooms, ration queues, creameries, turf, coast posts, border markets, local councils, Red Cross work, and postwar memory. | Irish-language phrases, folklore titles, church wording, exact broadcast lines, exact letters, newspaper headlines, songs, proverbs, and prayers remain blocked. |

## Audio gate

No audio candidate is selected or cleared.

Audio remains blocked for:

- all-island settlement reveal
- Emergency board or coastwatch custom GUI reveal
- Atlantic compact conference or faction reveal
- Labour, Blueshirt, or IRA capstone cue
- route achievements, news stingers, report-event stingers, and flavour-event sound cues

Reason: this pass did not verify any recording license, composition rights, duration, source file, or conversion path. If implementation decides a major surface needs audio, spawn `hoi4_audio_researcher` with the exact use, length, mood, and final file path target. Public-domain composition names are not enough; the specific recording must be licensed.

## Short implementation recommendation

Implement text now using plain in-world prose and the accepted institutional terms above. Do not include direct quotes, slogans, Gaelic phrases, prayers, song or poem fragments, exact headlines, or audio. When a surface feels like it needs a memorable line, use a neutral invented sentence that describes the visible action and consequence, not a source-dependent cultural reference.

## Sources checked

- Irish Statute Book, Constitution of Ireland: https://www.irishstatutebook.ie/en/constitution/index.html
- Irish Statute Book, Emergency Powers Act 1939: https://www.irishstatutebook.ie/eli/1939/act/28/enacted/en/html
- Documents on Irish Foreign Policy, Transfer of Treaty Ports, 1 June 1938: https://www.difp.ie/volume-5/1938/transfer-of-treaty-ports/2338/
- Documents on Irish Foreign Policy, Transfer of Treaty Ports, 18 May 1938: https://www.difp.ie/volume-5/1938/transfer-of-treaty-ports/2330/
- Military Archives, Lookout Post Logbooks: https://www.militaryarchives.ie/en/reading-room-collections/lookout-post-logbooks
- National Library of Ireland, Douglas Hyde, Eoin MacNeill, and the Gaelic League: https://www.nli.ie/1916/exhibition/en/content/stagesetters/culture/hyde-macneill/
- UCD National Folklore Collection, Schools' Collection: https://www.ucd.ie/irishfolklore/en/collections/schoolscollectionduchas/
- Queen's University Belfast, Frank Ryan: A revolutionary life: https://www.qub.ac.uk/sites/frankryan/InterpretativeResources/HistoricalContext/FrankRyanArevolutionarylife/
- History Ireland, Eoin O'Duffy's Blueshirts and the Abyssinian crisis: https://historyireland.com/eoin-oduffys-blueshirts-and-the-abyssinian-crisis/
- The Irish Story, Hermann Goertz, a German spy in wartime Ireland: https://www.theirishstory.com/2019/05/13/herman-goertz-a-german-spy-in-wartime-ireland/
