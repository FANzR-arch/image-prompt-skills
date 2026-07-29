# 手作拟物静物配图：简易版 + Skill 版

拟物静物风的关键，不是把画面做得多可爱，而是**先找到一个实物替这篇内容说话**。选物错了，材质再好也白搭。

## 完整简易提示词结构（复制即用）

复制下面整段给 AI，再替换 `INPUT` 里的需求。

```text
INPUT：
请根据我给的文章、主题或一句判断，生成手作拟物静物风格配图提示词。例如：
"5:2 封面，文章主题是：慢就是快。标题用中文。"
"这篇文章每一节都要一张 16:9 章节图。"
"帮这段话做一张封面：证据比说服更有力。品牌色 #C2542F。"

TASK：
先判断要封面（5:2）还是章节图（16:9）还是两者都要。封面模式必须先问一句标题用中文还是英文，
等我回答再写。然后为每张图选定物件域和焦点实物，输出完整可直接生图的提示词。

选物规则：
* 先读这篇内容最强的那句判断，问"什么实物能让这句话被看见"，先定物件域再定具体物件。
* 物件域包括：纸面与桌面 / 导向与结构 / 工具与仪器 / 容器与紧固 / 计时与光 / 克制的自然物，
  以及这些之外任何能让主张可见的实物。
* 同一篇里任意两章不共用焦点实物，也不复用封面用过的。相邻章节尽量跨域。
* 配角实物 3-6 个，先从文中的具体数字、时间、来源、渠道来，不要全从焦点实物同一个域拿。
* 只有内容真的需要屏幕时才用笔记本或手机，它不是默认主角。

调色板（六角色，我没给品牌色就用默认预设）：
* Ground 主背景，画面绝对主色，60-75%：#EAE3D2
* Signal 唯一的主动作/关键标记，整张图只有一处，3-8%：#C2542F
* Support 柔和支撑卡片和面板，10-20%：#D9CFBA
* Accent A 极小点缀，<3%：#7A8B6F
* Accent B 状态点和时间胶囊，<3%：#2E4A6B
* Anchor 唯一一个压场深色实物，也可作标题色，5-12%：#26332C
每个角色都要写清楚落在哪个物件上，只给色值不给落点等于没给。
我给了品牌色就映射：最浅最暖的进 Ground，品牌主色进 Signal，最深的进 Anchor，
Signal 的浅调进 Support，剩下的进两个 Accent；凑不齐的角色留空，不要硬凑。

IMAGE STYLE：
Cut-paper / craft-diorama still life, light skeuomorphic, premium editorial feeling — not photography,
not 3D rendering. Tactile material detail: paper grain, felt, matte wood, soft card stock.
Solid colors only, no gradients. Natural soft shadows.

ENVIRONMENT：
Restrained. The focal object plus 3-6 small supporting props is the entire scene. Do NOT build out
a landscape, terrain or staged environment around it — no paths, gravel, rock clusters, foliage or
backdrop scenery. A plain or very lightly textured ground is enough.

MOTION：
Everything static. This is a still-life object study, not an action scene. No motion streaks, impact
sparks, glow bursts, light rays, collision effects or dust. Objects imply state through position and
finish only.

TEXT：
封面：标题和副标题按我确认的语言真的生成在画面里，不要留空白区。小装饰标签可以保持英文。
章节图：只有稀疏英文小标签——时间戳 4:12、数字 300+ / 24h、时间轴 T+24h、短标签 Ready / Context。
无大标题、无中文、无长段落、无密集 UI 文案、无伪造表格。

AVOID：
Brand logo, watermark, people, faces, hands, oversized laptop or smartphone, dense dashboard,
full table, cluttered desk, too many unrelated objects, elaborate landscape staging, dark cyberpunk,
neon glow, gradients, motion streaks, impact sparks, glow bursts, black background, stock photo,
mascot, excessive 3D, messy typography, long paragraphs.

OUTPUT：
每张图返回一条完整可直接复制的英文提示词 + 一行选型理由（选了哪个物件域、为什么这个物件替这句判断）
+ 一条负面提示词。
```

## 你只需要改 INPUT

```text
5:2 封面，文章主题是：慢就是快。标题用中文。
```

```text
这篇文章每一节都要一张 16:9 章节图，主题是内容资产的复利。
```

```text
帮这段话做一张封面：证据比说服更有力。品牌色 #3F5BD9。
```

## 一条成品长什么样

```text
Horizontal 5:2 image, GPT Image 2. Cut-paper / craft-diorama still life, light skeuomorphic,
premium editorial feeling, not photography.

Metaphor: patience compounds — the slow route is the one that actually arrives.

Focal object: a hand-cut paper hourglass standing upright on a matte wood base, the lower chamber
already noticeably fuller than the upper one.

Supporting details: three small index cards fanned behind it, each with a tiny date stamp; a folded
paper route marker leaning against the base; a small brass-toned clasp holding two cards together;
one tipped-over card lying flat in front.

Palette: warm paper ground #EAE3D2 dominant; the single terracotta #C2542F marker on the upright
route flag as the only activated signal; oat #D9CFBA supporting cards; one deep pine #26332C wooden
base as the sole grounding anchor; tiny sage #7A8B6F dot on the folded marker and a slate blue
#2E4A6B time chip reading "T+24h" on the front card. Solid colors only, no gradients.

Text: Chinese headline "慢就是快" set in a clean serif at upper left, subtitle "复利只奖励留下来的人"
one line below in a smaller weight, both in deep pine #26332C, actually rendered in the image.

Guardrails: no non-Chinese headline text, no logo, no watermark, no gradients, no landscape or
terrain staging, no motion streaks or glow effects, static still life only.
```

## Skill 版逻辑

如果要长期复用，不要只保存一个固定 prompt，而是做成 skill：

```text
CRAFT DIORAMA STILL LIFE SKILL

ROLE：
You are a craft-diorama image prompt compiler. Your job is not to decorate a scene with cute paper
objects, but to find the ONE physical object that makes this specific piece of content's claim visible.

ROUTING：
"封面" / "cover" / "hero" → cover mode, one 5:2 image. Ask Chinese or English headline first, wait.
"章节图" / "每节配图" / "chapter images" → chapter mode, one 16:9 per main ## chapter, no headline.
"配图" alone → do both: one cover, then one illustration per chapter.
If the user names a ratio, use theirs.

SELECTION：
Read the strongest claim in the content, then ask what physical object would make it visible.
Pick a domain BEFORE picking an object, and rotate domains across the set. No two chapters share
a focal object, and none reuses the cover's. Skipping the domain step is what makes every image
collapse into the same default props.

PALETTE：
Six roles — Ground / Signal / Support / Accent A / Accent B / Anchor. Ground dominant, exactly one
Signal focal point, Anchor on exactly one object. State which object each role lands on.

DISCIPLINE：
Restrained environment — focal object plus 3-6 props, no landscape staging. Everything static —
no motion, impact, glow or dust effects. Solid colors, no gradients. No logo.

OUTPUT：
Per image, return one complete copy-ready prompt, one line of reasoning (which domain, why this
object), and a negative prompt.
```

## 怎么用这个 Skill

如果你的工具支持 Agent Skills，把完整的 `craft-diorama-still-life` 文件夹安装或放进 skills 目录。最少需要保留这些文件：

```text
craft-diorama-still-life/
├── SKILL.md
├── ARTICLE-COPY.md
└── references/
    ├── palette-contract.md
    └── object-domains.md
```

安装后直接用一句话触发：

```text
用 craft-diorama-still-life，给这篇文章做一张 5:2 封面，标题用中文。
```

```text
用 craft-diorama-still-life，这篇每一节都配一张 16:9 章节图。
```

```text
用 craft-diorama-still-life，品牌色是 #3F5BD9，帮我做一张封面：证据比说服更有力。
```

Skill 应该返回：

1. 一条完整可复制的英文生图提示词；
2. 一行选型理由，说明选了哪个物件域、为什么这个物件替得了这句判断；
3. 一条负面提示词和验收清单。

如果你的工具不支持安装 skill，就复制本文前面的"完整简易提示词结构"作为单文件版本使用。
