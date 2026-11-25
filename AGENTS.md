# lib-json-handl

`json` — JSON parser/serializer written in handl itself: the
pure-`.hnl` sibling of `lib-json` (the C/native codec). Pure `.hnl`
over the `data`/`match`/implicit-binder/`IO<sig>` surface.

## Layout

| path | role |
| --- | --- |
| `src/json.hnl` | the parser/serializer |
| `pkg.hnl` | manifest — `modules: ["json"]` |
| `scripts/hnl-gate.sh` | `.hnl` gate |
| `workflows/gate.yaml` | CI — shared `handl-gates` campaign |

## Contract

- Same `json` module name/surface as `lib-json` but pure handl — pick
  this when no native codec is available; keep parse/stringify
  semantics aligned with `lib-json` (lenient parse).
- No Rust crate.

## Verification

```bash
HNL=../host-cli/target/debug/hnl scripts/hnl-gate.sh
```

<!-- myco:agent-awareness -->

## Agent awareness

- Session start / any work discussion: run `myco status --prompt`
  before proposing next steps — know the board first.
- User describes new work → offer to capture it (`myco todo add`,
  `issue new`, `proposal new`). Don't wait to be asked.
- Picking up a task: `myco resume <ID>` is the briefing.
- Wrapping up: `myco handoff <ID>` anything resumable; keep statuses
  honest (claimed → in-progress → blocked/done).

<!-- /myco:agent-awareness -->
