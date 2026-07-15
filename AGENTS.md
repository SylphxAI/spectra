# spectra — local agent notes only

Doctrine and fleet delivery law live in the **host always-on constitution**
(`~/.grok/AGENTS.md` / Doctrine template). This file must **not** restate,
weaken, or fork that law (including PR-vs-direct-trunk delivery).

Local truth: `PROJECT.md`, `.doctrine/project.json` when present.

## Boundary hazards

- Keep Spectra focused on schema/spec generation from Dart models. Product API
- Do not publish pub.dev package changes without explicit release proof and
- Preserve compatibility expectations for Freezed, json_serializable, plain Dart
- Do not introduce a second source of truth for generated contracts.

## Local commands

- `dart format --set-exit-if-changed .`
- `dart analyze`
- `dart test`
- example build-runner generation for output-affecting changes
- Prefer the **narrowest** affected check before full workspace runs.
- Report layers honestly: local diff · trunk FF · deploy · prod proof (do not collapse).

## Validation notes

- Prefer the **narrowest** affected check before full workspace runs.
- Report layers honestly: local diff · trunk FF · deploy · prod proof (do not collapse).
