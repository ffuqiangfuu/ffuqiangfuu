# CodeWeave：多智能体代码协作引擎

**Multi-agent Code Collaboration Engine**

CodeWeave is a local agent harness for repository-based coding tasks. It coordinates multiple workers across isolated workspaces and integrates their changes into a reviewable result.

The goal is a reviewable engineering workflow: turn a task into a dependency graph, run independent workers, integrate their patches, and evaluate the result with explicit checks.

## How it works

1. **Plan:** validate the task graph, file ownership, and execution limits.
2. **Coordinate:** run ready tasks in independent processes, with explorer, coder, and reviewer roles.
3. **Isolate:** keep worker edits in Git worktrees and enforce declared write scopes.
4. **Integrate:** apply worker patches serially in an integration worktree.
5. **Verify:** run deterministic checks, with a limited repair cycle when applicable.
6. **Deliver:** produce a patch and a report for review.

## Implementation

- **Python:** independent worker processes and a coordinator around the existing runtime.
- **SQLite:** durable task state, team messages, events, and shared execution budgets.
- **Git worktrees:** separate workspaces and reviewable patch delivery.
- **Run artifacts:** task state, traces, and reports for inspection and recovery.

## Boundaries

Team coding starts from a clean, committed Git baseline. Results are delivered in an integration workspace and a patch; the current checkout is not automatically overwritten. Worktree and process separation do not provide an operating-system security sandbox.

Interrupted runs retry unfinished tasks. Checks are required for a verified completion status, and repairs have an explicit limit. The project does not claim production readiness or a performance speedup.

## 中文简介

CodeWeave 面向仓库级编码任务，使用任务依赖图、独立进程 Worker、Git worktree 隔离、SQLite 状态管理，以及验证和有限修复。它把多智能体协作的结果整理为可审查的补丁与执行报告。

## Project status

This overview describes the current local implementation. A public CodeWeave source repository has not been linked yet.
