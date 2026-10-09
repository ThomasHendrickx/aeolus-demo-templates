# aeolus-demo-templates

Squadron templates and blueprints for Tidewater, an invented app with tide tables for small harbours. The [Aeolus](https://github.com/ThomasHendrickx/aeolus-fleet) demo fleet forms its squadron from them.

They come from the example set in aeolus-fleet's [docs/squadrons-example](https://github.com/ThomasHendrickx/aeolus-fleet/tree/main/docs/squadrons-example), with each blueprint's references naming this repository. How templates, blueprints and their version tags work: aeolus-fleet's [docs/squadrons.md](https://github.com/ThomasHendrickx/aeolus-fleet/blob/main/docs/squadrons.md).

| Path | What |
| --- | --- |
| `.aeolus/squadrons/templates/` | The roles: planner, implementer, reviewer, tester |
| `.aeolus/squadrons/blueprints/` | `tidewater-feature` (planner, implementer, reviewer, tester; two implementers up to version 2) and `tidewater-fix` (implementer, tester) |

The demo forms `tidewater-feature@5`. Its templates, version 5, pin real model ids in their `crew.model` (the one place for a model since aeolus-fleet 0.20.3), in a mix a fleet would run: `claude-opus-5-5` for the planner, `claude-sonnet-5-5` for the implementer, `gpt-6.1-sol` (Codex) for the reviewer and `claude-haiku-4-5-20251001` for the tester. Each also says how its members are crewed, in the crew settings of aeolus-fleet 0.20.1 (a `crew` block: the harness that runs its model, an effort and a first prompt), and the planner takes the `area` it plans in as a parameter, which the blueprint fills. No file names a workspace or a machine label, so forming writes no crew requests and the members are crewed from their crew lines. The demo's members are scripted and state the model their template pins, so none shows a model mismatch; its tester hands a passed feature back to the planner, who starts the next one. `tidewater-fix@3` runs its implementer on Codex with `gpt-6.1-sol` and a lower effort, over the template's. Version 4 of the templates, `tidewater-feature@4` and `tidewater-fix@2` give the model outside `crew`, as aeolus-fleet 0.20.1 read it; 0.20.3 refuses them. Version 1 of every file, tagged `<name>@1`, is the example set as it was before crew settings, and `tidewater-fix@1` still uses it.

To use them in your own fleet: in the console, Settings, Repositories, add `https://github.com/ThomasHendrickx/aeolus-demo-templates`.
