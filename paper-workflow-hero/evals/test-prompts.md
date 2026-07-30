# 首轮测试提示词（五条）· 已跑完

> **结论（2026-07-31）**：风格层全过，调度层不合格。
>
> 成立：三语域分离、单一 accent 贯穿、四组色板、英文文字渲染（含卡片小字与 tagline 变色词）全部一次通过，无需修母版风格块。
>
> 不成立：五张的版式、人物位置、姿态、裁切、桌面道具几乎完全一样——初版母版把源图的一次调度决策（右 30%、齐腰裁切、一人托腮一人指、马克杯 + 摊开笔记本）写成了固定值。已拆成调度模块库，见 `references/from-scratch.md` 表一至表三，续测见 `test-prompts-round2.md`。
>
> 未验证：中文字形（实测时五张全走了英文）。

以下为首轮原始记录。

| # | 领域 | 道具 | 色板 | 人物 | 画幅 | 主测风险 | 结果 |
|---|---|---|---|---|---|---|---|
| 1 | 内容发布管线 | letterpress type tray | 默认（cream/violet） | 双人 | 5:2 | 三语域是否被统一 | 待测 |
| 2 | 记账结账 | brass balance scale | 灰纸墨蓝 | 单人 | 5:2 | 换色板后风格是否漂 | 待测 |
| 3 | 招聘交付 | rolodex | 墨绿信笺 | 双人 | 5:2 | 道具语义可读性 | 待测 |
| 4 | 工地项目管理 | wooden toolbox | 暖沙陶土 | 只有手 | 16:9 | 去人物 + 换画幅后构图 | 待测 |
| 5 | 合同审查（中文） | wooden drawer | 默认 | 双人 | 5:2 | 中文字形渲染 | 待测 |

第 5 条风险最高：中文标题在 gpt-image-2 上错字率明显高于英文。若字形崩坏，先减字数（标题缩到 5 字以内），再考虑标题留英文、卡片标签用中文的混排。

---

## 1 · 内容发布管线（默认色板 / 活字盘 / 双人 / 5:2）

```
Use case: wide marketing hero illustration for an AI writing service that publishes in the author's own voice, landing-page key visual, 5:2 horizontal.

Scene: a single warm cream paper background, one uniform ivory tone with a very subtle paper grain, soft even ambient light; an editorial flowchart tableau spread across the left two thirds of the frame; a plain light table surface at the bottom right merging into the background.

Subject: a left-to-right flowchart built from mixed physical and UI elements:
- input column at far left: three off-white rounded UI cards, each with one thin purple line icon and one short label, reading "Drafts", "Notes", "Voice memos";
- center: a wooden letterpress type tray holding rows of small metal type pieces, a real tactile object rendered photorealistically, carrying the core metaphor, with a small physical label on its front reading "Voice", and four compartment tabs inside reading "Rhythm", "Phrases", "Openings", "Past posts";
- next, a tall off-white UI card titled "House Style", listing "Rhythm", "Clarity", "Length", "Sources" as short lines each marked with a small purple check icon, thin divider lines above and below the list, and a small purple footer note "Set once";
- output at the right end of the diagram: a neat stack of layered paper sheets with realistic paper edges, the top sheet reading "Post published" with a smaller subline "In your voice. Every time." and one large purple circled checkmark;
- a feedback loop along the bottom: a small UI card with a purple growth-chart line icon captioned "Learns your edits", a purple pill badge on the loop line reading "Gets sharper", the line returning into the letterpress tray;
- one orange sticky note pinned with a realistic metal pushpin at the top left corner, slightly rotated, holding a simple white pen glyph and the words "Writing studio";
- in the right third: two people seated at the table, painted in a warm semi-realistic editorial style — one resting a hand on their chin in thought, the other pointing toward the diagram — both gazes fixed on the flowchart, never on the viewer.

Key details: three rendering registers coexist and must stay distinct — flat UI cards (matte off-white, rounded corners, soft diffuse drop shadows, thin purple line icons, clean humanist sans labels, no gradients), photoreal tactile props (visible fabric weave, metal, layered paper edges, soft contact shadows), and painted semi-realistic people (warm natural skin tones, soft brushed edges, fine canvas grain, no outlines, not photographic). All connectors are medium-weight deep-violet lines with rounded right-angle bends and small solid triangular arrowheads. One single deep-violet accent used for every icon, connector, checkmark and badge; one saturated orange allowed only on the sticky note. Lighting soft and warm from the upper left, shadow direction identical across cards, props and people.

Composition: 5:2 horizontal. Large serif headline in near-black forest green at top center-left, its top edge at roughly 8% of frame height; the flowchart occupies the left 65–70% of the width, reading strictly left to right with the feedback loop along the bottom edge of the diagram; the two people occupy the right 30%, cropped at the waist by the table edge; generous cream breathing room around every element; small serif tagline at the bottom right.

Text in image: headline "Write it once." and "Sound like you." stacked on two lines, large elegant high-contrast serif, near-black green; all card labels and list items in a clean humanist sans; tagline "You bring the ideas. Quill keeps the voice." at bottom right in a smaller serif with only the word "Quill" in the accent violet; render all text verbatim, no extra words.

Constraints: no glossy 3D plastic render, no gradients or glassmorphism on cards, no neon colors, background stays one clean cream tone with no texture buildup, people painted not photographic and never outlined, no photo-collage seams between people and background, people never look at the viewer, connector lines never cross card interiors, no more than six diagram nodes, no real brand logos or watermarks, shadow direction identical everywhere, render all text verbatim.
```

---

## 2 · 记账结账（灰纸墨蓝 / 天平 / 单人 / 5:2）

```
Use case: wide marketing hero illustration for a bookkeeping service that closes the month automatically, landing-page key visual, 5:2 horizontal.

Scene: a single cool light-grey paper background, one uniform tone with a very subtle paper grain, soft even ambient light; an editorial flowchart tableau spread across the left two thirds of the frame; a plain light table surface at the bottom right merging into the background.

Subject: a left-to-right flowchart built from mixed physical and UI elements:
- input column at far left: three off-white rounded UI cards, each with one thin ink-blue line icon and one short label, reading "Receipts", "Invoices", "Bank feeds";
- center: a brass balance scale with small folded paper notes resting on both pans, a real tactile object rendered photorealistically with warm metal reflections, carrying the core metaphor, with a small engraved plate on its base reading "Ledger", and a thin stack of filed slips tucked beneath it;
- next, a tall off-white UI card titled "Rules", listing "Categories", "Thresholds", "Approvals", "Cutoffs" as short lines each marked with a small ink-blue check icon, thin divider lines above and below the list, and a small ink-blue footer note "Set once";
- output at the right end of the diagram: a neat stack of layered paper sheets with realistic paper edges, the top sheet reading "Books closed" with a smaller subline "Balanced. On the day." and one large ink-blue circled checkmark;
- a feedback loop along the bottom: a small UI card with an ink-blue growth-chart line icon captioned "Learns your categories", an ink-blue pill badge on the loop line reading "Stays closed", the line returning into the balance scale;
- one marigold-yellow sticky note pinned with a realistic metal pushpin at the top left corner, slightly rotated, holding a simple white calendar glyph and the words "Month-end, done";
- in the right third: one person seated at the table, painted in a warm semi-realistic editorial style, chin resting on hand, studying the diagram with a faint smile, gaze fixed on the flowchart, never on the viewer.

Key details: three rendering registers coexist and must stay distinct — flat UI cards (matte off-white, rounded corners, soft diffuse drop shadows, thin ink-blue line icons, clean humanist sans labels, no gradients), photoreal tactile props (visible metal, paper edges, soft contact shadows), and painted semi-realistic people (warm natural skin tones, soft brushed edges, fine canvas grain, no outlines, not photographic). All connectors are medium-weight deep ink-blue lines with rounded right-angle bends and small solid triangular arrowheads. One single deep ink-blue accent used for every icon, connector, checkmark and badge; one saturated marigold yellow allowed only on the sticky note. Lighting soft and warm from the upper left, shadow direction identical across cards, props and people.

Composition: 5:2 horizontal. Large serif headline in near-black charcoal at top center-left, its top edge at roughly 8% of frame height; the flowchart occupies the left 65–70% of the width, reading strictly left to right with the feedback loop along the bottom edge of the diagram; the person occupies the right 30%, cropped at the waist by the table edge; generous grey-paper breathing room around every element; small serif tagline at the bottom right.

Text in image: headline "Close the month." and "Not your evening." stacked on two lines, large elegant high-contrast serif, near-black charcoal; all card labels and list items in a clean humanist sans; tagline "You set the policy. Ledgerly does the closing." at bottom right in a smaller serif with only the word "Ledgerly" in the accent ink-blue; render all text verbatim, no extra words.

Constraints: no glossy 3D plastic render, no gradients or glassmorphism on cards, no neon colors, background stays one clean light-grey tone with no texture buildup, people painted not photographic and never outlined, no photo-collage seams between people and background, people never look at the viewer, connector lines never cross card interiors, no more than six diagram nodes, no real brand logos or watermarks, shadow direction identical everywhere, render all text verbatim.
```

---

## 3 · 招聘交付（墨绿信笺 / 旋转名片盒 / 双人 / 5:2）

```
Use case: wide marketing hero illustration for a recruiting service that delivers a shortlist every week, landing-page key visual, 5:2 horizontal.

Scene: a single pale sage paper background, one uniform tone with a very subtle paper grain, soft even ambient light; an editorial flowchart tableau spread across the left two thirds of the frame; a plain light table surface at the bottom right merging into the background.

Subject: a left-to-right flowchart built from mixed physical and UI elements:
- input column at far left: three off-white rounded UI cards, each with one thin forest-green line icon and one short label, reading "Referrals", "Applications", "Sourcing";
- center: a metal rolodex with its address cards flipped open mid-rotation, a real tactile object rendered photorealistically with brushed metal and worn card edges, carrying the core metaphor, with a small physical label on its base reading "Shortlist", and four visible cards inside reading "Skills", "Track record", "References", "Notes";
- next, a tall off-white UI card titled "Bar", listing "Skills", "Seniority", "Culture", "Comp" as short lines each marked with a small forest-green check icon, thin divider lines above and below the list, and a small forest-green footer note "Set once";
- output at the right end of the diagram: a neat stack of layered paper sheets with realistic paper edges, the top sheet reading "Slate delivered" with a smaller subline "Five names. Every Friday." and one large forest-green circled checkmark;
- a feedback loop along the bottom: a small UI card with a forest-green growth-chart line icon captioned "Learns your yeses", a forest-green pill badge on the loop line reading "Keeps hiring", the line returning into the rolodex;
- one brick-red sticky note pinned with a realistic metal pushpin at the top left corner, slightly rotated, holding a simple white person glyph and the words "Hiring, handled";
- in the right third: two people seated at the table, painted in a warm semi-realistic editorial style — one resting a hand on their chin in thought, the other pointing toward the diagram — both gazes fixed on the flowchart, never on the viewer.

Key details: three rendering registers coexist and must stay distinct — flat UI cards (matte off-white, rounded corners, soft diffuse drop shadows, thin forest-green line icons, clean humanist sans labels, no gradients), photoreal tactile props (visible brushed metal, worn card edges, layered paper, soft contact shadows), and painted semi-realistic people (warm natural skin tones, soft brushed edges, fine canvas grain, no outlines, not photographic). All connectors are medium-weight deep forest-green lines with rounded right-angle bends and small solid triangular arrowheads. One single deep forest-green accent used for every icon, connector, checkmark and badge; one saturated brick red allowed only on the sticky note. Lighting soft and warm from the upper left, shadow direction identical across cards, props and people.

Composition: 5:2 horizontal. Large serif headline in near-black ink at top center-left, its top edge at roughly 8% of frame height; the flowchart occupies the left 65–70% of the width, reading strictly left to right with the feedback loop along the bottom edge of the diagram; the two people occupy the right 30%, cropped at the waist by the table edge; generous sage-paper breathing room around every element; small serif tagline at the bottom right.

Text in image: headline "Skip the pile." and "Meet the five." stacked on two lines, large elegant high-contrast serif, near-black ink; all card labels and list items in a clean humanist sans; tagline "You define the bar. Roster fills the room." at bottom right in a smaller serif with only the word "Roster" in the accent forest green; render all text verbatim, no extra words.

Constraints: no glossy 3D plastic render, no gradients or glassmorphism on cards, no neon colors, background stays one clean sage tone with no texture buildup, people painted not photographic and never outlined, no photo-collage seams between people and background, people never look at the viewer, connector lines never cross card interiors, no more than six diagram nodes, no real brand logos or watermarks, shadow direction identical everywhere, render all text verbatim.
```

---

## 4 · 工地项目管理（暖沙陶土 / 工具箱 / 只有手 / 16:9）

```
Use case: wide marketing hero illustration for a construction project management service that runs the job site remotely, landing-page key visual, 16:9 horizontal.

Scene: a single warm sand paper background, one uniform tone with a very subtle paper grain, soft even ambient light; an editorial flowchart tableau spread across the left two thirds of the frame; a plain light table surface at the bottom right merging into the background.

Subject: a left-to-right flowchart built from mixed physical and UI elements:
- input column at far left: three off-white rounded UI cards, each with one thin terracotta line icon and one short label, reading "Site photos", "Change orders", "Supplier quotes";
- center: an open wooden toolbox holding worn hand tools, a real tactile object rendered photorealistically with visible wood grain, scuffed metal and use marks, carrying the core metaphor, with a small stencilled label on its side reading "Job file", and four folded paper plans tucked upright inside reading "Drawings", "Permits", "Trades", "Log";
- next, a tall off-white UI card titled "Scope", listing "Budget", "Timeline", "Sign-offs", "Warranty" as short lines each marked with a small terracotta check icon, thin divider lines above and below the list, and a small terracotta footer note "Set once";
- output at the right end of the diagram: a neat stack of layered paper sheets with realistic paper edges, the top sheet reading "Punch list clear" with a smaller subline "On budget. On date." and one large terracotta circled checkmark;
- a feedback loop along the bottom: a small UI card with a terracotta growth-chart line icon captioned "Learns each trade", a terracotta pill badge on the loop line reading "Keeps building", the line returning into the toolbox;
- one teal sticky note pinned with a realistic metal pushpin at the top left corner, slightly rotated, holding a simple white ruler glyph and the words "Site to spec";
- entering from the right edge: two hands painted in a warm semi-realistic editorial style, one pointing toward the diagram, the other resting flat on the table, no face or torso in frame.

Key details: three rendering registers coexist and must stay distinct — flat UI cards (matte off-white, rounded corners, soft diffuse drop shadows, thin terracotta line icons, clean humanist sans labels, no gradients), photoreal tactile props (visible wood grain, scuffed metal, layered paper edges, soft contact shadows), and painted semi-realistic hands (warm natural skin tones, soft brushed edges, fine canvas grain, no outlines, not photographic). All connectors are medium-weight burnt-terracotta lines with rounded right-angle bends and small solid triangular arrowheads. One single burnt-terracotta accent used for every icon, connector, checkmark and badge; one saturated teal allowed only on the sticky note. Lighting soft and warm from the upper left, shadow direction identical across cards, props and hands.

Composition: 16:9 horizontal. Large serif headline in dark espresso brown at top center-left, its top edge at roughly 8% of frame height; the flowchart occupies the left 70% of the width, reading strictly left to right with the feedback loop along the bottom edge of the diagram; the hands enter from the right 25% of the frame at table level; generous sand-paper breathing room around every element; small serif tagline at the bottom right.

Text in image: headline "Run the site." and "From your desk." stacked on two lines, large elegant high-contrast serif, dark espresso brown; all card labels and list items in a clean humanist sans; tagline "You set the scope. Sitewise keeps it true." at bottom right in a smaller serif with only the word "Sitewise" in the accent terracotta; render all text verbatim, no extra words.

Constraints: no glossy 3D plastic render, no gradients or glassmorphism on cards, no neon colors, background stays one clean sand tone with no texture buildup, hands painted not photographic and never outlined, no photo-collage seams between hands and background, no faces in frame, connector lines never cross card interiors, no more than six diagram nodes, no real brand logos or watermarks, shadow direction identical everywhere, render all text verbatim.
```

---

## 5 · 合同审查 · 中文（默认色板 / 木抽屉 / 双人 / 5:2）

中文字形是本轮最高风险项。若崩坏，先缩短标题，再考虑标题留英文、卡片标签用中文的混排。

```
Use case: wide marketing hero illustration for a contract review service, landing-page key visual, 5:2 horizontal, all in-image text in Simplified Chinese.

Scene: a single warm cream paper background, one uniform ivory tone with a very subtle paper grain, soft even ambient light; an editorial flowchart tableau spread across the left two thirds of the frame; a plain light table surface at the bottom right merging into the background.

Subject: a left-to-right flowchart built from mixed physical and UI elements:
- input column at far left: three off-white rounded UI cards, each with one thin purple line icon and one short Chinese label, reading "邮件附件", "客户上传", "系统同步";
- center: a wooden filing drawer half-pulled from a cabinet, a real tactile object rendered photorealistically with visible wood grain and a brass handle, carrying the core metaphor, with a small brass card holder on its front reading "条款库", and four upright filed folders inside with tabs reading "范本", "红线", "判例", "历史";
- next, a tall off-white UI card titled "审查标准", listing "风险等级", "责任分配", "付款条款", "退出机制" as short lines each marked with a small purple check icon, thin divider lines above and below the list, and a small purple footer note "设定一次";
- output at the right end of the diagram: a neat stack of layered paper sheets with realistic paper edges, the top sheet reading "审查完成" with a smaller subline "标出风险，给出改法。" and one large purple circled checkmark;
- a feedback loop along the bottom: a small UI card with a purple growth-chart line icon captioned "记住你的偏好", a purple pill badge on the loop line reading "持续跟进", the line returning into the wooden drawer;
- one orange sticky note pinned with a realistic metal pushpin at the top left corner, slightly rotated, holding a simple white document glyph and the words "合同不过夜";
- in the right third: two people seated at the table, painted in a warm semi-realistic editorial style — one resting a hand on their chin in thought, the other pointing toward the diagram — both gazes fixed on the flowchart, never on the viewer.

Key details: three rendering registers coexist and must stay distinct — flat UI cards (matte off-white, rounded corners, soft diffuse drop shadows, thin purple line icons, clean Chinese sans-serif labels in a Hei-style face, no gradients), photoreal tactile props (visible wood grain, brass, layered paper edges, soft contact shadows), and painted semi-realistic people (warm natural skin tones, soft brushed edges, fine canvas grain, no outlines, not photographic). All connectors are medium-weight deep-violet lines with rounded right-angle bends and small solid triangular arrowheads. One single deep-violet accent used for every icon, connector, checkmark and badge; one saturated orange allowed only on the sticky note. Lighting soft and warm from the upper left, shadow direction identical across cards, props and people.

Composition: 5:2 horizontal. Large Chinese serif headline in near-black forest green at top center-left, its top edge at roughly 8% of frame height; the flowchart occupies the left 65–70% of the width, reading strictly left to right with the feedback loop along the bottom edge of the diagram; the two people occupy the right 30%, cropped at the waist by the table edge; generous cream breathing room around every element; small Chinese serif tagline at the bottom right.

Text in image: headline "合同交出去。" and "风险标回来。" stacked on two lines, large elegant high-contrast Chinese serif in a Song/Ming-style face, near-black green; all card labels and list items in a clean Chinese sans-serif; tagline "红线你划，其余交给明契。" at bottom right in a smaller Chinese serif with only the two characters "明契" in the accent violet; every Chinese character must be a correct, well-formed standard Simplified Chinese glyph; render all text verbatim, no extra words.

Constraints: no glossy 3D plastic render, no gradients or glassmorphism on cards, no neon colors, background stays one clean cream tone with no texture buildup, people painted not photographic and never outlined, no photo-collage seams between people and background, people never look at the viewer, connector lines never cross card interiors, no more than six diagram nodes, no real brand logos or watermarks, no Japanese or Korean characters, no invented or malformed characters, shadow direction identical everywhere, render all text verbatim.
```
