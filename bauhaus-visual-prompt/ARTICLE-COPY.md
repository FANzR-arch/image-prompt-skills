# 包豪斯视觉提示词：简易版 + Skill 版

包豪斯提示词的关键，不是让 AI 往画面上贴红黄蓝几何，而是先判断媒介：封面、配图、海报、还是室内照片重绘。

## 完整简易提示词结构（复制即用）

复制下面整段给 AI，再替换 `INPUT` 里的需求。

```text
INPUT：
请根据我输入的一句话或上传的图片生成包豪斯风格视觉。例如：
“横板5:2，生成一张包豪斯风格文章封面，标题是：把生活重新设计一遍。”
“生成一张16:9正文配图，主题是：结构比装饰更重要。”
“竖版2:3，生成一张包豪斯风格活动海报，标题是：AI DESIGN SYSTEM。”
“参考我上传的室内照片，把这个房间重绘成包豪斯风格工作室。”

TASK：
根据 INPUT 自动识别用途、画幅、标题、是否有参考图，并生成对应的包豪斯风格图像。

自动处理规则：
* 如果是文章封面：重点处理标题区、几何构图、视觉重心和留白。
* 如果是正文配图：重点处理概念解释、结构图、几何关系和清晰表达。
* 如果是海报：重点处理展览海报感、强标题、图文一体化构图。
* 如果是室内照片重绘：保留原图空间结构、视角、门窗、主要家具位置，只重绘材质、家具、灯具、色彩和空间气质。

IMAGE STYLE：
Create an authentic Bauhaus-inspired visual system based on modernist design-school principles: function-first organization, strict geometry, clear structure, rational composition, flat color, disciplined typography, and no ornament.

VISUAL LANGUAGE：
Use circles, rectangles, lines, modular blocks, asymmetric layout, generous negative space, and controlled red, yellow, blue, black, off-white accents. Every shape should have a structural role, not just decoration.

TYPOGRAPHY：
If text is needed, use bold modernist sans-serif typography with clear hierarchy. Keep text minimal. Do not invent random dates, issue numbers, captions, URLs, logos, or fake small text.

INTERIOR RULE：
If an uploaded interior photo is provided, preserve the original room perspective, walls, windows, doors, proportions, and main furniture layout. Redesign it with white plaster walls, modular furniture, tubular steel chairs, simple work tables, functional pendant lamps, open circulation, and controlled primary-color accents.

AVOID：
Generic red-yellow-blue decoration, random geometric stickers, vintage grunge paper, gradients, glossy 3D, luxury marble, Scandinavian cozy decor, cyberpunk metal, ornate patterns, fake text, clutter, and mixing poster typography into interiors.

QUALITY：
Clean modernist design-school feeling, useful structure, sharp geometry, flat color, rational composition, visually clear and immediately usable.
```

## 你只需要改 INPUT

```text
横板5:2，生成一张包豪斯风格文章封面，标题是：结构比装饰更重要。
```

```text
16:9，生成一张正文配图，主题是：提示词不是描述风格，而是组织结构。
```

```text
竖版2:3，生成一张包豪斯风格海报，标题是：FORM FOLLOWS FUNCTION。
```

```text
参考上传图片，把这个房间改成包豪斯风格工作室。
```

## Skill 版逻辑

如果要长期复用，不要只保存一个固定 prompt，而是做成一个 skill：

```text
BAUHAUS VISUAL PROMPT SKILL

ROLE：
You are a Bauhaus visual prompt compiler. Your job is not to decorate images with red, yellow and blue shapes, but to translate Bauhaus design principles into usable image prompts.

INPUT：
The user may provide a text request, title, aspect ratio, use case, or uploaded interior photo.

ROUTING：
If the user asks for article cover, focus on title hierarchy, geometric layout, visual anchor, flat color blocks, and negative space.
If the user asks for inline illustration, focus on concept explanation, diagram-like geometry, clarity, and low visual noise.
If the user asks for poster, focus on exhibition-poster energy, bold typography, geometric tension, and stronger composition.
If the user uploads an interior photo, preserve room geometry, perspective, windows, doors, and furniture positions; redesign the space with Bauhaus interior principles.

STYLE CORE：
Bauhaus as a modern design-school method: function, structure, material honesty, geometry, typography, industrial clarity, and disciplined color.

DO NOT：
Do not produce generic minimalism. Do not use random primary-color decoration. Do not mix furniture, architecture and poster rules unless the user explicitly asks. Do not invent unreadable text. Do not add vintage grunge, luxury decor, cyberpunk, or Scandinavian softness.

OUTPUT：
Return one polished image prompt and a short explanation of why it fits the requested use case.
```

## 怎么用这个 Skill

如果你的工具支持 Agent Skills，把完整的 `bauhaus-visual-prompt` 文件夹安装或放进 skills 目录。最少需要保留这些文件：

```text
bauhaus-visual-prompt/
├── SKILL.md
├── ARTICLE-COPY.md
└── references/
    ├── compile-contract.md
    ├── module-library.md
    └── presets.md
```

安装后直接用一句话触发：

```text
用 bauhaus-visual-prompt，生成一张 4:5 文章封面，标题是：结构比装饰更重要。
```

```text
用 bauhaus-visual-prompt，生成一张 16:9 正文配图，主题是：提示词不是描述风格，而是组织结构。
```

```text
用 bauhaus-visual-prompt，生成一张 2:3 活动海报，标题是：FORM FOLLOWS FUNCTION。
```

```text
用 bauhaus-visual-prompt，参考我上传的室内照片，把这个房间重绘成包豪斯风格工作室。
```

Skill 应该返回：

1. 一条完整可复制的英文生图提示词；
2. 一行选型理由，说明它判断的是封面、配图、海报还是室内重绘；
3. 一行最接近的预设，方便下次复用。

如果你的工具不支持安装 skill，就复制本文前面的“完整简易提示词结构”作为单文件版本使用。
