# Ireland BOP asset prompt

Use this prompt with `hoi4-feature-assets` and the correct asset subagents.

Feature slug: `ireland_focus_tree_bop`

Parent feature: `ireland_focus_tree`

Goal: create final visual assets for the Ireland BOP addendum. The canonical Ireland focus tree is already implemented. These assets support the new BOP surface, route warning states, BOP achievements, and optional warning animation.

Read:

- `matrices/ireland_bop_asset_matrix.md`
- `hoi4-feature-assets`
- `hoi4-frame-animation` if producing animated warning sprites

Reference folders to inspect before asset work:

- `.agents/skills/hoi4-feature-assets/assets/ideas`
- `.agents/skills/hoi4-feature-assets/assets/decisions`
- `.agents/skills/hoi4-feature-assets/assets/achievements`
- `.agents/skills/hoi4-feature-assets/assets/focuses`
- `.agents/skills/hoi4-feature-assets/assets/flags` if any flag or official symbol is requested

Asset families:

1. BOP side icons for all active side ids.
2. BOP crisis warning static icon.
3. Optional BOP crisis warning animated sprite with static fallback.
4. Achievement icons for BOP achievements.
5. Decision icons for BOP decision families if the existing decision category does not already provide suitable icons.

Source mode rules:

- Use generated symbolic icon art for ordinary BOP side icons.
- Use sourced asset work for real historical flags, real state symbols, real party symbols, real paramilitary insignia, real leader portraits, or attested movement symbols.
- Do not generate real people.
- Do not use real IRA or Blueshirt symbols unless sourced and documented.
- Do not put readable text, slogans, mottoes, or generated labels inside icons.
- Achievement icons need completed, grey, and not eligible variants if the repository achievement system requires them.
- Animated warning sprites must follow frame animation rules, with real source frames, static fallback, frame sheet, preview GIF for review only, manifest, and GFX handoff.

Suggested final folders:

- `gfx/interface/bop/ireland_focus_tree_bop/`
- `gfx/interface/decisions/ireland_focus_tree_bop/` if new decision icons are produced
- `gfx/achievements/` for achievement DDS files, following root achievement placement rules
- `docs/assets/ireland_focus_tree_bop/` for source, processed previews, manifest, handoff, contact sheets, and animation notes

Required outputs:

- source PNG for every asset
- processed PNG preview
- final DDS in the proper game folder
- manifest entry
- `gfx_handoff.md`
- contact sheet for side icons and achievements
- source or generated status for every asset
- blocker notes for any historical asset whose source is unclear

Do not edit gameplay files or localisation files from the asset task unless the parent explicitly expands scope.
