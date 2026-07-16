# Module Library

Use this library to select modules before compiling the final prompt. Do not paste the menu into the final prompt.

The module system should expand compositional choices, not over-restrict them. Plakatstil is locked by commercial object logic, hand-painted lettering, hand-painted object treatment, and paper/ink materiality. Color, layout, lettering placement, and background decoration remain flexible.

When the user asks for more freedom, use modules as a boundary system, not a fixed recipe. Lock the single-object ad logic and hand-painted paper materiality, then allow the image model to vary composition, crop, title placement, subtitle use, palette, and background treatment.

## Source Mode

- `text-theme`: user gives a word, concept, product name, article topic, or title. Translate abstract ideas into a concrete ad object.
- `product-photo`: user uploads a product, tool, object, gadget, shoe, bottle, food, book, or device. Preserve object identity and simplify into a hand-painted product hero.
- `package-photo`: user uploads packaging, label, box, bottle, tin, wrapper, or branded object. Let packaging typography become part of the poster.
- `portrait-service`: user uploads a person or asks for a personal/service poster. Treat as Plakatstil-inspired service, performer, lecture, craft, or personal-brand poster.
- `critique`: user asks whether samples match Plakatstil. Score with `evaluation-rubric.md`, then repair.

## Subject Treatment

- `H1 sparse flat object`: matches, cigarettes, pencils, keys, switches, wireless earbuds, simple tools. Few shapes, strong silhouette, minimal rendering.
- `H2 semi-rendered glass/metal`: bulbs, bottles, smartwatch, Sony camera lens, chrome, polished objects. Hand-painted highlights and simplified dimensionality; never photoreal.
- `H3 package/label hero`: soap, coffee, shoe polish, tea, medicine, perfume box, wrappers. Package label participates.
- `H4 cropped product macro`: boots, bags, tools, cameras, keyboard, smartphone, laptop. Product fills the frame and may be cropped.
- `H5 diagonal product hero`: long objects or directional forms: shoe, bottle, pen, lamp, cable, tube.
- `H6 product + action hand`: switch, lighter, razor, brush, stamp, camera shutter, tool use. Product remains the hero.
- `H7 portrait/service poster`: people, courses, performers, creators, consultants. Simplified portrait plus one trade object.
- `H8 hand-painted dimensional object`: object has volume and shadow, but all highlights, contours, and color transitions are visibly painted.

## Typography Behavior

- `T1 large hand-cut brand word`: big, rough, painted, irregular.
- `T2 object over brand word`: object overlaps or partly hides the brand name.
- `T3 packaging typography`: text exists on packaging and background.
- `T4 split word layout`: letters or words split across fields, bands, blocks, or empty space.
- `T5 text mostly on product`: package or label carries the main text.
- `T6 expressive but not comic`: energetic commercial lettering, not rock-band, manga, pulp, or superhero title.
- `T7 minimal wordmark`: only one short hand-painted word, integrated with the object and background.
- `T8 Chinese hand-painted title`: exact Chinese title characters, usually 2-4 characters, drawn as custom hand-painted commercial display lettering; can be angular, soft, blocky, brush-filled, cut-paper-like, split, hidden behind the object, or printed on packaging.
- `T9 one-line small subtitle`: one small explanatory or action-oriented subtitle line, clearly secondary to the main title; can sit on a paper band, label strip, product label, lower margin, corner tag, or quiet color block. Chinese usually 6-12 characters; English usually 2-6 words.

## Layout Families

- `L1 sparse negative-space field`: Priester-like object/word relationship.
- `L2 object over large brand`: Osram-like object over brand word.
- `L3 horizontal color bands`: muted stripes behind the object and brand word.
- `L4 diagonal hero crop`: boots, tools, tubes, brushes, pens, bottles, cables.
- `L5 package close-up`: wrapper, label, tin, box, bag, or package surface is the selling plane.
- `L6 framed worn poster`: printed border and worn edge support old-paper materiality.
- `L7 split field`: brand text and product sit across two color planes.
- `L8 corner/edge crop`: product enters from one edge and leaves large poster space.
- `L9 decorative stripe field`: horizontal or vertical stripes, bands, or simple printed rules decorate the background.
- `L10 color-block poster`: large hand-painted color blocks support object and lettering.
- `L11 pattern-backed object`: simple repeated motifs, dots, label fragments, or packaging-derived pattern behind the object.
- `L12 text-on-object composition`: text sits directly on the object, label, package, tag, or product surface.

## Background Families

- `B1 dark flat field`: black, brown-black, blue-black, tobacco black.
- `B2 cream/aged paper field`: warm paper with black ink and muted product color.
- `B3 color bands`: muted blue, tobacco green, ochre, rust, dull red, cream.
- `B4 package-derived field`: background echoes wrapper, tin, box, or label colors.
- `B5 border-led field`: subtle worn border, printed margin, imperfect poster edge.
- `B6 decorative stripe field`: hand-painted stripes or bands used as visual decoration.
- `B7 color-block field`: large blocks, split fields, rectangles, or planes of color.
- `B8 simple pattern field`: dots, waves, small geometric motifs, product fragments, or repeated label-like marks.
- `B9 plain open field`: no decoration; object and hand-painted word carry the image.

## Color Behavior

Do not select from a fixed palette by default. Choose freely based on object, theme, uploaded image, or reference mood.

- `C1 black/red/yellow`: match, warning, small hard goods, simple punch.
- `C2 dark/blue/rust/yellow`: bulb, glass, lens, technical object.
- `C3 brown/cream/ochre/muted red`: shoes, leather, soap, paper, coffee, craft objects.
- `C4 product-derived limited palette`: reduce uploaded image colors to 3-5 ink colors.
- `C5 cream paper + black ink`: strong silhouette and old printed label feel.
- `C6 packaging label palette`: visible package colors become muted lithographic inks.
- `C7 free hand-painted palette`: choose any colors that make the object and word memorable while staying hand-painted and paper-based.

## Texture Modules

- `P1 paper fiber`: visible fibers under flat ink.
- `P2 ink absorption`: edges bleed lightly into paper.
- `P3 lithographic misregistration`: small color shifts at edges.
- `P4 hand-painted contours`: uneven brush contours and filled shapes.
- `P5 worn printed border`: old poster edge and rubbed corners.
- `P6 matte ink surface`: no glossy digital finish.
- `P7 uneven hand-painted color`: slight color variation inside filled areas; no perfectly clean vector fill.
- `P8 painted highlight / shadow`: dimensionality made from painted shapes, not photo rendering.

## Selection Heuristics

- Matches, cigarettes, pencils, simple sticks -> H1 + T1/T7 + L1/L9 + B1/B3 + C1/C7.
- Wireless earbuds, keys, switches, small gadgets -> H1 + T2/T4/T7 + L1/L2 + B1/B2 + C3/C7.
- Glass bulb, bottle, smartwatch, Sony camera lens -> H2/H8 + T2 + L2/L3/L8 + B3/B7 + C2/C7.
- Soap, Starbucks coffee bag, shoe polish tin, wrapper, label -> H3 + T3/T5 + L5 + B4 + C3/C6.
- Chinese title requested -> add T8, keep the exact characters, and choose a layout where the object can overlap, split, frame, or carry the characters.
- Article cover with an explanatory or save/click cue -> add T9, generate one short subtitle line from the article theme, and keep it visibly smaller than the main title.
- Shoe, boot, keyboard, tools, Anker PowerCore, laptop -> H4/H5/H8 + T1/T4/T6 + L4/L7/L10 + B1/B2/B7 + C3/C7.
- Hand using product -> H6 + T1/T2 + L4/L8/L10 + B1/B2/B3 + C1/C7.
- Portrait/person/service -> H7 + T1/T4/T6 + L7/L10 + B1/B2/B7 + C4/C7.
- Abstract concept -> choose an object metaphor first, then use the matching object heuristic.

## Freedom Mode

Use this when the user says the output should be freer, less fixed, more varied, or less formulaic.

Keep fixed:

- one concrete object or one concrete object metaphor
- exact main title if user specifies it
- Plakatstil / Sachplakat commercial object logic
- hand-painted typography
- paper, ink, and uneven painted texture
- at most one small subtitle line

Allow variation:

- object metaphor, when the user does not specify an object
- object angle, crop, scale, and placement
- title shape, direction, stacking, split, overlap, and position
- subtitle presence and subtitle placement
- background family
- palette and contrast behavior
- decorative marks, borders, bands, rays, waves, labels, or empty space

## Variation Rule

When generating a set, vary at least three of:

- object metaphor
- layout family
- background family
- typography behavior
- subject treatment
- color behavior
- subtitle presence or placement

This prevents every result from becoming the same poster with a different object.
