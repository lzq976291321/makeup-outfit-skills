# 参数卡与提示词

## 参数卡
复制后填写；方括号是供人编辑的槽位，不是 API 参数。

```yaml
subject: 新的成年人物，或用户指定身份
identity_source: 无 / 图1
style_source: 图2 / 文字风格
pose_source: 自拟 / 图3
identity_keep: 脸部比例与个体特征；肤色默认冷白，明确要求可覆盖
mood: 安静、视线略向下
framing: 竖幅上半身近景
aspect_ratio: 3:4
lighting: 近轴前向闪光感，背景低亮度
palette: 低饱和玫瑰色与中性环境
makeup: 冷白透粉底妆，粉色珠光眼影与银粉细闪，水润玫瑰唇
pose: 双手松叠在下巴下方，明确遮挡
wardrobe: 细罗纹针织
material_contrast: 哑光织物、皮肤微光、少量银饰
background: 低细节室内
must_keep: 身份与可解释的手部结构
may_change: 发型、首饰、背景陈设
```

3:4 为通用默认，不是来源图比例。比例应按交付用途填写；工具不支持指定比例时说明限制，不伪造请求参数。

## 正向模板

```text
Create a photographic portrait of [SUBJECT / IDENTITY INSTRUCTION].
Use [STYLE SOURCE] only for [LIGHTING, COLOR AND MATERIAL RELATIONSHIPS].
[FRAMING, ASPECT RATIO, CAMERA PERSPECTIVE].
[HEAD ANGLE, GAZE, EXPRESSION].
[EXPLICIT HAND ACTION, OVERLAP AND CONTACT].
[ONE DOMINANT LIGHTING SETUP], with [SUBJECT–BACKGROUND SEPARATION].
[MAKEUP COLOR AND SELECTIVE SHEEN], preserving [SKIN TONE AND TEXTURE].
[WARDROBE WITH FABRIC BEHAVIOR], [LIMITED ACCESSORY DETAILS].
[BACKGROUND]. Keep [FOCAL HIERARCHY] and [DEPTH OF FIELD INTENT].
Preserve [IDENTITY / STRUCTURAL PRIORITIES].
```

删除未使用句子，不把所有可选项塞入同一提示词。重要约束放前面，具体动作比“优雅的手”更可执行。

## 负面约束
支持独立 negative prompt 时可用：

```text
identity drift, altered facial proportions, waxy skin,
excessive smoothing, oversized eyes, fused fingers, duplicated hands,
disconnected wrists, nails penetrating lips, floating rings,
unexplained lighting directions, clipped facial highlights,
plastic knit fabric, broken lacing, competing background details
```

负面词不能保证消除缺陷。不支持独立负面字段时，把关键项改为正向要求，例如“hands have coherent anatomy and gentle contact; retain natural facial proportions”。不要把“不许手部出错”的长列表代替具体手势。

## 工具参数的处理
仅使用目标工具实际支持的字段。尺寸/比例、参考强度、编辑保留范围、seed、步数与引导强度各有不同语义，不提供跨模型通用数值。未选模型时只交付语义参数卡。镜头和光圈放在文字提示中时属于视觉描述。

调参顺序：先身份与构图，再动作，再光线色彩，最后微小装饰。使用工具的参考强度时从其默认或已验证配置起步；加强身份参考可能同时带入原背景与姿态，需要检查。记录实际模型标识、支持的参数、参考图角色与每次改动。相同 seed 仅在部分相同模型配置下便于比较，不证明人物相同。
