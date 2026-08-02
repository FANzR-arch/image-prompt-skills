# 已验证成品

四条实测 prompt，原文照录。骨架完全一致，只换色场、主体、桥接元素、两词标题和排版寄存器——这四条本身就是本风格「同骨架换填空」的证明。

出图参数统一：size `2048×3072`，quality `high`。

---

## 母版 · 时尚（赤陶 / CLEAN）

色场：赤陶 · terracotta-cream-sage｜桥接：水彩花枝 lower-left｜遮挡：FLORAL 穿过头肩

```text
Use case: fashion magazine cover poster, vertical format, headline typography
baked into the image.
Scene: a flat, solid burnt-terracotta background with no gradient; warm, matte,
low-contrast vintage editorial grade over the whole image, subtle film grain.
Subject: a young woman with short tousled copper-red hair with bangs, fair
lightly freckled skin, chin raised and eyes looking down into the camera with a
calm confident expression; she wears small floral drop earrings and a cream
wrap dress with a V-neckline and short puffed sleeves, printed all over with
watercolor-style peach flowers and sage-green leaves; she stands centered and
frontal, framed from mid-thigh up, arms relaxed at her sides and behind her
back, hands not visible. Photorealistic model photography.
Key details: soft, even, warm studio light with gentle shadows; skin, hair,
dress and background all harmonized into one terracotta-cream-sage palette; a
large painted botanical branch — one peach flower with green leaves in the same
watercolor style as the dress print — overlaps the lower-left foreground,
bridging the photo layer and the graphic layer.
Composition: vertical cover layout; an oversized cream display headline in tall
condensed capitals spans the top third edge-to-edge, with the second line
passing behind the model's head and shoulders so the letters are partially
occluded; an editorial layout system surrounds her: a small label with two
short placeholder body-text blocks upper left, index numbers with thin rules at
mid-left and along the right edge, a small barcode-like tick row on the left,
a few tiny dots and plus marks; generous margins, everything aligned to a
clean grid.
Text in image: headline "EDITORIAL" on the first line and "FLORAL" on the
second line, in oversized tall condensed cream capitals; label "FASHION
FEATURE" in small letter-spaced cream capitals, upper left; index numbers
"01", "02", "03" in small cream figures beside thin rules; all other text
blocks are tiny illegible placeholder lines. Render the specified words
verbatim, no extra readable words.
Constraints: no logos, no watermark, no UI icons or buttons, no readable text
other than specified; keep the background a single flat color with no gradient
or scenery.
```

**注**：这条的标题是四条里唯一「长词在前、短词在后」的，遮挡效果也最弱。后三条改成短词在前、长词在后，遮挡明显更好。新做时按后三条走。

---

## 变体 A · 茶道（墨绿 / CLEAN）

色场：墨绿 · ink-green-ivory-terracotta-grey｜桥接：水墨茶枝 lower-right（光从左来）｜同源挂点：麻布与陶土的哑光肌理

```text
Use case: culture magazine cover poster, vertical format, headline typography
baked into the image.
Scene: a flat, solid ink-green background with no gradient; warm matte
low-contrast grade over the whole image.
Subject: a woman in her forties with hair pulled back smoothly, calm downward
gaze, wearing an ivory linen wrap jacket; she holds a small unglazed clay tea
bowl at chest height in both hands, framed from the waist up, centered and
frontal. Photorealistic portrait photography.
Key details: soft directional light from the left with long gentle shadows;
skin, linen, clay and background all harmonized into one ink-green, ivory and
terracotta-grey palette; a painted ink branch of tea leaves in loose sumi
brushwork overlaps the lower-right foreground, bridging the photo layer and the
graphic layer.
Composition: vertical cover layout; an oversized ivory display headline in tall
condensed capitals spans the top third edge-to-edge, with the second line
passing behind her head and shoulder so the letters are partially occluded; an
editorial layout system surrounds her: a small label with two short placeholder
text blocks upper left, index numbers with thin rules along the right edge, a
thin tick row lower left; wide margins, everything aligned to a clean grid.
Text in image: headline "SLOW" on the first line and "CEREMONY" on the second
line, in oversized tall condensed ivory capitals; label "TEA FEATURE" in small
letter-spaced ivory capitals, upper left; index numbers "01", "02", "03" in
small ivory figures beside thin rules; all other text blocks are tiny illegible
placeholder lines. Render the specified words verbatim, no extra readable words.
Constraints: no logos, no watermark, no UI elements, no readable text other
than specified; background stays a single flat color with no gradient or
scenery.
```

**注**：唯一一条把桥接元素放右下的——因为光从左来，元素走对侧。这是位置规则的来源。手捧茶碗是全套废图率最高的构图，重做时建议在 Constraints 追加 `the tea bowl stays a single continuous solid form`。

---

## 变体 B · 街头运动（柠檬黄 / ROUGH）

色场：柠檬黄 · lemon-yellow-black-warm-grey｜桥接：马克笔轨迹 lower-left｜**唯一深色标题、唯一 ROUGH 寄存器**

```text
Use case: sports magazine cover poster, vertical format, headline typography
baked into the image.
Scene: a flat, solid lemon-yellow background with no gradient; hard-contrast
daylight grade over the whole image.
Subject: a young sprinter caught mid-stride, torso twisted toward the camera,
breathing hard with a focused expression, short braided hair, wearing a plain
black tank top; framed from the thighs up, weight thrown forward. Photorealistic
sports photography.
Key details: hard direct light from the upper right with crisp shadows; skin,
kit and background harmonized into one lemon-yellow, black and warm-grey
palette; three thick hand-drawn marker strokes sweep across the lower-left
foreground tracing his motion path, bridging the photo layer and the graphic
layer.
Composition: vertical cover layout; an oversized black display headline in tall
condensed capitals spans the top third edge-to-edge, with the second line
passing behind his head and shoulder so the letters are partially occluded; a
deliberately rough editorial layout surrounds him: a small label with two short
placeholder text blocks upper left, index numbers with thick rules along the
left edge, a dense tick row lower right; tight margins, elements slightly
off-grid.
Text in image: headline "RAW" on the first line and "DISTANCE" on the second
line, in oversized tall condensed black capitals; label "TRACK FEATURE" in
small letter-spaced black capitals, upper left; index numbers "01", "02", "03"
in small black figures beside thick rules; all other text blocks are tiny
illegible placeholder lines. Render the specified words verbatim, no extra
readable words.
Constraints: no logos, no brand marks on the kit, no watermark, no readable
text other than specified; background stays a single flat color with no
gradient or scenery.
```

**注**：ROUGH 寄存器的完整样本——粗线、紧边距、出格、序号移左缘、刻度行移右下，五项一起改。同时是深色标题的唯一样本，因为柠檬黄明度太高，浅字会糊。追加了 `no brand marks on the kit`，运动服装必带。

---

## 变体 C · 香水夜色（深梅紫 / CLEAN）

色场：深梅紫 · deep-plum-antique-bronze-ivory｜桥接：水粉烟带 lower-left｜同源挂点：古铜耳饰的金属反光

```text
Use case: beauty magazine cover poster, vertical format, headline typography
baked into the image.
Scene: a flat, solid deep plum background with no gradient; rich low-key matte
grade over the whole image.
Subject: a woman with sleek dark hair swept back, eyes closed, chin lifted,
bare shoulders, a single antique-bronze drop earring catching the light; framed
from the chest up, centered and frontal. Photorealistic beauty photography.
Key details: soft rim light from behind the right shoulder with deep falloff
into shadow; skin, hair and background harmonized into one deep-plum,
antique-bronze and ivory palette; a painted ribbon of bronze smoke curls
through the lower-left foreground in loose gouache brushwork, bridging the
photo layer and the graphic layer.
Composition: vertical cover layout; an oversized ivory display headline in tall
condensed capitals spans the top third edge-to-edge, with the second line
passing behind her head and shoulder so the letters are partially occluded; an
editorial layout system surrounds her: a small label with two short placeholder
text blocks upper left, index numbers with thin rules along the right edge, a
thin tick row lower left; generous margins, everything aligned to a clean grid.
Text in image: headline "AFTER" on the first line and "MIDNIGHT" on the second
line, in oversized tall condensed ivory capitals; label "SCENT FEATURE" in
small letter-spaced ivory capitals, upper left; index numbers "01", "02", "03"
in small ivory figures beside thin rules; all other text blocks are tiny
illegible placeholder lines. Render the specified words verbatim, no extra
readable words.
Constraints: no logos, no watermark, no readable text other than specified;
background stays a single flat color with no gradient or scenery.
```

**注**：唯一用轮廓光的一条，也是三色板最窄的一条（深紫 + 古铜 + 象牙都在暖色轴上）。低调影调下要盯住底色，暗部很容易被渲染成渐变而不是平涂。

---

## 四条互相印证出来的规则

这一节是模块表的来源，改模块表前先看这里。

1. **骨架 100% 一致**，连句式和词序都没动过。变的只有九个槽位：品类、底色、影调、光位、景别、三色板、桥接元素、两词标题、排版寄存器。
2. **桥接元素必须和主体同源**：裙子印花是水彩花 → 前景是水彩花枝；喝茶 → 水墨茶叶；冲刺 → 运动轨迹；香水 → 烟带。四条无一例外。
3. **桥接元素放在光源对侧下角**。A 的光从左来，元素就在右下；B 的光从右上来，元素在左下。
4. **排版寄存器是联动开关**。B 一动就改了五处，且序号与刻度行整体镜像。
5. **标题第二行必须够长**（6–9 字母），后三条全是「短词 + 8 字母长词」。母版是唯一反例，遮挡也最弱。
6. **手部只有两种解**：母版明写 `hands not visible` 躲手，A 让手捧茶碗给手一个任务。没有第三种。
7. **Constraints 有品类专属追加项**：B 的 `no brand marks on the kit` 是运动品类必带。
