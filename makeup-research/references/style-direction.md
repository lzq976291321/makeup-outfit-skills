# 身份与整体造型分离：两套来源图的重新分析

用户指出先前双图的眼神、手势和发型不对。直接原因是提示词把身份图的齐肩发、低头微笑、指尖点下巴一并固定，导致只换肤色与眼妆。之前的妆面认可不等于整体造型迁移成功。

## 参考图一：象牙白珍珠造型

- 视线与表情：眼睛朝镜头，眼睑自然打开，并非低垂看手；嘴唇轻启、嘴角不明显上扬。应描述“安静直视、放松微启唇”，不能沿用身份照的微笑。
- 头与肩：脸朝画面左侧轻转，眼睛回看镜头；肩部躯干并不与脸完全同向。下巴略收，颈部舒展。画面右肩更靠前、更完整；肩线有斜度，不是左右平直的正面证件姿态。
- 手势：画面没有手。完整造型迁移时让双手离开画框，不能加交叠手、点唇或点下巴。
- 发型：深发向后归拢，头顶有自然蓬度与分缝，侧面发束收向耳后/后脑；额角、脸侧和耳边有细碎发丝。不是齐肩披发，也不是仅靠拉长头发。后部结构被布料遮挡，不能断定具体盘发结法。
- 头饰与服装：象牙白密褶织物从头顶斜包向后脑，后侧有明显体积；同色褶皱披肩在上臂以下聚拢，露出肩颈。原图具体纤维成分无法确认，不应直接断言真丝。
- 首饰：画面右侧耳垂一颗圆润白珍珠耳钉；另一侧遮挡，不推断两耳都看得见。没有可见项链，胸前留白，不从身份照带入吊坠。
- 妆与光：象牙白透淡桃，裸桃唇微湿，细长眼线与分束睫毛；不是银粉闪片妆。亮边、鼻侧与下颌有层次，但不能为了“立体”做成重暗半脸。
- 画面关系：黑背景、深发围合浅色面部，白色包头布扩展上方轮廓；颈部和锁骨长线条连接脸与披肩。不能只迁移耳钉与肤色而丢掉这套轮廓。

整体迁移提示片段：
```text
Preserve facial identity only. Turn the head slightly toward image-left while looking back toward the lens, eyes naturally open, lips gently parted without a smile. Sweep the dark hair back with soft crown volume, loose wisps at the temples and ear; wrap ivory densely pleated fabric across the crown and around the back of the head. A round pearl stud is visible at the exposed ear. No visible necklace. Both hands are outside the frame. An ivory pleated wrap rests below the shoulders, leaving the neck and natural collarbones unobstructed. Keep a gentle offset between head and shoulder orientation.
```

## 参考图二：冷白透粉闪光造型

- 视线与表情：下巴稍低，双眼看向下方中央、接近手部区域，不看镜头；上眼睑充分展示粉色细闪，唇轻启。没有微笑嘴角，不能把甜笑当成同一表情。
- 头与肩：脸接近正面但轻微偏转/倾斜，肩膀放松；手臂从画面下方两侧向脸下汇合，形成围合。不是把手放到胸口一侧后仍声称相同姿态。
- 手势：双手在嘴下交叠，若干手指横向铺叠；两根斜向抬起的手指在唇下形成窄三角，其中一枚长甲接近下唇边缘，另一根从下方斜向支撑。视觉重点是“横向手指层叠＋两根斜线引向唇”，不是单根食指点下巴。遮挡复杂，不能据图保证逐根手指归属；生成时明确接触、前后关系，保留几何关系并保证解剖合理。
- 发型：长直深发，长度延伸至胸前/画面下部；头顶近中分、略蓬松，额前有松散弧形碎发。两侧部分头发拨向耳后，长发仍落在躯干前，不是齐肩内扣发。
- 首饰：小银色圈耳环，细银链沿锁骨斜落；手指佩戴细圈与局部较宽装饰戒指，数量与位置须按可见区域记录，不从遮挡推断全部。不能一律换成珍珠耳钉。
- 美甲：长杏仁/尖椭圆甲，透明裸粉底，有银白水钻、亮片局部聚集，并非短纯色粉甲。甲面装饰与眼周闪点互相呼应。
- 衣服：奶油白罗纹露肩针织，袖口与肩/衣片侧边有金属孔交叉系带，画面右侧领口附近有矩形扣件。是大面积哑光纱线对照小面积首饰亮点。
- 皮肤与背景：冷白透粉、眼睑与局部眼下银粉细闪、水润玫瑰唇；室内暗背景保留低饱和绿座椅与灰墙，不能误套象牙白的纯黑背景、包头布与无项链造型。

整体迁移提示片段：
```text
Preserve facial identity only. Use long dark straight hair extending over the chest, a near-center part with soft crown volume and curved loose forehead wisps. Lower the gaze toward the hands, eyelids relaxed, lips slightly parted without smiling. Bring both forearms upward toward the center, overlap relaxed hands just below the mouth: several fingers lie across the other hand, while two gently raised fingers form a narrow triangular gesture toward the lower lip, one decorated nail lightly approaching its outer edge. Keep coherent joints, overlap and contact; do not substitute a single fingertip resting on the chin. Use long translucent nude-pink almond nails with localized silver-white crystal accents, small silver hoops, a fine silver chain and restrained rings. Ivory ribbed off-shoulder knit with plausible eyelet lacing and a small rectangular buckle.
```

## 参考图优先级补充
按 [主流程](../SKILL.md#有参考图时的优先级)，默认由 Skill 主导妆效和造型，参考图负责本人特征。只有用户明确要求保留原造型时，才使用局部换妆的冻结条件。下方“造型已认可后的局部加强”仅供已认可结果的后续局部编辑，不能用于把首次生成限制成原照轻修。

## 路由修正

- 固定人物仅固定脸部身份与个体特征，不自动锁住发型、眼神、表情、姿势和首饰。
- 用户明确“只换妆、其他不变”时才沿用身份图的这些元素；用户要求某个完整风格或指出这些元素不对时，采用该风格的造型描述。
- 身份参考与造型参考分别分配角色；两图冲突时不融合两张脸。仅有身份图也能使用上述文字配方，不能声称同时传入了风格原图。
- 迁移是关系与可见结构的迁移，不是固定复制原人物骨相、真实情绪或未知配件。


## 用户认可版本：造型确定后加强妆面

状态：已试图，用户明确反馈“满意，就是这种感觉”。本次使用一张人物身份图生成两套整体造型，再在已生成图上加强妆面；人物图片未收录仓库。两套风格同时展示只是本轮沟通方式，不是 Skill 固定输出格式。

用户接受左侧交叠手势；右侧头肩与包头造型虽与原风格图有变化，仍在用户允许范围内。后续不要为了机械对齐原图推翻已认可姿势。先前妆面偏弱；最终版保留两侧身份、眼神、发型、姿势、首饰与服装，只增强以下差异：

- 冷白闪光：冷乳白底色明显提亮，淡玫瑰红晕从白底透出；粉玫瑰眼影与眼睑、内眼角及局部下眼缘的银粉细闪明显，玫瑰粉唇湿润反光。细闪在整张图尺度下也能辨认，而非放大才可见。
- 象牙白：明亮中性偏冷乳白底色，淡桃粉衬色更清楚；淡桃米色眼影、细长眼线、分束睫毛与裸桃玫瑰唇强化；颧骨、额头、鼻梁、锁骨和肩部是连续柔润反光，不加入银色闪片。
- 两者：脸、颈、肩与可见手部妆面协调，背景与衣服不随肤色一起提亮；不改变五官或身体比例。细节仍需避免重复压纹，用户满意不代表微观纹理已完全真实。

### 造型已认可后的局部加强
仅用于用户已认可当前成片并明确要求局部加强的后续修改。根据当轮要求填写修改部位、妆色、强度与指定保留项；不提供可被首次生成误用的整套冻结提示词。历史认可针对上述两套成片，不代表应冻结新身份照的动作、发型、服装或背景，跨人物与跨模型复现仍需验证。
