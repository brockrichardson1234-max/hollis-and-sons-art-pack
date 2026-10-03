# Hollis and Sons Game Art

This repository contains the approved miner reference and 66 matching PNG art assets for a cheerful 1950s mining-company game. The miner is unchanged. The pack includes seven miner sprite sheets with fitted headwear and a female character, ready for review and integration into the existing game.

[Download the complete repository as a ZIP](https://github.com/brockrichardson1234-max/hollis-and-sons-art-pack/archive/refs/heads/main.zip). [manifest.json](manifest.json) lists each image, dimensions, raw download URL, generation prompt, and integration notes. The complete prompt set is also in [art-prompts.txt](art-prompts.txt).

Claude can start with the [raw manifest](https://raw.githubusercontent.com/brockrichardson1234-max/hollis-and-sons-art-pack/main/manifest.json) and fetch the images through its download URLs.

For integration:

- Preserve the approved miner and align its four pose frames during import. The approval reported that the miner remained readable at about 29 pixels in the game.
- The six helmet sheets already include their headwear. Use shared 627 x 627 frame rectangles and the same character origin when switching helmets. Tools remain separate sprites and keep the existing hand attachment positions. The original separate hat assets remain available.
- Use The Dynamo as the energy machine and the diamond-tipped drill as the final tool. Both use mechanical brass and copper construction. The double pick has two larger opposing points; preserve its taller proportions when scaling. Its separate browser check retained both tips at 10 pixels wide, with a 10×9 raster compared with 10×5 for the pickaxe.
- Use the selected mole v2 sheet. It is a 2×2 grid with two loaded frames in the top row and two lunch-pail return frames in the bottom row. All face left, with distinct walking steps.
- Big Bertha's nameplate is blank. Add the lettering in the game. Its downward-pointing drill bit is a separate image for animation.
- The ground sheet is fully opaque: a 3×3 grid of 418×418 cells. Row 1 is dirt, dirt variant, coal; row 2 is copper, silver, gold; row 3 is diamond, back wall, solid timber support. Keep the timber as a tile.
- The camp backdrop is opaque and has a 3:1 aspect ratio.
- Transparent PNGs have actual alpha. Some earlier gear, camp assets and the portrait retain soft colored fringes; trim those during their cutout pass. Keep the miner sheets on their shared frame origins. Check ground-tile seams under repetition in the game.
- Preserve all existing prices, rates, bonuses, and other gameplay values. Final scaling, alignment, and checks at game size happen during integration.

| Asset | File | Dimensions |
| --- | --- | --- |
| Approved miner, four poses | [PNG](miner-four-poses-v1.png) | 1254 × 1254 |
| Male miner — yellow hard hat, four poses | [PNG](miner-hardhat-v1.png) | 1254 × 1254 |
| Male miner — headlamp helmet, four poses | [PNG](miner-headlamp-v1.png) | 1254 × 1254 |
| Male miner — raised welder helmet, four poses | [PNG](miner-welder-v1.png) | 1254 × 1254 |
| Female miner — bare head, four poses | [PNG](miner-female-v1.png) | 1254 × 1254 |
| Female miner — yellow hard hat, four poses | [PNG](miner-female-hardhat-v1.png) | 1254 × 1254 |
| Female miner — headlamp helmet, four poses | [PNG](miner-female-headlamp-v1.png) | 1254 × 1254 |
| Female miner — raised welder helmet, four poses | [PNG](miner-female-welder-v1.png) | 1254 × 1254 |
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

The art was generated with the built-in imagegen tool using the approved miner as the style reference. The prompts and manifest document the selected versions and pass-2 rejected attempts. Unused draft images and local working files are excluded.

## Miner sheet checks

The male helmet sheets preserve the approved male body, gloves and boots pixel for pixel. The female base was independently drawn with her own body, aligned and checked first; her three helmet sheets preserve that female body. The lower faces and necks remain from each reference, with feathered head edits and soft brim shadows. All sheets have true alpha, the original 1254 x 1254 canvas, four 627 x 627 cells, the same pose order and no tools.

All 28 final poses were reviewed close up and in standalone previews at about 29 pixels standing height. [miner-sprite-checks.json](miner-sprite-checks.json) records hashes, pixel comparisons and preview scope. The game integration and Wardrobe playtest happen in the game repository.

## Miner generation prompts

These are the selected built-in imagegen prompts. Helmet outputs were then fitted to the checked body references with the user-authorized feathered-mask method. The female base was drawn and checked before her helmet variants.

<details>
<summary>miner-hardhat-v1.png</summary>

```text
Use case: identity-preserve / precise-object-edit.
Asset type: one transparent four-pose miner sprite sheet for the Hollis & Sons 2D game.
Treat the approved miner sheet as a locked edit target, not inspiration for a new drawing. Preserve its 1254×1254 square canvas and exact 2×2 cell layout: top left ready with fists together at waist height, top right wind-up with fists together behind the head, bottom left downward strike, bottom right recovering follow-through. All face right.
Keep the original figure's exact scale, position and proportions in every cell. Keep each boot, foot baseline, leg, torso, sleeve, glove, hand, face, expression, and outline in its original location. Do not recenter, rescale, re-pose, stretch, simplify, or redraw the body. Hand positions must be identical; add no tool.
Match the approved image's flat two-tone 1950s American industrial safety-poster drawing, chunky even dark-brown outlines, teal #2F6B66 coveralls, cream #EFE4C8 gloves, brown boots, natural warm skin, upper-left light, restrained grain inside the artwork.
Output exactly one sprite sheet, with genuinely transparent alpha outside the figures and between cells. No background color, checkerboard pixels, scenery, ground shadow, exterior glow, labels, text, logos, borders or grid lines. Preserve all available empty margins.

Image 1 is the approved male miner sheet and the sole edit target. Image 2 is the approved yellow hard hat design, to be scaled and fitted onto his head in each of the four existing poses.
Change ONLY the top of the head/hair and the immediate forehead shadow to make the same man wear this safety-yellow #F2B829 hard hat. Keep his facial identity and expression exactly. The head must sit INSIDE the crown; the brim rests snugly across the forehead, a little above the eyebrows. Hide the top and front hair under the hat; show only a little at the back and sides. Cast a soft, restrained brim shadow on the forehead. Rotate the fitted hat naturally with the head's existing angle, particularly the forward-bent bottom-left strike. Never perch the hat above the hair or leave an air gap. Size it as protective headwear, not an oversized costume.
Keep the whole figure, including hat, inside each original cell. Everything below the head remains unchanged. Preserve the exact original boot coordinates and body size. Save as miner-hardhat-v1.png.
```

Alignment refinement used before fitting the selected head edit:

```text
Use case: identity-preserve / precise-object-edit.
Asset type: one transparent four-pose miner sprite sheet for the Hollis & Sons 2D game.
Treat the approved miner sheet as a locked edit target, not inspiration for a new drawing. Preserve its 1254×1254 square canvas and exact 2×2 cell layout: top left ready with fists together at waist height, top right wind-up with fists together behind the head, bottom left downward strike, bottom right recovering follow-through. All face right.
Keep the original figure's exact scale, position and proportions in every cell. Keep each boot, foot baseline, leg, torso, sleeve, glove, hand, face, expression, and outline in its original location. Do not recenter, rescale, re-pose, stretch, simplify, or redraw the body. Hand positions must be identical; add no tool.
Match the approved image's flat two-tone 1950s American industrial safety-poster drawing, chunky even dark-brown outlines, teal #2F6B66 coveralls, cream #EFE4C8 gloves, brown boots, natural warm skin, upper-left light, restrained grain inside the artwork.
Output exactly one sprite sheet, with genuinely transparent alpha outside the figures and between cells. No background color, checkerboard pixels, scenery, ground shadow, exterior glow, labels, text, logos, borders or grid lines. Preserve all available empty margins.

Image 1 is the approved male miner sheet and the sole edit target. Image 2 is the approved yellow hard hat design, to be scaled and fitted onto his head in each of the four existing poses.
Change ONLY the top of the head/hair and the immediate forehead shadow to make the same man wear this safety-yellow #F2B829 hard hat. Keep his facial identity and expression exactly. The head must sit INSIDE the crown; the brim rests snugly across the forehead, a little above the eyebrows. Hide the top and front hair under the hat; show only a little at the back and sides. Cast a soft, restrained brim shadow on the forehead. Rotate the fitted hat naturally with the head's existing angle, particularly the forward-bent bottom-left strike. Never perch the hat above the hair or leave an air gap. Size it as protective headwear, not an oversized costume.
Keep the whole figure, including hat, inside each original cell. Everything below the head remains unchanged. Preserve the exact original boot coordinates and body size. Save as miner-hardhat-v1.png.

Alignment correction: the first attempt changed body pixels and shifted some gloves/boots, which is not acceptable. Edit Image 1 locally; preserve its original pixels outside these four head rectangles (coordinates in the 1254×1254 sheet): ready x276–431 y20–214; wind-up x879–1039 y35–225; strike x387–557 y670–852; follow-through x874–1044 y613–802. These rectangles are the ONLY permitted edit areas.
Image 2 is the previous fitted-hardhat result: use ONLY its four worn-hat/head treatments as reference. Do NOT use its body, gloves, face placement, or boots. Image 3 is the original yellow hat design.
Restore the exact ORIGINAL torso/legs/gloves/boots from Image 1; do not change any contour or shading outside the head rectangles. Original foot baselines, hand anchors, figure scales and cell offsets must match precisely. Keep the man’s eyes, nose, mouth and jaw in Image 1's original coordinates. Place the hat around that existing head, hiding the upper hair and touching the forehead, with the strike hat rotated down with the existing head. One 1254×1254 image with real alpha, no rescaling.
```

Finishing method: Generated headwear/hair edits fitted with an 8px feathered mask. The reference lower face, neck, coveralls, hands, legs and boots are preserved, with a soft brim shadow on the forehead. Helmet outlines are kept intact and stay within their original cells.

</details>

<details>
<summary>miner-headlamp-v1.png</summary>

```text
Use case: identity-preserve / precise-object-edit.
Asset type: one transparent four-pose miner sprite sheet for the Hollis & Sons 2D game.
Treat the approved miner sheet as a locked edit target, not inspiration for a new drawing. Preserve its 1254×1254 square canvas and exact 2×2 cell layout: top left ready with fists together at waist height, top right wind-up with fists together behind the head, bottom left downward strike, bottom right recovering follow-through. All face right.
Keep the original figure's exact scale, position and proportions in every cell. Keep each boot, foot baseline, leg, torso, sleeve, glove, hand, face, expression, and outline in its original location. Do not recenter, rescale, re-pose, stretch, simplify, or redraw the body. Hand positions must be identical; add no tool.
Match the approved image's flat two-tone 1950s American industrial safety-poster drawing, chunky even dark-brown outlines, teal #2F6B66 coveralls, cream #EFE4C8 gloves, brown boots, natural warm skin, upper-left light, restrained grain inside the artwork.
Output exactly one sprite sheet, with genuinely transparent alpha outside the figures and between cells. No background color, checkerboard pixels, scenery, ground shadow, exterior glow, labels, text, logos, borders or grid lines. Preserve all available empty margins.

Image 1 is the approved male miner sheet and sole edit target. Image 2 is the approved miner's headlamp helmet design: a yellow crown, machine-steel retaining band and front-mounted brass lamp. Fit that exact helmet onto the same man's head in each of the four existing poses.
Change ONLY the upper head/hair and a small shadow on the forehead. Preserve the existing face, eyes, nose, mouth, jaw and their positions. Put the top of the head INSIDE the helmet, with its brim resting on the forehead above the eyebrows, hair mostly tucked away and only a little brown hair visible behind the ear. A restrained soft brim shadow falls on the forehead. The helmet follows each original head tilt; bottom-left points downward with the bent striking head. The lamp faces right with the face and has a cream lens, without a projecting beam or exterior glow.
Keep the helmet small enough to wear naturally. It must not float or sit on top of visible hair. Never move or redraw the original torso, sleeves, gloves, fists, legs or boots. Foot baselines and hand anchors stay at the original exact coordinates. One 1254×1254 transparent PNG, no rescaling, named miner-headlamp-v1.png.
```

Finishing method: Generated headwear/hair edits fitted with an 8px feathered mask. The reference lower face, neck, coveralls, hands, legs and boots are preserved, with a soft brim shadow on the forehead. Helmet outlines are kept intact and stay within their original cells.

</details>

<details>
<summary>miner-welder-v1.png</summary>

```text
Use case: identity-preserve / precise-object-edit.
Asset type: one transparent four-pose miner sprite sheet for the Hollis & Sons 2D game.
Treat the approved miner sheet as a locked edit target, not inspiration for a new drawing. Preserve its 1254×1254 square canvas and exact 2×2 cell layout: top left ready with fists together at waist height, top right wind-up with fists together behind the head, bottom left downward strike, bottom right recovering follow-through. All face right.
Keep the original figure's exact scale, position and proportions in every cell. Keep each boot, foot baseline, leg, torso, sleeve, glove, hand, face, expression, and outline in its original location. Do not recenter, rescale, re-pose, stretch, simplify, or redraw the body. Hand positions must be identical; add no tool.
Match the approved image's flat two-tone 1950s American industrial safety-poster drawing, chunky even dark-brown outlines, teal #2F6B66 coveralls, cream #EFE4C8 gloves, brown boots, natural warm skin, upper-left light, restrained grain inside the artwork.
Output exactly one sprite sheet, with genuinely transparent alpha outside the figures and between cells. No background color, checkerboard pixels, scenery, ground shadow, exterior glow, labels, text, logos, borders or grid lines. Preserve all available empty margins.

Image 1 is the approved male miner sprite sheet and sole edit target. Image 2 is the approved machine-steel welder's helmet with its rectangular visor flipped UP, dark brown outlines, cream steel edge highlights and round hinge hardware. Scale and fit that exact helmet onto the existing man's head in each of his four poses.
Change ONLY the upper head/hair and the small immediate forehead shadow. The head is inside the steel crown, with its forehead band seated snugly above the eyebrows and a little brown hair visible only near the ear/back. The raised hinged visor stays above the face; all eyes, nose, smiling mouth and jaw remain visible, with their original identity and coordinates. Add the soft forehead shadow from the helmet's band. The crown, hinge and raised visor move together, tilting naturally with the existing head in each cell, especially the forward-down strike. No floating helmet, no visible thick hair mound under the crown, no dangling straps over hands.
Keep the head and face in their original positions; do not enlarge or lower them. Preserve the original body's contours, teal coveralls, cream gloves and brown boots pixel for pixel. Fists remain closed with no tool. Preserve the exact original baselines and margins. One transparent 1254×1254 sprite sheet, no rescaling, named miner-welder-v1.png.
```

Finishing method: Generated headwear/hair edits fitted with an 8px feathered mask. The reference lower face, neck, coveralls, hands, legs and boots are preserved, with a soft brim shadow on the forehead. Helmet outlines are kept intact and stay within their original cells.

</details>

<details>
<summary>miner-female-v1.png</summary>

```text
Use case: illustration-story / identity-preserve.
Asset type: female miner base sprite sheet for the Hollis & Sons 2D game, a genuinely transparent PNG.
Image 1 is the approved male miner sheet: use it as a precise canvas, pose, scale, glove-position, boot-position and style reference. Image 2 is the chosen female character: preserve her consistent short chestnut-brown swept-back hair and friendly adult female face across all four poses.

Redraw a complete female miner with HER OWN female body. This is not a male body with a swapped female head. Keep a sturdy, practical build in loose teal company coveralls, cream work gloves and brown work boots. Give her naturally feminine shoulder/torso/hip anatomy under the workwear, without exaggerated curves, a tiny waist, or sexualized clothing. Her body occupies the same overall size and stance as the approved male, with the same head scale, pose angles, hand grip centers and boot contact positions. Preserve the chosen woman's warm skin color, face, smiling expression and short practical hair consistently. No hat and no tool; closed hands gripping an invisible handle.

Exact composition: 1254×1254 square canvas, precise 2×2 grid, each cell 627×627. Top left READY: fists together at waist height. Top right WIND-UP: fists together raised behind the head. Bottom left STRIKE: forward bend and fists together lowered in front. Bottom right FOLLOW-THROUGH: recovering with hands in front. All face right. Match Image 1's figure position, size, hand placement and foot baseline separately in each corresponding cell. Do not add new padding, crop, rescale or recenter the sheet. Full boots visible and feet planted.

Match the reference illustration exactly: cheerful 1950s American industrial safety-poster art, flat colors with two-tone shading, chunky even dark-brown outlines, company teal #2F6B66, cream #EFE4C8 gloves, brown boots, copper-brown hair, upper-left lighting and restrained paper grain confined to the shapes.
Fully transparent alpha around and between the figures; no white or checkered background, exterior halo, glow, ground shadow, scene, tools, hats, jewelry, logos, text, borders or grid lines. One complete four-pose sheet named miner-female-v1.png. This sheet will become the fixed female body reference for all her helmet variants.
```

Finishing method: Female-only pixels aligned within the original 627px cells. All four boot baselines match the approved male sheet; the largest glove centroid difference is 0.25 native pixels.

</details>

<details>
<summary>miner-female-hardhat-v1.png</summary>

```text
Use case: identity-preserve / precise-object-edit.
Asset type: one transparent four-pose miner sprite sheet for the Hollis & Sons 2D game.
Treat the approved miner sheet as a locked edit target, not inspiration for a new drawing. Preserve its 1254×1254 square canvas and exact 2×2 cell layout: top left ready with fists together at waist height, top right wind-up with fists together behind the head, bottom left downward strike, bottom right recovering follow-through. All face right.
Keep the original figure's exact scale, position and proportions in every cell. Keep each boot, foot baseline, leg, torso, sleeve, glove, hand, face, expression, and outline in its original location. Do not recenter, rescale, re-pose, stretch, simplify, or redraw the body. Hand positions must be identical; add no tool.
Match the approved image's flat two-tone 1950s American industrial safety-poster drawing, chunky even dark-brown outlines, teal #2F6B66 coveralls, cream #EFE4C8 gloves, brown boots, natural warm skin, upper-left light, restrained grain inside the artwork.
Output exactly one sprite sheet, with genuinely transparent alpha outside the figures and between cells. No background color, checkerboard pixels, scenery, ground shadow, exterior glow, labels, text, logos, borders or grid lines. Preserve all available empty margins.

Image 1 is the CHECKED FEMALE BASE and sole edit target. Image 2 is the original male sheet, provided only as the original pose/style reference. Do not reuse the man's face or body. Image 3 is the approved yellow hard hat design.
Fit that safety-yellow #F2B829 hard hat naturally onto this same woman in every one of her four existing poses. Preserve her exact female face, smiling expression, head size, neck position, eye line and short chestnut-brown hair identity. Hide her entire top/front hair under the crown and cut the hair silhouette back to the brim line, showing only a small amount behind the ear and at the back. The crown surrounds the top of her head; the brim rests directly on her forehead above her eyebrows and casts a soft, restrained shadow onto the forehead. No hair through the brim and no gap between hat and head. Rotate the helmet with her original head tilt, including the forward/down bottom-left strike.
Leave HER existing body, sleeves, gloves, closed hands, outfit, legs, boots, figure positions and foot baselines unchanged. Do not substitute any male anatomy. We will preserve her approved body pixels and blend only the generated head/hat edit at the neck with a soft feathered mask. No tool, no background, no glow. One 1254×1254 transparent sheet named miner-female-hardhat-v1.png.
```

Finishing method: Generated headwear/hair edits fitted with an 8px feathered mask. The reference lower face, neck, coveralls, hands, legs and boots are preserved, with a soft brim shadow on the forehead. Helmet outlines are kept intact and stay within their original cells.

</details>

<details>
<summary>miner-female-headlamp-v1.png</summary>

```text
Use case: identity-preserve / precise-object-edit.
Asset type: one transparent four-pose miner sprite sheet for the Hollis & Sons 2D game.
Treat the approved miner sheet as a locked edit target, not inspiration for a new drawing. Preserve its 1254×1254 square canvas and exact 2×2 cell layout: top left ready with fists together at waist height, top right wind-up with fists together behind the head, bottom left downward strike, bottom right recovering follow-through. All face right.
Keep the original figure's exact scale, position and proportions in every cell. Keep each boot, foot baseline, leg, torso, sleeve, glove, hand, face, expression, and outline in its original location. Do not recenter, rescale, re-pose, stretch, simplify, or redraw the body. Hand positions must be identical; add no tool.
Match the approved image's flat two-tone 1950s American industrial safety-poster drawing, chunky even dark-brown outlines, teal #2F6B66 coveralls, cream #EFE4C8 gloves, brown boots, natural warm skin, upper-left light, restrained grain inside the artwork.
Output exactly one sprite sheet, with genuinely transparent alpha outside the figures and between cells. No background color, checkerboard pixels, scenery, ground shadow, exterior glow, labels, text, logos, borders or grid lines. Preserve all available empty margins.

Image 1 is the CHECKED FEMALE BASE and the sole edit target. Image 2 is the approved male sheet, only for original pose/style reference. Keep the woman's own face and body. Image 3 is the approved yellow headlamp helmet with a machine-steel band and front-mounted brass lamp.
Change only the woman's head/hair and immediate forehead shadow to wear that headlamp helmet naturally in all four poses. Her top of head sits INSIDE the crown. The brim rests on the forehead just above the eyebrows and casts a soft shadow. Tuck all top/front hair inside; cut the remaining hair back closely to the hat line and retain only a little short brown hair behind the ear. No hair passing through the brim and no visible bulky hair mound under the helmet. Keep her female face, eyes, smile, warm skin, head scale and head position unchanged.
The helmet tilts as one fitted piece with her existing head: right-facing in each frame, rotated forward/down in the strike. Its brass lamp faces the same direction as her face; cream lens without a beam or outer glow. Do not float the hat or enlarge it into a costume.
Keep HER original body, all cream-gloved hand pixels, boot positions and baselines fixed. No tool and no male body substitution. Only the generated head/hat will be blended at her collar using a softly feathered mask while her checked body pixels are kept intact. One genuinely transparent 1254×1254 2×2 sheet, named miner-female-headlamp-v1.png.
```

Finishing method: Generated headwear/hair edits fitted with an 8px feathered mask. The reference lower face, neck, coveralls, hands, legs and boots are preserved, with a soft brim shadow on the forehead. Helmet outlines are kept intact and stay within their original cells.

</details>

<details>
<summary>miner-female-welder-v1.png</summary>

```text
Use case: identity-preserve / precise-object-edit.
Asset type: one transparent four-pose miner sprite sheet for the Hollis & Sons 2D game.
Treat the approved miner sheet as a locked edit target, not inspiration for a new drawing. Preserve its 1254×1254 square canvas and exact 2×2 cell layout: top left ready with fists together at waist height, top right wind-up with fists together behind the head, bottom left downward strike, bottom right recovering follow-through. All face right.
Keep the original figure's exact scale, position and proportions in every cell. Keep each boot, foot baseline, leg, torso, sleeve, glove, hand, face, expression, and outline in its original location. Do not recenter, rescale, re-pose, stretch, simplify, or redraw the body. Hand positions must be identical; add no tool.
Match the approved image's flat two-tone 1950s American industrial safety-poster drawing, chunky even dark-brown outlines, teal #2F6B66 coveralls, cream #EFE4C8 gloves, brown boots, natural warm skin, upper-left light, restrained grain inside the artwork.
Output exactly one sprite sheet, with genuinely transparent alpha outside the figures and between cells. No background color, checkerboard pixels, scenery, ground shadow, exterior glow, labels, text, logos, borders or grid lines. Preserve all available empty margins.

Image 1 is the CHECKED FEMALE BASE and sole edit target. Image 2 is the approved male sheet for original pose/style reference only. Preserve this woman's own female face and body. Image 3 is the approved machine-steel welder's helmet, cream metal-edge highlights, hinge hardware and rectangular visor flipped UP.
Fit the exact raised-visor helmet onto the woman in all four existing poses. Keep the face fully visible below the raised visor: same eyes, friendly smile, nose, jaw, warm skin, short chestnut-brown hair identity and head coordinates as Image 1. The head sits INSIDE the crown. The forehead band rests directly just above the eyebrows, with a soft restrained shadow on the forehead. All top/front hair is tucked inside; cut the side/back hair closely to the helmet line and show only a little behind the ear, never poking through the band or crown.
The steel crown, hinge and raised visor form one worn helmet, tilting naturally with each original head angle, including the downward-looking bottom-left strike. No floating helmet, air gap, enlarged head, face-obscuring visor or dangling straps crossing the hands.
Keep HER approved body pixels, outfit, sleeves, gloves, closed hands, legs, brown boots and baselines fixed. No male body substitution, no tool, background or exterior glow. Only this head/helmet edit will be softly feathered into her collar while her own checked body pixels stay intact. One 1254×1254 genuine transparent PNG, named miner-female-welder-v1.png.
```

Finishing method: Generated headwear/hair edits fitted with an 8px feathered mask. The reference lower face, neck, coveralls, hands, legs and boots are preserved, with a soft brim shadow on the forehead. Helmet outlines are kept intact and stay within their original cells.

</details>

<!-- ART-PASS-2 -->
## Art pass 2

Published through stage 2: 39 new PNGs. Stage 1 contains 27 individual upgrade icons in `icons/` and the opaque app icon in `app-icon/`. Stage 2 adds five opaque 2×2 block sheets and six transparent ore overlays in `blocks/`.

Every image used these four style references: [approved miner](miner-four-poses-v1.png), [Big Bertha body](machines/machine-big-bertha-body-v1.png), [mole courier](moles/mole-four-frames-v2.png), and [yellow hard hat](hats/hat-yellow-hardhat-v2.png).

The icons were checked at 48 px on white, dark and earth backgrounds; the app icon at 60 px. It is fully opaque with square corners, and its face stays inside the central 80%. No text appears in the new artwork. Repeated hands have the requested three or five ghost copies, and the epic tap glove is gold. Wide-gap icon sheets were attempted and rejected; the individual icon files require no sheet cutting.

The normal 1024 px canvases were requested. Imagegen returned native dimensions recorded below, including 1254 px square assets. These original PNGs are preserved byte for byte, without resizing, hand painting, text removal, seam repair or alpha cleanup. Every prompt used, including rejected attempts, is in [art-prompts.txt](art-prompts.txt) and [manifest.json](manifest.json); the manifest also records per-image alpha checks, hashes and review notes.

Each block sheet holds four equally coloured material variants. Use its manifest crop rectangles to exclude grey gutters, then scale each tile to 24 px. Ore overlays were checked at 24 px over all five materials; the single emerald-green super crystal differs from the pale-cyan diamond cluster in both hue and shape.

The original approved miner and earlier assets remain intact. These checks cover standalone asset previews; the game integration and playtest happen in the game repository.

| File | Native dimensions | Background | Preview |
| --- | --- | --- | --- |
| [icons/icon-tap.png](icons/icon-tap.png) | 1254 × 1254 | Transparent | 48 px |
| [icons/icon-digger.png](icons/icon-digger.png) | 1254 × 1254 | Transparent | 48 px |
| [icons/icon-moles.png](icons/icon-moles.png) | 1254 × 1254 | Transparent | 48 px |
| [icons/icon-foreman.png](icons/icon-foreman.png) | 1254 × 1254 | Transparent | 48 px |
| [icons/icon-refinery.png](icons/icon-refinery.png) | 1254 × 1254 | Transparent | 48 px |
| [icons/icon-sharpen.png](icons/icon-sharpen.png) | 1254 × 1254 | Transparent | 48 px |
| [icons/icon-finetune.png](icons/icon-finetune.png) | 1254 × 1254 | Transparent | 48 px |
| [icons/icon-quarryeff.png](icons/icon-quarryeff.png) | 1254 × 1254 | Transparent | 48 px |
| [icons/icon-finer.png](icons/icon-finer.png) | 1254 × 1254 | Transparent | 48 px |
| [icons/icon-more.png](icons/icon-more.png) | 1254 × 1254 | Transparent | 48 px |
| [icons/icon-generator.png](icons/icon-generator.png) | 1254 × 1254 | Transparent | 48 px |
| [icons/icon-quarry.png](icons/icon-quarry.png) | 1254 × 1254 | Transparent | 48 px |
| [icons/icon-research.png](icons/icon-research.png) | 1254 × 1254 | Transparent | 48 px |
| [icons/icon-r-offline.png](icons/icon-r-offline.png) | 1254 × 1254 | Transparent | 48 px |
| [icons/icon-r-special.png](icons/icon-r-special.png) | 1254 × 1254 | Transparent | 48 px |
| [icons/icon-r-autogen.png](icons/icon-r-autogen.png) | 1254 × 1254 | Transparent | 48 px |
| [icons/icon-r-army.png](icons/icon-r-army.png) | 1254 × 1254 | Transparent | 48 px |
| [icons/icon-r-tap3.png](icons/icon-r-tap3.png) | 1254 × 1254 | Transparent | 48 px |
| [icons/icon-r-tap5.png](icons/icon-r-tap5.png) | 1254 × 1254 | Transparent | 48 px |
| [icons/icon-r-247.png](icons/icon-r-247.png) | 1254 × 1254 | Transparent | 48 px |
| [icons/icon-r-industrial.png](icons/icon-r-industrial.png) | 1254 × 1254 | Transparent | 48 px |
| [icons/icon-r-bargain.png](icons/icon-r-bargain.png) | 1254 × 1254 | Transparent | 48 px |
| [icons/icon-e-super.png](icons/icon-e-super.png) | 1254 × 1254 | Transparent | 48 px |
| [icons/icon-e-tap.png](icons/icon-e-tap.png) | 1254 × 1254 | Transparent | 48 px |
| [icons/icon-e-laser.png](icons/icon-e-laser.png) | 1254 × 1254 | Transparent | 48 px |
| [icons/icon-e-mole.png](icons/icon-e-mole.png) | 1254 × 1254 | Transparent | 48 px |
| [icons/icon-e-quarry.png](icons/icon-e-quarry.png) | 1254 × 1254 | Transparent | 48 px |
| [app-icon/app-icon-v1.png](app-icon/app-icon-v1.png) | 1254 × 1254 | Opaque | 60 px |
| [blocks/blocks-topsoil.png](blocks/blocks-topsoil.png) | 1254 × 1254 | Opaque | 24 px |
| [blocks/blocks-caves.png](blocks/blocks-caves.png) | 1254 × 1254 | Opaque | 24 px |
| [blocks/blocks-crystal.png](blocks/blocks-crystal.png) | 1254 × 1254 | Opaque | 24 px |
| [blocks/blocks-magma.png](blocks/blocks-magma.png) | 1254 × 1254 | Opaque | 24 px |
| [blocks/blocks-core.png](blocks/blocks-core.png) | 1254 × 1254 | Opaque | 24 px |
| [blocks/ore-coal.png](blocks/ore-coal.png) | 1254 × 1254 | Transparent | 24 px |
| [blocks/ore-copper.png](blocks/ore-copper.png) | 1254 × 1254 | Transparent | 24 px |
| [blocks/ore-silver.png](blocks/ore-silver.png) | 1254 × 1254 | Transparent | 24 px |
| [blocks/ore-gold.png](blocks/ore-gold.png) | 1254 × 1254 | Transparent | 24 px |
| [blocks/ore-diamond.png](blocks/ore-diamond.png) | 1254 × 1254 | Transparent | 24 px |
| [blocks/ore-super.png](blocks/ore-super.png) | 1254 × 1254 | Transparent | 24 px |
