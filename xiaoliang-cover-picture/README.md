<div align="center">

# Xiaoliang Cover Picture

<strong>科技小亮封面配图 Skill</strong>

<br />

<sub>把技术文章、AI 工具体验、开源项目和产品复盘，转成更适合发布的封面方案。</sub>

<br />
<br />

<kbd>WeChat Cover</kbd>
<kbd>Xiaohongshu Cover</kbd>
<kbd>Creator IP</kbd>
<kbd>Editorial Prompt System</kbd>

<br />
<br />

<a href="#中文">中文</a>
 ·
<a href="#english">English</a>
 ·
<a href="#quick-start">Quick Start</a>
 ·
<a href="#repository-structure">Structure</a>
 ·
<a href="#privacy-boundary">Privacy</a>

</div>

---

<a id="中文"></a>

<details open>
<summary><strong>中文说明</strong></summary>

<br />

## 项目定位

`xiaoliang-cover-picture` 是一个为「科技小亮」个人 IP 设计的 Codex Skill。

它不是普通的 AI 配图提示词，而是一套面向内容发布的封面生产方法：从文章标题、摘要、草稿或 Markdown 中提炼传播钩子，再转化成大标题、人物动作、主题物件、视觉隐喻和平台化构图。

公开仓库只保留可复用的 Skill 源文件。个人 IP 参考图、历史输出图、文章截图、用户草稿、本地脚本和任何私有素材都不会上传。

<a id="quick-start"></a>

## 快速开始

拿到这个仓库后，只需要补一张自己的 IP 参考图，就可以让 Skill 按照固定路径读取。

### 1. 创建本地素材目录

```text
assets/ip-reference/
outputs/covers/
```

### 2. 放入你的 IP 形象图

把自己的参考图放到：

```text
assets/ip-reference/xiaoliang-ip-reference.png
```

推荐使用清晰的正脸或半身图：

| 建议 | 原因 |
| --- | --- |
| 正脸或微侧脸 | 更容易保持人物识别度 |
| 干净背景 | 减少生成时把背景误当作角色特征 |
| 眼镜、发型、服装清楚 | 帮助 Skill 稳定保留 IP 形象 |
| 不要手持手机遮脸 | 避免封面反复生成手机自拍感 |

### 3. 开始使用 Skill

在 Codex 里提出任务时，直接给文章主题或草稿：

```text
使用 xiaoliang-cover-picture，基于这篇文章生成公众号封面和小红书封面。
```

Skill 会优先读取：

```text
assets/ip-reference/xiaoliang-ip-reference.png
```

生成后的封面建议保存在本地：

```text
outputs/covers/
```

这些素材和输出目录只用于本地生产，不需要上传 GitHub。

## 视觉系统

| 模块 | 设计方向 |
| --- | --- |
| 内容类型 | AI 工具、开源项目、产品测评、技术观点、失败复盘、创作者公告 |
| 输出格式 | 公众号 `2.35:1` 横封面、小红书 `3:4` 竖封面 |
| 画面风格 | 干净、真实、有张力、创作者主导、一个核心隐喻 |
| 标题策略 | 中文大标题优先，短句、粗体、缩略图可读 |
| 明确避开 | 浮窗堆叠、代码框、图标拼贴、普通桌面摆拍、泛化网红脸 |

## 为什么需要它

AI 生成封面很容易掉进几个陷阱：

| 常见问题 | Skill 的处理方式 |
| --- | --- |
| 标题太小，缩略图看不清 | 强制 2-4 行大标题，把标题当作视觉主角 |
| 人物不像原 IP | 保留人物识别特征和科技创作者气质 |
| 背景堆满 UI、代码和截图 | 限制为一个核心物件和一个明确动作 |
| 每张图都像同一个模板 | 强制变化姿态、手部动作、镜头角度、场景和光源 |
| 横图竖图只是裁切 | 公众号和小红书分别设计构图 |

## 设计原则

<table>
  <tr>
    <td width="50%"><strong>Title As The Hero</strong><br /><br />标题不是角落里的说明文字，而是封面的主视觉之一。每个标题都应该被压缩成 2-4 行短句，并在手机信息流里保持可读。</td>
    <td width="50%"><strong>One Image, One Hook</strong><br /><br />一张封面只表达一个核心洞察。优先使用一个具体物件和一个明确动作：打开、照亮、拆解、连接、比较、按下按钮、举起结果。</td>
  </tr>
  <tr>
    <td width="50%"><strong>Creator-Led, Not Stock-Led</strong><br /><br />人物需要像真实的科技创作者，而不是广告模特、商务男、网红脸或动漫角色。可以轻微美化，但不能失去自然质感和识别度。</td>
    <td width="50%"><strong>Platform-Specific Composition</strong><br /><br />公众号横图适合左右张力、前景纵深和大块标题区。小红书竖图适合近景人物、更大的标题、更强的瞬间感。</td>
  </tr>
</table>

## 工作流

| Step | Action |
| --- | --- |
| 01 | 读取文章标题、摘要、草稿、Markdown 或主题 |
| 02 | 判断文章类型：AI 教程、产品测评、工具体验、观点分析、趋势解读、失败复盘、硬件制作或创作者公告 |
| 03 | 提炼 2-4 行中文封面标题 |
| 04 | 选择一个核心视觉主体和一个文章隐喻 |
| 05 | 明确人物姿态、手部动作、表情、镜头角度、场景家族和光源 |
| 06 | 分别生成公众号横图和小红书竖图提示词 |
| 07 | 检查标题可读性、人物一致性、画面干净度、平台比例和禁区 |
| 08 | 将生成结果保存到本地输出目录，不提交到公开仓库 |

## 使用示例

```text
使用 xiaoliang-cover-picture，生成公众号封面和小红书封面。

文章主题：
Codex 可以操作 Windows 电脑了。

内容角度：
解释 Computer Use 到底能做什么、普通用户怎么理解它、真实体验中有哪些边界。
```

Skill 应输出：

- 2-4 行封面标题；
- 一个高亮关键词；
- 人物姿态和手部动作；
- 一个核心物件或隐喻；
- 公众号和小红书两套独立构图；
- 避免项和质量检查点。

</details>

---

<a id="english"></a>

<details>
<summary><strong>English</strong></summary>

<br />

## Positioning

`xiaoliang-cover-picture` is a Codex Skill for the 科技小亮 creator IP.

It is not a generic image prompt. It is an editorial cover-production system that turns an article title, outline, draft, or Markdown file into a strong Chinese cover title, a creator-led scene, one core visual object, one memorable metaphor, and platform-specific compositions.

The public repository contains only reusable Skill source files. Private IP references, generated cover outputs, article screenshots, user drafts, local scripts, and private production assets are intentionally excluded.

## Quick Start

After cloning the repository, add your own creator reference image to the local asset path before using the Skill.

### 1. Create local asset folders

```text
assets/ip-reference/
outputs/covers/
```

### 2. Add your IP reference image

Place your reference image here:

```text
assets/ip-reference/xiaoliang-ip-reference.png
```

Recommended reference image:

| Recommendation | Why |
| --- | --- |
| Front-facing or slight side profile | Helps preserve identity |
| Clean background | Prevents background noise from becoming part of the character |
| Clear glasses, hair, and outfit | Stabilizes creator appearance |
| No phone covering the face | Avoids repeated phone-selfie compositions |

### 3. Use the Skill

In Codex, provide an article topic or draft:

```text
Use xiaoliang-cover-picture to generate a WeChat cover and a Xiaohongshu cover.
```

The Skill will first look for:

```text
assets/ip-reference/xiaoliang-ip-reference.png
```

Generated covers should stay local:

```text
outputs/covers/
```

These assets and outputs are production materials, not public repository files.

## Visual System

| Module | Direction |
| --- | --- |
| Content type | AI tools, open-source projects, product reviews, tech opinions, failure reviews, creator announcements |
| Output format | WeChat `2.35:1` wide cover, Xiaohongshu `3:4` vertical cover |
| Visual style | Clean, realistic, high-tension, creator-led, one core metaphor |
| Typography | Large Chinese title first, short lines, bold, readable as a thumbnail |
| Avoid | Floating UI stacks, code boxes, icon collages, flat desk shots, generic influencer faces |

## Why It Exists

AI-generated covers often fail in predictable ways:

| Failure Mode | Skill Response |
| --- | --- |
| Text is too small to read | Compress the title into 2-4 large Chinese lines |
| The person becomes generic | Preserve creator identity and grounded tech temperament |
| The background becomes cluttered | Limit the scene to one object and one action |
| Every cover repeats the same setup | Force variation in pose, hand action, camera angle, scene, and lighting |
| Wide and vertical covers are just crops | Design WeChat and Xiaohongshu compositions separately |

## Design Principles

<table>
  <tr>
    <td width="50%"><strong>Title As The Hero</strong><br /><br />The title is not a small caption. It should function as a primary design object and remain readable in a mobile feed.</td>
    <td width="50%"><strong>One Image, One Hook</strong><br /><br />Each cover should communicate one insight through one object and one action: opening, revealing, lighting, dismantling, connecting, comparing, or pressing a physical button.</td>
  </tr>
  <tr>
    <td width="50%"><strong>Creator-Led, Not Stock-Led</strong><br /><br />The character should feel like a real tech creator, not an ad model, business stock portrait, influencer face, or anime character.</td>
    <td width="50%"><strong>Platform-Specific Composition</strong><br /><br />WeChat needs wide-frame tension and depth. Xiaohongshu needs close framing, larger title text, and stronger moment energy.</td>
  </tr>
</table>

## Workflow

| Step | Action |
| --- | --- |
| 01 | Read the article title, summary, draft, Markdown, or topic |
| 02 | Classify the article type |
| 03 | Rewrite the cover title into 2-4 short Chinese lines |
| 04 | Choose one core visual subject and one metaphor |
| 05 | Define pose, hand action, expression, camera angle, scene family, and lighting |
| 06 | Create separate prompts for WeChat and Xiaohongshu |
| 07 | Check title readability, identity consistency, clean composition, platform ratio, and avoid-list compliance |
| 08 | Save generated images locally only |

## Example Request

```text
Use xiaoliang-cover-picture to generate a WeChat cover and a Xiaohongshu cover.

Article topic:
Codex can now operate a Windows computer.

Angle:
Explain what Computer Use can actually do, how ordinary users should understand it, and where the real-world boundaries are.
```

The Skill should return:

- 2-4 Chinese title lines;
- one highlighted keyword;
- creator pose and hand action;
- one core object or metaphor;
- separate WeChat and Xiaohongshu compositions;
- avoid rules and quality checks.

</details>

---

<a id="repository-structure"></a>

## Repository Structure

```text
.
├─ README.md
├─ SKILL.md
├─ agents/
│  └─ openai.yaml
└─ references/
   ├─ cover-style.md
   ├─ quality-gate.md
   ├─ style-matrix.md
   └─ prompt-patterns.md
```

| File | Role |
| --- | --- |
| `SKILL.md` | Skill entrypoint, workflow, prompt requirements, identity constraints, composition rules, and quality gate. |
| `references/cover-style.md` | Editorial style guide for title, character, scene, color, platform rules, and final review. |
| `references/quality-gate.md` | Acceptance checklist for setup, prompt quality, image review, retries, and final delivery. |
| `references/style-matrix.md` | Article-type, platform, pose, title, and color matrix for more varied cover concepts. |
| `references/prompt-patterns.md` | Article-type prompt patterns for choosing metaphors, actions, and cover structures. |
| `agents/openai.yaml` | Agent display metadata and default prompt. |
| `assets/ip-reference/README.md` | Placeholder showing where to place the default Xiaoliang IP reference image. |
| `assets/references/README.md` | Placeholder for private visual reference boards. |
| `examples/README.md` | Placeholder for private taste calibration examples. |
| `outputs/covers/README.md` | Placeholder showing where generated covers should be saved. |
| `scripts/README.md` | Placeholder for local helper scripts. |

<a id="privacy-boundary"></a>

## Privacy Boundary

> This public repository contains the reusable Skill source and folder placeholders only.

Do not upload:

- personal IP reference photos;
- generated cover images;
- user articles, drafts, screenshots, or private outputs;
- local temporary scripts;
- files containing personal paths or private source material;
- example images derived from private production work.

For local production, keep private assets inside the tracked placeholder folders:

```text
assets/ip-reference/
examples/
outputs/covers/
scripts/
```

The README files in those folders are tracked so new users know where to place files. The actual images, generated outputs, and local scripts remain ignored by Git.

## Roadmap

| Item | Purpose |
| --- | --- |
| `quality-gate.md` | Turn title, ratio, identity, composition, and privacy checks into a deterministic review list. |
| `style-matrix.md` | Provide stronger scene, action, and object combinations for different article types. |
| Private toolchain | Convert one-off local scripts into reusable private production tools. |
| Private reference board | Maintain positive and negative examples for long-term style consistency. |

## License

This repository is maintained as a personal Codex Skill workflow. A formal license can be added when the public reuse policy is finalized.
