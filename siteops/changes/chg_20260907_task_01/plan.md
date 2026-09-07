# Plan — chg_20260907_task_01

## 策略
单文件、零构建、一次交付。规模极小（1 个文件，预估 < 200 行），不拆分多个实施任务，以降低协调成本。

## 步骤
1. T001：编写 `public/index.html` — 内联 CSS 布局 + 原生 JS 计算逻辑（按 spec.md 第 2/3 节）。
2. 验证：file_exists 检查 + HTML 结构检查 + 浏览器人工抽查 spec.md 验收用例 AC1–AC9。

## 文件变更预估
| 文件 | 动作 | 预估行数 |
|---|---|---|
| public/index.html | 新增 | ~150 |

合计 1 个文件，远低于 max_changed_files=30 / max_diff_lines=5000。

## 风险与缓解
- 除零/连续运算边界错误 → spec 验收用例 AC6/AC7 强制抽查。
- `public/` 目录不存在 → 任务内创建，属 `public/**` 允许范围。

## 回滚
删除 `public/index.html` 即可完全回滚。

## 依赖
无外部依赖；无需 install/build；不需要网络。
