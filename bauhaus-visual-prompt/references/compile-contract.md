# 编译契约

每次输出前必须满足。这是成品提示词和拼装草稿的分界。

## 6 条铁律

1. **先定媒介**：`article-cover`、`inline-illustration`、`poster`、`interior-redesign` 四选一。
2. **每个槽位唯一值**：删掉所有 `/` 选项、`{}` 占位和多套方案。
3. **一个主视觉**：只保留一种视觉引擎；不要同时写标题海报、家具、建筑、室内。
4. **正文零中文注释**：提示词正文只写英文美术指导；唯一例外是需要渲染进图里的中文标题。
5. **否定只进 AVOID**：正文用正向描述，所有 `no / not / avoid` 集中放到末尾。
6. **室内重绘保留原图结构**：有上传室内图时，必须明确保留视角、比例、门窗、墙体、主要家具位置。

## 锁死的风格内核

无论选什么用途，这些要点恒定：

- Bauhaus is a modern design-school method, not red-yellow-blue decoration.
- Function is visible: every shape, color, object, wall panel, or piece of furniture has a role.
- Geometry is structural: circles, rectangles, lines, modular blocks, asymmetric layout, and negative space organize the image.
- Color is disciplined: off-white, black, red, yellow, blue, steel, wood, leather, canvas, and white plaster appear only when the medium supports them.
- Typography is modernist and minimal: bold sans-serif for short titles, no fake small text.
- Surface is clean: flat color, hard edges, no grunge, no glossy 3D, no ornamental pattern.

## 字段顺序

成品提示词按此顺序输出：

```text
STYLE ANCHOR → FORMAT / USE CASE → LOCKED → DOMINANT VISUAL
→ MATERIAL & COLOR → TYPOGRAPHY / TEXT → PHOTO REDESIGN RULE（仅室内）
→ AVOID → QUALITY
```

## 成品骨架

```text
STYLE ANCHOR — Bauhaus as a modern design-school method: function-first organization, clear geometry, material honesty, disciplined typography, industrial clarity and no ornament.

FORMAT / USE CASE — ...

LOCKED — every element has a structural or practical role; geometric forms organize the image rather than decorate it; composition is rational, asymmetric, clear and disciplined.

DOMINANT VISUAL — ...

MATERIAL & COLOR — ...

TYPOGRAPHY / TEXT — ...

PHOTO REDESIGN RULE — ...

AVOID — ...

QUALITY — clean modernist design-school feeling, sharp geometry, flat color, useful structure, visually clear and immediately usable.
```

`PHOTO REDESIGN RULE` 只在室内照片重绘时出现。其他用途不要写这一行。
