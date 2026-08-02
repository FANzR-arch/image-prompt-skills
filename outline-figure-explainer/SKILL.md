---
name: outline-figure-explainer
description: 把一个概念、流程或对比编译成「粗黑描边简笔人 + 扁平撞色块」风格的说明插图提示词——纯白底、圆头无五官的黑线小人、无描边的饱和色块、块内白色细线图标、细黑连接线与箭头。用户提到说明插图、概念图、流程图配图、扁平插画、简笔小人插图、白底扁平风、explainer illustration、flat vector diagram，或要给一篇文章配一组解释性插图时使用。可单张也可成组，成组时风格基座逐条重复保证一致。不用于写实摄影、拟物质感、纯字体海报或黑白编辑封面（后者走 mono-editorial-banner）。
---

# Outline Figure Explainer（扁平说明插图编译器）

把**一个概念关系**编译成**一条**可直接交给图像模型的提示词。风格锁死：纯白底上，一个粗黑描边的简笔小人和若干扁平饱和色块，靠细黑线连成一件事。

核心原则：**一张图只讲一个关系。** 这套风格的清晰感来自元素少、留白多、色块纯。堆到七八个色块、给色块加描边、给人物画五官，风格立刻塌成廉价剪贴画。

## 画幅

按发布场景选，不是只有一档：

| 场景 | 比例 | size | 色块上限 |
|---|---|---|---|
| 长文内嵌插图（默认） | 16:9 | `2560×1440` | 5 |
| 分节横幅 / 仓库封面 | 5:2 | `2560×1024` | 3 |
| 小红书 / 方形社媒卡 | 1:1 | `2048×2048` | 3 |
| 竖版信息卡 / Story | 3:4 或 9:16 | `1536×2048` / `1088×1920` | 3 |

quality 统一 `high`。默认用 16:9，用户明确要发小红书、做竖版海报或分节横幅时才换。

画幅越窄或越方，色块越要精简；横向装置（流程 / 漏斗 / 阶梯）塞进竖版前先判断能不能改成自上而下排列，硬压扁成横条会失衡。

## 锁死的风格内核

无论画什么内容，下面三段逐字进每一条提示词，不改写不精简。**成组产出时每一条都要重复**——模型只看得见单条，共享规则不会自动继承。

**Scene 基座**
```
pure flat white background, no environment, no horizon, no gradient; a thin black horizontal ground line only where figures stand.
```

**Key details 基座**
```
flat vector illustration; all figures drawn with thick uniform black outlines, round heads, no facial features, and left completely unfilled white inside; all blocks are flat saturated solid colour with absolutely no gradient, no shading and no texture; icons inside the blocks are simple thin white line drawings; one soft pale grey ellipse shadow directly under each standing figure and nothing else casts shadow; generous empty white space between elements; mood: clean, friendly, instructional, modern explainer.
```

**Constraints 基座**
```
no gradients, no drop shadows other than the pale grey ellipses under standing figures, no outlines on the colour blocks, no facial features on any figure, no additional text, labels, logos or watermarks, no photographic elements, no 3D rendering, no background colour of any kind.
```

## 色板（可整体替换的子模块）

默认六色，写进 Key details 的 palette 从句：

```
drawn from the palette deep blue, orange, green, purple, yellow and pink
```

换色板是最省力的变体来源——换掉这一句，其余风格基因不动，整组图立刻换一套气质。一张图里同时出现的颜色**不超过四种**，超过就花。

## 装置词汇表（把关系转成画面）

先说清这句话讲的是什么**关系**，关系决定装置。装置必须能一眼读出，读不出就换。下表是常用起点，**不是穷举**——表里没有的关系不要硬套最接近的一条，直接按后面的判据自己设计。

| 讲的关系 | 装置 |
|---|---|
| 从 A 到 B / 派驻 / 迁移 | 左右两个色块 + 中间一条带箭头的细线 + 线上飘散的小方块，人物在其中一端 |
| 理想 vs 现实 / 演示 vs 落地 | 左边整齐排列的色块，中间一堵高色块墙，右边一团角度杂乱互相重叠的小方块 |
| 一进多出 / 产出有两份 | 一条线进入中心物件，两条等权重的线分岔而出，各指向一个色块 |
| 流程 / 阶段 / 链条 | 等高色块横排成一行，人物走在上面，一步跨在两块之间 |
| 分类 / 清单 / 构成 | 一个大对话气泡或大圆，内部横向分格，每格一个图标加一个标签 |
| 系统 / 网络 / 多方协同 | 中心一个白色主干结构，四周放射出多个色块节点，细线连回中心 |
| 层级 / 分层 / 由浅入深 | 色块自下而上堆叠成塔，每层比上一层宽 |
| 筛选 / 收窄 / 淘汰 | 上宽下窄的漏斗，上方大量小方块，下方只落出一两个 |
| 循环 / 迭代 | 四个色块沿一个大圆环排列，箭头首尾相接，人物站在环心 |
| 对照 / 两条路 | 从同一点分出的两条线，一条平直通向色块，一条曲折并中途断开 |
| 协作 / 谈判 / 师徒 / 博弈 | 不用色块当主角，让 2-3 个简笔人物直接面对面或并排站，姿态、朝向和之间的手势/道具表达关系，人物本身就是节点 |

选装置（无论选表内还是自己设计）的三条判据：**一眼能读出关系**、**色块不超过四种颜色**、**人物数量服务于关系本身**——关系是人与物 / 人与系统，用 1-2 人 + 色块的默认配置；关系本身就是人与人（协作、博弈、师徒、谈判），可以让 2-4 个简笔人物直接充当装置主体，不必强行给每个人配一个色块。三条缺一就换装置。

## Input

从用户输入推断，不要求填表：

1. **要讲的关系**：一句判断或一个概念。查装置词汇表。
2. **标签文字**：色块下方的小字。**中英文都可以直接写**，中文按原样渲染，不要因为怕出错就改成英文或改成留白后期加。
3. **张数**：单张还是成组。成组时先列清每张讲哪一段，避免两张讲同一件事。

## Workflow

1. **定画幅**：按发布场景查画幅表，没说明就用 16:9 默认；
2. **读关系** → 查装置词汇表选装置，表里没有就按三条判据自己设计；
3. **定人物位置与数量**：人与物/人与系统关系，1-2 人是读者的代入点，放在他应该站的位置（观察者放旁边、执行者放中间、跨越者放上方）；人与人关系，2-4 个人物本身就是装置，姿态和朝向要能读出角色差异；
4. **定色块数量与颜色**（若装置需要色块）：三到五块，不超过四色；
5. **写标签**：每个色块最多一个标签，短语不成句；
6. **按七槽编译**：Use case → Scene → Subject → Key details → Composition → Text in image → Constraints，三段基座逐字照抄；
7. **输出**：一条完整提示词 +（可选）一句装置选型理由。用户只要 prompt 时省略解释。

七槽的通用写法规则见 `gpt-image-prompt-spec`，本 skill 只管这套风格的内容。

## Quality Gates

- **色块无描边**：色块是纯色形状，只有人物有黑轮廓。给色块描黑边是这套风格最常见的塌方点。
- **人物内部留白**：黑线勾出轮廓，内部保持白色不填色，也不画五官。
- **阴影只有一种**：站立人物脚下一个浅灰椭圆，别的一律没有。色块不投影。
- **留白 ≥40%**：元素集中在中间带，上下留净空。
- **一张一关系**：出现两个平权的中心结构就是超载，拆成两张。
- **标签只标必要项**：能靠画面读懂的不加字。标签写全、写准，加 `render all text verbatim, no extra words`。
- 本 skill 只产出提示词，不编造已生成的图片结果。

## Read

- 成品参考、已验证提示词、成组案例：`references/examples.md`
