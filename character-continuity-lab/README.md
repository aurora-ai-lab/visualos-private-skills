# Open Nuyoah Skill

一组可以公开安装、修改和复用的 Agent Skills。

![白色软块双格漫画 Skill](docs/images/create-white-block-comic-hero.png)

## create-white-block-comic

把一个主题、一段文字或一个故事，转成上下双格的荒诞反差漫画。

它不会附送或静默调用作者的私人角色。第一次使用时，Skill 会先为你建立角色身份；只有你确认后，才会把角色保存为当前项目的可复用角色包。以后换故事，角色不需要重新设计。

### 它能做什么

- 创建并锁定你的白色软块角色
- 把短主题或长内容拆成上下双格漫画
- 维护角色身份、近景锚点和独立情绪资产
- 保存每张正式角色资产对应的完整 Prompt
- 在没有生图工具时退化为可复制的完整 Prompt，不伪造生成结果

### 使用

把 [`skills/create-white-block-comic`](skills/create-white-block-comic) 安装到支持 Agent Skills 的工具中，然后调用：

```text
使用 $create-white-block-comic，为我建立一个白色软块角色，
再把“每次说早点睡，都是为了心安理得地继续熬夜”做成上下双格漫画。
```

角色资产默认保存在当前项目：

```text
.white-block-comic/
├── config.json
└── characters/
    └── your-character/
```

仓库代码与文档使用 [MIT License](LICENSE)。用户输入、模型生成结果和保存在项目里的角色包不属于本仓库内容；请同时遵守所使用模型或服务的条款。
