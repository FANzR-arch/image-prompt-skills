# 编译契约（消歧义铁律）

每次输出前必须满足。这是「成品」和「拼装件」的分界：成品不留任何选项、菜单、占位符。

## 6 条铁律

1. **每个槽位解析成唯一值**：删掉所有 `/` 选项和 `<>` 占位。成品里不允许出现 `watercolor / ink / marker` 这类菜单。
2. **正文零中文**：提示词正文只能出现英文美术指导；唯一例外是「要渲染进画面的标题文字」。任何中文注释一律不留——模型会把它画进画面。
3. **三色板闭合**：Key details 段必须点名整张图只用哪三个色相，并写明皮肤、服装、道具、背景全部收进这三个色相。不写这句，背景会漏环境色。
4. **遮挡关系必须显式写出**：`the second line passing behind the subject's head and shoulder so the letters are partially occluded`。这句是本风格的身份特征，任何情况下不得省略、不得改写成 `behind the subject`（太模糊，模型会把整行推到人后）。
5. **否定只进 Constraints 段**：正文用正向描述，所有 `no / never` 收进末尾 Constraints。**不允许输出独立的 `Negative prompt:` 块**——目标模型没有 negative 通道。
6. **文字精确且只有四类**：标题两行、品类标签、三个序号、不可读占位行。必带 verbatim 条款。不允许模型自行补字、缩写、翻译或加装饰标点。

## 锁死的风格内核（LOCKED，每条必带）

无论什么主体、哪个寄存器，这几段的**结构**逐字照抄，只替换 `<>` 里的值。

**Scene 基座**

```
a flat, solid <COLOUR> background with no gradient; <GRADE> grade over the whole image.
```

`<GRADE>` 从色场表取，例：`warm, matte, low-contrast vintage editorial`、`hard-contrast daylight`、`rich low-key matte`。

**Key details 基座**

三句，缺一不可，顺序不动：

```
<LIGHT>; skin, <SUBJECT MATERIALS> and background all harmonized into one <C1>-<C2>-<C3> palette; a painted <BRIDGE OBJECT> in <MEDIUM> overlaps the <CORNER> foreground, bridging the photo layer and the graphic layer.
```

- 第一句是光：方向 + 硬度 + 阴影描述。
- 第二句是三色板闭合，`<SUBJECT MATERIALS>` 点名画面里出现的实际材质（hair、linen、clay、kit……）。
- 第三句是桥接元素。`<CORNER>` 取光源对侧下角。

**Composition 基座**

整段照抄，只换 `<HEADLINE COLOUR>` 和寄存器差异项：

```
vertical cover layout; an oversized <HEADLINE COLOUR> display headline in tall condensed capitals spans the top third edge-to-edge, with the second line passing behind the subject's head and shoulder so the letters are partially occluded; an editorial layout system surrounds the subject: a small label with two short placeholder body-text blocks upper left, index numbers with <RULE WEIGHT> rules along the <RULE EDGE>, a <TICK WEIGHT> tick row <TICK CORNER>; <MARGIN>, <GRID>.
```

**Text in image 基座**

```
headline "<W1>" on the first line and "<W2>" on the second line, in oversized tall condensed <HEADLINE COLOUR> capitals; label "<CATEGORY> FEATURE" in small letter-spaced <HEADLINE COLOUR> capitals, upper left; index numbers "01", "02", "03" in small <HEADLINE COLOUR> figures beside <RULE WEIGHT> rules; all other text blocks are tiny illegible placeholder lines. Render the specified words verbatim, no extra readable words.
```

**Constraints 基座**

```
no logos, no watermark, no UI icons or buttons, no readable text other than specified; keep the background a single flat colour with no gradient or scenery; the painted foreground element stays clearly hand-painted and sits in front of the photograph, never rendered as a real physical object; the subject's hands are either out of frame or clearly holding one named object.
```

按主体追加的排除项接在基座后面，不替换基座。常用追加项：

- 运动 / 有品牌风险的服装：`no brand marks on the clothing or kit`
- 美妆 / 特写：`no visible retouching artefacts, no plastic skin`
- 有器物在手：`the <OBJECT> stays a single continuous solid form`

## 两个排版寄存器（Composition 与 Text 段按此替换）

寄存器一动，下表五项**全部**跟着换。只改一两项会得到一张四不像。

| 参数 | CLEAN（默认） | ROUGH |
|---|---|---|
| `<RULE WEIGHT>` | `thin` | `thick` |
| `<RULE EDGE>` | `the right edge` | `the left edge` |
| `<TICK WEIGHT>` + `<TICK CORNER>` | `thin` + `lower left` | `dense` + `lower right` |
| `<MARGIN>` | `generous margins` | `tight margins` |
| `<GRID>` | `everything aligned to a clean grid` | `elements slightly off-grid` |

CLEAN 另可在 Composition 段插 `a small barcode-like tick row on the left` 增密；ROUGH 把编辑系统整段前缀改成 `a deliberately rough editorial layout surrounds the subject`。

## 标题选词约束（承重项）

遮挡效果完全由第二行的长度决定，选词阶段就要定死：

- **第一行**：3–6 个字母的短词。
- **第二行**：6–9 个字母的长词。这行要横跨画面、宽到能被头肩截断。第二行短于 6 个字母，遮挡就不会发生。
- 两行都全大写、压缩体、无标点。
- **标题色 = 三色板里明度离底色最远的那个**。深底配浅字（象牙 / 奶油），高明度底配深字（黑）。这条不判断会得到一张糊在一起的封面。
- 品类标签固定句式 `<CATEGORY> FEATURE`，一个词 + FEATURE。

**中文标题未实测**：四条实测全是拉丁字母，`tall condensed capitals` 是拉丁字形特征，中文没有对应物。用户要中文时，把 Composition 和 Text 里的 `tall condensed capitals` 整体换成 `an oversized headline in a heavy condensed Chinese sans (思源黑体 / Source Han Sans, Heavy)`，删掉 `capitals`。字形逐字核对；笔画多的字偶尔会糊，多生成两张挑，不要退回后期排字。

## 固定字段顺序

成品提示词永远按此七段顺序输出，带段落标签：

```
Use case → Scene → Subject → Key details → Composition → Text in image → Constraints
```

## 成品骨架（填好即发，无占位符）

```text
Use case: <CATEGORY> magazine cover poster, vertical format, headline typography baked into the image.

Scene: <Scene 基座>

Subject: <人物描述——年龄气质 + 发型 + 表情与视线 + 服装（点名材质与颜色，收进三色板）+ 景别 + 姿态 + 手部处理>. Photorealistic <GENRE> photography.

Key details: <Key details 基座三句>

Composition: <Composition 基座，按寄存器替换五项>

Text in image: <Text in image 基座>

Constraints: <Constraints 基座><按主体追加的排除项>
```

## 出图参数（不进正文）

- size `2048×3072`（2:3；长边 <3840、双边 16 的倍数、比例 ≤3:1、总像素 655,360–8,294,400）
- quality `high`

参数层信息绝不写进提示词正文。

## 迭代纪律

- **一次只改一处**。色场、光位、桥接元素三者互相联动，凭措辞猜因果容易归错因。
- **效果不对时先删修饰再加修饰**。修饰词过多会互相竞争。
- **已验证有效的提示词不为了合规去改**。回退到最近的已知良好版本是合法且常常最优的动作。
- 遮挡没发生时，**先查第二行词长**，再考虑改措辞——八成是词太短，不是句子写得不对。
- 桥接元素被画成真实物体时，往 Constraints 追加按名封堵，不要在 Key details 里堆更多绘画形容词。
