# 编译契约（消歧义铁律）

每次输出前必须满足。这是「成品」和「拼装件」的分界：成品不留任何选项、菜单、占位符。

## 6 条铁律

1. **每个槽位解析成唯一值**：删掉所有 `/` 选项和 `<>` 占位。成品里不允许出现 `chart / list / grid` 这类菜单。
2. **正文零中文**：提示词正文只能出现英文美术指导；唯一例外是「要渲染进画面的标题文字」。任何中文注释一律不留——模型会把它画进画面。
3. **一台笔记本、一张桌子、一个人**：不出现第二台设备、第二块屏、第二个人。
4. **否定只进 Constraints 段**：正文用正向描述，所有 `no / never` 收进末尾 Constraints。**不允许输出独立的 `Negative prompt:` 块**——目标模型没有 negative 通道。
5. **文字精确且只有六处**：kicker、headline 两行、三个卡片标签。必带 verbatim 条款，并明写屏幕与卡片上的其余内容都是无字形的占位条。
6. **不写自相矛盾的裁切**：`fully visible` 与 `cropped by the edge` 不能落在同一个物件上。桌面被裁，笔记本不被裁。

## 物件准确性条款（LOCKED，必带）

这段是本 skill 的存在理由。原始参考稿的所有画面错误都源于这六项没写清。

### 1 单体连续

笔记本必须被描述成**一个完整连续的物件**，而不是"机身 + 屏幕"两个部件的并列。正文里要同时出现三件事：底座压在桌上、上盖由铰链连着底座、两部分共享同一透视。

写法：

```
it is a single continuous object, the keyboard base resting flat on the desk with a tight contact shadow and the lid connected to it at the hinge, both parts sharing exactly the same perspective
```

### 2 屏幕在框内

屏幕 UI 是**画在屏幕边框内部的内容**，不是浮在机身上方的独立面板。必须写明内缩留边、共享屏幕透视平面。

写法：

```
the screen inside the bezel is drawn as a completely flat clean <SCREEN>, inset with an even margin inside the bezel and lying on the screen's own perspective plane, with no halftone texture on it
```

### 3 接触面点名

桌面必须在 **Scene 段**里作为实体存在，不能只在 Composition 里以 "desk edge" 出现。凡是画面里的实体物件（笔记本、杯子、纸），都要写清它落在什么面上、有没有接触阴影。

Scene 段固定尾句：

```
a plain desk surface runs across the lower part of the scene and is the only surface objects rest on
```

### 4 裁切唯一

只有桌面被下边缘裁切。笔记本整机在画内，底边与画面下缘之间留出可见空隙。

写法：

```
only the desk surface is cropped by the bottom edge of the frame; the whole laptop stays inside the frame with clear space between its base and the bottom edge
```

### 5 浅角度

笔记本走**浅角、屏幕近乎正对镜头**。深三分之四角 × 扁平矢量 UI 屏幕是已知最易崩的组合——扁平 UI 在强透视下要么被拉歪，要么被模型摊平成一块贴在机身前的独立画板。

写法：`seen from a shallow angle with the screen turned almost toward the viewer`。

### 6 手部预算与视线

- 一只手做动作，另一只手平放在桌面 / 垂在身侧 / 出画。
- 禁止：碰脸、扶眼镜、双手包握小物、手臂勾椅背、抱臂同时持物。
- 视线必须落在画内已存在的东西上：屏幕、右侧卡片、手上的纸。禁止"看向画外某物"。

## 锁死的风格基座（LOCKED，每条必带）

无论什么主题、哪个配色寄存器，下面四段逐字照抄，只替换 `{{}}` 变量（变量取值见 `module-library.md`）。

**Scene 基座**

```
flat {{BG}} background, completely even with no gradient and no texture; two small clusters of tiny dark dot-grids sit in the upper left and upper right corners; organic {{ORGANIC}} wave shapes anchor the bottom left and bottom right corners, each spanning at least a quarter of the frame width and staying under 18% of the frame height, with a few thin hand-drawn botanical line accents in the same {{ORGANIC}} tone; a plain desk surface runs across the lower part of the scene and is the only surface objects rest on.
```

**Key details 基座**

```
halftone texture applies only to the person, their chair and the laptop body; the laptop screen, all UI cards, the desk, the background and the organic shapes stay perfectly flat and clean. The halftone keeps clear facial features and open mid-tones, never crushing to a solid dark mass and never forming a large uniform grey plane. Every card carries a 1px warm grey hairline border and a tight low shadow with small offset and low opacity, sitting close to the surface. Strict colour roles: {{INK}} for icons, numbers, the kicker and all doodle marks; {{SWASH}} for the brush swash only; {{ACCENT}} for status accents and highlights only; {{ORGANIC}} for the bottom organic shapes and botanical line accents only; {{GREY}} for all placeholder bars, hairlines and borders. Hand-drawn doodle accents used confidently but sparingly: a short curved arrow, one four-point sparkle, two small dashes and a few loose dots — six marks at most, placed asymmetrically near the chip, in the gap between the headline and the person, and above the swash. Flat even lighting with no directional cast light.
```

**Composition 基座**

```
5:2 wide banner, read left to right in four bands with clear breathing room between them: a 4% left margin; then the headline block occupying about 32% of the frame width, left-aligned and vertically centred, dominant by a wide margin; then about 8% of empty background; then the person with their laptop occupying about 24% of the frame width, head close to the top edge; then about 3% of empty background; then the card column occupying about 26% of the frame width, inset 3% from the right edge, with a clear margin of background above the upper card and a visible gap between the two cards. Only the desk surface is cropped by the bottom edge of the frame; the whole laptop stays inside the frame with clear space between its base and the bottom edge. The organic shapes stay in the bottom corners under 18% of the frame height and sit behind everything else.
```

**Constraints 基座**

```
the laptop is one continuous object — no detached or floating screen, no screen panel separated from its base, no second screen, no duplicated or mirrored laptop, no laptop clipping into or overlapping the person's body, and no part of the laptop cropped by any edge of the frame; no extra or missing fingers, no third arm, no hand touching the face, no hand passing through the desk or the laptop; no readable words or sentences on the laptop screen, single letters and numerals used as column labels being the only lettering allowed there; no halftone texture on the laptop screen, the cards, the desk or the background; no white outline around the laptop, desk, chair or any furniture; no photographic colour on the person, strictly black-and-white halftone; no large flat featureless grey plane anywhere; no large soft blurry drop shadows on the cards; no identical structure between the two cards; no long curved arrows spanning across the frame between cards; no accent colour on the botanical line accents; all neutral greys stay warm and never cool or blue-toned, while the palette's own saturated blue, teal, plum or green hues are unaffected; no gradients on the background; no 3D effects, no glassmorphism, no texture on the cards or background; the headline must not overlap the person, the laptop or any card; preserve the flat vector cleanliness of every UI card; no real brand logos, no watermarks.
```

## 固定字段顺序

成品提示词永远按此七段顺序输出，带段落标签：

```
Use case → Scene → Subject → Key details → Composition → Text in image → Constraints
```

## 成品骨架（填好即发，无占位符）

```text
Use case: wide horizontal article cover banner for <TOPIC>, editorial collage style.

Scene: <Scene 基座，填入 {{BG}} 与 {{ORGANIC}}>

Subject: a <ROLE> <POSE, 含视线落点>, rendered as a black-and-white photograph in fine
halftone dot texture, positioned in the middle of the frame between the headline block and
the cards; a clean white sticker outline follows the contour of the person only. One laptop
sits on the desk directly in front of them, seen from a shallow angle with the screen turned
almost toward the viewer: it is a single continuous object, the keyboard base resting flat on
the desk with a tight contact shadow and the lid connected to it at the hinge, both parts
sharing exactly the same perspective; the lid, keyboard base and outer body are rendered in
the same halftone texture with clear edge definition, while the screen inside the bezel is
drawn as a completely flat clean <SCREEN>, inset with an even margin inside the bezel and
lying on the screen's own perspective plane, with no halftone texture and no readable words
on it. A rough
brush-stroke swash in <SWASH>, low saturation, sits behind the person's head and shoulders.
In the right third, two white rounded cards sit stacked with a visible gap between them: the
upper card is <CARD_A>; the lower card is <CARD_B>; one small rounded chip straddles the
lower-left corner of the upper card, overlapping both the card edge and the background,
reading "<CHIP>".

Key details: <Key details 基座，填入五个色变量>

Composition: <Composition 基座逐字照抄>

Text in image: a small all-caps kicker "<KICKER>" in <INK>, and directly beneath it a large
bold black headline "<HEADLINE>" set in two lines — Latin in a heavy geometric sans-serif, Chinese in a heavy Chinese sans (思源黑体 / Source Han Sans, Heavy) — together
occupying the left third; three card labels only: "<LABEL_A>", "<LABEL_B>", "<CHIP>". Every
other piece of copy, on the cards and on the laptop screen alike, is rendered as an abstract
placeholder bar with no letterforms, except for single-letter or numeric column labels.
Render all text verbatim, no extra words.

Constraints: <Constraints 基座逐字照抄><按主体追加的排除项>
```

按主体追加的排除项接在基座后面，**不替换基座**。例：人物手上拿纸时追加 `the sheet of paper stays a single flat rectangle held clear of the face`。

## 出图参数（不进正文）

- size `3200×1280`（5:2；长边 <3840、双边 16 的倍数、比例 ≤3:1、总像素 655,360–8,294,400）
- quality `high`

参数层信息绝不写进提示词正文。

## 迭代纪律

- **一次只改一处**。质感维度互相联动，凭措辞猜因果已实测出过错。
- **效果不对时先删修饰再加修饰**。修饰词过多会互相竞争。
- 笔记本连续出错时，**降级路径**：把 `seen from a shallow angle with the screen turned almost toward the viewer` 换成 `seen straight on, the screen facing the viewer square to the frame`。正面视角把透视问题整个删掉，是最省力的确定性解法。
- 手连续出错时，把动作手也改成 `both hands resting flat on the desk on either side of the laptop`。
- 措辞已到天花板时换工具：编辑模式定点改（`Change only X. Keep everything else exactly the same.`）、同提示词多抽几张再选。
