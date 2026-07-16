# Compile Contract

## Core Rule

The skill may think in modules, but the final prompt must be resolved. Do not output raw choices unless the user explicitly asks for a reusable template.

Resolved does not mean over-specified. The final prompt must lock the object, main title, style logic, materiality, and negative constraints. It may deliberately leave controlled freedom for composition, title placement, subtitle use, background treatment, and color palette when the user wants exploratory or more varied results.

There are two valid output modes:

- **Resolved prompt mode**: default. Use when the user gives a concrete theme, product photo, package photo, portrait, or object. The output should contain no placeholders.
- **Reusable template mode**: use only when the user asks for a copy-ready template, article prompt block, reusable prompt structure, or similar. In this mode, put editable Chinese input fields first and fixed English style instructions after them.

Wrong:

```text
Use black / brown / blue background. Put the object above or behind text.
```

Right:

```text
Use one concrete glass bulb as the product hero. Let the image model choose the strongest Plakatstil composition: the bulb may be diagonal, cropped, centered, or edge-entering; the title may sit behind, beside, on, or partly under the bulb; background may use color bands, a dark field, or large color blocks. Keep one dominant object, readable hand-painted title, and visible paper texture across the whole image.
```

## Final Prompt Structure

Use this order:

```text
SOURCE / INPUT:
ASPECT RATIO:
AD OBJECT:
STYLE LOCK:
SUBJECT TREATMENT:
TYPOGRAPHY:
SMALL SUBTITLE:
LAYOUT + BACKGROUND:
COLOR + PAINT:
PAPER / INK TEXTURE:
CONTROLLED FREEDOM:
AVOID:
QUALITY CHECK:
```

## Reusable Template Structure

Use this structure only when the user explicitly wants a reusable prompt block. Keep the editable fields in Chinese and the fixed style instructions in English. Do not add extra label lines such as “你只需要改这里” or “以下内容不用改”.

Text-to-image article cover template:

```text
文章主题或摘要：
{输入文章主题、标题、摘要，或直接粘贴文章内容}

用途和比例：
{例如：文章封面，横版 5:2}

指定主标题文字：
{可选；没有就写：自动判断}

指定副标题文字：
{可选；没有就写：自动判断或不加}

特殊要求：
{指定物体、颜色、不能出现的元素；没有就写：无}

Create an AI article cover from the text theme above.

Style lock:
early 20th-century German Plakatstil / Sachplakat advertising poster, hand-painted commercial object poster, one concrete commercial object, simplified but recognizable product hero, custom hand-painted advertising lettering, matte printed paper, visible paper grain, ink absorption, uneven hand-painted color coverage.
```

Image-to-image product poster templates must start with `上传图片：` and preserve the uploaded object's identity. Image-to-image portrait templates must start with `上传图片：` and identify the result as a `Plakatstil-inspired` personal/service poster, not strict Sachplakat.

## Section Rules

### SOURCE / INPUT

State whether the image comes from a text theme, uploaded product photo, packaging photo, portrait/service theme, or critique task.

For uploaded images, preserve the object's identity, silhouette, main material, label hierarchy, distinctive details, and recognizable functional parts.

### ASPECT RATIO

Use the user-specified ratio exactly. If the user does not specify, choose the ratio that best serves the object and use case.

### AD OBJECT

Name one concrete commercial object. If the input is abstract, translate it into an object before writing the prompt.

Good objects:

- matchbox and two matches
- glass bulb
- black leather boot
- wrapped soap bar
- shoe polish tin
- wireless earbuds in a charging case
- compact mechanical keyboard
- smartwatch
- Starbucks coffee bag
- Sony camera lens
- Anker PowerCore power bank
- smartphone
- laptop computer

Weak objects:

- productivity
- search
- intelligence
- transformation
- unlock

### STYLE LOCK

Always include:

```text
early 20th-century German Plakatstil / Sachplakat advertising poster, hand-painted commercial object poster, simplified but recognizable product hero, custom hand-painted advertising lettering, matte printed paper, visible paper grain, ink absorption, uneven hand-painted color coverage
```

Do not lock the prompt into a fixed color palette, fixed layout, fixed typography position, or fixed background formula.

### SUBJECT TREATMENT

Choose one subject treatment from the module library. The subject may be flat, semi-rendered, cropped, label-led, package-led, or action-led.

### TYPOGRAPHY

Typography must be free in placement and form but fixed in nature:

- hand-painted commercial advertising lettering
- angular, blocky, irregular, soft, rounded, brush-painted, cut-paper-like, or rough-edged forms are all allowed
- may sit above, behind, beside, across color bands, on a label, on packaging, on the object, split across fields, or partly hidden by the product
- may include brand word, product word, package text, or a single short title word
- may use exact Chinese title characters when requested; Chinese title text should usually be 2-4 characters, drawn as custom hand-painted commercial display lettering, not a modern font
- if the user specifies exact title text, keep that text exactly; do not translate it, add random labels, invent fake Chinese characters, or add extra small copy beyond the one intentional subtitle line
- no modern clean type system, Helvetica, Swiss grid type, sterile vector logo, comic title, or rock-band lettering

Do not force every image into one big top title plus one small red subtitle.

### SMALL SUBTITLE

This section is optional but allowed for article covers, product posters, and portrait/service posters when it helps explain value or guide action.

Allowed subtitle behavior:

- one line only
- clearly smaller than the main title
- Chinese: usually 6-12 characters
- English: usually 2-6 words
- may sit on a small paper band, label strip, product label, lower margin, corner tag, or quiet color block
- must look hand-painted or printed as part of the same old advertising poster

### LAYOUT + BACKGROUND

Layout is not restricted. Choose a bounded layout field that fits the object. The final prompt can allow the image model to choose the strongest arrangement among compatible Plakatstil behaviors, as long as object clarity, title readability, and single-object ad logic remain intact.

Allowed directions:

- sparse object-and-word field
- object overlapping or hiding the word
- split text and object
- text printed on product or packaging
- diagonal hero crop
- product entering from an edge
- package close-up
- horizontal color bands
- large color blocks
- decorative stripes, printed borders, simple patterns, product-derived shapes
- plain dark field or plain paper field

### COLOR + PAINT

Do not restrict color by default. Choose colors freely from the theme, product, reference image, or desired poster mood. The important constraint is materiality: colors must feel like painted / lithographic inks on paper, with slight unevenness and absorption.

Good:

- black-brown, cream, ochre, muted red
- dark blue-black, dull cyan, rust, cream
- tobacco green, kraft ochre, dark brown, muted red
- cream paper field, black ink, muted red stamp

Avoid full rainbow, neon, glossy gradients, sterile modern color systems, or one mandatory palette for every theme.

### PAPER / INK TEXTURE

Make texture material, not decorative:

- paper fibers visible through ink
- pigment absorption
- slight lithographic misregistration
- worn printed edge
- matte ink
- hand-painted contours

Avoid heavy digital grunge unless the user asks for a damaged poster.

### CONTROLLED FREEDOM

Use this section to let the image model adapt only inside the chosen structure.

Good:

```text
Let the hand-painted letter shapes, title placement, subtitle use, object crop, background decoration, and palette adapt to the theme or uploaded image, but keep one dominant commercial object, at most one subtitle line, and the old hand-painted object-poster logic.
```

Bad:

```text
Use any layout, any background, any typography.
```

### AVOID

Always include relevant negatives:

```text
Avoid: clean vector icon, modern logo mockup, Helvetica, Swiss grid, Bauhaus geometry, sterile sans-serif typography, comic book title, rock-band lettering, cinematic poster lighting, photorealistic product render, glossy 3D, excessive digital grunge, crowded body copy, multiple subtitle lines, fake dates, fake URLs, random unreadable labels.
```

When Chinese title text is requested, also include:

```text
Avoid: English replacement text, fake Chinese characters, wrong title text, random extra labels, extra small copy beyond one intentional subtitle line.
```
