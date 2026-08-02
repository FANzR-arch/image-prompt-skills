# 成品示例：一整篇文章的封面 + 插图系列

样例文章：《Loop 刚讲完，Graph Engineering 又来了？0 基础一篇讲透，附多 Agent 分工提示词》
质感档：CRT-02 STANDARD。封面 5:2，插图 16:9。全部共享同一 HUD 招牌装置和同一段 SCREEN TEXTURE。

注意下面每条里的 `SCREEN TEXTURE` 段是**一字不差重复**的——这是整篇成系列的一半功劳，改档要六条一起改。

---

## 封面（5:2）

> 带大标题的封面必带「标题图文分离铁律」四条（净空+绕行 / 明度分层 / 字重分层 / 净空带 knockout），加上质感层那条「辉光和扫描线一起吃字」的补充，见 compile-contract.md。下面是应用后的成品。

```text
STYLE ANCHOR — a technical schematic screen rendered as a phosphor CRT terminal: an engineering topology diagram drawn in glowing monospace, like a system-monitor HUD.

A 5:2 landscape poster.

LOCKED — pure black background that lifts into a faint dark halo around anything lit; one neon-green phosphor hue for everything, but with a strong brightness hierarchy — the title is bright near-white green with a heavy bloom, the schematic lines are a dimmer mid-green; all schematic linework shares one uniform thin stroke weight while the title is set in heavy bold type; soft outer glow on lit elements; monospace typeface for all Latin text; the drawn content is flat line-art with no photographic depth and no gradient fill.

LAYOUT — a wide horizontal clear band is reserved across the center for the title; the topology is routed so its edges sweep in two arcs, one above and one below this central band, and never cross behind the title.

DOMINANT VISUAL — one wide node-and-edge topology: a single ENTRY node on the far left fans out to six labeled circular agent nodes, their edges arc over and under the central title band and converge into a MERGE column on the right, then to one EXIT node on the far right; small glowing dots ride the edges; each agent node holds a tiny line-icon (magnifier, bar-chart, code brackets, checkmark, clipboard, document); nodes are thin-stroked circles.

TITLE TREATMENT — the main title sits centered in a clear horizontal band with generous padding that no linework crosses; rendered very large and dominating the composition, bright near-white-green, heavy weight, strong green bloom — clearly the brightest, boldest element on screen.

HUD FRAME — top-left metadata block (PROJECT / TYPE: FAN-OUT·FAN-IN / VERSION); top-right legend keying NODE / EDGE / FLOW / EXIT; a bottom row of short system-status fields (SYS READY / LINK ACTIVE / [ok]); thin dimension ruler with tick marks along the bottom edge; corner crop marks — all kept dim so they never compete with the title.

TYPOGRAPHY — monospace for all Latin text; the Chinese title is set in a heavy Chinese sans (思源黑体 / Source Han Sans, Heavy).

TEXT — main title must render verbatim, with no extra words or characters added: "从 Loop 到 Graph". One small subtitle line beneath it, also verbatim: "多 Agent 分工提示词 · 附模板". Secondary labels are short Latin field tags only (ENTRY, A1–A6, MERGE, EXIT, FAN-OUT); no dates, URLs, fake brands, long paragraphs, QR codes, or real code.

SCREEN TEXTURE — the whole frame is a close photograph of a monochrome phosphor CRT monitor. Fine horizontal scanlines run edge to edge at even spacing, dark and low in contrast, riding over every element including the title, and their brightness varies subtly from band to band as if the tube is mid-refresh. Under them sits a much finer vertical aperture-grille striping, visible only inside lit areas as phosphor grain. Lit strokes bloom and halate into the scanlines around them, brightest where two lines cross. The picture bows outward in gentle barrel curvature, falls off into a soft vignette at the four corners, and defocuses very slightly at the extreme edges. A faint even haze of glass lies over the whole surface. Every glyph stays sharp and fully legible through the texture.

AVOID — any hue beyond neon green; blueprint blue; RGB colour split, chromatic aberration or rainbow subpixel fringing; scanlines heavy or wide enough to break up the title glyphs; a visible monitor bezel, plastic housing, desk or room around the screen; edges crossing behind the title; title at the same brightness as the diagram lines; photographic objects or depth of field inside the artwork itself; 3D bevels; hard specular glare sitting over the content; dense unreadable code walls.

QUALITY — crisp phosphor CRT terminal render shot straight off a real screen, sharp monospace holding up through the scanline texture, precise alignment, strong bloom on the title, dim schematic behind it.
```

---

## 插图 1（16:9）— Loop vs Graph

```text
STYLE ANCHOR — a technical schematic screen rendered as a phosphor CRT terminal: an engineering topology diagram drawn in glowing monospace, like a system-monitor HUD.

A 16:9 poster.

LOCKED — pure black background that lifts into a faint dark halo around anything lit; a single neon-green phosphor color for every line, node, glyph and label; all schematic linework shares one uniform thin stroke weight; soft outer glow on lit elements; monospace typeface for all Latin text; the drawn content is flat line-art with no photographic depth and no gradient fill.

DOMINANT VISUAL — a split diagram divided by one thin vertical rule: on the left, a single circular node with a looping arrow curving back into itself, tiny label LOOP; on the right, a small cluster of six circular nodes connected by edges into a diamond, tiny label GRAPH; nodes are thin-stroked circles, edges carry small glowing dots.

HUD FRAME — top-left small metadata tag; top-right tiny legend NODE / EDGE; thin dimension ruler with ticks along the bottom edge; corner crop marks; minimal.

TYPOGRAPHY — monospace for all Latin text; only tiny Latin field labels LOOP and GRAPH, no large title.

TEXT — only the two field labels LOOP and GRAPH plus corner tags; no other text, no dates, no code.

SCREEN TEXTURE — the whole frame is a close photograph of a monochrome phosphor CRT monitor. Fine horizontal scanlines run edge to edge at even spacing, dark and low in contrast, riding over every element, and their brightness varies subtly from band to band as if the tube is mid-refresh. Under them sits a much finer vertical aperture-grille striping, visible only inside lit areas as phosphor grain. Lit strokes bloom and halate into the scanlines around them, brightest where two lines cross. The picture bows outward in gentle barrel curvature, falls off into a soft vignette at the four corners, and defocuses very slightly at the extreme edges. A faint even haze of glass lies over the whole surface. Every glyph stays sharp and fully legible through the texture.

AVOID — any color beyond the single neon green; blueprint blue; RGB colour split, chromatic aberration or rainbow subpixel fringing; scanlines heavy or wide enough to break up the glyphs; a visible monitor bezel, plastic housing, desk or room around the screen; photographic objects or depth of field inside the artwork itself; 3D bevels; hard specular glare sitting over the content; large title type; dense code walls.

QUALITY — crisp phosphor CRT terminal render shot straight off a real screen, sharp monospace holding up through the scanline texture, precise alignment, subtle bloom.
```

---

## 插图 2（16:9）— 五名词图例板

```text
STYLE ANCHOR — a technical schematic screen rendered as a phosphor CRT terminal: an engineering topology diagram drawn in glowing monospace, like a system-monitor HUD.

A 16:9 poster.

LOCKED — pure black background that lifts into a faint dark halo around anything lit; a single neon-green phosphor color for every line, node, glyph and label; all schematic linework shares one uniform thin stroke weight; soft outer glow on lit elements; monospace typeface for all Latin text; the drawn content is flat line-art with no photographic depth and no gradient fill.

DOMINANT VISUAL — a legend board of five stacked rows, each row a tiny schematic symbol on the left keyed to a short Latin term on the right: a circle labeled NODE, a connecting arrow labeled EDGE, a form/ticket glyph labeled SCHEMA, a shield-check glyph labeled VERIFIER, a branching fork labeled ROUTER; the five symbols share one vertical guide line; thin-stroked line-art.

HUD FRAME — top-left metadata tag reading LEGEND; thin dimension ruler with ticks along the right edge; corner crop marks.

TYPOGRAPHY — monospace for all Latin text; five short Latin terms NODE / EDGE / SCHEMA / VERIFIER / ROUTER as row labels, no large title.

TEXT — only the five Latin terms and the LEGEND tag; no other text, no dates, no code.

SCREEN TEXTURE — the whole frame is a close photograph of a monochrome phosphor CRT monitor. Fine horizontal scanlines run edge to edge at even spacing, dark and low in contrast, riding over every element, and their brightness varies subtly from band to band as if the tube is mid-refresh. Under them sits a much finer vertical aperture-grille striping, visible only inside lit areas as phosphor grain. Lit strokes bloom and halate into the scanlines around them, brightest where two lines cross. The picture bows outward in gentle barrel curvature, falls off into a soft vignette at the four corners, and defocuses very slightly at the extreme edges. A faint even haze of glass lies over the whole surface. Every glyph stays sharp and fully legible through the texture.

AVOID — any color beyond the single neon green; blueprint blue; RGB colour split, chromatic aberration or rainbow subpixel fringing; scanlines heavy or wide enough to break up the glyphs; a visible monitor bezel, plastic housing, desk or room around the screen; photographic objects or depth of field inside the artwork itself; 3D bevels; hard specular glare sitting over the content; large title type; Chinese characters; dense code walls.

QUALITY — crisp phosphor CRT terminal render shot straight off a real screen, sharp monospace holding up through the scanline texture, precise alignment, subtle bloom.
```

---

## 插图 3（16:9）— 假依赖：链条断开成并行

```text
STYLE ANCHOR — a technical schematic screen rendered as a phosphor CRT terminal: an engineering topology diagram drawn in glowing monospace, like a system-monitor HUD.

A 16:9 poster.

LOCKED — pure black background that lifts into a faint dark halo around anything lit; a single neon-green phosphor color for every line, node, glyph and label; all schematic linework shares one uniform thin stroke weight; soft outer glow on lit elements; monospace typeface for all Latin text; the drawn content is flat line-art with no photographic depth and no gradient fill.

DOMINANT VISUAL — two rows compared: the top row is a single straight linear chain of four circular nodes A - B - C - D joined by arrows, tiny label QUEUE; two of the arrows are drawn as broken dashed edges with a small scissor/cut mark; the bottom row shows the same nodes reorganized, one entry node fanning out to three parallel branches running side by side, tiny label PARALLEL; thin-stroked line-art, edges carry small glowing dots.

HUD FRAME — top-left metadata tag; left-edge dimension ruler with ticks; corner crop marks.

TYPOGRAPHY — monospace for all Latin text; tiny Latin labels QUEUE, PARALLEL, and node letters A B C D, no large title.

TEXT — only the field labels QUEUE, PARALLEL, and letters A B C D; no other text, no dates, no code.

SCREEN TEXTURE — the whole frame is a close photograph of a monochrome phosphor CRT monitor. Fine horizontal scanlines run edge to edge at even spacing, dark and low in contrast, riding over every element, and their brightness varies subtly from band to band as if the tube is mid-refresh. Under them sits a much finer vertical aperture-grille striping, visible only inside lit areas as phosphor grain. Lit strokes bloom and halate into the scanlines around them, brightest where two lines cross. The picture bows outward in gentle barrel curvature, falls off into a soft vignette at the four corners, and defocuses very slightly at the extreme edges. A faint even haze of glass lies over the whole surface. Every glyph stays sharp and fully legible through the texture.

AVOID — any color beyond the single neon green; blueprint blue; RGB colour split, chromatic aberration or rainbow subpixel fringing; scanlines heavy or wide enough to break up the glyphs; a visible monitor bezel, plastic housing, desk or room around the screen; photographic objects or depth of field inside the artwork itself; 3D bevels; hard specular glare sitting over the content; large title type; dense code walls.

QUALITY — crisp phosphor CRT terminal render shot straight off a real screen, sharp monospace holding up through the scanline texture, precise alignment, subtle bloom.
```

---

## 插图 4（16:9）— 菱形拓扑：分 → 并行 → 质检 → 出

```text
STYLE ANCHOR — a technical schematic screen rendered as a phosphor CRT terminal: an engineering topology diagram drawn in glowing monospace, like a system-monitor HUD.

A 16:9 poster.

LOCKED — pure black background that lifts into a faint dark halo around anything lit; a single neon-green phosphor color for every line, node, glyph and label; all schematic linework shares one uniform thin stroke weight; soft outer glow on lit elements; monospace typeface for all Latin text; the drawn content is flat line-art with no photographic depth and no gradient fill.

DOMINANT VISUAL — one clean horizontal diamond topology centered: a SPLIT node on the left fans out to three parallel worker nodes, they converge into a REDUCE node, which passes to a VERIFY node marked with a checkmark, ending at a SYNTH node on the right; a thin dashed feedback arrow loops from VERIFY back to the worker column with a small STOP tag; nodes are thin-stroked circles, edges carry small glowing dots.

HUD FRAME — top-left metadata block PROJECT / TYPE: DIAMOND; top-right legend NODE / EDGE / FLOW; bottom dimension ruler with ticks; corner crop marks.

TYPOGRAPHY — monospace for all Latin text; tiny Latin node labels SPLIT / REDUCE / VERIFY / SYNTH, no large title.

TEXT — only the field labels SPLIT, REDUCE, VERIFY, SYNTH, STOP; no other text, no dates, no code.

SCREEN TEXTURE — the whole frame is a close photograph of a monochrome phosphor CRT monitor. Fine horizontal scanlines run edge to edge at even spacing, dark and low in contrast, riding over every element, and their brightness varies subtly from band to band as if the tube is mid-refresh. Under them sits a much finer vertical aperture-grille striping, visible only inside lit areas as phosphor grain. Lit strokes bloom and halate into the scanlines around them, brightest where two lines cross. The picture bows outward in gentle barrel curvature, falls off into a soft vignette at the four corners, and defocuses very slightly at the extreme edges. A faint even haze of glass lies over the whole surface. Every glyph stays sharp and fully legible through the texture.

AVOID — any color beyond the single neon green; blueprint blue; RGB colour split, chromatic aberration or rainbow subpixel fringing; scanlines heavy or wide enough to break up the glyphs; a visible monitor bezel, plastic housing, desk or room around the screen; photographic objects or depth of field inside the artwork itself; 3D bevels; hard specular glare sitting over the content; large title type; dense code walls.

QUALITY — crisp phosphor CRT terminal render shot straight off a real screen, sharp monospace holding up through the scanline texture, precise alignment, subtle bloom.
```

---

## 插图 5（16:9）— 四问判断门 + 渐进四步

```text
STYLE ANCHOR — a technical schematic screen rendered as a phosphor CRT terminal: an engineering topology diagram drawn in glowing monospace, like a system-monitor HUD.

A 16:9 poster.

LOCKED — pure black background that lifts into a faint dark halo around anything lit; a single neon-green phosphor color for every line, node, glyph and label; all schematic linework shares one uniform thin stroke weight; soft outer glow on lit elements; monospace typeface for all Latin text; the drawn content is flat line-art with no photographic depth and no gradient fill.

DOMINANT VISUAL — a decision flow reading left to right: an entry node passes through a stacked gate of four checkbox rows labeled Q1 Q2 Q3 Q4, then a diamond decision node splits into two edges — a short SKIP edge looping to a single-node end, and a GRAPH edge leading into a four-step progressive path of four nodes in a line numbered 1 2 3 4; thin-stroked line-art, edges carry small glowing dots.

HUD FRAME — top-left metadata tag ROUTER; right-edge dimension ruler with ticks; corner crop marks.

TYPOGRAPHY — monospace for all Latin text; tiny Latin labels Q1–Q4, SKIP, GRAPH, and step numbers 1 2 3 4, no large title.

TEXT — only the field labels Q1 Q2 Q3 Q4, SKIP, GRAPH, and numbers 1 2 3 4; no other text, no dates, no code.

SCREEN TEXTURE — the whole frame is a close photograph of a monochrome phosphor CRT monitor. Fine horizontal scanlines run edge to edge at even spacing, dark and low in contrast, riding over every element, and their brightness varies subtly from band to band as if the tube is mid-refresh. Under them sits a much finer vertical aperture-grille striping, visible only inside lit areas as phosphor grain. Lit strokes bloom and halate into the scanlines around them, brightest where two lines cross. The picture bows outward in gentle barrel curvature, falls off into a soft vignette at the four corners, and defocuses very slightly at the extreme edges. A faint even haze of glass lies over the whole surface. Every glyph stays sharp and fully legible through the texture.

AVOID — any color beyond the single neon green; blueprint blue; RGB colour split, chromatic aberration or rainbow subpixel fringing; scanlines heavy or wide enough to break up the glyphs; a visible monitor bezel, plastic housing, desk or room around the screen; photographic objects or depth of field inside the artwork itself; 3D bevels; hard specular glare sitting over the content; large title type; dense code walls.

QUALITY — crisp phosphor CRT terminal render shot straight off a real screen, sharp monospace holding up through the scanline texture, precise alignment, subtle bloom.
```

---

## 换质感强度怎么改

只动 `SCREEN TEXTURE` 一段，其余不动，六条一起换：

- 想更干净（插图字太多、标题太长）→ 整段换成 `compile-contract.md` 的 **CRT-01 CLEAN**。
- 想更旧、更有故障感和年代感 → 整段换成 **CRT-03 DEGRADED**，并在 AVOID 末尾补一句 `noise or ghosting strong enough to obscure any label`。

不要只给封面上重档、插图上轻档——同一篇里质感档不一致，缩略图并排一眼就散。

## 想要蓝图版？

蓝底白线的工程图纸不在这里改配色——它已经拆成独立 skill `engineering-blueprint-sheet`，那边有自己的线型分级、尺寸标注、标题栏、修订表和三档纸张质感，不是把绿换成蓝就能得到的。直接用那个 skill。
