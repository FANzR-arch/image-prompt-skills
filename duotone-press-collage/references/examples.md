# 成品实例

两套成组产出。第一套的封面已实测出图（`assets/preview.png`），章节图未逐张验证。

---

## 首图实测记录

**2026-08-01 · 5:2 封面「一眼就假」· 寄存器 R2 暗酒红**

验证成立：

- 平涂底全程干净无网点 —— 第一失败点未发生
- 双色套印偏移清晰，全尺寸可见黑版与芥末黄版错位
- 白色刀切描边只跟剪贴物，未爬到平涂色块
- 放大镜下的粗网点与全图网点形成两档密度差，机械感成立
- 四角裁切线、套版十字线、底部六格色条全部到位
- 中文四层文字（kicker / 主标 / 副标 / 底部长句）逐字渲染正确

暴露一点，已回写规则：

> **局部密度差要显式写成"比全图粗几倍"。**只写 `magnified` 会得到一个普通放大效果，看不出机械感。有效写法：`inside the lens circle the halftone dots are blown up several times coarser than everywhere else, crude and obviously mechanical`。

---

## 第一套 · 《一眼就假 —— AI 写的东西差在哪》

抽取表：

| 图 | 寄存器 | 主物件 | 连接物 | 标签 |
|---|---|---|---|---|
| 封面 5:2 | R2 暗酒红 | 检品灯箱 + 放大镜 | 层压（纸角压标题） | — |
| 章节 1 | R6 暖石灰 | 秒表 | 绷紧的线 | 三秒露馅 |
| 章节 2 | R3 深墨绿 | 天平 | 物理反常 | 水词堆 |
| 章节 3 | R7 骨白 | 方格校对纸 + 钢尺 | 磨损对比（唯一手写行） | 太整齐 |
| 章节 4 | R5 焦赭 | 票据穿刺针 | 悬空未落 | 没代价 |
| 章节 5 | R4 钴蓝 | 校对样张 | 引线 + 编号圈 | 只动三处 |

### 封面（5:2）· 已实测

```text
Use case: Wide article cover banner.

Scene: A flat oxblood background arranged like an inspection bench — torn pulp-paper strips, crop marks at the four corners, a six-swatch colour control bar along the bottom edge, one strip of masking tape holding a scrap down.

Subject: A cast-metal light table at the left, its glass surface glowing pale mustard from beneath, rendered as a coarse duotone halftone cut-out. A printed proof sheet lies on the glass and its torn right corner lifts off the table and overlaps the headline block, casting a hard paper shadow on it. A brass magnifier is clamped over one small area of the sheet; inside the lens circle the halftone dots are blown up several times coarser than everywhere else, crude and obviously mechanical. A mustard registration crosshair sits above the magnifier.

Key details: Mid-century print-shop collage. Every physical object is a photograph reproduced as a coarse visible duotone halftone — a black dot screen plus a second spot-colour dot screen offset by one or two pixels, so the misregistration is legible at full size. Each object is then die-cut with a crisp 3px white sticker outline and a faint hard drop shadow. Edges stay razor sharp and are never eroded by the texture; keep the magnifier's rim, the table's metal corners and the torn paper edge sharp. The halftone dots appear only on the cut-out objects and paper scraps — the flat colour field behind them carries no dots. Paper-fibre grain covers the whole image. Colour architecture: oxblood as the ground and pulp off-white as the neutral paper layer, mustard yellow as the single spot colour reserved for the light-table glow, the registration marks and the second halftone plate, black for all geometric marks and text blocks, no colour on the magnifier's brass beyond a warm grey.

Composition: 5:2 ultra-wide horizontal. The light table occupies the left 46% of the width, tilted about 7 degrees. The headline block occupies the right side from 48% to 96% width, vertically centred, with the lifted proof corner crossing into it.

Text in image: On a pulp off-white torn block, very large heavy Chinese sans (思源黑体 / Source Han Sans, Heavy) in black: "一眼就假". Directly beneath, on a narrower kraft strip, medium-weight black Chinese sans (思源黑体 / Source Han Sans): "AI 写的东西差在哪". Above the headline, small white Chinese inside a thin mustard bar: "去 AI 味". Along the lower right, small white Chinese on a black bar: "差的从来不是文笔，是这五处". Render all text verbatim, no extra words.

Constraints: no gradients, no glow bloom beyond the table's glass, no 3D rendering, no vector illustration look, no soft or feathered edges, no halftone dots over the flat background field, no tin robots, no globes, no CRT computers, no proof press, no readable English body text beyond the specified strings, preserve the visible dot pattern and the plate offset at 100% zoom.
```

### 章节 1「三秒露馅」（16:9）

```text
Use case: In-article section illustration.

Scene: A flat warm slate-grey background arranged like a bench under inspection — torn pulp-paper strips, crop marks at the corners, a signal-red registration crosshair at the upper left, one black triangle at the lower right.

Subject: A brass stopwatch lying face-up at the left, rendered as a coarse duotone halftone cut-out, its second hand stopped hard at the three-second mark. To its right a printed sheet lies flat with its lower-left corner peeled back and curling, revealing beneath it a rigid machine-set grid of identical empty ruled boxes. A taut signal-red thread runs from the stopwatch's crown across the frame and ties to the peeled corner, pulling it open.

Key details: Mid-century print-shop collage. Every physical object is a photograph reproduced as a coarse visible duotone halftone — a black dot screen plus a second spot-colour dot screen offset by one or two pixels, so the misregistration is legible at full size. Each object is then die-cut with a crisp 3px white sticker outline and a faint hard drop shadow. Edges stay razor sharp and are never eroded by the texture; keep the stopwatch's hand tip, its knurled crown and the peeled paper's crease sharp. The halftone dots appear only on the cut-out objects and paper scraps — the flat colour field behind them carries no dots. Paper-fibre grain covers the whole image. Colour architecture: warm slate grey as the ground, pulp off-white and kraft as the neutral paper layer, signal red as the single spot colour reserved for the thread, the second hand and the second halftone plate, brass ochre for the stopwatch body, black for geometric marks and the label block.

Composition: 16:9 horizontal. The stopwatch occupies 12%–34% of the width, centred at 48% height. The printed sheet occupies 40%–90% of the width and 20%–86% of the height, rotated about 9 degrees. The peeled corner sits at 44%–58% width. The label block sits at the lower right.

Text in image: On the stopwatch dial, small black numerals "0", "15", "30", "45" around the rim. The revealed grid boxes stay empty. At the lower right, white heavy Chinese sans (思源黑体 / Source Han Sans, Heavy) inside a solid black rectangle with a signal-red vertical bar along its left edge and a clipped upper-right corner: "三秒露馅". Render all text verbatim, no extra words.

Constraints: no gradients, no glow, no 3D rendering, no vector illustration look, no soft or feathered edges, no halftone dots over the flat background field, no tin robots, no folded maps, no wristwatches or digital timers, no motion blur or speed lines, no readable text beyond the specified strings, preserve the visible dot pattern and the plate offset at 100% zoom.
```

### 章节 2「水词堆」（16:9）· 连接物 = 物理反常

```text
Use case: In-article section illustration.

Scene: A flat deep pine-green background arranged like a compositor's bench — torn pulp-paper strips, crop marks at the corners, a six-swatch colour control bar down the right edge, a strip of masking tape at the upper left.

Subject: A cast-iron balance scale seen from the side, rendered as a coarse duotone halftone cut-out. Its left pan is heaped past the brim with dozens of identical metal type sorts, more of them spilled across the bench below — yet that pan hangs high. Its right pan carries a single type sort and has sunk all the way down, tilting the beam steeply. A deep-teal pointer needle at the beam's fulcrum swings hard toward the single sort.

Key details: Mid-century print-shop collage. Every physical object is a photograph reproduced as a coarse visible duotone halftone — a black dot screen plus a second spot-colour dot screen offset by one or two pixels, so the misregistration is legible at full size. Each object is then die-cut with a crisp 3px white sticker outline and a faint hard drop shadow. Edges stay razor sharp and are never eroded by the texture; keep the beam's straight edge, the pan chains and the individual type sorts' shoulders sharp so the heap never blurs into flat texture. The halftone dots appear only on the cut-out objects and paper scraps — the flat colour field behind them carries no dots. Paper-fibre grain covers the whole image. Colour architecture: deep pine green as the ground, pulp off-white and kraft as the neutral paper layer, deep teal as the single spot colour reserved for the pointer needle and the second halftone plate, rust orange as small punctuation in one background scrap, black for geometric marks and the label block.

Composition: 16:9 horizontal. The scale occupies 20%–82% of the width and 14%–84% of the height, the beam tilted about 22 degrees down to the right. The spilled type sorts scatter across 14%–46% of the width along the bottom. The label block sits at the lower right.

Text in image: No lettering on the type sorts — they read as blank metal blocks. At the lower right, white heavy Chinese sans (思源黑体 / Source Han Sans, Heavy) inside a solid black rectangle with a deep-teal vertical bar along its left edge and a clipped upper-right corner: "水词堆". Render all text verbatim, no extra words.

Constraints: no gradients, no glow, no 3D rendering, no vector illustration look, no soft or feathered edges, no halftone dots over the flat background field, no tin robots, no speaking tubes, no digital scales, no coins or money, no legible letters on the type sorts, no readable text beyond the specified string, preserve the visible dot pattern and the plate offset at 100% zoom.
```

### 章节 3「太整齐」（16:9）

```text
Use case: In-article section illustration.

Scene: A flat pale bone-grey background arranged like a proofreader's desk — torn pulp-paper strips, crop marks at the corners, a rust-orange registration crosshair at the lower left, one stapled kraft corner at the upper right.

Subject: A large printed sheet filling most of the frame, rendered as a coarse duotone halftone cut-out, its body text set as rows of identical black bars of exactly equal length, stacked into a flawless brick wall with no ragged edge anywhere. A steel setting rule lies across the upper third, its milled edge aligned dead flat against the rows. Near the lower third one single line breaks the pattern: it is handwritten, slanted and uneven, and a rust-orange grease-pencil ellipse is drawn around it, the stroke overshooting and doubling back at the join.

Key details: Mid-century print-shop collage. Every physical object is a photograph reproduced as a coarse visible duotone halftone — a black dot screen plus a second spot-colour dot screen offset by one or two pixels, so the misregistration is legible at full size. Each object is then die-cut with a crisp 3px white sticker outline and a faint hard drop shadow. Edges stay razor sharp and are never eroded by the texture; keep the steel rule's milled edge, the ends of every text bar and the pencil stroke's overshoot sharp. The halftone dots appear only on the cut-out objects and paper scraps — the flat colour field behind them carries no dots. Paper-fibre grain covers the whole image. Colour architecture: pale bone grey as the ground, pulp off-white as the neutral paper layer, rust orange as the single spot colour reserved for the grease-pencil ellipse, the registration marks and the second halftone plate, cool steel grey for the rule, black for the text bars, geometric marks and the label block. Never tint the printed sheet itself.

Composition: 16:9 horizontal. The printed sheet occupies 8%–92% of the width and 10%–88% of the height, rotated about 4 degrees. The steel rule crosses at 28% height. The circled handwritten line sits at 30%–68% of the width at 66% height. The label block sits at the lower right.

Text in image: The body rows are solid black bars carrying no readable letters. The circled line is handwritten and illegible. At the lower right, white heavy Chinese sans (思源黑体 / Source Han Sans, Heavy) inside a solid black rectangle with a rust-orange vertical bar along its left edge and a clipped upper-right corner: "太整齐". Render all text verbatim, no extra words.

Constraints: no gradients, no glow, no 3D rendering, no vector illustration look, no soft or feathered edges, no halftone dots over the flat background field, no tin robots, no thermometers, no readable body copy anywhere on the sheet, no ragged right margin in the machine-set rows, no readable text beyond the specified string, preserve the visible dot pattern and the plate offset at 100% zoom.
```

### 章节 4「没代价」（16:9）· 连接物 = 悬空未落 + 磨损对比

```text
Use case: In-article section illustration.

Scene: A flat burnt-ochre background arranged like a shop counter at closing — torn pulp-paper strips, crop marks at the corners, a six-swatch colour control bar along the top edge, one black triangle at the lower left.

Subject: A cast-iron receipt spike standing upright on a wooden base, rendered as a coarse duotone halftone cut-out, its steel point already driven through a thick sheaf of old receipts — creased, thumbed, water-marked, edges furred from handling, some torn where the spike pulled through. A single receipt hangs suspended in the air above the point, pristine and uncreased, its total line printed 0.00, not yet pierced. A brick-red thread of stamp ink runs down the spike's shaft from the sheaf.

Key details: Mid-century print-shop collage. Every physical object is a photograph reproduced as a coarse visible duotone halftone — a black dot screen plus a second spot-colour dot screen offset by one or two pixels, so the misregistration is legible at full size. Each object is then die-cut with a crisp 3px white sticker outline and a faint hard drop shadow. Edges stay razor sharp and are never eroded by the texture; keep the spike's needle point, the torn holes in the old receipts and the clean sheet's four corners sharp — the contrast between the furred old edges and the pristine floating one is the point of the image and must read instantly. The halftone dots appear only on the cut-out objects and paper scraps — the flat colour field behind them carries no dots. Paper-fibre grain covers the whole image. Colour architecture: burnt ochre as the ground, pulp off-white and aged kraft as the neutral paper layer, brick red as the single spot colour reserved for the ink trace and the second halftone plate, cool steel grey for the spike, black for geometric marks and the label block.

Composition: 16:9 horizontal. The spike and its sheaf occupy 34%–58% of the width, base at 88% height, point at 34% height. The floating clean receipt occupies 30%–64% of the width at 8%–30% height, rotated about 14 degrees. The label block sits at the lower right.

Text in image: On the floating clean receipt, small black monospaced type: "TOTAL  0.00". The pierced old receipts carry smudged illegible lines only. At the lower right, white heavy Chinese sans (思源黑体 / Source Han Sans, Heavy) inside a solid black rectangle with a brick-red vertical bar along its left edge and a clipped upper-right corner: "没代价". Render all text verbatim, no extra words.

Constraints: no gradients, no glow, no 3D rendering, no vector illustration look, no soft or feathered edges, no halftone dots over the flat background field, no tin robots, no folded maps, no coins, banknotes or currency symbols, no blood or injury imagery, no readable text beyond the specified strings, preserve the visible dot pattern and the plate offset at 100% zoom.
```

### 章节 5「只动三处」（16:9）· 留白即论点

```text
Use case: In-article section illustration.

Scene: A flat cobalt-blue background arranged like a proofreader's desk mid-pass — torn pulp-paper strips, crop marks at the corners, a signal-red registration crosshair at the upper right, a strip of masking tape at the lower left.

Subject: A single clean printed proof sheet occupying most of the frame, rendered as a coarse duotone halftone cut-out, its body text set as evenly spaced black bars carrying no readable letters. Exactly three signal-red proofreader's marks are struck onto it in grease pencil, each pulled out to the sheet's margin by a short red leader line ending in a small numbered circle: a deletion loop through one bar, a transposition hook swapping two adjacent bars, a caret with a replacement stroke above a third. Everything else on the sheet is untouched. A red-and-blue proofreading pencil rests diagonally across the sheet's lower edge, its worn tip pointing at the third mark.

Key details: Mid-century print-shop collage. Every physical object is a photograph reproduced as a coarse visible duotone halftone — a black dot screen plus a second spot-colour dot screen offset by one or two pixels, so the misregistration is legible at full size. Each object is then die-cut with a crisp 3px white sticker outline and a faint hard drop shadow. Edges stay razor sharp and are never eroded by the texture; keep the pencil's sharpened tip, the caret's point and the ends of every text bar sharp — the grease-pencil strokes are the only hand-made line in the frame and keep their waxy broken texture without softening. The halftone dots appear only on the cut-out objects and paper scraps — the flat colour field behind them carries no dots. Paper-fibre grain covers the whole image. Colour architecture: cobalt blue as the ground, pulp off-white as the neutral paper layer, signal red as the single spot colour reserved for the three marks, their leader lines and the second halftone plate, black for the text bars, geometric marks and the label block. Keep the untouched majority of the sheet visually quiet — no marks, no tint, no texture beyond the halftone.

Composition: 16:9 horizontal. The proof sheet occupies 10%–90% of the width and 12%–86% of the height, rotated about 5 degrees. The three marks sit at 26% height, 48% height and 70% height, staggered horizontally so no two share a column. The pencil crosses 52%–88% of the width along the bottom. The label block sits at the lower left.

Text in image: Small black numerals "1", "2", "3" inside the three margin circles. The body rows are solid black bars carrying no readable letters. At the lower left, white heavy Chinese sans (思源黑体 / Source Han Sans, Heavy) inside a solid black rectangle with a signal-red vertical bar along its left edge and a clipped upper-right corner: "只动三处". Render all text verbatim, no extra words.

Constraints: no gradients, no glow, no 3D rendering, no vector illustration look, no soft or feathered edges, no halftone dots over the flat background field, no tin robots, no speaking tubes, no more than three red marks anywhere in the frame, no readable body copy on the sheet, no readable text beyond the specified strings, preserve the visible dot pattern and the plate offset at 100% zoom.
```

---

## 第二套 · 《从 0 到 1 装上 Claude Code》· 抽取表

同一母版换题材。抽取表先列全再编译，确认三张表都不重复：

| 图 | 寄存器 | 主物件 | 连接物 | 标签 |
|---|---|---|---|---|
| 封面 5:2 | R1 油墨黑 | 活字排版盘 + 样张 | 层压（样张角压标题） | — |
| 章节 1 | R6 暖石灰 | 斜置的排字盘（三格） | 红色印章戳过格沿 | 备齐三样 |
| 章节 2 | R3 深墨绿 | 凸版打样机 | 杠杆被压下 → 吐出样张 | 一行命令 |
| 章节 3 | R4 钴蓝 | 摊开的折叠地图 | 虚线路径 + 红图钉 | 认路 |
| 章节 4 | R5 焦赭 | 传声筒喇叭 + 售货柜 | 垂坠的编织线 | 说人话 |
| 章节 5 | R7 骨白 | 玻璃温度计 | 颜色的断点（红骤降为蓝） | 泼冷水 |

代表条 · 章节 2「一行命令」：

```text
Use case: In-article section illustration.

Scene: A flat deep pine-green background arranged like a print-shop floor — torn pulp-paper strips, crop marks at the corners, a six-swatch colour control bar running down the right edge, one black triangle at the lower left.

Subject: A cast-iron tabletop proof press seen three-quarter from the left, its long lever pulled down, rendered as a coarse duotone halftone cut-out. A single crisp proof sheet emerges from under the platen and lies flat toward the viewer, carrying one line of monospaced type. Two crumpled rejected proofs lie discarded at the lower left, their printed lines smeared. A rust-orange registration crosshair sits directly above the press.

Key details: Mid-century print-shop collage. Every physical object is a photograph reproduced as a coarse visible duotone halftone — a black dot screen plus a second spot-colour dot screen offset by one or two pixels, so the misregistration is legible at full size. Each object is then die-cut with a crisp 3px white sticker outline and a faint hard drop shadow. Edges stay razor sharp and are never eroded by the texture; keep the lever's handle, the platen's straight edge and the crumpled paper's creases sharp. The halftone dots appear only on the cut-out objects and paper scraps — the flat colour field behind them carries no dots. Paper-fibre grain covers the whole image. Colour architecture: deep pine green as the ground, pulp off-white as the neutral paper layer, rust orange as the single spot colour reserved for the second halftone plate and the registration marks, mustard yellow as small punctuation in one scrap, black for geometric marks and the label block.

Composition: 16:9 horizontal. The press occupies 22%–66% of the width, its top edge at 14% of the image height. The clean proof sheet lies across 40%–80% of the width in the lower third, angled about 20 degrees. The crumpled proofs sit at 6%–24% width along the bottom. The label block sits at the lower right.

Text in image: On the clean proof sheet, one line of black monospaced type, letterpress-crisp: "npm install -g @anthropic-ai/claude-code". The crumpled proofs carry smeared illegible lines only. At the lower right, white heavy Chinese sans (思源黑体 / Source Han Sans, Heavy) inside a solid black rectangle with a rust-orange vertical bar along its left edge and a clipped upper-right corner: "一行命令". Render all text verbatim, no extra words.

Constraints: no gradients, no glow, no 3D rendering, no vector illustration look, no soft or feathered edges, no halftone dots over the flat background field, no tin robots, no vacuum tubes, no punched paper tape, no CRT computers, no rubber stamps, no readable text beyond the specified strings, preserve the visible dot pattern and the plate offset at 100% zoom.
```

> 这条里的命令行是全套唯一的硬伤点。`quality` 走 high，出图后逐字符核 `@anthropic-ai/claude-code`，错一个字符整张作废。

---

## 三个可复用的手法

从这两套里提炼，换题材可直接搬：

- **物理反常**（「水词堆」）——堆满的一侧翘起、单枚的一侧沉底。用一个违反常识的物理状态把论点画出来，不靠文字解释。适合"量大但无效"这类判断。
- **磨损对比**（「没代价」）——同一件物品的两种磨损状态并置：边缘起毛磨破 vs 四角笔挺。这是这套质感体系里最省力的叙事装置，因为网点本身就放大边缘差异。
- **留白即论点**（「只动三处」）——画面 90% 保持干净，只有三处标记。必须在 Constraints 里写死 `no more than three red marks`，不写模型一定会多画。
