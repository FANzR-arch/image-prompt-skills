# 编译契约（消歧义铁律）

每次输出前必须满足。这是「成品」和「拼装件」的分界：成品不留任何选项、菜单、占位符。

## 7 条铁律

1. **每个槽位解析成唯一值**。删掉所有 `/` 选项和 `<>` 占位。成品里不允许出现 `a cord / a lever / a thread` 这类菜单。
2. **正文零中文**。提示词正文只能出现英文美术指导；唯一例外是要渲染进画面的文字。任何中文注释一律不留——模型会把它画进画面。
3. **必须有且只有一件主连接物**。第二条连接线会把关系读乱。装饰性的线（裁切线、色条）不算连接物。
4. **否定只进 Constraints 段**。正文用正向描述，所有 `no / never` 收进末尾。**不允许输出独立的 `Negative prompt:` 块**——目标模型没有 negative 通道。
5. **锐点必须点名**。Key details 里要出现 `keep A, B and C sharp`，A/B/C 是这张图里具体的尖端与硬转折，不写泛指。
6. **占比必须给数字**。Composition 里主体的横向区间、纵向区间和旋转角度都用百分比和度数写死，不写 `left side`、`slightly tilted`。
7. **文字必带 verbatim 条款**，并明写画面里其余印刷内容是不可读的占位纹理。

## 锁死的风格基座（LOCKED，每条必带）

无论什么主题、哪个色寄存器，下面两段逐字照抄，只替换 `{{}}` 变量（取值见 `module-library.md`）。

**Key details 基座**

```
Mid-century print-shop collage. Every physical object is a photograph reproduced as a coarse
visible duotone halftone — a black dot screen plus a second spot-colour dot screen offset by
one or two pixels, so the misregistration is legible at full size. Each object is then die-cut
with a crisp 3px white sticker outline and a faint hard drop shadow. Edges stay razor sharp and
are never eroded by the texture; keep {{SHARP_POINTS}} sharp. The halftone dots appear only on
the cut-out objects and paper scraps — the flat colour field behind them carries no dots.
Paper-fibre grain covers the whole image. Colour architecture: {{GROUND}} as the ground, pulp
off-white and kraft as the neutral paper layer, {{SPOT}} as the single spot colour reserved for
{{CONNECTOR}} and the second halftone plate, {{METAL}} for the metal instruments, black for
geometric marks and the label block.
```

`{{SHARP_POINTS}}` 至少三项，用这张图里真实存在的部位名，例如 `the spike's needle point, the torn holes in the old receipts and the clean sheet's four corners`。

**Constraints 基座**

```
no gradients, no glow, no 3D rendering, no vector illustration look, no soft or feathered edges,
no halftone dots over the flat background field, no tin robots, no globes, no watering cans,
no CRT computers, no cartoon faces, no readable text beyond the specified strings, preserve the
visible dot pattern and the plate offset at 100% zoom.
```

基座后面**追加**主体相关的排除项，不替换基座。追加项守 2–5 条，例如：

- 堆积类主体：`no legible letters on the type sorts`
- 数量必须锁死时：`no more than three red marks anywhere in the frame`
- 成组产出时：把上一张用过的器物按名追加，例如 `no proof press, no folded maps`

**负向项总数守 8–14 条。**已验证有效的提示词不要剪——实测反证：一条正常工作的提示词把负向项大幅削减后成图直接畸形。确需剪时一次只剪一条并验证。

## 固定字段顺序

成品提示词永远按此七段输出，带段落标签：

```
Use case → Scene → Subject → Key details → Composition → Text in image → Constraints
```

## 成品骨架（填好即发，无占位符）

```text
Use case: <wide article cover banner | in-article section illustration>.

Scene: A flat {{GROUND}} background arranged like <一个具体的工作面：inspection bench /
compositor's bench / proofreader's desk / shop counter> — torn pulp-paper strips, crop marks at
the corners, <从装饰表取 2–3 件>.

Subject: <主物件：一件有内部结构的工坊器物，带状态或动作>, rendered as a coarse duotone
halftone cut-out<, 姿态或倾斜>. <一到两个配角物件，各自写清落在什么面上>. <连接物：写清从哪里
出发、经过哪里、终止在哪里>.

Key details: <Key details 基座，填入 SHARP_POINTS / GROUND / SPOT / CONNECTOR / METAL>

Composition: <5:2 ultra-wide | 16:9> horizontal. <主物件占 A%–B% of the width, C%–D% of the
height, rotated about N degrees>. <配角与连接物的位置区间>. The label block sits at the
<lower right | lower left>.

Text in image: <器物上的印刷文字：数字、刻度、等宽标签或印章大写，各自写清印在哪件东西上>.
<不可读的部分：carries smudged illegible lines only / carries no readable letters>. At the
<corner>, white heavy Chinese sans-serif inside a solid black rectangle with a {{SPOT}} vertical
bar along its left edge and a clipped upper-right corner: "<标签，2–4 字>". Render all text
verbatim, no extra words.

Constraints: <Constraints 基座逐字照抄><追加 2–5 条主体相关排除项>
```

## 封面骨架的两处差异

5:2 封面与 16:9 章节图共用同一套基座，只有两处不同：

1. **层压**：封面必须有一件剪贴物的一角**压在标题块上**并投下硬纸影。这是封面区别于章节图的手法，也是它显得是"排出来的"而不是"摆出来的"原因。写法：

```
its torn right corner lifts off the table and overlaps the headline block, casting a hard paper
shadow on it
```

2. **文字层级**：封面是四层——kicker 小条 / 超大主标 / 次行副标 / 底部小字长句。章节图只有一个标签块（加器物上的零星印刷字）。

封面四层的固定写法：

```
Text in image: On a pulp off-white torn block, very large heavy geometric sans-serif Chinese in
black: "<主标>". Directly beneath, on a narrower kraft strip, medium-weight black Chinese:
"<副标>". Above the headline, small white Chinese inside a thin {{SPOT}} bar: "<kicker>". Along
the lower <right|left>, small white Chinese on a black bar: "<底部长句>". Render all text
verbatim, no extra words.
```

## 出图参数（不进正文）

| 交付物 | size | quality |
|---|---|---|
| 5:2 封面 | `3840×1536` | high |
| 16:9 章节图 | `3840×2160` | high |

参数层信息绝不写进提示词正文。

## 迭代纪律

- **一次只改一处**。质感四维互相联动，凭措辞的字面语义猜因果已实测出过错。
- **质感例外**：修质感整段重写，不逐词补丁。
- **效果不对时先删修饰再加修饰**。修饰词过多会互相竞争。
- **双色套印是可拆的一维**：整张糊掉时先把 `plus a second spot-colour dot screen offset by one or two pixels` 单独删掉验证，退回单色黑网点仍是合法的良好版本。
- **背景长网点的降级路径**：把 `the flat colour field behind them carries no dots` 从 Key details 中段提到段首，并在 Scene 段末尾追加一句 `the background field itself is perfectly flat and untextured`。
- **堆积主体糊成纹理时减数量，不加修饰**。三十枚减到十二枚比补五个形容词有效。
- 措辞已到天花板时换工具：编辑模式定点改（`Change only X. Keep everything else exactly the same.`）、同提示词多抽几张再选。
