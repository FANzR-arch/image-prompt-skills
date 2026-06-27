# Module Library

Use this library to select modules before compiling the final prompt. Do not paste the menu into the final prompt.

## Source Mode

- `text-theme`: user gives a word, concept, product name, article topic, or title. Translate abstract ideas into a concrete ad object.
- `product-photo`: user uploads a product, tool, object, gadget, shoe, bottle, food, book, or device. Preserve object identity and simplify into a hand-painted product hero.
- `package-photo`: user uploads packaging, label, box, bottle, tin, wrapper, or branded object. Let packaging typography become part of the poster.
- `portrait-service`: user uploads a person or asks for a personal/service poster. Treat as Plakatstil-inspired service, performer, lecture, craft, or personal-brand poster.
- `critique`: user asks whether samples match Plakatstil. Score with `evaluation-rubric.md`, then repair.

## Subject Treatment

- `H1 sparse flat object`: matches, cigarettes, pencils, keys, switches, wireless earbuds, simple tools. Few shapes, strong negative space, flat silhouette.
- `H2 semi-rendered glass/metal`: bulbs, bottles, smartwatch, Sony camera lens, chrome, polished objects. Hand-painted highlights and simplified realism.
- `H3 package/label hero`: soap, coffee, shoe polish, tea, medicine, perfume box, wrappers. Package label participates.
- `H4 cropped product macro`: boots, bags, tools, cameras, keyboard, smartphone, laptop. Product fills the frame and may be cropped.
- `H5 diagonal product hero`: long objects or directional forms: shoe, bottle, pen, lamp, cable, tube.
- `H6 product + action hand`: switch, lighter, razor, brush, stamp, camera shutter, tool use. Product remains the hero.
- `H7 portrait/service poster`: people, courses, performers, creators, consultants. Simplified portrait plus one trade object.

## Typography Behavior

- `T1 large hand-cut brand word`: big, rough, painted, irregular.
- `T2 object over brand word`: object overlaps or partly hides the brand name.
- `T3 packaging typography`: text exists on packaging and background.
- `T4 small product descriptor`: one small product word, often muted red, cream, or blue.
- `T5 text mostly on product`: package or label carries the main text.
- `T6 expressive but not comic`: energetic commercial lettering, not rock-band, manga, pulp, or superhero title.

## Layout Families

- `L1 sparse negative-space field`: Priester-like object/word relationship.
- `L2 object over large brand`: Osram-like object over brand word.
- `L3 horizontal color bands`: muted stripes behind the object and brand word.
- `L4 diagonal hero crop`: boots, tools, tubes, brushes, pens, bottles, cables.
- `L5 package close-up`: wrapper, label, tin, box, bag, or package surface is the selling plane.
- `L6 framed worn poster`: printed border and worn edge support old-paper materiality.
- `L7 split field`: brand text and product sit across two color planes.
- `L8 corner/edge crop`: product enters from one edge and leaves large poster space.

## Background Families

- `B1 dark flat field`: black, brown-black, blue-black, tobacco black.
- `B2 cream/aged paper field`: warm paper with black ink and muted product color.
- `B3 color bands`: muted blue, tobacco green, ochre, rust, dull red, cream.
- `B4 package-derived field`: background echoes wrapper, tin, box, or label colors.
- `B5 border-led field`: subtle worn border, printed margin, imperfect poster edge.

## Palette Families

- `C1 black/red/yellow`: match, warning, small hard goods, simple punch.
- `C2 dark/blue/rust/yellow`: bulb, glass, lens, technical object.
- `C3 brown/cream/ochre/muted red`: shoes, leather, soap, paper, coffee, craft objects.
- `C4 product-derived limited palette`: reduce uploaded image colors to 3-5 ink colors.
- `C5 cream paper + black ink`: strong silhouette and old printed label feel.
- `C6 packaging label palette`: visible package colors become muted lithographic inks.

## Texture Modules

- `P1 paper fiber`: visible fibers under flat ink.
- `P2 ink absorption`: edges bleed lightly into paper.
- `P3 lithographic misregistration`: small color shifts at edges.
- `P4 hand-painted contours`: uneven brush contours and filled shapes.
- `P5 worn printed border`: old poster edge and rubbed corners.
- `P6 matte ink surface`: no glossy digital finish.

## Selection Heuristics

- Matches, cigarettes, pencils, simple sticks -> H1 + T1 + L1 + B1 + C1.
- Wireless earbuds, keys, switches, small gadgets -> H1 + T2 or T4 + L1/L2 + B1/B2 + C3/C4.
- Glass bulb, bottle, smartwatch, Sony camera lens -> H2 + T2 + L2/L3/L8 + B3 + C2/C4.
- Soap, Starbucks coffee bag, shoe polish tin, wrapper, label -> H3 + T3/T5 + L5 + B4 + C3/C6.
- Shoe, boot, keyboard, tools, Anker PowerCore, laptop -> H4/H5 + T1/T4 + L4/L7 + B1/B2 + C3/C4.
- Hand using product -> H6 + T1 + L4/L8 + B1/B2 + C1/C3.
- Portrait/person/service -> H7 + T1 + L7 + B1/B2 + C4.

## Variation Rule

When generating a set, vary at least two of:

- layout family
- background family
- typography behavior
- subject treatment
- palette family

This prevents every result from becoming the same poster with a different object.
