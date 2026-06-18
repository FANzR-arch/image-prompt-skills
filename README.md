# Image Prompt Skills

一组可复制、可安装、可持续更新的 AI 生图提示词 Skills。

## Skills

| Skill | 用途 | 文章复制版 |
| --- | --- | --- |
| [travel-postcard-agent](https://github.com/FANzR-arch/image-prompt-skills/tree/main/travel-postcard-agent) | 根据城市、节日、季节或特殊主题生成现代旅行拼贴明信片提示词 | [ARTICLE-COPY.md](travel-postcard-agent/ARTICLE-COPY.md) |

## 使用方式

### 直接复制给 AI

打开对应 Skill 目录中的 `ARTICLE-COPY.md`，复制全部内容发送给 AI，然后输入城市或主题。

例如：

```text
杭州 中秋
```

### 作为 Agent Skill 安装

支持 Agent Skills 的工具可以使用包含 `SKILL.md` 的完整目录。`references/` 存放按需读取的参考资料，`evals/` 存放测试用例。

## 目录约定

```text
image-prompt-skills/
├── README.md
└── skill-name/
    ├── SKILL.md
    ├── ARTICLE-COPY.md
    ├── references/
    └── evals/
```

每个 Skill 同时维护两个版本：

- `SKILL.md`：适合支持 Agent Skills 的工具；
- `ARTICLE-COPY.md`：单文件、自包含，适合放进文章供读者复制。

## 当前状态

仓库处于持续整理阶段，后续会增加更多生图提示词 Skills。
