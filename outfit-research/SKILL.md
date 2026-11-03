---
name: outfit-research
description: 研究版型配色材质、设计搭配并进行固定人物换装检查。
---

# 穿搭研究

适用于分析参考穿搭、提炼组合规律、固定人物换装与 AI 造型效果检查。关注衣服与人物、场景和妆容的关系；不默认改变人物体型、五官或肤色。
## 输入与边界
明确身份图、衣服图、场景、用途和必须保留的单品。身份图负责人物，衣服图负责服装细节，风格图负责搭配关系。缺少尺寸时不能承诺实穿合体；仅凭图片不猜品牌、成分或价格。只有上半身参考时，不虚构鞋裤为已知信息。
## 研究流程
1. 拆解轮廓、松量、肩线、领口、腰线、衣长、层次、配色面积、材质反光与配饰密度。将看得见的结构与推测分开。
2. 提炼组合关系：上松下紧或整体宽松、长短层次、明暗面积、软硬材质对照、视觉重点位置。不要把“显瘦”设为所有人的目标。
3. 给出可替换项与不可变项。商品还原保留颜色、领口、袖型、扣件和图案；自由搭配才允许重设计。
4. 按人物本身比例设计衣服的松量与落点，不拉长腿、缩腰或改变肩宽。用衣料垂坠和裁切表达造型。
5. 写清材质行为：针织有纱线与受力变化，棉有哑光褶皱，缎有宽幅连续反射，皮革有厚度，金属为小面积硬反光。系带穿孔、纽扣受力和衣片连接要可解释。
6. 换装任务保留人物、姿态与指定背景；检查领口、腋下、袖口、手指和首饰接触。复杂服装先解决结构，再调装饰。
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
accessories: 数量、尺度、材质
framing: 上半身/全身
must_keep: 人物、体型、妆容、单品细节
may_change: 用户允许调整项
```
## 提示词模板
```text
Dress the same person from the identity reference in [GARMENTS]. Preserve their face, hairstyle, body proportions, pose and [OTHER FIXED ELEMENTS]. Match [GARMENT REFERENCE DETAILS]. Use [SILHOUETTE, FIT AND LAYERING], [COLOR AREA RELATIONSHIPS] and [MATERIAL BEHAVIOR]. Show plausible seams, closures, folds and contact with skin and hands. Keep [MAKEUP AND BACKGROUND] unchanged. Frame [CROP] so the intended outfit details remain visible. Avoid altered body proportions, fused fabric, floating straps and broken fastenings.
```
## 示例：哑光针织衬托闪光妆
奶油白细罗纹露肩针织，领口露出自然锁骨；袖子有金属孔和连续交叉系带；银饰控制在小面积。白衣承担柔软大色块，细闪眼妆和皮肤承担亮点。换成深灰羊毛仍可保留软硬对照，不必复制白色。
## 验收与沉淀
检查单品结构、配色面积、衣料受力、露肤位置、配饰接触、人物一致性与画幅。不能仅凭模特图宣称现实穿着效果。输出搭配逻辑、参数卡、提示词、实际检查结论和替换建议。未经生成验证的方案标为待试；保存案例时区分用户确认与助手建议。

