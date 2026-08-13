---
id: T-20260813-215509-c88e
status: ready
depends_on: []
---

# 引导 Rules-mini 工作流

## 目标与验收

- 将 Rules-mini-v1.2.1 的规则、工作流目录和文档工具应用到项目。
- 建立 `main` 官方镜像、`dev` 长期集成、`task/*` 独立开发的分支结构。
- Markdown 工具安装和针对性 lint 通过，仓库不跟踪本地依赖或敏感配置。
- Task 改动提交、合并并推送到 `dev`，完成后归档本文件。

## TODO

- [x] 核对 `main`、`origin/main` 和 `upstream/main` 基线。
- [x] 创建并推送 `dev`，从 `dev` 创建正式 Task 分支。
- [x] 应用 Rules-mini-v1.2.1 和项目专属规则。
- [x] 初始化 `.nm-workflow/`、Markdown 工具和忽略规则。
- [x] 执行格式化、lint、锁文件和 Git 边界验证。
- [x] 提交 Task 改动。
- [ ] 将 Task 合入 `dev` 并归档。
- [ ] 修改 Fork 默认分支并清理 `custom`。

## 验证

- `pnpm install --frozen-lockfile --ignore-scripts`
- `pnpm exec prettier PROJECT_STRUCTURE.md .nm-workflow/0b-tasks/active/task-T-20260813-215509-c88e-bootstrap-rules-mini.md --check`
- `pnpm exec markdownlint --dot AGENTS.md PROJECT_STRUCTURE.md .nm-workflow/0b-tasks/active/task-T-20260813-215509-c88e-bootstrap-rules-mini.md`
- `git check-ignore node_modules Comflyapi.json .env`
- 复核提交差异、分支跟踪关系及 GitHub 默认分支。
