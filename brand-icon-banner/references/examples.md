# 品牌寄存器 · 道具库 · 已验证成品

## 品牌寄存器表

三档明度是承重项，**必须分开给值**。下表是起手值，实际以调研到的当前品牌色为准。

| 品牌 | 当前图标版 | 正面 / 侧面 / 底面 | 强调色 | 底色 | 必封堵 |
|---|---|---|---|---|---|
| X | 纯黑砖 + 白色 X 字标 | `#16181C` / `#0A0B0D` / `#050506` | 纯黑 `#000000` | 冷白 | 蓝鸟、任何蓝色 |
| 小红书 | 珊瑚红砖 + 白色手写字标 | `#FF4E58` / `#E23A45` / `#C42F3A` | 珊瑚红 | 暖白 | 微博标、通用红心 / 书本图标 |
| 抖音 | 黑砖 + 青红重影音符 | `#1C1C22` / `#101015` / `#08080B` | 纯黑 | 冷白 | 重影错位过度、音符被拉变形 |
| 微信 | 绿砖 + 白色双气泡 | `#2DC100` / `#23A000` / `#1A7A00` | 绿 | 暖白 | 单气泡、通用聊天图标 |
| Notion | 白砖 + 黑色字标 | `#FFFFFF` / `#EDEDED` / `#D8D8D8` | 纯黑 | 冷白 | 白砖糊进白底——此例必须加强轮廓光 |
| Apple | 银砖 + 黑标 | `#F0F0F2` / `#DCDCE0` / `#C4C4CA` | 纯黑 | 冷白 | 同上，浅色砖靠轮廓光救 |

**浅色品牌（Notion、Apple）有专项风险**：白砖压在近白底上，三档明度差必须拉大，右缘轮廓光要写成 `a pronounced cool rim-light`，否则整枚图标消失在背景里。

## 道具映射表

按文章主题选 **1–2 件**，上限两件。道具是意义层，不是装饰。

| 主题类型 | 道具 | 摆法 |
|---|---|---|
| 分成 / 收益 / 定价 | 两枚薄圆片（硬币尺度） | 一枚倚靠底座，一枚平躺在侧 |
| 实名 / 认证 / 身份 | 一张小卡片 | 斜靠底座，卡面朝外 |
| 算法 / 推荐机制 | 三片平行薄板 | 错层堆叠在底座后方 |
| 隐私 / 权限 / 封禁 | 一枚厚圆片 | 立压在底座正前方，部分遮住底边 |
| 增长 / 流量 | 两根不等高细柱 | 并排立在底座右后方 |
| 版权 / 规则 / 条款 | 一叠薄片 | 平叠在底座左前方，边缘错开 |
| 合并 / 收购 / 竞争 | 第二枚同尺寸小砖 | 侧倒在主砖后方，只露一角 |

最后一条是唯一允许出现第二枚砖的场合，且必须**明确从属**（更小、侧倒、被遮）——两枚平权立砖会毁掉主角关系。

## 已验证成品

主题：X 创作者分成新规则。出图 `2560×1024`，quality `high`。成图见 `../assets/preview.png`。

```
Use case: Ultra-wide editorial header banner for a business-analysis article, 5:2, a three-tier Chinese headline block on the left and one hero object on the right.

Scene: A seamless studio void with no horizon and no floor edge, filled with a clean cool off-white that stays even across the frame and darkens only in a soft neutral falloff around the object on the right. It reads as one continuous lit surface, never as two joined panels.

Subject: On the right, a single thick rounded-square app tile carrying the current X app icon as X uses it today — a pure black tile with the white X mark printed flat on its front face, never the retired Twitter bird. The tile is a solid extruded slab about one fifth as deep as it is wide, with generously rounded corners and softly filleted edges, and its front face carries a shallow inset lip about one twentieth of its width in from the silhouette, giving the object an internal step. It hovers just above the ground plane, rotated about 12 degrees clockwise in plane and angled a few degrees toward the viewer's right, so the right side face and the underside read as two distinct darker planes. Leaning against its lower-left base and lying flat beside it are two thin matte-black discs the size of large coins, catching the same rim light. Nothing else occupies the scene.

Key details:
Form — pure primitive geometry, one squircle prism plus two flat discs, no bevelled facets, no low-poly faceting, no sub-detail.
Edges — crisp and unbroken silhouettes. The fillets carry one soft broad specular sweep along the top-left edge and a thin cool rim-light down the right edge; these two highlights are the only things separating the tile from the backdrop and from itself, so they must stay clearly visible. Outlines are never eroded by texture.
Texture — none; every surface is uniform soft-matte moulded plastic with a low satin sheen, no grain, no scratches, no fingerprints, and no mirror reflection of the surroundings.
Texture scope — the backdrop is equally clean; no grain, noise, or paper texture anywhere in the frame.
Value architecture — the black tile is built from three separated steps so its form reads without any colour: front face #16181C, right side face #0A0B0D, underside #050506; the discs sit one step lighter than the face they rest against. Off-white backdrop is the ground and covers about 85% of the area. Pure black #000000 is the single accent, used in exactly three places in the type. Near-black #14161A is the primary type colour. Cool mid-grey #6B7280 is the secondary type colour. Pure white appears only as the X mark on the tile and as knocked-out characters inside a black block. No colour hue anywhere in the image.
Light — one large soft key from the upper left, grazing the top-left fillet to produce the specular sweep. The tile casts a two-part neutral cool-grey shadow falling to the lower right, away from the text: a small dense contact shadow immediately beneath it, and a wide soft shadow dissolving within one tile-width. No coloured bounce light.

Composition: Straight-on eye-level camera with an orthographic feel, no perspective distortion in the type. Equal 10% margins on the left and the right, and at least 14% clear backdrop above and below everything in the frame. The text block is left-aligned, begins at 10% of the frame width and never crosses 56%. The tile spans from 64% to 88% of the frame width and about 60% of the frame height, its optical centre at 50% height. The headline's midline sits at exactly that same height, so type and object share one horizontal axis. Ultra-wide 5:2 landscape.

Text in image, three lines sharing one left edge, stacked with fixed spacing:
A short pure black horizontal rule sits above the kicker, on the same left edge, about one third the kicker's width and two pixels thick, separated from the kicker by six tenths of the kicker's height.
Kicker: "平台观察" in a Chinese sans (思源黑体 / Source Han Sans, Regular), cool mid-grey, height about 4% of the frame, widely letter-spaced. The gap between the kicker and the headline is nine tenths of the kicker's height.
Headline, one line, cap height about 15% of the frame height, tight tracking: the first five characters "创作者分成" are knocked out in pure white inside a solid pure black rounded rectangle whose padding equals eighteen hundredths of the cap height and whose corner radius equals twelve hundredths of the cap height; immediately after the block and on the same baseline, the three characters "新规则" are set in near-black in the same 思源黑体 / Source Han Sans at Heavy weight. No brackets, no quotation marks.
Subtitle, one line set below the headline by one and a half times the subtitle's own height: "商业分析 & 潜在机会" in a light Chinese sans (思源黑体 / Source Han Sans, Light), cool mid-grey, loosely letter-spaced, about 38% the size of the headline; the single ampersand "&" is pure black and every other character is mid-grey.
Render all Chinese text verbatim, character for character, no extra words, no translation, no watermark, no caption.

Constraints: the X mark stays flat, undistorted and aligned to the front face, never warped, stretched, or wrapped around the fillets; no bird, feather, or avian mark anywhere and no blue of any shade; the cast shadow never reaches the text block; no glossy piano-black lacquer, no mirror reflection on the tile, no reflective ground; no more than two discs and no other props; no floor line, horizon, table edge, or wall corner; no banding in the backdrop and no vignette; no drop shadow, outline, stroke, or glow on any text; no perspective skew, arc, or italics on the headline; no text or rule crossing the 10% margins. Preserve the three separated value steps on the tile faces, preserve the shallow inset lip on the front face, and preserve the shared left edge of the three text lines.
```

### 实测偏离（成图与提示词的差）

这条提示词已验证可用，但成图有两处稳定偏离，用之前先知道：

1. **比 `low satin sheen` 更亮面**。倒角和正面出现了明显的高光带，观感接近半光泽注塑件而不是哑光件。这个偏离让立体感更强，实际上是正向的——**不要为了"贴合描述"去加更多哑光词**，加了会把倒角高光压掉，图标反而塌。
2. **透视强于 `orthographic feel`**。图标带真实近大远小，不是正投影。文字层不受影响（仍是平面无透视），所以这个偏离也可接受。

两处都属于「跑得通就不改」。真要压回哑光正投影，一次只改一处，并做好图标读不出体积的准备。

### 换主题时改的槽

其余逐字照抄。

| 位置 | 换什么 |
|---|---|
| — | **先查该品牌当前 logo 版本** |
| Subject 第一句 | 品牌名 + 版本 + 呈现方式 |
| Value architecture | 三档明度 + 强调色 |
| Subject 末句 | 道具（查道具映射表） |
| Constraints 前两条 | 该品牌的退役旧标 / 易混标 |
| Text 段 | kicker / 强调词 / 尾词 / 副标题 |

强调词保持「四到五字」、尾词「三字」。超过五字反白块会长到压掉右侧留白，图标和文字就撞上了。
