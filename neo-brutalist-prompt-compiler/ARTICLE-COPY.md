# 新粗野主义（Neubrutalism）提示词编译器

新粗野主义不是"故意做乱"，是被精确控制的粗糙：粗黑边框、硬偏移阴影、扁平撞色块、超大标题字。边框多粗、阴影多硬、色块怎么撞，都是设计决策。

它有三个方向：文章封面（A）、产品视觉（B）、开发者视觉（C）。**只有方向 A 适合直接 AI 生图**——封面只是海报，不需要真能操作。产品截图和代码卡片一旦被识破是假的，反而毁掉"这个工具很诚实"的第一印象，方向 B/C 优先引用真实案例（Gumroad、RetroUI、Panda CSS），AI 生图只做明确标注的概念示意图。

## 文章封面：复制即用

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

用法核心是第三段 Image logic：把主题转译成**一个**组件感隐喻。自动化 → Toggle 开关；方法论 → 终端输入卡；资产 → 卡片堆；趋势本身 → 断裂网格。一张图一个主隐喻，不做完整 dashboard。

## 成品示例｜AI Agent 自动化，标题「自动」

```text
Create a neo-brutalist article cover poster.

Main visual:
One oversized black-bordered toggle switch, rendered in "on" position, dominating the right two-thirds of the frame.

Style lock:
neo-brutalist digital graphic design, thick black borders, hard offset drop shadow (bottom-right, no blur), flat bold color blocks, oversized bold typography, anti-polished but systematic.

Typography:
One large bold Chinese headline "自动" in black, positioned top-left, sitting on a flat yellow color block. No subtitle.

Layout and background:
Background split into two flat color panels: signal yellow on the left third, off-white on the right two-thirds. The toggle switch sits on the off-white panel with a hard black shadow beneath it.

Color:
Signal yellow, off-white, pure black, one small red accent dot on the toggle's "on" indicator.

Avoid:
glassmorphism, soft shadow, glossy 3D, gradient, realistic hardware photo, cyberpunk neon, extra UI chrome, fake microcopy.
```

更多成品案例（断裂网格「粗野」、终端卡「提示词」、卡片堆「资产」）和产品/开发者方向的完整模板，见 `references/compile-templates.md` 和 `references/examples.md`。

## 出图判断：四条底线

1. 粗边框是结构显形——界面像被搭出来的结构，不是被磨平的皮肤。
2. 硬阴影让组件变成物体——右下偏移、无羽化，按钮和卡片要有重量。
3. 扁平强色比渐变重要——靠边界、撞色、块面和标题层级，不靠光感，主动避开蓝紫渐变 SaaS 默认值。
4. 反精致不等于混乱——画面必须能读出标题、组件和主视觉的关系。

信息层级很多、要讲清楚多步流程的主题，不适合这个风格：它负责建立强记忆点和态度，不负责装下所有信息。
