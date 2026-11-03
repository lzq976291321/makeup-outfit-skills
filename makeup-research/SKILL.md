---
name: makeup-research
description: 用户要求生成一张人像或写真、参考图换妆及妆容研究时使用。有图保留人物换妆，无图生成新成年人物；默认冷白透粉、眼周细闪与皮肤光泽。
---

# 妆容研究

适用于分析参考妆容、提炼可迁移配方、固定人物试妆和对比修正。输出可执行妆面参数与提示词；不把某个人的五官当作妆容，默认采用冷白透粉闪光妆，突出眼周细闪、皮肤光泽与自然锁骨。
## 默认人像生成
用户说“生成一张人像”“来张写真”等泛指人像生成时即可使用本 Skill，不必再次要求用户指定妆容。
- 有人物参考图：以当前明确的人物图为唯一身份参考，保留五官比例、脸型、发型和体型，默认换成冷白透粉闪光妆。只给一张清楚人物照时，默认它是身份图；多张人物且身份不明确时才澄清。不将纯服装图或无人场景图当作身份图。
- 无人物参考图：直接生成一位新的成年人物，默认冷白皮与完整招牌妆面，不索要身份图、不沿用之前案例中的人物脸。人物性别表达等未指定项可按当前语境决定。
- 默认妆面：明亮冷乳白底色透淡玫瑰红晕，粉色珠光眼影与银粉色细闪集中眼睑、内眼角及局部下眼缘，水润玫瑰唇；脸颈肩肤色协调，保留皮肤纹理。
- 默认表现：近轴闪光感、主体明亮背景较暗、上半身竖幅 3:4，以脸和眼妆为中心，突出皮肤光泽；画幅和衣着允许时自然展示锁骨，不为此改体型或强改用户指定衣服。
- 有图换妆时优先保留已有服装、背景和构图；完整招牌写真请求或无图生成才使用上述默认摄影场景。按需读取冷白透粉配方。
- 用户明确指定其他肤色、妆容、光线、衣服或比例时，以当轮要求为准。只要求分析或提示词时不擅自生成图片；明确要求生成时应调用可用图像工具，而非只返回提示词。

## 输入与边界
明确身份图、妆容图、目标强度与任务（分析、生成或编辑）。身份图负责五官，妆容图负责色彩与表面反射。没有身份图时只做妆容方案或新人物；看不到图片时不得声称已分析。不自动改服装、体型、发型或背景，除非用户要求或为露出妆面作必要调整。
## 研究流程
1. 先观察底色、明度分区、遮盖度、眼妆、眉、腮红、唇、局部高光和皮肤纹理。区分可见效果与灯光/后期推断，不猜化妆品品牌。
2. 写出位置、范围、边界、颜色、反射形态与强度。区分珠光的连续柔亮、细闪的离散亮点和唇釉的湿润反射；不要只写“高级、通透、漂亮”。
3. 分离妆容与照明：检查白是否来自底妆或曝光，红是否受环境色影响。灯位未知时给复现假设，不当成事实。
4. 按身份图的眼睑、眉骨、颧骨和唇形适配妆面，不缩鼻、削脸或放大眼睛。默认呈现冷白底色，用户明确要求保留原肤色或其他妆容时覆盖默认，脸颈肩保持协调。
5. 先建立底色与红晕关系，再安排眼唇重点，最后调细闪和高光。只要求分析时不执行生成；要求试妆时使用当前可用图像工具。
6. 对照检查身份、妆面位置、颜色、纹理和曝光，每轮只改一组主要变量。已满意图优先局部编辑，复查非目标区域是否漂移。
## 参数卡
```yaml
identity_source: 当前人物参考图；无图则新成年人物
makeup_source: 参考图或文字
base: 冷乳白透粉，保留细纹理（默认）
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
[WITH A PERSON REFERENCE: Use it as the sole source of facial identity. WITHOUT ONE: Create a new adult person with cool porcelain-fair skin.] Preserve facial anatomy and recognizable individual features. Apply [BASE], with [BLUSH PLACEMENT AND EDGE]. Shape [EYE MAKEUP] to the existing eyelids, add [SPARKLE SIZE, DENSITY AND LOCATION], and finish with [LIP COLOR AND SHEEN]. Use [LIGHTING] to reveal [SELECTIVE HIGHLIGHTS] while retaining skin texture and tonal detail. Keep [UNCHANGED ELEMENTS]. Avoid identity drift, clipped highlights, waxy skin and misplaced glitter.
```
## 无图生成示例
```text
Create one photographic upper-body portrait of a new adult person with luminous cool porcelain-fair skin. Apply a bright milky-ivory base with translucent rose blush, pink pearlescent eyelids and crisp fine silver-pink twinkles around the eyelids and inner corners. Glossy rose lips, visible fine skin texture, consistent face-neck-shoulder finish. Near-axis flash against a dim neutral background. Vertical 3:4 framing; naturally visible collarbones where clothing allows. Preserve natural anatomy and controlled highlight detail.
```

## 验收与沉淀
检查五官比例未改、睫毛眼睑仍清楚、细闪未糊成颗粒、腮红边界自然、脸颈无突兀色差、反光有主次。交付观察、配方、提示词、实际结果与待改项。没有实际图片不写“已验收”。新案例记录适用范围、参数、用户反馈和未验证范围；用户认可的强妆感不被助手擅自淡化。
## 已有案例
下方子页面保存“固定人物·冷白透粉闪光妆”的完整 Skill 与提示词：亮白底色透淡红、眼周细闪、突出锁骨及皮肤。这是本 Skill 的默认招牌风格；用户明确指定其他效果时覆盖默认。


本地案例入口：[固定人物·冷白透粉闪光妆](portrait-aesthetic-skill/SKILL.md)。
