# Project Reasoning

A Codex skill for making a project decision when the goal, the proposed approach, or the cause of a problem is uncertain. Invoke it with `$project-reasoning` and describe the decision. The four examples below follow a team considering a daily project digest. For other projects, use the [copyable prompt templates](QUICKSTART.md).

## 1. Clarify a requirement

Describe a real situation and the outcome you want. This works especially well when you have a feature in mind and want to decide whether it would solve the problem.

```text
Use $project-reasoning to clarify a requirement. Every morning I read several project threads before I can tell what to do next. I'm considering a daily digest. What outcome should I aim for, and how could I check cheaply whether a digest would help? Ask me a question only if the answer could change your recommendation.
```

## 2. Review a proposal

Supply a proposed approach and a success criterion. Ask for the cheapest observation that could change your decision before implementation.

```text
Use $project-reasoning to review my plan to combine daily summaries from each project thread into a single digest. The goal is to identify my next task within two minutes. Which assumption is most likely to undermine the plan? How can I test it cheaply? Recommend whether to proceed, revise, or defer.
```

## 3. Diagnose a failure

Choose a specific failure and include the expected result, actual output, and relevant input. If you want a repair, specify what may be changed.

```text
Use $project-reasoning to investigate a missing entry in yesterday's digest. The original task record is [record], and the generated digest is [output]. Trace the record to the step where it disappears. What evidence distinguishes an input omission from a summarization error?
```

For a repair, add “Once you verify the cause, fix the digest script and check both the missing entry and an entry that already appeared correctly.”

## 4. Review maintenance and rework

Provide independent incident records to investigate a recurring problem. Ask for one preventive measure and a way to measure whether it helps.

```text
Use $project-reasoning to review the last three missing digest entries. Here are the incident records: [records]. Do they share a cause? Recommend one preventive measure and tell me how to evaluate it next month.
```

For a handoff, supply a task the next person needs to complete independently.

```text
Use $project-reasoning to assess this project's handoff. Walk through how a newcomer would find the current task and continue it. At which step would they need help from an experienced teammate? Suggest the smallest change that would let them finish independently and a way to verify it.
```

## Installation

Place the repository directory under your personal Codex skills directory, usually at `~/.codex/skills/project-reasoning/`, with [SKILL.md](SKILL.md) at its root. Then include `$project-reasoning` in your request.
