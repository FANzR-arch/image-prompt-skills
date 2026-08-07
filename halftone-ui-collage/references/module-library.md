# 模块库

四张表，每次生成从每张各抽一项。**成组产出时先把整组抽取结果列成表，确认无重复再编译。**

---

## 表一 · 配色寄存器（五个角色色，一色一职）

一次选一个，整条提示词统一。五个角色分别填进基座的 `{{BG}}` `{{INK}}` `{{SWASH}}` `{{ACCENT}}` `{{ORGANIC}}` `{{GREY}}`。

| 寄存器 | BG 背景 | INK 主色 | SWASH 笔刷 | ACCENT 强调 | ORGANIC 底角 | GREY 中性 |
|---|---|---|---|---|---|---|
| **Ink & Clay** | warm sand | deep ink navy | pale dusty blue | warm terracotta | deep olive green | warm greige |
| **Plum & Moss** | pale oat | deep aubergine plum | dusty rose | bright moss green | deep charcoal green | warm greige |
| **Slate & Amber** | pale bone | charcoal slate blue | pale dusty lilac | amber gold | deep pine green | oat grey |
| **Teal & Rust** | pale linen | deep teal | pale seafoam | burnt rust orange | deep espresso brown | warm stone grey |
| **Burgundy & Sage** | warm ivory | deep burgundy | dusty blush | sage green | deep bottle green | warm oat grey |

**三条色彩规则：**

1. **SWASH 必须是低饱和的有色相，永不用中性灰。** 用中性灰会和「no large flat featureless grey plane」直接打架，也会和黑白网点人物糊在一起。
2. **BG 与 GREY 不共用色名。** 同名会让占位条在卡片上失去层次，或让背景被读成一排条。
3. **ACCENT 全图只允许出现在状态与高亮上**——不上植物线、不上占位条、不上背景。

扩新寄存器时照这六个角色补齐，缺任何一个角色都不算完整寄存器。

---

## 表二 · 人物调度（全部在手部预算内，视线均有画内落点）

| # | 姿态 | 动作手 | 另一只手 | 视线落点 |
|---|---|---|---|---|
| P1 | 前景坐在办公椅上，身体微向右转 | 一只手轻放在腿上 | 轻放桌面 | 肩后显示器 |
| P2 | 前景坐姿，上身微向左转 | 一只手轻放桌面 | 轻放腿上 | 右侧卡片方向 |
| P3 | 前景端坐，身体略转 | 一只手放在椅子扶手 | 垂在桌沿内侧 | 肩后显示器 |
| P4 | 前景坐姿，身体略偏 | 一只手拿一张纸，放在身体侧面、不遮脸 | 轻放桌面 | 手上的纸 |
| P5 | 前景放松靠椅 | 一只手轻扶放在桌面的马克杯柄 | 轻放腿上 | 肩后显示器 |
| P6 | 前景端坐 | 双手都轻放在腿上或椅子扶手 | — | 肩后显示器 |

P6 是**降级姿态**：手连续出错时直接换成它，把手部风险清零。

**禁用姿态**（原始参考稿里出现过、已实测为高危）：扶眼镜、双手包握杯子、抱臂同时持物、手臂勾椅背、指向画外某物。

---

## 表三 · 卡片组合（上下两卡必须一图形一行列）

**图形卡**（上卡默认）

| 代号 | 写法 |
|---|---|
| G1 堆叠块 | `a diagram card showing a vertical stack of four labelled blocks` |
| G2 分支树 | `a diagram card showing a small branching tree of connected nodes fanning from one point into four` |
| G3 节点网 | `a diagram card showing eight small circles connected by thin straight lines into a loose web` |
| G4 折线图 | `a chart card showing a flat line graph with one clearly marked peak circled in the accent colour` |
| G5 周网格 | `a schedule card showing a seven-column week grid with three filled cells` |
| G6 数字磁贴 | `a stat card showing three small tiles, each with a short number and a placeholder caption bar` |

**行列卡**（下卡默认）

| 代号 | 写法 |
|---|---|
| L1 状态列表 | `a status list with a faint tinted header strip and three rows separated by hairlines, each row holding a status icon, a placeholder bar and a short right-aligned meta bar` |
| L2 来源列表 | `a source list with five rows, each holding a small rounded square, a placeholder bar and a short right-aligned meta bar` |
| L3 标签列表 | `a tag list with a faint tinted header strip and three rows, each holding a small rounded pill, a placeholder bar and a short right-aligned meta bar` |
| L4 指标列表 | `a metrics list with a faint tinted header strip and three rows separated by hairlines, each row holding a small icon, a placeholder bar and a short right-aligned meta bar` |
| L5 版本列表 | `a version list with three rows separated by hairlines, each row holding a small dot marker, a placeholder bar and a short right-aligned meta bar` |

上下顺序可互换（图形卡放下面也成立），但**两张必须跨类**。同为行列卡时行数、图标形状再怎么改，出图仍会读成一对孪生卡——这是「no identical structure between the two cards」真正想封的东西。

**chip**：1–2 词，跨压上卡左下角，同时压住卡边和背景。

---

## 表四 · 屏幕内容（全部无可读单词）

| 代号 | 写法 |
|---|---|
| S1 文本编辑器 | `text editor with several placeholder bars and three short highlighted token chips in the ink colour` |
| S2 搜索结果 | `interface showing a search field and a stack of result rows` |
| S3 周排期条 | `interface showing a horizontal week strip with five slots, two of them filled in the accent colour` |
| S4 仪表盘 | `dashboard with two small stat tiles and a short row of bars` |
| S5 笔记界面 | `note interface with a title bar and several short placeholder lines` |
| S6 看板 | `board interface with three columns of small stacked rectangles` |

一律接 `no readable words on the screen`——屏幕上出现真单词是这套风格第二常见的失手。

**单字母例外**：日历列头（M T W T F S S）、序号这类单字母和数字是想要的东西，首图实测出得很干净，不要封。封堵只针对**可读单词与句子**。

---

## 主题映射（起手建议，不是硬绑定）

| 主题类型 | 人物 | 屏幕 | 上卡 | 下卡 | 寄存器 |
|---|---|---|---|---|---|
| 写作 / 提示词工程 | P1 | S1 | G1 | L5 | Ink & Clay |
| 调研 / Agent 工作流 | P4 | S2 | G2 | L2 | Plum & Moss |
| 排期 / 发布管线 | P3 | S3 | G5 | L1 | Slate & Amber |
| 数据 / 回测复盘 | P5 | S4 | G4 | L4 | Teal & Rust |
| 知识库 / 笔记系统 | P2 | S5 | G3 | L3 | Burgundy & Sage |
| 协作 / 项目管理 | P6 | S6 | G6 | L1 | 任选未用过的 |

成组产出时按此表铺一遍，再检查六项模块有没有跨张重复。
