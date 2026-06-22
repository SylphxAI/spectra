# Spectra Agent Instructions

## Scope

This file is the repo-local operating policy for agents working in
`SylphxAI/spectra`. Organization-wide engineering doctrine is owned by
`SylphxAI/doctrine`; `PROJECT.md` and `.doctrine/project.json` own this
repository's local identity, lifecycle, boundary, and delivery facts.

Spectra is a Dart package that generates JSON Schema, OpenAPI, and Protocol
Buffers from annotated Dart data classes.

## Read First

1. `PROJECT.md` and `.doctrine/project.json` for project goals, boundaries,
   delivery proof, package-release facts, and adoption gaps.
2. `README.md` for the public API, annotations, generated outputs, and migration
   notes.
3. `pubspec.yaml` before changing package identity, dependencies, SDK
   constraints, or publish behavior.
4. `example/pubspec.yaml` and generated-output examples before changing builder
   behavior.

## Non-Negotiables

- Keep Spectra focused on schema/spec generation from Dart models. Product API
  policy, auth, persistence, and deployment belong in consuming applications.
- Do not publish pub.dev package changes without explicit release proof and
  package registry readback.
- Preserve compatibility expectations for Freezed, json_serializable, plain Dart
  models, JSON Schema, OpenAPI, and Protobuf outputs.
- Do not introduce a second source of truth for generated contracts.

## Validation

Use the narrowest meaningful validation first, then broaden as needed:

- `dart format --set-exit-if-changed .`
- `dart analyze`
- `dart test`
- example build-runner generation for output-affecting changes

Docs-only boundary changes may be validated by diff review, referenced-file
checks, and the central project manifest audit.
