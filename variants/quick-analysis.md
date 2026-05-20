# Quick Analysis Variant

> Fast analysis focusing on Abstract + Key Figures only. ~5 min per paper.

## Prompt

请对这篇文献进行「快速深度解析」，生成Word文档报告。按以下流程执行：

【第一步】提取全文，识别文献结构。

【第二步】对摘要的每个段落，生成逐段对照表（原文 + 中文翻译 + 术语解释）。

【第三步】对文章中每张Figure，为每个小图生成简要解析：
- 小图编号 | 核心发现（1-2句话）
每张图后附一段「关键结论」。

【第四步】用表格汇总：
- 主要结论（5条以内）
- 核心术语表（中英文对照，8-10个）

【输出】生成.docx文件，蓝色表头，微软雅黑+Arial字体。

ANALYSIS_SCOPE: abstract+figures
FIGURE_DEPTH: brief
