---
name: outfit-research
description: 分析参考穿搭与耳环、项链、戒指、美甲等配饰，提炼可迁移搭配规律、积累风格案例并根据反馈迭代 Skill；也用于固定人物换装与结构检查。
---

# 穿搭研究

适用于分析参考穿搭、提炼组合规律、固定人物换装与 AI 造型效果检查。关注衣服与人物、场景和妆容的关系；不默认改变人物体型、五官或肤色。
## 输出形式
宫格仅是历史验收时便于比较的展示方式，不是 Skill 的输出约束。默认生成独立单张成片；风格卡中的多个版本是可选方案，不要求一次全部生成。只有用户当轮明确要求宫格或拼图时才采用；要求多张时默认分别交付。历史记录里的左右、A–D 与格位仅用于识别当时样片，不规定新版布局。

## 参考图研究与持续迭代
用户要求研究参考穿搭或配饰、提炼风格及迭代 Skill 时，读取 [参考图学习流程](references/reference-learning.md)。耳环、项链、美甲等可单独研究，不要求每次提供整套穿搭。美甲配色与首饰关系在此记录，详细甲面配方按需交给妆容流程；保留各风格自身特点，不把新风格覆盖为已有造型。

## 风格索引
- [灰棕猫眼裸唇与黑银颈圈](../makeup-research/references/styles/taupe-cat-eye-nude-lips-black-silver.md#整体造型)：与妆容共用主配方，记录松散黑长发、黑色银钉颈圈与十字吊坠、裸粉细闪长甲及脸旁手势；有身份图独立单张完整造型获用户认可；服装从参考图未显示部分补全设计。
- [蜜桃碎闪猫眼与金饰黑卷发](../makeup-research/references/styles/peach-sparkle-cat-eye-gold.md#整体造型发型神态与配饰)：与妆容共用主配方，记录双环耳饰、黑金短链与细金叠链、长卷发及局部美甲；无图完整成片及一次有身份图的完整造型迁移均获用户认可，服装为可选补全设计。
- [玫瑰棕四版完整造型](../makeup-research/references/styles/muted-rose-brown-defined-eyes.md#完整造型复现配饰穿搭与神态)：与妆容共用主配方，记录四版耳饰、项链、低位眼镜、颈巾、领口及神态；有身份图完整造型四宫格获用户认可。
- 本文“哑光针织衬托闪光妆”为组合示例，尚未独立换装验收；新增参考按学习流程追加案例链接。

## 输入与边界
明确身份图、衣服图、场景、用途和必须保留的单品。身份图负责人物，衣服图负责服装细节，风格图负责搭配关系。缺少尺寸时不能承诺实穿合体；仅凭图片不猜品牌、成分或价格。只有上半身参考时，不虚构鞋裤为已知信息。

主动观察上传图片并结合请求判断角色，同一张图可兼作身份和风格参考。完整造型任务中，根据本人可见特点设计适合的轮廓、搭配和画面；风格参考则提炼用户关注的单品、配色、材质和组合关系，融入具体设计。商品还原保留指定细节；只给人物照且没有风格意图时，把它作为身份参考，自主设计其余部分。明确的局部换装、指定保留项和仅分析请求按用户范围执行。只有身份或关键用途无法合理判断且影响结果时才询问。
## 研究流程
1. 拆解轮廓、松量、肩线、领口、腰线、衣长、层次、配色面积、材质反光与配饰密度。将看得见的结构与推测分开。
2. 提炼组合关系：上松下紧或整体宽松、长短层次、明暗面积、软硬材质对照、视觉重点位置。不要把“显瘦”设为所有人的目标。
3. 给出可替换项与不可变项。商品还原保留颜色、领口、袖型、扣件和图案；自由搭配才允许重设计。
4. 按人物本身比例设计衣服的松量与落点，不拉长腿、缩腰或改变肩宽。用衣料垂坠和裁切表达造型。
5. 写清材质行为：针织有纱线与受力变化，棉有哑光褶皱，缎有宽幅连续反射，皮革有厚度，金属为小面积硬反光。系带穿孔、纽扣受力和衣片连接要可解释。
6. 明确只换衣服时保留人物、姿态与指定背景；参与完整写真设计时只固定脸部辨识特征和用户指定项，其余按目标风格设计；检查领口、腋下、袖口、手指和首饰接触。复杂服装先解决结构，再调装饰。
7. 与当前妆容协调：强细闪妆可减少首饰与服装的反光竞争；但用户要求华丽叠加时按目标执行。只改穿搭时保留已有妆容。
## 参数卡
```yaml
identity_source: 用户指定人物
garment_source: 服装图或文字
purpose: 写真/日常/通勤/其他
silhouette: 轮廓与松量
neckline_shoulders: 领口、肩线、露肤范围
waist_length: 腰线、衣长、层次
palette: 主色、辅色、点缀及面积
materials: 纤维纹理、厚度、垂坠、反光
construction: 缝线、扣件、系带、衣片连接
accessories: 耳环、项链、戒指、手链的数量、尺度、位置、材质及接触
nails: 甲型、长度、底色、透明度、亮片与首饰呼应
framing: 上半身/全身
must_keep: 脸部辨识特征与用户明确指定项；不以冻结姿态保持身体比例
may_change: 用户允许调整项
```
## 提示词模板
以下模板仅用于明确的局部换装任务。完整写真设计不使用冻结发型、姿态与背景的句子，应将这些维度按目标风格重新填写。
```text
Dress the same person from the identity reference in [GARMENTS]. Preserve recognizable facial identity and [USER-EXPLICIT FIXED ELEMENTS]. Design [HAIR, POSE, BACKGROUND, LIGHTING AND COMPOSITION] for the requested scope. Match [GARMENT REFERENCE DETAILS]. Use [SILHOUETTE, FIT AND LAYERING], [COLOR AREA RELATIONSHIPS] and [MATERIAL BEHAVIOR]. Show plausible seams, closures, folds and contact with skin and hands. Preserve only [USER-EXPLICIT MAKEUP OR BACKGROUND CONSTRAINTS, IF ANY]. Frame [CROP] so the intended outfit details remain visible. Avoid altered body proportions, fused fabric, floating straps and broken fastenings.
```
## 示例：哑光针织衬托闪光妆
奶油白细罗纹露肩针织，领口露出自然锁骨；袖子有金属孔和连续交叉系带；银饰控制在小面积。白衣承担柔软大色块，细闪眼妆和皮肤承担亮点。换成深灰羊毛仍可保留软硬对照，不必复制白色。
## 验收与沉淀
检查单品结构、配色面积、衣料受力、露肤位置、配饰接触、人物一致性与画幅。不能仅凭模特图宣称现实穿着效果。输出搭配逻辑、参数卡、提示词、实际检查结论和替换建议。未经生成验证的方案标为待试；保存案例时区分用户确认与助手建议。
