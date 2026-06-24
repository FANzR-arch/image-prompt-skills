# 编译契约（消歧义铁律）

每次输出前必须满足。这是「成品」和「拼装件」的分界：拼装件可以有选项，成品不能。

## 5 条铁律

1. **每个槽位解析成唯一值**：删掉所有 `/` 选项和 `{}` 占位。成品里不允许出现 `red / cobalt / yellow` 这类菜单。
2. **正文零中文**：提示词正文只能出现英文美术指导；唯一例外是「要渲染进画面的标题文字」。任何中文注释（如「需要照片时改为…」）一律不能留——模型会把它画进海报。
3. **一个主视觉**：DOMINANT VISUAL 只保留一种引擎。不并列「密集系统」和「单个大形」。
4. **否定只进 AVOID**：正文用正向描述，所有 `no / not / never / avoid` 收进末尾 AVOID 块（图像模型对散落的否定词处理弱）。
5. **要渲染的文字只声明一次**：在 TEXT 行用引号 `"..."` 和「」逐项写明画面里出现的字，并要求精确呈现；其它字段不再重复文字本身。

## 锁死的风格内核（LOCKED，每条必带）

无论选什么模块，这几条恒定：

- 一切元素对齐**同一套严格模块网格（如 6 栏）**；type、几何标记、图块都吸附同一套网格；
- **层级靠尺度和位置，不靠装饰**；
- **单一中性 grotesk** 字族，中等字重（禁衬线 / 手写 / 重装饰中文美术黑体 / 粗海报体）；
- **平涂、硬边**；无渐变、3D、投影、纸纹、做旧颗粒、半调网点；
- **客观、理性、无装饰花纹**；
- **非对称倾向**；留白要有比例、是结构的一部分，不是没填满的背景。

## 风格纯度护栏（反偏移，必带进 AVOID）

瑞士国际主义的内核是「用网格组织排印/信息」，不是几何抽象。AI 最常把它生成成邻近流派，必须显式挡住：

- **De Stijl**：红黄蓝大色块构成 → 禁。配色走「黑 / 米白 / 暖灰 + 一个强调色」；多原色块不要。
- **Bauhaus 基础课**：模块变体矩阵、符号图谱、图案展示板 → 禁。几何要服务信息，不做"展示板"。
- **Op Art**：旋转螺旋、视错觉图形 → 禁。
- **当代品牌视觉**：大斜带 / 满版品牌色 / logo 化孤立单形 → 禁，除非该元素有明确网格功能。
- **数据图表**：条形图 / 流程图既视感 → 弱化，几何要像版面不像图表。

> 两个合法 register 不算偏移：①「编辑/克制向」黑白灰 + 红细线；②「音乐会/冲击向」整版**单色**（满版红即 Müller-Brockmann Beethoven 海报）。要禁的是**多原色块**，不是单一饱和色。

> 中文标题：中等字重中性黑体，不用粗海报体；最多一个大中文主标 + 一行小字。

## 固定字段顺序

成品提示词永远按此顺序，人和模型都不必猜：

```
STYLE ANCHOR  →  FORMAT  →  LOCKED(风格内核)  →  DOMINANT VISUAL(一个)
→  COLOR(解析后)  →  TYPOGRAPHY(字体+标题位置)  →  GRID & SPACE
→  TEXT(要渲染的文字, 声明一次)  →  AVOID(所有否定)  →  QUALITY
```

## 成品骨架（填好即发，无占位符）

```text
STYLE ANCHOR — in the manner of <anchor>: <anchor mechanism>.

A <format> Swiss International Typographic Style poster — authentic 1950s offset print.

LOCKED — everything aligns to one underlying modular grid; one grotesk sans-serif family only; flat color with hard edges; no gradient, 3D, shadow, texture or ornament; objective, rational, asymmetric.

DOMINANT VISUAL — <one resolved engine, flat-painted>.

COLOR — <one resolved palette>. Hard edges, no gradients.

TYPOGRAPHY — one neutral grotesk family, medium weight (Latin may go bold; Chinese stays medium, never bold poster type), tight optical spacing, two or three sizes; hierarchy by scale and position, not decoration.
  · <headline declaration: Latin and/or Chinese per textmode> placed <one resolved placement> on the grid, grid-aligned.

GRID & SPACE — the modular grid governs every element; negative space is structural, balanced, grid-defined.

TEXT — only <the exact strings to render>. Render them precisely, no extra or garbled text.

AVOID — Bauhaus module matrix / pattern board; De Stijl primary-color blocks; Op Art spiral; data-chart look; brand-style diagonal ribbon or logo-like single form without grid function; modern minimalist AI poster; PowerPoint / brochure template; gradients; 3D; drop shadows; vintage grunge; heavy / bold display CJK type.

QUALITY — authentic 1950s Swiss offset print, sharp edges, precise alignment, flat color.
```

## 文字模式如何落到 TEXT / TYPOGRAPHY

- **TA 纯拉丁**：headline = 一个大拉丁词 + 可选一行小拉丁副标；不出现中文。
- **TB 中文主标 + 拉丁小字**：大中文标题承担意义，小拉丁副标承担纹理。用于传播封面。
- **TC 拉丁主标 + 中文小标**：大拉丁词当视觉冲击，一行小中文交代主题。用于展示图。

三种模式都遵守铁律 2/5：中文只作为「要渲染的标题」出现，且在 TEXT 行声明。
