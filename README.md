# aeolus-demo-templates

Squadron templates and blueprints for Tidewater, an invented app with tide tables for small harbours. The [Aeolus](https://github.com/ThomasHendrickx/aeolus-fleet) demo fleet forms its squadron from them.

They come from the example set in aeolus-fleet's [docs/squadrons-example](https://github.com/ThomasHendrickx/aeolus-fleet/tree/main/docs/squadrons-example), with each blueprint's references naming this repository. How templates, blueprints and their version tags work: aeolus-fleet's [docs/squadrons.md](https://github.com/ThomasHendrickx/aeolus-fleet/blob/main/docs/squadrons.md).

| Path | What |
| --- | --- |
| `.aeolus/squadrons/templates/` | The roles: planner, implementer, reviewer, tester |
| `.aeolus/squadrons/blueprints/` | `tidewater-feature` (planner, two implementers, reviewer, tester) and `tidewater-fix` (implementer, tester) |

The demo forms `tidewater-feature@2`. Its templates, version 2, pin `aeolus-demo-script-1`, the model the demo's scripted members state, so none shows a model mismatch; its tester hands a passed feature back to the planner, who starts the next one. Version 1 of every file, tagged `<name>@1`, is the example set as it is, and `tidewater-fix@1` still uses it.

To use them in your own fleet: in the console, Settings, Repositories, add `https://github.com/ThomasHendrickx/aeolus-demo-templates`.
