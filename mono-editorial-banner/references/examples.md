# 主体词汇表 · 已验证成品

## 主体词汇表（把一句判断转成一个装置）

先说清这句话讲的是什么**关系**，关系决定装置。装置必须是**叫得出名字的实物**——抽象几何形披层材质皮不算，读者认不出物件，后面全断。

| 文案讲的关系 | 视觉装置 | 黑锚点在哪 |
|---|---|---|
| 表面光鲜 vs 底下代价 | 悬浮的洁白屏幕 / 展台，正下方一团缠结 | 下方那团（线缆、纸屑、夹具） |
| 反复修补后才成立 | 单一实心块体，带焊缝、缺角、打磨痕 | 块体本身 |
| 看不见的东西在承重 | 白色平面 + 沉入黑暗的支撑结构（桥、柱、地基） | 平面之下的整片阴影 |
| 深不见底的积累 | 白色容器（抽屉、匣、井口）打开，内部无底 | 容器内部的虚空 |
| 连锁反应 / 系统性 | 一列多米诺，透视排向消失点 | 骨牌本身 |
| 方向 / 判断 / 校准 | 单一精密仪器（罗盘、天平、卡尺、摆锤） | 仪器主体 |
| 门槛 vs 真正的差异 | 白色机械手指向一个孤立球体 | 球体 |
| 被选中 / 被引用 | 白色堆叠中唯一一片被抽出悬浮的 | 那一片 |
| 复利 / 长期主义 | 巨大飞轮 + 一只白袖手部局部搭在轮缘 | 飞轮 |
| 信号 vs 噪音 | 密集点场中一个孤立的实心体 | 那个孤立体 |
| 入口收窄 / 筛选 | 白色漏斗或闸口，下方汇成一条细流 | 流出的那一股 |
| 断裂 / 不可逆 | 一根横梁断成两截，断口锋利 | 断口与投影 |

选装置的三条判据：**能叫出名字**、**自带一块纯黑**、**只有一处受光**。三条缺一就换装置。

## 完整成品（EN，直接可用）

其余成品只需替换 Subject 句和两行文字，Scene / Key details / Composition / Constraints 逐字不动。

```text
Use case: article cover banner, ultra-wide 5:2 editorial format.

Scene: pure white void; the ground plane is a sparse field of very small fine black dots in receding perspective rows, starting only in the lower third of the frame and fading quickly to clean white toward the horizon; no other environment.

Subject: a photorealistic articulated robotic arm enters from the lower-left edge of the frame, cropped by the frame edge; its mechanical hand reaches forward with the index finger extended toward a perfectly smooth matte pure-black sphere resting on the dotted ground; the sphere casts one single soft contact shadow.

Key details: strict black-and-white palette with extreme tonal purity — the background reads as clean paper white, the black anchor reads as solid ink black, grey exists only as a narrow transition on the subject's own surfaces and never as a field tone; clean studio product-photography lighting with one soft directional key light; the arm's glossy white polymer shell carries a single crisp specular highlight, its joints and cabling are deep black; the sphere is flawlessly smooth with a razor-sharp silhouette; sharp points to preserve: the extended fingertip, the sphere's edge; hard clean edges throughout; photorealistic rendering; mood: minimal, rational, quietly surreal, premium editorial.

Composition: 5:2 horizontal banner; headline centered in the upper 30% of the frame; the arm occupies the lower-left, the sphere sits at about 60% of frame width; at least half of the total image area stays empty clean white.

Text in image: two lines only, centered, rendered as flat solid-black graphic type with no shadow, no bevel, no perspective. Line 1: "PHYSICAL AI" in small, widely letterspaced uppercase serif. Line 2: "DATA IS TABLE STAKES." in very large high-contrast Didone serif with extreme thick-thin stroke contrast and hairline serifs, the first visual focus; size ratio about 1:6. Render all text verbatim, no extra words.

Constraints: no overall grey cast, no mottled grey noise, no film grain, no colour of any kind; no additional text, labels, logos or watermarks; no second competing subject and no scattered props; the dot grid stays sparse and light, never dense enough to read as a dark texture field; the arm stays cropped by the left frame edge; the subject never overlaps or occludes the text.
```

## 已验证 Subject 句（换这一句即换一张图）

以下七条均已出图验证。装配时把 Subject 句整段替换进上面的骨架，改两行文字即可。

**1 · PHYSICAL AI / DATA IS TABLE STAKES.**
> a photorealistic articulated robotic arm enters from the lower-left edge of the frame, cropped by the frame edge; its mechanical hand reaches forward with the index finger extended toward a perfectly smooth matte pure-black sphere resting on the ground; the sphere casts one single soft contact shadow.

*本条的 Scene 用点阵地面（见完整成品），非细线地面。*

**2 · WHAT ACTUALLY SCALES / TRUST IS INFRASTRUCTURE.**
> seen from the side at deck level, the underside of a massive brutalist bridge falls into deep pure black shadow; only the one wider central monumental pillar catches grazing light on its front face; the remaining rows of piers are barely visible, dissolving almost completely into the black void; strict left-right symmetry around the central pillar.

*本条改 Scene 与 Composition：上半纯白 + 白色桥面横贯，deck line 落在画面 55% 高度；追加排除项 `only the central pillar is lit; all other piers stay near-invisible in the black`。这是「单一受光」铁律的教科书案例。*

**3 · DEMO DEBT / THE NEXT NINETY DAYS**
> a pristine glossy white dashboard screen floats in the lower-middle of the empty space, its surface showing clean abstract chart shapes; directly beneath it on the floor sits a single dense tangled knot of black cables, clamps and crumpled paper, one solid black mass casting a hard contact shadow.

*追加排除项：`the chart shapes on the screen stay blurred and unreadable`。屏幕类主体必带这条，否则模型会生成可读小字，抢走主标题。*

**4 · AGE OF BUILDERS / THIRD VERSION.**
> one heavy matte black machined metal block rests alone on the white floor, cube-like and monolithic; three visible weld seams cross its front face, one corner is chipped and one edge shows repair grinding marks; it casts a single hard contact shadow.

*追加排除项：`the block stays solid black and is never lifted to grey`。*

**5 · CONTEXT LAYER / MEMORY IS THE MOAT**
> a single white filing drawer is pulled open from an otherwise invisible white cabinet, floating in the void; the drawer holds no papers — its interior is a bottomless void of pure black, its rim razor sharp where white meets black.

*追加排除项：`the drawer interior stays absolutely black with no visible back wall or contents; no papers or folders`。这条最吃影调纯度，抽屉内出现可见底面即失败。*

**6 · COMPOUNDING EDGE / SYSTEMS OVER SPRINTS**
> a single line of glossy black dominoes stands on the white floor, marching from a large near domino in the foreground into sharp perspective toward a vanishing point, each tile smaller than the last; the nearest tiles show crisp white pips; all cast one continuous hard shadow.

**7 · SIGNAL > NOISE / DECISIONS COMPOUND**
> one precision black compass lies open on the white floor, seen at a low three-quarter angle; its glass face catches a single crisp highlight, the engraved cardinal points and needle rendered in fine white detail against the black case; it casts one hard contact shadow.

## CN 寄存器示例（未出图验证）

中文寄存器已按契约写好，但**尚未出图实测**。首次使用时先出一张验证字形，再批量。

Text 段替换为：

```text
Text in image: two lines only, centered, rendered as flat solid-black graphic type with no shadow, no bevel, no perspective. Line 1: "上下文层" in small, widely letterspaced Chinese Song/Ming serif characters. Line 2: "记忆才是护城河" in a very large high-contrast Chinese Song/Ming serif typeface with thin horizontal strokes, thick vertical strokes and sharp triangular serifs, the first visual focus; size ratio about 1:5. Render every Chinese character exactly as given, with correct and complete strokes; no invented, malformed, simplified-into-nonsense or extra glyphs.
```

Constraints 段末尾追加：`no malformed or invented Chinese characters, no Latin text anywhere in the image.`

出图后逐字核对；连续坏字就走降级路径（Text 段整体换成 `no text anywhere in the image`，后期排字）。

## 成组产出检查

同一批封面出完，并排缩略图看三件事：

1. 地面处理是否一致（全是细线，或全是点阵，不混）；
2. 影调是否一致（有没有某一张明显发灰）；
3. 标题位置和字号是否一致（都在上部 30%，字号比例一致）。

任何一张偏了，只重抽那一张，不动其余——同批次里已经对的图不要为了统一去改提示词。
