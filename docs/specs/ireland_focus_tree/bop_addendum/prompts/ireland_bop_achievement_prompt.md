# Ireland BOP achievement prompt

Implement BOP achievements as a post implementation addendum if the repository achievement system is active.

Read:

- `matrices/ireland_bop_achievement_matrix.md`
- `prompts/ireland_bop_asset_prompt.md`
- existing Slop Redux achievement registry and localisation patterns
- `hoi4-feature-assets` for icon requirements

Achievement rules:

- Working labels are not final achievement titles.
- Write final achievement localisation from design direction only.
- Do not use unresearched slogans, quotes, or cultural remarks.
- Every achievement needs clear unlock conditions, disqualifiers, tracking flags or variables where needed, icon direction, and route connection.
- BOP achievements should reward mastery of the new mechanic, not normal route completion alone.
- Track BOP extreme disqualifiers during the run if final state checks cannot prove the condition.

Planned achievements:

- `ireland_bop_constitutional_mastery`
- `ireland_bop_thread_the_emergency`
- `ireland_bop_bargain_without_bases`
- `ireland_bop_congress_without_clientage`
- `ireland_bop_guard_on_a_leash`
- `ireland_bop_front_over_council`
- `ireland_bop_restore_civilian_rule`
- `ireland_bop_civic_revival_no_capture`

Required implementation handoff:

- achievement ids
- localisation keys
- icon DDS paths and variants
- tracking flags or variables
- disqualifier logic
- validation notes
- any achievement deferred with reason
