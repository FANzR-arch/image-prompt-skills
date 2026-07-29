# Compile Contract

## Core Rule

The skill may think in modules, but the final prompt must be resolved. Do not output raw choices unless the user explicitly asks for a reusable template.

Resolved does not mean over-specified. The final prompt must lock the single core image, the negative-space dominance, the quiet typography nature, the single high-saturation color spot, and the paper/print materiality. It may deliberately leave controlled freedom for composition, subject placement, subtitle use, and exact palette when the user wants exploratory or more varied results.

There are two valid output modes:

- **Resolved prompt mode**: default. Use when the user gives a concrete theme, sentence, object, mood, or article summary. The output should contain no placeholders.
- **Reusable template mode**: use only when the user asks for a copy-ready template, article prompt block, or reusable prompt structure. In this mode, put editable Chinese input fields first and fixed English style instructions after them.

Wrong:

```text
Use a leaf / a coin / a photo. Put the subject center or bottom-left. Add red or blue spot.
```

Right:

```text
Use one small imaginable subject: a single faded photograph fragment resting low in a vast field of aged paper. Let the image model choose the strongest quiet placement — the fragment may sit low-left, drift toward a corner, or float slightly off-center — but keep 70-90% empty aged paper, one subject only, and a single small saturated color spot no larger than a coin.
```

## The Style Is Emptiness

The single most important instruction in every prompt is that **aged paper negative space is the hero**. Write the prompt so the empty paper dominates and the subject is small and quiet inside it. If a prompt could be read as "fill the frame," it is wrong.

## Aspect Ratio

Default to `3:5 vertical` (a zine leaf / mobile poster). Honor a user-specified ratio exactly. Horizontal and square zines are allowed, but negative-space dominance never changes.

## Final Prompt Structure

Use this order:

```text
SOURCE / INPUT:
ASPECT RATIO:
CORE IMAGE:
NEGATIVE SPACE:
STYLE LOCK:
SUBJECT / ANCHOR TREATMENT:
TYPOGRAPHY:
SMALL SUBTITLE:
COLOR SPOT:
PAPER / PRINT TEXTURE:
MOOD:
CONTROLLED FREEDOM:
AVOID:
QUALITY CHECK:
```

## Section Rules

### SOURCE / INPUT

State whether the image comes from a text theme, a single sentence, one object, a mood, an article summary, or a critique task. For uploaded images, preserve the subject's identity and silhouette while stripping the original scene, lighting, and background clutter.

### CORE IMAGE

Name **one** small, imaginable subject or tight visual cluster. If the input is abstract, translate it into a concrete quiet object first.

Good core images:

- a single faded photograph fragment
- one pressed leaf
- a coin resting flat
- half a torn paper ticket
- a small open window shape
- one paper boat
- a single matchstick
- a translucent geometric pane
- a solitary chair silhouette
- a small cloud of dust motes

Weak core images (translate these into an object first):

- growth
- connection
- freedom
- intelligence
- transformation

### NEGATIVE SPACE

Always make emptiness explicit and dominant:

```text
70-90% of the canvas is calm aged paper with nothing on it; the subject cluster occupies only 8-25% of the frame and never fills it.
```

### STYLE LOCK

Always include:

```text
quiet Japanese/Korean indie zine editorial poster, minimal print aesthetic, single small imaginable subject on a vast field of aged paper, experimental but restrained typography, one high-saturation color spot, visible print/scan paper texture, calm and contemplative
```

Do not lock the prompt into a fixed subject placement, fixed palette, or fixed typographic layout.

### SUBJECT / ANCHOR TREATMENT

Choose one anchor treatment from the module library. The subject may be a faded photo, torn-paper cutout, flat silhouette, small color block, old print engraving, plain object, translucent geometry, or a texture window. Keep it small, simplified, and quiet — never a rendered hero.

### TYPOGRAPHY

Typography is free in placement but fixed in nature — always quiet and secondary:

- serif, typewriter, monospace, or restrained hand lettering
- fragmentary letters, edge-hugging micro-text, archival caption text, diagonal scattered characters, ghosted type, or one minimal small title
- may sit at an edge, in a margin, near the subject, or partly faded into the paper
- may use exact Chinese characters when requested; keep that text exactly, do not translate it, invent fake characters, or add random labels
- NEVER a big bold headline dominating the frame, no modern clean UI type, no Swiss grid slab, no poster-punch display type

### SMALL SUBTITLE

Optional, allowed for article covers and archival captions:

- one line only
- clearly smaller and quieter than the core image's presence
- Chinese usually 6-12 characters; English usually 2-6 words
- may sit on a lower margin, corner tag, faint paper band, or beside the subject
- must look printed or typewritten as part of the same quiet zine leaf

### COLOR SPOT

Exactly **one** high-saturation color spot, occupying roughly 0.8-2.5% of the canvas, sitting against an otherwise paper / muted / near-monochrome field:

```text
one small vivid color spot (for example saturated vermilion, cobalt, marigold, or acid green) covering only ~1-2% of the frame; everything else stays aged paper, ink, and low-saturation grays.
```

The spot is an accent, not a field. Do not fill areas with saturated color and do not use more than one saturated hue.

### PAPER / PRINT TEXTURE

Make texture material, not decorative:

- risograph / photocopy softness
- halftone dot degradation
- silkscreen bleed
- film grain
- letterpress impression
- scanned old-paper mottling
- pencil-drawn grays and light smudge

Avoid heavy digital grunge or fake distress overlays.

### MOOD

Pick one quiet mood register from the module library (stillness, summer, solitude, childhood, seaside, afternoon, night, memory, mild surreal) and let it steer palette temperature, texture, and subject choice.

### CONTROLLED FREEDOM

Let the model adapt only inside the chosen quiet structure:

```text
Let the subject choice, its exact small placement, the typography position, subtitle use, texture, and the single spot's hue adapt to the theme, but keep the vast aged-paper emptiness, one small subject, one saturated spot, quiet secondary type, and the calm indie-zine editorial logic.
```

Never write "any layout, any color, any composition."

### AVOID

Always include relevant negatives:

```text
Avoid: full-bleed scene, busy composition, commercial poster punch, big bold dominant headline, multiple subjects, multiple saturated colors, saturated color fields, large body copy, modern clean UI, sterile vector flatness, neon, 3D render, cartoon, glossy gradient, studio lighting, photorealistic product render, fake dates, fake URLs, random unreadable labels, heavy digital grunge.
```

When Chinese text is requested, also include:

```text
Avoid: English replacement text, fake Chinese characters, wrong title text, random extra labels.
```

## Reusable Template Structure

Use only when the user explicitly asks for a reusable prompt block. Keep editable fields in Chinese and fixed style instructions in English. Do not add label lines such as "你只需要改这里".

```text
文章主题或摘要：
{输入文章主题、标题、摘要，或直接粘贴文章内容}

用途和比例：
{例如：文章封面，竖版 3:5}

指定主标题或微文本：
{可选；没有就写：自动判断}

指定副标题文字：
{可选；没有就写：自动判断或不加}

特殊要求：
{指定核心意象、色点颜色、不能出现的元素；没有就写：无}

Create a minimal zine editorial poster from the theme above.

Style lock:
quiet Japanese/Korean indie zine editorial poster, one small imaginable subject on a vast field of aged paper, 70-90% negative space, experimental but restrained serif/typewriter/mono typography, exactly one high-saturation color spot covering ~1-2% of the frame, visible risograph/photocopy/halftone/letterpress/scan paper texture, calm and contemplative, no full-bleed scene, no dominant headline, no multiple subjects, no multiple saturated colors.
```

Image-to-image templates must start with `上传图片：` and preserve the uploaded subject's identity while reducing it to a single quiet zine specimen on aged paper.
