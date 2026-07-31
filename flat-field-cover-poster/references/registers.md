# 模块库（色场 / 桥接元素 / 机位 / 品类）

四张表。编译前各取一行，取完即锁死，不在成品里留菜单。

## 一 · 色场寄存器

底色决定影调、三色板和标题色，是最先定的东西。**标题色取三色板里明度离底色最远的那个**。

### 已验证（四条实测）

| 底色 | 影调 grade | 三色板 | 标题色 | 对口品类 |
|---|---|---|---|---|
| 赤陶 burnt terracotta | `warm, matte, low-contrast vintage editorial` + 细微颗粒 | terracotta / cream / sage-green | cream | 时尚、生活方式 |
| 墨绿 ink green | `warm matte low-contrast` | ink-green / ivory / terracotta-grey | ivory | 东方、茶道、文化、手艺 |
| 柠檬黄 lemon yellow | `hard-contrast daylight` | lemon-yellow / black / warm-grey | **black** | 运动、街头、青年文化 |
| 深梅紫 deep plum | `rich low-key matte` | deep-plum / antique-bronze / ivory | ivory | 美妆、香氛、夜色 |

柠檬黄是唯一用深色标题的一条——底色明度太高，浅字会糊掉。这条是判断规则的来源，不是例外。

### 待验证（按同一逻辑推导，首次使用时告知用户未实测）

| 底色 | 影调 grade | 三色板 | 标题色 | 对口品类 |
|---|---|---|---|---|
| 石板蓝 slate blue | `cool matte low-contrast` | slate-blue / bone-white / rust | bone-white | 商业人物、科技、访谈 |
| 陈玫粉 dusty rose | `soft matte low-contrast` | dusty-rose / oat / charcoal | charcoal | 生活方式、家居、亲密主题 |
| 橄榄绿 olive | `dry warm matte` | olive / sand / brick-red | sand | 户外、工艺、农事、旅行 |
| 炭黑 charcoal | `low-key matte with a single soft key` | charcoal / off-white / amber | off-white | 深度人物、思想、纪实 |

新增色场的判定：底色一个、辅助色一个明度对立、点缀色一个色相偏移。三个色相封顶，第四个一律砍掉。

## 二 · 桥接元素

**全套的命门。** 它压在前景下角，是唯一同时属于照片层和图形层的东西。

两条硬约束，同时满足才成立：

1. **是主题的物质隐喻**——喝茶配茶枝，冲刺配轨迹，香氛配烟。
2. **和主体身上某样东西同源**——裙子的水彩印花 ↔ 前景的水彩花枝。找不到同源关系就换元素，宁可换主体服装来制造同源，也不要放一个纯装饰。

位置取**光源的对侧下角**：光从右上来，元素落左下。

| 主题域 | 元素 | 媒介写法 | 同源挂点 |
|---|---|---|---|
| 时尚 / 植物 | 一枝花配叶 | `watercolor-style` | 服装印花用同一批花 |
| 茶 / 东方 / 手艺 | 茶枝、竹节、器物剪影 | `loose sumi brushwork` | 麻布、陶土的哑光肌理 |
| 运动 / 速度 | 三道运动轨迹笔触 | `thick hand-drawn marker strokes` | 身体的动势方向 |
| 香氛 / 夜色 | 一缕卷曲烟带 | `loose gouache brushwork` | 首饰或发丝的金属反光 |
| 音乐 / 声音 | 一组弦线或声波 | `single-weight ink lines` | 乐器材质或耳饰 |
| 建筑 / 设计 | 一段轴测线稿构件 | `technical pen line drawing` | 服装的结构剪裁 |
| 食物 / 农事 | 食材的枝叶与切面 | `watercolor-style` | 围裙或器皿的釉色 |
| 写作 / 文学 | 一片墨迹或翻起的纸角 | `ink wash` | 纸质感的衣料 |
| 科技 / 数据 | 一小段节点连线图 | `hand-drawn marker` | 屏幕光或金属配饰 |
| 旅行 / 地理 | 一段等高线或路径 | `watercolor-style` | 行囊材质或织物纹样 |

## 三 · 主体机位

景别、姿态、手部处理三项一起定。**手部只有两种合法处理：不入画，或明确抓着一件叫得出名字的东西。**

| 景别 | 姿态 | 手部 | 适合 |
|---|---|---|---|
| 大腿以上 | 正面站立，下巴微抬，俯视镜头 | 手垂在身侧与身后，不入画 | 时尚全身感、服装是主角 |
| 腰以上 | 正面，视线下垂 | 双手在胸前捧一件命名器物 | 文化、手艺、器物同时出镜 |
| 胸以上 | 微仰头，闭眼 | 不入画 | 美妆、香氛、情绪特写 |
| 大腿以上 | 动态扭身，重心前压 | 在运动中，需按名描述位置 | 运动、街头 |
| 腰以上 | 四分之三侧身，回看镜头 | 一只手扶在肩或臂上 | 人物访谈、商业肖像 |

高风险提示：胸前捧物是全套里手部废图率最高的构图，器物要写 `a single continuous solid form`；动态姿态的手必须点名，否则会长出多余手指。

## 四 · 品类标签与摄影体裁

左上角 `<CATEGORY> FEATURE`，一个词；Subject 段末尾的 `Photorealistic <GENRE> photography` 跟着走。

| 品类 | 标签词 | GENRE |
|---|---|---|
| 时尚 | FASHION | model |
| 文化 / 茶 | TEA、CRAFT、CULTURE | portrait |
| 运动 | TRACK、FIELD、SPORT | sports |
| 美妆 / 香氛 | SCENT、BEAUTY | beauty |
| 人物访谈 | PROFILE | editorial portrait |
| 食物 | KITCHEN、HARVEST | portrait |

## 成组产出

一组封面共享骨架，**每张之间换四样**：色场、主体、桥接元素、两词标题。排版寄存器整组统一，不要一张 CLEAN 一张 ROUGH。

风格基座四段（Scene 结构 / Composition / Text 规格 / Constraints）逐字写进每一条，模型看不见组的概念。
