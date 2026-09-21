<div align="center">

# AUR

### Reusable AI skills for visual creation, interface design, and web motion.

视觉创作 · Agent 技能 · 界面动效

[![Documentation check](https://github.com/aurora9986/visualos-private-skills/actions/workflows/docs-check.yml/badge.svg)](https://github.com/aurora9986/visualos-private-skills/actions/workflows/docs-check.yml)
[![20 skills](https://img.shields.io/badge/skills-20-7657ff?style=flat-square)](CATALOG.md)
[![Topics](https://img.shields.io/badge/focus-AI%20%2B%20visual%20systems-111827?style=flat-square)](CATALOG.md)

</div>

AUR 把视觉创作和界面动效的方法整理成可安装、可调用、可复用的 AI Agent 技能。

A personal library of reusable skills for turning references, ideas, and interaction goals into clear visual direction and implementation guidance.

## Explore AUR

| 方向 | 你可以用它做什么 | 从这里开始 |
| --- | --- | --- |
| **Reference → Prompt** | 拆解构图、色彩、光线和材质，生成可复用提示词 | [Reference Image Analysis](visual-reference-decoder/USAGE.md) |
| **Portrait & Editorial** | 规划写真分镜、人物情绪、姿态和摄影语言 | [Portrait Direction](portrait-scene-director/USAGE.md) |
| **Poster & Zine** | 制作纸感海报、照片拼贴和编辑式视觉方案 | [Paper Posters](paper-editorial-maker/USAGE.md) · [Zine](photo-zine-composer/USAGE.md) |
| **Visual Systems** | 统一系列风格，组织批量提示词和视觉变化 | [Batch Prompts](prompt-batch-conductor/USAGE.md) |
| **Motion & UI** | 把交互想法转成触发器、时间、缓动和 GSAP 实现 | [Motion Direction](ui-gpt-skil/USAGE.md) · [GSAP](gsap-skills/gsap-core/USAGE.md) |
| **Apple-inspired UI** | 依据 Apple HIG 组织层级、导航、组件和无障碍体验 | [Apple Design](apple-design/SKILL.md) |

## Quick start

1. 打开 [技能目录](CATALOG.md)，选择一个与你的任务匹配的入口。
2. 阅读对应的 `USAGE.md` 和 `SKILL.md`，确认安装方式与调用名。
3. 在已安装该技能的 Agent 中提供素材、目标和约束。

```text
$nuyoah-image-reverse-prompt
拆解这张参考图的构图、色彩、光线和材质，输出可复用的中文提示词。
```

```text
$zine
保留照片主体，制作纸张质感的杂志拼贴海报，采用大留白和一处强调色。
```

```text
$ui-gpt-skil
为这个页面设计入场和按钮反馈动效，说明触发条件、时长，并考虑减少动态效果的偏好。
```

> 调用名以各目录 `SKILL.md` 的 `name` 为准。技能文件本身不包含模型、API 服务或凭证；图片生成需要当前 Agent 提供相应工具。

## Library map

- **VisualOS**：10 个视觉创作技能，覆盖参考图、人像、海报、Zine 和系列提示词。
- **UI GPT SKIL**：动效设计入口，以及 `gsap-skills/` 下的 8 个 GSAP 技能。
- **Apple Design**：基于 Apple 官方 Human Interface Guidelines 的界面设计指导。
- **Archive**：`character-continuity-lab/` 目前是资料归档，缺少 `SKILL.md`，暂不可调用。

当前共有 **20 个技能入口**。完整用途、目录和调用名见 [CATALOG.md](CATALOG.md)。

## Contributing

想修正文档、补充示例或添加技能？请先阅读 [CONTRIBUTING.md](CONTRIBUTING.md)，并在提交前运行仓库的文档检查。安全问题请查看 [SECURITY.md](SECURITY.md)。

## Attribution & licensing

AUR 是个人整理与适配的技能集合。各目录可能有不同的来源、许可证和使用限制，请在使用或再分发前阅读对应文件。

- GSAP 技能来自 [greensock/gsap-skills](https://github.com/greensock/gsap-skills)。
- VisualOS 适配技能在各自的 `Provenance` 部分记录来源。
- Apple Design 参考 [Apple Design](https://developer.apple.com/design/)，其技能文件标注为 `Internal-use`。
- 详细说明见 [LICENSE.md](LICENSE.md)。

## Changelog

查看 [CHANGELOG.md](CHANGELOG.md) 了解项目变化。

