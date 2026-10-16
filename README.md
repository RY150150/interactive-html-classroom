# 交互式 HTML 教学课堂

将教材、PDF、文档或网址制作成详细、可离线使用的单文件 HTML 教学课堂的 Codex Skill。

## 能做什么

- 先确认学习者基础、学习目标和教学范围，再决定讲解深度和习题难度。
- 建立知识点覆盖表，提供连贯讲解、推导、完整例子、适用条件和反例。
- 设计有实际计算或机制演示的交互，以及附逐项解析的自测。
- 提供搜索、概念速查、阅读进度、答题记录、错题筛选、主题切换和打印。
- 交付无必需外部请求的单文件 HTML，并检查桌面、手机和离线使用。
- 专门检查目录高亮与锚点同步，防止跳转后仍高亮上一节。

这是供 Codex 读取的工作流程与验收要求，不含预制课程内容，也不包含教材原文。实际输出取决于提供的资料、任务范围和可用工具；技能格式校验不能代替内容与交互的实际验证。

## 安装

在尚未安装同名技能的环境中，可将仓库克隆到本地技能目录。以下示例使用 `~/.codex/skills`；若你的客户端使用其他技能目录，请相应调整目标位置。

```sh
git clone https://github.com/RY150150/interactive-html-classroom.git ~/.codex/skills/interactive-html-classroom
```

已存在同名目录时，请先确认其中是否有自定义修改，避免覆盖。安装后通过客户端技能列表确认可用。

## 使用

在 Codex 中指定技能，并提供你的主题与材料：

```text
使用 $interactive-html-classroom，把这些资料制作成交互教学课堂。

主题／教材与版本：
教学范围：
学习者基础：
学习目标：
主要资料：
参考样式（可选）：
输出位置（可选）：
```

主题、范围、基础或目标缺失时，技能要求先询问，等待回答后再确定教学深度。仅修复现有课堂的导航、布局或保存问题时，可以直接处理与教学深度无关的修复。

## 文件结构

```text
interactive-html-classroom/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── navigation.md
    └── verification.md
```

- [SKILL.md](SKILL.md)：主要流程、内容要求与交付约束。
- [agents/openai.yaml](agents/openai.yaml)：技能的界面名称和默认提示词。
- [references/navigation.md](references/navigation.md)：锚点与高亮同步的实现和检查要求。
- [references/verification.md](references/verification.md)：内容、习题、交互、学习记录与离线布局的验收清单。

默认视觉采用米白、深绿色和少量橙色；用户提供的样式、范围和其他明确要求优先。
