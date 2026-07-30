# Module Library

Use this library to select modules before compiling the final prompt. Do not paste the menu into the final prompt.

The module system expands quiet compositional choices; it does not turn the poster loud. Minimal zine style is locked by aged-paper negative-space dominance, a single small imaginable subject, quiet secondary typography, one high-saturation color spot, and print/scan materiality. Placement, exact subject, palette temperature, texture, and mood remain flexible.

When the user asks for more freedom, use modules as a boundary system: lock the emptiness, the single subject, the single spot, and the quiet type, then let the model vary the rest.

## Source Mode

- `text-theme`: user gives a word, concept, article topic, or title. Translate abstract ideas into one concrete quiet object.
- `sentence`: user gives one line or a fragment. Pull a single image out of it; keep the line as optional edge micro-text.
- `object`: user names a concrete thing. Reduce it to a small, quiet zine specimen on paper.
- `mood`: user gives a feeling, memory, or atmosphere. Choose a soft anchor and let the mood register steer palette and texture.
- `article-summary`: user gives article text for a cover. Extract one image; a single small subtitle line is allowed.
- `critique`: user asks whether samples match minimal zine style. Score against the quality gates, then repair.

## Core Image Inventory

Pick **one** subject. Abstract themes must be translated into a concrete item from this inventory (or something equally imaginable) before compiling.

The families exist to break the default gravity of this style, which otherwise collapses into leaf / photo / coin / boat forever. When generating a set, **每张必须来自不同家族**.

- `N 自然与季节`: pressed leaf, single seed pod, dandelion head, pine cone scale, dried flower stem, small stone, shell fragment, frost pattern on glass, cicada shell, sprig of grass.
- `O 日常器物`: chipped enamel mug, single key, empty matchbox, folded handkerchief, spool of thread, hairpin, small glass bottle, worn eraser, paper clip, safety pin, single chopstick, candle stub.
- `W 纸与文字`: torn ticket stub, faded photograph fragment, envelope corner with a stamp, page corner folded down, receipt curl, index card, postage stamp, library due-date slip, a single line of someone else's handwriting, ink blot.
- `B 身体与穿戴`: one loose button with thread, broken shoelace, folded sock, single glove, spectacle frame, a strand of hair, worn shirt cuff, thumbprint in ink, small bandage.
- `L 光影与天气`: a parallelogram of window light on floor, one cast shadow of an unseen object, a single raindrop track on glass, breath fog patch, a lens flare disc, dust motes in a light shaft, snow speck cluster.
- `T 工具与机械`: bent nail, screw, sewing needle, single gear, pencil stub, ruler fragment, tuning fork, cassette tape spool, light bulb filament, wire twist, unbent paper clip.
- `F 食物与残留`: peach pit, single grain of rice, tea leaf at cup bottom, orange peel spiral, half an eggshell, cherry stem knot, crumb trail, sugar cube, bread crust corner.
- `A 动物痕迹`: single feather, bird footprint, cat whisker, snail shell, moth wing, fish scale, empty nest fragment, insect specimen pin.
- `S 建筑与空间碎片`: a small window shape, one doorframe corner, single stair step, crack in a wall, tile fragment, a distant chair silhouette, ladder rung, keyhole.
- `G 几何与符号`: a solitary circle, one crossed-out mark, an arrow drawn once, a seal or stamp impression, a single tally line group, an ellipsis of three dots, a torn-off corner shape, a lone bracket.

Scale rule: the chosen subject occupies **12-25%** of the frame and must read clearly at thumbnail size. Quiet does not mean invisible — a subject so small or so pale that it disappears is a failure, not a success.

Weak core images (translate these into an inventory item first): growth, connection, freedom, intelligence, transformation, focus, burnout, clarity.

## Layout Families

- `L1 single specimen`: one tiny subject alone in a huge empty field; maximum negative space.
- `L2 low-left drift`: subject rests low and to one side, large calm space above.
- `L3 top-right block`: a small block or fragment sits high in one corner.
- `L4 twin panel`: two quiet fragments in loose dialogue across mostly empty paper.
- `L5 irregular crop`: subject partly cropped by the paper edge, entering and leaving quietly.
- `L6 type-led`: sparse fragmentary type carries the frame; the image is a whisper.
- `L7 dot orbit`: a few small marks or dots orbit a central void.
- `L8 centered island`: one small subject floats slightly off dead-center in stillness.

## Anchor Treatment

- `A1 faded photograph`: a small washed-out photo fragment, edges soft, half-remembered.
- `A2 torn-paper cutout`: a hand-torn paper shape with visible fibrous edge.
- `A3 flat silhouette`: a single clean flat silhouette, no rendering.
- `A4 small color block`: one quiet rectangle or shape of muted color (not the saturated spot).
- `A5 old print engraving`: a small antique-engraving-style motif, line-based, archival.
- `A6 plain object`: one simplified everyday object drawn quietly, minimal shading.
- `A7 translucent geometry`: a semi-transparent pane, circle, or overlap of soft shapes.
- `A8 texture window`: a small rectangular window revealing a different paper texture or scan.
- `A9 ink brush mark`: the subject drawn in one or two confident sumi-ink strokes, wet edges visible.
- `A10 rubbing / seal impression`: the subject rendered as a pressed rubbing or stamped seal, uneven ink coverage.
- `A11 line diagram`: the subject drawn as a thin technical line study, like a page from an old manual.
- `A12 attached object`: the subject taped, pinned, stitched, or clipped onto the paper, the attachment visible.

## Typography Behavior

- `T1 fragment letters`: a few isolated letters or a broken word, quiet and incidental.
- `T2 edge-hugging micro-text`: one small line pinned to a margin or edge.
- `T3 archival caption`: tiny typewriter/mono caption, like a museum tag or archive stamp.
- `T4 diagonal scatter`: characters scattered lightly on a gentle diagonal.
- `T5 ghost type`: type faded almost into the paper, barely readable.
- `T6 rough small title`: one modest hand or serif title, still clearly secondary to the space.
- `T7 in-block text`: small text set inside a muted block or the texture window.
- `T8 minimal title`: one restrained short title in the margin; nothing else.
- `T9 Chinese quiet title`: exact Chinese characters (usually 2-4), set small as quiet serif/typewriter lettering; edge-set or beside the subject. Use when the title should stay a whisper.
- `T10 one-line subtitle`: one small explanatory or archival line, clearly secondary; Chinese 6-12 chars, English 2-6 words; sits in a lower margin, corner tag, faint band, or beside the subject.
- `T11 大字中文手写标题`: **the default whenever a Chinese title or a cover title is wanted.** Exact Chinese characters (best at 2-5), written by hand in ink brush, fountain pen, or soft pencil — visible stroke entry and exit, slight irregularity, real handwriting rather than a computer script font. Character height is roughly 10-18% of the canvas height, so the title reads instantly at thumbnail size and clearly outweighs any caption. It stays a handwritten mark on paper, not a printed display headline: no heavy black poster type, no outlined or filled logo lettering.
- `T12 handwritten Latin title`: same treatment for English titles — hand-lettered, medium-large, legible, ink-textured, never a typeset display headline.

Title legibility rule: a title that dissolves into the paper is a defect. Ghosting and fragmentation (`T5`, `T1`) apply to incidental text, never to the main title.

## Color Spot Behavior

Exactly one saturated hue, ~0.8-2.5% of the canvas, against paper / muted / near-monochrome. Choose the hue by mood, not from a fixed palette.

- `C1 vermilion spot`: warm urgent red-orange point; strong against cream paper.
- `C2 cobalt spot`: cool deep blue point; quiet melancholy.
- `C3 marigold spot`: saturated yellow-orange; summer, afternoon, childhood.
- `C4 acid green spot`: sharp green; mild surreal, modern zine edge.
- `C5 magenta/pink spot`: vivid pink point; memory, tenderness.
- `C6 theme-derived spot`: pull one saturated hue from the subject or uploaded image.
- The rest of the frame stays aged paper, ink black/brown, and low-saturation grays. Never a second saturated hue, never a saturated field.

## Texture Modules

- `P1 risograph softness`: soft riso ink, slight misregistration, grainy fill.
- `P2 photocopy`: high-contrast xerox grain, dust, toner flecks.
- `P3 halftone degradation`: visible dot screen, slightly broken.
- `P4 silkscreen bleed`: screen-print edges that bleed lightly into paper.
- `P5 film grain`: fine photographic grain over the paper.
- `P6 letterpress impression`: pressed ink with slight debossed edge.
- `P7 aged-paper mottling`: foxing, stains, uneven scanned old-paper tone.
- `P8 pencil gray`: light pencil shading, smudge, eraser ghosts.

## Mood Register

Pick one; let it steer palette temperature, texture, and subject.

- `M1 stillness` · `M2 summer` · `M3 solitude` · `M4 childhood` · `M5 seaside` · `M6 afternoon` · `M7 night` · `M8 memory` · `M9 mild surreal`

## Selection Heuristics

- One word / one sentence -> L1/L8 + A3/A6 + T2/T5 + P2/P7 + one restrained spot + M1/M3.
- Mood / memory / essay -> L2/L5 + A1/A7/A8 + T3/T5 + P1/P5/P7 + low-saturation spot + M3/M8.
- Article cover (needs a cue) -> L2/L6 + A1/A2/A6 + add T10 subtitle + P1/P3 + spot from theme + fitting mood.
- Concrete object -> L5/L8 + A3/A6 + T1/T8 + P2/P6 + theme-derived spot + M1.
- Chinese title requested -> use T11 大字中文手写标题, keep the exact characters, and choose a layout that leaves one clear open field for the handwriting so the paper still dominates around it.
- Uploaded image -> reduce to A1/A3/A6 specimen, strip original scene, keep silhouette, add one small spot and paper texture.
- Summer / childhood / seaside mood -> C3 or C5 spot, P1/P5 texture, softer warm paper.
- Night / solitude / mild surreal -> C2 or C4 spot, P2/P7 texture, cooler muted paper.

## Freedom Mode

Use when the user wants freer, less formulaic, more varied output.

Keep fixed:

- 70-80% aged-paper negative space
- one imaginable subject or tight cluster at 12-25% of the frame, legible at thumbnail size
- one high-saturation color spot (~1.5-2.5% of frame), placed on or touching the subject
- typography that is secondary in quantity but legible in fact; a handwritten main title may be medium-large
- print/scan paper materiality
- exact main title text if the user specifies it

Allow variation:

- which subject / object metaphor, when the user does not specify one
- exact subject placement, scale, and crop
- typography position, fragmentation, and subtitle presence
- layout and mood register
- the single spot's hue
- texture module

## Variation Rule

When generating a set, every image must draw its core image from a **different family in the Core Image Inventory**, and at least three of these must also differ:

- layout family
- anchor treatment
- typography behavior
- texture module
- color spot hue
- mood register

This prevents every result from becoming the same empty poster with a different tiny object. A set of five paper-and-botanical specimens is a failed set even if the layouts differ.
