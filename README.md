# Gmarc's Gen 1 Kanto in First Person 2.0.1

A [gen1recomp](https://github.com/bryanthaboi/gen1recomp) mod.
A companion for modern gen1recomp, installed alongside **DRAMATIC_SHAPE**.
Adds interiors with ceilings, textured cave roofs and rock, forest canopy,
native grass, birds, skies, horizon, weather and ambient sound to the voxel
renderer. This mod does not include a voxel renderer or any ROM data.

## Install

Import `KANTO_FIRST_PERSON.zip` and `DRAMATIC_SHAPE.zip` through the engine's
mod importer. Enable both in the Mods menu and restart the game. Use the
appropriate game generation: Red, Blue or Yellow.
Choose **VOXEL → 1ST** or **3RD** in the game's options (or cycle with `3`).
The companion does not force your camera or modify your save.

Disable/remove the old `ds_fp_ceiling` companion before enabling this replacement. It is intentionally incompatible with the old disk patcher. If the old companion patched your renderer, reinstall the clean updated DRAMATIC_SHAPE ZIP first.

## Controls and settings

The voxel mod owns the camera: mouse/right stick/touch drag to look; arrows,
left stick or touch d-pad to walk relative to it. Existing engine menus,
collision and native ledges remain in charge.

The companion settings are in the Mods menu. **FIRST PERSON EFFECTS** disables
all companion drawing. **EFFECT QUALITY** defaults to BALANCED; LOW reduces
clouds, birds and rain and disables particles, insects, aircraft, ground flocks
and puddles. HIGH restores the larger effect budgets. Individual options
control ceiling/headroom, third-person cutaway, weather, sky, sound, grass,
FOV and jump feel. Keep the renderer's AA and water-reflection settings low
on slower devices; those costs belong to the renderer.

Space (pad Y by default, configurable) makes a short camera hop during idle
first/third-person roaming. It never crosses walls or replaces native ledge
movement. It passes controls through in menus, scripts and near an NPC.

## Modernization

Shared code is in `mods/shared/first-person-effects`; `lib/` and `assets/` are
relative development links. `scripts/export-mods.py` materializes these into
a self-contained companion ZIP. Do not ZIP this source folder directly.
Runtime hooks replace the old file patcher and global callback replacements.
Disabling effects restores the camera FOV and releases ambient sound.
Legacy FAST CHUNKS/removal controls and patched TALL TREES lifting are retired;
the voxel renderer keeps its native tree models.

Kanto keeps its native Gen 1 tiles and imported Pokémon sprites. This release also requires the updated Dramatic Shape 1.6.3 for current engine compatibility and indexed terrain rendering.

Original presentation code/assets: mrmushrooms11's Kanto in First Person,
upstream commit `94d0151` (original version 1.57.2). Modern runtime integration,
native Gen 2 adapter and quality controls are maintained in this workspace.
See the shared project's README and `docs/architecture.md` for development.

## Original mod

This continues **Kanto in First Person** by **mrmushrooms11**:
<https://github.com/mrmushrooms11/kanto-first-person> — last updated August
2026 and no longer maintained upstream. The history in this repository starts
fresh from that code so it can be maintained here.
