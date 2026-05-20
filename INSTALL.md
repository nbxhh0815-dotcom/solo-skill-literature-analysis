# 安装与使用指南

本技能支持在 **Claude Code** 和 **OpenAI Codex CLI** 中直接调用。

---

## Claude Code 使用方法

### 安装步骤

1. 打开终端，创建技能目录：
   ```bash
   mkdir -p ~/.claude/skills
   ```

2. 克隆技能仓库：
   ```bash
   cd ~/.claude/skills
   git clone https://github.com/nbxhh0815-dotcom/solo-skill-literature-analysis.git literature-analysis
   ```

3. 验证安装：
   ```bash
   ls ~/.claude/skills/literature-analysis/SKILL.md
   ```
   应显示文件路径，表示安装成功。

4. 重启 Claude Code（如果正在运行）

### 使用方法

#### 方式一：上传PDF文件

1. 在 Claude Code 中上传 PDF 文件
2. 输入：
   ```
   用 literature-analysis 解析这篇文献
   ```

#### 方式二：指定本地文件路径

```
用 literature-analysis 解析 /Users/你的用户名/Downloads/paper.pdf
```

#### 方式三：批量解析文件夹

```
用 literature-analysis 解析 /Users/你的用户名/Documents/papers/ 文件夹中的所有PDF
```

### 常用命令示例

| 场景 | 命令 |
|------|------|
| 单篇解析 | `用 literature-analysis 解析这篇文献` |
| 快速解析 | `用 literature-analysis 快速解析这篇文献` |
| 批量解析 | `用 literature-analysis 解析这个文件夹中的所有PDF` |
| 指定范围 | `用 literature-analysis 解析这篇文献，只看摘要和结果` |

---

## OpenAI Codex CLI 使用方法

### 安装步骤

1. 打开终端，创建技能目录：
   ```bash
   mkdir -p ~/.codex/skills
   ```

2. 克隆技能仓库：
   ```bash
   cd ~/.codex/skills
   git clone https://github.com/nbxhh0815-dotcom/solo-skill-literature-analysis.git literature-analysis
   ```

3. 验证安装：
   ```bash
   ls ~/.codex/skills/literature-analysis/SKILL.md
   ```

### 使用方法

#### 方式一：显式调用技能

在 Codex CLI 中输入：
```
用 literature-analysis 解析 /path/to/paper.pdf
```

#### 方式二：使用 $ 前缀调用

```
$literature-analysis 解析 /path/to/papers/ 文件夹中的所有PDF
```

#### 方式三：批量处理

```
用 literature-analysis 批量解析以下文件夹：/Users/xxx/Documents/papers/
```

### 常用命令示例

| 场景 | 命令 |
|------|------|
| 单篇解析 | `用 literature-analysis 解析 ~/Downloads/paper.pdf` |
| 批量解析 | `用 literature-analysis 解析 ~/Documents/papers/` |
| 快速模式 | `用 literature-analysis 快速解析这篇文献` |
| 指定输出 | `用 literature-analysis 解析这篇文献，输出到 ~/Reports/` |

---

## 目录结构验证

安装成功后，目录结构应为：

```
~/.claude/skills/literature-analysis/     # Claude Code
# 或
~/.codex/skills/literature-analysis/      # Codex CLI

├── SKILL.md           # 核心技能文件（必需）
├── README.md          # 使用说明
├── INSTALL.md         # 本文件
├── config.json        # 配置文件
├── variants/          # 变体版本
│   ├── quick-analysis.md
│   ├── full-analysis.md
│   └── batch-analysis.md
└── examples/
    └── sample-output.md
```

---

## 卸载方法

### Claude Code

```bash
rm -rf ~/.claude/skills/literature-analysis
```

### Codex CLI

```bash
rm -rf ~/.codex/skills/literature-analysis
```

---

## 更新方法

```bash
cd ~/.claude/skills/literature-analysis  # 或 ~/.codex/skills/literature-analysis
git pull origin main
```

---

## 故障排除

### 问题：技能没有被识别

**解决方案**：
1. 确认 `SKILL.md` 文件存在于正确路径
2. 重启 Claude Code 或 Codex CLI
3. 检查文件权限：`chmod -R 755 ~/.claude/skills/literature-analysis`

### 问题：PDF 解析失败

**解决方案**：
1. 确认 PDF 文件未加密
2. 尝试使用绝对路径
3. 检查文件是否损坏

### 问题：批量处理卡住

**解决方案**：
1. 减少文件夹中的 PDF 数量（建议每次不超过10篇）
2. 使用 `FIGURE_DEPTH: brief` 减少解析深度
3. 分批处理

---

## 快速测试

安装后，运行以下命令测试：

```bash
# 创建测试目录
mkdir -p ~/test-papers

# 下载一篇开放获取的 PDF（示例）
curl -o ~/test-papers/test.pdf https://arxiv.org/pdf/2301.00001.pdf

# 在 Claude Code 或 Codex CLI 中测试
用 literature-analysis 解析 ~/test-papers/test.pdf
```

如果成功生成 Word 文档，说明技能安装正确。
