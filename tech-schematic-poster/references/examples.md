# 成品示例：一整篇文章的封面 + 插图系列

样例文章：《Loop 刚讲完，Graph Engineering 又来了？0 基础一篇讲透，附多 Agent 分工提示词》
寄存器：TERMINAL（黑底霓虹绿）。封面 5:2，插图 16:9。全部共享同一 HUD 招牌装置。

---

## 封面（5:2）

> 带大标题的封面必带「标题图文分离铁律」四条（净空+绕行 / 明度分层 / 字重分层 / 黑底板），见 compile-contract.md。下面是应用后的成品。

```text
STYLE ANCHOR — a technical schematic screen rendered as a phosphor CRT terminal: an engineering topology diagram drawn in glowing monospace, like a system-monitor HUD.

A 5:2 landscape poster.

LOCKED — pure black background; one neon-green phosphor hue for everything, but with a strong brightness hierarchy — the title is bright near-white green with a heavy bloom, the schematic lines are a dimmer mid-green; the diagram uses thin uniform strokes while the title uses heavy bold weight; soft outer glow on lit elements; faint horizontal scanline texture; monospace typeface throughout; flat, no photographic depth, no gradient fill.

LAYOUT — a wide horizontal clear band is reserved across the center for the title; the topology is routed so its edges sweep in two arcs, one above and one below this central band, and never cross behind the title.

DOMINANT VISUAL — one wide node-and-edge topology: a single ENTRY node on the far left fans out to six labeled circular agent nodes, their edges arc over and under the central title band and converge into a MERGE column on the right, then to one EXIT node on the far right; small glowing dots ride the edges; each agent node holds a tiny line-icon (magnifier, bar-chart, code brackets, checkmark, clipboard, document); nodes are thin-stroked circles.

TITLE TREATMENT — the main title sits centered on its own subtle black knockout plate with generous padding that interrupts any line behind it; rendered very large and dominating the composition, bright near-white-green, heavy weight, strong green bloom — clearly the brightest, boldest element on screen.

HUD FRAME — top-left metadata block (PROJECT / TYPE: FAN-OUT·FAN-IN / VERSION); top-right legend keying NODE / EDGE / FLOW / EXIT; bottom system-log lines with timestamps and [ok] tags; thin dimension ruler with tick marks along the bottom edge; corner crop marks — all kept dim so they never compete with the title.

TYPOGRAPHY — monospace only.

TEXT — main title must render exactly: 从 Loop 到 Graph. One small subtitle line beneath it: 多 Agent 分工提示词 · 附模板. Secondary labels are short Latin field tags (ENTRY, A1–A6, MERGE, EXIT, FAN-OUT) and log lines only; no random dates, URLs, fake brands, long paragraphs, QR codes, or real code.

AVOID — any hue beyond neon green; blueprint blue; edges crossing behind the title; title at the same brightness as the diagram lines; photographic texture; 3D bevels; glossy reflections; dense unreadable code walls.

QUALITY — crisp phosphor CRT terminal render, sharp monospace, precise alignment, strong bloom on the title, dim schematic behind it.
```

---

## 插图 1（16:9）— Loop vs Graph

```text
STYLE ANCHOR — a technical schematic screen rendered as a phosphor CRT terminal: an engineering topology diagram drawn in glowing monospace, like a system-monitor HUD.

A 16:9 poster.

LOCKED — pure black background; a single neon-green phosphor color for every line, node, glyph and label; thin uniform strokes; soft outer glow on lit elements; faint horizontal scanline texture; monospace typeface throughout; flat, no photographic depth, no gradient fill.

DOMINANT VISUAL — a split diagram divided by one thin vertical rule: on the left, a single circular node with a looping arrow curving back into itself, tiny label LOOP; on the right, a small cluster of six circular nodes connected by edges into a diamond, tiny label GRAPH; nodes are thin-stroked circles, edges carry small glowing dots.

HUD FRAME — top-left small metadata tag; top-right tiny legend NODE / EDGE; thin dimension ruler with ticks along the bottom edge; corner crop marks; minimal.

TYPOGRAPHY — monospace only; only tiny Latin field labels LOOP and GRAPH, no large title.

TEXT — only the two field labels LOOP and GRAPH plus corner tags; no other text, no dates, no code.

AVOID — any color beyond the single neon green; blueprint blue; photographic texture; 3D bevels; large title type; dense code walls.

QUALITY — crisp phosphor CRT terminal render, sharp monospace, precise alignment, subtle bloom.
```

---

## 插图 2（16:9）— 五名词图例板

```text
STYLE ANCHOR — a technical schematic screen rendered as a phosphor CRT terminal: an engineering topology diagram drawn in glowing monospace, like a system-monitor HUD.

A 16:9 poster.

LOCKED — pure black background; a single neon-green phosphor color for every line, node, glyph and label; thin uniform strokes; soft outer glow on lit elements; faint horizontal scanline texture; monospace typeface throughout; flat, no photographic depth, no gradient fill.

DOMINANT VISUAL — a legend board of five stacked rows, each row a tiny schematic symbol on the left keyed to a short Latin term on the right: a circle labeled NODE, a connecting arrow labeled EDGE, a form/ticket glyph labeled SCHEMA, a shield-check glyph labeled VERIFIER, a branching fork labeled ROUTER; the five symbols share one vertical guide line; thin-stroked line-art.

HUD FRAME — top-left metadata tag reading LEGEND; thin dimension ruler with ticks along the right edge; corner crop marks.

TYPOGRAPHY — monospace only; five short Latin terms NODE / EDGE / SCHEMA / VERIFIER / ROUTER as row labels, no large title.

TEXT — only the five Latin terms and the LEGEND tag; no other text, no dates, no code.

AVOID — any color beyond the single neon green; blueprint blue; photographic texture; 3D bevels; large title type; Chinese characters; dense code walls.

QUALITY — crisp phosphor CRT terminal render, sharp monospace, precise alignment, subtle bloom.
```

---

## 插图 3（16:9）— 假依赖：链条断开成并行

```text
STYLE ANCHOR — a technical schematic screen rendered as a phosphor CRT terminal: an engineering topology diagram drawn in glowing monospace, like a system-monitor HUD.

A 16:9 poster.

LOCKED — pure black background; a single neon-green phosphor color for every line, node, glyph and label; thin uniform strokes; soft outer glow on lit elements; faint horizontal scanline texture; monospace typeface throughout; flat, no photographic depth, no gradient fill.

DOMINANT VISUAL — two rows compared: the top row is a single straight linear chain of four circular nodes A - B - C - D joined by arrows, tiny label QUEUE; two of the arrows are drawn as broken dashed edges with a small scissor/cut mark; the bottom row shows the same nodes reorganized, one entry node fanning out to three parallel branches running side by side, tiny label PARALLEL; thin-stroked line-art, edges carry small glowing dots.

HUD FRAME — top-left metadata tag; left-edge dimension ruler with ticks; corner crop marks.

TYPOGRAPHY — monospace only; tiny Latin labels QUEUE, PARALLEL, and node letters A B C D, no large title.

TEXT — only the field labels QUEUE, PARALLEL, and letters A B C D; no other text, no dates, no code.

AVOID — any color beyond the single neon green; blueprint blue; photographic texture; 3D bevels; large title type; dense code walls.

QUALITY — crisp phosphor CRT terminal render, sharp monospace, precise alignment, subtle bloom.
```

---

## 插图 4（16:9）— 菱形拓扑：分 → 并行 → 质检 → 出

```text
STYLE ANCHOR — a technical schematic screen rendered as a phosphor CRT terminal: an engineering topology diagram drawn in glowing monospace, like a system-monitor HUD.

A 16:9 poster.

LOCKED — pure black background; a single neon-green phosphor color for every line, node, glyph and label; thin uniform strokes; soft outer glow on lit elements; faint horizontal scanline texture; monospace typeface throughout; flat, no photographic depth, no gradient fill.

DOMINANT VISUAL — one clean horizontal diamond topology centered: a SPLIT node on the left fans out to three parallel worker nodes, they converge into a REDUCE node, which passes to a VERIFY node marked with a checkmark, ending at a SYNTH node on the right; a thin dashed feedback arrow loops from VERIFY back to the worker column with a small STOP tag; nodes are thin-stroked circles, edges carry small glowing dots.

HUD FRAME — top-left metadata block PROJECT / TYPE: DIAMOND; top-right legend NODE / EDGE / FLOW; bottom dimension ruler with ticks; corner crop marks.

TYPOGRAPHY — monospace only; tiny Latin node labels SPLIT / REDUCE / VERIFY / SYNTH, no large title.

TEXT — only the field labels SPLIT, REDUCE, VERIFY, SYNTH, STOP; no other text, no dates, no code.

AVOID — any color beyond the single neon green; blueprint blue; photographic texture; 3D bevels; large title type; dense code walls.

QUALITY — crisp phosphor CRT terminal render, sharp monospace, precise alignment, subtle bloom.
```

---

## 插图 5（16:9）— 四问判断门 + 渐进四步

```text
STYLE ANCHOR — a technical schematic screen rendered as a phosphor CRT terminal: an engineering topology diagram drawn in glowing monospace, like a system-monitor HUD.

A 16:9 poster.

LOCKED — pure black background; a single neon-green phosphor color for every line, node, glyph and label; thin uniform strokes; soft outer glow on lit elements; faint horizontal scanline texture; monospace typeface throughout; flat, no photographic depth, no gradient fill.

DOMINANT VISUAL — a decision flow reading left to right: an entry node passes through a stacked gate of four checkbox rows labeled Q1 Q2 Q3 Q4, then a diamond decision node splits into two edges — a short SKIP edge looping to a single-node end, and a GRAPH edge leading into a four-step progressive path of four nodes in a line numbered 1 2 3 4; thin-stroked line-art, edges carry small glowing dots.

HUD FRAME — top-left metadata tag ROUTER; right-edge dimension ruler with ticks; corner crop marks.

TYPOGRAPHY — monospace only; tiny Latin labels Q1–Q4, SKIP, GRAPH, and step numbers 1 2 3 4, no large title.

TEXT — only the field labels Q1 Q2 Q3 Q4, SKIP, GRAPH, and numbers 1 2 3 4; no other text, no dates, no code.

AVOID — any color beyond the single neon green; blueprint blue; photographic texture; 3D bevels; large title type; dense code walls.

QUALITY — crisp phosphor CRT terminal render, sharp monospace, precise alignment, subtle bloom.
```

---

## 换 BLUEPRINT 寄存器怎么改

把每条里的 LOCKED 段和 QUALITY 段整段替换成 `compile-contract.md` 的 BLUEPRINT 预设，并把 AVOID 里的 `blueprint blue` 改成 `neon green / terminal phosphor`。其余拓扑、HUD、TEXT 不动——这样蓝图版和终端版是同结构的两套皮肤。
