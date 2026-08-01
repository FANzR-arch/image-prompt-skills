# 编译契约（消歧义铁律）

每次输出前必须满足。这是「成品」和「拼装件」的分界：成品不留任何选项、菜单、占位符。

## 5 条铁律

1. **每个槽位解析成唯一值**：删掉所有 `/` 选项和 `{}` 占位。成品里不允许出现 `green / cyan / amber` 这类菜单。
2. **正文零中文**：提示词正文只能出现英文美术指导；唯一例外是「要渲染进画面的标题文字」。任何中文注释一律不留——模型会把它画进海报。
3. **单一色相**：全图只有一种霓虹绿，绝不并列第二套配色。屏幕质感层也受这条管——CRT 做单色荧光屏，不许出现 RGB 子像素三联点、色散分离、彩虹边，那会把单色打破。
4. **否定只进 AVOID**：正文用正向描述，所有 `no / not / avoid` 收进末尾 AVOID 块。
5. **主标题精确，次级 micro-text 受控**：主标题必须精确渲染（如 `从 Loop 到 Graph`、`GRAPH`）。次级小字只能是短拉丁字段标签（NODE / EDGE / FAN-OUT / A1–A6 / MERGE / EXIT / [ok] / timestamps），tiny、锁网格、有功能感。禁随机日期、URL、假品牌名、长段落、二维码、真代码块。

## 锁死的风格内核（LOCKED，每条必带）

无论封面还是插图，这几条恒定：

- 主视觉是**一张节点-连线拓扑图**：节点为细描圆圈，连线为均匀细线，连线上有发光小圆点当数据流；
- 一层 **HUD 仪表框**：角落数据面板（PROJECT / TYPE / VERSION 类短标签）、图例（key NODE / EDGE / FLOW）、边缘标尺带刻度、底部系统日志行；
- **等宽字体**贯穿全图；
- **画的内容是平面线稿**，无照片景深、无写实材质、无渐变填充（发光辉光除外）；
- **所有线一样粗**——这是屏幕的语法，线型分级（粗轮廓 / 细尺寸线 / 点划中心线）属于图纸，不进这里；
- 画的内容之上盖一层 **SCREEN TEXTURE**，见下节，这层是必带的，不是可选装饰；
- 层级靠尺度和位置，不靠装饰花纹。

「平面线稿」管的是被画出来的图，「屏幕质感」管的是承载它的那块屏。两者不冲突，写提示词时也不要混在同一句里。

## 唯一寄存器预设（LOCKED 段照抄）

```
LOCKED — pure black background that lifts into a faint dark halo around anything lit; a single neon-green phosphor color for every line, node, glyph and label; thin uniform strokes; soft outer glow on lit elements; monospace typeface throughout; the drawn content is flat line-art with no photographic depth and no gradient fill.
QUALITY — crisp phosphor CRT terminal render shot straight off a real screen, sharp monospace holding up through the scanline texture, precise alignment, subtle bloom.
```

## 屏幕质感层（SCREEN TEXTURE）

这是这套风格「像不像真东西」的分水岭。没有这一层，出来的是干净的矢量流程图；有了这一层，出来的是一块正在发光的老显像管屏幕。

**一句话原则：质感盖在内容之上，永远不吃内容。** 扫描线压过标题和节点标签，但压不糊——缩略图状态下所有字仍然认得出来。

三档强度，一次选一档，整篇统一。用户没指定用 **CRT-02**。

**CRT-01 CLEAN（轻）** — 信息密度高的插图、或标题很长的封面
```
SCREEN TEXTURE — the whole frame is the glowing face of a monochrome CRT monitor. Fine horizontal scanlines run edge to edge at even spacing, dark and low in contrast, riding over every element including the title. Lit strokes bleed a little light into the scanlines beside them. A gentle vignette darkens the four corners. Every glyph stays sharp and fully legible through the texture.
```

**CRT-02 STANDARD（默认）** — 封面和大多数插图
```
SCREEN TEXTURE — the whole frame is a close photograph of a monochrome phosphor CRT monitor. Fine horizontal scanlines run edge to edge at even spacing, dark and low in contrast, riding over every element including the title, and their brightness varies subtly from band to band as if the tube is mid-refresh. Under them sits a much finer vertical aperture-grille striping, visible only inside lit areas as phosphor grain. Lit strokes bloom and halate into the scanlines around them, brightest where two lines cross. The picture bows outward in gentle barrel curvature, falls off into a soft vignette at the four corners, and defocuses very slightly at the extreme edges. A faint even haze of glass lies over the whole surface. Every glyph stays sharp and fully legible through the texture.
```

**CRT-03 DEGRADED（重）** — 只用在封面或单张大图，讲「旧 / 遗留 / 故障 / 归档」时
```
SCREEN TEXTURE — the whole frame is a close photograph of a tired old monochrome phosphor CRT monitor. Fine horizontal scanlines run edge to edge at even spacing, dark and low in contrast, riding over every element including the title, their brightness pulsing subtly band to band. Under them sits a much finer vertical aperture-grille striping, visible inside lit areas as phosphor grain. One wide, very faint horizontal refresh band drifts across the picture, lifting whatever it passes over. Bright strokes bloom, halate, and trail a short horizontal ghost smear to their right. A barely-visible burn-in ghost of an older diagram lingers underneath. The picture bows outward in barrel curvature, darkens into heavy corner vignette, defocuses at the extreme edges, and carries a fine dusting of analog static across dusty, aged glass. Every glyph stays sharp and fully legible through the decay — the wear stays under the content, never on top of it.
```

配套要求（选了任一档都要同步）：

- **AVOID 必须换掉旧的 `photographic texture`**——那句会把整层质感否掉。改成禁「画里出现照片实物 / 景深」，见下文骨架。
- **AVOID 必带三条新禁令**：RGB 色散分离与彩虹边（破单色）、扫描线粗到把字咬碎、画面里出现显示器边框外壳和桌面（屏幕面要铺满整幅）。
- **QUALITY 用上面那段新版**，里面已经写了「字要穿过扫描线仍然锐利」。

想要纸的质感（纸纹、折痕、水渍、图钉孔）不在这里改——那是 `engineering-blueprint-sheet` 的 PRINT TEXTURE，整套语法都不同，转过去用。

## 固定字段顺序

成品提示词永远按此顺序。质感层排在 TEXT 之后、AVOID 之前——它是盖在画完的成品上的一道后期，不是画的内容：

```
STYLE ANCHOR  →  FORMAT(锁死画幅)  →  LOCKED  →  [LAYOUT(带大标题的封面必带)]
→  DOMINANT VISUAL(一张拓扑)  →  HUD FRAME  →  TYPOGRAPHY  →  TEXT(要渲染的文字, 声明一次)
→  SCREEN TEXTURE(按强度档)  →  AVOID  →  QUALITY
```

## 成品骨架（填好即发，无占位符）

```text
STYLE ANCHOR — a technical schematic screen rendered as a phosphor CRT terminal: an engineering topology diagram drawn in glowing monospace, like a system-monitor HUD.

A <5:2 landscape / 16:9> poster.

LOCKED — <粘贴 LOCKED 段>

DOMINANT VISUAL — <one resolved topology, flat line-art>: <描述入口 / fan-out / 并行节点 / 汇合 / 出口 / 回环中实际用到的那些>; nodes are thin-stroked circles with tiny line-icons, edges are thin lines carrying small glowing dots.

HUD FRAME — top-left metadata block (short mono labels like PROJECT / TYPE / VERSION); top-right legend keying NODE / EDGE / FLOW; bottom system-log lines with timestamps reading short status tags; thin dimension rulers with tick marks along an edge; corner crop marks.

TYPOGRAPHY — monospace only; <封面: the main title set very large across the center, glowing / 插图: only tiny Latin field labels, no large title>.

TEXT — main title must render exactly: <主标题>. <封面可加一行小副标>. Secondary labels are short Latin field tags and log lines only; no random dates, URLs, fake brands, long paragraphs, QR codes, or real code.

SCREEN TEXTURE — <粘贴选中的 CRT 强度档>

AVOID — any hue beyond the single neon green; blueprint blue; RGB colour split, chromatic aberration or rainbow subpixel fringing; scanlines heavy or wide enough to break up the glyphs; a visible monitor bezel, plastic housing, desk or room around the screen; paper texture, fold creases or stains; varying line weights, dimension arrows or a ruled title block; photographic objects or depth of field inside the artwork itself; 3D bevels; hard specular glare sitting over the content; heavy display poster type; decorative icons outside the schematic; dense unreadable code walls.

QUALITY — <粘贴 QUALITY 段>
```

## 封面标题图文分离铁律（防止字和图糊在一起）

封面的巨型标题和拓扑图同处一块画面、又同为一个绿相，最容易糊成一团。凡是带大标题的封面，必带下面四条，缺一即改：

1. **留净空 + 线绕行**：中央横向留一条净空带给标题；fan-out 的连线从标题的上方和下方两道弧线绕过去，**绝不从标题正后方穿过**（`edges never cross behind the title`，写进 LAYOUT，并进 AVOID）。
2. **明度分层**：单色不等于单一亮度。标题用近白亮绿 + 强辉光（`bright near-white green, heavy bloom`），拓扑线压暗成中绿（`dimmer mid-green`）。这是最有效的图文分离手段，且不破坏单色。
3. **字重分层**：标题粗重（`heavy bold weight`），示意线细（`thin uniform strokes`）。
4. **黑底板 knockout**：标题坐在一块低调黑底板上、带留白，物理切断任何经过其后的线（`subtle black knockout plate that interrupts any line behind it`）。同时 HUD 面板 / 日志 / 标尺整体压暗，不与标题争亮度。

插图（16:9）通常没有大标题、只有拉丁小标签，不受本节约束；一旦某张插图要放大标题，同样套这四条。

**加了屏幕质感层之后还有一条**：辉光和扫描线是两个方向相反的力——bloom 让标题往外糊，scanline 让标题被横向切碎，两个叠在一起最先牺牲的就是最大的那几个字。所以 SCREEN TEXTURE 段末尾那句 `every glyph stays sharp and fully legible through the texture` 是硬性的，不许删；标题笔画本来就细的字（细体、纤细中文）在这套风格里直接不用。

## 招牌装置一致性（批量成系列的关键）

同一篇文章的封面 + 所有插图，必须共享：

1. 同一套 HUD FRAME 元素（角落面板 + 图例 + 标尺 + 日志，风格一致）；
2. 同一种节点画法（细圆圈 + 线图标 + 连线发光点）；
3. **同一档 SCREEN TEXTURE**：整篇同一强度，一字不改地复制粘贴。封面 CRT-03、插图 CRT-01 会当场散架——一张像旧屏幕，一张像新屏幕，缩略图并排一眼假。真有某张插图信息太密扛不住质感，做法是**整篇一起降档**，不是单张降。

**只有中央拓扑图的结构和封面主标题变**，边框系统和质感层一字不变。出图后并排缩略图检查：一眼能认出是同一系列。

## 拓扑词汇表（把段落逻辑转成图）

| 段落逻辑 | 对应拓扑 |
|---|---|
| 一个 Agent 反复干（Loop） | 单节点 + 一条自循环回环箭头 |
| 组队分工（Graph 总览） | ENTRY → fan-out 到多个具名节点 → MERGE → EXIT 的完整菱形 |
| 有先后 vs 能并行（假依赖） | 上排一条 A→B→C→D 线性链（标注 chain），下排断开的假边 + 展开成并行分支 |
| Fan-out / Fan-in 菱形 | 一入口散射到 N 节点，再收束到一个汇合节点 |
| 验收 / 循环回退 | 菱形末端一个 verifier 节点，一条虚线回环箭头指回上游，带 stop 标记 |
| Router 分诊 / 判断清单 | 一个菱形判断节点分出两条边（light path / heavy path）或四个 checkbox 门 |

## 和 engineering-blueprint-sheet 的边界

两个 skill 长得像，但载体不同，元素不能串：

| | tech-schematic-poster（屏） | engineering-blueprint-sheet（纸） |
|---|---|---|
| 线 | 全部等粗细 | 分级：粗轮廓 / 细尺寸 / 点划中心 / 虚线隐藏 |
| 光 | 辉光、bloom、halation | 无。印上去的墨 |
| 质感 | 扫描线、荧光颗粒、屏幕弧度、烧屏 | 纸纹、折痕、水渍、图钉孔 |
| 框 | HUD 面板 + 图例 + 系统日志 | 图框分区 + 标题栏 + 修订表 |
| 字 | 等宽字 | 制图技术字 |

用户要「终端 / HUD / 赛博 / 扫描线」走这个；要「蓝图 / 图纸 / 三视图 / 爆炸图 / 标题栏」转过去。两个都想要就出两张，不要合成一张。
