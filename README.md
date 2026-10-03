# Hollis and Sons Game Art

This repository contains the approved miner reference and 20 matching PNG art assets for a cheerful 1950s mining-company game. The miner is unchanged. The remaining images are ready for review and integration into the existing game.

[Download the complete repository as a ZIP](https://github.com/brockrichardson1234-max/hollis-and-sons-art-pack/archive/refs/heads/main.zip). [manifest.json](manifest.json) lists each image, dimensions, raw download URL, generation prompt, and integration notes. The complete prompt set is also in [art-prompts.txt](art-prompts.txt).

Claude can start with the [raw manifest](https://raw.githubusercontent.com/brockrichardson1234-max/hollis-and-sons-art-pack/main/manifest.json) and fetch the images through its download URLs.

For integration:

- Preserve the approved miner and align its four pose frames during import. The approval reported that the miner remained readable at about 29 pixels in the game.
- Hats and tools are separate sprites. Fit them to the miner's head and hands using the game's existing attachment logic.
- Use The Dynamo as the energy machine and the diamond-tipped drill as the final tool. Both use mechanical brass and copper construction. The double pick has two larger opposing points; preserve its taller proportions when scaling. Its separate browser check retained both tips at 10 pixels wide, with a 10×9 raster compared with 10×5 for the pickaxe.
- Use the selected mole v2 sheet. It is a 2×2 grid with two loaded frames in the top row and two lunch-pail return frames in the bottom row. All face left, with distinct walking steps.
- Big Bertha's nameplate is blank. Add the lettering in the game. Its downward-pointing drill bit is a separate image for animation.
- The ground sheet is fully opaque: a 3×3 grid of 418×418 cells. Row 1 is dirt, dirt variant, coal; row 2 is copper, silver, gold; row 3 is diamond, back wall, solid timber support. Keep the timber as a tile.
- The camp backdrop is opaque and has a 3:1 aspect ratio.
- The character, gear, camp assets, and portrait have actual alpha transparency. Some retain soft colored fringes outside their outlines; trim those during the cutout pass. Check ground-tile seams under repetition in the game.
- Preserve all existing prices, rates, bonuses, and other gameplay values. Final scaling, alignment, and checks at game size happen during integration.

| Asset | File | Dimensions |
| --- | --- | --- |
| Approved miner, four poses | [PNG](miner-four-poses-v1.png) | 1254 × 1254 |
| headlamp helmet | [PNG](hats/hat-headlamp-helmet-v1.png) | 1536 × 1024 |
| raised welder's visor | [PNG](hats/hat-welder-visor-v1.png) | 1254 × 1254 |
| yellow hard hat | [PNG](hats/hat-yellow-hardhat-v2.png) | 1536 × 1024 |
| diamond-tipped drill | [PNG](tools/tool-diamond-drill-v1.png) | 1774 × 887 |
| double-headed pick | [PNG](tools/tool-double-pick-v2.png) | 1536 × 1024 |
| jackhammer | [PNG](tools/tool-jackhammer-v1.png) | 1774 × 887 |
| pickaxe | [PNG](tools/tool-pickaxe-v1.png) | 1774 × 887 |
| pneumatic rock drill | [PNG](tools/tool-rock-drill-v1.png) | 1774 × 887 |
| shovel | [PNG](tools/tool-shovel-v1.png) | 2109 × 745 |
| Mole courier — four frames with distinct walking steps | [PNG](moles/mole-four-frames-v2.png) | 1254 × 1254 |
| Big Bertha — separate moving drill bit | [PNG](machines/machine-big-bertha-bit-v1.png) | 1214 × 1295 |
| Big Bertha body | [PNG](machines/machine-big-bertha-body-v1.png) | 1254 × 1254 |
| Foreman's Office | [PNG](machines/machine-foremans-office-v1.png) | 1374 × 1145 |
| Power House | [PNG](machines/machine-power-house-v1.png) | 1448 × 1086 |
| The Dynamo | [PNG](machines/machine-dynamo-v1.png) | 1536 × 1024 |
| Spoil Heap | [PNG](machines/machine-spoil-heap-v1.png) | 1536 × 1024 |
| Wash Plant | [PNG](machines/machine-wash-plant-v1.png) | 1536 × 1024 |
| Ground — nine opaque tiles | [PNG](ground/ground-nine-tiles-v1.png) | 1254 × 1254 |
| Camp backdrop — wide panorama | [PNG](backdrop/camp-backdrop-v1.png) | 2172 × 724 |
| Old Hollis — framed founder portrait | [PNG](portrait/old-hollis-portrait-v1.png) | 1024 × 1536 |

The art was generated with the built-in imagegen tool using the approved miner as the style reference. The prompts and manifest document the selected versions. Unused drafts and local working files are excluded.
