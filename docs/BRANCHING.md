# 分支与命名规范

## 分支模型

| 分支 | 用途 | 生命周期 |
|---|---|---|
| `main` | 与论文版本对齐的稳定快照，只接受 PR | 长期 |
| `feat/<slug>` | 功能开发 | 合入即删 |
| `exp/<study>-<slug>` | 实验运行分支，如 `exp/study-a-pilot` | 结束后归档或删除 |
| `chore/<slug>` | 仓库维护 | 合入即删 |

不设 `develop`：单人研究项目，多一层分支只增加合并负担。

## 实验分支为什么单独一类

实验分支承载**一次特定运行的配置快照**（场景集、K 值、模型温度、seed）。它的产出要被写进论文的 Methods，
所以必须能凭分支名 + 终点提交定位到"是哪一次运行"。因此：

- 命名固定为 `exp/<study>-<slug>`，`<study>` 用 `study-a` / `study-b`
- 分支第一个提交必须包含该次运行的参数快照
- 运行结束后打 tag：`exp/study-a-pilot-v1`

## 提交信息

`<type>: <中文一句话>`

- `type` ∈ `feat` / `fix` / `exp` / `test` / `chore` / `docs`
- 涉及读数的提交，正文必须写**日期 + 参数 + 数值**，缺一不写

## 红线

1. 冻结材料（`materials_v5_20261106`、`truth_v5_full.json`、`formal_manifest_*`）不得修改
2. 不提交 `.env`、Token、API Key
3. 不把 `定价数据集/` 的原始 CSV 推上来（单文件最大 165.5 MB，超过 GitHub 100 MB 上限）
4. 不擅自改已冻结的假设、处理条件、结果变量