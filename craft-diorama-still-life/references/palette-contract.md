# 调色板契约

拟物静物风的辨识度有一半来自用色纪律，而不是物件本身。这份文件定义六个固定角色、映射规则和三套可直接用的预设。

## 六个角色

| 角色 | 面积 | 作用 |
| --- | --- | --- |
| Ground | 60-75% | 主背景、主承载面。画面的绝对主色，也是「温暖纸感」的来源 |
| Signal | 3-8% | 唯一的主动作／关键标记／被点亮的那个状态。整张图只有一处 |
| Support | 10-20% | 柔和的支撑卡片、面板、浅色表面。永远比 Signal 弱 |
| Accent A | < 3% | 极小面积的提醒、社群、人味点缀 |
| Accent B | < 3% | 状态点、时间胶囊、进度条 |
| Anchor | 5-12% | 唯一一个压场的深色实物、结构锚点。也可以当标题色 |

## 用色纪律

- Ground 绝对主导。画面看上去应该是「一片温暖的底 + 几个物件」，不是拼色块。
- **Signal 只有一个焦点。** 出现第二个同等强度的 Signal，画面立刻散掉。
- **Anchor 只落在恰好一个实物上**，不能铺成大色块或背景色。它的作用是把整张图压住。
- Accent A / B 是点，不是面。宁可少给，不要撒。
- 不引入霓虹、赛博朋克、荧光配色。这个风格靠材质取胜，不靠亮度。
- 纯色，无渐变。深浅变化只允许来自投影和材质本身。

## 品牌色映射规则

用户给了品牌色时，按下面的顺序映射，不要机械按色卡顺序填：

1. **先定 Ground。** 找品牌色里最浅、最暖、饱和度最低的那个；如果品牌色全是高饱和，就用品牌中性色或自选一个同温度的浅底，不要拿高饱和色当背景。
2. **再定 Signal。** 品牌主色（最常出现在按钮、主 CTA、logo 主体上的那个）直接进 Signal。
3. **再定 Anchor。** 品牌里最深的那个色；没有就取品牌主色的深色调，或用一个中性深色（深墨绿、深棕、炭黑偏暖）。
4. **Support** 用 Signal 的浅色调，或品牌辅助色里最柔和的一个。
5. **Accent A / B** 从剩下的品牌色里挑两个，挑不出就留空——**角色可以空着，但不能硬凑**。

只有一个品牌色时：该色进 Signal，Support 用它的 20% 浅调，Ground 和 Anchor 用中性色，两个 Accent 留空。

## 预设

### 预设一：Warm Ivory（默认）

温暖纸底＋紫色信号＋深绿压场，最贴近这个风格的本体，也是 README 里那张预览图用的配色。不确定时用这套。

| 角色 | 色值 | 名称 |
| --- | --- | --- |
| Ground | `#E1DAC0` | Warm Ivory |
| Signal | `#644FB8` | Iris Purple |
| Support | `#BAB2FF` | Lavender Mist |
| Accent A | `#B268D8` | Orchid Bloom |
| Accent B | `#504DDC` | Cobalt Pulse |
| Anchor | `#1B4038` | Deep Moss |

这套配色的成立之处：Warm Ivory 和 Deep Moss 都是低饱和的自然色，把 Iris Purple 衬成画面里唯一「被点亮」的东西；Lavender Mist 是 Iris Purple 的浅调，所以支撑面板不会跟主信号抢。换自己的品牌色时保持这个关系，比照抄色值更重要。

### 预设二：Cool Studio

偏冷、偏工具感，适合方法论、系统、工程类内容。

| 角色 | 色值 | 名称 |
| --- | --- | --- |
| Ground | `#E4E6E1` | Studio Grey |
| Signal | `#3F5BD9` | Working Blue |
| Support | `#CBD3D8` | Mist |
| Accent A | `#D98E3F` | Amber |
| Accent B | `#5B7F73` | Eucalyptus |
| Anchor | `#22262B` | Graphite |

### 预设三：Dusk Desk

低照度暖调，适合复盘、记忆、夜间工作、长期主义类内容。

| 角色 | 色值 | 名称 |
| --- | --- | --- |
| Ground | `#DCCDB4` | Lamplight |
| Signal | `#B4472C` | Ember |
| Support | `#C4B49A` | Parchment |
| Accent A | `#8A6E9E` | Plum |
| Accent B | `#3D6B63` | Teal Slate |
| Anchor | `#2A211C` | Cocoa Black |

## 写进提示词的方式

不要只丢一串色值。每个角色都要写清楚**落在哪个物件上**：

```text
Palette: warm ivory ground #E1DAC0 dominant; the single iris purple #644FB8 marker on the raised
route flag; lavender mist #BAB2FF supporting cards; one deep moss #1B4038 wooden base as the only
grounding anchor; tiny orchid #B268D8 dot on the side note and a cobalt #504DDC time chip. Solid
colors only, no gradients.
```

只给色值不给落点，生图模型会自己乱分配面积，Ground 主导和单一 Signal 这两条纪律就废了。
