# Ireland Focus Icon Handoff

Scope: focus-icon lane only for the Slop Redux Ireland focus tree.

No gameplay, localisation, achievement, idea, decision, animation, GUI, or `.gfx` files were edited. Existing sprite registrations were read from `interface/ireland_focus_tree.gfx` and preserved.

## Output Summary

- Source inputs: `docs/assets/ireland_focus_tree/source_png/goal_ireland_<token>_source.png`
- Processed PNG outputs: `docs/assets/ireland_focus_tree/processed_png/goal_ireland_<token>.png`
- Final DDS outputs: `gfx/interface/goals/goal_ireland_<token>.dds`
- Final contact sheet: `docs/assets/ireland_focus_tree/focus_icons_contact_sheet.png`
- Checker-background transparency review sheet: `docs/assets/ireland_focus_tree/focus_icons_checker_contact_sheet.png`
- Source review contact sheet: `docs/assets/ireland_focus_tree/focus_source_review_contact_sheet.png`
- Reference review contact sheet: `docs/assets/ireland_focus_tree/focus_reference_contact_sheet.png`

## Size And Alpha

Final dimensions are `96x96` for both processed PNG and DDS outputs. The generic focus-icon target in the asset skill is `94x86`, but the already-registered Ireland focus icon files and existing sprite assets in this package are `96x96`; this pass preserves that established repository pattern for the registered texture paths.

All final PNG and DDS files are `RGBA` with real alpha. Alpha validation result for every icon: `(0, 255)`. The source magenta matte was removed and unused pixels are transparent.

## Focus Icons

| Token | Sprite | Source PNG | Processed PNG | Final DDS | Dimensions | Alpha |
|---|---|---|---|---|---|---|
| `opening` | `GFX_goal_ireland_opening` | `docs/assets/ireland_focus_tree/source_png/goal_ireland_opening_source.png` | `docs/assets/ireland_focus_tree/processed_png/goal_ireland_opening.png` | `gfx/interface/goals/goal_ireland_opening.dds` | `96x96` | transparent RGBA |
| `authority` | `GFX_goal_ireland_authority` | `docs/assets/ireland_focus_tree/source_png/goal_ireland_authority_source.png` | `docs/assets/ireland_focus_tree/processed_png/goal_ireland_authority.png` | `gfx/interface/goals/goal_ireland_authority.dds` | `96x96` | transparent RGBA |
| `constitutional` | `GFX_goal_ireland_constitutional` | `docs/assets/ireland_focus_tree/source_png/goal_ireland_constitutional_source.png` | `docs/assets/ireland_focus_tree/processed_png/goal_ireland_constitutional.png` | `gfx/interface/goals/goal_ireland_constitutional.dds` | `96x96` | transparent RGBA |
| `neutrality` | `GFX_goal_ireland_neutrality` | `docs/assets/ireland_focus_tree/source_png/goal_ireland_neutrality_source.png` | `docs/assets/ireland_focus_tree/processed_png/goal_ireland_neutrality.png` | `gfx/interface/goals/goal_ireland_neutrality.dds` | `96x96` | transparent RGBA |
| `labour` | `GFX_goal_ireland_labour` | `docs/assets/ireland_focus_tree/source_png/goal_ireland_labour_source.png` | `docs/assets/ireland_focus_tree/processed_png/goal_ireland_labour.png` | `gfx/interface/goals/goal_ireland_labour.dds` | `96x96` | transparent RGBA |
| `blueshirt` | `GFX_goal_ireland_blueshirt` | `docs/assets/ireland_focus_tree/source_png/goal_ireland_blueshirt_source.png` | `docs/assets/ireland_focus_tree/processed_png/goal_ireland_blueshirt.png` | `gfx/interface/goals/goal_ireland_blueshirt.dds` | `96x96` | transparent RGBA |
| `ira` | `GFX_goal_ireland_ira` | `docs/assets/ireland_focus_tree/source_png/goal_ireland_ira_source.png` | `docs/assets/ireland_focus_tree/processed_png/goal_ireland_ira.png` | `gfx/interface/goals/goal_ireland_ira.dds` | `96x96` | transparent RGBA |
| `industry` | `GFX_goal_ireland_industry` | `docs/assets/ireland_focus_tree/source_png/goal_ireland_industry_source.png` | `docs/assets/ireland_focus_tree/processed_png/goal_ireland_industry.png` | `gfx/interface/goals/goal_ireland_industry.dds` | `96x96` | transparent RGBA |
| `military` | `GFX_goal_ireland_military` | `docs/assets/ireland_focus_tree/source_png/goal_ireland_military_source.png` | `docs/assets/ireland_focus_tree/processed_png/goal_ireland_military.png` | `gfx/interface/goals/goal_ireland_military.dds` | `96x96` | transparent RGBA |
| `ports` | `GFX_goal_ireland_ports` | `docs/assets/ireland_focus_tree/source_png/goal_ireland_ports_source.png` | `docs/assets/ireland_focus_tree/processed_png/goal_ireland_ports.png` | `gfx/interface/goals/goal_ireland_ports.dds` | `96x96` | transparent RGBA |
| `emergency` | `GFX_goal_ireland_emergency` | `docs/assets/ireland_focus_tree/source_png/goal_ireland_emergency_source.png` | `docs/assets/ireland_focus_tree/processed_png/goal_ireland_emergency.png` | `gfx/interface/goals/goal_ireland_emergency.dds` | `96x96` | transparent RGBA |
| `diplomacy` | `GFX_goal_ireland_diplomacy` | `docs/assets/ireland_focus_tree/source_png/goal_ireland_diplomacy_source.png` | `docs/assets/ireland_focus_tree/processed_png/goal_ireland_diplomacy.png` | `gfx/interface/goals/goal_ireland_diplomacy.dds` | `96x96` | transparent RGBA |
| `foreign_access` | `GFX_goal_ireland_foreign_access` | `docs/assets/ireland_focus_tree/source_png/goal_ireland_foreign_access_source.png` | `docs/assets/ireland_focus_tree/processed_png/goal_ireland_foreign_access.png` | `gfx/interface/goals/goal_ireland_foreign_access.dds` | `96x96` | transparent RGBA |
| `partition` | `GFX_goal_ireland_partition` | `docs/assets/ireland_focus_tree/source_png/goal_ireland_partition_source.png` | `docs/assets/ireland_focus_tree/processed_png/goal_ireland_partition.png` | `gfx/interface/goals/goal_ireland_partition.dds` | `96x96` | transparent RGBA |
| `late` | `GFX_goal_ireland_late` | `docs/assets/ireland_focus_tree/source_png/goal_ireland_late_source.png` | `docs/assets/ireland_focus_tree/processed_png/goal_ireland_late.png` | `gfx/interface/goals/goal_ireland_late.dds` | `96x96` | transparent RGBA |
| `route_choice` | `GFX_goal_ireland_route_choice` | `docs/assets/ireland_focus_tree/source_png/goal_ireland_route_choice_source.png` | `docs/assets/ireland_focus_tree/processed_png/goal_ireland_route_choice.png` | `gfx/interface/goals/goal_ireland_route_choice.dds` | `96x96` | transparent RGBA |
| `support_lanes` | `GFX_goal_ireland_support_lanes` | `docs/assets/ireland_focus_tree/source_png/goal_ireland_support_lanes_source.png` | `docs/assets/ireland_focus_tree/processed_png/goal_ireland_support_lanes.png` | `gfx/interface/goals/goal_ireland_support_lanes.dds` | `96x96` | transparent RGBA |
| `hidden_civic` | `GFX_goal_ireland_hidden_civic` | `docs/assets/ireland_focus_tree/source_png/goal_ireland_hidden_civic_source.png` | `docs/assets/ireland_focus_tree/processed_png/goal_ireland_hidden_civic.png` | `gfx/interface/goals/goal_ireland_hidden_civic.dds` | `96x96` | transparent RGBA |
| `hidden_directorate` | `GFX_goal_ireland_hidden_directorate` | `docs/assets/ireland_focus_tree/source_png/goal_ireland_hidden_directorate_source.png` | `docs/assets/ireland_focus_tree/processed_png/goal_ireland_hidden_directorate.png` | `gfx/interface/goals/goal_ireland_hidden_directorate.dds` | `96x96` | transparent RGBA |
| `hidden_atlantic` | `GFX_goal_ireland_hidden_atlantic` | `docs/assets/ireland_focus_tree/source_png/goal_ireland_hidden_atlantic_source.png` | `docs/assets/ireland_focus_tree/processed_png/goal_ireland_hidden_atlantic.png` | `gfx/interface/goals/goal_ireland_hidden_atlantic.dds` | `96x96` | transparent RGBA |
| `hidden_common` | `GFX_goal_ireland_hidden_common` | `docs/assets/ireland_focus_tree/source_png/goal_ireland_hidden_common_source.png` | `docs/assets/ireland_focus_tree/processed_png/goal_ireland_hidden_common.png` | `gfx/interface/goals/goal_ireland_hidden_common.dds` | `96x96` | transparent RGBA |

## Reference And Source Review

Reference folder inspected before processing: `.agents/skills/hoi4-feature-assets/assets/focuses`.

The new source PNGs are detailed painted/iconic focus-style subjects with wreaths, symbols, and aged texture. No source was a simple shape, flat geometric diagram, placeholder silhouette, text badge, or recolored icon. No source was blocked.

Weak inputs: none. The source files used a solid magenta matte rather than alpha; this was handled as cleanup by keyed matte removal and alpha validation.

Simplification or fallback used: none.

## Processing Notes

Processing used the new generated source files exactly as named by the parent prompt. The script keyed the saturated magenta matte, preserved the painted subjects, centered each icon inside the existing `96x96` focus sprite canvas, wrote processed PNG previews, and converted those PNGs to DDS through Pillow's DDS encoder. The resulting DDS files match the existing package DDS size/header pattern (`36992` bytes each).

## Validation Results

Validation command form:

```text
python -  # parsed interface/ireland_focus_tree.gfx, opened each processed PNG and registered DDS, checked dimensions, alpha ranges, file existence, readability, and visible matte pixels
```

Results:

- Registered focus sprites found in `interface/ireland_focus_tree.gfx`: `21`
- Missing registered focus tokens: `0`
- Missing or unreadable PNG/DDS files: `0`
- Processed PNG dimensions: all `96x96`
- DDS dimensions: all `96x96`
- PNG alpha ranges: all `(0, 255)`
- DDS alpha ranges: all `(0, 255)`
- Visible magenta matte pixels after cleanup: `0`
- Visual contact-sheet review: all final focus icons are detailed painted/iconic assets, not simple shapes or text badges.
