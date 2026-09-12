---
name: editorial-emotion-control
description: VisualOS 私域视觉处理 Skill。
license: Internal-private
metadata:
  adaptation: VisualOS original distillation
---

# editorial-emotion-control

从眼神、嘴角、泪痕、姿态、光线和画面节奏控制人物情绪，避免夸张表演。来源：GrayNoteLab 公开方法摘要。

## Workflow

1. 识别输入主体、目标平台、风格和保真要求。
2. 提取不可改变的主体特征与可变化的视觉变量。
3. 生成一份主方案，并提供 3 个有明确差异的构图或处理方向。
4. 明确镜头、光线、色彩、材质、动作、文字和负面约束。
5. 检查主体身份、比例、手部、服装、商品细节、文字和风格一致性。
6. 返回可直接用于图像模型的中文提示词；用户要求批量时分别输出独立提示词。

## Provenance

本 Skill 为 VisualOS 私域改写，保留方法来源记录，不代表原作者官方发布。
