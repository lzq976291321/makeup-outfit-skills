---
name: makeup-research
description: 研究参考妆容、提炼配方、固定人物试妆与检查妆面迁移。
---

# 妆容研究

适用于分析参考妆容、提炼可迁移配方、固定人物试妆和对比修正。输出可执行妆面参数与提示词；不把某个人的五官当作妆容，也不默认所有风格都要冷白皮。
## 输入与边界
明确身份图、妆容图、目标强度与任务（分析、生成或编辑）。身份图负责五官，妆容图负责色彩与表面反射。没有身份图时只做妆容方案或新人物；看不到图片时不得声称已分析。不自动改服装、体型、发型或背景，除非用户要求或为露出妆面作必要调整。
## 研究流程
1. 先观察底色、明度分区、遮盖度、眼妆、眉、腮红、唇、局部高光和皮肤纹理。区分可见效果与灯光/后期推断，不猜化妆品品牌。
2. 写出位置、范围、边界、颜色、反射形态与强度。区分珠光的连续柔亮、细闪的离散亮点和唇釉的湿润反射；不要只写“高级、通透、漂亮”。
3. 分离妆容与照明：检查白是否来自底妆或曝光，红是否受环境色影响。灯位未知时给复现假设，不当成事实。
4. 按身份图的眼睑、眉骨、颧骨和唇形适配妆面，不缩鼻、削脸或放大眼睛。提亮肤色只有用户选择时启用，脸颈肩保持协调。
5. 先建立底色与红晕关系，再安排眼唇重点，最后调细闪和高光。只要求分析时不执行生成；要求试妆时使用当前可用图像工具。
6. 对照检查身份、妆面位置、颜色、纹理和曝光，每轮只改一组主要变量。已满意图优先局部编辑，复查非目标区域是否漂移。
## 参数卡
```yaml
identity_source: 用户指定身份图
makeup_source: 参考图或文字
base: 明度、冷暖、遮盖度、质地
brows: 颜色、形状、毛流
eyes: 眼影色、范围、眼线、睫毛
blush: 颜色、位置、范围、边界
lips: 颜色、饱和度、轮廓、湿润度
sparkle: 粒径、密度、位置
highlights: 位置、面积、强度
skin_texture: 保留程度
lighting: 光线假设与目标
must_keep: 身份、发型、服装及构图中需保留项
```
## 提示词模板
```text
Use the supplied identity reference as the sole source of facial identity. Preserve facial anatomy and recognizable individual features. Apply [BASE], with [BLUSH PLACEMENT AND EDGE]. Shape [EYE MAKEUP] to the existing eyelids, add [SPARKLE SIZE, DENSITY AND LOCATION], and finish with [LIP COLOR AND SHEEN]. Use [LIGHTING] to reveal [SELECTIVE HIGHLIGHTS] while retaining skin texture and tonal detail. Keep [UNCHANGED ELEMENTS]. Avoid identity drift, clipped highlights, waxy skin and misplaced glitter.
```
## 验收与沉淀
检查五官比例未改、睫毛眼睑仍清楚、细闪未糊成颗粒、腮红边界自然、脸颈无突兀色差、反光有主次。交付观察、配方、提示词、实际结果与待改项。没有实际图片不写“已验收”。新案例记录适用范围、参数、用户反馈和未验证范围；用户认可的强妆感不被助手擅自淡化。
## 已有案例
下方子页面保存“固定人物·冷白透粉闪光妆”的完整 Skill 与提示词：亮白底色透淡红、眼周细闪、突出锁骨及皮肤。这是可选风格，不是通用肤色标准。


本地案例入口：[固定人物·冷白透粉闪光妆](portrait-aesthetic-skill/SKILL.md)。
