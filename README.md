# Editing Toolbar

一个为 Obsidian 提供类 MS-Word 工具栏的插件，支持顶部工具栏和光标跟随工具栏，内置丰富的编辑命令和 AI 功能。

> 基于 [cmenu](https://github.com/chetachiezikeuzor/cMenu-Plugin) 重构和扩展。

## 安装

### 通过 BRAT（推荐）
1. 安装 [BRAT](obsidian://show-plugin?id=obsidian42-brat) 插件
2. 添加仓库 `pengivy1990/obsidian-editing-toolbar`
3. 启用 Editing Toolbar 插件

### 手动安装
1. 从 [Releases](https://github.com/pengivy1990/obsidian-editing-toolbar/releases) 下载 `main.js`、`manifest.json`、`styles.css`
2. 放入 vault 的 `.obsidian/plugins/editing-toolbar/` 目录
3. 在 Obsidian 设置中启用插件

## AI 功能

插件内建 OpenAI 兼容 API 客户端，支持流式重写和补全，无需额外安装其他插件。

### 配置

进入设置 → AI，启用 AI 功能后配置：

| 字段 | 说明 | 示例 |
|------|------|------|
| **Base URL** | API 端点地址 | `https://api.openai.com/v1` |
| **Model** | 模型名称 | `gpt-4o` / `claude-sonnet-4-20250514` |
| **API Key** | 你的密钥 | `sk-...` |
| **Temperature** | 随机性控制 (0-2) | `0.7` |
| **API Format** | 协议格式 | OpenAI Compatible / Ollama |

支持任意 OpenAI 兼容接口，包括：
- **OpenAI** — `https://api.openai.com/v1`
- **OpenRouter** — `https://openrouter.ai/api/v1`
- **本地 Ollama** — `http://localhost:11434`（无需 API Key）
- 其他兼容服务

### 重写
选中文本后，右键菜单选择 **AI Tools** 或使用命令面板触发重写。支持：
- Improve writing、Fix grammar、Make shorter/longer
- Professional/Casual tone
- 翻译（中/英/日/德/法/西）
- Explain、Summarize、Continue
- 自定义提示词模板

### 内联补全
在编辑器中按 `Ctrl+J` 触发 AI 补全（需在内联补全设置中启用）。

### Canvas AI
在 Canvas 视图中，支持节点扩展和全局指令。

## 工具栏功能

### 工具栏样式
- **Top** — 固定在编辑器顶部
- **Following** — 跟随光标位置
- **Tiny** — 紧凑模式

### 内置命令
| 分类 | 命令 |
|------|------|
| 格式 | 加粗、斜体、删除线、下划线、代码、高亮 |
| 颜色 | 字体颜色、背景颜色（格式刷功能） |
| 段落 | 标题 1-6、引用块、列表、待办 |
| 对齐 | 左对齐、居中、右对齐、两端对齐 |
| 插入 | 分割线、表格、Emoji |
| 编辑 | 撤销、重做、缩进/取消缩进 |
| 视图 | 全屏专注、工作区全屏 |

### 自定义
- 支持拖拽排序工具栏按钮
- 支持添加子菜单
- 支持自定义命令图标和名称
- 支持导入/导出配置

## 配合插件
- [Enhanced Editing](obsidian://show-plugin?id=obsidian-canzi-enhanced-editing) — 更多编辑命令
- [Emoji Toolbar](obsidian://show-plugin?id=obsidian-emoji-toolbar) — 快速插入 Emoji
- [Table Generator](https://github.com/Quorafind/Obsidian-Table-Generator/) — 快速插入表格

## License
MIT
