# Image Generation Style Skills

## 中文

一个持续扩展的生图风格 skill 集合，面向图片和视频生成工作流。每个 skill 都将一种视觉参考或摄影语言整理成可复用的提示词塑形层，可以与下游生成工具组合使用。

### 当前包含的风格

- [`iphone-computational-photography`](skills/iphone-computational-photography/SKILL.md) — 用于静态图片和视频的高端、真实 iPhone 计算摄影风格。
- [`editorial-analogy-style`](skills/editorial-analogy-style/SKILL.md) — 用于将日常系统与科技隐喻结合的克制木刻版画 / 编辑插画风格。

### 仓库结构

```text
skills/
  <skill-name>/
    SKILL.md                 # 必需：skill 说明与输出约定
    references/              # 可选：结构化输出或媒介专项说明
    examples/                # 可选：提示词示例
    assets/                  # 可选：本地参考素材

templates/
  SKILL.template.md          # 新建风格 skill 的起始模板
```

### 新增风格 skill

1. 将 `templates/SKILL.template.md` 复制为 `skills/<kebab-case-name>/SKILL.md`。
2. 为 skill 定义清晰的适用范围和可复用输出约定。
3. 除非该风格有明确要求，否则不要在风格 skill 中决定下游模型、凭证、尺寸、时长或画面比例。
4. 将结构化输出约定或媒介专项细节放入 `references/`，并从 `SKILL.md` 建立链接。
5. 将新 skill 加入上面的列表，并检查 skill 目录下的相对链接。

### 设计原则

- 保留用户明确指定的主体、场景、情绪和交付约束。
- 让风格层可以复用于图片和视频生成工作流。
- 使用具体的视觉控制，少用空泛的审美形容词。
- 仅在确实能减少模型偏移时加入实用的负面约束。
- 不要在 skill 中放置 API key、中继地址或服务商凭证。

### 许可证

除非文件另有说明，本仓库使用 MIT License。详见 [LICENSE](LICENSE)。

---

## English

A growing collection of reusable visual-style skills for image and video generation. Each skill turns a visual reference or photographic language into a portable prompt-shaping layer that can be combined with downstream generation tools.

### Included skills

- [`iphone-computational-photography`](skills/iphone-computational-photography/SKILL.md) — a realistic, high-end iPhone computational-photography treatment for still images and video.
- [`editorial-analogy-style`](skills/editorial-analogy-style/SKILL.md) — a restrained woodcut/editorial treatment for conceptual scenes that combine everyday systems with technology analogies.

### Repository layout

```text
skills/
  <skill-name>/
    SKILL.md                 # required skill instructions and output contract
    references/              # optional structured-output or medium-specific guidance
    examples/                # optional prompt examples
    assets/                  # optional local reference assets

templates/
  SKILL.template.md          # starting point for a new style skill
```

### Adding a new style skill

1. Copy `templates/SKILL.template.md` into `skills/<kebab-case-name>/SKILL.md`.
2. Give the skill a focused scope and a reusable output contract.
3. Keep downstream model, credential, size, duration, and aspect-ratio decisions outside the style skill unless the style explicitly requires them.
4. Put structured contracts or medium-specific details in `references/` and link to them from `SKILL.md`.
5. Add the skill to the list above and verify all relative links from the skill directory.

### Design principles

- Preserve the user's explicit subject, setting, mood, and delivery constraints.
- Make the style portable across image and video generation workflows.
- Prefer concrete visual controls over vague aesthetic adjectives.
- Include practical negatives only when they help prevent predictable model drift.
- Never place API keys, relay URLs, or provider credentials in a skill.

### License

Unless a future file states otherwise, the repository is released under the MIT License. See [LICENSE](LICENSE).
