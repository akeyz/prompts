[English Version](README.en.md) | [现代文版](README.md)

# 御AI秘笈：正心诚意，化育天工

## 此乃何物？

夫AI者，天工开物，潜力无穷，然其心猿意马，代码纷繁，犹如未琢之璞。今有此秘笈，非为强令，乃循循善诱，**以正AI之心，化其顽性**，使其由混沌归于清明，代码合乎规矩，犹如良匠运斤，精准无碍。此非朝夕之功，需持之以恒，方能驯化天工，为我所用。

## 何人需此秘笈？

*   **诸位匠人**：工欲善其事，必先利其器。AI虽为利器，亦需调教，方能得心应手，代码如行云流水。
*   **同道团队**：众行者易，独行者难。团队协作，若AI代码杂乱无章，则如沙上建塔，倾覆在即。此笈可助AI融入集体，同心同德。
*   **格物致知者**：欲探AI之本源，穷其奥秘，非止于表面之功。此笈助尔格物，以臻化境。
*   **运筹帷幄者**：明察秋毫，洞悉真需。AI若能领会真意，不生虚妄，则如虎添翼。

## 法器宝库

此秘笈所载，乃调御AI之法门，循序渐进，层层深入：

*   **正心之法**：定其心性，明其根本，AI之行为准则。
*   **格物之道**：阐明优劣，示以典范，AI代码之戒律。
*   **演化之式**：顺其自然，因势利导，化繁为简之流程。
*   **利器之用**：善假于物，而非役于物，AI工具运用之巧。

## 秘笈各卷详解

`[.github/instructions/](.github/instructions/)` 目录所藏，皆为驯化AI之良方：

### 总纲领
*   `[.github/instructions/overview.md](.github/instructions/overview.md)`：此乃全局之策，统御诸法，以成AI调教之大业。

### 炼心篇（核心行为）
*   `[.github/instructions/memory-bank.instructions.md](.github/instructions/memory-bank.instructions.md)`：建AI之“藏经阁”，使其不昧前尘，温故知新。可谓革故鼎新之举。
*   `[.github/instructions/response-and-prompt-guidelines.md](.github/instructions/response-and-prompt-guidelines.md)`：正其言，使其沟通有度，如君子之风，远避繁冗。内含八股文章之精义。
*   `[.github/instructions/programming-workflow.md](.github/instructions/programming-workflow.md)`：AI之“格物、致知、诚意、正心、修身”流程，防微杜渐，免蹈覆辙。
*   `[.github/instructions/workflow-and-task-splitting.md](.github/instructions/workflow-and-task-splitting.md)`：授AI以“庖丁解牛”之技，化繁为简，从容不迫（MECE心法）。

### 品鉴篇（代码质量）
*   `[.github/instructions/code-standards.md](.github/instructions/code-standards.md)`：代码之“礼义廉耻”，清净庄严，如琢如磨（SOLID、DRY诸法）。
*   `[.github/instructions/avoid-bad-smells.md](.github/instructions/avoid-bad-smells.md)`：代码之“病灶”与“魔障”大全。AI当避之如蛇蝎，远三毒，净六根。
*   `[.github/instructions/testing-guidelines.md](.github/instructions/testing-guidelines.md)`：演练兵法，务求实效，而非纸上谈兵。覆盖周全，方保万无一失。

### 开物篇（流程工程）
*   `[.github/instructions/req.md](.github/instructions/req.md)`：化虚为实，点石成金。循序引导，使AI洞明需求，如拨云见日。
*   `[.github/instructions/ba.md](.github/instructions/ba.md)`：专为“运筹者”打造，AI辅助擘画“用户故事”，巨细靡遗，层层确认。

### 神通篇（高级技巧）
*   `[.github/instructions/sequential-thinking.md](.github/instructions/sequential-thinking.md)`：启AI之“灵台”，展“序进思维”之神通，应对复杂如反掌。
*   `[.github/instructions/shortcut-system-instruction.md](.github/instructions/shortcut-system-instruction.md)`：设“快捷方式”之符咒，一触即发，提升效能。如 `r!`、`d!`、`t!` 等，皆随心所欲。

## 如何修习此法

1.  **灌顶**：将此秘笈心法，或链接，或复制，注入尔之AI（如Copilot、自定义GPT等）灵台，通常于其“系统提示”或“知识库”中设定。
2.  **静观**：观AI之行，由桀骜不驯，渐入佳境，成为得力臂助。
3.  **精进**：此法亦需与时俱进，随项目之特性，灵活变通，日臻完善。

## 紫电青霜令：VS Code御AI之章 (正确格式！)

欲于VS Code之内，直接调教Copilot，当循章法：

1.  启VS Code之“设定”（`Ctrl+,` 或 `Cmd+,`）。
2.  索 `github.copilot.chat.codeGeneration.instructions`。
3.  增列条目，各为对象，内含 `text` 或 `file` 之钥。示例如下：

```jsonc
"github.copilot.chat.codeGeneration.instructions": [
    { "text": "警之！代码勿与尘世已存之码雷同。" },
    { "file": "../prompts/.github/instructions/req.md" },
    { "file": "../prompts/.github/instructions/ba.md" },
    { "file": "../prompts/.github/instructions/overview.md" },
    { "file": "../prompts/.github/instructions/memory-bank.instructions.md" },
    { "file": "../prompts/.github/instructions/code-standards.md" },
    { "file": "../prompts/.github/instructions/workflow-and-task-splitting.md" },
    { "file": "../prompts/.github/instructions/programming-workflow.md" },
    { "file": "../prompts/.github/instructions/response-and-prompt-guidelines.md" },
    { "file": "../prompts/.github/instructions/testing-guidelines.md" },
    { "file": "../prompts/.github/instructions/avoid-bad-smells.md" },
    { "file": "../prompts/.github/instructions/shortcut-system-instruction.md" }
]
```
4. 存之，重启Copilot Chat，以纳新法。
5. 观Copilot是否俯首听命（或勉力为之）。

**心法要诀：** 文件路径宜用相对之道，亦可自定义箴言。愈精愈详，则AI愈能心领神会。

## 警示箴言

驯化天工，乃精微之道，非一蹴而就，亦非万应灵丹。结果或因AI之悟性、指令之巧妙而异。倘若AI因此恃才傲物，桀骜不驯，务必戒慎恐惧，善加引导。运用之妙，存乎一心。
