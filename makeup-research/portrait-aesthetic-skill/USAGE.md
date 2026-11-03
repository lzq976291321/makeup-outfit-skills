# 使用与安装

本包是模型无关的文本 Skill，不包含生图程序、模型权重、账户配置或原人物照片。它提供参考分析、提示词生成和结果检查方法，不保证任何模型逐字遵循。

## 安装
解压后将完整 `portrait-aesthetic-skill` 文件夹复制到所用环境的技能目录，保留目录内引用关系。

- Codex：通常为 `~/.codex/skills/portrait-aesthetic-skill/`。
- Claude Code：可放在项目的 `.claude/skills/portrait-aesthetic-skill/`，或个人的 `~/.claude/skills/portrait-aesthetic-skill/`。

以上为常见本地目录约定，实际以你正在使用的客户端配置为准。本包未自动安装到本机技能目录。已完成一次固定人物生成与一次妆面加强编辑，最终效果获用户认可。

## 直接使用
在支持技能的环境中按名称调用，或直接让助手读取 `SKILL.md`：

> 使用 portrait-aesthetic-skill。图 1 是人物 A 的身份参考，图 2 只提供摄影风格。保留 A 的肤色与脸部比例，换成深色针织和单手扶领，输出 4:5 人像提示词与检查清单。

> 分析这张新参考图，提炼三个可以迁移的视觉关系。不要复制人物长相，给一个窗光版本。

> 检查这张生成图的手部、首饰接触和身份一致性，给出一次局部修复提示词。

## 文件地图
- `SKILL.md`：触发范围、核心判断与工作流。
- `references/visual-analysis.md`：本次原图观察、推断边界和可迁移规律。
- `references/photography-decisions.md`：身份、光线、妆容、手部、材质与构图的具体决策。
- `references/prompt-template.md`：参数卡、正向与负面模板、模型参数边界。
- `references/examples.md`：三个跨人物/场景示例及局部修复示例。
- `references/quality-check.md`：检查标准、修复优先级和验收记录。

验证范围：本包可检查结构、引用与内容覆盖；通用示例仍为未生成提示词；冷白透粉配方已在本次指定人物的一次编辑中获用户认可，跨人物与跨模型效果尚未验证。

- `references/porcelain-rose-flash.md`：已认可的冷白透粉闪光妆配方与编辑模板。
