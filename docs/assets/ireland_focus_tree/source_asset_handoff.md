# Ireland Focus Tree Real-Source Asset Handoff

Review date: 2026-07-08

Scope: source-status verification for real leaders, real flags, real symbols, and real historical/photo assets likely to matter for the Ireland focus tree and BOP addendum. This pass did not edit gameplay, localisation, `.gfx`, focus, decision, spec, or final asset files. It did not generate art, process PNGs, convert DDS files, or download source images.

Canonical inputs read:

- `docs/specs/ireland_focus_tree/prompts/ireland_focus_tree_asset_prompt.md`
- `docs/specs/ireland_focus_tree/bop_addendum/prompts/ireland_bop_asset_prompt.md`
- `docs/specs/ireland_focus_tree/specs/ireland_focus_tree_spec_part_9_country_package_deltas.md`
- `docs/specs/ireland_focus_tree/research/*.md`
- `docs/specs/ireland_focus_tree/matrices/ireland_focus_tree_asset_matrix.md`
- `docs/specs/ireland_focus_tree/matrices/ireland_focus_tree_event_asset_matrix.md`
- `docs/assets/ireland_focus_tree/manifest.md`
- `docs/assets/ireland_focus_tree/gfx_handoff.md`

Asset workflow references checked:

- `.agents/skills/hoi4-feature-assets/SKILL.md`
- `.agents/skills/hoi4-feature-assets/assets/flags/`
- `.agents/skills/hoi4-feature-assets/assets/news_event_images/`
- `.agents/skills/hoi4-feature-assets/assets/report_event_images/`

## Status Key

- `accepted`: Source status is clear enough for an asset worker to download and process later, subject to normal crop/quality review.
- `needs_user_review`: A plausible source exists, but rights, provenance, identification, sensitivity, or fit needs human review before game use.
- `blocked`: Do not use until a better source or explicit permission is supplied.
- `conditional`: Source only matters if implementation exposes that person/symbol/event visibly.

## Executive Recommendations

- Do not treat vanilla portrait reuse as a complete source handoff unless the vanilla file's provenance is documented elsewhere. If Ireland leaders are visible, attach one of the source records below to the corresponding portrait workflow or replace the portrait from a documented source.
- Preserve the base Irish tricolour. The current `IRE_ALL_ISLAND` tricolour handling is identity-safe if it remains a direct tricolour copy and does not imply a new historical flag. Use official Irish flag sources in the manifest.
- Avoid real Blueshirt, IRA, Labour Party, Conradh na Gaeilge, Red Cross, and Northern symbols in generated icons unless a specific, documented source and use case has been approved.
- For event images, use real sourced photographs only when depicting a real historical scene/person/document. Otherwise use generated period-documentary imagery under `hoi4-feature-assets`, especially for alternate-history route moments.
- Do not use slogans, quotations, Gaelic wording, anthems, songs, or cultural phrases from asset notes. Those remain blocked pending `hoi4-text-audio-research`.

## Real Leader Portrait Source Ledger

| Working use | Person | Status | Recommended source | Author/archive | Date | Rights note | Era/fit note | Uncertainty / action |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| `leader_eamon_de_valera` / `ire_de_valera_leader` | Eamon de Valera | accepted | https://commons.wikimedia.org/wiki/File:%C3%89amon_de_Valera.jpg | National Photo Company collection, Library of Congress | c. 1922-1930 | Commons records no known copyright restrictions / public domain source from LOC | Strong period portrait for 1936 start-era leader after HOI4-style crop | Use this before unsourced vanilla reuse. |
| `leader_douglas_hyde` / `ire_douglas_hyde_president` | Douglas Hyde | accepted | https://commons.wikimedia.org/wiki/File:Douglas_Hyde,_1938_(cropped).jpg | Unknown Irish photographer, Commons source record | 1938 | Commons records Irish anonymous-work public domain status | Excellent presidency-era source for constitutional/presidency surfaces | Verify the file page at download time still carries both source and rights tags. |
| `advisor_sean_lemass` / `ire_sean_lemass_industry` | Sean Lemass | accepted | https://commons.wikimedia.org/wiki/File:Se%C3%A1n_Lemass_circa_1932.png | Unknown/NLI-derived election or political source per Commons | c. 1932 | Commons records anonymous-work public domain status | Period-suitable younger Lemass; better than postwar/1960s images | Use the circa 1932 source rather than the CC0 1966 image for wartime-era fit. |
| `leader_wt_cosgrave` / `ire_wt_cosgrave_opposition` | W. T. Cosgrave | accepted | https://commons.wikimedia.org/wiki/File:W._T._Cosgrave,_circa_1930_(cropped).jpg | Commons source record, cropped from circa 1930 image | c. 1930 | Commons records public domain in US and source-country public domain tags | Good opposition-route era fit | Confirm original file/source link during download. |
| `leader_william_norton` / Labour route | William Norton | accepted | https://commons.wikimedia.org/wiki/File:William_Norton_circa_1927_to_1932.png | Unknown author; NLI catalogue source listed on Commons | c. 1927-1932 | Commons records anonymous-work public domain status | Strong period Labour leader/advisor fit | Prefer this over later 1945 source unless older portrait quality fails crop review. |
| `leader_eoin_oduffy` / Blueshirt route | Eoin O'Duffy | accepted with sensitivity note | https://commons.wikimedia.org/wiki/File:Eoin_O%27Duffy,_circa_1930.jpg or https://commons.wikimedia.org/wiki/File:Eoin_O%27Duffy_1934.jpg | Commons records unknown Irish author/source | c. 1930 or 1934 | Commons records public domain status | Period fit for route leader | Use neutral portrait crop only. Do not use rally/salute imagery as a default leader portrait. |
| `ire_frank_aiken_security_or_defence` | Frank Aiken | accepted | https://commons.wikimedia.org/wiki/File:Frank_Aiken_1944_cropped.jpg | Unknown author, Commons source record | 1944 | Commons records anonymous-work public domain status | Strong Emergency-era fit for defence/security role | Good candidate if Aiken appears as advisor/minister. |
| `advisor_frank_ryan` | Frank Ryan | needs_user_review, conditional | https://commons.wikimedia.org/wiki/File:Frank_Ryan_from_the_International_Brigades,_Zaragoza,_5_April_1938_(28963225728).jpg | National Library of Spain source; modern Flickr colorization by Cassowary Colorizations | Original photo 1938; derivative uploaded 2018 | Commons records CC BY 2.0 for the colorized derivative | Real 1938 prisoner image; historically sensitive and colorized | Use only if Frank Ryan is visibly implemented. Prefer a non-colorized original from BNE/ALBA if available. If using this derivative, attribution is required and B/W processing should remove speculative color. |
| `leader_sean_russell` | Sean Russell | needs_user_review, conditional | https://commons.wikimedia.org/wiki/File:Sean_Russell.jpg | Unknown author; source magazine via NUI Galway digital library | listed as 1938 / magazine published 1942 | Commons records public domain / PDM, but the file page includes jurisdiction notes for anonymous works | Period portrait exists; subject is highly sensitive due IRA/Nazi route context | Use only if implementation visibly uses Russell. Record Nazi-contact context in asset notes; avoid celebratory framing. |
| `leader_stephen_hayes` | Stephen Hayes | blocked, conditional | DIB identity source: https://www.dib.ie/biography/hayes-stephen-a3880 ; NLI document source: https://catalogue.nli.ie/Record/vtls000284997 | DIB/NLI; commercial image hits found elsewhere | n/a | No acceptable public-domain/free portrait source verified in this pass | Identity source exists, portrait source does not | Do not create or use a Hayes portrait unless a documented free/public-domain portrait is found or user supplies one. |
| Northern leader if active Northern tag appears | James Craig | blocked for now | NPG identity/portrait source: https://www.npg.org.uk/collections/search/person/mp53158/james-craig-1st-viscount-craigavon ; Wikipedia file: https://en.wikipedia.org/wiki/File:James_Craig,_1st_Viscount_Craigavon.jpg | Walter Stoneman / National Portrait Gallery | 1917 | Wikipedia states US public domain only and explicitly not Commons-suitable until 2029; NPG page directs licensing | Useful identity source, not a safe reusable asset source now | Do not use the NPG/Wikipedia portrait in mod assets without separate licensing or a better public-domain source. |
| Northern leader if active Northern tag appears | J. M. Andrews | needs_user_review, conditional | https://commons.wikimedia.org/wiki/File:John_Millers_Andrews_(cropped).png | Unknown author, sourced from Creative Centenaries page per Commons | c. 1910s | Commons records US public domain; page carries missing/source-country-status caveat | Usable likeness candidate but not fully clean | If a Northern tag is active, review source-country status before processing. |
| extra prompt candidate | Sean Mac Eoin | accepted, conditional | https://commons.wikimedia.org/wiki/File:Sean_MacEoin.jpg | Unknown author, Commons source record | early 20th c. | Commons records anonymous-work public domain and US public domain status | Good period fit if opposition/military role is used | Not in the required user candidate list, but asset prompt names him. |
| extra prompt candidate | Daniel McKenna | blocked until researched | none accepted in this pass | n/a | n/a | No suitable source verified | n/a | If implementation exposes him, run a dedicated source search. |
| extra prompt candidate | Hugo MacNeill | blocked until researched | none accepted in this pass | n/a | n/a | No suitable source verified | n/a | If implementation exposes him, run a dedicated source search. |

## Flag and Symbol Source Ledger

| Surface | Status | Source(s) checked | Rights / official note | Implementation-safe recommendation |
| --- | --- | --- | --- | --- |
| Base Irish tricolour / `flag_ireland_base` / `IRE_ALL_ISLAND` tricolour copies | accepted | Irish Statute Book Constitution Article 7: https://www.irishstatutebook.ie/en/constitution/index.html ; Department of the Taoiseach flag guidance: https://www.gov.ie/en/department-of-the-taoiseach/publications/the-national-flag/ | Official state/legal sources establish the green-white-orange tricolour and proportions/direction | Preserve base tricolour. Do not add emblems, slogans, seals, or route marks to the no-suffix base flag. |
| All-island civic cosmetic using unchanged tricolour | accepted | Same as base tricolour | Official flag source supports unchanged national flag identity | Current manifest note is safe if it remains a copied tricolour and not a claimed new historical all-island flag. |
| Labour/social republic flag variant | needs_user_review | No safe historical Labour Party flag/logo source accepted in this pass | Modern Labour marks are likely trademark/copyright controlled; historical route flag not verified | Use generated fictional civic/social-republic design only if clearly marked fictional synthesis. Avoid real Labour Party logos, roses, slogans, or readable text. |
| Blueshirt/corporate-state flag variant | needs_user_review | Commons reconstruction: https://commons.wikimedia.org/wiki/File:Flag_of_the_Irish_Blueshirts.svg ; FOTW/CRW source lead: https://www.crwflags.com/fotw/flags/ie%7Dblsh.html ; History Ireland O'Duffy context: https://historyireland.com/eoin-oduffys-blueshirts-and-the-abyssinian-crisis/ | Commons SVG is own-work public domain, but historical reconstruction/source basis needs review; movement is extremist/sensitive | Do not use this as a route flag without explicit approval. Prefer generated fictional corporatist chamber imagery that avoids real movement insignia and fascist salute framing. |
| IRA/revolutionary republican route symbols | needs_user_review | Sean Russell source above; NLI/NUI Galway source lead; Plan Kathleen/Hermann Goertz context from National Archives UK: https://images.nationalarchives.gov.uk/asset/28594/ | Real IRA symbols/logos and modern republican marks are not cleared here | Use generated safehouse, courier, arms-cache, or council imagery. Do not use modern IRA emblems, readable slogans, swastikas, Axis marks, or real badges without a specific source review. |
| Gaelic League / civic-cultural symbols | needs_user_review | NLI Gaelic League/Hyde/MacNeill page: https://www.nli.ie/1916/exhibition/en/content/stagesetters/culture/hyde-macneill/ ; Constitution Article 8: https://theconstitution.ie/articles/8 | Cultural/history source is acceptable, but logos, harp variants, and Gaelic text need separate source/text review | Use Hyde portrait and generated civic-school/archive imagery. Do not use Conradh na Gaeilge logo, Gaelic slogans, or invented Irish text from asset prompts. |
| Presidential/harp/state seal motifs | needs_user_review | Constitution and official state sources checked only for flag/language; no harp/seal asset rights review completed | Irish harp/state emblem use can imply official state authority and may be protected/controlled | Generated icons may use generic harp-like motifs only if not copied from official seals. Exact presidential/state seals need dedicated source review. |
| Red Cross / humanitarian relief symbols | needs_user_review for official event scenes; blocked as decorative icon motif | Irish Red Cross history: https://www.redcross.ie/a-history-of-the-irish-red-cross/ ; Irish Red Cross Society Order 1939: https://www.irishstatutebook.ie/eli/1939/sro/206/made/en/print ; ICRC emblem rules: https://www.icrc.org/en/document/emblems | The Irish Red Cross is historically valid from 1939, but the red cross emblem is legally protected and misuse-sensitive | Do not use a red cross as a generic first-aid/decision icon. For real Irish Red Cross report/news scenes, use only a sourced historical image or an approved depiction where the emblem use is contextual and not decorative branding. |
| Northern Ireland / Ulster banner handling | needs_user_review | No final Northern tag requirement verified in this source-only pass; James Craig/J. M. Andrews sources checked above | Northern flags and symbols are politically sensitive and require source/legal review | If an active Northern tag is implemented, source its flag separately. Do not invent a Northern flag or use modern/provincial/party symbols casually. |
| Atlantic compact emblem | accepted as generated-only direction | Asset prompt/matrix and existing manifest | Fictional faction/conference emblem; no real historical symbol required | Keep generated symbolic treatment. Do not present it as a historical Irish or all-island flag. |

## Real Event Photo and Documentary Source Ledger

| Event/photo family | Status | Sources checked | Era-fit / rights note | Recommendation |
| --- | --- | --- | --- | --- |
| Treaty Ports returned / Cobh-Spike Island / Berehaven / Lough Swilly | source context accepted; photo asset not accepted yet | DIFP Treaty Ports records: https://www.difp.ie/volume-5/1938/transfer-of-treaty-ports/2338/ ; Spike Island handover context: https://www.spikeislandcork.ie/the-handover-of-spike-island-1938/ ; Military Archives coastal defence listing: https://www.militaryarchives.ie/uploads/images/Coastal-Defence-Artillery.pdf | Strong 1938 historical basis; no clearly reusable period photo selected in this pass | For a real-news image, find a clearly licensed 1938 handover photo. Otherwise generate a period-documentary port handover scene and cite DIFP/Spike Island as context only. |
| Coastwatch / Look Out Posts | source context accepted; photo asset needs review | Military Archives Lookout Post Logbooks: https://www.militaryarchives.ie/en/reading-room-collections/lookout-post-logbooks ; RIA coastwatchers article: https://www.ria.ie/blog/the-coastwatchers-irelands-second-world-war-early-warning-system/ ; Geograph modern CC photo lead: https://www.geograph.ie/photo/5876661 | Military Archives confirms 83 LOPs and logbooks; modern photos are not period imagery; Geograph is CC but visually modern | For report images, prefer generated 1939-1945 documentary scene or a licensed period archive image. Do not use modern tourism/ruin photos as wartime event art. |
| G2 intercept / IRA courier / Plan Kathleen-style crisis | source context accepted; photo asset not accepted | National Archives UK Hermann Goertz asset lead: https://images.nationalarchives.gov.uk/asset/28594/ ; Irish Story context: https://www.theirishstory.com/2019/05/13/herman-goertz-a-german-spy-in-wartime-ireland/ ; Sean Russell source above | Real document/person sources exist but route is sensitive and rights are not all clear | Use generated documentary files/radio/map scene unless a specific archival document image is licensed. Avoid Nazi insignia and readable fake text. |
| Labour congress / cooperative industry / cross-border Labour mediation | generated preferred; real photo not accepted | William Norton and Frank Ryan sources above; CWU Norton context source from bibliography: https://www.cwu.ie/conference-centre-and-meeting-rooms/william-norton-1900-1963-an-unsung-trade-union-labour-leader/ | No safe real congress photo selected | Use generated period hall/union-office imagery without official Labour logos or slogans. |
| Blueshirt guard crisis / corporate chamber | generated preferred; real photo needs review | O'Duffy portrait sources above; Blueshirt flag and History Ireland sources above; Commons photo lead: https://commons.wikimedia.org/wiki/File:O%27Duffy_Blue_Shirt_Movement_fascist_salute.jpg | Real rally/salute imagery is public-domain-claimed in some records but glorification/sensitivity risk is high | Use generated symbolic chamber/guard-pressure imagery. If using real rally photos, require explicit user review and critical framing. |
| Northern settlement / unionist alarm / integration commission | generated preferred unless exact sourced photo selected | James Craig/J. M. Andrews/NPG sources above; CAIN/Government of Ireland Act source from bibliography | Northern political imagery is sensitive; Craig portrait source blocked | Use generated observer/commission/public-office imagery unless a clean public-domain photo is found. |
| Irish Red Cross / humanitarian relief flavour events | needs_user_review | Irish Red Cross and ICRC sources above | Historical institution valid from 1939; emblem is protected | Generated humanitarian scenes should avoid using the protected red cross emblem decoratively. If exact Irish Red Cross depiction is needed, source a period image and review emblem use. |
| Civic school / folklore / Gaelic restoration | generated preferred with source context | UCD Schools Collection: https://www.ucd.ie/irishfolklore/en/collections/schoolscollectionduchas/ ; Duchas info: https://www.duchas.ie/en/info/cbe ; UNESCO collection background: https://www.unesco.org/en/memory-world/irish-folklore-commission-collection-1935-1970 | Strong source context, but collection images/text may have reuse conditions | Use generated school/archive imagery unless a specific collection image is licensed. No readable Irish text or folklore quotes without text research. |
| Ardnacrusha / sugar beet / turf / Aer Lingus / Irish Shipping | source context accepted; photo assets not selected | ESB Ardnacrusha PDF/source from bibliography; Ask About Ireland sugar sources; Bord na Mona history; Aer Lingus about page; Oireachtas Irish Shipping report | Historical basis strong; image rights not checked for final reuse | Use generated documentary industry scenes or perform specific archive image licensing checks per event. |

## Existing Asset Package Notes

- `docs/assets/ireland_focus_tree/manifest.md` currently states that real leader portraits are reused from vanilla character assets and that `IRE_ALL_ISLAND` copies vanilla Ireland tricolour flag files. This source handoff does not verify vanilla file provenance because this task forbids vanilla-file inspection.
- The tricolour identity is accepted using official Irish state sources. The actual copied game files should still be documented as implementation assets, not as archival source images.
- Real leader visibility should be mapped to the source ledger above before final completion claims. If the implementation keeps vanilla portraits, add provenance notes tying each visible real person to a verified source, or mark that portrait `needs_user_review`.

## Blocked / Needs-Review Summary

Blocked:

- Stephen Hayes portrait: no free/public-domain portrait verified.
- James Craig portrait: best NPG/Wikipedia image is US-public-domain only and not Commons-suitable until 2029.
- Daniel McKenna and Hugo MacNeill portraits: not verified in this pass.
- Decorative Red Cross emblem use: blocked unless contextual, sourced, and legally reviewed.

Needs user review:

- Frank Ryan portrait: usable-looking 1938 source exists, but the available Commons file is a modern colorized CC BY derivative and the prisoner context is sensitive.
- Sean Russell portrait: plausible public-domain source exists, but the route context and file-page jurisdiction notes require explicit review if he is visible.
- J. M. Andrews portrait: plausible Commons source exists, but source-country rights are not cleanly documented in the visible file page.
- Blueshirt route flag/symbols: available reconstructions are not enough by themselves for historical-flag claims.
- IRA, Labour, Gaelic League, presidential/harp, Northern, and Red Cross official-symbol use.

## Source Files

No source files were downloaded in this pass. The sources above are ready for a later asset-source worker to download only after the corresponding `accepted` or `needs_user_review` status is resolved for the exact implementation surface.
