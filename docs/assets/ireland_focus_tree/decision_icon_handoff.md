# Ireland Decision Icon Handoff

## Scope

This handoff covers only the Ireland decision icons and decision category icons registered in `interface/ireland_focus_tree.gfx`.

No gameplay, localisation, focus, idea, achievement, animation, flag, or `.gfx` files were edited for this asset pass.

## Source Mode

Source mode: generated artwork via Codex `imagegen`, processed locally for HOI4 decision icon use.

The generated artwork was produced as five chroma-key source atlases with painted object icons on a flat green background, then cropped into per-icon source PNGs. The generated sources avoid text, leader portraits, slogans, charts, and simple shape placeholders.

Generated atlas source files:

- `docs/assets/ireland_focus_tree/source_png/ireland_decision_category_atlas_source.png`
- `docs/assets/ireland_focus_tree/source_png/ireland_decision_authority_atlas_source.png`
- `docs/assets/ireland_focus_tree/source_png/ireland_decision_security_atlas_source.png`
- `docs/assets/ireland_focus_tree/source_png/ireland_decision_economy_integration_atlas_source.png`
- `docs/assets/ireland_focus_tree/source_png/ireland_decision_diplomacy_atlas_source.png`

Per-icon source crops were saved under:

- `docs/assets/ireland_focus_tree/source_png/decision_category_ireland_*_source.png`
- `docs/assets/ireland_focus_tree/source_png/decision_ireland_*_source.png`

## Processed Outputs

Processed transparent PNG previews:

- `docs/assets/ireland_focus_tree/processed_png/decision_category_ireland_*.png`
- `docs/assets/ireland_focus_tree/processed_png/decision_ireland_*.png`

Final DDS outputs use the already registered texture paths:

- `gfx/interface/decisions/categories/decision_category_ireland_*.dds`
- `gfx/interface/decisions/decision_ireland_*.dds`

Counts:

- Decision category icons: 8 processed PNGs and 8 DDS files at 64x64.
- Decision icons: 58 processed PNGs and 58 DDS files at 32x32.
- Total decision/category icon package: 66 source crops, 66 processed PNGs, 66 DDS files.

Review assets:

- Contact sheet: `docs/assets/ireland_focus_tree/processed_png/ireland_decision_icons_contact_sheet.png`
- Manifest TSV: `docs/assets/ireland_focus_tree/processed_png/ireland_decision_icon_manifest.tsv`

## Registered Path Note

The parent prompt listed category paths in the form `gfx/interface/decisions/categories/ireland_authority.dds`. The actual registered paths in `interface/ireland_focus_tree.gfx` use `decision_category_ireland_*.dds`, for example:

- `gfx/interface/decisions/categories/decision_category_ireland_authority.dds`

This pass preserved the current registered paths and sprite names exactly, so the replacement art lands where the existing `.gfx` file already points.

## Validation

Validation was run against the actual registered `GFX_decision_ireland_*` and `GFX_decision_category_ireland_*` sprite texture paths extracted from `interface/ireland_focus_tree.gfx`.

Result:

- Registered entries checked: 66.
- Decision icons checked: 58.
- Decision category icons checked: 8.
- Missing DDS files: 0.
- Unreadable DDS files: 0.
- Dimension failures: 0.
- DDS alpha format failures: 0.
- Useful alpha failures: 0.

No blocker remains in the decision/category icon lane.
