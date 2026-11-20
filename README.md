# lib-json-handl

`json` — JSON parser/serializer written in handl itself: the pure-`.hnl`
sibling of `lib-json` (the C-backed codec). Pure `.hnl` over the
`data`/`match`/implicit-binder/`IO<sig>` surface.

## Layout

```text
src/        the .hnl sources
pkg.hnl     package manifest — modules, deps, description, license
```

## Gate

```bash
HNL=../host-cli/target/debug/hnl scripts/hnl-gate.sh
```

## License

MIT.
