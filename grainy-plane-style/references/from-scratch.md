# 从零生成 · 母版与模块库

组合方式：**主体类型 × 配色逻辑 × 机位构图**。填母版即可。

## DNA 固定块（逐字复用，只换方括号内容）

```text
Scene: a single flat [主场色] field that is perfectly smooth and completely free
of any grain, noise or texture, no scenery, no horizon.

Key details: the subject only is filled with a dense, fine, even stipple, like
spray paint pushed through a stencil, and that stipple erodes the subject's
boundaries into finely speckled, slightly ragged edges — each shape stays
completely legible and in focus, yet no edge is a smooth clean vector line. The
background stays untouched clean flat colour with no grain at all. Keep tonal
steps minimal: one even colour per plane, no faceted shading inside a plane.
Closed palette — [色板].

Constraints: no grain, noise or texture anywhere in the background, no smooth
clean vector edges, no flat crisp digital shapes, no faceted tonal stepping, no
blurring or soft focus, no woolly or felted texture, no low-poly triangulation,
not photorealistic, no 3D render, no outlines, no gradients, no logos, no
watermark.
```

## 母版

```text
Use case: editorial illustration [肖像 / 静物 / 动物 / 地景 / 场景 / 植物],
vertical 2:3, no text.

Scene: ……（DNA 固定块，换主场色）

Subject: [主体 + 状态], built from only a handful of large planes — [逐个点名
4–6 个大面及其颜色归属]; [需要保持锐利的局部逐个点名].

Key details: ……（DNA 固定块，换色板）

Composition: [机位], [主体在画面的位置与占比], [留空区域].

Text in image: no text.

Constraints: ……（DNA 固定块）
```

参数层：size `1024x1536`（2:3）或按用途改；quality `medium`。

地景题材唯一允许的 DNA 放宽：单一色场改两条平涂色带（天/海），**两条色带都要写零噪**，且仍须写 `no rendered scenery, clouds or waves`。

## 配色逻辑模块

换的是逻辑不是色号——换逻辑才换气质。

| 代号 | 逻辑 | 适用 | 参考色板 |
|---|---|---|---|
| P1 | 高对比补色（黑白作锐点） | 英雄式单主体，张力最强 | 钴蓝场 / 玫瑰粉 / 深洋红 / 暖白 / 金黄 / 黑 |
| P2 | 同类色近邻，靠明度差分层 | 安静高级，需明度差撑可读性 | 赤陶橙场 / 深棕 / 砖红 / 奶白 / 金黄 |
| P3 | 暗调单色 + 单点亮色 | 器物、静物、夜感 | 暗墨绿场 / 铁灰 / 石板灰 / 奶油 / 朱红 |
| P4 | 大地矿物色，全低饱和暖调 | 手工感、时间感、自然题材 | 鼠尾草绿场 / 橄榄 / 陶土 / 赭石 / 象牙 |
| P5 | 冷灰低饱和 + 一小块暖 | 空旷、疏离、地景 | 雾灰蓝场 / 石灰白 / 深青 / 炭灰 / 暖橙 |
| P6 | 明快三原色 | 海报感、运动、大众题材 | 柠檬黄场 / 朱红 / 钴蓝 / 纯黑 / 纯白 |

## 机位构图模块

| 代号 | 机位 | 效果与适用 |
|---|---|---|
| C1 | 极低仰视紧裁 | 压迫感、纪念碑感 |
| C2 | 正侧剪影 | 轮廓最大化、最图形化，适合动物与器物 |
| C3 | 正上方俯视平铺 | 消除纵深、纯图案化，适合植物与工具 |
| C4 | 平视中景 | 中性叙事，适合多主体并置 |
| C5 | 极特写局部 | 靠质感与局部形状取胜 |
| C6 | 极远景大留空 | 主体极小、色场为主，情绪空旷 |

## 组合禁忌

1. **C6 极远景 × 细密颗粒**：主体过小时颗粒会盖掉形状。最小色块面积须占画面 3% 以上，否则改用 C4；
2. **P2 同类色 × C6**：可读性双重削弱，必须拉开明度差；
3. **多主体 × 少量大棱面**：主体越多每个越要简化（脸可直接处理成无五官的暗色面），否则面数爆炸退回 low-poly；
4. **C3 正上方俯视**：须显式写 `no perspective depth`，否则模型会加透视和投影；
5. **P3 单点亮色**：亮色只许出现一处，在 Subject 槽就点名 `the only bright element`。

## 六条参照示例

`references/examples.md`，覆盖器物 / 动物 / 地景 / 多人 / 植物 / 人物全身六类主体，配色与机位各不重复，固定块已对齐当前 DNA，直接取用。未逐条实测。
