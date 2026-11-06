# Tech Research Skill (跨 Agent 通用技术调研与方案选型技能)

> 面向工程师、架构师与技术管理者的通用方案调研能力。  
> 告别每次做技术选型、架构设计、方案调研时写长篇累赘的 Prompt。支持一键接入 **DeepSeek Harness (DSH)**、**OpenAI Codex**、**Cursor / Windsurf** 以及任何主流 AI 助手。

---

## 🌟 核心能力

输入一句话需求（例如：`“调研一下移动端离线数据同步方案”` 或 `“调研 GraphQL vs gRPC 在中后台网关的选型与避坑”`），AI 自动执行：
1. **多源交叉检索**：结合 GitHub 高星开源活跃生态、社区真实开发者讨论（Reddit、V2EX、Hacker News、Stack Overflow、知乎/掘金）；
2. **严防纸上谈兵**：深入分析隐藏成本、性能代价、学习心智负担与官方版本断代风险；
3. **结构化决策白皮书交付**：
   - 核心约束与非功能性指标
   - 主流方案横向决策矩阵（对比表格）
   - 精选 GitHub 工业级开源参考
   - 生产环境真实踩坑指南（DO / DON'T 准则）
   - MVP 到生产级的落地演进路径与明确拍板结论

---

## 📁 目录结构

```text
tech-research-skill/
├── README.md                           # 本说明文档
├── skills/
│   └── tech-research/
│       └── SKILL.md                    # DSH & 原生 Agent 标准规范定义
├── adapters/
│   ├── codex-prompt.md                 # 供 OpenAI Codex / ChatGPT / Copilot 一键粘贴的提示词
│   └── .cursorrules                    # 供 Cursor / Windsurf 专用的规则文件
└── examples/
    └── example-research-report.md      # 标准产出示例（前端大文件断点续传调研）
```

---

## 🚀 接入指南

### 1. 在 DeepSeek Harness (DSH) 中使用
只需将本项目软链接或复制到 DSH 的 skills 目录下：
```bash
ln -s "$(pwd)/skills/tech-research" ~/.dsh/skills/tech-research
```
挂载后，在 DSH 对话中直接说：
> *“帮我调研一下 [某个技术选型/方案设计]”*  
DSH 将自动匹配并激活 `tech-research` Skill。

---

### 2. 在 OpenAI Codex / ChatGPT / Claude 中使用
打开 `adapters/codex-prompt.md`，将内容复制到：
- **ChatGPT / Claude** 的 **Custom Instructions (自定义指令)** 中；
- 或新建一个专门的 **Custom GPT (如命名为 Tech Research Architect)**。

配置完成后，平时只需输入一句话即可触发高质量结构化分析。

---

### 3. 在 Cursor / Windsurf 中使用
将 `adapters/.cursorrules` 复制到你的工程项目根目录：
```bash
cp adapters/.cursorrules /path-to-your-project/.cursorrules
```
在编辑器与 AI 对话时，AI 会严格按照首席架构师的标准进行方案调研和代码选型。

---

## 📄 授权与贡献
欢迎自由 Fork、Star 或扩展适配更多 Agent 平台！
