# 瑞士国际主义海报：6 套换标题即用的生图提示词

做科技、方法论、商业分析、AI 工具这类内容的封面时，瑞士国际主义（Swiss International Typographic Style）通常比复古插画、赛博、拼贴更合适——它不靠装饰，靠信息秩序。

但直接让 AI「画一张瑞士风格海报」，十有八九给你一张 2020s 企业 PPT 封面：大标题在左上、右边一张配图、底部几个小色块标签。干净、现代，却不是瑞士。

下面 6 套提示词是反复测试后固化的，换掉标题就能用。先讲清楚它们为什么有效。

## 四个让 AI 真出瑞士味的动作

1. **锚一个设计师，别只写「瑞士风格」。** 流派名已被模型平均化，会退回当代极简。第一行指名 Müller-Brockmann / Hofmann / Ruder / Max Bill / Weingart，方向立刻收窄。
2. **几何成系统或成结构。** 几十个按数学级数排列的元素（弧、方阵、色带），或一个被放到结构尺度的大形。要避免的是孤立的卡通式图标。
3. **拉丁扛冲击，中文扛意义。** 瑞士排印的节奏长在拉丁字母上，纯中文大字容易变标语。大拉丁词当主视觉 + 一行小中文交代主题，都对齐同一套网格。
4. **留白要被网格切分。** 大留白本身没问题，要避免的是「左满右空」那种没经营的死空。

## 怎么用

- 复制对应一套，把 `"<LATIN>"` 换成你的大拉丁词，把 `「<标题>」` 换成中文主题。
- 想要**纯拉丁炫技图**：删掉中文那行。
- 想要**传播封面**（读者要秒懂）：把中文调大、拉丁缩小当副标。
- 模型推荐 gpt-image-2 / ChatGPT Images。中文短标题能稳定渲染；超长中文建议留区域后期叠加。

---

## 1 · 同心弧 / 红（最经典，适合工具、科技、秩序感主题）

```text
STYLE ANCHOR — in the manner of Josef Müller-Brockmann's 1950s Zürich concert posters: mathematical grid, systematic geometry, type as structure.
A vertical 4:5 Swiss International Typographic Style poster — authentic 1950s offset print.
LOCKED — everything aligns to one underlying modular grid; one grotesk sans-serif family only; flat color with hard edges; no gradient, 3D, shadow, texture or ornament; objective, rational, asymmetric.
DOMINANT VISUAL — a dense progressive series of dozens of concentric arcs on mathematical progression, flat-painted, radiating from one corner.
COLOR — flat saturated vermilion red field; black and warm off-white only. Hard edges, no gradients.
TYPOGRAPHY — one grotesk family, regular-to-bold weight, tight optical spacing, two sizes with clear hierarchy.
  · Latin headline "<LATIN>" very large, placed across the top band on the grid, grid-aligned; small Chinese line 「<标题>」 directly beneath it on the same grid.
GRID & SPACE — the modular grid governs every element; negative space is structural, balanced, grid-defined.
TEXT — only "<LATIN>" and 「<标题>」. Render them precisely, no extra or garbled text.
AVOID — modern minimalist AI poster; PowerPoint / brochure template; isolated clip-art icon; decorative full-bleed or stock photo; gradients; 3D; drop shadows; vintage grunge; heavy decorative CJK display type.
QUALITY — authentic 1950s Swiss offset print, sharp edges, precise alignment, flat color.
```

## 2 · 黑白形态（高张力、无彩色，适合对比、冷峻主题）

```text
STYLE ANCHOR — in the manner of Armin Hofmann: black-and-white form, positive-negative figure-ground tension.
A vertical 4:5 Swiss International Typographic Style poster — authentic 1950s offset print.
LOCKED — everything aligns to one underlying modular grid; one grotesk sans-serif family only; flat color with hard edges; no gradient, 3D, shadow, texture or ornament; objective, rational, asymmetric.
DOMINANT VISUAL — one or few boldly scaled geometric forms (a large circle, a rectangle and one diagonal axis) with large structural negative space, exploiting positive-negative tension.
COLOR — pure black and white only. Hard edges, no gradients.
TYPOGRAPHY — one grotesk family, bold weight, tight optical spacing, two sizes with clear hierarchy.
  · Latin headline "<LATIN>" very large, placed across the bottom band on the grid, grid-aligned; small Chinese line 「<标题>」 above it on the same grid.
GRID & SPACE — the modular grid governs every element; negative space is structural, balanced, grid-defined.
TEXT — only "<LATIN>" and 「<标题>」. Render them precisely, no extra or garbled text.
AVOID — modern minimalist AI poster; PowerPoint / brochure template; isolated clip-art icon; decorative full-bleed or stock photo; gradients; 3D; drop shadows; vintage grunge; heavy decorative CJK display type.
QUALITY — authentic 1950s Swiss offset print, sharp edges, precise alignment, flat color.
```

## 3 · 字体即图 / 黄黑（出图最稳，适合观点、方法论金句）

```text
STYLE ANCHOR — in the manner of Emil Ruder: typographic rhythm, flush structure, controlled hierarchy.
A 16:9 landscape Swiss International Typographic Style poster — authentic 1950s offset print.
LOCKED — everything aligns to one underlying modular grid; one grotesk sans-serif family only; flat color with hard edges; no gradient, 3D, shadow, texture or ornament; objective, rational, asymmetric.
DOMINANT VISUAL — the headline itself is the composition, set on a visible grid; the remaining columns hold a small block of thin functional rules so no area is dead.
COLOR — high-alert yellow field; black only. Hard edges, no gradients.
TYPOGRAPHY — one grotesk family, regular-to-bold weight, tight optical spacing, three sizes with clear hierarchy.
  · Latin headline "<LATIN>" very large, stepped across two columns on the grid, grid-aligned; small Chinese line 「<标题>」 set tiny, flush to the same grid.
GRID & SPACE — the modular grid governs every element; negative space is structural, balanced, grid-defined.
TEXT — only "<LATIN>" and 「<标题>」. Render them precisely, no extra or garbled text.
AVOID — modern minimalist AI poster; PowerPoint / brochure template; isolated clip-art icon; decorative full-bleed or stock photo; gradients; 3D; drop shadows; vintage grunge; heavy decorative CJK display type.
QUALITY — authentic 1950s Swiss offset print, sharp edges, precise alignment, flat color.
```

## 4 · 纯网格 / 黑底红（编辑感、信息密度，适合报告、数据观点）

```text
STYLE ANCHOR — in the manner of Josef Müller-Brockmann der Film: strict column grid, objective, type-driven.
A 16:9 landscape Swiss International Typographic Style poster — authentic 1950s offset print.
LOCKED — everything aligns to one underlying modular grid; one grotesk sans-serif family only; flat color with hard edges; no gradient, 3D, shadow, texture or ornament; objective, rational, asymmetric.
DOMINANT VISUAL — a dense strict multi-column modular grid as the protagonist, with flat geometric marks of progressing size snapping to columns and one flat red form used structurally.
COLOR — black field; warm off-white type; one flat red accent used structurally. Hard edges, no gradients.
TYPOGRAPHY — one grotesk family, regular-to-bold weight, tight optical spacing, two sizes with clear hierarchy.
  · Latin headline "<LATIN>" very large, placed in a middle band across the left columns on the grid, grid-aligned; small Chinese line 「<标题>」 on the same grid nearby.
GRID & SPACE — the modular grid governs every element; negative space is structural, balanced, grid-defined.
TEXT — only "<LATIN>" and 「<标题>」. Render them precisely, no extra or garbled text.
AVOID — modern minimalist AI poster; PowerPoint / brochure template; isolated clip-art icon; decorative full-bleed or stock photo; gradients; 3D; drop shadows; vintage grunge; heavy decorative CJK display type.
QUALITY — authentic 1950s Swiss offset print, sharp edges, precise alignment, flat color.
```

## 5 · 光谱色带（结构 / 层次主题，适合决策、框架、分层方法）

```text
STYLE ANCHOR — in the manner of Max Bill: concrete art, color geometry, precise proportion.
A vertical 4:5 Swiss International Typographic Style poster — authentic 1950s offset print.
LOCKED — everything aligns to one underlying modular grid; one grotesk sans-serif family only; flat color with hard edges; no gradient, 3D, shadow, texture or ornament; objective, rational, asymmetric.
DOMINANT VISUAL — flat-painted horizontal bands of mathematically progressing width, edge-to-edge, integrated with the typography as one composition.
COLOR — warm off-white field; black; one flat cyan accent on a single band. Hard edges, no gradients.
TYPOGRAPHY — one grotesk family, regular-to-bold weight, tight optical spacing, two sizes with clear hierarchy.
  · Latin headline "<LATIN>" very large, placed across the top band on the grid, grid-aligned; small Chinese line 「<标题>」 on the same grid beneath it.
GRID & SPACE — the modular grid governs every element; negative space is structural, balanced, grid-defined.
TEXT — only "<LATIN>" and 「<标题>」. Render them precisely, no extra or garbled text.
AVOID — data-chart / infographic / bar-chart look; modern minimalist AI poster; PowerPoint / brochure template; isolated clip-art icon; decorative photo; gradients; 3D; drop shadows; vintage grunge; heavy decorative CJK display type.
QUALITY — authentic 1950s Swiss offset print, sharp edges, precise alignment, flat color.
```

## 6 · 受控破格 / 米白橙（设计、实验、反叛主题）

```text
STYLE ANCHOR — in the manner of Wolfgang Weingart: Swiss New Wave, one controlled rule-break, layering.
A vertical 4:5 Swiss International Typographic Style poster — authentic 1950s offset print.
LOCKED — everything aligns to one underlying modular grid; one grotesk sans-serif family only; flat color with hard edges; no gradient, 3D, shadow, texture or ornament; objective, rational, asymmetric.
DOMINANT VISUAL — a strict grid as base with one deliberate rule-break: a single flat orange rectangle rotated a few degrees and layered over the grid; everything else strictly aligned.
COLOR — warm off-white field; black; one flat orange accent. Hard edges, no gradients.
TYPOGRAPHY — one grotesk family, regular-to-bold weight, tight optical spacing, two sizes with clear hierarchy.
  · Latin headline "<LATIN>" very large, set vertically along the left margin on the grid, grid-aligned; small Chinese line 「<标题>」 on the same grid.
GRID & SPACE — the modular grid governs every element; negative space is structural, balanced, grid-defined.
TEXT — only "<LATIN>" and 「<标题>」. Render them precisely, no extra or garbled text.
AVOID — over-broken layout; modern minimalist AI poster; PowerPoint / brochure template; isolated clip-art icon; decorative photo; gradients; 3D; drop shadows; vintage grunge; heavy decorative CJK display type.
QUALITY — authentic 1950s Swiss offset print, sharp edges, precise alignment, flat color.
```

---

## 一句话选型

| 你的主题 | 用哪套 |
|---|---|
| 工具教程 / 科技 / 秩序 | 1 同心弧 |
| 对比 / 张力 / 冷峻 | 2 黑白形态 |
| 观点 / 金句 | 3 字体黄黑 |
| 报告 / 数据 / 编辑感 | 4 纯网格 |
| 结构 / 层次 / 决策 | 5 色带 |
| 设计 / 实验 / 反叛 | 6 破格 |
