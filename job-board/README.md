# Job Board artwork

Artwork for [JOB_BOARD_DESIGN.md](https://github.com/brockrichardson1234-max/dirt-inc-rebuild/blob/ca0a7e37313c1af904294f478fa61f12c885de94/docs/JOB_BOARD_DESIGN.md), read from `claude/save-and-tap-feel` at `ca0a7e37313c1af904294f478fa61f12c885de94`.

[Contact sheet](contact-sheet.png) · [Manifest](manifest.json) · [Small-size reviews](review/) · [Generation prompts and selection notes](generation-log.json) · [Validation](qa.json)

59 deliverable assets, each in two formats: 55 transparent RGBA PNGs and 4 opaque Herald JPGs, plus 59 lossless WebPs. The contact sheet and review composites are opaque documentation images, not game sprites. All production artwork was made with imagegen; export processing separates sheet cells, excludes neighboring sprites, uniformly downsamples, places sprites on shared transparent canvases, and encodes the requested formats. No game code or existing art was changed.

| Category | Files | Size | Count |
| --- | --- | --- | --- |
| Client stamps | `clients/stamp-{client}.png` / `.webp` | 256 × 256 | 10 |
| Camp construction / finished | `camp/{client}-a.png`, `camp/{client}-b.png` / `.webp` | 440 × 440 | 20 |
| Gold Crate, closed / open | `crates/gold-crate-{state}-{size}.png` / `.webp` | 128 × 128 and 256 × 256 | 4 |
| Reputation shields | `reputation/{rank}.png` / `.webp` | 256 × 256 | 7 |
| Rush, Big Job, Idle | `icons/job-{rush,big,idle}.png` / `.webp` | 128 × 128 | 3 |
| PAID stamp | `ui/paid.png` / `.webp` | 400 × 200 | 1 |
| Job Board menu tile | `icons/job-board.png` / `.webp` | 128 × 128 | 1 |
| County Dam stages | `weekly/county-dam-{1,2,3,4}.png` / `.webp` | 780 × 240 | 4 |
| Millbrook Rail Bridge stages | `weekly/millbrook-rail-bridge-{1,2,3,4}.png` / `.webp` | 780 × 240 | 4 |
| Herald photographs | `herald/{dam-opening,bridge-ribbon-cutting,crew-group,hollis-handshake}.jpg` / `.webp` | 768 × 512 | 4 |
| Empty company sign | `camp/sign-empty.png` / `.webp` | 400 × 160 | 1 |

The client IDs match the design: `rail`, `steel`, `dam`, `diner`, `icecream`, `phone`, `lumber`, `brick`, `farm`, `radio`. Rank IDs are `greenhorn`, `hand`, `regular`, `trusted`, `foremans-pick`, `master`, `legend`.

## Placement

Keep the complete canvases. Camp building anchors are **(220, 424)** on 440 × 440 canvases; weekly structure anchors are **(390, 226)** on 780 × 240 canvases. Coordinates use a bottom-edge ground line. Each A/B pair and each weekly sequence uses a common uniform scale. Transparent headroom is intentional, particularly on unfinished stages. The 400 × 160 sign is separate from the building canvas convention.

Stage A is construction and stage B is finished. Dam stages are foundation, half wall, full wall, and finished with water. Bridge stages are pilings, frame, deck, and finished with a train. Water belongs only to the final dam stage; the train belongs only to the final bridge stage.

The gold crates share one source-to-output scale within each resolution. The 128px versions are separately downsampled from the generated artwork. Their star, brass fittings and contained warm light distinguish them from normal gear crates. The open crate has no lid or visible reward item.

Client emblems use two pigments, cream and brown, with antialiasing and restrained print texture. All other sprites use the existing warm-brown outlines, upper-left lighting, cream/teal/red/copper/brass palette and painted grain. Distant landmarks intentionally have paler outlines and lower contrast. Herald panels use the existing sepia halftone treatment and the narrator's white hair, curled moustache and suit. They contain no headlines or captions.

The game supplies client names, rank names, company title and newspaper copy. The sign and notes are blank. `PAID` is the only baked-in lettering. Big Job uses a large single crane hook to remain readable at 32px.

## Review and remaining reservations

Every delivered asset was inspected in the labeled contact sheet and small-size composites: stamps at 36px, badges and job/menu/crate icons at 32px, camp stages at 110px, weekly stages at 390px wide, and Herald panels at 240px wide. UI and camp sprites were reviewed on cream, dark teal and earth backgrounds; weekly landmarks on cream and dark teal. The blank sign and PAID stamp were also reviewed at reduced sizes. Each WebP is lossless and has the same decoded RGBA pixels as its PNG or JPG counterpart.

The first Big Job sheet clipped its chain; a second hook-and-crate version remained too spindly at 32px. Both were replaced with the large single hook. The first dam foundation looked too complete and was regenerated lower. The landmarks received a separate distance/palette pass. Adjacent sheet fragments were excluded during camp sprite extraction. The PAID stamp received a final imagegen pass to replace pale opaque distress flecks with clean red ink and transparent chips.

Remaining reservations:

- Construction and finished images are discrete illustrations, not pixel-registered animation frames. Some small details and positions change; the farm tractor moves from the right side in construction to the left in the finished scene. Use a state switch or crossfade.
- Saw teeth, telephone wires, scaffolding and train wheel details naturally soften at the review sizes. The major silhouettes remain clear. The train should stay a background detail.
- The Herald ceremony bridge/dam illustrations are matching editorial depictions, not exact renderings of the weekly construction sprites.

These checks are standalone art reviews. No game integration or gameplay tests were performed because this task changes only the art-pack repository.
