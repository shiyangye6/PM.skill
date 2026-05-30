# <Skill Display Name>

## 一句话

<用一句话说明这个 skill 能帮用户完成什么产品工作。>

## 适合谁

- <目标用户 1>
- <目标用户 2>
- <目标用户 3>

## 适合解决什么问题

- <问题 1>
- <问题 2>
- <问题 3>

## 安装

本 Skill 基于开放的 Agent Skills 结构，可在 Claude Code、Codex、Cursor 等 skills-compatible AI agent runtime 中运行。

### 方式一：一句话让 Agent 安装（最简单）

在 Claude Code、Codex、Cursor 等支持 GitHub Skill 安装的工具里，直接发送：

```text
帮我安装这个 skill：<repo-url>
```

如果你的 agent 支持从 GitHub 安装 skills，它会自动拉取仓库并安装到对应目录。

### 方式二：一行命令安装

```bash
npx skills add <owner>/<repo>
```

通用 CLI 安装器会自动识别当前 runtime，并把 Skill 放到正确目录。需要指定 runtime 时，可加参数：

```bash
npx skills add <owner>/<repo> -a claude-code
npx skills add <owner>/<repo> -a codex
npx skills add <owner>/<repo> -a cursor
```

### 方式三：手动安装

如果上面两种方式不可用，可以手动克隆到对应目录：

| Runtime | 安装路径 |
| --- | --- |
| Claude Code | `~/.claude/skills/<skill-id>/` |
| Codex | `~/.codex/skills/<skill-id>/` |
| Cursor | `~/.cursor/skills/<skill-id>/` |

Claude 本地 skill 示例：

```bash
git clone <repo-url> ~/.claude/skills/<skill-id>
```

Windows PowerShell 示例：

```powershell
git clone <repo-url> "$env:USERPROFILE\.claude\skills\<skill-id>"
```

Codex 本地 skill 示例：

```bash
git clone <repo-url> ~/.codex/skills/<skill-id>
```

### 方式四：不安装，直接当 Prompt 用

如果你的工具暂时不支持 Agent Skills 自动加载，也可以直接复制 `SKILL.md` 的内容粘贴进对话。

## 使用

```text
请使用 <skill-id> 帮我审查下面这个产品想法，并输出第一版 Spec.md：

<粘贴产品想法>
```

或：

```text
请使用 <skill-id> 从 <方法论视角> 帮我判断这个 MVP 范围是否过大。
```

安装后可以这样触发：

```text
使用 <skill-id> 帮我审查这个产品想法。
```

## 仓库结构

```text
.
├── README.md
├── SKILL.md
├── references/
│   └── sources.md
└── examples/
    └── sample-output.md
```

## 能力边界

这个 skill 基于公开材料蒸馏方法论，不代表本人授权，也不声称能复刻某位真实人物的完整判断。

它适合做产品分析、文档生成、MVP 取舍和思路校准，不适合替代真实用户研究、商业尽调、法律审查或技术架构评审。

## 主索引

本 skill 属于 [`产品经理 Skill 图鉴`](https://github.com/shiyangye6/PM.skill) 目录。

## 关于作者

我是小叶，正在持续整理和蒸馏适合独立开发者、AI 编程新人使用的产品经理方法论 Skill。

如果你也在做 AI 产品、独立开发、产品经理训练，或者想一起完善这些 Skill，欢迎通过公众号联系我，一起讨论和共创。

- 公众号：江城AI小叶
