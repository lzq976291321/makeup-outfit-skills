# 珍珠柔光裸桃妆

状态：仅分析；尚未生成试妆或获得生成效果认可。
来源：用户提供的白色褶皱头巾、珍珠耳钉、黑背景肩颈肖像。风格名是便于检索的描述，不代表已知流派或产品。未收录人物原图。

## 目标

轻透象牙白肌肤上铺低饱和裸桃色，用清晰细眼线建立眼部重心，以连续、柔和的皮肤反光和湿润唇面形成光泽。没有明显的眼周大颗粒闪片；不要自动加入冷白透粉闪光妆的银粉细闪。

## 可见观察

|区域|图中可见特征|迁移时的操作|
|---|---|---|
|底妆|明亮象牙色，颊部偏柔粉桃，仍见细纹理；额头、鼻梁、颧骨有反光|轻薄均匀底色，柔化色差但不抹掉全部纹理；保持脸颈肩连贯|
|眉|低饱和灰棕色，眉头松散、有毛流，眉尾收细|沿目标人物原眉形梳理，不固定复制参考眉峰与眉眼距离|
|眼影|淡米桃、浅棕层次，外眼角略深，未见大块亮片|用低对比薄晕染表现眼窝，不把浅眼影加深成烟熏妆|
|眼线|上睫毛根部清楚，眼尾细长外延、微上扬|贴合原眼形，小幅延伸；不靠放大眼睛制造效果|
|睫毛|上睫毛分束、外侧较有存在感；下睫毛细且分离|保留睫毛根部和睑缘，不做整片浓黑假睫毛|
|腮红|面颊有低饱和粉桃晕染，边缘柔和|小面积薄叠，避免高饱和粉团或跨鼻大片晒伤色|
|唇|裸桃玫瑰色，内侧略深，下唇有局部湿润高光|保留本人的唇线、唇峰与细纹；薄光泽而非厚玻璃唇|
|细节|眼下与颊部可见少数浅棕小点，少量细软发丝|可作为可选细节，不把斑点位置与数量固定到新人物|
|肩颈|锁骨上缘及肩头有宽窄变化的高光，骨下有柔影|用光影与遮挡表现自然锁骨，不加深凹陷或削瘦身体|

眼睛呈棕色，但不能确认是否佩戴美瞳；不将瞳色、虹膜大小作为妆容必须项。图中没有手与美甲，相关字段不适用，不能补写成观察事实。

## 光线、配饰与不确定项

画面左侧发丝和肩缘较亮，脸与上胸有明显明暗体积，黑背景与浅色皮肤/布料形成分离。可以尝试画面左前上方偏轴主光，保留亮边；不能据图确认具体灯具、灯数、焦距或光圈。皮肤提亮、纹理与反光可能同时受后期或生成处理影响，不能把上胸较密的纹理照单全收为真实皮肤标准。

珍珠耳钉提供小面积乳白圆形亮点；白色褶皱头巾与披肩形成大面积纹理，黑发、黑背景使面部颜色更显干净。这些是衬托妆容的可选造型，不是复制妆效的必要条件。珍珠的柔亮、唇部湿亮、布料褶皱反光和皮肤起伏应彼此区分。无可见项链，不为“完整造型”默认添加。

## 可迁移规律

1. **色彩轻、轮廓清**：低饱和眼颊唇统一在裸桃色系，用细眼线与分束睫毛建立重心，避免所有区域同时加深。
2. **柔亮代替闪点**：重点是皮肤和唇面的连续反射，而不是眼周布灵布灵颗粒。珠光可极弱，明显闪片为零。
3. **质感有层次**：皮肤微纹理、珍珠圆润反光、纱布状褶皱各有尺度；不能把整张图统一成塑料表面。
4. **暗背景让亮部成立**：先保留明暗过渡，再提高局部亮度；象牙白不等于全脸曝光溢出。
5. **肩颈是延伸**：领口、发丝与姿态为锁骨留白，亮点由脸延伸到肩颈；不改变人物解剖结构。

## 参数配方

```yaml
base: luminous-ivory, sheer-to-medium-coverage
undertone: neutral-ivory-with-soft-peach
brows: muted-gray-brown, visible-hair-strokes
eyeshadow: pale-peach-beige, subtle-taupe-outer-corner
eyeliner: fine-dark-brown-or-soft-black, slightly-extended-tail
lashes: separated, restrained-outer-emphasis
blush: low-saturation-peach-rose, diffuse-edge
lips: nude-peach-rose, subtly-deeper-inner-lip, selective-moist-sheen
sparkle_particles: none
skin_highlight: forehead-nose-upper-cheek, narrow-to-broad-natural-transitions
collarbone: natural-relief, no-body-reshaping
freckles: optional, do-not-copy-identity-marks
earrings: optional-small-pearl-studs
necklace: none-by-default
nails: not-visible-in-reference
lighting: off-axis-front-upper-light-hypothesis
```

肤色按本轮明确目标决定；复现此图时采用明亮象牙底色，不强制更冷、更白。固定人物优先保留骨相、眼型、眉眼距离、鼻唇特征与原发型；头巾和露肩造型仅在用户要求时加入。

## 提示词：有身份图，换妆

```text
Use the supplied person reference as the sole identity source. Preserve recognizable facial anatomy, eye shape and spacing, nose, lip outline, jawline and hairstyle. Change the makeup to a luminous ivory nude-peach look: a sheer, even base with fine skin texture and soft peach-rose cheeks, muted gray-brown brows with visible hair strokes, pale peach-beige eyelids with subtle taupe depth at the outer corners, and a precise fine upper lash line extending slightly outward. Keep lashes separated, with restrained emphasis at the outer corners. Use nude peach-rose lips, subtly deeper inside, with small moist highlights and visible lip texture. Keep the eye area free of glitter particles. Shape gentle continuous skin highlights across the forehead, nose and upper cheekbones. Preserve clothing, background and framing unless a change is requested. Where the existing composition reveals the shoulders, keep natural collarbone relief and a consistent face-neck-shoulder finish. Do not copy another person's facial proportions, enlarge irises, carve collarbones, add jewelry or turn the skin into plastic.
```

## 提示词：无身份图，完整造型示例

```text
Create a photographic portrait of a new adult woman, framed from the upper chest upward, with a gentle three-quarter head turn and gaze toward the camera. Luminous ivory skin with delicate natural texture, low-saturation peach-rose blush, pale peach-beige eyelids, softly defined outer corners, fine extended upper eyeliner and separated lashes. Muted natural brows and nude peach-rose lips with selective moist highlights. No visible glitter particles around the eyes. A small pearl stud, softly gathered dark hair with a few loose strands, and ivory pleated fabric framing the head and shoulders create restrained tonal harmony. Dark quiet background; off-axis light from the upper camera-left side gives gentle facial volume, luminous hair edges and natural collarbone highlights. Preserve highlight detail, realistic skin and distinct pearl and fabric reflections. No excessive smoothing, coarse repeated skin texture, oversized eyes, exaggerated collarbone hollows, text or watermark.
```

这是完整造型的可选示例，不要求每次试妆都加头巾、耳钉或露肩服装。

## 质量检查与修正

- 缩略图先看脸和眼睛，白布料不应比脸更抢眼；过亮时降低布料亮度，别一并压暗肤色。
- 眼线细且与眼睑连接，上下睫毛分束；眼下没有被误加银色闪片或浓黑眼袋。
- 唇颊同色系但有深浅，唇光不铺满唇外皮肤；腮红不过饱和。
- 脸颈肩不出现色差断层，高光保留细节，皮肤纹理不呈规则压纹或重复颗粒。
- 固定人物时并排对比身份图；不得把参考图的眼睛大小、脸型或棕瞳当作妆效迁移。
- 珍珠耳钉贴合耳垂，发丝与布料遮挡合理；没有凭空添加项链或未观察到的美甲。

## 反馈与修订

本轮只依据参考图完成观察、候选配方和提示词，未执行生图。新人物迁移、布光复现与用户试妆认可均待验证。后续反馈应修订此案例，不覆盖已有冷白透粉闪光妆。
