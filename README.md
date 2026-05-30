# Awesome Product Manager Skills

## 面向独立开发者和 AI 编程新人的产品经理 Skill 主索引

这个项目是一个主页面和索引仓库，用来收集、孵化和链接一组“产品经理方法论 Skill”。

每一个成熟的产品经理 Skill 都建议独立成一个 GitHub 仓库，类似：

- `marty-cagan-product-skill`
- `teresa-torres-discovery-skill`
- `yu-jun-product-skill`
- `zhang-xiaolong-product-skill`

当前仓库负责做三件事：

- 展示所有产品经理 Skill 的目录和链接。
- 提供通用的 `pm-spec-writer` 元 Skill，帮助生成第一版产品文档。
- 提供单个产品经理 Skill 的蒸馏、发布和 README 模板。

它不是为了“复刻某个人”，而是为了把公开方法论整理成可被 AI 协作使用的产品工作流。在你做独立产品、AI 应用、小工具、SaaS、内容产品时，它可以帮你快速产出第一版：

- `Spec.md`
- `PRD.md`
- `DevDoc.md`
- MVP 范围
- 用户故事
- 验收标准
- 技术实现说明
- 上线前检查清单

> 目标：让 AI 编程新人少写模糊需求，独立开发者更快把想法变成可以开工的文档。

---

## 快速使用

把下面这段交给 AI 编程工具，并附上你的产品想法：

```text
请使用本项目的 PM.skill 工作流，基于我的想法生成第一版 Spec.md。
先补齐关键假设，再用 3-5 位产品经理方法论视角交叉审视，最后输出可直接给开发使用的文档。

我的想法：
<在这里描述你的产品、目标用户、使用场景、平台、商业目标、已有约束>
```

如果你已经有技术方向，可以要求同时生成开发文档：

```text
请基于 templates/DevDoc.md 生成第一版 DevDoc.md，要求包含数据模型、页面结构、接口草案、状态流转、边界情况和验收标准。
```

---

## 项目结构

```text
.
├── SKILL.md                         # 给 AI 编程工具读取的核心技能说明
├── README.md                        # 项目说明和目录
├── CONTRIBUTING.md                  # 如何新增产品经理方法论
├── catalog/
│   └── skills.yml                   # 产品经理 Skill 注册表
├── personas/
│   ├── product-leaders.md           # 国内外产品经理/产品思想家方法论目录
│   └── archetypes.md                # 抽象后的产品经理原型
├── prompts/
│   ├── generate-spec.md             # 生成 Spec.md 的提示词
│   └── review-spec.md               # 审查 Spec.md 的提示词
├── templates/
│   ├── Spec.md                      # 产品规格文档模板
│   ├── PRD.md                       # 产品需求文档模板
│   ├── DevDoc.md                    # 开发文档模板
│   ├── ProductLeader.SKILL.md       # 单个产品经理 Skill 模板
│   └── SkillRepo.README.md          # 单个 Skill 仓库 README 模板
├── workflows/
│   ├── spec-first.md                # 从想法到第一版 Spec 的流程
│   ├── persona-distillation.md      # 新增产品经理方法论的蒸馏流程
│   └── single-skill-release.md      # 单个 Skill 独立发布流程
└── examples/
    └── indie-ai-app.Spec.md         # 示例：独立 AI 应用第一版 Spec
```

---

## 仓库组织建议

推荐使用“两层结构”：

### 1. 主索引仓库

当前仓库：[`shiyangye6/PM.skill`](https://github.com/shiyangye6/PM.skill)

用途：

- 放总目录。
- 放通用模板。
- 放发布规范。
- 放 `pm-spec-writer` 这种跨人物的元 Skill。
- 链接每个独立产品经理 Skill 仓库。

### 2. 单个 Skill 仓库

每个成熟产品经理方法论单独一个仓库。

建议命名：

```text
<person-or-framework>-product-skill
<person-or-framework>-discovery-skill
<person-or-framework>-growth-skill
```

例如：

```text
marty-cagan-product-skill
teresa-torres-discovery-skill
yu-jun-product-skill
zhang-xiaolong-product-skill
```

每个仓库至少包含：

```text
.
├── README.md
├── SKILL.md
├── references/
│   └── sources.md
└── examples/
    └── sample-output.md
```

### 3. 本地孵化区

`.claude/` 可以继续作为本地蒸馏工作区，不上传到主仓库。

适合放：

- 女娲 skill
- 原始提示词
- 半成品产品经理 skill
- 资料摘要
- 对比实验
- 未清洗的草稿

等某个 skill 稳定后，再从 `.claude/` 拆出来，按 `templates/ProductLeader.SKILL.md` 和 `templates/SkillRepo.README.md` 建独立仓库。

---

## Skill 链接目录

| Skill | 定位 | 状态 | 仓库 |
| --- | --- | --- | --- |
| PM Spec Writer | 通用产品文档生成元 Skill | 已发布 | [shiyangye6/PM.skill](https://github.com/shiyangye6/PM.skill) |
| Marty Cagan Product Skill | 产品发现、赋能团队、结果导向 | 计划中 | 待创建 |
| Teresa Torres Discovery Skill | 持续发现、机会树、用户访谈 | 计划中 | 待创建 |
| Gibson Biddle Strategy Skill | 产品战略、品牌承诺、指标树 | 计划中 | 待创建 |
| Lenny Rachitsky Growth Skill | 冷启动、增长、GTM、playbook | 计划中 | 待创建 |
| Julie Zhuo Design PM Skill | 设计协作、体验评审、清晰表达 | 计划中 | 待创建 |
| Jobs Product Taste Skill | 端到端体验、取舍、产品品味 | 计划中 | 待创建 |
| Yu Jun Product Skill | 用户价值、交易模型、效用分析 | 计划中 | 待创建 |
| Zhang Xiaolong Product Skill | 克制、自然、用户心理、关系链 | 计划中 | 待创建 |
| Zhang Yiming Product Skill | 信息效率、反馈系统、数据迭代 | 计划中 | 待创建 |
| Liang Ning Product Skill | 场景、情绪、痛点爽点、产品人格 | 计划中 | 待创建 |
| Su Jie Product Skill | 需求分析、PRD、产品推进 | 计划中 | 待创建 |
| Growth PM Skill | AARRR、留存、变现、实验 | 计划中 | 待创建 |

详细注册表见 [`catalog/skills.yml`](./catalog/skills.yml)。

---

## 技能列表

### 国际产品方法论

- **Marty Cagan 型** - 强调 empowered product team、产品发现、结果导向、持续验证。
- **Teresa Torres 型** - 强调 continuous discovery、机会解决方案树、用户访谈节奏。
- **Gibson Biddle 型** - 强调产品战略、品牌承诺、指标树和取舍。
- **Lenny Rachitsky 型** - 强调增长、冷启动、市场进入、可执行 playbook。
- **Julie Zhuo 型** - 强调设计协作、团队管理、清晰表达和评审机制。
- **Jobs 型产品直觉** - 强调端到端体验、少即是多、体验完整性和品味标准。

### 国内产品方法论

- **俞军型** - 强调用户价值、交易模型、效用、供需匹配。
- **张小龙型** - 强调克制、默认自然、用户心理、社交关系链和长期体验。
- **张一鸣型** - 强调信息效率、数据反馈、人才密度、系统迭代。
- **梁宁型** - 强调用户情绪、场景、痛点、爽点、痒点和产品人格。
- **苏杰型** - 强调产品经理职业化、需求分析、产品规划、项目推进。
- **增长产品型** - 强调获客、激活、留存、变现和推荐闭环。

> 以上是基于公开方法论的抽象工作视角，不代表任何本人授权或完整思想复刻。

---

## 推荐工作流

1. 用 `prompts/generate-spec.md` 收集想法。
2. 用 `workflows/spec-first.md` 补齐用户、场景、价值、范围和约束。
3. 从 `personas/product-leaders.md` 选择 3-5 个产品视角进行交叉审视。
4. 用 `templates/Spec.md` 生成第一版规格。
5. 如果要开工，用 `templates/DevDoc.md` 生成开发文档。
6. 用 `prompts/review-spec.md` 做一次范围、风险、指标和验收审查。

---

## 适合的场景

- 独立开发者从一个模糊点子开始做 MVP。
- AI 编程新人不知道如何写需求给 Cursor、Codex、Claude Code、Copilot。
- 小团队需要先把产品想清楚，再决定是否投入开发。
- 想把一个工具、插件、SaaS、知识产品、内容社区、AI Agent 做成第一版可交付文档。

---

## 不适合的场景

- 需要冒充某位真实产品经理本人。
- 需要未经验证地引用私人观点、内部资料或非公开材料。
- 需要替代用户研究、法务审查、安全审查或商业尽调。
- 产品已经非常复杂，需要完整技术架构评审和多轮真实用户验证。

---

## 一句话

把顶级产品经理的公开方法论，压缩成独立开发者能直接开工的第一版产品文档。
