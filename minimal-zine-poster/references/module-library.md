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

## Typography Behavior

- `T1 fragment letters`: a few isolated letters or a broken word, quiet and incidental.
- `T2 edge-hugging micro-text`: one small line pinned to a margin or edge.
- `T3 archival caption`: tiny typewriter/mono caption, like a museum tag or archive stamp.
- `T4 diagonal scatter`: characters scattered lightly on a gentle diagonal.
- `T5 ghost type`: type faded almost into the paper, barely readable.
- `T6 rough small title`: one modest hand or serif title, still clearly secondary to the space.
- `T7 in-block text`: small text set inside a muted block or the texture window.
- `T8 minimal title`: one restrained short title in the margin; nothing else.
- `T9 Chinese quiet title`: exact Chinese characters (usually 2-4), set as quiet serif/typewriter/hand lettering; may be small, edge-set, ghosted, or beside the subject. Never a bold dominant headline.
- `T10 one-line subtitle`: one small explanatory or archival line, clearly secondary; Chinese 6-12 chars, English 2-6 words; sits in a lower margin, corner tag, faint band, or beside the subject.

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
- Chinese title requested -> add T9, keep exact characters, choose a layout where the paper space stays dominant around them.
- Uploaded image -> reduce to A1/A3/A6 specimen, strip original scene, keep silhouette, add one small spot and paper texture.
- Summer / childhood / seaside mood -> C3 or C5 spot, P1/P5 texture, softer warm paper.
- Night / solitude / mild surreal -> C2 or C4 spot, P2/P7 texture, cooler muted paper.

## Freedom Mode

Use when the user wants freer, less formulaic, more varied output.

Keep fixed:

- 70-90% aged-paper negative space
- one small imaginable subject or tight cluster
- one high-saturation color spot (~1-2% of frame)
- quiet secondary serif/typewriter/mono/hand typography
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

When generating a set, vary at least three of:

- core image / subject
- layout family
- anchor treatment
- typography behavior
- texture module
- color spot hue
- mood register

This prevents every result from becoming the same empty poster with a different tiny object.
