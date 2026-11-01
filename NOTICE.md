# Modified Apotheotic Additions data

Ported affix data and corresponding English affix names are adapted from
Bryce792 / MCreator's Apotheotic Additions 2.2.2. Upstream metadata declares
Academic Free License v3.0; its license text accompanies this source and JAR.
(Its CurseForge page states the MIT License; see "Permission, licence and status" below.)
Original project: https://github.com/Bryce792/ApotheoticAdditions
Pinned source revision: `822ecf6993ceaada1504e8dd10a8fea727a6235d`.

This is modified source data: resource namespace, modifier-operation names,
loot-category mapping, attribute-library namespace and affix definition
weights were adapted for native Minecraft 1.21.1 / Apotheosis 8.9.0.
Original rarity-specific min/steps/step curves and affix names are retained.
The checked-in migration manifest records each source file and pending work.
No original Java classes are included. **No upstream textures are included** (since 17 Oct 2026; see "Textures" below). The gem item models under `assets/apotheosis/models/item/gems/` (where stock Apotheosis scans for gem models) are adapted from upstream.
Original native port Java/helpers remain MIT licensed; ported data remains
under AFL-3.0. Read LICENSE.AFL-3.0 before redistributing or using the ported
data. The upstream authors do not endorse this compatibility prototype.

Corresponding modified source and migration tooling:
https://github.com/alsynth/AmbientOdyssey/tree/experimental/v046-wetsand-apotheotic-ports-20261011

Status: a prototype release for the Ambient Odyssey modpack (version 0.4.8-kit5c); the migration manifest records the upstream content that is not ported. Natural drop weights of the custom rarities and gems follow the original data (gems) and
`tools/data/rarity_weights.json` (rarities).

## Apotheosis
The affix pools use the structure of Apotheosis 8.9.0's affix definitions, re-emitted under this mod's own ids, names and weights (no Apotheosis file is copied or
overridden). The only file under the `apotheosis` data namespace is the item tag `data/apotheosis/tags/item/rarity_materials.json`, which ADDS the
four port materials (`"replace": false`). The three always-false overrides that disabled the giant-slaying, gravitational and fireproof affixes were
removed from this JAR in kit2 (17 Oct 2026); Ambient Odyssey ships them in its own pack datapack instead.
(Quote removed pending owner evidence, 16 Oct 2026.)

## Textures (17 Oct 2026)
All 42 item textures (37 gems, the four rarity materials and the Sigil of Awakening, with their `.mcmeta` files) are **original Ambient Odyssey artwork** (17 Oct 2026): drawn for this project by Claude (Anthropic), an AI model, under the owner's direction, as hand-authored code (`ports/apotheotic-additions/tools/texture_generators/`), with no pixels taken from any upstream Apotheotic Additions, Apotheosis, vanilla or other mod texture. They replace every upstream texture; resource names, item models and registry ids are unchanged. The four rarity-material icons are 32x32 per frame; all other textures are 16x16. The owner holds the rights to use them as the project's own art; they are MIT licensed like the port's code. The Ancient Material item is now named "Ancient Material" (previously "Odyssey Pearl").

## Apex-tier gleam textures (17 Oct 2026, kit3)
The 12 rarity textures `assets/ao_apotheotic_port/textures/rarity/{ancient,artifact,heirloom,esoteric}_{beam,glow,shadow}.png` (16x16 beam and glow,
64x1024 shadow of 16 frames) are original Ambient Odyssey artwork, drawn for this project by Claude (Anthropic) under the owner's direction as
hand-authored code (`ports/apotheotic-additions/tools/texture_generators/gleams.py`), with no pixels taken from any upstream, Apotheosis, vanilla or
other mod texture. They replace the port rarities' references to Apotheosis' own beam, glow and shadow textures. MIT licensed like the port's code.

## Sigil of Awakening, new look (18 Oct 2026, kit4)
`assets/ao_apotheotic_port/textures/items/gembound_sigil.png` was redrawn: drawn for this project by Claude (Anthropic) under the owner's direction
as hand-authored code (`ports/apotheotic-additions/tools/texture_generators/sigil_new.py`), using the owner's screenshot of an Apotheosis basic
sigil as a visual style reference only; no pixels were copied; geometry, palette, corner marks and the central gem differ. MIT licensed like the
port's code.

## Permission, licence and status (corrected 16 Oct 2026; 21 Oct 2026)
Unofficial port of content from Apotheotic Additions by Bryce792 (textures credited to malcomriley on its CurseForge page),
made for Apotheosis. **No permission from Bryce792 is claimed**, and none is claimed from the Apotheosis author (as on the approved CurseForge page).

Licence of the original project, exactly as stated (checked 16 Oct 2026):
- CurseForge project page (https://www.curseforge.com/minecraft/mc-mods/apotheotic-additions, project 924640): "MIT License"
  (standard MIT text; its copyright line is the unfilled template "Copyright (c) <year> <copyright holders>").
- Mod metadata at revision `822ecf69` (`META-INF/mods.toml`): `license="Academic Free License v3.0"`.
- GitHub repository: no LICENSE file.
Neither statement separates code, data and textures, so this port keeps both notices: the AFL-3.0 text (LICENSE.AFL-3.0) and
the MIT text (LICENSE, which also covers AO's own code and textures). No upstream Java is included.
Not endorsed by Bryce792 or by the Apotheosis author.

## Earlier texture history
16 Oct 2026: four gem textures (`ars_mana`, `purity`, `undergarden`, `decay`) were first replaced by `tools/make_original_gem_textures.py`. 17 Oct 2026: all 42 textures, including those four, were replaced by the set described under "Textures".
