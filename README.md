[English Version](README.en.md)

# AI 代理指令框架

## 概述

本代码仓库包含一套全面的系统指令，旨在指导 AI 代理（如 GitHub Copilot、Cline、Roo Code 及类似平台）精确、高质量并有条不紊地执行复杂的软件开发任务。

这些指令旨在通过强制执行编码、设计、测试、工作流管理和人机协作方面的既定最佳实践来增强 AI 代理的能力。

## 谁能受益？

该框架对以下人员有益：

*   **开发人员**：使用或构建 AI 辅助编码工具，并寻求标准化 AI 行为的开发人员。
*   **团队**：希望将 AI 代理集成到其软件开发生命周期中，并获得一致且高质量输出的团队。
*   **研究人员和工程师**：致力于提高 AI 生成代码和开发过程的可靠性、质量和可预测性的研究人员和工程师。
*   **业务分析师和产品负责人**：与 AI 代理协作进行需求获取和用户故事生成的业务分析师和产品负责人。

## 指令模块

这些指令被组织成几个关键模块，反映了 `[.github/instructions/overview.md](.github/instructions/overview.md)` 中概述的结构：

*   **核心行为定义**：定义代理操作和交互的基本原则。
*   **标准与质量规范**：确保所有生成工件和流程卓越的质量保障。
*   **流程模板**：将概念转化为可实施解决方案的系统化工作流。
*   **工具使用指南**：利用专门（可能是假设的）工具加速复杂认知任务的指南。

## 详细文件说明

以下是位于 `[.github/instructions/](.github/instructions/)` 目录中每个指令文件的说明：

### 总体概述
*   `[.github/instructions/overview.md](.github/instructions/overview.md)`: 提供所有指令模块及其战略整合的高级概览。

### 核心行为定义
*   `[.github/instructions/memory-bank.instructions.md](.github/instructions/memory-bank.instructions.md)`: 详细说明“记忆库”系统，这是 AI 代理跨会话保持项目知识和上下文的关键组件。它概述了记忆文件的结构（例如 `projectbrief.md`、`activeContext.md`）并定义了其使用和更新的工作流程。
*   `[.github/instructions/response-and-prompt-guidelines.md](.github/instructions/response-and-prompt-guidelines.md)`: 概述了 AI 代理的结构化交互协议和响应格式，包括语言使用（例如，用户解释使用中文，技术术语使用英文）和强制性的8段式响应结构。
*   `[.github/instructions/programming-workflow.md](.github/instructions/programming-workflow.md)`: 为 AI 代理详细制定了以测试驱动开发（TDD）为核心的开发生命周期。该工作流涵盖从准备和理解（包括记忆库查阅）到设计、测试实现、编码、重构及最终审查的各个阶段。
*   `[.github/instructions/workflow-and-task-splitting.md](.github/instructions/workflow-and-task-splitting.md)`: 描述了将复杂需求分解为更小、可操作且可验证子任务的核心原则（MECE、明确目标、可管理大小、优先级、独立性、可验证性）和系统化流程。

### 标准与质量规范
*   `[.github/instructions/code-standards.md](.github/instructions/code-standards.md)`: 指定整洁代码原则、类/方法设计最佳实践（SOLID、DRY）、数据库、DevOps 和特定技术栈（如 Java/Spring Boot）的标准。
*   `[.github/instructions/avoid-bad-smells.md](.github/instructions/avoid-bad-smells.md)`: 列出 AI 代理必须主动识别并避免的代码异味（例如，重复代码、长方法、特性依恋、魔法数）和反模式（例如，输入问题、接口臃肿、贫血领域模型）。
*   `[.github/instructions/testing-guidelines.md](.github/instructions/testing-guidelines.md)`: 提供设计和实现高质量测试的指南，包括测试用例结构和断言最佳实践。

### 流程模板
*   `[.github/instructions/req.md](.github/instructions/req.md)`: 定义了一个工作流程，通过一个单一的、迭代优化的 Markdown 文档，将模糊的想法转化为具体的实施计划，涵盖构思、需求、任务、设计和测试用例等阶段，并采用“暂停-提问-优化-继续”的交互模型。
*   `[.github/instructions/ba.md](.github/instructions/ba.md)`: 指导 AI 助手支持业务分析师（BA）创建用户故事，强调敏捷最佳实践和协作式“暂停-提问-优化-继续”模型。

### 工具使用指南
*   `[.github/instructions/sequential-thinking.md](.github/instructions/sequential-thinking.md)`: 解释如何使用假设的 `sequentialthinking` MCP 工具进行动态、反思性问题解决和复杂任务分解。
*   `[.github/instructions/shortcut-system-instruction.md](.github/instructions/shortcut-system-instruction.md)`: 定义 AI 代理应如何识别和执行用户定义的快捷命令（例如 `d!`、`t!`、`plan!`），以触发各种开发任务的特定工作流程。

## 如何使用

这些说明主要用作参与软件开发的高级 AI 代理的系统提示或指导文件。开发人员和团队可以：

*   将这些说明集成到他们的 AI 交互框架中。
*   将其用作为 AI 助手制作有效提示的参考。
*   根据特定的项目需求和 AI 能力调整和扩展它们。

通过遵守此框架，AI 代理可以生成更可靠、可维护和高质量的软件，同时更有效地与人类开发人员和利益相关者协作。

