# SOLO 技能：文献深度解析

一个可复用的 Agent Skill，用于科学文献的逐段对照深度解析，支持中英双语对照、图表深度解读、结构化报告生成。

## 功能特点

- **逐段对照解析**：英文原文 + 中文翻译 + 术语解释，三栏对照
- **图表深度解读**：每张组图的每个小图（a, b, c...）逐一分析
- **方法总结**：制备方法、动物模型、检测技术的结构化汇总表
- **结论与意义**：主要发现、临床转化潜力、研究局限性
- **术语表**：核心术语中英对照及定义
- **输出格式**：专业 Word 文档（.docx）

## 安装方法

### Claude Code

```bash
mkdir -p ~/.claude/skills
cd ~/.claude/skills
git clone https://github.com/nbxhh0815-dotcom/solo-skill-literature-analysis.git literature-analysis
```

### OpenAI Codex CLI

```bash
mkdir -p ~/.codex/skills
cd ~/.codex/skills
git clone https://github.com/nbxhh0815-dotcom/solo-skill-literature-analysis.git literature-analysis
```

> 📖 详细安装说明请查看 [INSTALL.md](INSTALL.md)

## 使用方法

安装后，在 Claude Code 或 Codex CLI 中直接说：

```
解析这篇文献
```

或上传 PDF 后说：

```
请对这篇PDF进行深度解析
```

AI 会自动识别并调用此技能，无需手动复制提示词。

## 仓库结构

```
solo-skill-literature-analysis/
├── SKILL.md                          # 核心技能文件（Claude Code / Codex 格式）
├── README.md                         # 本文件
├── INSTALL.md                        # 安装指南
├── config.json                       # 技能元数据
├── variants/                         # 变体版本
│   ├── quick-analysis.md             # 快速版（仅摘要+图表）
│   ├── full-analysis.md              # 完整版（全部章节）
│   └── batch-analysis.md             # 批量版（多篇文献）
└── examples/
    └── sample-output.md              # 输出示例结构
```

## 配置选项

可在请求中追加以下选项：

```
ANALYSIS_SCOPE: abstract+results+discussion   # 只解析这三个部分
FIGURE_DEPTH: brief                           # 图表简要解析
BATCH_MODE: true                              # 多篇文献合并报告
```

## 输出示例

解析报告包含以下章节：

1. **文献概述**：研究背景、目的、创新点
2. **摘要逐段对照**：原文 + 翻译 + 术语表
3. **引言逐段对照**：原文 + 翻译 + 术语表
4. **图表深度解析**：每张图每个小图的详细分析
5. **方法总结**：制备方法、动物模型、检测方法汇总表
6. **结论与意义**：主要结论、转化意义、局限性
7. **术语表**：核心术语中英对照

## 系统要求

- Claude Code 或 OpenAI Codex CLI
- PDF 文献文件（建议英文文献）
- 输出格式：.docx

## 许可证

MIT License - 可自由使用、修改和分发。
