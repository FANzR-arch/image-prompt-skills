# Image Prompt Skills

一组给 AI Agent 使用的视觉生成 Skills。可以把文章、主题、城市、产品或现有视觉资产，编译成可直接生图的完整提示词。

每个 Skill 都同时提供：

- `SKILL.md`：适合 Codex、Claude Code 等支持 Agent Skills 的工具。
- `ARTICLE-COPY.md`：单文件复制版，适合直接粘贴给 AI。

## 安装

把下面这段话发给支持 Skills 的 AI Agent：

```text
请安装这个仓库里的全部 Skills：
https://github.com/FANzR-arch/image-prompt-skills
```

也可以只安装一个 Skill：

```text
请安装这个 Skill：
https://github.com/FANzR-arch/image-prompt-skills/tree/main/acid-depth-poster
```

## 可用 Skills

### 从主题出发

给一个主题、标题、城市或照片，编译成对应风格的提示词。

| 视觉方向 | Skill ID | 适合内容 |
| --- | --- | --- |
| 现代旅行拼贴明信片 | [`travel-postcard-agent`](travel-postcard-agent/) | 城市、节日、季节、旅行纪念和地点文化 |
| 瑞士国际主义海报 | [`swiss-typographic-poster`](swiss-typographic-poster/) | 字体主导、网格排版、编辑设计和理性视觉 |
| 包豪斯视觉生成 | [`bauhaus-visual-prompt`](bauhaus-visual-prompt/) | 文章封面、正文配图、海报和室内照片重绘 |
| Plakatstil 商品海报 | [`plakatstil-prompt-compiler`](plakatstil-prompt-compiler/) | 商品、包装、服务、品牌物体和德国广告海报 |
| 新粗野主义视觉 | [`neo-brutalist-prompt-compiler`](neo-brutalist-prompt-compiler/) | AI、产品、技术项目、教程和强组件感封面 |
| 前进色 × 后退色实验海报 | [`acid-depth-poster`](acid-depth-poster/) | Y2K、Acid Graphics、夜间城市、青年文化和地下传单 |
| 安静纸面标本 | [`quiet-paper-specimen`](quiet-paper-specimen/) | 随笔、情绪、记忆向主题，单物件加大留白加中文手写标题的安静封面 |
| 工程蓝图 / 赛博终端示意图 | [`tech-schematic-poster`](tech-schematic-poster/) | AI 概念、Agent 工作流、技术项目的节点拓扑封面和插图 |
| 手作拟物静物 | [`craft-diorama-still-life`](craft-diorama-still-life/) | 用一个实物替一句判断的文章封面和逐章配图 |
| 颗粒棱面风格 | [`grainy-plane-style`](grainy-plane-style/) | 照片改插画风、平涂大色块加细密颗粒的肖像和器物图 |
| 暖纸拟物流程主视觉 | [`paper-workflow-hero`](paper-workflow-hero/) | 产品与服务工作流的官网 hero、营销主图和带真人质感的流程叙事 |
| 黑白编辑横幅 | [`mono-editorial-banner`](mono-editorial-banner/) | 观点长文、判断句和思想类内容的极简黑白超宽封面，中英文标题 |

### 从已有的视觉资产出发

手上已经有 Logo、头像、角色或产品图，围绕它做成套延展。风格由这张图决定，不预设。

| 用途 | Skill ID | 输入 |
| --- | --- | --- |
| 视觉身份延展 | [`visual-identity-expander`](visual-identity-expander/) | Logo、人物头像、个人形象、IP 角色、插画、产品照片或标志性物件 |

## 风格样例

| | | |
|:---:|:---:|:---:|
| [![现代旅行拼贴明信片](travel-postcard-agent/assets/preview.png)](travel-postcard-agent/) | [![瑞士国际主义海报](swiss-typographic-poster/assets/preview.png)](swiss-typographic-poster/) | [![包豪斯视觉生成](bauhaus-visual-prompt/assets/preview.png)](bauhaus-visual-prompt/) |
| 现代旅行拼贴明信片 | 瑞士国际主义海报 | 包豪斯视觉生成 |
| [![Plakatstil 商品海报](plakatstil-prompt-compiler/assets/preview.png)](plakatstil-prompt-compiler/) | [![新粗野主义视觉](neo-brutalist-prompt-compiler/assets/preview.png)](neo-brutalist-prompt-compiler/) | [![前进色 × 后退色实验海报](acid-depth-poster/assets/preview.png)](acid-depth-poster/) |
| Plakatstil 商品海报 | 新粗野主义视觉 | 前进色 × 后退色实验海报 |
| [![手作拟物静物](craft-diorama-still-life/assets/preview.png)](craft-diorama-still-life/) | [![工程蓝图 / 赛博终端示意图](tech-schematic-poster/assets/preview.png)](tech-schematic-poster/) | [![颗粒棱面风格](grainy-plane-style/assets/preview.png)](grainy-plane-style/) |
| 手作拟物静物 | 工程蓝图 / 赛博终端示意图 | 颗粒棱面风格 |
| [![安静纸面标本](quiet-paper-specimen/assets/preview.png)](quiet-paper-specimen/) | [![暖纸拟物流程主视觉](paper-workflow-hero/assets/preview.png)](paper-workflow-hero/) | [![黑白编辑横幅](mono-editorial-banner/assets/preview.png)](mono-editorial-banner/) |
| 安静纸面标本 | 暖纸拟物流程主视觉 | 黑白编辑横幅 |

## travel-postcard-agent

根据城市、节日、季节或特殊主题，生成现代旅行拼贴明信片提示词。

![现代旅行拼贴明信片](travel-postcard-agent/assets/preview.png)

[进入 Skill](travel-postcard-agent/) ｜ [文章复制版](travel-postcard-agent/ARTICLE-COPY.md)

### 使用示例

```text
用 travel-postcard-agent，生成一张杭州中秋主题的旅行拼贴明信片。
```

## swiss-typographic-poster

把瑞士国际主义视觉拆成网格、字体、几何图形和色彩模块，再编译成一条确定性提示词。

![瑞士国际主义海报](swiss-typographic-poster/assets/preview.png)

[进入 Skill](swiss-typographic-poster/) ｜ [文章复制版](swiss-typographic-poster/ARTICLE-COPY.md)

### 使用示例

```text
用 swiss-typographic-poster，生成一张 5:2 横版文章封面，标题是：结构决定秩序。
```

## bauhaus-visual-prompt

识别文章封面、正文配图、海报或室内重绘需求，生成对应的包豪斯视觉提示词。

![包豪斯视觉生成](bauhaus-visual-prompt/assets/preview.png)

[进入 Skill](bauhaus-visual-prompt/) ｜ [文章复制版](bauhaus-visual-prompt/ARTICLE-COPY.md)

### 使用示例

```text
用 bauhaus-visual-prompt，生成一张 4:5 文章封面，标题是：结构比装饰更重要。
```

```text
用 bauhaus-visual-prompt，参考我上传的室内照片，把这个房间重绘成包豪斯风格工作室。
```

## plakatstil-prompt-compiler

把文字主题、商品照片或包装照片，编译成 Plakatstil / Sachplakat 商品广告海报提示词。

![Plakatstil 商品海报](plakatstil-prompt-compiler/assets/preview.png)

[进入 Skill](plakatstil-prompt-compiler/) ｜ [文章复制版](plakatstil-prompt-compiler/ARTICLE-COPY.md)

### 使用示例

```text
用 plakatstil-prompt-compiler，把我上传的商品照片重绘成 Plakatstil 广告海报。
```

## neo-brutalist-prompt-compiler

用粗黑边框、硬阴影、扁平撞色和组件式构图，生成新粗野主义视觉提示词。

![新粗野主义视觉](neo-brutalist-prompt-compiler/assets/preview.png)

[进入 Skill](neo-brutalist-prompt-compiler/) ｜ [文章复制版](neo-brutalist-prompt-compiler/ARTICLE-COPY.md)

### 使用示例

```text
用 neo-brutalist-prompt-compiler，给这个 AI 产品生成一张 16:9 发布封面。
```

## acid-depth-poster

用清晰前景层和模糊后景层制造空间深度，把主题编译成 Y2K / Acid Graphics / 地下传单气质的实验海报提示词。

![前进色 × 后退色实验海报](acid-depth-poster/assets/preview.png)

[进入 Skill](acid-depth-poster/) ｜ [文章复制版](acid-depth-poster/ARTICLE-COPY.md)

### 使用示例

```text
用 acid-depth-poster，生成一张 5:2 横版封面，标题是：前进色 × 后退色。配色使用荧光玫红 × 电光蓝印刷底。
```

## quiet-paper-specimen

大留白陈纸背景、单一主体、中文手写大标题、一个落在主体上的高饱和色点，编译成「安静纸面标本」封面提示词。核心意象从十大家族的意象库里选，避免每张都退回叶子和旧照片。

![安静纸面标本](quiet-paper-specimen/assets/preview.png)

[进入 Skill](quiet-paper-specimen/)

### 使用示例

```text
用 quiet-paper-specimen，把这段随笔做成一张留白封面：那年冬天我没有寄出的信。
```

```text
用 quiet-paper-specimen，做一张 5:2 横版封面，标题用中文手写：凉了。
```

## tech-schematic-poster

用节点-连线拓扑图作主视觉，配 HUD 边框、图例、标尺和系统日志，编译成工程蓝图 / 赛博终端风格的封面和插图提示词。

![工程蓝图 / 赛博终端示意图](tech-schematic-poster/assets/preview.png)

[进入 Skill](tech-schematic-poster/)

### 使用示例

```text
用 tech-schematic-poster，给这篇讲多 Agent 分工的文章做一张 5:2 封面，标题是：从 Loop 到 Graph。
```

## craft-diorama-still-life

用剪纸、手作微缩和轻拟物质感，把一篇内容最强的那句判断压进一个实物里，编译成封面和逐章配图提示词。调色板是角色制的，可以直接填自己的品牌色。

![手作拟物静物](craft-diorama-still-life/assets/preview.png)

[进入 Skill](craft-diorama-still-life/) ｜ [文章复制版](craft-diorama-still-life/ARTICLE-COPY.md)

### 使用示例

```text
用 craft-diorama-still-life，给这篇文章做一张 5:2 封面，标题用中文。
```

```text
用 craft-diorama-still-life，品牌色是 #D64545，这篇每一节都配一张 16:9 章节图。
```

## grainy-plane-style

平涂大色块加细密颗粒，颗粒只落在主体、背景保持绝对干净。既能把一张照片整段改成插画风，也能不用照片、只给主题就出封面和插图。

![颗粒棱面风格](grainy-plane-style/assets/preview.png)

[进入 Skill](grainy-plane-style/) ｜ [文章复制版](grainy-plane-style/ARTICLE-COPY.md)

### 使用示例

```text
用 grainy-plane-style，把我这张照片改成颗粒棱面风格。
```

```text
用 grainy-plane-style，做一张 2:3 封面，主题是一台老打字机的局部特写。
```

## paper-workflow-hero

奶油纸底上，扁平 UI 卡片、写实拟物道具和半写实绘画人物三种质感共存，用流程图讲「输入→核心→标准→交付→回流」的产品叙事，适合官网 hero 和营销主图。版式、人物调度和桌面道具都做成模块库，成组产出时每张重抽，不会长成一个样。

![暖纸拟物流程主视觉](paper-workflow-hero/assets/preview.png)

[进入 Skill](paper-workflow-hero/) ｜ [文章复制版](paper-workflow-hero/ARTICLE-COPY.md)

### 使用示例

```text
用 paper-workflow-hero，给我的 AI 客服产品做一张 5:2 官网主视觉，核心概念是"知识库"。
```

```text
用 paper-workflow-hero，给这五个功能各做一张主视觉，版式和人物都要不一样。
```

## mono-editorial-banner

纯白虚空里放一个写实主体，主体自身带出纯黑作为画面唯一的黑色锚点，超大高反差衬线主标题压在上方，5:2 超宽横板。中英文标题都走衬线（Didone / 高对比宋体）。附一张主体词汇表，把「表面光鲜 vs 底下代价」「看不见的东西在承重」这类关系直接映射成具体装置。

![黑白编辑横幅](mono-editorial-banner/assets/preview.png)

[进入 Skill](mono-editorial-banner/) ｜ [文章复制版](mono-editorial-banner/ARTICLE-COPY.md)

### 使用示例

```text
用 mono-editorial-banner，给这篇文章做一张 5:2 封面，主标题是：TRUST IS INFRASTRUCTURE.
```

```text
用 mono-editorial-banner，中文标题，做一张 5:2 封面：记忆才是护城河。
```

---

## visual-identity-expander

**这一个从已有的视觉资产出发，风格不预设，从你给的那张图里现场萃取。**

把 Logo、头像、IP、插画或产品图扩展成统一的视觉身份提示词，适合继续制作头像、海报、贴纸、场景和产品化延展。

身份默认双锚——文字化写满、有图时再挂图锚点，所以出来的提示词离开对话仍然能用。附一张载体词汇表，包装和传播场景不会每次都退回马克杯和帆布袋。

[进入 Skill](visual-identity-expander/) ｜ [文章复制版](visual-identity-expander/ARTICLE-COPY.md)

### 使用示例

```text
用 visual-identity-expander，分析我上传的 Logo，并扩展成一组统一的品牌视觉提示词。
```

```text
用 visual-identity-expander，把我上传的头像扩展成一套 X 账号的个人品牌视觉。
```

```text
用 visual-identity-expander，我只要三张贴纸和一张动作设定板，不用出全套。
```

## 目录约定

```text
image-prompt-skills/
├── README.md
└── skill-name/
    ├── SKILL.md
    ├── ARTICLE-COPY.md
    ├── assets/
    ├── references/
    └── evals/
```

`assets/preview.png` 同时用于顶部风格样例宫格和各 Skill 分节里的示例图，是「从主题出发」那类 Skill 的必备项——它们各自锁定一种风格，预览图就是这个风格的样子。

`visual-identity-expander` 没有 `assets/`，也不需要有：它的成品长什么样由用户上传的图决定，放任何一张预览都会暗示一种它并不锁定的风格。

## 当前状态

仓库持续更新中。新增 Skill 时，会同步补充技能总表、调用示例和预览图。
