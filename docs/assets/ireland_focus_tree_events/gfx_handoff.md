# Ireland Focus Tree Major Event Art GFX Handoff

Asset subagent handoff only. Do not treat this as a `.gfx` edit.

Suggested target `.gfx` file: `interface/ireland_focus_tree.gfx`, or the existing event-picture registry if the main implementation has already created one.

Ready-to-copy pattern:

```txt
spriteType = {
	name = "GFX_news_ireland_ports_return"
	texturefile = "gfx/event_pictures/ireland_focus_tree/news_ireland_ports_return.dds"
}
```

| Proposed sprite | Final DDS | Intended event family | Size |
| --- | --- | --- | --- |
| `GFX_news_ireland_ports_return` | `gfx/event_pictures/ireland_focus_tree/news_ireland_ports_return.dds` | ports return / port defence public event | 397x153 |
| `GFX_report_ireland_coastwatch` | `gfx/event_pictures/ireland_focus_tree/report_ireland_coastwatch.dds` | coastwatch / LOP Emergency reports | 210x176 |
| `GFX_report_ireland_g2_intercept` | `gfx/event_pictures/ireland_focus_tree/report_ireland_g2_intercept.dds` | G2 intercept / counter-espionage reports | 210x176 |
| `GFX_news_ireland_commonwealth_liaison` | `gfx/event_pictures/ireland_focus_tree/news_ireland_commonwealth_liaison.dds` | Commonwealth liaison / guarded cooperation news | 397x153 |
| `GFX_news_ireland_labour_congress` | `gfx/event_pictures/ireland_focus_tree/news_ireland_labour_congress.dds` | Labour congress / democratic labour route news | 397x153 |
| `GFX_news_ireland_corporate_chambers` | `gfx/event_pictures/ireland_focus_tree/news_ireland_corporate_chambers.dds` | corporate chambers route news | 397x153 |
| `GFX_report_ireland_safehouse_network` | `gfx/event_pictures/ireland_focus_tree/report_ireland_safehouse_network.dds` | safehouse network / courier exposure reports | 210x176 |
| `GFX_news_ireland_northern_settlement` | `gfx/event_pictures/ireland_focus_tree/news_ireland_northern_settlement.dds` | Northern settlement public news | 397x153 |
| `GFX_report_ireland_integration_commission` | `gfx/event_pictures/ireland_focus_tree/report_ireland_integration_commission.dds` | post-settlement integration commission reports | 210x176 |
| `GFX_news_ireland_unified_identity` | `gfx/event_pictures/ireland_focus_tree/news_ireland_unified_identity.dds` | verified all-island civic identity news | 397x153 |
| `GFX_news_ireland_atlantic_compact` | `gfx/event_pictures/ireland_focus_tree/news_ireland_atlantic_compact.dds` | Atlantic neutral compact conference news | 397x153 |
| `GFX_report_ireland_emergency_directorate` | `gfx/event_pictures/ireland_focus_tree/report_ireland_emergency_directorate.dds` | Emergency Directorate hidden-route reports | 210x176 |
| `GFX_report_ireland_civic_cultural_route` | `gfx/event_pictures/ireland_focus_tree/report_ireland_civic_cultural_route.dds` | civic cultural restoration reports | 210x176 |
| `GFX_report_ireland_bop_warning_authority` | `gfx/event_pictures/ireland_focus_tree/report_ireland_bop_warning_authority.dds` | BOP authority warning event surface | 210x176 |

Use notes:

- News images are final black-and-white 397x153 DDS files.
- Report images are final 210x176 DDS files with transparent report-card corners.
- All sources are generated period-documentary scenes and should be wired as final art, not placeholders.
- No `.gfx`, gameplay, localisation, focus, decision, or spec files were edited by this asset pass.
