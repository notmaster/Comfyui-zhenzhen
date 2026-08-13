# 项目结构

```text
<project>/
├── .github/workflows/               # GitHub 自动化工作流
├── .nm-workflow/
│   ├── 0a-docs/                     # 长期有效的需求、设计、决策和报告
│   ├── 0b-tasks/
│   │   ├── active/                  # active、blocked 或 ready Task
│   │   └── archive/                 # done 或 cancelled Task
│   ├── 0c-work-packages/
│   │   ├── active/                  # 未归档 Work Package
│   │   └── archive/                 # 已归档 Work Package
│   └── templates/                   # 可复用工作流模板
├── certs/                            # API TLS 证书
├── docs/mjstyle/                     # Midjourney 样式数据
├── pic/                              # README 图片与演示媒体
├── web/js/                           # ComfyUI 前端扩展
├── workflow/                         # 示例 ComfyUI 工作流
├── .gitignore                       # Git 忽略规则
├── .markdownlint.json               # Markdown lint 规则配置
├── .markdownlintignore              # Markdown lint 排除边界
├── .prettierignore                  # Markdown 格式化排除边界
├── AGENTS.md                        # 项目工作规则
├── __init__.py                      # ComfyUI 自定义节点加载入口
├── Comfly.py                        # 主要节点实现与映射
├── ComflyConcurrent.py              # 并发提交与收集节点
├── package.json                     # 文档工具配置
├── pnpm-lock.yaml                   # pnpm 依赖锁文件
├── PROJECT_STRUCTURE.md             # 本文件
├── pyproject.toml                   # Python 项目元数据
├── requirements.txt                 # Python 依赖声明
└── README.md                        # 项目定位、状态和使用入口
```
