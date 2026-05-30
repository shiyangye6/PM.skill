# Single Skill Release Workflow

这个流程用于把 `.claude/` 中孵化成熟的产品经理 skill，拆成一个独立 GitHub 仓库。

## 什么时候应该单独建仓库

满足以下条件再建：

- `SKILL.md` 已经可以独立使用。
- 有清楚的触发场景和边界。
- 至少有一个示例输出。
- 公开资料来源已经整理到 `references/sources.md`。
- README 能让陌生人 30 秒内看懂用途。
- 不依赖主仓库里的私有草稿或本地文件。

如果只是半成品、资料摘要或提示词实验，先留在 `.claude/`。

## 推荐仓库结构

```text
<skill-repo>/
├── README.md
├── SKILL.md
├── references/
│   └── sources.md
└── examples/
    └── sample-output.md
```

## 发布步骤

1. 从 `templates/ProductLeader.SKILL.md` 复制生成 `SKILL.md`。
2. 从 `templates/SkillRepo.README.md` 复制生成 `README.md`。
3. 新建 `references/sources.md`，只列公开来源和自己的摘要。
4. 新建 `examples/sample-output.md`，展示一次真实产品问题的输出。
5. 本地初始化 git 仓库。
6. 上传到独立 GitHub 仓库。
7. 回到主索引仓库，更新：
   - `README.md` 的 Skill 链接目录
   - `catalog/skills.yml` 的 `status` 和 `repo`

## 命名建议

```text
marty-cagan-product-skill
teresa-torres-discovery-skill
gibson-biddle-strategy-skill
lenny-rachitsky-growth-skill
julie-zhuo-design-pm-skill
yu-jun-product-skill
zhang-xiaolong-product-skill
zhang-yiming-product-skill
liang-ning-product-skill
su-jie-product-skill
```

## 主仓库更新规则

主仓库只放：

- 已发布 skill 的链接。
- 计划中的 skill 名单。
- 通用模板和流程。
- 元 skill。

主仓库不放：

- 每个人的完整长篇 `SKILL.md`。
- 未整理的语料。
- 女娲生成过程。
- 私人资料或未授权内容。

## 发布质量线

一个单独 skill 仓库至少要回答：

- 这个 skill 什么时候触发？
- 它能产出什么？
- 它不适合做什么？
- 它基于哪些公开来源？
- 用户可以复制哪段 prompt 直接试用？
