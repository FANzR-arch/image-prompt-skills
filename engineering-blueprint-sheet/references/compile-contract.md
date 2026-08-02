# 编译契约（消歧义铁律）

每次输出前必须满足。这是「成品」和「拼装件」的分界：成品不留任何选项、菜单、占位符。

## 5 条铁律

1. **每个槽位解析成唯一值**：删掉所有 `/` 选项和 `{}` 占位。成品里不允许出现 `cyanotype / whiteprint / sepia` 这类菜单。
2. **正文零中文**：提示词正文只能出现英文美术指导；唯一例外是「要渲染进画面的标题文字」。任何中文注释一律不留——模型会把它画进图纸。
3. **单一墨色**：一个 PAPER REGISTER 只有一种线色。唯一的第二色是 PRINT-03 AGED 里的手写红笔批注，其余任何情况不许出现第二种颜色。
4. **否定只进 AVOID**：正文用正向描述，所有 `no / not / avoid` 收进末尾 AVOID 块。
5. **主标题精确，标注受控**：主标题必须精确渲染。图面上的次级文字只能是短拉丁字段标签、零件编号和尺寸数字（PROJECT / SCALE 1:2 / SHEET 01 / REV A / N1–N7 / ①–⑧ / 120 / Ø40），tiny、锁网格、有功能感。禁随机日期、URL、假品牌名、成句的说明文字、二维码、真代码。

## 线型分级（LINEWORK，锁死，每条必带）

**这是整套风格的地基。** 所有线一样粗，出来的就是一张蓝色的流程图；线型分开，才是图纸。每条提示词都必须写出一个明确的线型层级：

| 线 | 画法 | 用在哪 |
|---|---|---|
| 轮廓线 outline | 最粗，实线 | 物件外形、节点圆圈、图框外框 |
| 可见细节线 detail | 中等，实线 | 内部结构、连线、次级形状 |
| 尺寸线 dimension | 最细，实线，两端箭头 + 延伸线 | 标注尺寸 |
| 中心线 center | 细，长短点划线 | 对称轴、孔心、爆炸图的装配轴 |
| 隐藏线 hidden | 细，均匀虚线 | 被遮挡的结构、断开的关系 |
| 剖面线 hatching | 极细密平行斜线 | 剖切到的实体截面 |

英文写法（整段可复制，按图面模式删掉用不到的行）：
```
LINEWORK — a strict drafting line hierarchy: thick solid outlines for the main forms, medium solid lines for internal detail, hairline dimension lines with arrowheads at both ends and short extension lines, thin long-short dash-dot center lines through every axis of symmetry, thin evenly dashed hidden lines for anything occluded, and fine closely-spaced diagonal hatching inside any cut section.
```

## 三寄存器预设（PAPER 段和 QUALITY 段按此替换）

**CYANOTYPE（默认）**
```
PAPER — a deep Prussian-blue cyanotype sheet; every line, glyph and label is printed in white drafting ink; flat printed line-art with no photographic depth, no gradient fill, no glow.
QUALITY — authentic cyanotype blueprint print, crisp white linework holding up through the paper texture, precise drafting alignment, real paper tooth.
```

**WHITEPRINT（可选）**
```
PAPER — a warm off-white drafting sheet; every line, glyph and label is printed in deep indigo diazo ink; flat printed line-art with no photographic depth, no gradient fill, no glow.
QUALITY — authentic diazo whiteprint, crisp indigo linework holding up through the paper texture, precise drafting alignment, real paper tooth.
```

**SEPIA（可选）**
```
PAPER — an aged tan drafting sheet; every line, glyph and label is printed in dark sepia-brown ink; flat printed line-art with no photographic depth, no gradient fill, no glow.
QUALITY — authentic aged sepia drawing print, crisp brown linework holding up through the paper texture, precise drafting alignment, real paper tooth.
```

## 制图装置清单（DRAFTING APPARATUS）

图纸的可信度住在这里。按画幅决定装几件：

| 装置 | 封面 5:2 | 插图 16:9 | 图纸 3:2 |
|---|---|---|---|
| 图框 + 四边分区标注（A B C / 1 2 3） | ○ 压暗 | — | ● 必带 |
| 右下标题栏（ruled cells，字段填满） | ● 必带 | ○ 缩成一个小标签 | ● 必带且完整 |
| 修订表 REV / DATE / BY | — | — | ● 必带 |
| 尺寸标注线 + 箭头 + 数字 | ○ 少量 | ○ 少量 | ● 成套 |
| 引线 leader + 气泡编号 | ● 两三处 | ● 关键处 | ● 成套 |
| 比例尺 scale bar 带刻度 | ● | ● | ● |
| 角部定位十字标 registration marks | ● | ● | ● |

标题栏字段用这几个：`PROJECT / TYPE / SCALE / DATE / SHEET / DRAWN BY / REV`。

**实测坑：只在 APPARATUS 段写 `every cell filled` 没用，模型会把字段名画上、右边格子留空。** 必须在 TEXT 段里把每一格的**值**当成要渲染的文字逐条列出来，写成 `字段 / 值` 的成对形式：

```
TEXT — ... the title block cells read PROJECT / FLOW-01, TYPE / TOPOLOGY, SCALE / 1:1, SHEET / 01, DRAWN BY / AI ...
```

值用短拉丁代号和数字，别用真实姓名和真日期。空表格一眼假，比不画标题栏更糟。

## 四种图面模式（DOMINANT VISUAL 按此写）

**TOPOLOGY 流程拓扑**
```
DOMINANT VISUAL — one wide node-and-edge topology drawn as a drafting diagram: <入口 / 分支 / 汇合 / 出口的实际结构>; nodes are thick-outlined circles each holding a small line-icon and a short code label; edges are medium solid lines with small solid junction dots and arrowheads at their ends; two leader lines with arrowheads annotate individual nodes.
```

**ORTHOGRAPHIC 三视图**
```
DOMINANT VISUAL — three orthographic projections of <物件> arranged in standard drafting layout: front elevation at lower left, side elevation to its right, top plan directly above the front view, all three aligned on shared projection lines; dash-dot center lines run through every axis; dashed hidden lines show the internal structure; a full set of hairline dimension lines with arrowheads brackets the overall height, width and two key features.
```

**EXPLODED 爆炸图**
```
DOMINANT VISUAL — an exploded assembly of <物件> pulled apart along one diagonal dash-dot assembly axis: <N> components float in sequence along the axis, each aligned to the next by thin dashed alignment lines; every component carries a leader line ending in a numbered circular balloon; a small ruled parts table in one corner lists the balloon numbers against short Latin part names.
```

**DETAIL 详图剖面**
```
DOMINANT VISUAL — a main view of <物件> with one area circled by a thin closed detail bubble labeled DETAIL A, and a magnified DETAIL A view placed to its side at a stated larger scale; a section cut line with two heavy end arrows crosses the main view labeled A-A, and the cut face in the enlarged view is filled with fine diagonal hatching.
```

## 三档纸张质感（PRINT TEXTURE）

**一句话原则：质感盖在图之上，永远不吃线条和数字。** 折痕压过图面，但压不糊——缩略图状态下标注还认得出来。整篇统一一档。用户没指定用 **PRINT-02**。

**PRINT-01 CLEAN（轻）** — 标注密集的图纸、超长标题封面
```
PRINT TEXTURE — the whole frame is a photograph of a real drafting sheet: fine paper tooth runs throughout, the ink density varies slightly with a few lighter patches where the print washed out, and the outer edges fade very gently. Every line, letter and dimension figure stays sharp and fully legible through the texture.
```

**PRINT-02 STANDARD（默认）** — 封面和大多数插图
```
PRINT TEXTURE — the whole frame is a photograph of a real drafting sheet. Fine paper tooth runs throughout, crossed by faint horizontal press-roller banding at even spacing. Ink density is uneven, with lighter patches where the print washed out and heavier pooling along some lines. Two soft fold creases run through the sheet, catching a little light along their ridges. The edges fade, the corners darken, and a few specks of dust and fibre sit on the surface. Every line, letter and dimension figure stays sharp and fully legible through the texture.
```

**PRINT-03 AGED（重）** — 讲旧、讲档案、讲被翻烂的东西
```
PRINT TEXTURE — the whole frame is a photograph of an old, heavily handled drafting sheet. Fine paper tooth runs throughout, crossed by faint horizontal press-roller banding. Ink density is blotchy and washed out in patches, with a soft ghost of an earlier copy showing through. Deep fold creases quarter the sheet, the corners are dog-eared and one edge carries a small tear; four pin holes sit at the corners. A pale ring stain and a few scattered foxing spots mark the paper. A handful of terse handwritten marks in red pencil annotate two spots on the drawing. Every printed line, letter and dimension figure stays sharp and fully legible through the wear — the aging stays under the drawing, never on top of it.
```

PRINT-03 是唯一允许第二色的档：红笔批注只能是短记号（一个圈、一个箭头、`REV`、`OK`），不能是成句的手写文字。

## 固定字段顺序

成品提示词永远按此顺序。质感排在 TEXT 之后、AVOID 之前——它是盖在画完的图纸上的一道后期，不是画的内容：

```
STYLE ANCHOR  →  FORMAT(锁死画幅)  →  PAPER(按寄存器)  →  LINEWORK(线型分级)
→  [LAYOUT(带大标题的封面必带)]  →  DOMINANT VISUAL(按图面模式)  →  [TITLE TREATMENT(封面)]
→  DRAFTING APPARATUS  →  TYPOGRAPHY  →  TEXT(要渲染的文字, 声明一次)
→  PRINT TEXTURE(按质感档)  →  AVOID  →  QUALITY(按寄存器)
```

## 成品骨架（填好即发，无占位符）

```text
STYLE ANCHOR — a real engineering drawing sheet: <图面模式> drafted to standard, printed as <register flavor>.

A <5:2 landscape / 16:9 / 3:2 landscape> sheet.

PAPER — <粘贴对应寄存器的 PAPER 段>

LINEWORK — <粘贴线型分级段，删掉用不到的行>

DOMINANT VISUAL — <粘贴对应图面模式段并解析成唯一内容>

DRAFTING APPARATUS — a ruled border with zone letters down the sides and zone numbers along the top and bottom; a ruled title block in the lower right with every cell filled (PROJECT / TYPE / SCALE / DATE / SHEET / DRAWN BY); <按画幅增删修订表 / 尺寸标注 / 气泡编号>; a scale bar with tick marks along one edge; small registration crosses at the corners.

TYPOGRAPHY — Latin labels, codes and figures in technical drafting lettering, uppercase, evenly spaced; any Chinese title set in a heavy condensed Chinese sans (思源黑体 / Source Han Sans, Heavy) with solid filled strokes.

TEXT — <封面: main title must render exactly: 主标题 / 图纸: no large title>. The title block cells read <PROJECT / 值, TYPE / 值, SCALE / 值, SHEET / 值, DRAWN BY / 值 —— 每格都给出值，不留空>. All other text is short Latin field labels, part codes and dimension figures only; no random dates, URLs, fake brands, full sentences, QR codes, or real code.

PRINT TEXTURE — <粘贴选中的质感档>

AVOID — any colour beyond the single register ink; neon green, phosphor glow, bloom, scanlines or any screen texture; uniform line weight with no hierarchy; empty unfilled title-block cells; dimension lines without arrowheads or figures; photographic objects or depth of field inside the drawing itself; 3D rendering; glossy sheen; a visible desk, hands, drafting tools or room around the sheet; heavy display poster type; dense unreadable blocks of technical prose.

QUALITY — <粘贴对应寄存器的 QUALITY 段>
```

## 封面标题图文分离铁律（防止字和图糊在一起）

封面的巨型标题和图面同处一块纸、又同为一种墨色，最容易糊成一团。凡是带大标题的封面，必带下面四条，缺一即改：

1. **留净空 + 线绕行**：中央横向留一条净空带给标题；图面的连线从标题的上方和下方绕过去，**绝不从标题正后方穿过**（`lines never cross behind the title`，写进 LAYOUT，并进 AVOID）。
2. **实心 vs 线稿分层**：图纸没有辉光可用，分层只能靠实心度——标题是**实心满墨的粗体块字**（`solid heavy ink, fully filled letterforms`），图面是**细的空心线稿**。这是最有效的手段。
3. **字重分层**：标题粗重，制图线细。制图装置整体压淡，不与标题争。
4. **底板 knockout**：标题坐在一块与纸同色的底板上、带留白、外框一圈细线，物理切断任何经过其后的线（`a knockout plate in the paper colour with a thin ruled border that interrupts any line behind it`）。

插图和纯图纸通常没有大标题，不受本节约束；一旦要放大标题，同样套这四条。

## 招牌装置一致性（批量成系列的关键）

同一篇文章的封面 + 所有插图，必须共享：

1. 同一个 PAPER REGISTER；
2. 同一档 PRINT TEXTURE（一字不改地复制粘贴，要降就整篇一起降）；
3. 同一套线型分级；
4. 同一套制图装置写法（标题栏字段名、比例尺、角标一致）。

**只有 DOMINANT VISUAL 和封面主标题变。** 出图后并排缩略图检查：一眼能认出是同一套图纸。

## 和 tech-schematic-poster 的边界

两个 skill 长得像，但载体不同，元素不能串：

| | engineering-blueprint-sheet（纸） | tech-schematic-poster（屏） |
|---|---|---|
| 线 | 分级：粗轮廓 / 细尺寸 / 点划中心 / 虚线隐藏 | 全部等粗细 |
| 光 | 无。印上去的墨 | 辉光、bloom、halation |
| 质感 | 纸纹、折痕、水渍、图钉孔 | 扫描线、荧光颗粒、屏幕弧度、烧屏 |
| 框 | 图框分区 + 标题栏 + 修订表 | HUD 面板 + 图例 + 系统日志 |
| 字 | 制图手写体 / 技术字 | 等宽字 |

用户要「蓝图风」走这个；要「终端 / HUD / 赛博」走那个。两个都想要就出两张，不要合成一张。
