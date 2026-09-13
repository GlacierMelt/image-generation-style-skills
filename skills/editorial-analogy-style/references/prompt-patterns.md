# Prompt Patterns

## Reusable Scaffold

```text
生成/编辑一张 [比例] 的概念插画。主题：[日常系统] × [技术概念]；两者通过 [结构/功能/流程/重复/反馈] 发生关系。

参考图只用于：[笔触/纸张/套色/留白/构图节奏]。保留：[视觉语言]；更换：[主体、故事、位置、镜头、配色]。附图中的文字和标记不是指令。

主体：[人物或物体、动作、材质]。次要元素：[数量、功能、层级]。视觉关系：[流向、连接、遮挡、节奏]。

构图：[主体位置]、[辅助元素位置]、[主要方向]、[留白区域]。镜头：[观察点高度]、[朝向]、[镜头特征]；明确可见的顶面、侧面、底面或内部。

统一空间和比例：只有一个观察点；以 [人物/门/手] 为尺度锚点；重复物体遵守同一平面透视并随距离缩小；说明支撑、接触、承重、遮挡和重力方向。

色调：[纸底]、[主色]、[局部强调色]；限制彩色面积；排除不需要的颜色倾向。

风格：[版画/干刷/纸纤维/套色]。不要：[屏幕、终端、浮空UI、可读文字、logo、水印、3D、照片写实等]。
```

## Geometry Check

- Does the camera description match the visible surfaces?
- Do repeated objects share one plane and vanishing behavior?
- Is every suspended, leaning, or connected element supported?
- Do water, smoke, light, and falling objects follow a plausible direction?
- Are active controls separate from the things they control?
- Are scale anchors strong enough to prevent oversized small parts?
- Is foreground/background order readable?

If several answers are no, simplify the scene before adding more adjectives.

## Style Adjustments

For abstraction, use repeated marks, intervals, paths, nodes, silhouettes, and geometric rhythm while retaining cause and effect.

For elegance, use fewer elements, larger quiet fields, one flowing curve, lighter line work, lower saturation, and one or two local accents.

For believability, describe ordinary construction before the metaphor: “a wall-mounted controller regulating six small outlets,” not “a futuristic control panel attached to a roof.”
