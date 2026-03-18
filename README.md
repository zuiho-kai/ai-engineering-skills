# AI Engineering Skills

从多个实战项目（6+ 里程碑、180+ 条错题、50+ 次复犯记录）中提炼的 AI 辅助开发方法论。

## Skill 列表

### v2 — OpenClaw 项目提炼（8 个）

| Skill | zip | 一句话 | 来源 |
|-------|-----|--------|------|
| 任务入口门禁 | [task-entry-gate.zip](./task-entry-gate.zip) | 先分类再动手，入口不拦出口白搭 | DEV-4（17 次复犯） |
| 代码修改 Checklist | [code-change-checklist.zip](./code-change-checklist.zip) | 改一行影响十个文件，11 步自检 | DEV-6（3 次复犯） |
| Phase 完成门禁 | [phase-completion-gate.zip](./phase-completion-gate.zip) | 测试绿 ≠ 完成，CR 归零才算 | 10 次复犯 |
| 出问题自动落盘 | [error-landing.zip](./error-landing.zip) | 归因决策树 A/B/C/D，落文件不落脑子 | 全项目通用 |
| 五方评审 | [five-party-review.zip](./five-party-review.zip) | 5 角色多视角审查，消除单人盲区 | DEV-46/48/49/50/51 |
| 系统测试 Checklist | [st-checklist.zip](./st-checklist.zip) | pytest ≠ ST，七条约束防冒充 | DEV-33（8 次复犯） |
| Token 优化与模型选择 | [token-and-model-strategy.zip](./token-and-model-strategy.zip) | 四层优化降 40% + 三层模型金字塔 | 实测数据 |
| LLM 输出防御 | [llm-output-defense.zip](./llm-output-defense.zip) | LLM 输出永远不可信，Pydantic 是防线 | DEV-BUG-16/17 |

### v1 — GreyWind 项目提炼（6 个）

| Skill | zip | 一句话 | 核心场景 |
|-------|-----|--------|---------|
| 分层任务门禁 | [task-gate.zip](./task-gate.zip) | 分层任务门禁 | 防止跳步、漏审、口头承诺 |
| 错题本驱动开发 | [error-book.zip](./error-book.zip) | 错题本驱动开发 | 自动落盘、归因分析、防复发 |
| CR 闭环 | [cr-loop.zip](./cr-loop.zip) | Code Review 闭环 | 独立审查、P0/P1 归零 |
| 补丁螺旋熔断器 | [patch-spiral-breaker.zip](./patch-spiral-breaker.zip) | 补丁螺旋熔断器 | 连续修复失败时强制换路径 |
| 愿景生长开发模式 | [vision-growth.zip](./vision-growth.zip) | 愿景生长开发模式 | 愿景锁定 + 最小脊柱 + 逐步生长 |
| 信息持久化纪律 | [auto-persist.zip](./auto-persist.zip) | 信息持久化纪律 | 口头承诺 = 没做，必须落盘 |

## 安装

下载 zip 后解压到 skill 目录：

```bash
# Claude Code
unzip task-entry-gate.zip -d ~/.claude/skills/task-entry-gate/

# 或直接克隆整个仓库
git clone https://github.com/zuiho-kai/ai-engineering-skills
```

## 设计原则

1. **结构化拦截 > 口头提醒**：把"下次注意"变成"模板强制输出"
2. **分层按需 > 全量加载**：错题本 1000+ 行 → 按需 100-200 行，token 降 60%
3. **独立审查 > 自我检查**：CR 和评审必须用独立 agent
4. **落盘持久 > 对话临时**：所有经验写入文件，不依赖对话记忆

## 关系图

```
task-entry-gate（入口门禁）
    ├── 改代码 → code-change-checklist（11 步自检）
    ├── 大功能 → five-party-review（五方评审）
    ├── 测试绿 → phase-completion-gate（完成门禁）→ CR 归零
    ├── 跑 ST → st-checklist（七条约束）
    ├── 出错时 → error-landing（归因落盘）
    ├── 接 LLM → llm-output-defense（防御性编程）
    └── 全程 → token-and-model-strategy（成本优化）
```

## 数据来源

- 180+ 条工程错题本（两个项目实战积累）
- 50+ 条硬规则
- 6+ 个里程碑完整开发周期验证
- Token 优化实测降低 40-50%

## License

MIT
