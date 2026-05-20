# SOLO 技能：文献深度解析

一个可复用的 Agent Skill，用于科学文献的逐段对照深度解析，支持中英双语对照、图表深度解读、结构化报告生成。

## 功能特点

- **逐段对照解析**：英文原文 + 中文翻译 + 术语解释，三栏对照
- **图表深度解读**：每张组图的每个小图（a, b, c...）逐一分析
- **方法总结**：制备方法、动物模型、检测技术的结构化汇总表
- **结论与意义**：主要发现、临床转化潜力、研究局限性
- **术语表**：核心术语中英对照及定义
- **批量处理**：支持本地文件夹中多篇PDF的批量解析
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

**必须显式调用**，AI 不会自动触发此技能。

### 单篇PDF

上传PDF后说：
```
用 literature-analysis 解析这篇文献
```

### 多篇PDF

上传多个PDF后说：
```
用 literature-analysis 解析这些文献，合并为一个报告
```

### 本地文件夹（Codex CLI）

```
用 literature-analysis 解析 /Users/xxx/papers/ 文件夹中的所有PDF
```

### 快速模式

```
用 literature-analysis 快速解析这篇文献（只看摘要和图表）
```

## 支持的输入类型

| 输入类型 | 说明 |
|---------|------|
| 单篇PDF | 上传一个PDF文件，生成单个报告 |
| 多篇PDF | 上传多个PDF，合并为一个报告（每篇独立章节） |
| 本地文件夹 | 指定文件夹路径，批量解析所有PDF |

## 批量处理输出

多篇文献解析后，报告末尾会添加横向对比表：

| 文献 | 研究主题 | 核心方法 | 主要发现 | 创新点 |
|------|---------|---------|---------|--------|
| 文献1 | ... | ... | ... | ... |
| 文献2 | ... | ... | ... | ... |

## 配置选项

可在请求中追加：

```
ANALYSIS_SCOPE: abstract+results+discussion  # 只解析这三个部分
FIGURE_DEPTH: brief                          # 图表简要解析
OUTPUT_SEPARATE: true                        # 多篇文献分别生成独立报告
```

## 仓库结构

```
solo-skill-literature-analysis/
├── SKILL.md                          # 核心技能文件
├── README.md                         # 本文件
├── INSTALL.md                        # 安装指南
├── config.json                       # 技能元数据
├── variants/                         # 变体版本
│   ├── quick-analysis.md             # 快速版
│   ├── full-analysis.md              # 完整版
│   └── batch-analysis.md             # 批量版
└── examples/
    └── sample-output.md              # 输出示例
```

## 系统要求

- Claude Code 或 OpenAI Codex CLI
- PDF 文献文件（建议英文文献）
- 输出格式：.docx

## 许可证

MIT License - 可自由使用、修改和分发。
