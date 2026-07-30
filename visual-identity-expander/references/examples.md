# Examples

四类输入的路由走查，加一条完整编译样例。

样例演示的是**编译结构**，不是已验证成品——色值、比例这些具体数字必须换成当次参考图里量出来的真实值。

## 路由走查

### 人物头像

```text
把我上传的头像扩展成 X 账号的个人品牌视觉，保留黑框眼镜和灰色夹克，整体偏理性、实验感。
```

路由：人物头像。锁定脸部身份、黑框眼镜、发型和灰色夹克；允许改变动作、背景和画幅。变化系统出动作与表情设定板。

交付提示词时提醒：文字锚点保得住眼镜、发型、夹克和气质，保不住同一张脸。

### Logo

```text
把这个橙色几何 Logo 扩展成一个科技工作室的视觉系统。
```

路由：Logo。锁定几何比例、橙色和负空间；变化系统走辅助图形与纹样，不默认生成人物 IP。几何关系要量化到边长比和笔画宽度。

### IP 角色

```text
让这个红色圆头角色拥有一套贴纸、动作设定和社交媒体封面。
```

路由：IP。锁定圆头轮廓、头身比、红色和五官。用户点名了三样东西——贴纸、动作、社交封面，就出对应的三条，不补齐五条。

### 产品

```text
用这张键盘照片做一套新品发布视觉。
```

路由：产品。锁定键盘布局、外壳材质和键帽配色；变化系统走视角与细节，应用系统走包装和电商载体。

## 完整编译样例

输入：橙色几何 Logo，科技工作室，品牌名 `NORTHLINE`。交付提示词，双锚。

### 视觉 DNA（原料，不直接交付）

- 核心轮廓：等边三角形去掉下半，切角 45°，负空间宽度等于笔画宽度
- 主色：saturated warm orange `#F25C1F`；辅色：near-black `#141414`、warm off-white `#F4F1EC`
- 图形语言：hard edges, no gradients, no ornament, 45° 与 90° 两种角度
- 材质与光线：matte uncoated stock，微弱纸纹，柔和方向光，无高光
- 气质：cool, restrained, engineered

### 01 主视觉

```text
Use case: brand key visual, single hero image.

Scene: a flat matte uncoated paper surface in warm off-white #F4F1EC, faint paper grain, soft directional light from the upper left casting a short soft-edged shadow.

Subject: the NORTHLINE mark — an equilateral triangle with its lower half removed, corners cut at 45 degrees, the negative space between strokes exactly as wide as the strokes themselves — rendered in saturated warm orange #F25C1F, sitting slightly above centre at 40% of the frame width. Image 1: identity reference — preserve the mark's proportions and negative space exactly.

Key details: hard edges throughout, no gradients, no bevels, no ornament; only 45-degree and 90-degree angles; matte finish with no specular highlight; near-black #141414 used only for the wordmark; cool, restrained, engineered mood.

Composition: 4:5 vertical, mark centred horizontally with 30% clear space above, wordmark set below the mark, generous margins, at least 55% empty surface.

Text in image: "NORTHLINE" set in a geometric sans, uppercase, wide letter-spacing, near-black #141414, small scale directly beneath the mark. Render all text verbatim, no extra words.

Constraints: preserve the triangle proportions, the 45-degree corner cuts, the negative space width and the orange #F25C1F; no gradients, no drop shadows on the mark, no additional logos, no invented taglines, no photographic texture on the mark, no perspective distortion.
```

### 02 视觉识别系统（同一基座，只换 Use case / Scene / Composition）

```text
Use case: identity system board, flat presentation layout.

Scene: a flat matte uncoated paper surface in warm off-white #F4F1EC, faint paper grain, even soft light, no cast shadows.

Subject: four separated panels laid out on a 2×2 grid with clear gutters between them. Panel one: the NORTHLINE mark — an equilateral triangle with its lower half removed, corners cut at 45 degrees, negative space as wide as the strokes — in saturated warm orange #F25C1F. Panel two: the same mark in single-colour near-black #141414. Panel three: a horizontal colour bar of three solid swatches, orange #F25C1F, near-black #141414, warm off-white #F4F1EC. Panel four: the mark at small scale with clear-space margins marked by thin rules. Image 1: identity reference — preserve the mark's proportions and negative space exactly.

Key details: hard edges throughout, no gradients, no bevels, no ornament; only 45-degree and 90-degree angles; matte finish with no specular highlight; cool, restrained, engineered mood.

Composition: 4:5 vertical, 2×2 grid, equal gutters, panels clearly separated rather than overlapping, generous outer margin.

Text in image: no text beyond the colour values "#F25C1F", "#141414", "#F4F1EC" set in small geometric sans beneath their swatches. Render all text verbatim, no extra words.

Constraints: preserve the triangle proportions, the 45-degree corner cuts, the negative space width and the orange #F25C1F; no gradients, no drop shadows, no additional logos, no invented labels, no overlapping panels, no perspective distortion.
```

对照两条看三件事：identity lock 一字未改；色板与气质整段重复；Constraints 的 preserve 清单完全一致，只有跟当前载体相关的排除项（`no overlapping panels`）是新加的。剩下三条同理往下推。
