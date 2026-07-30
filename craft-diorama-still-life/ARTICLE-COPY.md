# 手作拟物静物配图：简易版 + Skill 版

拟物静物风的关键，不是把画面做得多可爱，而是**先找到一个实物替这篇内容说话**。选物错了，材质再好也白搭。

## 完整简易提示词结构（复制即用）

复制下面整段给 AI，再替换 `INPUT` 里的需求。

```text
INPUT：
请根据我给的文章、主题或一句判断，生成手作拟物静物风格配图提示词。例如：
"5:2 封面，文章主题是：慢就是快。"
"这篇文章每一节都要一张 16:9 章节图。"
"帮这段话做一张封面：证据比说服更有力。品牌色 #D64545。"

TASK：
先判断要封面（5:2）还是章节图（16:9）还是两者都要。标题语言从主题本身推断——中文主题就配中文
标题，说明一句让我能翻，不要停下来问。然后为每张图选定物件域和焦点实物，输出完整可直接生图的
提示词。

选物规则：
* 先读这篇内容最强的那句判断，问"什么实物能让这句话被看见"，先定物件域再定具体物件。
* 物件域包括：纸面与桌面 / 导向与结构 / 工具与仪器 / 容器与紧固 / 计时与光 / 克制的自然物，
  以及这些之外任何能让主张可见的实物。
* 物件必须是能叫出名字的现实东西。读者先认物、再解意，抽象几何形披上材质皮不算物。
* 抽象的量（数据、优劣、表现）要落成可读的字和数，或落成物件的物理属性（高低、厚薄、大小）——
  微型条形图和小图标在缩略尺寸下会退化成纹理。
* 同一篇里任意两章不共用焦点实物，也不复用封面用过的。相邻章节尽量跨域。
* 只有内容真的需要屏幕时才用笔记本或手机，它不是默认主角。

调色板（六角色，我没给品牌色就用默认预设）：
* Ground 主背景，画面绝对主色，60-75%：#E1DAC0
* Signal 唯一的主动作/关键标记，整张图只有一处，3-8%：#644FB8
* Support 柔和支撑卡片和面板，10-20%：#BAB2FF
* Accent A 极小点缀，<3%：#B268D8
* Accent B 状态点和时间胶囊，<3%：#504DDC
* Anchor 唯一一个压场深色实物，也可作标题色，5-12%：#1B4038
每个角色都要写清楚落在哪个物件上，只给色值不给落点等于没给。
整张图只有一件物件是 Signal 色——第二个想要它的元素改用 Support。Anchor 只落在一件压场物件加
若干小标签条上，不能铺成大色块。
每个元件的颜色都要在提示词里点名：纸和板一律 Ground 色，除非明确给了别的角色色。不写死，模型
会漂到牛皮纸、土黄或硬纸板棕。
我给了品牌色就映射：最浅最暖的进 Ground，品牌主色进 Signal，最深的进 Anchor，
Signal 的浅调进 Support，剩下的进两个 Accent；凑不齐的角色留空，不要硬凑。

IMAGE STYLE：
Cut-paper / craft-diorama still life, light skeuomorphic, premium editorial feeling — not photography,
not 3D rendering. Tactile material detail: paper grain, felt, matte wood, soft card stock.
Solid colors only, no gradients. Natural soft shadows.
材质完全开放——剪纸、卡纸、绳线、黄铜和其他金属、木、玻璃、石头，物件本来是什么就用什么，
当主角也行。调色板管颜色，不管材质。

ENVIRONMENT：
不搭景：不要地景、地形或舞台（小径、碎石、岩块、植丛、背景布景），一片素净的 Ground 底就够。
但**不搭景不等于少道具**——素底上摆十来件物件依然成立。画面靠两层完成：
* 意义层：主角实物、实物之间的关系、印在它们上面的标注；
* 氛围层：不承担语义、只让台面显得真实的桌面陪衬（台灯、笔、回形针、便签）。
两层都要有，砍掉氛围层画面就干。丰富来自种类多样，不是同一形状复制多份。

RELATIONSHIP：
物件之间的关系必须画出来，不能靠并排摆着暗示。流向、路由、先后、归属，都要一个看得见的连接物
——绳、线、箭头、图钉、连续排布。并置的物件读起来互不相干。

MOTION：
一切静止：不要运动拖影、撞击火花、飞溅、碰撞或摩擦效果、扬尘。**静态的光是可以的**——台灯光晕、
光束、边缘光、发光标记都允许。物件靠位置、成色和光暗示状态，不靠暗示运动。

TEXT：
封面：**大标题和副标题永远成对**，不能只有大标题。大标题用古典衬线（中文明宋体、拉丁配套衬线），
副标题小一号无衬线紧贴其下，同为 Anchor 色，两者都真的生成在画面里，不要留空白区。副标题承担
主张的后半句，不是重复大标题。
副标题下那排小胶囊是产品横幅的手段，只有确实有可量化证明点（响应时长、数量、状态）时才加；
概念科普封面画面已经把事实显示出来了，就不要加。
章节图：只用英文，无大标题。**印在道具上的文字是主要的意义载体，不是点缀**——小胶囊、索引标签、
字段名、状态行、铭牌刻字、手写便签、真实数字都可以用，密度按篇定。
每一串字都过一遍判据：它说的东西物件是不是已经显示了？重复画面已有信息的就删掉。
logo、平台图标、产品字形和 UI 控件都允许，内容需要它们承担信息时就用。

OUTPUT：
每张图返回一条完整可直接复制的英文提示词，写成七段并保留段落标签：
Use case / Scene / Subject / Key details / Composition / Text in image / Constraints。
排除项直接并进 Constraints 段，**不要单独输出成一个负面提示词块**——GPT Image 2 没有 negative
通道，独立成块的约束只会丢失或被当成正面描述画出来。
另附一行选型理由：选了哪个物件域、为什么这个物件替得了这句判断。
```

## 你只需要改 INPUT

```text
5:2 封面，文章主题是：慢就是快。
```

```text
这篇文章每一节都要一张 16:9 章节图，主题是内容资产的复利。
```

```text
帮这段话做一张封面：证据比说服更有力。品牌色 #D64545。
```

## 一条成品长什么样

```text
Use case: editorial article cover, wide 5:2 horizontal banner, headline and subtitle baked into the image.

Scene: a warm cut-paper craft-diorama still life staged on a plain warm ivory #E1DAC0 desk surface,
light skeuomorphic, premium editorial register; no scenery or terrain; a pale paper desk lamp at the
upper right casts warm directional light with a soft glow, throwing short consistent shadows toward
the lower left; everything at rest.

Subject: a hand-cut paper hourglass stands upright on a matte deep moss #1B4038 base right of centre,
its lower chamber already noticeably fuller than the upper one. A thin iris purple #644FB8 cord runs
from the base of the hourglass down to a row of four index cards fanned across the lower centre,
pinned at each card by a small brass tack — the cord shows which cards the accumulated time belongs to.

Key details: all paper and board is warm ivory #E1DAC0 unless named otherwise; no kraft, tan or
cardboard brown anywhere. Exactly one element is iris purple #644FB8 — the cord — and nothing else in
the frame is purple; the four index cards carry lavender mist #BAB2FF header bands, each stamped with
a date. Deep moss appears on the hourglass base, the pen and the headline. Brass on the tacks and the
pen trim. Ambient desk props sit in the lower left carrying no meaning: two brass paperclips and a
deep moss pen lying at an angle. Solid flat colours only, warm ivory dominant, visible paper thickness
and clean cut edges, tactile paper grain, soft warm shadows.

Composition: wide 5:2 horizontal frame, eye-level still-life view slightly above the desk so both
chambers of the hourglass and every card date stay legible; the hourglass and card row occupy the
right two thirds; the left third holds a two-tier text column — headline, then subtitle — in its upper
half, ambient props beneath it; keep the frame comfortably filled, no large dead areas.

Text in image: headline "慢就是快" in a classic serif typeface, Ming/Song-style characters, deep moss
#1B4038, large, upper left. Directly below it the subtitle "复利只奖励留下来的人" in a smaller
sans-serif, same deep moss. The four index cards read "M1", "M6", "Y1" and "Y3" on their header bands
from left to right. Render all text verbatim, no extra words.

Constraints: no people, hands, or faces; no landscape or terrain staging; no gradients; no motion
streaks, impact sparks, splashes, or friction effects; no watermark.
```

## Skill 版逻辑

如果要长期复用，不要只保存一个固定 prompt，而是做成 skill：

```text
CRAFT DIORAMA STILL LIFE SKILL

ROLE：
You are a craft-diorama image prompt compiler. Your job is not to decorate a scene with cute paper
objects, but to find the ONE physical object that makes this specific piece of content's claim visible.

ROUTING：
"封面" / "cover" / "hero" → cover mode, one 5:2 image. Infer the headline language from the topic and
say which you chose; do not stop and wait.
"章节图" / "每节配图" / "chapter images" → chapter mode, one 16:9 per main ## chapter, no headline.
"配图" alone → do both: one cover, then one illustration per chapter.
If the user names a ratio, use theirs.

SELECTION：
Read the strongest claim in the content, then ask what physical object would make it visible.
Pick a domain BEFORE picking an object, and rotate domains across the set. No two chapters share
a focal object, and none reuses the cover's. Every object must be nameable — an abstract shape in a
material costume is not an object. Skipping the domain step is what makes every image collapse into
the same default props.

PALETTE：
Six roles — Ground / Signal / Support / Accent A / Accent B / Anchor. Ground dominant, exactly ONE
element carries Signal, Anchor on one object and never as a large slab. State which object each role
lands on, and pin every element's colour — unstated paper drifts to kraft brown. Materials are open:
paper, cord, metal, wood, glass, stone, at any scale including the hero.

DISCIPLINE：
No scenery — but no scenery is not the same as few props. Build two layers: a meaning layer (hero
object, the relationships between objects, the labels printed on them) and an ambient layer (desk
props carrying no meaning). Draw relationships with a visible connector; objects merely placed side
by side read as unrelated. Everything static — no motion, impact, splash or dust effects; static
light, glow and rim light are fine. Solid colors, no gradients. Logos, platform icons and UI controls
are allowed when they carry the content.

TEXT：
Cover always carries BOTH a serif headline and a smaller sans-serif subtitle — never a headline alone.
Text printed on props is a primary carrier of meaning, not a garnish. Test every string: does it say
something the objects do not already show? Cut the ones that don't.

OUTPUT：
Per image, return one complete copy-ready prompt in seven labelled segments — Use case / Scene /
Subject / Key details / Composition / Text in image / Constraints — with exclusions baked into the
Constraints segment, never as a separate negative-prompt block. Add one line of reasoning (which
domain, why this object).
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
用 craft-diorama-still-life，给这篇文章做一张 5:2 封面。
```

```text
用 craft-diorama-still-life，这篇每一节都配一张 16:9 章节图。
```

```text
用 craft-diorama-still-life，品牌色是 #D64545，帮我做一张封面：证据比说服更有力。
```

Skill 应该返回：

1. 一条完整可复制的英文生图提示词，七段带标签，约束并在正文里；
2. 一行选型理由，说明选了哪个物件域、为什么这个物件替得了这句判断；
3. 一份验收清单。

如果你的工具不支持安装 skill，就复制本文前面的"完整简易提示词结构"作为单文件版本使用。
