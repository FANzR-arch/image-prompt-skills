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
Use one imaginable subject: a chipped enamel mug resting low in a wide field of aged paper, drawn at 20% of the frame with crisp ink contrast so it reads at thumbnail size. Let the image model choose the strongest quiet placement — low-left, toward a corner, or slightly off-center — but keep 70-80% empty aged paper, one subject only, and a single saturated color spot sitting on the subject itself.
```

## The Style Is Emptiness

The single most important instruction in every prompt is that **aged paper negative space is the hero**. Write the prompt so the empty paper dominates and the subject sits quietly inside it. If a prompt could be read as "fill the frame," it is wrong.

Emptiness is not invisibility. The counter-failure is just as common and just as fatal: a subject so small or so pale that the cover reads as a blank page, a color spot that vanishes, a title that dissolves into the texture. Every prompt must state that the subject and the title read clearly at thumbnail size. Quiet composition, legible content.

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
MAIN TITLE:
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

Name **one** imaginable subject or tight visual cluster, chosen from the Core Image Inventory in `module-library.md`. If the input is abstract, translate it into a concrete object from that inventory first.

Do not default to the same handful of objects. Paper fragments, pressed leaves, coins, and paper boats are one corner of the inventory, not the whole of it — household objects, tools, food remains, animal traces, light and shadow, worn clothing, and architectural fragments are equally native to this style and make a set feel authored rather than generated.

Always state the subject's scale and contrast in the prompt:

```text
drawn at roughly 20% of the frame, in ink dark enough to separate cleanly from the paper, legible at thumbnail size
```

### NEGATIVE SPACE

Always make emptiness explicit and dominant, with a floor as well as a ceiling:

```text
70-80% of the canvas is calm aged paper with nothing on it; the subject occupies 12-25% of the frame — clearly present and readable, never filling the page.
```

### STYLE LOCK

Always include:

```text
quiet Japanese/Korean indie zine editorial poster, minimal print aesthetic, single small imaginable subject on a vast field of aged paper, experimental but restrained typography, one high-saturation color spot, visible print/scan paper texture, calm and contemplative
```

Do not lock the prompt into a fixed subject placement, fixed palette, or fixed typographic layout.

### SUBJECT / ANCHOR TREATMENT

Choose one anchor treatment from the module library: faded photo, torn-paper cutout, flat silhouette, small color block, old print engraving, plain object, translucent geometry, texture window, ink brush mark, rubbing or seal impression, line diagram, or attached object. Keep it simplified and quiet — never a rendered hero — but give it enough ink weight to hold its place on the page.

### MAIN TITLE

Use this section whenever the poster is a cover or the user gives title text. Skip it only for pure specimen images with no title.

Default treatment is **手写标题** — handwritten, not typeset:

```text
the handwritten title 「蝉蜕」 in ink-brush Chinese calligraphy, character height about 14% of the canvas height, visible brush entry and exit strokes and slight irregularity, clearly legible at thumbnail size, sitting alone in the open paper field
```

Rules:

- Chinese titles default to `T11 大字中文手写标题`: exact characters, 2-5 of them, brush / fountain pen / soft pencil, character height 10-18% of canvas height.
- English titles default to `T12`: hand-lettered at comparable scale.
- Always quote the exact characters the user gave. Never translate them, never substitute English, never invent characters.
- The title is a handwritten mark on paper — ink texture, human irregularity. It is not a computer script font, not a heavy black poster headline, not outlined or filled logo lettering.
- The title occupies its own open field; the paper still dominates around it. Big and legible is required; loud and dominant is not.
- Never ghost, fragment, or shrink the main title into illegibility. That treatment belongs to incidental text only.

### TYPOGRAPHY

This section covers everything except the main title. Secondary text is free in placement but fixed in nature — always quiet:

- serif, typewriter, monospace, or restrained hand lettering
- fragmentary letters, edge-hugging micro-text, archival caption text, diagonal scattered characters, or ghosted type
- may sit at an edge, in a margin, near the subject, or partly faded into the paper
- keep it sparse: one or two small elements at most, clearly subordinate to the main title
- no modern clean UI type, no Swiss grid slab, no poster-punch display type, no paragraphs of body copy

### SMALL SUBTITLE

Optional, allowed for article covers and archival captions:

- one line only
- clearly smaller and quieter than the core image's presence
- Chinese usually 6-12 characters; English usually 2-6 words
- may sit on a lower margin, corner tag, faint paper band, or beside the subject
- must look printed or typewritten as part of the same quiet zine leaf

### COLOR SPOT

Exactly **one** high-saturation color spot, occupying roughly 1.5-2.5% of the canvas, sitting against an otherwise paper / muted / near-monochrome field:

```text
one vivid color spot (for example saturated vermilion, cobalt, marigold, or acid green) covering ~2% of the frame and sitting on the subject itself — a match head, a painted rim, a single thread — plainly the brightest thing on the page; everything else stays aged paper, ink, and low-saturation grays.
```

The spot is an accent, not a field. Anchor it to the subject rather than floating it in the margin — an unanchored dot reads as a printing flaw. Do not fill areas with saturated color and do not use more than one saturated hue.

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
Let the subject's exact placement, the handwriting's slant and rhythm, subtitle use, texture, and the single spot's hue adapt to the theme, but keep the dominant aged-paper emptiness, one legible subject, one saturated spot on that subject, the exact handwritten title text at readable scale, and the calm indie-zine editorial logic.
```

Never write "any layout, any color, any composition."

### AVOID

Always include relevant negatives:

```text
Avoid: full-bleed scene, busy composition, commercial poster punch, heavy black display headline, multiple subjects, multiple saturated colors, saturated color fields, large body copy, modern clean UI, sterile vector flatness, neon, 3D render, cartoon, glossy gradient, studio lighting, photorealistic product render, fake dates, fake URLs, random unreadable labels, heavy digital grunge, illegible or microscopic title text, subject so faint it disappears into the paper, accidental stain-like marks.
```

When Chinese text is requested, also include:

```text
Avoid: English replacement text, fake or malformed Chinese characters, wrong title text, computer script font imitating handwriting, random extra labels.
```

## Reusable Template Structure

Use only when the user explicitly asks for a reusable prompt block. Keep editable fields in Chinese and fixed style instructions in English. Do not add label lines such as "你只需要改这里".

```text
文章主题或摘要：
{输入文章主题、标题、摘要，或直接粘贴文章内容}

用途和比例：
{例如：文章封面，竖版 3:5}

指定主标题（默认中文手写大字）：
{可选；没有就写：自动判断}

指定副标题文字：
{可选；没有就写：自动判断或不加}

特殊要求：
{指定核心意象、色点颜色、不能出现的元素；没有就写：无}

Create a minimal zine editorial poster from the theme above.

Style lock:
quiet Japanese/Korean indie zine editorial poster, one imaginable subject at 12-25% of the frame on a wide field of aged paper, 70-80% negative space, the main title hand-written in ink at 10-18% character height and fully legible, secondary text sparse and quiet, exactly one high-saturation color spot covering ~2% of the frame and sitting on the subject, visible risograph/photocopy/halftone/letterpress/scan paper texture, calm and contemplative, no full-bleed scene, no heavy black display headline, no multiple subjects, no multiple saturated colors, nothing so faint it disappears.
```

Image-to-image templates must start with `上传图片：` and preserve the uploaded subject's identity while reducing it to a single quiet zine specimen on aged paper.
