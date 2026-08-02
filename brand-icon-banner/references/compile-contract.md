# 编译契约

固定骨架 + 全部数值。编译时**照抄骨架，只替换尖括号里的槽**。

## 铁律

1. 七段结构带标签输出：Use case / Scene / Subject / Key details / Composition / Text in image / Constraints。
2. 正文全英文，只有渲染进画面的中文放引号里。
3. 没有 negative 通道——排除项写进 Constraints 正文，不输出独立 `Negative prompt:` 块。
4. 没有 seed / 权重 / `--` 参数。
5. 不用水词（masterpiece / 8k / ultra detailed），换成视觉事实。
6. 单条完整可复制，约束不散落在正文之外。

## 数值表（全部锁死）

| 项 | 值 |
|---|---|
| 画幅 | 5:2，出图 `2560×1024`，quality `high` |
| 左右边距 | 各 10% |
| 上下安全区 | 各 ≥14% 净底 |
| 文字块 | 10% → 不越过 56% |
| 图标 | 64% → 88% 画宽，约 60% 画高 |
| 图标光心 | 50% 画高 |
| 大标题中线 | 与图标光心同高 |
| 图标厚度 | 约为宽度的 1/5 |
| 正面内凹唇 | 距轮廓约 1/20 图标宽 |
| 图标旋转 | 平面内顺时针约 12°，向右微转 |
| kicker 字高 | 约 4% 画高 |
| 大标题字高 | 约 15% 画高 |
| 副标题 | 大标题的 38% |
| 细线 → kicker | kicker 字高 × 0.6 |
| kicker → 大标题 | kicker 字高 × 0.9 |
| 大标题 → 副标题 | 副标题自身高 × 1.5 |
| 反白块内边距 | 大标题字高 × 0.18 |
| 反白块圆角 | 大标题字高 × 0.12 |

**行距一律用「相对自身字高的倍数」，不用形容词**。写 `a small gap` 模型会自由发挥，写 `six tenths of the kicker's height` 才是硬约束。反白块的内边距和圆角同理。

## 固定骨架

```
Use case: Ultra-wide editorial header banner for a business-analysis article, 5:2, a three-tier Chinese headline block on the left and one hero object on the right.

Scene: A seamless studio void with no horizon and no floor edge, filled with a clean <冷/暖> off-white that stays even across the frame and darkens only in a soft neutral falloff around the object on the right. It reads as one continuous lit surface, never as two joined panels.

Subject: On the right, a single thick rounded-square app tile carrying the current <品牌> app icon as <品牌> uses it today — <一句呈现方式：底色 + logo 颜色 + 平贴正面>, never <退役旧标>. The tile is a solid extruded slab about one fifth as deep as it is wide, with generously rounded corners and softly filleted edges, and its front face carries a shallow inset lip about one twentieth of its width in from the silhouette, giving the object an internal step. It hovers just above the ground plane, rotated about 12 degrees clockwise in plane and angled a few degrees toward the viewer's right, so the right side face and the underside read as two distinct darker planes. <道具句：1–2 件，写清倚靠/平躺关系与受光>. Nothing else occupies the scene.

Key details:
Form — pure primitive geometry, one squircle prism plus <道具形体>, no bevelled facets, no low-poly faceting, no sub-detail.
Edges — crisp and unbroken silhouettes. The fillets carry one soft broad specular sweep along the top-left edge and a thin cool rim-light down the right edge; these two highlights are the only things separating the tile from the backdrop and from itself, so they must stay clearly visible. Outlines are never eroded by texture.
Texture — none; every surface is uniform soft-matte moulded plastic with a low satin sheen, no grain, no scratches, no fingerprints, and no mirror reflection of the surroundings.
Texture scope — the backdrop is equally clean; no grain, noise, or paper texture anywhere in the frame.
Value architecture — the tile is built from three separated steps so its form reads: front face <色1>, right side face <色2>, underside <色3>; the props sit one step lighter than the face they rest against. Off-white backdrop is the ground and covers about 85% of the area. <强调色> is the single accent, used in exactly three places in the type. Near-black #14161A is the primary type colour. Cool mid-grey #6B7280 is the secondary type colour. Pure white appears only as <logo 位置> and as knocked-out characters inside a <强调色> block.
Light — one large soft key from the upper left, grazing the top-left fillet to produce the specular sweep. The tile casts a two-part neutral cool-grey shadow falling to the lower right, away from the text: a small dense contact shadow immediately beneath it, and a wide soft shadow dissolving within one tile-width.

Composition: Straight-on eye-level camera with an orthographic feel, no perspective distortion in the type. Equal 10% margins on the left and the right, and at least 14% clear backdrop above and below everything in the frame. The text block is left-aligned, begins at 10% of the frame width and never crosses 56%. The tile spans from 64% to 88% of the frame width and about 60% of the frame height, its optical centre at 50% height. The headline's midline sits at exactly that same height, so type and object share one horizontal axis. Ultra-wide 5:2 landscape.

Text in image, three lines sharing one left edge, stacked with fixed spacing:
A short <强调色> horizontal rule sits above the kicker, on the same left edge, about one third the kicker's width and two pixels thick, separated from the kicker by six tenths of the kicker's height.
Kicker: "<kicker>" in a Chinese sans (思源黑体 / Source Han Sans, Regular), cool mid-grey, height about 4% of the frame, widely letter-spaced. The gap between the kicker and the headline is nine tenths of the kicker's height.
Headline, one line, cap height about 15% of the frame height, tight tracking: the first <n> characters "<强调词>" are knocked out in pure white inside a solid <强调色> rounded rectangle whose padding equals eighteen hundredths of the cap height and whose corner radius equals twelve hundredths of the cap height; immediately after the block and on the same baseline, the characters "<尾词>" are set in near-black in the same 思源黑体 / Source Han Sans at Heavy weight. No brackets, no quotation marks.
Subtitle, one line set below the headline by one and a half times the subtitle's own height: "<副标题>" in a light Chinese sans (思源黑体 / Source Han Sans, Light), cool mid-grey, loosely letter-spaced, about 38% the size of the headline; the single <点缀字符> is <强调色> and every other character is mid-grey.
Render all Chinese text verbatim, character for character, no extra words, no translation, no watermark, no caption.

Constraints: the <品牌> mark stays flat, undistorted and aligned to the front face, never warped, stretched, or wrapped around the fillets; <退役旧标与易混标封堵，1–2 条>; the cast shadow never reaches the text block; no glossy piano lacquer, no mirror reflection on the tile, no reflective ground; no more than <n> props and no other objects; no floor line, horizon, table edge, or wall corner; no banding in the backdrop and no vignette; no drop shadow, outline, stroke, or glow on any text; no perspective skew, arc, or italics on the headline; no text or rule crossing the 10% margins. Preserve the three separated value steps on the tile faces, preserve the shallow inset lip on the front face, and preserve the shared left edge of the three text lines.
```

## 槽位清单

编译前逐项确认，缺一项就是漏槽：

- [ ] 品牌名 + **当前** logo 版本（已调研）
- [ ] 退役旧标 / 易混标（进 Constraints）
- [ ] 三档明度色值（正面 / 侧面 / 底面）
- [ ] 强调色（纯黑或品牌主色）
- [ ] 底色冷暖
- [ ] 道具 1–2 件 + 倚靠关系
- [ ] kicker / 强调词 / 尾词 / 副标题四段文字
- [ ] 副标题里的点缀字符（`&`、`·`、`/`）

## 改提示词时

- **一次只改一处**，归因只在版本差异集合里找。
- 质感四维（形体简化度 / 边缘处理 / 纹理性质 / 纹理作用域）互相联动，修质感整段重写，不逐词打补丁。
- 效果不对时**先删修饰再加修饰**——修饰词过多会互相竞争。
- 回退到最近的已知良好版本是合法动作。
