# 模块库（作者工具，不外露给用户）

每个槽位选一个，交给编译契约组装。下表的英文短语就是写进成品的措辞。

## 锚点 ANCHOR（设计师，放第一行）

| ID | 锚点 | 写进 prompt 的机制 |
|---|---|---|
| MB | Josef Müller-Brockmann | `mathematical grid, systematic geometry, type as structure` |
| HOF | Armin Hofmann | `black-and-white form, positive-negative figure-ground tension` |
| RUD | Emil Ruder | `typographic rhythm, flush structure, controlled hierarchy` |
| BILL | Max Bill | `concrete art, color geometry, precise proportion` |
| WEIN | Wolfgang Weingart | `Swiss New Wave, one controlled rule-break, layering` |

## 主视觉 ENGINE（只选一个）

| ID | 名称 | 写进 prompt |
|---|---|---|
| E1 | 同心弧 | `a dense progressive series of dozens of concentric arcs on mathematical progression` |
| E2 | 旋转方阵 | `a full field of nested and progressively rotated squares on a strict grid` |
| E3 | 色带 | `flat-painted bands of mathematically progressing width, integrated with the type` |
| E4 | 字体即图 | `the headline itself is the composition, set on a visible grid` |
| E5 | 纯网格 | `a dense strict multi-column modular grid as the protagonist, with flat geometric marks of progressing size snapping to columns` |
| E6 | 对角动势 | `one strong diagonal axis with flat geometric forms balancing along it` |
| E7 | 单个大形 | `one or few boldly scaled geometric forms with large structural negative space` |
| E8 | 客观摄影 | `one objective black-and-white photo, hard rectangular crop, locked into a single grid cell` |

## 配色 COLOR（只选一个）

| ID | 写进 prompt |
|---|---|
| K1 红 | `flat saturated vermilion red field; black and warm off-white only` |
| K2 钴蓝 | `cobalt blue field; black and white only` |
| K3 黄黑 | `high-alert yellow field; black only` |
| K4 黑底强调 | `black field; warm off-white type; one flat saturated accent (red or cyan) used structurally` |
| K5 纯黑白 | `pure black and white only` |
| K6 米白次色 | `warm off-white field; black; one flat secondary (orange / cobalt / cyan)` |

> 内核要求平涂硬边无渐变；可用 1–3 个平涂色，禁渐变和脏色。

## 标题位置 PLACEMENT（只选一个）

`P1 顶部横带` / `P2 底部横带` / `P3 竖排沿边缘` / `P4 中段` / `P5 阶梯错位` — 写法统一为 `placed <position> on the grid, grid-aligned`。

## 画幅 FORMAT

`F1 vertical 4:5` / `F2 16:9 landscape` / `F3 1:1 square` / `F4 wide 5:2 landscape`

> 注：gpt-image-2 / ChatGPT 原生只给 1:1 / 3:2 / 2:3，5:2 需裁切或换支持自定义比例的工具。

## 文字模式 TEXTMODE

`TA 纯拉丁` / `TB 中文主标+拉丁小字` / `TC 拉丁主标+中文小标`（落法见编译契约）。

---

## 意图 → 模块映射表

按用户标题与上下文推断，给每个槽位定一个值。

| 维度 | 推断信号 | 选 |
|---|---|---|
| 用途 | 展示图 / 作品集 / 炫技 | TEXTMODE = TC（或纯炫技 TA） |
| 用途 | 传播封面 / 要被读者秒懂 | TEXTMODE = TB |
| 内容 | 方法论 / 系统 / 知识管理 | E5 或 E3；K4 / K2 |
| 内容 | 工具教程 / 科技 / AI | E1 或 E2；K1 / K2 |
| 内容 | 商业 / 报告 / 数据 | E5 或 E3；K6 / K4 |
| 内容 | 设计 / 字体 / 排版 | E4 或 E2；K1 / K5 |
| 内容 | 设计实验 / 文化 / 反叛 | WEIN + E7/E6（受控破格）；K6 |
| 内容 | 决策 / 层次 / 结构 | E3；K4 |
| 语气 | 理性 / 可信 / 冷静 | K2 / K5 |
| 语气 | 高能 / 警示 / 冲突 | K3 / K1 |
| 平台 | X / 小红书竖版 | F1 |
| 平台 | 文章头图 / 视频封面 | F2 |
| 平台 | 方形 / 头像位 | F3 |
| 锚点 | 跟随主视觉 | E1/E5→MB，E2/E3→BILL，E4→RUD，E7→HOF，破格→WEIN，E6→MB/构成主义 |

冲突时优先级：用户明确指定 > 用途 > 内容类型 > 语气 > 默认。同一标题允许多种合理解，**择优定一个**，在选型理由里说明，不要并列输出。
