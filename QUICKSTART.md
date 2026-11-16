# Project Reasoning prompt templates

Copy a prompt and replace the bracketed fields with your own evidence. The [README](README.md) includes worked examples.

## Clarify a requirement

```text
Use $project-reasoning to clarify a requirement. In [situation], I run into [problem or cost]. I am considering [approach] to achieve [desired outcome]. Check the problem definition and suggest a low-cost way to verify the need. Ask about missing information only if it would change the recommendation.
```

## Decide whether to implement a proposal

```text
Use $project-reasoning to review [proposal]. Success means [criterion]. The constraints are [time, cost, or compatibility requirements]. Identify an assumption that could change the decision, a way to test it, and the most significant downstream effect. Recommend whether to proceed, revise, or defer, with reasons.
```

## Locate a failure

```text
Use $project-reasoning to diagnose [failure]. The input or reproduction steps are [details]. I expected [result] and observed [actual result]. The available evidence is [logs, files, or sample]. Trace the failing path. If the cause remains uncertain, identify a check that would distinguish the remaining explanations.
```

## Prevent recurring rework

```text
Use $project-reasoning to review [rework, defects, or rollbacks] over [period]. Here are the incident records: [records]. Assess whether they share a cause, cite the evidence, and recommend one preventive measure. Specify how and when to evaluate its effect.
```
