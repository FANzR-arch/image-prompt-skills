# Compile Contract

## Core Rule

The skill may think in modules, but the final prompt must be resolved. Do not output raw choices unless the user explicitly asks for a reusable template.

Wrong:

```text
Use black / brown / blue background. Put the object above or behind text.
```

Right:

```text
Use a deep brown-black background with a broad empty upper field. Place the cream hand-lettered brand word behind the glass bottle, partly hidden by the object.
```

## Final Prompt Structure

Use this order:

```text
SOURCE / INPUT:
AD OBJECT:
STYLE LOCK:
SUBJECT TREATMENT:
TYPOGRAPHY:
LAYOUT + BACKGROUND:
COLOR + PRINT:
PAPER / INK TEXTURE:
CONTROLLED FREEDOM:
AVOID:
QUALITY CHECK:
```

## Section Rules

### SOURCE / INPUT

State whether the image comes from a text theme, uploaded product photo, packaging photo, portrait/service theme, or critique task.

For uploaded images, preserve the object's identity, silhouette, main material, label hierarchy, and distinctive details.

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
early 20th-century German Plakatstil / Sachplakat advertising poster, simplified commercial object poster, hand-painted lithographic look, minimal copy, bold product silhouette, custom advertising lettering, matte printed paper
```

### SUBJECT TREATMENT

Choose one subject treatment from the module library. The subject may be flat, semi-rendered, cropped, label-led, package-led, or action-led.

### TYPOGRAPHY

Typography must be free in form but fixed in nature:

- custom painted advertising lettering
- irregular hand-cut or brush-painted edges
- may sit above, behind, beside, on a label, on packaging, or partly hidden by the product
- may include brand word, product word, or package text
- no modern clean type system

Do not force every image into one big top title plus one small red subtitle.

### LAYOUT + BACKGROUND

Choose one layout family and write it as a resolved decision. Do not say "choose any layout."

### COLOR + PRINT

Use a limited ink palette selected for the object.

Good:

- black-brown, cream, ochre, muted red
- dark blue-black, dull cyan, rust, cream
- tobacco green, kraft ochre, dark brown, muted red
- cream paper field, black ink, muted red stamp

Avoid full rainbow, neon, glossy gradients, or one mandatory palette for every theme.

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
Let the label proportions adapt to the package shape, but keep the poster sparse and commercial.
```

Bad:

```text
Use any layout, any background, any typography.
```

### AVOID

Always include relevant negatives:

```text
Avoid: clean vector icon, modern logo mockup, Helvetica or Swiss grid, Bauhaus geometry, comic book title, cinematic poster, photorealistic product render, excessive digital grunge, crowded body copy.
```
