# Compile Templates — 三方向模板与段落规则

最终提示词必须是已决策成品：锁风格、锁标题、锁主隐喻、锁负面约束。构图和配色可以在模板边界内留给图像模型判断，但不要输出斜杠菜单和未决定选项。

## 风格锁（所有方向必含）

```text
neo-brutalist digital graphic design, thick black borders, hard offset drop shadow (bottom-right, no blur), flat bold color blocks, oversized bold typography, deliberately rough but systematic
```

## 通用负面（所有方向必含，按方向增删）

```text
Avoid: glassmorphism, soft shadow, glossy 3D, gradient, blue-purple gradient SaaS look, cinematic lighting, realistic scene, stock-photo style, fake microcopy, unreadable fake labels.
```

## 方向 A｜文章封面 / 观点封面

最适合 AI 生图的方向：封面只是海报，不需要真能操作。

```text
文章主题或摘要：
{输入文章标题、摘要，或直接粘贴文章内容}

用途和比例：
{例如：文章封面，横版 5:2}

指定主标题文字：
{可选；没有就写：自动判断}

特殊要求：
{指定颜色、图形隐喻，或不能出现的元素；没有就写：无}

Create a neo-brutalist article cover.

Style lock:
neo-brutalist digital graphic design, thick black borders, hard drop shadows, flat bold color blocks, oversized typography, one abstract UI-like icon or interface fragment as visual metaphor.

Image logic:
Translate the article theme into one bold title plus one abstract graphic or interface-like metaphor (a button, a toggle, a broken grid fragment, a card shape). Do not build a full dashboard or complex scene — keep it poster-like.

Typography:
One large bold Chinese headline. Add at most one small subtitle line. Do not create fake UI labels.

Color and layout:
High-contrast flat color block background, hard edges, asymmetric or centered composition, deliberate not messy.

Avoid:
glassmorphism, soft gradient SaaS look, glossy 3D, realistic scene, full complex dashboard, stock-photo style.
```

编译成品时，把占位字段解析成具体决策：写明主隐喻是什么组件、标题是哪几个字、背景用哪几个扁平色。

## 方向 B｜产品 / 工具视觉（概念示意图）

默认先建议引用真实案例；用户确认要生成时才用此模板，输出必须当"概念图"标注。

```text
产品或主题说明：
{输入产品名、功能介绍，或文章主题}

用途：
{例如：官网首屏 / Dashboard 概念图 / Pricing 页}

画幅：
{例如：横版 5:2 / 16:9}

特殊要求：
{指定颜色、组件、不能出现的元素；没有就写：无}

Create a neo-brutalist product/tool visual.

Style lock:
neo-brutalist digital graphic design, thick black borders, hard drop shadows, flat bold color blocks, oversized typography, visible grid, bold rectangular buttons, modular cards, direct UI-like composition.

Image logic:
Turn the product/theme into a product page, tool interface, dashboard fragment, or pricing block. Use input fields, buttons, toggles, tabs, status labels, or pricing cards when relevant to the stated use. Keep the structure clear and intentionally rough but readable.

Typography:
Large bold title. Short Chinese headline if needed. Add at most one small subtitle line if it helps explain the value. Do not create fake UI labels or unreadable microcopy.

Color and layout:
Bright flat colors, off-white, black, signal yellow, red, blue, green, or other high-contrast colors. Hard edges, flat blocks, asymmetric or broken-grid layout allowed if it stays deliberate.

Avoid:
glassmorphism, soft shadows, glossy 3D, Apple-style clean UI, blue-purple gradient SaaS look, cinematic lighting, realistic office scene, generic laptop mockup, stock-photo style.
```

## 方向 C｜开发者 / 开源项目视觉（概念示意图）

同 B：真实项目截图优先；生成时绝不渲染可读真代码。

```text
项目或教程说明：
{输入开源项目名、API 名称，或技术教程主题}

用途：
{例如：GitHub 封面 / 文档封面 / 技术教程配图}

画幅：
{例如：横版 5:2 / 16:9}

特殊要求：
{指定颜色、需要保留的品牌标识，或不能出现的元素；没有就写：无}

Create a neo-brutalist developer-facing visual.

Style lock:
neo-brutalist digital graphic design, thick black borders, hard drop shadows, flat bold color blocks, oversized typography, terminal window, code-card motif, API/status tag blocks.

Image logic:
Use a terminal window, code-card shape, module tags, or status labels as the dominant visual motif. Do not render real, readable code — use abstracted blocky text lines instead. Keep it feeling like a tool, not a screenshot.

Typography:
Large bold title, monospace-flavored accents allowed for tags/labels only. Add at most one small subtitle line.

Color and layout:
High-contrast flat colors, dark terminal background or off-white/black base allowed. Hard edges, visible grid, modular card layout.

Avoid:
glassmorphism, soft gradient SaaS look, realistic IDE screenshot, readable real code, glossy 3D, cyberpunk neon, stock-photo style.
```

## 出图判断（编译前过一遍）

1. 粗边框是结构显形——界面像被搭出来的结构，不是被磨平的皮肤。
2. 硬阴影让组件变成物体——右下偏移、无羽化，按钮和卡片要有重量。
3. 扁平强色比渐变重要——靠边界、撞色、块面和标题层级，不靠光感。
4. 反精致不等于混乱——画面必须能读出标题、组件和主视觉的关系。

信息层级很多、要讲清楚多步流程的主题，不适合新粗野主义；它负责建立强记忆点和态度，不负责装下所有信息。遇到这种输入直接建议换方向或换风格。
