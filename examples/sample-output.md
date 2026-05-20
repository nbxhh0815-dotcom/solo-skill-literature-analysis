# Sample Output Structure

This document shows the expected structure of a full analysis report.

---

## Document Structure

```
Cover Page
├── Title: 文献深度解析报告
├── Paper Title (bilingual)
├── Journal, Date, Authors, Institution
└── [Page Break]

Section 1: 文献概述
├── 1.1 研究背景
├── 1.2 研究目的
└── 1.3 核心创新点

Section 2: 摘要逐段对照解析
├── H3: 段落1：研究背景与问题
│   └── [3-column table: Original | Translation | Terminology]
├── H3: 段落2：研究方法
│   └── [3-column table]
├── H3: 段落3：主要结果
│   └── [3-column table]
└── H3: 段落4：研究意义
    └── [3-column table]

Section 3: 引言逐段对照解析
├── H3: 段落1：...
│   └── [3-column table]
└── ...

Section 4: 图表深度解析
├── H2: 4.1 Figure 1: [Figure Title]
│   ├── [Subfigure analysis table: Label | Content | Result]
│   ├── [Subfigure analysis table]
│   ├── ...
│   └── Key Conclusion (red text)
├── H2: 4.2 Figure 2: [Figure Title]
│   ├── [Subfigure analysis table]
│   ├── ...
│   └── Key Conclusion (red text)
└── ...

Section 5: 研究方法总结
├── 5.1 纳米材料/药物制备
├── 5.2 动物模型
└── 5.3 主要检测方法 [Summary Table]

Section 6: 研究结论与意义
├── 6.1 主要结论
├── 6.2 临床转化意义
└── 6.3 研究局限与展望

Section 7: 核心术语表
└── [Terminology table: English | Chinese | Definition]

Footer: — 文献解析报告完 —
```

---

## Table Examples

### Paragraph Comparison Table

| 原文 Original | 翻译 Translation |
|---------------|-----------------|
| Rheumatoid arthritis (RA) is a chronic autoimmune disorder... | 类风湿性关节炎（RA）是一种慢性自身免疫性疾病... |

**术语解释：**
- Rheumatoid arthritis (RA): 类风湿性关节炎，以对称性滑膜炎为特征的慢性自身免疫病
- Autoimmune disorder: 自身免疫性疾病，免疫系统攻击自身组织的疾病

### Figure Analysis Table

| 小图 | 实验内容 | 结果解读 |
|------|---------|---------|
| a | DLS表征纳米颗粒粒径和PDI | 粒径~130 nm，PDI<0.1，表明颗粒高度均一 |
| b | TEM观察纳米颗粒形态 | 颗粒呈球形，大小均一，与DLS结果一致 |

**关键结论：** CMLT纳米疫苗具有理想的粒径和均一性。

### Methods Summary Table

| 检测类型 | 方法 | 检测指标 |
|---------|------|---------|
| 理化表征 | DLS、TEM | 粒径、电位、形态 |
| 蛋白表达 | Western blot、ELISA | TSP-1、TGF-β1 |

### Terminology Table

| 英文术语 | 中文翻译 | 定义 |
|---------|---------|------|
| TSP-1 | 血小板反应蛋白-1 | 多功能糖蛋白，可激活TGF-β |
