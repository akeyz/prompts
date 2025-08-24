# Claude Code 全面集成重构计划

## 目标

对 `.github/instructions/` 中的**9 个核心指令文件**进行精准分析和重构，将实用内容精确映射到 Claude Code 的**4 大核心组件**：**Sub-agents（子代理）**、**Slash Commands（斜杠命令）**、**Output Styles（输出风格）**和**CLAUDE.md（记忆系统）**，实现高效的 Claude Code 原生集成。

## 核心映射策略

### 映射原则

- **基础性、持久化内容** → CLAUDE.md（核心思维原则、质量标准、最佳实践）
- **复杂多步骤工作流程** → Sub-agents（需要专业判断和工具组合的任务）
- **快速任务触发器** → Slash Commands（单一目标的快速启动命令）
- **明确价值的交互模式** → Output Styles（有特定格式要求的响应模式）
- **不强制映射**：只保留实用且有价值的映射，避免为了覆盖而创建无意义的组件

### 4 大组件分工

- **Sub-agents**：复杂的多步骤工作流程和专业角色行为（5 个）
- **Slash Commands**：快速启动的单一任务和工作流触发器（7 个）
- **Output Styles**：特定的交互模式和响应格式（1 个）
- **CLAUDE.md**：持久化的知识、原则和配置信息（集成所有基础内容）

## 逐文件详细分解计划

### 1. `foundational-principles.md`

**当前内容**：核心思维原则、人机协作模型、指令框架概览

**映射分解**：

- **CLAUDE.md**: 导入核心思维原则（系统、辩证、创新、批判思维）和人机协作模型作为基础框架，这些是持久化的基础知识，应该始终可用

### 2. `memory-bank.instructions.md`

**当前内容**：知识持久化、会话间记忆管理

**映射分解**：

- **Slash Command**: `/memory` - 快速记忆操作
  - 功能：查看、更新、清理、搜索记忆库
- **CLAUDE.md**: 记忆管理的具体方法和最佳实践

### 3. `response-and-prompt-guidelines.md`

**当前内容**：8 段式响应结构、沟通协议、提示澄清

**映射分解**：

- **Output Style**: `structured-responder.md` - 8 段式响应模式
  - 格式：强制执行 8 段式结构输出
- **Slash Command**: `/improve-prompt` - 提示优化
  - 职责：提示改写、意图澄清、结构化输出、最佳 persona 选择
- **CLAUDE.md**: 沟通协议和语言使用规范

### 4. `programming-workflow.md`

**当前内容**：TDD 生命周期、4 阶段编程流程

**映射分解**：

- **Sub-agent**: `tdd-coach-agent.md` - TDD 教练
  - 职责：指导 4 阶段 TDD 流程（准备 → 设计 → 测试 → 实现 → 审查）
  - 工具：Read, Write, Edit, Bash
- **Slash Command**: `/tdd` - 启动 TDD 循环
  - 功能：初始化 TDD 流程、阶段指导、代码生成
- **CLAUDE.md**: TDD 核心原则和阶段检查清单

### 5. `planning-workflow.md`

**当前内容**：想法到实现的 4 阶段规划流程、MECE 分解

**映射分解**：

- **Sub-agent**: `planning-specialist-agent.md` - 规划专家
  - 职责：执行 4 阶段规划（想法 → 需求 → 任务 → 设计 → 测试）
  - 工具：Read, Write, Edit
- **Slash Command**: `/plan` - 启动规划工作流
  - 功能：创建规划文档、阶段推进、用户确认
- **CLAUDE.md**: 规划模板、MECE 原则、文档结构

### 6. `quality-standards.md`

**当前内容**：SOLID 原则、代码异味、反模式、质量标准

**映射分解**：

- **Sub-agent**: `code-quality-guardian-agent.md` - 代码质量守护者
  - 职责：质量检查、重构建议、最佳实践应用
  - 工具：Read, Edit, Grep
- **Slash Command**: `/review` - 代码质量审查
  - 功能：全面质量分析、问题检测、改进建议
- **CLAUDE.md**: SOLID 原则、代码异味清单、反模式定义

### 7. `testing-guidelines.md`

**当前内容**：测试设计原则、测试策略、覆盖率要求

**映射分解**：

- **Sub-agent**: `test-architect-agent.md` - 测试架构师
  - 职责：测试设计、覆盖率分析、测试策略制定
  - 工具：Read, Write, Bash
- **CLAUDE.md**: 测试原则、覆盖率标准、测试类型定义

### 8. `ba.md`

**当前内容**：业务分析师协作流程、用户故事撰写

**映射分解**：

- **Sub-agent**: `business-analyst-agent.md` - 业务分析专家
  - 职责：需求分析、用户故事创建、验收标准定义
  - 工具：Read, Write, Edit
- **Slash Command**: `/ba` - 业务分析工作流
  - 功能：史诗分解、用户故事生成、验收标准
- **CLAUDE.md**: BA 工作流模板、用户故事格式

### 9. `shortcut-system-instruction.md`

**当前内容**：快捷命令定义（plan!、r!、d!、t!等）

**映射分解**：

- **全部转换为 Slash Commands**：
  - `plan!` → `/plan`
  - `r!` → `/review`
  - `d!` → `/design`
  - `t!` → `/test`
  - `ba!` → `/ba`
  - `m!` → `/memory`
  - `me!` → `/improve-prompt`
- **CLAUDE.md**: 命令使用指南和快捷键映射表

## 实施文件结构

```
prompts/
├── .github/instructions/           # 保持原文件作为源文档
├── .claude/
│   ├── agents/                     # Sub-agents配置 (5个)
│   │   ├── tdd-coach-agent.md
│   │   ├── planning-specialist-agent.md
│   │   ├── code-quality-guardian-agent.md
│   │   ├── test-architect-agent.md
│   │   └── business-analyst-agent.md
│   ├── commands/                   # Slash Commands (7个)
│   │   ├── memory-bank.md
│   │   ├── improve-prompt.md
│   │   ├── tdd.md
│   │   ├── plan.md
│   │   ├── review.md
│   │   ├── ba.md
│   │   └── design.md
│   └── output-styles/              # Output Styles (1个)
│       └── structured-responder.md
├── claude-config/
│   ├── templates/ todo: no need
│   ├── migration-tools/ todo: no need
│   └── setup.sh todo: this one is enough
```

## 集成工作流示例

### 规划场景

```
用户: "我需要设计一个用户认证系统"
→ /plan 触发规划工作流
→ planning-specialist-agent接管
→ 生成完整的4阶段规划文档
```

### 开发场景

```
用户: "开始实现登录功能"
→ /tdd 启动TDD循环
→ tdd-coach-agent指导
→ 4阶段TDD开发流程
```

### 质量检查场景

```
用户: "检查这段代码质量"
→ /review 启动质量审查
→ code-quality-guardian-agent分析
→ SOLID原则详细检查报告
```

### 业务分析场景

```
用户: "写一个用户登录的需求"
→ /ba 启动业务分析
→ business-analyst-agent接管
→ 完整的史诗和用户故事
```

## 成功指标

### 功能完整性

- [ ] 9 个核心指令文件 100% 有效覆盖
- [ ] 5 个专业 sub-agents 正常工作
- [ ] 7 个核心 slash commands 可用
- [ ] 1 个实用 output style 可切换
- [ ] CLAUDE.md 包含所有核心知识

### 用户体验

- [ ] 3 步快速配置流程
- [ ] 角色无缝切换
- [ ] 工作流自动化
- [ ] 专业化响应模式

### 技术实现

- [ ] Sub-agents 独立运行
- [ ] Commands 快速响应
- [ ] Style 正确输出格式
- [ ] Memory 正确导入知识

## 详细映射总结

| 原始文件                | Sub-agent                   | Command         | Output Style         | CLAUDE.md 内容     |
| ----------------------- | --------------------------- | --------------- | -------------------- | ------------------ |
| foundational-principles | -                           | -               | -                    | 思维原则、协作模型 |
| memory-bank             | -                           | /memory         | -                    | 记忆管理方法       |
| response-guidelines     | -                           | /improve-prompt | structured-responder | 沟通协议           |
| programming-workflow    | tdd-coach-agent             | /tdd            | -                    | TDD 原则清单       |
| planning-workflow       | planning-specialist-agent   | /plan           | -                    | 规划模板、MECE     |
| quality-standards       | code-quality-guardian-agent | /review         | -                    | SOLID、代码异味    |
| testing-guidelines      | test-architect-agent        | -               | -                    | 测试原则标准       |
| ba.md                   | business-analyst-agent      | /ba             | -                    | BA 工作流模板      |
| shortcut-system         | -                           | 全转为 commands | -                    | 命令映射表         |

**跳过的文件**：sequential-thinking.md（按照 todo 反馈跳过）

## 下一步行动

1. **创建 5 个专业 sub-agents**，每个都有明确的职责和工具权限
2. **开发 7 个 slash commands**，实现快速工作流触发
3. **设计 1 个 output style**，提供专业化交互模式
4. **构建增强版 CLAUDE.md**，集成所有核心知识和配置
5. **开发配置工具**，实现一键部署和迁移
