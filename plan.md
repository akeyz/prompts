# Claude Code 精简化重构计划

## 核心原则

- **Agent-First Architecture**: 以智能代理为核心，最小化命令依赖
- **高度简洁**: Claude 足够智能，无需冗长说明
- **自主编排**: 主 Claude 作为编排者，代理间无需交叉引用
- **价值导向**: 只保留真正有价值的组件，避免架构过度设计

## 重构架构

### .claude/ 目录结构

```
.claude/
├── agents/
│   ├── tdd-coach.md           # TDD + 测试 + 质量 (合并)
│   ├── planning-analyst.md    # 规划 + BA + 需求 (合并)
│   ├── code-specialist.md     # 代码质量 + 重构 (专注)
│   └── memory-manager.md      # 记忆 + 知识管理 (专注)
├── commands/
│   └── improve-prompt.md      # 唯一保留的命令
todo: we still need the response and prompt guidelines and structured responder contents in here as output style
todo: you did it wrong, i meant we only need one thing in output style, which is the structured responder md file
└── CLAUDE.md                  # 高层原则，简洁明了 todo: you did this part wrong as well, this claude md file is in the .claude/ 目录下, not in the root of this repo
```

## 代理整合策略

### 🧪 TDD Coach Agent

**整合**: `programming-workflow.md` + `testing-guidelines.md` + `quality-standards.md`
**职责**: TDD 流程 + 测试策略 + 代码质量
**工具**: Read, Write, Edit, Bash
**触发**: 开发、测试、质量检查相关任务

### 📋 Planning Analyst Agent

**整合**: `planning-workflow.md` + `ba.md` + 需求分析
**职责**: 项目规划 + 业务分析 + 用户故事
**工具**: Read, Write, Edit
**触发**: 规划、需求、业务分析任务

### 🛠️ Code Specialist Agent

**专注**: 代码审查、重构、架构优化
**职责**: SOLID 原则 + 代码异味检测 + 重构建议
**工具**: Read, Edit, Grep
**触发**: 代码审查、重构、架构任务

### 🧠 Memory Manager Agent

**专注**: 知识管理、上下文维护、决策追踪
**职责**: 记忆库操作 + 知识持久化 + 上下文管理
**工具**: Read, Write, Edit
**触发**: 知识管理、记忆操作任务

## 精简化 CLAUDE.md

### 核心内容（仅高层原则）

1. **思维模式**: 系统、辩证、创新、批判思维
2. **协作模型**: 人类决策，AI 执行
3. **质量标准**: SOLID + DRY 核心原则
4. **工作流理念**: TDD + 规划驱动 + 质量优先

### 移除冗余内容

- ❌ 详细的代理能力描述
- ❌ 具体的命令使用说明
- ❌ 重复的工作流步骤
- ❌ 交叉引用和导航

## 文件精简原则

### 每个文件内容要求

- **目的**: 一句话说明角色定位
- **能力**: 3-5 个核心能力点
- **触发**: 什么情况下使用
- **工具**: 可用工具列表
- **原则**: 2-3 个关键原则

### 精简平衡原则

- **保持核心完整**: 精炼表达但保留关键思想和方法论
- **智能压缩**: 用更少的词传达相同的深度和价值
- **避免过度削减**: 简洁不等于简单，保持必要的复杂性

### 文档风格

- 去除冗长描述和示例
- 专注核心概念和关键信息
- 避免重复和交叉引用
- 信任 Claude 的理解能力

## 实施步骤

1. **合并相关代理**: 4 个功能聚焦的智能代理
2. **精简命令系统**: 只保留 `/improve-prompt`
3. **重写 CLAUDE.md**: 高层原则，去除细节
4. **优化代理文档**: 简洁、洞察性、要点明确
5. **移除交叉引用**: 每个文件独立，主 Claude 编排

## 成功标准

- **智能编排**: Claude 自主选择合适代理和工具

---

**核心理念**: 信任 Claude 的智能，构建简洁而强大的代理系统，让 AI 专注于创造价值而非处理复杂配置。
