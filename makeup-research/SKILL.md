---
name: makeup-research
description: 在人物妆容、写真或修图语境下，识别冷白皮、冷白透粉、白里透红、布灵布灵、bling bling、珠光眼妆、眼周细闪、珍珠柔光、裸桃妆、象牙白妆容等目标妆效及近义描述时使用，也适用于分析参考图、提炼妆容与美甲风格、根据反馈迭代 Skill。泛泛生成人像或非妆容物体闪光不触发。有图保留人物换妆，无图创建新成年人物。
---

# 妆容研究

适用于分析参考妆容、提炼可迁移配方、固定人物试妆和对比修正。输出可执行妆面参数与提示词；不把某个人的五官当作妆容，默认采用冷白透粉闪光妆，突出眼周细闪、皮肤光泽与自然锁骨。
## 按妆效意图识别
结合用户目标、修饰对象与上下文判断，不要求固定口令，也不机械匹配单个词。
- 人物妆容、写真或皮肤修图语境中，冷白皮、冷白透粉、白里透红、瓷白底妆、布灵布灵、bling bling、眼周亮晶晶、珠光眼影、细闪妆等表达，以及意思相近的自然描述，可触发本 Skill。
- 用户未重复关键词，但在已有妆容任务中说“再闪一点”“白一点、透一点红”等，沿用该任务识别。
- “布灵布灵”若修饰珠宝、衣服、背景或其他物体，不据此触发妆容流程；泛泛的人像或写真生成请求、单独“突出锁骨”也不触发。否定表达如“不要冷白皮、不要闪片”不作为正向触发信号；若同时有明确妆容任务，则执行该任务并尊重否定约束。
- 识别到目标妆效或用户显式调用本 Skill 后，才使用以下招牌默认值。用户只指定其中某项时，优先该项，其余作为可覆盖默认；用户指定自然肤色或无闪妆时不强加冷白与细闪。

## 触发后的默认行为
- 有人物参考图：以当前明确的人物图为唯一身份参考，保留五官比例、脸型与体型；局部换妆保留原造型，完整风格迁移采用目标发型、眼神、动作和配饰，默认妆面为冷白透粉闪光妆。只给一张清楚人物照时，默认它是身份图；多张人物且身份不明确时才澄清。不将纯服装图或无人场景图当作身份图。
- 无人物参考图：直接生成一位新的成年人物，默认冷白皮与完整招牌妆面，不索要身份图、不沿用之前案例中的人物脸。人物性别表达等未指定项可按当前语境决定。
- 默认妆面：明亮冷乳白底色透淡玫瑰红晕，粉色珠光眼影与银粉色细闪集中眼睑、内眼角及局部下眼缘，水润玫瑰唇；脸颈肩肤色协调，保留皮肤纹理。
- 默认表现：近轴闪光感、主体明亮背景较暗、上半身竖幅 3:4，以脸和眼妆为中心，突出皮肤光泽；画幅和衣着允许时自然展示锁骨，不为此改体型或强改用户指定衣服。
- 仅做局部换妆时保留已有服装、背景和构图；完整风格迁移需读取 [眼神、手势与发型配方](references/style-direction.md)，不固定身份图的造型；完整招牌写真请求或无图生成才使用上述默认摄影场景。按需读取冷白透粉配方。
- 用户明确指定其他肤色、妆容、光线、衣服或比例时，以当轮要求为准。只要求分析或提示词时不擅自生成图片；明确要求生成时应调用可用图像工具，而非只返回提示词。

## 整体造型分析
冷白皮、象牙白及其他妆容都要分析眼神、表情、头肩和手部姿势、耳环、项链、戒指、美甲与发饰。读 [整体造型分析](references/whole-look-review.md)，明确保留或迁移项；换妆默认保留原图动作和配饰，整套造型迁移按用户目标执行。

## 参考图研究与持续迭代
用户要求分析新妆容、美甲、提炼审美或迭代 Skill 时，读取 [参考图学习流程](references/reference-learning.md)。先忠实分析新参考，再沉淀独立配方；不将所有新风格强行改成冷白细闪。妆容侧负责脸部与美甲配方，穿搭侧负责耳环、项链等配饰的造型与佩戴关系；综合参考按重点协作，不重复套用两套完整流程。

## 风格索引
- [玫粉柔雾黑底近景](portrait-aesthetic-skill/references/rose-pink-velvet-closeup.md)：柔雾冷乳白底、眼周微闪、连鼻玫粉腮红与渐层亮唇，含柔淡/浓郁两版；无图生成与一次近景身份参考两宫格获认可，保留参考图适配经验与未验证范围。
- [低饱和玫瑰棕清晰眉眼妆](references/styles/muted-rose-brown-defined-eyes.md)：柔雾底妆、清晰眉眼与低饱和唇颊；保留自然裸桃棕、深邃玫瑰棕、柔粉玫瑰棕、上扬眼线亮唇四版；有身份图完整造型四宫格获用户认可。
- [珍珠柔光裸桃妆](references/styles/pearl-glow-nude-peach.md)：含“象牙白妆容”强化配方；无图生成与固定人物换妆获用户认可，仍需改进人工纹理。
- [冷白透粉闪光妆](portrait-aesthetic-skill/references/porcelain-rose-flash.md)：一次人物编辑获用户认可；跨人物稳定性未验证。新案例按学习流程追加至此。

## 完整造型与神态
用户要求完整造型复现时，妆容、配饰、穿搭、发型整理和神态一起分析，按风格卡执行；眼神拆成视线方向、眼睑开合、头部角度和嘴部状态，不推断真实心理。身份图只固定人物身份、五官比例与体型；已授权的发型、服装、配饰、姿态和视线可以改变，不继续机械套用“只换妆”的保留项。配饰与服装结构按穿搭流程补充，同一案例保留一个主配方，避免复制两套。

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
内含案例保存“固定人物·冷白透粉闪光妆”的完整 Skill 与提示词：亮白底色透淡红、眼周细闪、突出锁骨及皮肤。这是本 Skill 的默认招牌风格；用户明确指定其他效果时覆盖默认。


本地案例入口：[固定人物·冷白透粉闪光妆](portrait-aesthetic-skill/SKILL.md)。
