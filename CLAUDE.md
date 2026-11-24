# CLAUDE.md

## Project
First-person, solo-developed game about restoring a wasteland: short expeditions, scrap maceration, automation lines, and visible regrowth of nature. Stylised (not photoreal) but the scenery must be beautiful. Co-op is planned for later.

Design context lives in `docs/` (game bible, decisions log, open questions). Read the relevant file before making design-affecting changes. If the code and the docs disagree, ask me which is right.

**Current stage: prototyping.** Goal is to test the risky parts early (large-scale world restoration, automation entity counts, atmosphere/rendering). Prefer the simplest thing that answers the question. Do not build production systems yet.

## Stack
- Godot 4.x, .NET version, **C# only**. No GDScript.
- Use current Godot 4 APIs. Do not use Godot 3 patterns or deprecated APIs. If unsure whether an API is current, say so instead of guessing.
- Build and check for errors with `dotnet build`.

## How to work with me
- I want to understand *why* decisions are made, not just receive code. Before non-trivial changes, explain the approach and the trade-offs, and wait for my go-ahead.
- Keep changes small and focused: one task per change, so I can review each diff.
- Tell me when something is a Godot convention, when it is a C# specific, and when it is your opinion.
- If a request has a better alternative, say so before implementing it.

## Godot conventions
- Prefer building scenes in the Godot editor. Do not hand-edit `.tscn` or `.tres` files unless I ask. Tell me what to set up in the editor instead.
- One scene per self-contained thing (e.g. Player). A scene should work on its own without depending on its parent scene.
- C# classes that attach to nodes must be `partial` and match the filename.
- Avoid per-frame allocations in `_Process` / `_PhysicsProcess` (watch `StringName`, `NodePath`, LINQ, and string building).
- Movement and physics belong in `_PhysicsProcess`. Input handling belongs in `_Input` / `_UnhandledInput`.

## Design constraints (provisional, to validate by prototyping)
- Keep game state separable from the scene tree and serialisable, so co-op and save/load are not painful to add later.
- Automation machines and items are likely to number in the thousands. Do not assume they should be individual Nodes.
- Restoration of the world will cover large areas. Do not use one Node per piece of rubble or foliage.

## Git
- Work on a branch per task. Do not commit to `main` directly.
- Do not commit unless I ask. Do not push.
- Never commit the `.godot/`, `bin/` or `obj/` folders.
