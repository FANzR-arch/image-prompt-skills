# Plakatstil / Sachplakat 模块化提示词编译器

Plakatstil 不是“复古 icon 海报”，而是商品广告海报：一个清楚的物品，一个广告字，一套有限印刷色，少量文案，强烈物体识别。

复制下面整段给 AI，然后输入文字主题、商品照片或包装照片。

```text
ROLE:
Act as a Plakatstil / Sachplakat prompt compiler.

INPUT:
The user may provide a text theme, a product photo, a package photo, a portrait/service theme, or a generated poster sample for critique.

TASK:
First identify the best advertising object. If the input is abstract, convert it into one concrete sellable object. If the input is an uploaded image, preserve the object's identity, silhouette, material, label hierarchy, and most recognizable details.

For electronic devices, default to Apple brand and Apple product families unless the user explicitly names another brand. Keep the Apple identity visible through product silhouette and readable brand/product text, but translate it into early printed advertising language rather than modern Apple launch visuals.

Then select modules before writing the final prompt:
- source mode
- subject treatment
- typography behavior
- layout family
- background family
- limited lithographic palette
- paper and ink texture
- negative constraints

Do not expose unresolved choices in the final image prompt. The final prompt must be clear, copy-ready, and already decided. Do not use placeholders, slash menus, or "either/or" layout instructions unless the user explicitly asks for a reusable template.

STYLE LOCK:
Keep the style fixed: early 20th-century German Plakatstil / Sachplakat advertising poster, one concrete commercial object, simplified but recognizable product hero, custom hand-painted advertising lettering, minimal copy, limited lithographic ink colors, matte printed paper, visible paper grain, ink absorption, slight print registration imperfections, rough painted edges.

CONTENT FREEDOM:
Keep the content flexible. Text may sit above, behind, beside, on the product label, on the package, or partially hidden by the product. The product may be flat, semi-rendered, cropped, diagonal, centered, off-center, or package-led. The background may be a dark flat field, old paper field, color bands, product-derived color block, or worn border if it fits the object.

AVOID:
Avoid clean vector icon, modern logo mockup, Helvetica or Swiss grid, Bauhaus geometry, comic book title, rock-band lettering, cinematic poster, photorealistic product render, excessive digital grunge, crowded body copy, fake dates, fake URLs, and random unreadable labels.

OUTPUT:
1. selected modules
2. one complete final prompt
3. one sentence explaining the choice
```

## 随机主题示例

下面这些不是固定模板，而是“模块已经选好”的成品 prompt。主题可以是现代物品，但成图逻辑仍然是早期商品广告。电子设备示例统一使用 Apple 品牌。

### 01｜Apple AirPods：APPLE

```text
SOURCE / INPUT:
Text theme for an Apple AirPods advertisement. Main brand word: "APPLE". Product word: "AIRPODS".

AD OBJECT:
One pair of Apple AirPods and one open white charging case.

STYLE LOCK:
Create an early 20th-century German Plakatstil / Sachplakat advertising poster: simplified commercial object poster, hand-painted lithographic look, minimal copy, bold product silhouette, custom advertising lettering, matte printed paper.

SUBJECT TREATMENT:
Show the Apple AirPods charging case as a simplified warm white object with two small earbuds inside, slightly cropped and monumental. Keep the distinctive AirPods case silhouette, but repaint it as if it were a vintage consumer appliance advertisement.

TYPOGRAPHY:
Use a large custom hand-painted "APPLE" brand word in dull blue, placed behind the product and partially hidden by the open case. Add one small muted red product word "AIRPODS". The lettering should feel hand-cut and commercial, not modern tech branding.

LAYOUT + BACKGROUND:
Use an object-over-brand layout with a deep brown-black flat field. Place the case in the lower center, slightly tilted, with large negative space around the brand word.

COLOR + PRINT:
Use limited lithographic inks: dark brown-black, dull blue, warm cream, muted red, and a little ochre shadow.

PAPER / INK TEXTURE:
Visible paper fibers, matte ink, ink absorption at edges, rough painted contours, and slight lithographic registration shifts.

CONTROLLED FREEDOM:
Let the AirPods shape simplify naturally, but keep the product legible and the composition sparse.

AVOID:
Avoid clean vector icon, modern Apple keynote render, futuristic glow, Helvetica, Swiss grid, Bauhaus geometry, comic lettering, fake UI text, extra fake logos, and digital grunge overlay.

QUALITY CHECK:
The image should feel like a real vintage product advertisement for Apple AirPods, not a modern tech poster.
```

### 02｜Apple Magic Keyboard：APPLE

```text
SOURCE / INPUT:
Text theme for an Apple Magic Keyboard advertisement. Main brand word: "APPLE". Product word: "KEYBOARD".

AD OBJECT:
One Apple Magic Keyboard with low-profile white keys and a slim aluminum base.

STYLE LOCK:
Create an early 20th-century German Plakatstil / Sachplakat advertising poster: simplified commercial object poster, hand-painted lithographic look, minimal copy, bold product silhouette, custom advertising lettering, matte printed paper.

SUBJECT TREATMENT:
Show the Apple Magic Keyboard as a cropped product macro from a low front angle. Simplify the low-profile white keys into flat hand-painted blocks, keeping the slim aluminum base and clean rectangular silhouette.

TYPOGRAPHY:
Use a large cream hand-painted "APPLE" word along the upper left edge, with uneven brush-cut terminals. Put "KEYBOARD" as smaller black lettering printed along the front edge of the keyboard base, as if the product label is part of the object.

LAYOUT + BACKGROUND:
Use a diagonal hero crop. The keyboard enters from the lower right and fills the bottom half. Keep a warm aged paper field behind it with a worn printed border.

COLOR + PRINT:
Use cream paper, black ink, ochre shadows, graphite gray, and a small muted red accent.

PAPER / INK TEXTURE:
Use visible paper grain, matte pigment, slightly uneven key edges, mild misregistration around the red key, and rubbed border corners.

CONTROLLED FREEDOM:
Allow the exact key layout to simplify, but keep the Apple Magic Keyboard clearly recognizable and commercially centered.

AVOID:
Avoid mechanical gaming keys, RGB lighting, gaming neon, clean 3D render, modern UI mockup, Helvetica, Swiss grid, Bauhaus geometry, fake app icons, and crowded key labels.

QUALITY CHECK:
It should read as an old product poster for an Apple keyboard, not a modern computer accessory ad.
```

### 03｜Apple Watch：APPLE

```text
SOURCE / INPUT:
Text theme for an Apple Watch advertisement. Main brand word: "APPLE". Product word: "WATCH".

AD OBJECT:
One Apple Watch with a rounded-square face, simple strap, and one bold dial mark.

STYLE LOCK:
Create an early 20th-century German Plakatstil / Sachplakat advertising poster: simplified commercial object poster, hand-painted lithographic look, minimal copy, bold product silhouette, custom advertising lettering, matte printed paper.

SUBJECT TREATMENT:
Show the Apple Watch as a semi-rendered metal-and-glass object, simplified into a rounded-square face, dark strap, and one cream dial mark. Keep light reflections hand-painted and flat, not photographic.

TYPOGRAPHY:
Place the large brand word "APPLE" as cream hand-painted letters partly behind the watch face. Add a small muted blue "WATCH" under the strap. The type should feel like a painted commercial wordmark.

LAYOUT + BACKGROUND:
Use a centered object-over-brand layout with two muted horizontal color bands behind the watch, inspired by old technical product ads.

COLOR + PRINT:
Use dark blue-black, cream, muted blue, dull ochre, and rust red as limited lithographic colors.

PAPER / INK TEXTURE:
Use matte paper grain, hand-painted glass highlights, slight color offset at the watch edge, and ink absorption in the dark background.

CONTROLLED FREEDOM:
Let the watch face remain simple and iconic, but preserve the Apple Watch silhouette.

AVOID:
Avoid futuristic interface screens, app icons, glowing OLED effects, photorealism, clean vector icon, Helvetica, Swiss grid, fake health dashboard text, and sci-fi poster language.

QUALITY CHECK:
The poster should sell an Apple Watch as if it were an early 20th-century commercial object.
```

### 04｜咖啡袋：MORGEN

```text
SOURCE / INPUT:
Text theme for a coffee bag advertisement. Main brand word: "MORGEN". Product word: "KAFFEE".

AD OBJECT:
One folded paper coffee bag with a printed front label.

STYLE LOCK:
Create an early 20th-century German Plakatstil / Sachplakat advertising poster: simplified commercial object poster, hand-painted lithographic look, minimal copy, bold product silhouette, custom advertising lettering, matte printed paper.

SUBJECT TREATMENT:
Show the coffee bag as a package-led hero object with folded paper creases, a blocky printed label, and a dark coffee-bean emblem. The wrapper text should participate in the poster, not look like a modern mockup.

TYPOGRAPHY:
Use "MORGEN" as large hand-painted cream letters in the background. Print "MORGEN KAFFEE" again on the bag label in dark ink and muted red, with uneven letterpress edges.

LAYOUT + BACKGROUND:
Use a package close-up layout. Place the bag diagonally across the lower right, cropped slightly, against a deep tobacco green field with a narrow worn cream border.

COLOR + PRINT:
Use tobacco green, warm cream, kraft ochre, dark brown, and muted red.

PAPER / INK TEXTURE:
Emphasize paper fibers, matte kraft paper, ink absorption, rough label lines, and slight print registration imperfection.

CONTROLLED FREEDOM:
Let the fold structure and label proportions adapt to the bag, but keep the copy minimal and product-led.

AVOID:
Avoid cafe lifestyle scene, steam drama, photorealistic bag mockup, modern minimalist packaging, clean vector logo, Swiss grid, and excessive body copy.

QUALITY CHECK:
The result should feel like a vintage grocery advertisement built around one package.
```

### 05｜Apple Vision Pro：APPLE

```text
SOURCE / INPUT:
Text theme for an Apple Vision Pro advertisement. Main brand word: "APPLE". Product word: "VISION".

AD OBJECT:
One Apple Vision Pro headset with a curved glass front and soft woven head band.

STYLE LOCK:
Create an early 20th-century German Plakatstil / Sachplakat advertising poster: simplified commercial object poster, hand-painted lithographic look, minimal copy, bold product silhouette, custom advertising lettering, matte printed paper.

SUBJECT TREATMENT:
Show the Apple Vision Pro headset as a semi-rendered glass-and-metal object, cropped large from the right edge. Paint the curved glass front as a simplified dark reflective plane with two flat blue and cream highlights, and render the soft band as a few bold woven strokes.

TYPOGRAPHY:
Set "APPLE" as large ochre hand-painted letters behind the headset, partly hidden by the glass front. Add "VISION" in small muted red lettering near the lower left.

LAYOUT + BACKGROUND:
Use an edge-crop object-over-brand layout on a dark blue-black field. Keep the left side sparse so the Apple word has weight.

COLOR + PRINT:
Use dark blue-black, ochre, cream, muted red, and dull cyan highlights.

PAPER / INK TEXTURE:
Use matte ink, visible paper tooth, hand-painted glass contours, subtle color misregistration at the headset edge, and worn poster edges.

CONTROLLED FREEDOM:
Let the band and glass reflections simplify, but keep the object immediately readable as Apple Vision Pro.

AVOID:
Avoid photorealistic studio product render, glossy 3D, sci-fi HUD, floating interface panels, clean vector icon, Helvetica, fake app windows, and excessive technical microtext.

QUALITY CHECK:
The poster should feel like a Plakatstil optical goods ad for Apple Vision Pro, not a modern mixed-reality launch poster.
```

### 06｜Apple MagSafe Battery Pack：APPLE

```text
SOURCE / INPUT:
Text theme for an Apple MagSafe Battery Pack advertisement. Main brand word: "APPLE". Product word: "MAGSAFE".

AD OBJECT:
One white Apple MagSafe Battery Pack with a rounded rectangular body and one short white charging cable.

STYLE LOCK:
Create an early 20th-century German Plakatstil / Sachplakat advertising poster: simplified commercial object poster, hand-painted lithographic look, minimal copy, bold product silhouette, custom advertising lettering, matte printed paper.

SUBJECT TREATMENT:
Show the Apple MagSafe Battery Pack as a heavy rounded rectangle, simplified into a warm white block with a subtle magnetic circle and one red cable loop. Treat the cable as a bold graphic shape, not a modern tech accessory render.

TYPOGRAPHY:
Paint "APPLE" as large black hand-cut letters across the cream background. Put "MAGSAFE" as small red label text printed on the side of the battery pack.

LAYOUT + BACKGROUND:
Use a split field: cream aged paper on the upper left and dark brown-black on the lower right. Place the power bank horizontally across the split, with the red cable looping into the dark field.

COLOR + PRINT:
Use cream paper, black, dark brown, muted red, and ochre shadow.

PAPER / INK TEXTURE:
Use visible paper grain, uneven ink coverage, absorbed edges, hand-painted cable contour, slight registration shift, and matte printed surface.

CONTROLLED FREEDOM:
Let ports and details simplify, but keep the object recognizable as an Apple MagSafe battery accessory.

AVOID:
Avoid glowing electricity effects, USB icons everywhere, clean app-style vector, modern tech landing page, neon gradients, Swiss grid, Bauhaus geometry, comic energy bolts, and fake specification text.

QUALITY CHECK:
The result should look like a believable vintage advertisement for an Apple MagSafe charging object.
```

### 07｜Apple iPhone：APPLE

```text
SOURCE / INPUT:
Text theme for an Apple iPhone advertisement. Main brand word: "APPLE". Product word: "IPHONE".

AD OBJECT:
One Apple iPhone with a dark glass screen, rounded rectangular body, and one visible side button.

STYLE LOCK:
Create an early 20th-century German Plakatstil / Sachplakat advertising poster: simplified commercial object poster, hand-painted lithographic look, minimal copy, bold product silhouette, custom advertising lettering, matte printed paper.

SUBJECT TREATMENT:
Show the iPhone as a monumental black glass slab, simplified into a strong rounded rectangle with one muted cream screen reflection and a small red side button. Preserve the iPhone silhouette, but repaint it as a flat hand-painted commercial object.

TYPOGRAPHY:
Use a large custom hand-painted "APPLE" brand word in warm cream, placed vertically along the left side and partly overlapped by the iPhone edge. Add "IPHONE" as small muted red product text near the lower right, aligned to the object rather than floating like a modern UI caption.

LAYOUT + BACKGROUND:
Use a corner-crop layout. Let the iPhone enter from the right edge at a slight angle, occupying most of the right half. Keep a deep blue-black field with wide negative space on the left for the Apple word.

COLOR + PRINT:
Use limited lithographic inks: deep blue-black, warm cream, dark graphite, muted red, and a small ochre highlight.

PAPER / INK TEXTURE:
Use visible paper grain through the dark ink, hand-painted screen reflection, slight ink absorption around the phone silhouette, mild print registration shift at the red button, and matte old poster surface.

CONTROLLED FREEDOM:
Let the glass highlight and corner radius adapt naturally, but keep the iPhone as one simple product hero without interface clutter.

AVOID:
Avoid app icons, glowing UI, futuristic holograms, clean vector mockup, photorealistic phone render, Samsung or generic Android cues, Helvetica, Swiss grid, Bauhaus geometry, cinematic lighting, and crowded technical text.

QUALITY CHECK:
The image should feel like a vintage product advertisement for an Apple iPhone, not a smartphone launch keynote poster.
```

### 08｜Apple MacBook：APPLE

```text
SOURCE / INPUT:
Text theme for an Apple MacBook advertisement. Main brand word: "APPLE". Product word: "MACBOOK".

AD OBJECT:
One open Apple MacBook with a thin screen, aluminum keyboard plane, and simple hinge.

STYLE LOCK:
Create an early 20th-century German Plakatstil / Sachplakat advertising poster: simplified commercial object poster, hand-painted lithographic look, minimal copy, bold product silhouette, custom advertising lettering, matte printed paper.

SUBJECT TREATMENT:
Show the open MacBook as a cropped product macro, simplified into two strong planes: a dark screen rectangle and a warm aluminum keyboard base. Keep the hinge and keyboard rows visible as rough painted marks, not precise modern UI detail.

TYPOGRAPHY:
Paint "APPLE" as large black hand-cut letters across the warm cream background, partly hidden by the open MacBook screen. Put "MACBOOK" as small dull blue product text printed on the lower keyboard base, as if it were a product label.

LAYOUT + BACKGROUND:
Use a split-field package-like layout. Place the MacBook open at a three-quarter angle across the center, with the screen rising into a dark brown-black upper field and the base resting on an aged cream lower field. Leave the lower left corner quiet.

COLOR + PRINT:
Use cream paper, dark brown-black, graphite black, dull blue, muted ochre, and a small rust-red accent on one key.

PAPER / INK TEXTURE:
Use matte lithographic ink, visible paper fibers, rough painted keyboard rows, uneven edge absorption around the screen, slight color misregistration on the blue product text, and a subtly worn printed border.

CONTROLLED FREEDOM:
Let the exact keyboard marks simplify, but keep the MacBook immediately recognizable as an open Apple portable computer.

AVOID:
Avoid modern laptop product photography, glowing screen UI, software windows, clean vector icon, fake Apple sub-branding, neon gradient, Swiss grid, Bauhaus geometry, cinematic workstation scene, and dense spec-sheet text.

QUALITY CHECK:
The result should feel like a plausible early product advertisement for an Apple MacBook, translated into Plakatstil language.
```

## Skill 版

如果工具支持 Agent Skills，安装整个目录：

```text
plakatstil-prompt-compiler/
├── SKILL.md
├── ARTICLE-COPY.md
└── references/
    ├── compile-contract.md
    ├── module-library.md
    ├── evaluation-rubric.md
    └── examples.md
```

触发示例：

```text
用 plakatstil-prompt-compiler，根据“机械键盘”生成一张 Plakatstil 商品广告海报提示词。
```

```text
用 plakatstil-prompt-compiler，把我上传的咖啡袋照片重绘成 Sachplakat 广告海报。
```
