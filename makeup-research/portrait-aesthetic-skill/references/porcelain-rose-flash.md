# 冷白透粉闪光妆：已确认的风格配方

## 目标与适用范围
生成“明亮冷白区域、淡淡红晕、眼周闪烁、肩颈锁骨清楚”的人像。人物来源每次可换；不固定复制某张脸。识别到冷白皮、布灵布灵、眼周细闪等人物妆效意图，或用户明确调用本配方后，默认启用这个妆面；用户明确要求其他妆容或肤色时覆盖默认。固定人物需要身份图与支持参考的图像工具；无人物参考时直接创建冷白皮成年新人物，不能声称固定人物。

## 视觉关系
- 白：额心、鼻梁、颧骨上方、下巴和肩头形成明亮冷乳白区域，保留细微色阶，避免整片无细节死白。
- 红：粉玫瑰色从面颊、鼻尖、眼睑轻轻透出；边界柔和，不做饱和红色团块。
- 闪：上眼睑、内眼角和局部下眼缘有清楚的银粉色细碎亮点。眼妆是闪光中心；脸部其余区域以柔和光泽衬托。
- 皮肤：脸、颈、肩、上胸色温和明度协调；细纹理仍可见。软针织保持哑光，避免与皮肤同样反光。
- 锁骨：领口适当降低、手移到一侧、发束让开肩颈；靠锁骨上缘窄高光和下方柔影表现体积，不削瘦身体或改变骨架。
- 光：近轴前向闪光感让皮肤亮于环境，鼻侧与下颌仍有体积；暗背景安静退后。

## 参数卡
```yaml
identity: 用户本轮指定参考，唯一身份来源
base_luminance: porcelain        # natural / bright / porcelain
undertone: cool-ivory
rose_flush: subtle           # subtle / medium
sparkle_density: medium      # low / medium / dense
sparkle_placement: upper-lids, inner-corners, selective-lower-lash-line
skin_sheen: selective        # selective / dewy
collarbone_visibility: clear # natural / clear
hand_position: relaxed-overlap-to-one-side
fabric: matte-ivory-ribbed-knit
background: dim-neutral-interior
```
这些是提示词语义槽位，不是工具参数。起始建议使用 medium 细闪、selective 光泽；喜欢更强闪耀时再增加密度，避免同时把全脸油光和闪片密度都加到最高。

## 执行
1. 标明唯一身份图，保留眼距、眼型、鼻唇比例、脸部轮廓与发型长度。妆面提亮不得转化成削脸、缩鼻或放大眼睛。
2. 已有满意肖像时优先编辑该图，明确保留人物与构图，只改妆面、光泽和必要的遮挡。需要更突出锁骨时允许调整领口、手与头发位置。
3. 先建立冷白与淡红的底色关系，再定位细闪；不要仅写“漂亮、白、闪”。
4. 生成后检查脸颈色差、肩部曝光、细闪大小和锁骨阴影。若太油，降低额头和肩部连续高光；若太素，优先增加眼睑粉色与局部细闪，不盲目提亮全图。
5. 用用户反馈选择效果。不要把助手个人偏好的更克制妆容覆盖用户已认可的强妆感。

## 可直接使用：固定人物生成
```text
Create one photorealistic upper-body portrait of the same adult person in the supplied identity reference. Preserve their recognizable facial anatomy, eye shape and spacing, eyebrows, nose, lip outline, jaw contour and hairstyle length. Apply luminous cool porcelain-ivory cosmetic makeup: bright milky highlights across the central forehead, nose bridge, upper cheek planes and chin, retaining subtle skin texture and tonal detail. A faint translucent rose-pink flush shines through across the cheeks, eyelids and nose tip. Use clearly visible pink pearlescent eyeshadow and tiny crisp silver-pink twinkles across upper lids, inner corners and selected lower-lash areas. Keep the sparkle fine and localized, with glossy rose lips. Near-camera frontal flash-like illumination makes the skin bright against a dim neutral interior while retaining nose and jaw shadows. A matte ivory off-shoulder ribbed knit top frames the neck and upper chest. Keep both collarbones visible by resting hair behind the shoulders and placing relaxed overlapping hands toward one side below the clavicles. Show natural collarbone structure with narrow pearly highlights and gentle shadows, without changing body shape. Match the luminous makeup finish across face, neck, shoulders and upper chest. Face first, sparkling eyes second, hands subordinate. Preserve coherent hand anatomy and fine material distinctions. No identity drift, plastic skin, blown-out white patches, oversized glitter, artificial carved collarbones, floating rings, text or watermark.
```

## 可直接使用：现有肖像编辑
```text
Edit this portrait while preserving the same person's facial anatomy, recognizable features, hairstyle length, framing and background. Change the makeup to a substantially brighter cool milky-ivory base, with a delicate translucent pink-red flush on cheeks, eyelids and nose tip. Add fine silver-pink sparkling highlights on the upper eyelids, inner corners and selectively beneath the eyes; glossy rose-pink lips. Retain fine skin texture and highlight detail. Make the collarbones clearly visible by gently lowering the off-shoulder neckline, moving the overlapping hands down to one side and clearing hair from the shoulder area. Emphasize existing collarbone structure with pearly upper-edge highlights and soft shadows beneath, without reshaping anatomy. Keep face, neck, shoulder and chest finish consistent. Use brighter near-axis flash against the dim room, distinguishing luminous skin from matte knit. Avoid excessive oiliness, opaque glitter patches, blown highlights and identity changes.
```

## 质量检查
- 远看：脸与肩颈明亮，背景退后；没有只剩白色块面。
- 近看：眼周细闪清楚，粉红从白底透出，睫毛与眼睑边缘仍能辨认。
- 身份：妆前参考与成图并排，五官比例和特征未被美化改写。
- 皮肤：脸与脖子无突兀分界，针织与皮肤反光不同，肩头没有塑料质感。
- 姿态：锁骨区域未被手发遮满；肩颈与胸骨结构连贯，手指接触自然。

## 实测范围
本次先用一张用户指定人物照生成肖像，再对生成结果加强冷白、透粉、眼周闪光并露出锁骨。用户看见第二版后明确反馈“好漂亮”，并要求沉淀。说明这一输入和这次编辑得到了用户认可；不代表跨人物、跨模型或随机重复生成都已验证。工具为内置 imagegen，没有暴露可记录的具体模型版本、seed 或采样参数，不补造这些信息。


## 整体造型分析
按 [眼神、姿势与配饰分析](../../references/whole-look-review.md) 记录本轮参考的眼睑开合、视线、头肩角度、手部接触、耳环、项链、戒指、美甲和发饰，逐项注明保留或迁移。只换妆时不擅自更换首饰与动作。
