# 玫粉柔雾黑底近景：已认可变体

## 范围与验证状态
冷白透粉闪光妆的可选变体，不替换默认配方。用于冷乳白柔雾底妆、连鼻玫粉腮红、眼周银粉细闪与亮泽玫粉唇。黑背景、方形近景、触唇手势和服装为案例造型，可按用户要求替换。

2026-11-04：用户对原提示词第一版反馈“感觉不错”，要求稍微修饰再评估沉淀。内置 imagegen 编辑第一版后，助手观察连鼻腮红和唇中央色差更清楚，肤质与眼周细闪基本保留；向画面左侧转脸仍不明显。用户随后认为两版各有感觉。后续两张身份参考均进行了两宫格试妆：餐厅参考的结果被反馈为“整体感觉很好但是妆容没有把人画的更好看一些”；换用近景参考后，最终两宫格获“好好看”确认，并明确要求沉淀。说明无图生成与这张近景身份图的迁移得到认可；不代表任意人物、任意参考或独立重复生成都稳定。未提供具体模型版本或 seed。

## 配方
- 冷乳白柔雾绒感底妆，保留毛孔与细纹理，仅鼻尖、颧骨顶部有小面积受控高光。
- 高位眼下玫粉腮红透明、柔边，明确横跨鼻梁连接双颊，避免不透明横条。
- 玫粉眼影包围眼周，外眼角与下眼睑略深。银粉微闪限于上眼睑、内眼角、双侧下睫毛缘与卧蚕，不散落面颊。
- 唇中央略深，向边缘柔和渐淡。嘴唇为连续湿润反射，眼周保留局部珠光与离散亮点。
- 近轴柔闪、黑背景，脸为主视觉、手为次要；指尖停在下唇外缘，不穿插。

## 原提示词的最小修订片段
保留用户原提示词的其他内容，仅替换相应描述；以下整合写法尚未独立生成复测。
```text
Cool milky-ivory soft-matte velvety base with fine visible skin texture and pores; only tiny controlled highlights on the nose tip and cheekbone tops.
Saturated translucent rose-pink blush placed high under the eyes, diffused outward, forming a clearly visible continuous translucent band across the nose bridge connecting both cheeks, with soft edges, never an opaque stripe.
Glossy rose-pink lips with a slightly deeper rose center fading softly toward the edges. Lips are the only area with a continuous wet glossy surface; eye shimmer remains localized silver-pink sheen and discrete micro-sparkles strictly on the eye area.
```
这三段替代原来的底妆、腮红和唇部描述，避免同时叠加 satin-finish 与 soft-matte，也避免用“only glossy area”压掉眼周珠光。

## 本次实际编辑指令摘要
保留第一版人物、自然五官、肤质、黑背景、方形近景、柔闪、发丝、耳饰、露肩针织与黑吊带、右侧触唇手势及美甲；稍加强连鼻腮红与唇中央色差，略向画面左侧转脸并保持直视。皮肤限制连续油光，眼周保留细闪，其余不变。该轮结果只验证了编辑路径；后续身份参考迁移另见下文。

## 复用与验收
无身份图创建新成年人物；有身份图按主流程保留本人辨识特征，不沿用案例脸。检查腮红跨鼻连接、双侧细闪位置与粒径、皮肤纹理与油光、唇中央色差、触唇解剖。转脸单独验收，不因妆面通过默认姿态通过。

## 对照素材
路径相对于本 Skill 根目录：
- `assets/rose-pink-velvet-closeup/v1.png`：用户正向反馈的第一版。
- `assets/rose-pink-velvet-closeup/v2.png`：无图微调版，用户反馈两版各有感觉。


## 已认可：身份参考两宫格
使用用户本轮指定的新近景照片作为唯一身份来源，不混入前一位人物或无图生成的人脸。身份参考提供眼型、眼距、鼻唇与脸部个体特征；妆面、直视神态、光线和黑底造型由配方主导。

共同修饰：顺原眉形整理毛流与眉尾，玫棕色压深外眼角和睫毛根部，细棕内眼线与短上扬眼尾、根根分明的卷翘睫毛；控制下眼睑粉色范围，避免疲惫或浮肿感。整理自然唇缘并做中央渐深；面颊下部保留清爽空间。重点是化妆对原有五官的修饰，不以放大眼睛、缩鼻或削脸代替。

- 柔淡版：轻盈高位玫粉腮红、较淡的鼻梁连接、柔玫粉渐层唇，眼妆和细闪仍应充分呈现。
- 浓郁版：连鼻腮红更明确、眼尾玫棕层次略深、唇中央更深。保持透明柔边，不画成横向色条。
- 双宫格只是本次比较方式，不是今后的固定输出要求。两版保留为平行选择，不将浓郁版自动视为优于柔淡版。

### 可复用提示词
以下为已认可生成指令的精简复用稿，精简稿未单独复测。按用户所需版式与身份来源替换开头，不需要每次生成两宫格。
```text
Create a photorealistic horizontal diptych of two equal square close-up portraits of the same adult person in the supplied identity reference, separated by a narrow clean divider, no text. Use this image as the sole source of recognizable facial identity. Preserve individual facial anatomy, eye shape and spacing, nose and lip shapes, cheek and jaw proportions. Apply the target makeup and styling rather than copying the reference's existing makeup, gaze or lighting.
Shared makeup: cool milky-ivory soft-matte velvety cosmetic base with fine visible skin texture, tiny controlled highlights on nose tip and cheekbone tops. Groomed brows with individual hair strokes and defined tails following the existing brow shape. Rose-pink eye wash with rose-brown depth at outer corners and lash roots, fine brown tightline and a short softly lifted outer flick, curled separated lashes. Controlled lower-lid pink, not swollen or tired. Fine silver-pink sheen on upper lids and inner corners, delicate discrete pinpoint sparkles along BOTH lower lash lines and aegyo-sal, strictly confined to the eye area. Glossy rose-pink lips with softly refined natural edges and a deeper center fading toward the edges.
Left: airy translucent high rose-pink blush, softly diffused outward with a lighter connection across the nose bridge, soft rose-pink lips and delicate romantic freshness. Fully realized eye makeup, not barely-there makeup.
Right: slightly more saturated high rose-pink blush clearly connecting across the nose bridge with translucent soft edges, subtly deeper rose-brown outer-eye definition and a deeper rose lip center. Keep lower cheeks relatively clear and preserve natural facial structure.
Near-camera soft frontal flash against a black background, no clipped highlights. Direct gaze, lips slightly parted without a broad smile, face turned slightly toward image-left with a gentle tilt. Face primary, hand secondary. One hand at image-right in each panel, a single fingertip resting naturally at the outer edge of the lower lip, other fingers loosely curled, long nude-pink almond nails. Small silver beaded ear climber, thin black camisole strap under off-shoulder white knit, one bare shoulder, dark hair with loose forehead strands. Match face scale, light and styling across panels. Lips have continuous wet gloss; eyes have localized sheen and discrete micro-sparkles.
Avoid replacement face, identity drift, facial reshaping, oversized eyes, flat all-over pink tint, oily or sweaty skin, rhinestones, gems, chunky glitter, cheek glitter, excessive smoothing, waxy skin, fused fingers, duplicated hands, nail penetration, text and watermark.
```
无身份图时，将身份参考开头替换为创建一位有自然个体特征的新成年人物；不沿用案例人物脸。

### 参考图选择经验与边界
本次换用更接近目标的近景参考后获认可，用户反馈“参考图也很重要”。可优先使用五官清楚、遮挡少、脸部占比足够的照片；原妆、表情与光线也可能影响迁移。两次输入的人物、原妆、神态与生成指令均不同，不能据此断定差异全由参考图质量造成，也不评价人物本身的美丑。清晰餐厅照仍可作为身份来源，不应强制用户换图或要求身份照本来就符合目标妆容。

### 验收范围
最终近景参考两宫格的整体审美获用户认可；双侧细闪、柔淡与浓郁妆面差异可见。两版差异偏小，转脸幅度等精确姿态不作为已稳定验证能力；本人辨识保留不等于逐项五官无漂移的客观测量。无图好看不能代替有图适配验收。

### 已认可图
`assets/rose-pink-velvet-closeup/identity-diptych-accepted.png`，内置 imagegen 生成。只保留生成结果，不将用户原始身份照片打包进 Skill。
