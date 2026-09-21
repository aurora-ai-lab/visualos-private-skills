# VisualOS Skills Library

[![Documentation check](https://github.com/aurora9986/visualos-private-skills/actions/workflows/docs-check.yml/badge.svg)](https://github.com/aurora9986/visualos-private-skills/actions/workflows/docs-check.yml)
[![Skills](https://img.shields.io/badge/skills-20-6d5dfc)](CATALOG.md)
[![License](https://img.shields.io/badge/license-see%20individual%20folders-lightgrey)](LICENSE.md)

把视觉创作与界面动效的方法，整理成 AI Agent 可以复用的技能。

A personal collection of skills for visual creation, interface design, and web motion.

[完整目录](CATALOG.md) · [参考图拆解](visual-reference-decoder/USAGE.md) · [照片 Zine](photo-zine-composer/USAGE.md) · [界面动效](ui-gpt-skil/USAGE.md)

## 可以用来做什么

| 方向 | 适合的任务 | 入口 |
| --- | --- | --- |
| 参考图与人像 | 拆解构图、色彩、材质，规划写真场景和摄影提示词 | [参考图分析](visual-reference-decoder/USAGE.md) / [人像摄影](portrait-scene-director/USAGE.md) |
| 海报与 Zine | 组织纸感海报、照片拼贴、杂志式版面与视觉风格 | [纸感海报](paper-editorial-maker/USAGE.md) / [Zine](photo-zine-composer/USAGE.md) |
| 系列视觉创作 | 规划多组视觉方向，控制表情、风格与批量提示词 | [批量提示词](prompt-batch-conductor/USAGE.md) / [情绪控制](editorial-emotion-control/USAGE.md) |
| 网页动效 | 将自然语言需求转成动效设计，并用 GSAP 实现 | [动效设计](ui-gpt-skil/USAGE.md) / [GSAP Core](gsap-skills/gsap-core/USAGE.md) |
| Apple 风格界面 | 依据官方 HIG 组织导航、层级、组件与无障碍体验 | [Apple Design](apple-design/SKILL.md) |

## 快速开始

1. 从上方选择任务，阅读对应的使用说明和技能文件。
2. 按所用 Agent 的技能安装方式，安装目标技能目录及其附属文件。GSAP 的各个技能位于 `gsap-skills/` 的子目录中。
3. 确认技能已被 Agent 识别，再提供素材、目标和约束，并调用技能。

以下为技能已在 Codex 中可用后的调用示例：

**分析参考图** — 附上图片后输入：

```text
$nuyoah-image-reverse-prompt 拆解这张图的构图、色彩、光线和材质，输出可复用的中文提示词。
```

**制作照片 Zine** — 附上照片后输入：

```text
$zine 保留照片主体，制作纸张质感的杂志拼贴海报，采用大留白和一处强调色。
```

**设计网页动效** — 提供页面或相关代码后输入：

```text
$ui-gpt-skil 为这个页面设计入场和按钮反馈动效，说明触发条件、时长，并考虑减少动态效果的偏好。
```

调用名以 `SKILL.md` 中的 `name` 为准，可能与目录名不同。图片生成需要当前环境提供生图工具；这些技能文件本身不包含模型或 API 服务。

## 仓库结构与状态

- **VisualOS**：10 个视觉创作技能，位于各自的顶层目录。
- **UI GPT SKIL**：1 个动效设计技能，以及 `gsap-skills/` 下的 8 个 GSAP 技能。
- **Apple Design**：1 个基于 Apple 官方设计指导的技能。
- **资料归档**：`character-continuity-lab/` 目前只有说明资料，缺少 `SKILL.md`，尚不可调用。

当前共有 **20 个技能入口**。详细用途、目录和准确调用名见 [CATALOG.md](CATALOG.md)。

## 参与改进

发现调用名不一致、文档缺失或使用问题？请先阅读 [贡献指南](CONTRIBUTING.md)，再提交 [Issue](https://github.com/aurora9986/visualos-private-skills/issues)。

## 来源与使用说明

这是个人整理与适配的技能集合。目录分组不替代原作者署名，各目录保留原有说明与许可；使用或再分发前，请查看对应文件。

- GSAP 技能来自 [greensock/gsap-skills](https://github.com/greensock/gsap-skills)。
- VisualOS 中的适配技能在各自的 `Provenance` 部分记录来源。
- Apple Design 参考 [Apple Design](https://developer.apple.com/design/)，其技能文件标注为 `Internal-use`。
- 许可范围和第三方来源见 [LICENSE.md](LICENSE.md)。

## 变更

查看 [CHANGELOG.md](CHANGELOG.md) 了解版本记录。
