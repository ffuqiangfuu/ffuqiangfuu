# Ffuqiangfuu

**AI Agents · Harness Engineering · Agent Applications**

I build agents and the systems that support them, from tool integration and context management to workflow orchestration and application development.

专注智能体开发、运行框架与应用落地。

[CodeWeave](#codeweave) · [Agent Harness Picks](#agent-harness-picks) · [Engineering Notes](#engineering-notes)

## CodeWeave

**CodeWeave：多智能体代码协作引擎**  
*Multi-agent Code Collaboration Engine*

A local coding-agent harness for coordinating multiple workers, isolating their changes, and delivering reviewable patches.

> From a task graph to isolated changes and a reviewable patch.

- **Coordinate work.** Schedule dependent tasks across independent worker processes.
- **Keep changes scoped.** Give workers declared write scopes and separate Git worktrees.
- **Verify the result.** Integrate patches, run explicit checks, and apply bounded repairs.
- **Preserve context.** Persist task state, messages, and budgets; resume unfinished work.

**Stack:** Python · SQLite · Git worktrees  
**Stage:** Local development

[Explore CodeWeave](projects/CodeWeave.md) · [How it works](projects/CodeWeave.md#how-it-works) · [Project status](projects/CodeWeave.md#project-status)

## A little about me

```yaml
# agent.config
focus:
  - agent development
  - harness engineering
  - agent applications
building: CodeWeave
care_about:
  - clear task ownership
  - inspectable execution
  - verifiable changes
```

## Agent Harness Picks

Four open-source projects worth exploring. Each links to the original repository and credits its maintainers.

**[OpenHands Agent Canvas](https://github.com/OpenHands/OpenHands)** · Maintained by **OpenHands**  
A self-hosted control center for coding agents and automations. Explore how agent work is organized and surfaced through a shared interface.

**[mini-swe-agent](https://github.com/SWE-agent/mini-swe-agent)** · Maintained by the **SWE-agent team**  
A minimal software-engineering agent. A useful starting point for understanding the agent loop behind repository tasks.

**[Aider](https://github.com/Aider-AI/aider)** · Maintained by **Aider-AI**  
Terminal pair programming with repository context and Git integration. Explore the feedback loop between conversation, code edits, and commits.

**[LangGraph](https://github.com/langchain-ai/langgraph)** · Maintained by **LangChain**  
Stateful agent orchestration with persistence and human oversight. Explore how explicit state and checkpoints support longer workflows.

## Engineering Notes

Notes from the current CodeWeave implementation:

- [From task graphs to patch delivery](projects/CodeWeave.md#how-it-works) — planning, worker coordination, integration, and verification.
- [The runtime underneath](projects/CodeWeave.md#implementation) — Python processes, SQLite state, and Git worktrees.
- [Execution boundaries](projects/CodeWeave.md#boundaries) — clean baselines, interrupted runs, and bounded repairs.

---

[Browse my repositories](https://github.com/ffuqiangfuu?tab=repositories) · [CodeWeave project notes](projects/CodeWeave.md)
