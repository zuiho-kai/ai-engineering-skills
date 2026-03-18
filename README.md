# Skills — 从 GreyWind 项目提炼的工程实践

从一个桌面 AI 伴侣项目的 104+ 条工程错题本和 40+ 条硬规则中，提炼出 6 个可跨项目复用的 skill。

## Skill 列表

| Skill | 一句话 | 核心场景 |
|-------|--------|---------|
| [task-gate](./task-gate/) | 分层任务门禁 | 防止跳步、漏审、口头承诺 |
| [error-book](./error-book/) | 错题本驱动开发 | 自动落盘、归因分析、防复发 |
| [cr-loop](./cr-loop/) | Code Review 闭环 | 独立审查、P0/P1 归零、四步声明 |
| [patch-spiral-breaker](./patch-spiral-breaker/) | 补丁螺旋熔断器 | 连续修复失败时强制换路径 |
| [vision-growth](./vision-growth/) | 愿景生长开发模式 | 愿景锁定 + 最小脊柱 + 逐步生长 |
| [auto-persist](./auto-persist/) | 信息持久化纪律 | 口头承诺 = 没做，必须落盘 |

## 关系图

```
task-gate（入口）
    ├── 多文件功能 → vision-growth（新模块走 5 步）
    ├── 修复场景 → patch-spiral-breaker（≥3 次熔断）
    ├── 代码写完 → cr-loop（独立 CR 闭环）
    └── 出错时 → error-book（自动落盘）
                     └── auto-persist（持久化纪律）
```

## 数据来源

- 104+ 条工程错题本（实战积累）
- 40+ 条硬规则（6 个规则文件）
- 4 层门禁体系（20+ 次违规打磨）
- 多个模块的完整开发周期验证
