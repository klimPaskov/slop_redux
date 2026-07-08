# Ireland focus tree text and audio research prompt

Feature slug: `ireland_focus_tree`
Feature name: Ireland comprehensive national focus tree

This prompt is for `hoi4-text-audio-research` and the quote, remark, and audio research subagents. It is not a localisation file. Do not treat any working label as a final title, slogan, decision name, option text, focus title, achievement title, quote, cultural remark, or audio choice.

## Research gate rules

Unresearched wording is blocked. Do not invent quotes, slogans, song fragments, literary allusions, cultural remarks, mottoes, or final audio selections. Verify exact wording, attribution, source, license, and copyright risk. Mark unclear material as blocked or unsuitable.

Prefer official archives, primary sources, Dictionary of Irish Biography, Documents on Irish Foreign Policy, Military Archives, official presidential profiles, reputable historical journals, libraries, museums, and academic sources. Avoid unsourced quote sites.

## Surfaces that may need research

Research is only justified for major presentation moments. Ordinary focus and decision localisation should be written by the implementation agent from the spec direction and does not need quotes or audio.

| Package working label | Trigger or use | Needed research | Tone direction | Notes |
| --- | --- | --- | --- | --- |
| `constitution_sovereignty_package` | 1937 constitution milestone or president office reveal | source check for constitutional wording references and possible short public source excerpt if legally safe | sober state building and legal sovereignty | Use Irish Statute Book and official constitutional sources. Do not quote long legal text. |
| `ports_return_package` | Treaty Ports return event or report image | source review for official transfer records and period phrasing | strategic relief and sovereignty regained through negotiation | Documents on Irish Foreign Policy should be primary. |
| `emergency_watch_package` | coast watching or Emergency board reveal | source review for Coastwatching Service and Look Out Post terminology | watchful, practical, coastal defence | Military Archives and scholarly source review. |
| `neutrality_crisis_package` | strict neutrality under pressure, major incident | quote or remark research only if implementation uses event | restrained and tense, not celebratory | Avoid modern debates unless directly relevant to historical note. |
| `labour_social_republic_package` | Labour capstone, worker congress, anti fascist branch | Labour, trade union, Connolly memory, Frank Ryan, International Brigades source checks | democratic socialist or anti fascist, depending route | Do not invent slogans. Avoid lyrics unless tiny and source checked. |
| `blueshirt_corporatist_package` | Blueshirt route reveal or corporate state capstone | O'Duffy, Blueshirts, Catholic corporatism, Spain and Italy source checks | authoritarian, self justifying, and uneasy | Research must avoid glorifying fascist imagery or copy. |
| `ira_underground_package` | IRA takeover, foreign courier, Plan Kathleen exposure | IRA S-Plan and Plan Kathleen source checks | dangerous, exposed, clandestine, unstable | Treat German contact as risk. Do not frame as clean victory. |
| `all_island_settlement_package` | peaceful unified Ireland formation | source check for all island settlement references and public legal language | constitutional, reconciliatory, high stakes | No final proclamation until researched. |
| `violent_northern_crisis_package` | uprising, ultimatum, or war route if eventized | source checks for period language and caution notes | severe, coercive, unstable | Do not use cheap humour or triumphant slogans. |
| `atlantic_compact_package` | rare neutral conference or compact | source review for Irish neutrality, small state diplomacy, postwar conference language | careful, legalistic, maritime | Audio only if implementation makes this a major reveal. |
| `cultural_epilogue_package` | rare peaceful cultural restoration epilogue | Gaelic League, Douglas Hyde, language revival source checks | ceremonial, cultural, civic | No high kingship fantasy, no occult content. |
| `achievement_reference_package` | achievement title and description direction | title like references only after source and copyright checks | route specific and clever but not flippant | Working achievement labels are not final titles. |

## Audio research scope

Audio is optional. Research audio only for major presentation surfaces that the implementation confirms will use audio.

Potential audio roles:

- Major all island settlement reveal.
- Emergency board reveal if custom GUI needs a short cue.
- Rare Atlantic compact conference reveal.
- Route capstone for Labour, Blueshirt, or IRA only if implementation treats it as a major event.

Audio requirements:

- Public domain or clearly licensed recording.
- Composition and recording rights checked separately.
- Final `.ogg` conversion only if source and license are usable.
- No generated test tones, oscillator beds, or placeholder music.
- No modern copyrighted songs unless a very short researched allusion is used in text and no audio is copied.

## Candidate research questions

- What period sources best support the public meaning of the 1937 constitution and the first presidency?
- What official records best describe the 1938 agreements and port transfer?
- What terminology did Ireland use for the Emergency, the Defence Forces, the Coastwatching Service, and Look Out Posts?
- Which Irish Labour and trade union figures can be used safely and historically in the 1930s context?
- How should Frank Ryan and International Brigade memory be handled without making Labour only a Soviet route?
- Which Blueshirt and O'Duffy sources can support route presentation without copying extremist slogans or glorifying fascism?
- What sources best describe the S-Plan, Plan Kathleen, Seán Russell, Stephen Hayes, and Hermann Goertz?
- What cultural language revival sources around Douglas Hyde and the Gaelic League can support a peaceful cultural epilogue?

## Research output required

Create a research note with:

- considered quote candidates and reasons accepted or rejected
- selected quote only when source and confidence are good
- considered cultural remark or allusion candidates
- selected cultural remark only when source and copyright risk are acceptable
- audio candidates if audio is in scope
- license and public domain notes
- source URLs or repository source paths
- confidence and uncertainty notes
- implementation handoff that states which material is safe, blocked, or needs user review

## Blocked wording reminder

The implementation agent must not convert research directions, role labels, working focus labels, asset names, achievement working labels, or rough package labels into final localisation. Final text requires source work for source dependent material and normal localisation writing for ordinary focus and decision text.

## Canonical hidden path research addendum

Hidden paths are now mandatory planned content. Research the following only when implementation creates a major reveal, final achievement text, event, report, news item, or audio cue.

| Package working label | Trigger or use | Needed research | Notes |
| --- | --- | --- | --- |
| `hidden_civic_cultural_restoration_package` | civic cultural restoration reveal or capstone | Article 8 language status, Douglas Hyde, Gaelic League, non political and non sectarian cultural work, Gaeltacht policy | no final Gaelic wording without source checks |
| `common_platform_settlement_package` | common platform Northern settlement variant | cross community cultural history, observer backed settlement language, minority guarantee language | avoid sectarian or triumphalist wording |
| `emergency_directorate_package` | emergency directorate crisis reveal | Emergency institutions, G2, LDF, coast watch, public order language | present as survival tradeoff, not clean power |
| `atlantic_neutral_compact_package` | compact conference or faction reveal | Irish neutrality, small state diplomacy, neutral shipping, conference language | audio only if major reveal exists |

Any Gaelic slogan, motto, poem, song fragment, prayer, legal phrase, or cultural allusion is blocked until researched and documented.

## Canonical consolidated hidden path research addendum

Research gates now cover every hidden path from Part 10. Do not write final Gaelic wording, slogans, quotes, cultural remarks, movement phrases, achievement titles, or audio choices without source verification.

Required hidden path research questions:

- What safe source checked language can support civic cultural restoration without turning it into mythology or forced cultural policy?
- What Emergency powers, censorship, LDF, G2, and coast watch sources can support Emergency directorate text direction?
- What source checked material is safe for Aiséirghe inspired rare radicalisation without turning extremist rhetoric into celebratory flavour?
- What source basis can support compromised republican network wording around courier exposure and foreign dependency?
- What Labour, trade union, anti fascist, and democratic defence sources can support cross border Labour Council wording without Soviet dependency?
- What neutral diplomacy and small state language can support the Atlantic compact as a conference or faction concept?
- What rights, autonomy, observer, and policing language can support common platform settlement and Northern emergency protectorate text direction?

Any unclear attribution, symbol, slogan, movement phrase, song, poem, or audio license remains blocked.
