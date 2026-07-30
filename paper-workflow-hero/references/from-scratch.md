# 从零生成：母版 + 模块库

母版分两层，改法不同：

- **风格层**（Key details / Constraints）——逐字照抄，任何主题任何张数都不动；
- **调度层**（Composition / 人物 / 桌面道具）——**每张必须重抽**，从下方三张模块库各选一项，同一组内不得重复。

`{{…}}` 是内容空槽，`[[…]]` 是调度槽（从模块库填）。

## 母版

```
Use case: wide marketing hero illustration for {{TOPIC}}, landing-page key visual, [[RATIO]].

Scene: a single warm cream paper background, one uniform ivory tone with a very subtle paper grain, soft even ambient light; an editorial flowchart tableau; [[SURFACE]].

Subject: a flowchart built from mixed physical and UI elements, read in one clear order:
- inputs: three off-white rounded UI cards, each with one thin purple line icon and one short label, reading "{{INPUT_1}}", "{{INPUT_2}}", "{{INPUT_3}}";
- core: {{CENTRAL_PROP}}, a real tactile object rendered photorealistically, carrying the core metaphor, with a small physical label on its front reading "{{CENTRAL_LABEL}}", and {{CENTRAL_PROP_DETAIL}};
- standards: a tall off-white UI card titled "{{RULES_TITLE}}", listing {{RULES_ITEMS}} as short lines each marked with a small purple check icon, thin divider lines above and below the list, and a small purple footer note "{{RULES_FOOTER}}";
- output: a neat stack of layered paper sheets with realistic paper edges, the top sheet reading "{{OUTPUT_TITLE}}" with a smaller subline "{{OUTPUT_SUBLINE}}" and one large purple circled checkmark;
- feedback loop: a small UI card with a purple growth-chart line icon captioned "{{LOOP_LABEL}}", a purple pill badge on the loop line reading "{{LOOP_BADGE}}", the line returning into the core object;
- one orange sticky note pinned with a realistic metal pushpin, slightly rotated, holding a simple white glyph and the words "{{STICKY_TEXT}}";
- people: [[PEOPLE]];
- on the surface near them: [[TABLE_PROPS]].

Key details: three rendering registers coexist and must stay distinct — flat UI cards (matte off-white, rounded corners, soft diffuse drop shadows, thin purple line icons, clean humanist sans labels, no gradients), photoreal tactile props (visible fabric weave, metal, layered paper edges, soft contact shadows), and painted semi-realistic people (warm natural skin tones, soft brushed edges, fine canvas grain, no outlines, not photographic). All connectors are medium-weight deep-violet lines with rounded right-angle bends and small solid triangular arrowheads. One single deep-violet accent used for every icon, connector, checkmark and badge; one saturated orange allowed only on the sticky note. Lighting soft and warm from the upper left, shadow direction identical across cards, props and people.

Composition: [[LAYOUT]] Generous cream breathing room around every element.

Text in image: headline "{{HEADLINE_LINE_1}}" and "{{HEADLINE_LINE_2}}" in a large elegant high-contrast serif, near-black forest green, [[HEADLINE_PLACEMENT]]; all card labels and list items in a clean humanist sans; tagline "{{TAGLINE}}" in a smaller serif with only the word "{{TAGLINE_ACCENT_WORD}}" in the accent violet; render all text verbatim, no extra words.

Constraints: no glossy 3D plastic render, no gradients or glassmorphism on cards, no neon colors, background stays one clean cream tone with no texture buildup, people painted not photographic and never outlined, no photo-collage seams between people and background, main figure never looks at the viewer, connector lines never cross card interiors, no more than six diagram nodes, no real brand logos or watermarks, shadow direction identical everywhere, render all text verbatim.
```

参数层：5:2 用 2560×1024，16:9 用 2560×1440，3:2 用 2496×1664。

## 内容空槽对照

| 空槽 | 填什么 | 例 |
|---|---|---|
| `{{TOPIC}}` | 一句话产品/服务定位 | an AI-native service that runs delegated work |
| `{{INPUT_1..3}}` | 三个输入渠道，1–2 词 | Community / Requests / Support |
| `{{CENTRAL_PROP}}` | 从道具库选 | a linen-covered card-catalog box |
| `{{CENTRAL_PROP_DETAIL}}` | 道具内容物 | four tabbed index cards inside reading "Policies", "Processes", "Preferences", "History" |
| `{{CENTRAL_LABEL}}` | 核心概念，1 词 | Context |
| `{{RULES_TITLE/ITEMS/FOOTER}}` | 标题 / 3–5 短项 / 脚注 | Standards / "Tone", "Quality", "Approvals", "SLAs" / Set once |
| `{{OUTPUT_TITLE/SUBLINE}}` | 交付物 / 结果句 | Work delivered / On standard. On time. |
| `{{LOOP_LABEL/BADGE}}` | 回流机制 / 徽章短语 | Improves as it goes / Keeps running |
| `{{STICKY_TEXT}}` | 便利贴，≤3 词 | AI-native services |
| `{{HEADLINE_LINE_1/2}}` | 两行对仗短句 | Hand over the work. / Get the result. |
| `{{TAGLINE}}` / `{{..._ACCENT_WORD}}` | 收尾句 / 其中变紫的词 | You set the standards. Quill keeps it running. / Quill |

---

# 调度模块库

**抽取规则**：三张表各抽一项，同组内不重复。成组产出前先把整组抽取结果列成表，确认无重复再编译。

## 表一 · 版式（填 `[[LAYOUT]]` `[[SURFACE]]` `[[HEADLINE_PLACEMENT]]` `[[RATIO]]`）

**表一只管人物在哪、多大、什么景别；表二只管几个人、在做什么。** 两表冲突时以表一的景别为准，换一个表二项——不要把姿态写回表一，那正是首轮五图雷同的成因。

| | 画幅 | 人物区 | 可配表二 |
|---|---|---|---|
| A | 5:2 | 右 30%，坐桌前，齐腰裁切 | 全部 |
| B | 5:2 | 左 28%，坐桌前，齐腰裁切 | 全部 |
| C | 16:9 | 底缘一条带，稍高机位背面 | ⑦⑨⑪⑫ |
| D | 3:2 | 桌子远端 + 近端边缘 | ①③⑥⑨⑩⑫ |
| E | 5:2 | 正中单人 | ②④⑦⑧⑩⑪ |
| F | 16:9 | 右下角，占画高约 1/6，全身 | ①③④⑤⑧ |
| G | 4:5 | 右下角，胸口裁切 | ②④⑦⑧⑩⑪ |

### A · 右侧人物带（源图版）

- `[[SURFACE]]`：a plain light table surface at the bottom right merging into the background
- `[[LAYOUT]]`：5:2 horizontal. The flowchart occupies the left 65–70% of the width, reading strictly left to right with the feedback loop along its bottom edge; the people occupy the right 30%, seated at the table and cropped at the waist by its edge.
- `[[HEADLINE_PLACEMENT]]`：at top center-left, its top edge at roughly 8% of frame height

### B · 人物在左（镜像）

- `[[SURFACE]]`：a plain light table surface at the bottom left merging into the background
- `[[LAYOUT]]`：5:2 horizontal. The people occupy the left 28% of the frame, at the table and cropped at the waist by its edge; the flowchart fills the right 70%, reading left to right with the feedback loop along its bottom edge.
- `[[HEADLINE_PLACEMENT]]`：at top right, right-aligned, its top edge at roughly 8% of frame height

### C · 上下分层

- `[[SURFACE]]`：a long light desk running across the lower third of the frame
- `[[LAYOUT]]`：16:9 horizontal. The flowchart spans the full width of the upper two thirds, reading left to right with the feedback loop dropping below it; the people occupy a shallow band along the bottom edge, seen from behind and slightly above, only heads and shoulders breaking into frame.
- `[[HEADLINE_PLACEMENT]]`：at top left, its top edge at roughly 6% of frame height

### D · 桌面俯视

- `[[SURFACE]]`：a wide light wooden desk seen from a raised three-quarter angle, all elements resting on it
- `[[LAYOUT]]`：3:2 horizontal, viewed from an elevated three-quarter angle looking down at the desk. The flowchart lies flat across the desk surface in slight perspective, reading from the near-left to the far-right; the people are placed at the far side of the desk and at its near edge, hands and forearms prominent in the foreground.
- `[[HEADLINE_PLACEMENT]]`：at top center, its top edge at roughly 7% of frame height

### E · 人物居中·图表环绕

- `[[SURFACE]]`：a light table running the full width of the lower frame
- `[[LAYOUT]]`：5:2 horizontal. A single figure sits at the center of the frame at the table in three-quarter view; the input cards and core object cluster to their left, the standards card, output stack and loop to their right, so the diagram wraps around them and still reads left to right.
- `[[HEADLINE_PLACEMENT]]`：spanning the top of the frame above everything, its top edge at roughly 6% of frame height

### F · 人物远小·图表主导

- `[[SURFACE]]`：a pale floor and a low table in the lower right, receding slightly
- `[[LAYOUT]]`：16:9 horizontal. The flowchart is large and dominant across the upper left three quarters; the people appear small in the lower right at roughly one sixth of the frame height, full figures visible, giving a sense of scale.
- `[[HEADLINE_PLACEMENT]]`：at top left, its top edge at roughly 6% of frame height

### G · 竖版（社媒用）

- `[[SURFACE]]`：a light table across the bottom of the frame
- `[[LAYOUT]]`：4:5 vertical. The flowchart stacks top to bottom down the upper two thirds, reading downward with the feedback loop curving back up the left side; a single figure occupies the lower right corner, cropped at the chest by the frame edge.
- `[[HEADLINE_PLACEMENT]]`：at the very top, centered, its top edge at roughly 5% of frame height

## 表二 · 人物（填 `[[PEOPLE]]`）

写进母版时全部前缀 `painted in a warm semi-realistic editorial style,`。至少一位主要人物注意力在图表上；配角可以看对方、看手里的东西或闭眼想，但**没有人看镜头**。

| # | 调度 |
|---|---|
| 1 | two people seated side by side, one resting a hand on their chin in thought, the other pointing toward the diagram, both gazes on the flowchart |
| 2 | one person standing and leaning forward with both palms flat on the table, studying the diagram closely |
| 3 | two people mid-conversation turned toward each other, one gesturing back at the diagram without looking at it, the other following the gesture |
| 4 | one person seated leaning back in a chair with arms crossed, head tilted, considering the diagram from a distance |
| 5 | three colleagues clustered together, one crouching to point at the feedback loop, two standing behind |
| 6 | one person reaching out to lift the top sheet off the output stack, the other watching their hand |
| 7 | one person writing in a notebook without looking up, a second beside them tracking the diagram |
| 8 | one person half-turned away mid-stride, glancing back over their shoulder at the diagram |
| 9 | two people seated at opposite ends of the table, one sliding a physical index card across toward the core object |
| 10 | one person holding a small printed card up beside the diagram, comparing the two |
| 11 | one person seen from behind over the shoulder, facing the diagram, face not visible |
| 12 | only two hands entering from the frame edge, one pointing at the diagram, the other resting on the table, no face in frame |

## 表三 · 桌面道具（填 `[[TABLE_PROPS]]`）

抽 0–2 件，**每张换掉**。首轮五图全部自动生成了同一组「马克杯 + 摊开的笔记本」，不点名就会默认长这样。

| # | 道具 |
|---|---|
| 1 | nothing — the surface is bare |
| 2 | a single ceramic mug, no other objects |
| 3 | an open notebook and a pen |
| 4 | a closed laptop pushed to one side |
| 5 | a loose scatter of index cards |
| 6 | a small potted plant at the far edge |
| 7 | a pair of eyeglasses folded on the surface |
| 8 | a phone face-down and a paper coffee cup |
| 9 | a shallow tray of pens and a roll of tape |
| 10 | a stack of printed sheets with one sheet pulled aside |

---

# 中心道具库（内容层，不属调度）

- a linen-covered card-catalog box with tabbed index cards（知识 / 上下文 / 积累）
- a wooden drawer half-pulled from a cabinet, papers filed inside（档案 / 沉淀）
- a letterpress type tray holding metal type pieces（内容 / 出版 / 组装）
- a brass balance scale with paper notes on both pans（权衡 / 评估）
- a wooden toolbox with worn hand tools（执行 / 手艺）
- a rolodex with flipped address cards（关系 / 客户）
- a canvas mail sorting bag with bundled letters（分发 / 信息流）
- a brass hotel desk bell on a wooden base（服务 / 响应）
- a wooden block tower mid-build（依赖 / 稳定性）
- a large magnifying glass resting over a printed sheet（筛选 / 审查）

选择标准：能一眼隐喻核心概念，且是**可拍摄的日常实物**。概念性物体（大脑、云、机器人）一律不选。

# 色板变体（只换色，其余不动）

把母版里 cream/ivory、deep-violet、forest green、orange 四个色名整体替换，一次全换，不混搭。

| 变体 | 底 | 主 accent | 标题 | 单点暖色 |
|---|---|---|---|---|
| 默认 | warm cream / ivory | deep violet | near-black forest green | saturated orange |
| 墨绿信笺 | pale sage paper | deep forest green | near-black ink | brick red |
| 灰纸墨蓝 | cool light-grey paper | deep ink blue | near-black charcoal | marigold yellow |
| 暖沙陶土 | warm sand paper | burnt terracotta | dark espresso brown | teal |
