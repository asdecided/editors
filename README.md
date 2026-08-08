# AsDecided Editors

[Product site](https://asdecided.com/) · [Ecosystem documentation](https://asdecided.com/docs/ecosystem/) · [Canonical sources](https://asdecided.com/sources)

IDE / editor integrations for [AsDecided](https://github.com/asdecided/core)
(requirements-as-code) — one subdir per client. Per ADR-092 (one repo per
concern, subdir per member) this is the single home for the editor clients;
future editors (for example `jetbrains/`) land as sibling subdirs.

The repository is [`asdecided/editors`](https://github.com/asdecided/editors).
Published extension identities remain unchanged until their own explicit
release cutovers.

## Members

| Subdir | Client |
| --- | --- |
| [`vscode/`](vscode/) | VS Code / Cursor extension ("Lore for VS Code") |

## History

`vscode/` is the former **`itsthelore/lore-vscode`** repository, moved here with
its history preserved (ADR-092 convergence). The Marketplace / OpenVSX listing
identity and the published extension id are unchanged, so installed users are
unaffected — only the source repository moves. The extension consumes the
published `@itsthelore/rac-sdk` from
[`asdecided/sdk`](https://github.com/asdecided/sdk) and the public CLI, never
engine internals (ADR-063). Its migration from the legacy `rac` command to the
native `decided` API is separate release work.
