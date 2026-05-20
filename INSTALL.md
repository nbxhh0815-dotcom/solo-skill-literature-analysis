# 安装指南

本技能支持在 **Claude Code** 和 **OpenAI Codex CLI** 中直接调用。

---

## Claude Code 安装方法

### 方法一：手动安装

1. 创建技能目录（如果不存在）：
   ```bash
   mkdir -p ~/.claude/skills
   ```

2. 克隆或下载本仓库到技能目录：
   ```bash
   cd ~/.claude/skills
   git clone https://github.com/nbxhh0815-dotcom/solo-skill-literature-analysis.git literature-analysis
   ```

3. 重启 Claude Code

### 方法二：直接复制文件

1. 下载 `SKILL.md` 文件
2. 放置到 `~/.claude/skills/literature-analysis/SKILL.md`
3. 重启 Claude Code

### 使用方法

在 Claude Code 中直接说：
```
解析这篇文献
```

或上传 PDF 后说：
```
请对这篇PDF进行深度解析
```

Claude 会自动识别并调用此技能。

---

## OpenAI Codex CLI 安装方法

### 方法一：作为 Skill 安装

1. 创建技能目录：
   ```bash
   mkdir -p ~/.codex/skills
   ```

2. 克隆仓库：
   ```bash
   cd ~/.codex/skills
   git clone https://github.com/nbxhh0815-dotcom/solo-skill-literature-analysis.git literature-analysis
   ```

3. 在 Codex 中调用：
   ```
   $literature-analysis 解析这篇文献
   ```

### 方法二：作为 Prompt 安装

1. 创建 prompts 目录：
   ```bash
   mkdir -p ~/.codex/prompts
   ```

2. 复制提示词文件：
   ```bash
   cp SKILL.md ~/.codex/prompts/literature-analysis.md
   ```

3. 在 Codex 中调用：
   ```
   /literature-analysis
   ```

---

## 验证安装

### Claude Code

启动后查看技能是否加载：
```
你有哪些可用的技能？
```

### Codex CLI

查看已安装的技能：
```
/skills
```

---

## 目录结构

安装后的目录结构应为：

```
~/.claude/skills/literature-analysis/    # Claude Code
# 或
~/.codex/skills/literature-analysis/     # Codex CLI

├── SKILL.md           # 核心技能文件（必需）
├── README.md          # 使用说明
├── config.json        # 配置文件
├── variants/          # 变体版本
│   ├── quick-analysis.md
│   ├── full-analysis.md
│   └── batch-analysis.md
└── examples/
    └── sample-output.md
```

---

## 快速测试

安装后，上传任意 PDF 文献，然后说：

```
请用 literature-analysis 技能解析这篇文献
```

如果技能正确安装，Claude/Codex 会自动按照技能定义的流程进行深度解析。
