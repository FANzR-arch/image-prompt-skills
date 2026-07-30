# 照片改风格 · 定稿提示词

整段复制，不改任何字。quality `medium` 即可，画幅跟随原照片。

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

## 换配色

只替换上面的 `COLOUR —` 段，其他段落一律不碰。仍是同一条提示词、同样三步。

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
Colour: closed palette — sage green background, olive and ochre, ivory, with
terracotta accents.
```

```text
Colour: closed palette — misty grey-blue background, limestone white, deep teal,
charcoal, and one small warm orange accent.
```

```text
Colour: closed palette — lemon yellow background, vermilion, cobalt blue, pure
white, pure black.
```

```text
Colour: closed palette — deep plum background, aubergine, dusty rose, ivory, and
one antique-bronze accent.
```

```text
Colour: closed palette — ochre background, burnt sienna, deep olive, cream, and
one small teal accent.
```

```text
Colour: closed palette — oxblood background, deep maroon, warm sand, bone white,
and one small gold accent.
```

## 色相仍偏蓝时的追加顺序（一次只加一条）

定稿版已删掉带蓝色偏置的形容词并给出候选色相清单。若实测仍偏蓝：

1. `DO NOT` 的 Background 行增 `no defaulting to a blue background`；
2. `COLOUR` 第 3 项（Skin）改为随背景自适应：`warmer against cool backgrounds, paler and cooler against warm ones`。暖底配暖肤可能糊成一片，属预判风险，**不预先加**；
3. 仍不行则放弃在提示词内解决，改为按需替换整段 `COLOUR`。

## 改动前必读

当前这版是唯一产出被认可成图的版本，此后三次改进全部劣化并回退：

| 改动 | 结果 |
|---|---|
| 脸型改「定向查找」+ 负向由 18 项剪至 7 项 | 畸形（颅骨放大、五官缩小） |
| 加美学下限、删 Shift 操作、`caricature` 换成 `designed character illustration` | 退回写实 |
| 改用结构规格（八个可数平面、几何原语、拉长四分之一） | 仍偏写实 |

**关键反证**：畸形一度被归因于 `visibly wrong` / `caricature` / `Shift` 三处措辞——归因错误，这三处在正常出图的版本里原样存在，真正原因是同批做的负向剪枝。被剪掉的 `no accurate facial proportions` / `no fine detail` / `no muddy skin` 是承重项。

**由此三条纪律**：`DO NOT` 十七项不要剪；要改一次只改一处；归因只在版本差异集合里找。
