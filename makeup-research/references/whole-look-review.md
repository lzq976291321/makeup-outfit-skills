# 整体造型分析

冷白透粉闪光妆和象牙白妆都必须分析整体造型，不只记录底妆。此流程也适用于后来新增的妆容案例。

## 先标注参考图角色

身份图负责人物是谁，风格图负责妆容、配饰和姿势的目标。单张人物照用于换妆时，默认保留它的眼神、姿势和首饰；研究整套参考风格时，记录全部元素及其可迁移关系。换妆不等于默认更换首饰、动作与服装；复现整体造型或用户指定时才迁移这些元素。

## 必须观察的字段

|维度|记录内容|检查边界|
|---|---|---|
|眼神|看镜头或看向哪里、上下左右视线、眼睑开合、眉部张力、嘴角与唇部开合|描述可见状态，不推断人物真实情绪；不能用放大眼睛代替眼神|
|头肩姿势|头部转向与倾斜、下巴高低、肩线、躯干朝向、锁骨留白|左右按画面方向标注；不把姿态效果归因于改骨相|
|手部姿势|手掌朝向、前后遮挡、手腕弯曲、指尖接触点、承重关系|未出现手就标不可见，不凭空分析美甲|
|耳环|轮廓、尺寸相对耳垂与下颌的比例、颜色、反光、发丝遮挡|耳钉贴合耳垂、垂坠遵循重力；不猜品牌|
|项链与其他首饰|链长落点、吊坠形状尺度、叠戴间距、戒指手链位置、与领口关系|链条不能穿皮肤，戒指围合手指，遮挡有逻辑|
|美甲与发饰|甲型长度、颜色、透明度、亮片装饰；发夹或头巾的体积与位置|区分图中可见、未出现和遮挡无法判断|
|服装与材质|领口、肩线、袖口、褶皱、配色面积及软硬反光对照|不凭未显示部分补造完整穿搭|

每项标明：保留 / 迁移 / 调整 / 不适用。提炼至少一个关系，例如耳饰与下颌留白、项链与锁骨、指尖与视线导向，而非堆砌首饰名称。

## 提示词组织

在身份与妆面描述后，明确填写以下字段，不把槽位原样交给生成工具：

```text
Gaze and expression: [direction, eyelid openness, brow tension, lip state].
Head and body pose: [head turn/tilt, chin, shoulder line, torso direction].
Hands: [orientation, overlap, contact point; or outside the frame].
Jewelry and accessories: [earrings, necklace, rings, nails, hair accessories; exact placement and material].
Preserve [specified elements] from the identity image; transfer only [authorized style elements].
```
