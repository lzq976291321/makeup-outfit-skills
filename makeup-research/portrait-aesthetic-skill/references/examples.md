# 完整示例

以下是可执行的提示词示例，尚未生成或验收图片。无身份图的示例默认新人物；并不复制来源人物。

## 示例一：迁移原图的视觉关系
参数：新成年女性；竖幅 3:4；上半身近景；简化双手动作；浅灰针织；低亮度室内。

```text
Create a photographic upper-body portrait of a new adult woman with individual, natural facial proportions. Vertical 3:4 composition. Her head is slightly lowered, gaze directed toward her hands, lips relaxed. Her left hand rests loosely below her chin; the right fingertips rest gently on the back of the left hand, with both wrists relaxed and the overlap clearly readable. Use a near-camera frontal flash-like light: a bright face and hands against a dim, low-detail interior, with soft but visible nose and jaw shadows. Keep her natural skin tone and fine skin texture. Muted rose eye makeup, a few fine reflective accents on the eyelids, subtle blush and softly glossy lips. A light gray ribbed knit top has visible fibers and folds that follow the arms. Small silver earrings provide restrained bright accents. The face is the primary focal point, the hands secondary; keep both readable without excessive blur. Preserve coherent finger anatomy and believable contact.
```

负面：plastic skin, fused fingers, floating jewelry, overexposed face, busy background。
检查重点：是否仍保留脸—手的主次；是否被饰品抢走注意力；针织与皮肤是否同样光滑。

## 示例二：换人物 A，保持身份
前提：图 1 是用户指定成年人物 A，图 2 是风格参考。若未上传图 1，不假装可锁定身份。

```text
Use image 1 as the sole identity reference for this adult person. Preserve their facial proportions, eye shape and spacing, nose, lip shape, jawline, skin tone and distinctive asymmetries. Use image 2 only for the bright-subject/dim-background relationship, restrained reflective makeup and soft-versus-metallic material contrast; do not transfer its face or hairstyle. Create a vertical 4:5 chest-up portrait. The subject looks slightly downward with a calm expression. One hand gently holds the edge of a charcoal wool cardigan near the collarbone; the other stays outside the frame. Use a near-axis frontal photographic light with visible facial modeling, retaining wool texture and a small silver pendant highlight. Apply subtle warm copper eye makeup suited to this subject, maintaining realistic skin texture. Keep the face dominant and the background quiet.
```

检查重点：把人物 A 与结果并排对比，妆容卸除后是否仍像同一人；深色衣服是否失去纹理。此例通过单手与深衣验证迁移，不依赖原图的白衣和复杂手势。

## 示例三：换场景与主光
参数：新的成年深肤色女性；窗边；靛蓝棉衬衫；轻扶袖口；横幅 4:3。

```text
Create a horizontal 4:3 photographic portrait of a new adult woman with deep brown skin, seated beside a window. Frame from the waist up with room in the direction of her gaze. Soft daylight from the window on camera left shapes the face; the room behind her stays subdued. Preserve the depth and warmth of her skin tone, with fine skin texture and controlled highlights. Muted bronze eyelids and softly moisturized lips provide small reflective accents. She looks toward her lowered right hand while her left hand gently adjusts the right shirt cuff, fingers naturally curved and clearly separated where visible. An indigo cotton shirt shows matte fibers, seams and plausible folds. A small brushed-metal bracelet adds a restrained hard-material accent. Prioritize the face, then the cuff-adjusting gesture; keep the surroundings low in detail.
```

检查重点：窗光方向能否解释脸、手和衣服；肤色是否被错误提亮；仍保留局部光泽与材质对比，但不再强制直闪。

## 局部修复示例
仅当现有图片已经满足身份、构图和光线时使用：

```text
Edit only the overlapping hands and their immediate contact area. Keep the person's face, expression, skin tone, hairstyle, clothing design, camera framing and lighting unchanged. Make the right fingertips rest gently on the back of the left hand, with connected wrists, plausible joints, nails aligned with the fingertips and subtle contact shadows. Preserve the existing rings only where they fit naturally around a finger. Blend the repaired area with the original texture and light direction.
```

工具支持遮罩时限制编辑范围；不支持时描述范围并复查全图，不能声称其他区域一定未变。
