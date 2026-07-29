# 编译契约（消歧义铁律）

每次输出前必须满足。这是「成品」和「拼装件」的分界：成品不留任何选项、菜单、占位符。

## 5 条铁律

1. **每个槽位解析成唯一值**：删掉所有 `/` 选项和 `{}` 占位。成品里不允许出现 `green / cyan / amber` 这类菜单。
2. **正文零中文**：提示词正文只能出现英文美术指导；唯一例外是「要渲染进画面的标题文字」。任何中文注释一律不留——模型会把它画进海报。
3. **单一色相**：REGISTER 只保留一个。TERMINAL = 一种霓虹绿；BLUEPRINT = 蓝底白线 + 最多一个强调色。绝不并列两套配色。
4. **否定只进 AVOID**：正文用正向描述，所有 `no / not / avoid` 收进末尾 AVOID 块。
5. **主标题精确，次级 micro-text 受控**：主标题必须精确渲染（如 `从 Loop 到 Graph`、`GRAPH`）。次级小字只能是短拉丁字段标签（NODE / EDGE / FAN-OUT / A1–A6 / MERGE / EXIT / [ok] / timestamps），tiny、锁网格、有功能感。禁随机日期、URL、假品牌名、长段落、二维码、真代码块。

## 锁死的风格内核（LOCKED，每条必带）

无论封面还是插图、哪个寄存器，这几条恒定：

- 主视觉是**一张节点-连线拓扑图**：节点为细描圆圈，连线为均匀细线，连线上有发光小圆点当数据流；
- 一层 **HUD 仪表框**：角落数据面板（PROJECT / TYPE / VERSION 类短标签）、图例（key NODE / EDGE / FLOW）、边缘标尺带刻度、底部系统日志行；
- **等宽字体**贯穿全图；
- **平面**，无照片景深、无写实材质、无渐变填充（发光辉光除外）；
- 层级靠尺度和位置，不靠装饰花纹。

## 两寄存器预设（LOCKED 段按此替换）

**TERMINAL（默认）**
```
LOCKED — pure black background; a single neon-green phosphor color for every line, node, glyph and label; thin uniform strokes; soft outer glow on lit elements; faint horizontal scanline texture; monospace typeface throughout; flat, no photographic depth, no gradient fill.
QUALITY — crisp phosphor CRT terminal render, sharp monospace, precise alignment, subtle bloom.
```

**BLUEPRINT（可选）**
```
LOCKED — deep blueprint-blue background; white technical ink for every line, node, glyph and label; thin uniform strokes; drafting-table cyanotype feel; monospace / technical lettering throughout; flat, no photographic depth, no gradient fill.
QUALITY — authentic engineering blueprint print, sharp white linework, precise alignment, faint paper grain.
```

## 固定字段顺序

成品提示词永远按此顺序：

```
STYLE ANCHOR  →  FORMAT(锁死画幅)  →  LOCKED(按寄存器)  →  DOMINANT VISUAL(一张拓扑)
→  HUD FRAME  →  TYPOGRAPHY  →  TEXT(要渲染的文字, 声明一次)  →  AVOID  →  QUALITY(按寄存器)
```

## 成品骨架（填好即发，无占位符）

```text
STYLE ANCHOR — a technical schematic screen rendered as <register flavor>: an engineering topology diagram drawn in glowing monospace, like a system-monitor HUD.

A <5:2 landscape / 16:9> poster.

LOCKED — <粘贴对应寄存器的 LOCKED 段>

DOMINANT VISUAL — <one resolved topology, flat line-art>: <描述入口 / fan-out / 并行节点 / 汇合 / 出口 / 回环中实际用到的那些>; nodes are thin-stroked circles with tiny line-icons, edges are thin lines carrying small glowing dots.

HUD FRAME — top-left metadata block (short mono labels like PROJECT / TYPE / VERSION); top-right legend keying NODE / EDGE / FLOW; bottom system-log lines with timestamps reading short status tags; thin dimension rulers with tick marks along an edge; corner crop marks.

TYPOGRAPHY — monospace only; <封面: the main title set very large across the center, glowing / 插图: only tiny Latin field labels, no large title>.

TEXT — main title must render exactly: <主标题>. <封面可加一行小副标>. Secondary labels are short Latin field tags and log lines only; no random dates, URLs, fake brands, long paragraphs, QR codes, or real code.

AVOID — any color beyond the single register palette; the other register's colors; photographic texture; 3D bevels; glossy reflections; heavy display poster type; decorative icons outside the schematic; dense unreadable code walls.

QUALITY — <粘贴对应寄存器的 QUALITY 段>
```

## 封面标题图文分离铁律（防止字和图糊在一起）

封面的巨型标题和拓扑图同处一块画面、又同为一个绿相，最容易糊成一团。凡是带大标题的封面，必带下面四条，缺一即改：

1. **留净空 + 线绕行**：中央横向留一条净空带给标题；fan-out 的连线从标题的上方和下方两道弧线绕过去，**绝不从标题正后方穿过**（`edges never cross behind the title`，写进 LAYOUT，并进 AVOID）。
2. **明度分层**：单色不等于单一亮度。标题用近白亮绿 + 强辉光（`bright near-white green, heavy bloom`），拓扑线压暗成中绿（`dimmer mid-green`）。这是最有效的图文分离手段，且不破坏单色。
3. **字重分层**：标题粗重（`heavy bold weight`），示意线细（`thin uniform strokes`）。
4. **黑底板 knockout**：标题坐在一块低调黑底板上、带留白，物理切断任何经过其后的线（`subtle black knockout plate that interrupts any line behind it`）。同时 HUD 面板 / 日志 / 标尺整体压暗，不与标题争亮度。

插图（16:9）通常没有大标题、只有拉丁小标签，不受本节约束；一旦某张插图要放大标题，同样套这四条。

## 招牌装置一致性（批量成系列的关键）

同一篇文章的封面 + 所有插图，必须共享：

1. 同一个 REGISTER（要么全 TERMINAL，要么全 BLUEPRINT）；
2. 同一套 HUD FRAME 元素（角落面板 + 图例 + 标尺 + 日志，风格一致）；
3. 同一种节点画法（细圆圈 + 线图标 + 连线发光点）。

**只有中央拓扑图的结构和封面主标题变**，边框系统一字不变。出图后并排缩略图检查：一眼能认出是同一系列。

## 拓扑词汇表（把段落逻辑转成图）

| 段落逻辑 | 对应拓扑 |
|---|---|
| 一个 Agent 反复干（Loop） | 单节点 + 一条自循环回环箭头 |
| 组队分工（Graph 总览） | ENTRY → fan-out 到多个具名节点 → MERGE → EXIT 的完整菱形 |
| 有先后 vs 能并行（假依赖） | 上排一条 A→B→C→D 线性链（标注 chain），下排断开的假边 + 展开成并行分支 |
| Fan-out / Fan-in 菱形 | 一入口散射到 N 节点，再收束到一个汇合节点 |
| 验收 / 循环回退 | 菱形末端一个 verifier 节点，一条虚线回环箭头指回上游，带 stop 标记 |
| Router 分诊 / 判断清单 | 一个菱形判断节点分出两条边（light path / heavy path）或四个 checkbox 门 |
