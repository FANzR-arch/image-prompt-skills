# 颗粒棱面风格配图：简易版 + Skill 版

平涂大色块 + 细密颗粒的图形风格。

这套风格最容易做砸的地方不在颗粒本身，而在**颗粒的作用域**：颗粒只能在主体上，背景必须是绝对干净的单一平涂色，零噪点零纹理。多数模型默认会把颗粒铺满整张图，背景一脏，风格立刻塌成"加了噪点的普通插画"。下面每一段提示词里反复出现的那句背景约束，就是为这件事写的。

![颗粒棱面风格](assets/preview.png)

## 一、照片改风格（最简单，三步）

传照片 → 粘贴下面整段 → 生成。不需要参考图，不需要 API。

**整段复制，不要改字。** 这条经过多轮实测定稿，三次"优化"尝试全部劣化并回退（记录在文末）。

```text
GOAL
Restyle this photo completely as a flat, heavily grained graphic portrait
illustration. This is a full restyling and a strong caricature — not a filter,
and not a likeness.

SUBJECT — exaggeration: push this much further than feels comfortable, and treat
the photo as a reference for character, not for geometry:
- Elongate: stretch the head, neck and body noticeably longer and narrower than
  they are in the photo.
- Oversize: pick the two or three most distinctive things — the hair silhouette,
  the glasses, the nose, the jaw, the hands — and make them clearly bigger than
  life.
- Angularise: turn soft curves into straight edges and wedges. The nose becomes
  a hard wedge, the jaw one angled plane, the cheek a single flat facet.
- Drop: delete every undistinctive small feature outright rather than shrinking
  it.
- Shift: freely move features up, down or further apart from where the photo
  puts them.
The finished proportions must look visibly wrong when measured against the
photo. If it still reads as an accurate likeness, it has not gone far enough.

SURFACE — texture, the defining feature: fill the subject with a heavy, dense
stipple of fine dots, so densely packed and high in contrast that the surface
reads as fuzzy and velvety at a glance, like velvet flocking or spray paint
blasted through a stencil. The grain must eat into the subject's edges so every
boundary reads as finely speckled and slightly ragged, never a clean vector
line. The background, by contrast, must be perfectly smooth flat colour with
absolutely zero grain, noise or texture. That contrast between the fuzzy grainy
subject and the dead-smooth background is what defines this style and must be
immediately obvious.

SURFACE — planes: every plane must be one single flat colour meeting the next
plane at a hard edge. No continuous shading, no blending, no gradual tonal
transition across a form — where two areas differ in tone they must be two
separate planes with a visible boundary between them. Keep the stipple even and
consistent within each plane, never blotchy, mottled or dirty-looking.

COLOUR — five flat colours, assigned exactly like this:
1. Background: one strong flat hue, smooth and even. Choose it deliberately and
   vary it — do not default to blue. Pick whichever suits this particular
   subject: ochre, mustard, burnt orange, oxblood, plum, forest green, olive,
   deep teal, slate grey, near-black or cobalt.
2. Hair and clothing: a darker shade from the same family as the background, so
   they sit together quietly.
3. Skin: one clear warm tone in only two flat steps — a light plane and one
   darker shadow plane, with a hard edge between them. Never a muddy, greyish or
   neutral beige.
4. One light neutral, used only for small bright areas, never for the face.
5. One saturated accent, used in a single small place.
Never set two fully saturated complementary colours against each other across
the two largest areas of the image.

FRAMING: keep the entire subject inside the frame with clear breathing space
around it — do not crop the head, and leave a visible margin of background on at
least two sides.

DO NOT
- Stylisation strength: no accurate facial proportions; no realistic likeness;
  no timid or half-hearted stylisation.
- Background: no grain, noise or texture in the background; no pale or
  washed-out background.
- Colour: no saturated colour clash between background and subject; no muddy or
  greyish skin.
- Rendering: no continuous or blended shading; no fine detail; no gradients; no
  soft focus or blurring.
- Wrong surface: no woolly felted look; no clean vector edges; no low-poly
  triangulation; no outlines.
- Output: no text; no watermark.
```

### 换气质只换配色段

只替换上面的 `COLOUR —` 整段，**其他段落一律不碰**。仍是同一条提示词、同样三步。

```text
Colour: closed palette — cobalt blue background, dusty rose and deep crimson for
the subject's planes, warm white, golden yellow, black.
```

```text
Colour: closed palette — terracotta orange background, deep brown, brick red,
cream, golden yellow; all warm and close in hue, separated by value alone.
```

```text
Colour: closed palette — dark moss green background, iron grey and slate grey,
cream, and one single vermilion accent as the only bright element.
```

```text
Colour: closed palette — ochre background, burnt sienna, deep olive, cream, and
one small teal accent.
```

```text
Colour: closed palette — deep plum background, aubergine, dusty rose, ivory, and
one antique-bronze accent.
```

```text
Colour: closed palette — misty grey-blue background, limestone white, deep teal,
charcoal, and one small warm orange accent.
```

```text
Colour: closed palette — oxblood background, deep maroon, warm sand, bone white,
and one small gold accent.
```

```text
Colour: closed palette — sage green background, olive and ochre, ivory, with
terracotta accents.
```

```text
Colour: closed palette — lemon yellow background, vermilion, cobalt blue, pure
white, pure black.
```

### 两条经验

- 正脸平光自拍效果最差，源照有明确单侧光时最稳。
- 出图不满意直接重生成一次，不要开始逐轮微调——这条提示词是按"一次成"设计的。

## 二、从零生成（不用照片，给主题就出图）

复制下面整段给 AI，只填主题和比例。风格、色板架构、质感、约束全部锁死。

```text
请根据我给出的指令，生成一张「颗粒棱面风格」的配图提示词。

输入：
【主题：】
【比例：】

生成规则：
1. 只输出一段英文提示词，不要解释、不要给选项、不要反问我。
2. 按七段结构输出，保留段落标签：Use case / Scene / Subject / Key details /
   Composition / Text in image / Constraints。
3. 主题只决定 Subject 和 Scene 里画什么；风格段落（Scene 的句式、Key details、
   Constraints）逐字照抄下面的固定块，一个字都不要改。
4. 比例写进 Use case 段末尾。没填就用 vertical 2:3。
5. 背景色相从这些里挑一个最配主题的，不要默认用蓝：ochre、mustard、burnt
   orange、oxblood、plum、forest green、olive、deep teal、slate grey、
   near-black、cobalt。挑定后按这个顺序配满五色：背景色 → 主体某一大块取背景
   同色系做呼应 → 主色（与背景对比但降饱和）→ 一个中性色 → 一个小面积高饱和
   点睛色。
6. 主题留空时，画一件有明确轮廓的日常器物。
7. Subject 段用 "built from only a handful of large planes" 起手，逐个点名 4-6 个
   大色块分别是什么、什么颜色，并点名哪些局部要保持锐利。另外：
   - 高饱和点睛色只许出现在一个地方，在 Subject 段就写明 "the only bright
     element"；
   - 主体是多个人或多个物件时，每个都要更简化，人脸直接处理成没有五官的单色
     面，否则面数过多会退回低多边形；
   - 主体在画面里不能太小，最小的色块也要占到画面 3% 以上，否则颗粒会盖掉形状。
     主题适合远景时，用中景代替极远景。
8. Composition 段写机位、主体位置与占比、留空区域。如果选正上方俯视，必须在
   Constraints 段开头补 "no perspective depth, no cast shadows"。

Scene 段固定这样写，只换背景色：
Scene: a single flat [背景色] field that is perfectly smooth and completely free
of any grain, noise or texture, no scenery, no horizon.

例外：主题是风景、海景、山景这类需要地平线的题材时，Scene 段改成两条平涂色带，
其余段落不变：
Scene: two flat colour bands only — a large [上带色] field above, a [下带色]
field below, meeting at a clean horizon; both bands perfectly smooth and
completely free of any grain, noise or texture; no rendered scenery, clouds or
waves.

Key details 段（逐字照抄，只替换方括号里的五色）：
Key details: the subject only is filled with a dense, fine, even stipple, like
spray paint pushed through a stencil, and that stipple erodes the subject's
boundaries into finely speckled, slightly ragged edges — each shape stays
completely legible and in focus, yet no edge is a smooth clean vector line. The
background stays untouched clean flat colour with no grain at all. Keep tonal
steps minimal: one even colour per plane, no faceted shading inside a plane.
Closed palette — [按规则 5 配好的五色].

Constraints 段（逐字照抄，不要增删）：
Constraints: no grain, noise or texture anywhere in the background, no smooth
clean vector edges, no flat crisp digital shapes, no faceted tonal stepping, no
blurring or soft focus, no woolly or felted texture, no low-poly triangulation,
not photorealistic, no 3D render, no outlines, no gradients, no logos, no
watermark.
```

### 想一步直接出图

在上面规则 1 后面加一句：

```text
输出提示词后，直接用它生成图片。
```

代价是拿不到可复用的提示词文本。**默认不加**——提示词能改、能存、能复用，图片不能。

### 你只需要改两个空

```text
【主题：一台老打字机的局部特写】
【比例：2:3 竖版】
```

```text
【主题：正侧面的鹭鸟头颈】
【比例：16:9】
```

```text
【主题：从正上方俯视的一株龙舌兰】
【比例：1:1】
```

## 三、一条成品长什么样

```text
Use case: editorial illustration still life, vertical 2:3, no text.

Scene: a single flat dark moss-green field that is perfectly smooth and
completely free of any grain, noise or texture, no scenery, no horizon.

Subject: an extreme close-up of part of an old typewriter — three rows of round
keys cut off by the frame edges, the curved platen roller crossing the upper
area as one broad plane, a single sheet of paper rising behind it, and one
vermilion return lever as the only bright element; built from only a handful of
large planes.

Key details: the subject only is filled with a dense, fine, even stipple, like
spray paint pushed through a stencil, and that stipple erodes the subject's
boundaries into finely speckled, slightly ragged edges — each shape stays
completely legible and in focus, yet no edge is a smooth clean vector line. The
background stays untouched clean flat colour with no grain at all. Keep tonal
steps minimal: one even colour per plane, no faceted shading inside a plane.
Closed palette — dark moss green field, iron grey and slate grey for the machine
planes, cream for the paper, vermilion for the single lever, near-black for the
key faces.

Composition: extreme close-up from a slight high angle, the machine filling most
of the frame and cropped on three sides, one wedge of empty green field in the
upper left corner.

Text in image: no text.

Constraints: no grain, noise or texture anywhere in the background, no smooth
clean vector edges, no flat crisp digital shapes, no faceted tonal stepping, no
blurring or soft focus, no woolly or felted texture, no low-poly triangulation,
not photorealistic, no 3D render, no outlines, no gradients, no logos, no
watermark.
```

## 四、为什么不要"优化"照片那条

这条提示词有过三次改进尝试，全部劣化并回退：

| 改动 | 结果 |
|---|---|
| 脸型改「定向查找」+ 负向由 18 项剪至 7 项 | 畸形（颅骨放大、五官缩小） |
| 加美学下限、删 Shift 操作、`caricature` 换成 `designed character illustration` | 退回写实 |
| 改用结构规格（八个可数平面、几何原语、拉长四分之一） | 仍偏写实 |

**关键反证**：畸形一度被归因于 `visibly wrong` / `caricature` / `Shift` 三处措辞——归因错了。这三处在正常出图的版本里原样存在，真正原因是同一批做的负向剪枝。被剪掉的 `no accurate facial proportions` / `no fine detail` / `no muddy skin` 是承重项。

**由此三条纪律**：`DO NOT` 十七项不要剪；要改一次只改一处；归因只在版本差异集合里找。

## 五、Skill 版逻辑

如果要长期复用，不要只存一条固定 prompt，做成 skill：

```text
GRAINY PLANE STYLE SKILL

ROLE：
You are a grainy-plane image prompt compiler. The style is flat large planes plus
a dense stipple, and it lives or dies on one thing: the grain belongs to the
subject only, never the background.

STYLE DNA (never varies)：
Fine even dot stipple like spray paint through a stencil. Grain on the subject
only — the background is a single perfectly smooth flat colour with zero noise.
Edges are grain-eroded: hard, legible, in focus, speckled and slightly ragged,
neither clean vector lines nor blur. Few large planes, one flat colour each, no
tonal stepping inside a plane. Closed 5–6 colour palette, no gradients, no
outlines. Silhouette legible at a glance; graphic reading beats realism.

ROUTING：
User supplies a photo → photo-restyle mode: return the locked prompt verbatim.
User supplies a topic → from-scratch mode: fill the master template.
Unclear → ask once, do not guess.

PHOTO-RESTYLE MODE：
The prompt is settled. Return it whole and unedited. Only the COLOUR block may be
swapped, and only for another complete palette — never edit individual lines. Do
not prune the DO NOT list: it is load-bearing, and pruning it is what caused every
past regression.

FROM-SCRATCH MODE：
Compose subject type × palette logic × camera angle. Reuse the DNA fixed blocks
verbatim, swapping only the palette. Name 4-6 large planes and their colour
assignments explicitly. Guard three failure modes: name the single bright accent
as "the only bright element"; simplify harder as subject count rises (faces become
featureless single-colour planes); keep the smallest plane above 3% of the frame,
using a mid shot instead of an extreme wide one. Overhead views need "no
perspective depth, no cast shadows" in Constraints. Landscapes are the only
allowed relaxation of the single-field background: two flat bands, both stated as
zero-noise.

OUTPUT：
One complete copy-ready English prompt in seven labelled segments — Use case /
Scene / Subject / Key details / Composition / Text in image / Constraints — with
exclusions baked into the Constraints segment, never as a separate negative-prompt
block.

GUARDRAILS：
Describe the style by visual features, never by naming a living artist. Other
people's photos need their consent. If an image disappoints, regenerate once
rather than starting a multi-round tuning loop.
```

## 六、怎么用这个 Skill

如果你的工具支持 Agent Skills，把完整的 `grainy-plane-style` 文件夹安装或放进 skills 目录：

```text
grainy-plane-style/
├── SKILL.md
├── ARTICLE-COPY.md
└── references/
    ├── photo-restyle.md
    ├── from-scratch.md
    └── examples.md
```

安装后一句话触发：

```text
用 grainy-plane-style，把我这张照片改成颗粒棱面风格。
```

```text
用 grainy-plane-style，做一张 2:3 的封面，主题是一台老打字机的局部特写。
```

```text
用 grainy-plane-style，配色换成暗墨绿加一点朱红。
```

如果你的工具不支持安装 skill，直接复制本文前两节的提示词当单文件版用。
