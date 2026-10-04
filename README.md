# aeolus-demo-templates

Squadron templates and blueprints for Tidewater, an invented app with tide tables for small harbours. The [Aeolus](https://github.com/ThomasHendrickx/aeolus-fleet) demo fleet forms its squadron from them.

They are the example set from aeolus-fleet's [docs/squadrons-example](https://github.com/ThomasHendrickx/aeolus-fleet/tree/main/docs/squadrons-example), with each blueprint's references naming this repository. How templates, blueprints and their version tags work: aeolus-fleet's [docs/squadrons.md](https://github.com/ThomasHendrickx/aeolus-fleet/blob/main/docs/squadrons.md).

| Path | What |
| --- | --- |
| `.aeolus/squadrons/templates/` | The roles: planner, implementer, reviewer, tester |
| `.aeolus/squadrons/blueprints/` | `tidewater-feature` (planner, two implementers, reviewer, tester) and `tidewater-fix` (implementer, tester) |

Every file is version 1, tagged `<name>@1`.

To use them in your own fleet: in the console, Settings, Repositories, add `https://github.com/ThomasHendrickx/aeolus-demo-templates`.
