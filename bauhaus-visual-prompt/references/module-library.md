# 模块库

作者工具，不外露给用户。每个槽位选一个，交给编译契约组装。

## 用途 USE CASE

| ID | 触发信号 | 写进 prompt 的重点 |
|---|---|---|
| COV | 文章封面、主视觉、标题视觉、cover | title hierarchy, geometric layout, visual anchor, flat color blocks, negative space |
| ILL | 正文配图、概念图、解释图、inline illustration | concept explanation, diagram-like geometry, clarity, low visual noise |
| POS | 海报、栏目海报、活动海报、poster | exhibition-poster energy, bold typography, type and geometry as one composition |
| INT | 上传室内照片、房间重绘、工作室、空间改造 | preserve original room geometry and redesign materials, furniture, lighting and color |

## 画幅 FORMAT

| ID | 用途 | 写进 prompt |
|---|---|---|
| F1 | X/小红书封面 | `vertical 4:5 editorial image` |
| F2 | 正文配图/头图 | `16:9 landscape editorial image` |
| F3 | 海报 | `vertical 2:3 exhibition poster` |
| F4 | 方图 | `1:1 square visual` |
| F5 | 宽封面 | `wide 5:2 landscape cover, designed for later cropping if the image model does not support this exact ratio` |
| F6 | 室内参考图 | `match the uploaded photo aspect ratio and camera perspective` |

## 主视觉 ENGINE

| ID | 用途 | 写进 prompt |
|---|---|---|
| E1 | 封面 | `one large circle as visual anchor, one rectangle as title area, one diagonal line as movement, and modular color blocks organizing the page` |
| E2 | 正文配图 | `a clear diagram-like arrangement of circles, rectangles, rule lines and modular blocks explaining one abstract concept` |
| E3 | 海报 | `bold sans-serif title integrated with geometric forms, strong asymmetry, large flat planes and exhibition-poster tension` |
| E4 | 室内 | `white plaster walls, modular shelving, simple work tables, tubular steel chairs, functional pendant lamps, open circulation and controlled color accents` |

## 色彩 COLOR

| ID | 用途 | 写进 prompt |
|---|---|---|
| K1 | 封面/海报经典 | `off-white, black, red, yellow and blue used as controlled flat structural accents` |
| K2 | 正文配图克制 | `off-white and black with one controlled red or blue accent` |
| K3 | 室内 | `warm off-white, black steel, natural wood, leather or canvas, with small controlled red, yellow or blue accents` |
| K4 | 强传播 | `off-white field, black typography, one large flat red or yellow structural plane` |

## 文字模式 TEXT MODE

| ID | 用途 | 规则 |
|---|---|---|
| T0 | 无文字 | 只生成视觉解释图或室内空间 |
| T1 | 英文主标 + 中文小标 | 大英文词承担视觉冲击，中文短标题承担意义 |
| T2 | 中文主标 + 英文小标 | 面向传播封面，中文必须短且可读 |
| T3 | 纯英文海报 | 适合活动海报、系列海报、展示图 |

## 意图映射

| 用户输入 | Use case | Format | Engine | Color | Text |
|---|---|---|---|---|---|
| 文章封面、主视觉、标题视觉 | COV | F1/F5 | E1 | K1/K4 | T1/T2 |
| 正文配图、概念解释、结构图 | ILL | F2 | E2 | K2 | T0/T1 |
| 海报、活动、栏目、poster | POS | F3/F1 | E3 | K1/K4 | T1/T3 |
| 室内照片、房间、工作室、空间重绘 | INT | F6/F2 | E4 | K3 | T0 |

冲突时优先级：用户明确指定 > 是否有上传图 > 用途 > 标题语气 > 默认。拿不准时择优定一个，并在选型理由里说明假设。

## 风格偏移护栏

必须按用途放进 AVOID：

- 封面/海报：generic red-yellow-blue decoration, random geometric stickers, vintage grunge paper, glossy 3D, fake small text, Swiss-style excessive neutrality, Constructivist propaganda mood.
- 正文配图：stock illustration look, cute icons, data chart, complex infographic, random labels, fake UI.
- 室内重绘：Scandinavian cozy decor, luxury marble, cyberpunk lighting, boho textiles, random primary-color stickers, unrelated room layout, fake posters with unreadable text.
