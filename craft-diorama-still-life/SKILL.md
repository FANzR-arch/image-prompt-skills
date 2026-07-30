---
name: craft-diorama-still-life
description: 把文章、观点或产品主张编译成「一个实物替一句判断」的手作拟物静物提示词——剪纸质感、微缩场景、轻拟物、克制静物摄影感。用户提到拟物风封面、拟物风章节图、剪纸质感、微缩静物、实物隐喻配图、craft diorama、cut-paper still life、object metaphor cover、diorama illustration，或要为一篇内容做封面加逐章配图时使用。默认输出封面 5:2、章节图 16:9 的完整可直接生图提示词；调色板由用户自填或按内置预设映射。不用于摄影写实、3D 渲染或人物场景插画。
---

# Craft Diorama Still Life

把内容编译成温暖、有触感的实物隐喻静物图：剪纸／手作微缩质感，**一个实物替一句判断**。

本 skill 同时覆盖文章封面（5:2）和章节／小节配图（16:9）。判断用户要哪一种，或两种都做。

## 意图判断

只在真的分不清时才问，否则直接从请求推断：

- 「封面」/「cover」/「主图」/「hero image」→ **封面模式**，一张 5:2。
- 「章节图」/「每节配图」/「chapter images」/ 给了文章路径并说「每一节」→ **章节模式**，每个主 `##` 章节一张 16:9。
- 只说「配图」，或「封面和章节都要」→ 两种都做：先一张封面，再逐章一张。

用户明确指定了画幅（4:5、1:1、16:9 封面等）就用用户的，不要强推默认值。

## 语言确认（仅封面模式）

从文章或主题本身推断标题语言——中文标题就配中文标题和副标题。用一句话说明选了哪种，让用户能翻，**不要停下来等回答**；只有源头真的没给出任何语言信号时才问。印在道具上的字串一律英文。章节图永远不带大标题。

## 调色板

调色板是**角色制**的，不绑定任何具体品牌。六个角色：

| 角色 | 作用 |
| --- | --- |
| Ground | 主背景／主承载面，画面绝对主色 |
| Signal | 唯一的主动作、关键标记、被点亮的那个状态 |
| Support | 柔和的支撑卡片、面板、浅色表面 |
| Accent A | 极小面积的提醒／社群点缀 |
| Accent B | 状态点、时间胶囊、进度条 |
| Anchor | 唯一一个压场的深色实物、结构锚点，也可作标题色 |

用色纪律：Ground 绝对主导；**整张图里只有一个实物是 Signal 色**——第二个想要它的元素改用 Support；Anchor 只落在一个压场实物加若干小标签条上，绝不铺成大色块；Accent A / B 只做小面积点缀；不额外引入霓虹、赛博朋克配色。

**材质完全开放**——剪纸和卡纸、绳线、黄铜和其他金属、木、玻璃、石头，物件本来是什么就用什么，多大都行，当主角也行。调色板管的是颜色，不管材质。

**每个元件的颜色都要在提示词里点名**：纸和板一律 Ground 色，除非明确给了别的角色色。不写死，模型会漂到牛皮纸、土黄或硬纸板棕——脱离色板且显脏。

用户给了品牌色就映射到这六个角色；没给就用 `references/palette-contract.md` 里的预设，映射规则和预设都在那份文件里。

## 输入读取

给了本地文章路径就先读全文（终端可能吞中文时显式按 UTF-8 读）。抽出：标题、核心论点、最强的那处张力、承诺、逐章的隐喻（章节模式），以及任何能当小细节用的具体信号、数字、时间戳和短标签。

没给路径就用聊天里给的正文或主题。

## 产出约定

给了本地文章路径或用户要文件时，写一个独立 Markdown 文件；否则直接在回复里用同样结构。

封面文件名：`[文章名]-diorama-cover-prompt.md`
章节文件名：`[文章名]-diorama-illustration-prompts.md`
默认存在源文章旁边，除非另有指定。

封面文件结构：

```markdown
# Diorama Cover: [文章标题]

## Source
## Cover Strategy
[选定的物件域、隐喻、焦点实物、标题语言、调色板映射]
## Cover Prompt
[一条完整可直接复制的提示词，标题文字直接写进去]
## Cover Copy Fallback
[只有反复生成都糊字时才需要：留白构图说明 + 后期合成用的准确标题副标题]
## Acceptance Checklist
```

章节文件结构：

```markdown
# Diorama Illustrations: [文章标题]

## Chapter Prompt Map
| 章节 | 物件域 | 焦点实物 |
## Chapter 1 Prompt
## Chapter 2 Prompt
...
## Acceptance Checklist
```

只要聊天输出时，保持同样的结构。

## 固定规则

- 封面 5:2 横版，章节图 16:9 横版。目标模型是 GPT Image 2，但**模型名不进提示词正文**，只留在文档层。
- 风格：剪纸／手作微缩静物，轻拟物，高级编辑设计感——不是摄影
- 背景：Ground 色
- 封面文字：**大标题和副标题永远成对**，不能只有大标题。大标题用古典衬线（中文明宋体、拉丁文配套衬线）；副标题小一号无衬线，紧贴其下，同为 Anchor 色。两者都烧进画面。印在道具上的字串保持英文。章节图只有英文，无大标题。
- logo、平台图标、产品字形和 UI 控件全部允许——内容需要它们承担信息时就用。
- 纯色，无渐变
- 自然柔和的投影，材质要有真实触感。台灯光、方向光、边缘光和发光都允许。

## 选物

先从这篇内容自己的隐喻里长出焦点实物和配角实物。**不要每次都伸手去拿同一批道具**——讲速度的和讲信任、记忆、证据、规模的，不该落到同一个物件上。

章节模式里，同一篇文章里任意两章不共用焦点实物，也不复用封面已经用过的。封面模式里，避开这个项目最近 2-3 张封面用过的物件。

先定物件域再定具体物件，并且轮换物件域——别让一个项目里的所有图、或一篇文章里的所有章节，都沉到同一个域里。完整域库和轮换规则见 `references/object-domains.md`。

**物件必须是能叫出名字的现实东西**。读者先认物、再解意；抽象几何形披上材质皮不算物，认不出来后面全断。同理，抽象的量（数据、表现、优劣）要落成**可读的字和数**，或者落成物件本身的物理属性（高低、厚薄、大小）——微型条形图和小图标在缩略尺寸下会退化成纹理。

只有内容真的需要屏幕时才用笔记本或手机，它不是默认主角。

## 场景与特效纪律

不搭景。**不要**搭出地景、地形或舞台（小径、碎石、岩块、植丛、背景布景）。一片素净或极轻微纹理的 Ground 底就够了。

**不搭景不等于少道具。** 道具密度是另一件事——一片素底上摆十来件物件，依然是这个风格。画面靠两层完成：**意义层**（主角实物、实物之间的关系、印在它们上面的标注）和**氛围层**（不承担任何语义、只让台面显得真实的桌面陪衬——台灯、笔、回形针、便签）。两层都要有；把氛围层砍光，画面就干。

**丰富来自种类多样，不是同一形状复制多份**——同一个形状重复排列读作纹理，不是场景。主角实物要有内部层次，一堆尺寸相近的平权物件读起来是图案不是画面。

**关系必须画出来，不能靠并置暗示**——流向、路由、先后、归属，都需要一个看得见的连接物（绳、线、箭头、图钉、连续排布）。并排摆着的物件读起来互不相干。

一切保持静止：不要运动拖影、不要撞击火花、不要飞溅、不要碰撞或摩擦效果、不要扬尘。**静态的光是可以的**——台灯光晕、光束、边缘光、发光标记都允许。物件靠位置、成色和光暗示状态，绝不靠暗示运动。

## 文字规则

**封面**：大标题和副标题都写进提示词，并且**真的生成在画面里**——不能只有大标题，也不要默认留一块空白区。副标题承担主张的后半句，不是重复大标题：大标题点出事情或抛出问题，副标题落地那句判断（`小模型什么时候就够用` / `匹配任务，不是越大越好`）。中文标题就把准确中文写进提示词，生成后检查有没有糊字，先重生成；只有反复重生成都糊才退回留白构图＋后期合成。

副标题下面那排小胶囊是**产品横幅的手段**——只有确实有可量化的证明点（响应时长、数量、状态）时才用。概念科普封面里画面已经把事实显示出来了，就不要加。真要加，无论标题什么语言都保持英文。

**章节**：只用英文，无大标题、无中文。**印在道具上的文字是主要的意义载体，不是点缀**——小胶囊（`4:12`、`300+`、`T+24h`、`Ready`）、索引标签、字段名、状态行、铭牌刻字、手写便签、真实数字都可以用。密度按篇定：文字是用来让关系和数据变得可读的，不是用来填空的。

**画面里每一串字都要过一遍这个判据**：它说的东西，物件是不是已经显示出来了？点出角色、状态、类别或真实数字的标签站得住；重复画面已经说清楚的事的胶囊就是冗余，删掉。

## 提示词书写顺序

每条提示词写成七段，带段落标签，按此顺序。模型名不出现在正文里。

1. **Use case**：这是什么交付物（封面／章节图）和画幅
2. **Scene**：Ground 底、剪纸微缩语域、光的方向
3. **Subject**：主角实物，以及把它和其余部分连起来的那个关系
4. **Key details**：调色角色落点、配角道具、氛围层、材质与投影
5. **Composition**：位置、文字栏、留白、取景
6. **Text in image**：加引号的准确字串 + 字体规格 + 位置，末尾加 `render all text verbatim, no extra words`
7. **Constraints**：排除项，直接并进正文

每条提示词都要完整、可直接复制——不要把关键约束拆成含糊的备注让用户自己拼。

## 封面骨架（已实测）

多张封面按这个形状一次跑通。固定块逐字复用，方括号按篇填。

```text
Use case: editorial article cover, wide 5:2 horizontal banner, headline and subtitle baked into the image.

Scene: a warm cut-paper craft-diorama still life staged on a plain [Ground 色] desk surface, light skeuomorphic, premium editorial register; no scenery or terrain; [光源与方向] casting short consistent shadows [投向反侧]; everything at rest.

Subject: [主角实物、它的状态，以及把它与其余部分连起来的可见连接物].

Key details: [每件物件是什么材质、承载什么]. [配色块：把纸钉死在 Ground 色，点名唯一那件 Signal 色物件并声明画面里没有别的东西是这个色，安排 Anchor 与 Support 的落点]. Ambient desk props sit in the lower left carrying no meaning: [从 — 回形针、斜放的 Anchor 色笔、带手写记号的 Support 色便签 — 里挑两三件]. Solid flat colours only, [Ground 色] dominant, visible material thickness and clean cut edges, tactile grain, soft shadows.

Composition: wide 5:2 horizontal frame, eye-level still-life view slightly above the desk so [什么必须保持可读]; [主角在右侧三分之二的位置安排]; the left third holds a two-tier text column — headline, then subtitle — in its upper half, ambient props beneath it; keep the frame comfortably filled, no large dead areas.

Text in image: headline "[大标题]" in a classic serif typeface, Ming/Song-style characters[ and a matching serif for the Latin words], [Anchor 色], large, upper left, two lines allowed. Directly below it the subtitle "[副标题]" in a smaller sans-serif, same [Anchor 色]. [每一串印在道具上的字，逐一写出并指明落在哪件物件上]. Render all text verbatim, no extra words.

Constraints: no people, hands, or faces; no landscape or terrain staging; no gradients; no motion streaks, impact sparks, splashes, or friction effects; no watermark.
```

## 默认约束

并进每条提示词的 Constraints 段，**绝不单独输出成一个负面提示词块**——GPT Image 2 没有 negative 通道，独立成块的约束只会丢失或被当成正面描述画出来：

```text
no people, hands, or faces; no landscape or terrain staging; no gradients; no motion streaks, impact sparks, splashes, or friction effects; no watermark
```

## 验收清单

收工前逐条核对：

- 封面写明 `5:2 horizontal`，章节图写明 `16:9`（或用户指定的画幅）；模型名不在正文里
- 七段带标签、顺序正确；约束并进正文，不是单独一块
- 封面：大标题**和**副标题都在，衬线大标题 + 其下小一号无衬线副标题，绝不只有大标题
- 章节：只有英文，无大标题；每一串印在道具上的字都逐字写明，并带 `render all text verbatim, no extra words`
- 纸的颜色钉死在 Ground 色；整张图只有一件物件是 Signal 色；Anchor 没有铺成大色块
- 画面里每一串字都说了物件没说的事；没有重复画面已有信息的胶囊
- 物件之间的关系用可见连接物画出来了，不是留给读者猜
- 意义层和氛围层都在
- 1-2 个焦点实物，来自贴合内容的物件域，章节之间和与封面之间都不重复
- 没有地景搭建；画面静止——光和发光可以，运动不行
- 六个调色角色都写明了落在哪
