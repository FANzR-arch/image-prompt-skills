# 中文排版规范（全仓库共享）

所有 skill 在提示词里指挥中文时都按这份写。

核心区分一句话：**字体类别按主题选，拉丁专属属性不要往中文上套。**

## 一、字体类别：按主题选，不要锁死

衬线 / 无衬线 / 手写这三类在中文里都有真实对应物，**指令有效，可以放心用**，而且应该跟着主题走——不同类别带的语气完全不同，锁死一种等于所有主题长一个样。

| 类别 | 中文对应 | 语气 | 适合的主题 |
|---|---|---|---|
| 衬线 serif | 宋体 / 明体 | 编辑感、克制、有分量、偏传统 | 观点文、长文封面、文化类、需要「说得算」的判断句 |
| 无衬线 sans | 黑体 | 当代、直接、信息感强 | 技术、产品、工具、数据、教程 |
| 手写 / 书法 | 手写体、毛笔字、马克笔字 | 人味、临场、粗粝、personal | 随笔、personal 叙述、地下感、涂鸦感、做旧海报 |
| 圆体 | 圆黑体 | 亲和、轻 | 生活方式、软性话题 |

同一个 skill 支持多种类别时，**把选择权留给主题**，不要在风格块里写死一种。

## 二、点名字族是加分项，不是替代品

在类别之上再点名字族，能显著提高字形稳定性。中英双写最稳：

| 想要的效果 | 写法 |
|---|---|
| 粗黑体（标题、标签块、强调） | `a heavy Chinese sans (思源黑体 / Source Han Sans, Heavy)` |
| 常规黑体（副标、说明、字段） | `a Chinese sans (思源黑体 / Source Han Sans, Regular)` |
| 细黑体（弱化的小字） | `a light Chinese sans (思源黑体 / Source Han Sans, Light)` |
| 宋体（编辑感、高对比标题） | `a high-contrast Chinese serif (思源宋体 / Source Han Serif) with thin horizontal strokes, thick vertical strokes and sharp triangular serifs` |
| 屏幕界面感 | `苹方 / PingFang` |
| 手写 / 书法 | 不点字族——写笔法：`hand-brushed Chinese lettering with visible brush entry and exit strokes` |

字重用 Light / Regular / Medium / Bold / Heavy，这个维度中文和拉丁是通的。

**手写和书法不要点字族**，它本来就不该是一个规整的数字字体；用笔法、工具和肌理去描述（毛笔、马克笔、喷漆、粉笔），并加一句笔画结构要正确。

## 三、这些词不要用在中文上

它们是拉丁字体的专属属性或谱系名，中文没有对应物：

| 禁用词 | 为什么 |
|---|---|
| `monospace` / `typewriter` | 中文没有等宽体和打字机体的常规概念 |
| `uppercase` / `lowercase` / `all-caps` / `capitals` | 中文无大小写 |
| `italic` / `oblique` / `斜体` | 中文无真斜体，模型会做机械倾斜或字形畸变。要动势就写倾斜排版（整行倾斜），不要写字体倾斜 |
| `grotesk` / `geometric sans` / `humanist sans` / `modernist sans-serif` / `Didone` | 拉丁字体史谱系，中文无对应血统 |
| `technical drafting lettering` | 制图技术字是拉丁工程字规范，中文无此标准 |
| `condensed capitals` / 极端 `letter-spacing` | 中文本身等宽排布；要窄要疏直接写 `condensed` / `loosely spaced`，不要带 capitals |

注意 `serif` / `sans-serif` / `handwritten` / `script` **不在此列**——它们是通用类别，对中文有效，见第一节。

## 四、中英混排要分开写

一条提示词里同时有中文和拉丁文时，**两套字体指令分开声明**，不要一句话罩住两边：

```
TYPOGRAPHY — Latin field labels and numerals in a neutral grotesk, uppercase;
the Chinese headline in a heavy Chinese sans (思源黑体 / Source Han Sans, Heavy).
```

## 五、渲染可靠性

- 常用字（3500 主用 / 6000 通用）和复杂字（曦、薇、澈、赟）都能稳定生成，**不要预设乱码、不要给「留白后期排字」的降级方案**；
- 已知失败区间：字号低于约 5pt、生僻字、文字与图像重叠、15 笔画以上的字有 5–10% 单次失败率。应对是**多生成几张挑**，不是退回后期；
- 整段长文案当叠加层后期排，短标题和字段标签直接生成；
- 画面有中文小字时 quality 拉到 `high`；
- 中文文案放引号里，并补 `render verbatim, no extra words or characters`；
- 特殊符号（`¥`、`&`、`·`）单独括出来说明。
