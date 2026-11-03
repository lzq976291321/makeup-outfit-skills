# 妆容与穿搭研究 Skills

用于研究参考图、提炼可迁移配方、固定人物生成或编辑，并检查实际结果。

默认行为：说“生成一张人像”即可使用妆容 Skill；有人物参考图就保留身份换妆，无图就生成新的冷白皮成年人物。招牌效果是冷白透粉底色、眼周细闪、水润唇与鲜明皮肤光泽；用户当轮明确要求可覆盖默认。

## 目录

```text
makeup-research/
  SKILL.md
  portrait-aesthetic-skill/
    SKILL.md
    references/
outfit-research/
  SKILL.md
```

- [妆容研究](makeup-research/SKILL.md)：底妆、色彩、眼唇、细闪、皮肤与身份一致性。
- [冷白透粉闪光妆案例](makeup-research/portrait-aesthetic-skill/SKILL.md)：完整摄影方法与用户认可的妆面配方。
- [穿搭研究](outfit-research/SKILL.md)：版型、配色、材质、配饰与换装检查。

## 使用

让助手读取所需目录的 `SKILL.md`，再提供身份图、风格图和本轮目标。可将两个顶层目录分别复制到所用客户端的技能目录。妆容目录内的案例通过相对路径按需读取；若要独立调用该案例，也可将其单独复制到技能目录。

不包含人物照片、账户配置或模型权重。冷白透粉风格已在一次指定人物编辑中获得用户认可；跨人物、跨模型的稳定性尚未验证。穿搭研究流程尚未单独生图验收。

## Notion

- [妆容研究 Skill](https://app.notion.com/p/40d58286365f81cca57debff5721972c)
- [穿搭研究 Skill](https://app.notion.com/p/40d58286365f81139c3dc70ddcb42b6e)

Notion 与仓库是独立副本，修改一端不会自动同步另一端。
