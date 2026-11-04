# 后期与整图调色

## 任务与执行边界
后期权重低于妆容、高于配饰。先检查妆面是否精致、充分且悦目，再设计整图调色；妆面未达到目标时先修妆面，不靠滤镜、逆光光晕或环境氛围掩盖。自进化中该顺序指设计与验收，不构成图生图后处理的授权。

- 自进化文生图：把后期作为成片目标加入提示词，从文字重新生成；不传任何图片，不把生成后再编辑包装成纯文生图。没有实际后期操作时称“生成的目标调色效果”，不声称做过独立修图。
- 已有图调色：用户明确要求给现有图片调色时，用可用图像编辑工具处理整图。先查看图片，以它为编辑目标，默认保留身份、五官、妆面位置、动作、构图、服饰与场景结构，只改变色调、影调及必要的细节呈现。用户要求重设计时再扩展。
- 仅方案：只要求分析或调色提示词时不自动生成或编辑。工具不能实现精确曲线、HSL 或 LUT 时，使用视觉语义，不声称已应用具体软件数值。

## 分清三个来源
妆容决定底色、色料位置及表面反光；照明决定光位、光比与投影；后期决定整幅成片的颜色映射、影调与细节表现。后期不能替代缺失的眼妆或凭空生成新的光源结构。全局调色影响人物、服装、饰品与背景，不应只给脸刷白；为保留肤色与妆色可约束肤色区域，不强迫所有物体统一冷粉。

## 可控规格
每轮选一个明确的整图方向，按需要填写，不强制把所有项目都调一遍：

|维度|需要明确的视觉结果|
|---|---|
|白平衡与色偏|中性或偏冷/暖的整体基准；肤色与白色织物是否受染|
|曝光与影调|主体亮度、背景亮度、黑位深浅、暗部可读性、亮部滚降|
|对比|全局明暗与局部细节分开；保留脸部体积，避免全脸灰雾或硬锐化|
|色彩|主辅色、整体饱和度、粉红/橙/紫的取向；肤色与背景的分离|
|高光与阴影色|如中性亮部配轻冷灰阴影；不靠蓝黑皮肤制造冷感|
|细节|纹理、颗粒、锐度和柔光程度；避免反复压纹、皮肤塑料化与吞掉细闪|
|保护项|原妆颜色与位置、唇面光泽、眼周闪点、服装色及必要暗部信息|

这些是文字规格，不是图像工具的真实滑块或保证可精确复现的参数。

## 当前审美方向：冷白透粉、细闪泪光、水润唇、不油
可从“中性偏冷、亮部干净、肤色透粉、暗部安静”起步，保留原构图中的主体与背景层次，不要求所有场景用同一个黑位或对比。肤色保留微妙明暗，白不变青灰、粉不变紫红；白衣仍与肤色有色彩和材质区别。适度压低背景杂色，不能把环境细节一并染成粉色。

区分三种反射：皮肤大面柔雾至缎光；眼周细闪是小而离散的亮点，泪光是局部清透湿润反射；唇面是连续水润高光。后期不能一刀切压掉眼唇高光，也不能用全图泛光、提清晰度或拉亮高光制造油汗感。颗粒和柔光均为可选，不默认为所谓胶片感覆盖全部作品。

## 从 GitHub Skills 吸收的后期方法
研究日期：2026-11-04。以下为阅读后的选择性改写，未安装或运行外部 Skill，不继承其批处理、上传、模型调用和强制流程。自进化仅文生图，所有处理术语在此模式下均是成片目标，不是已执行的 Photoshop 操作。

### 先诊断，再校正，再做风格
先确认问题是曝光、白平衡、黑位、妆色还是反射，而不是直接叠胶片预设。亮部过强时要求肩缘与脸部亮部柔和过渡，不能一起压暗眼周细闪和唇部水光；暗部发灰时恢复背景与黑发的深浅，不把整脸对比拉硬。补暗部只恢复需要的信息，不将所有阴影提成灰雾。来源：[Adobe 人像精修](https://github.com/openai/plugins/blob/main/plugins/adobe/skills/adobe-retouch-portraits/SKILL.md)、[Photo Cull Retouch](https://github.com/dudachun/photo-cull-retouch/blob/main/SKILL.md)。

### 肤色与环境色分别保护
先排除环境造成的黄、绿或紫色污染，再保留有意设计的粉色腮红、眼影和唇色；不能把目标玫粉妆误判为红偏色而一并消除。环境可以更冷、更低饱和，人物仍需冷乳白底透出干净粉润，避免全局降温让脸发青。增加色彩鲜活度时关注肤色区域，不默认提高全图饱和度；外部 Skill 的自然饱和度建议也不保证自动识别并保护妆色。通用肤色色相、亮度数值只适合其特定工作流程，不是本项目审美目标。来源：[Adobe 人像精修](https://github.com/openai/plugins/blob/main/plugins/adobe/skills/adobe-retouch-portraits/SKILL.md)、[Color Grade AI](https://github.com/isaacrowntree/color-grade-ai/blob/main/SKILL.md)。

### 分区控制明暗与质感
借鉴 Dodge & Burn 的局部明暗思路：压住额头、鼻翼、面颊和肩部宽大的反光，保留小面积脸部高点、眼周离散闪点及唇面连续水光；不以一条全局高光指令消灭全部亮点。轻微明暗整理增强妆面层次，不能重新雕刻鼻子和脸型。借鉴频率分离中颜色与纹理分开处理的思路，目标是色调均匀但纹理轻且不规则，不用全脸模糊抹去眼睑、唇纹与闪点。仅创建频率分离或加减光图层并不等于完成手工精修。来源：[Photoshop colour-retouch 参考](https://github.com/Immersive-Media-Technologies/photoshop-mcp-imt/blob/main/skills/ps/references/color-retouch.md)。

### 最后再处理细节与氛围
眼线、睫毛和唇缘应可辨，但不把皮肤也同等锐化。微对比与锐度过强会加重毛孔、眼下阴影和假纹理；不要靠去雾把柔润妆面变硬。光晕只在明确强光边缘少量出现，不覆盖五官。颗粒、胶片和 LUT 均为可选风格，不默认叠加；LUT 不能完成局部油光控制、磨皮或锐化。来源：[Photo Cull Retouch](https://github.com/dudachun/photo-cull-retouch/blob/main/SKILL.md)、[Color Grade AI](https://github.com/isaacrowntree/color-grade-ai/blob/main/SKILL.md)。

### 应用于本任务的文生图后期段
```text
Final finish: clean neutral-cool color balance, luminous milky-ivory skin with intentional translucent rose makeup preserved. Keep the environment subdued and slightly cooler without cyan contamination on skin. Retain dimensional midtones and deep readable hair and background shadows, not raised gray blacks. Compress broad skin reflections gently on forehead, cheeks and shoulders, while preserving fine eye sparkles, localized moist tear-light and continuous watery lip highlights. Even skin color without erasing delicate irregular texture; keep lash roots and lip edges readable without sharpening pores. Restrict optical bloom to the brightest backlit hair tips, no glow veil across the face. No automatic film tint or grain.
```
按具体图的目标删减；没有逆光就删除光晕句。不能用这段替代妆容的颜色、位置和边界设计。

### 验证范围
以上为来源阅读与提示词适配，尚未完成本项目实际生成验收。外部仓库的工具能力、自评分数、色彩科学宣传不作为本项目验证结果。以后只记录可见改善与用户反馈，不因增加术语就声称质量已提升。

## 逆光与后期配合
用户提出常见逆光手法时，将逆光列为可选照明设计，并配套整图后期；不将光源方向误归为调色，也不只靠全图泛光伪造逆光。自进化仍只通过文字生成，不传图。

|方式|画面效果与适用选择|
|---|---|
|侧逆光＋正面柔补光|光源从人物侧后方照来，发丝、耳侧和肩缘有亮边；正面保持清楚的妆色与眼神，优先用于当前妆容展示|
|正后方逆光＋正面补光|头发外轮廓有透光边缘，人物与背景分离；注意光源遮挡关系，避免光晕吞掉脸缘|
|窗边逆光＋反射补光|窗户在后方或侧后方，形成柔和发丝亮边与明亮环境；窗外可淡化，但保留脸部层次与衣料细节|
|低角度暖逆光＋中性补光|发丝可带少量暖金边，与中性偏冷面部区分；避免整张脸和白衣都染黄|

逆光不是每张图的固定要求。选择时明确主光在人物哪一侧后方、光质与强度关系、正面补光及背景亮度。以可见效果描述，不编造灯光数值。细闪需要能被相机看到的反射，不能假设后方逆光自然就能照亮正面眼妆；用柔和正面补光或轻微近轴闪光感支撑眼部亮点，同时控制皮肤大面反光。

当前方向：发丝和肩缘局部透亮，脸由中性白柔光照清，保留冷白透粉与自然体积；皮肤柔雾至缎光，唇面水润，眼周局部细闪泪光。后期让亮部柔和滚降、暗部保留信息，光晕仅在强逆光边缘小范围出现；不抬成整图灰雾，不加覆盖五官的耀斑，不将肩部亮边扩成整片油亮。轮廓光的颜色可随环境变化，不能以破坏面部目标色为代价。

文生图提示词示例（按构图选择一侧，不照抄为固定灯位）：
```text
Soft backlight from behind the subject at camera-right catches fine hair strands and a narrow shoulder rim. Broad neutral-white frontal fill keeps the face dimensional and the cool milky-ivory complexion with translucent pink blush clearly readable. A restrained near-axis catchlight reveals tiny eye sparkles and moist tear-light accents without making the forehead and cheeks glossy. Keep watery lip highlights distinct from the soft-matte skin. Grade the entire image with gentle highlight rolloff, clear midtones and restrained shadow lift; preserve the luminous hair edge without a broad milky veil, clipped facial detail or flare across the eyes.
```

验证状态：逆光规格尚未实际出图验收，不将文字规则记为稳定生成能力。

## 提示词片段
只替换本轮选定项，避免与光线和妆面规格矛盾：

```text
Final whole-image color grade: [WHITE BALANCE AND TINT]. Set [SUBJECT/BACKGROUND TONAL RELATIONSHIP], with [BLACK LEVEL, SHADOW DETAIL AND HIGHLIGHT ROLLOFF]. Keep [PALETTE AND SATURATION RELATIONSHIPS]. Preserve natural dimensional skin tones and the intended makeup colors. Skin remains soft-matte to satin; retain discrete eye micro-sparkles, localized moist tear-light accents and continuous watery lip highlights. [TEXTURE/GRAIN/SHARPNESS]. Apply the tonal and color treatment coherently to the entire image, including clothing and background, without flattening their distinct materials or adding an all-over colored veil.
```

已有图调色时，加上明确保留身份、五官、构图、动作、衣服和场景结构的编辑约束；自进化不使用图片输入或身份保留指令。

## 验收
先缩略图检查整图色彩、视觉重心与主体分离，再检查脸颈手肤色、眼影与唇色、亮暗部细节。整图调色需同时作用于场景并保住妆面：避免青灰脸、洋红皮肤、白衣偏色、黑发死黑、高光溢出、细闪消失与全脸油亮。单独调色任务有原图时对照结构与非目标改变；文生图不将两次新人物生成当作同一图片的严格调色前后对比。

状态：支持规则与提示词；尚未完成独立整图调色实测。记录实际工具、输入方式、目标后期、输出观察和用户反馈后再更新验证范围。

## 已认可应用
[夜景橱窗冷白透粉妆](styles/night-storefront-porcelain-rose.md)：2026-11-04 一次纯文生图成片获“不错，通过”确认。验证的是文字生成的妆容与真实夜景调色组合，不是对已有图片执行独立后期；不扩大为所有逆光或背景方案均已通过。
