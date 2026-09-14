---
name: ui-gpt-skil
description: 用自然语言为网页设计和实现可执行的 UI 动效。当用户要求网页动效、交互反馈、页面转场或 Vibe Coding 动效描述时使用。
---

# UI GPT SKIL

将模糊的“高级动效”需求拆成四层：

1. **技术工具**：优先检查现有技术栈；简单效果用 CSS，React 用 Motion，复杂时间线或滚动叙事用 GSAP。
2. **触发方式**：明确是 Hover、Focus、Click、Pointer、In view、Scroll-linked、Gesture、Route、State change、Timer/Idle。
3. **动效类型**：明确 Fade、Crossfade、Slide、Scale、Blur reveal、Clip-path reveal、Mask reveal、Wipe、Text/Line/Word reveal 等。
4. **UX 边界**：说明结束状态、快速重复操作、键盘与触屏替代方案，以及 prefers-reduced-motion 下的静态降级。

写提示词或实现时，必须交代：谁触发、何时开始、元素如何变化、何时结束或复位。动效要服务层级和反馈，正文保持可读，避免整页同节奏淡入、逐字播放长文或无意义弹跳。

常用表达：
- 首屏主标题按行显现（Line reveal），说明文字短暂延迟后淡入，卡片按阅读顺序 Stagger。
- 卡片进入视口后播放一次，返回滚动时保持最终状态。
- 按钮 Hover 时轻微抬升，Focus 保留清晰可见的键盘轮廓，触屏关闭指针跟随。
- 页面转场使用 Wipe 或 Crossfade；快速切换时取消未完成动画，不阻塞导航。

需要完整词典、参数建议和更多示例时，读取 `references/vibe-motion-dictionary.md`。
