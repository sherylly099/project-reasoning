---
name: project-reasoning
description: Use when a project decision calls for clarifying requirements, testing a proposal, diagnosing a recurring failure, assessing a handoff, or reviewing repeated rework. Use for questions about causes, trade-offs, or what to verify next.
---

# Project reasoning

Start with the decision the user needs to make. Use the goals, constraints, evidence, and permissions already available. If several approaches apply, start with the uncertainty most likely to change the next decision. Explain what supports the conclusion and give an observable next step. Where evidence is missing, identify what would distinguish the remaining explanations.

## Clarify a requirement

Use a real example to identify who needs a different outcome and what success would look like. Check whether the proposed feature is necessary to achieve that outcome. If another interpretation fits, give the evidence and let the user judge. Recommend a path when the evidence is sufficient. Ask up to three questions at a time only if the answers could change the recommendation. Where alternatives involve a meaningful trade-off, explain their costs and why one is preferable.

## Review a proposal

Identify an assumption whose failure would change the decision. Describe an observation that would disprove it and the least expensive way to obtain that observation. For viable proposals, trace a concrete user action or dependency to its immediate and downstream effects. State the conditions under which each effect would occur. Recommend proceeding, revising, or deferring, and identify a result that would change the recommendation.

## Diagnose and repair a failure

Start with one failing example. Compare the input, expected behavior, observed behavior, and relevant logs. When multiple explanations fit, choose a check that predicts a different result for each and record what happens. Consult commits, pull requests, or design notes when version differences or compatibility requirements could explain the failure. If a repair was requested, make the smallest supported change within scope and verify both the original failure and a related working case. Before removing legacy logic, check its consumers and compatibility requirements. If the cause is still uncertain, report the remaining explanations and the observation needed to distinguish them.

## Assess maintenance and recurring problems

- **Handoffs.** Walk through a real task a newcomer should complete independently. Identify the step where progress depends on undocumented context and locate the file or dependency that holds the missing information. Propose a small improvement and verify it with an independent walkthrough.
- **Recurring failures or rework.** Choose a time window and consolidate duplicate reports of the same incident. Trace each proposed common cause to independent incidents. Similar symptoms can have different causes. Choose one proportionate preventive measure. Consider a test when stable inputs and outputs can detect the issue, or a short rule when human judgment matters. Specify how and when to measure recurrence. Implement changes within the user's requested scope.
- **Delivery delays.** When reviewing pull request cycle time, use event timestamps to distinguish review queues, revisions, CI, and merge waits. Compare similar changes and account for drafts and pauses. Open and merge timestamps establish total duration. Attribution requires intermediate events.

## Explore alternatives when stuck

If a specific constraint blocks the usual options, look for a comparable mechanism in another field. Explain what transfers, where the situations differ, and how a small experiment could test the idea in this project.
