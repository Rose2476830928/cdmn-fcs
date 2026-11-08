# cdmn-fcs

代码仓库 —— Controlled Data-Market Negotiations（CDMN）× Functional Coverage Score（FCS）。

对应研究：*How Do LLM Buyers Use Task-Relevant Competitor Information? Evidence from Controlled Data-Market Negotiations*

## 状态

**空仓库骨架阶段。业务代码尚未推入。**

- 当前只有 `README.md` 与 `.gitignore`
- 代码推入的前置条件：本地 `D:\1` 的 git 历史需先清除明文 API Key
- 研究记忆与文档在 [llm-data-market-research-hub](https://github.com/Rose2476830928/llm-data-market-research-hub)

## 规划中的目录

```
src/         实验实现（v51_sim、study_a 入口）
tests/       门禁与回归测试
output/      运行产物（按 .gitignore 选择性入库）
docs/        分支规范、复现说明
```

## 分支模型

- `main` —— 可复现的稳定快照，与论文版本对齐
- `feat/<slug>` —— 功能开发
- `exp/<study>-<slug>` —— 实验分支，如 `exp/study-a-pilot`
- `chore/<slug>` —— 仓库维护