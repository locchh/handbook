# Delivery & Productivity Metrics

How to measure a delivery team's speed, quality, and cost: DORA adapted for outsourcing (ITO) projects, SPACE, cost per outcome, and what large companies measure. Every number here is computed from the fields on [work items](https://locchh.github.io/handbook/software/process/work_items/index.md), so the last part of this page is about keeping those fields right.

Delivery dashboards don't measure the team directly. They read the fields on your work items and compute metrics from them. A delivery dashboard such as **Andon** computes DORA and SPACE metrics from Jira (and the repo), and a governance and cost dashboard such as **Banto** meters the AI tokens spent per story, user, and agent. Both are only as good as the work items behind them: a wrong field on the ticket gives a wrong number on the dashboard.

Two ground rules come first:

- **The metrics describe the delivery system, not people.** They are never used for individual appraisal.
- **Read every metric as a trend against your own baseline**, never as a single-period score and never alone. Set the baseline before the first measured sprint or phase.

## The ITO Clock

Standard DORA reads production deploy events. In outsourcing (ITO) projects the team usually hands over for the client's acceptance test and has no production access, so every metric is anchored to delivery milestones instead. All durations are counted in **working days**.

```
flowchart LR
    T0["T0 Start Implementation<br/>(Start date / Planned start)"] --> D["D Story Done<br/>(Closed date)"]
    D --> T1["T1 Delivered for Acceptance<br/>(release / product released)"]
    T1 --> T2["T2 Accepted by client"]
```

| Point  | Comes from                                                                                                    | Notes                                                                                       |
| ------ | ------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| **T0** | The work item's *Start date* or *Planned start*                                                               | If both are empty the tool falls back to the *Create date*, and Lead Time inflates silently |
| **D**  | The date the story is *Closed*                                                                                | Close it when it is really done, not in a bulk move at sprint end                           |
| **T1** | Agile: the *Fix Version* release date. Plan-driven: a *Product* with status *Released* and marked deliverable | A release at T1 is the delivery event                                                       |
| **T2** | Client acceptance                                                                                             | T1 → T2 is the client acceptance period                                                     |

## DORA for ITO

| Metric                        | Question it answers                     | ITO formula                                        | Work-item data it needs                                                                                                   |
| ----------------------------- | --------------------------------------- | -------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------- |
| **DF** Delivery Frequency     | Are we hitting the delivery commitment? | Delivery events at T1 ÷ measurement window         | Releases / products marked *Released*; merges to the branch named in a deployment rule                                    |
| **LT** Lead Time for Delivery | Is the pipeline slowing down?           | MEDIAN(T1 − T0), working days                      | T0 filled; item type ticked as a delivery unit; item linked to its release                                                |
| **CFR** Change Failure Rate   | Are deliveries causing damage?          | Failed deliveries ÷ all deliveries × 100%          | Customer-reported Bug with priority *Critical* or *Blocker*, linked to the release, raised within the CFR window after T1 |
| **MTTR** Recovery Time        | When it fails, how fast do we fix it?   | MEDIAN(bug reported → fix delivered), working days | *Created* and *Resolved* dates of the CFR / DRR bugs; *Resolved* set when the fix reaches the client                      |
| **DRR** Delivery Rework Rate  | How often is a delivery sent back?      | Rejected and redelivered ÷ all deliveries × 100%   | Customer-reported Bug at any priority, linked to the release, raised within the DRR window after T1                       |

CFR and DRR read the same bugs. CFR counts only *Critical* and *Blocker*, so every CFR delivery is also a DRR delivery and CFR ≤ DRR. The window lengths are agreed with the client per project.

```
flowchart LR
    REL["Delivery at T1"] --> BUG{"Customer bug<br/>on this delivery?"}
    BUG -- "No" --> OK["Counts in DF only"]
    BUG -- "Any priority, inside DRR window" --> DRR["Counts in DRR"]
    DRR --> SEV{"Critical / Blocker,<br/>inside CFR window?"}
    SEV -- "Yes" --> CFR["Also counts in CFR"]
```

## SPACE: Why the DORA Numbers Move

DORA says *what* happened; SPACE explains *why*. Read them in pairs (for example, Lead Time with Efficiency, or AI-assisted ratio with DRE).

| Dimension                         | Measure                                                                                            | Work-item data it needs                                                               |
| --------------------------------- | -------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- |
| **S** Satisfaction                | Quarterly team survey                                                                              | —                                                                                     |
| **P** Performance (DRE)           | Defects found in the sprint or phase ÷ all defects, including those escaped to later phases or UAT | Each Bug records the phase or sprint where it was found and is linked when it escaped |
| **A** Activity: AI-assisted ratio | Agent-completed tasks ÷ all completed tasks                                                        | AI-assisted tasks are tagged the same way every time                                  |
| **C** Collaboration               | MEDIAN(first review − PR opened)                                                                   | PRs with timestamps, linked to their items                                            |
| **E** Efficiency                  | D − T0 per story, working days                                                                     | T0 and the Closed date filled correctly                                               |

## Cost per Outcome

When agents do part of the work, effort hours no longer show what a story cost. The cost becomes **token + labor + other**. Banto meters token spend live per story, user, and agent, logs every AI conversation (prompt, model, tokens, tool calls, file edits), and flags violations such as an unapproved model or PII in a prompt. Labor cost comes from the timesheet or project system (for example MB4 or Jira), and other cost (licences, infrastructure) from finance systems.

```
flowchart LR
    TOK["Token cost<br/>(Banto: per story / user / agent)"] --> TOTAL["Total cost per outcome"]
    LAB["Labor cost<br/>(timesheet / project system)"] --> TOTAL
    OTH["Other cost<br/>(licences, infrastructure)"] --> TOTAL
```

## Keep Work Items Measurable

| Mistake on the work item                                      | What the dashboard shows                                                                 |
| ------------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| *Start date* / *Planned start* empty                          | Lead Time inflated (T0 falls back to the Create date)                                    |
| Wrong item type, or the type is not ticked as a delivery unit | Item missing from Lead Time, or not seen as a failure                                    |
| Wrong bug *Priority*                                          | CFR under- or overstated                                                                 |
| *Detected By* / *Role* not set to *Customer*                  | CFR = 0 and looks perfect                                                                |
| Bug not linked to the release where it was found              | Bug counted against the wrong release, or not counted                                    |
| Release not marked *Released* / deliverable                   | DF = 0, no T1                                                                            |
| *Resolved* not set when the fix is delivered                  | MTTR inflated (or understated if resolved too early)                                     |
| PR not linked to its item or release                          | No Lead Time breakdown (Readiness → Coding → Review → Merge), or a release counted twice |

A short checklist for the Definition of Done:

- [ ] Item has the right type and is linked to its release (Fix Version / Product)
- [ ] *Start date* is set when work starts; the item is *Closed* when it is really done
- [ ] PRs reference the item key (see [Linking Issues](https://locchh.github.io/handbook/software/process/work_items/#linking-issues))
- [ ] AI-assisted work is tagged consistently
- [ ] Client bugs carry *Detected By = Customer*, a priority, the affected release, and *Resolved* when the fix is delivered

If you cannot name the issues behind a number, it is not evidence yet. Every tile should resolve to a saved filter listing its work items.

## How Large Companies Measure

The DORA-for-ITO and SPACE metrics above are adaptations of public frameworks that large engineering organizations use. The main ones:

| Framework                                  | From                                                      | What it measures                                                                                                                                                       | Worth knowing                                                                                                                                                                                                                                                                                                                                                                                                 |
| ------------------------------------------ | --------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **DORA metrics**                           | Google's DORA research program                            | Five metrics in two groups. Throughput: change lead time, deployment frequency, failed deployment recovery time. Instability: change fail rate, deployment rework rate | Rework rate was added in 2024, and recovery time moved from stability to throughput. See [DORA: History of the metrics ↗](https://dora.dev/guides/dora-metrics/history/)                                                                                                                                                                                                                                      |
| **DORA 2024 on AI**                        | Google Cloud, 2024 State of DevOps report                 | Delivery performance as AI adoption grows                                                                                                                              | "As AI adoption increased, it was accompanied by an estimated decrease in delivery throughput by 1.5%, and an estimated reduction in delivery stability by 7.2%." Measure delivery outcomes, not only AI usage. See [Announcing the 2024 DORA report ↗](https://cloud.google.com/blog/products/devops-sre/announcing-the-2024-dora-report)                                                                    |
| **SPACE**                                  | GitHub, Microsoft Research, University of Victoria (2021) | Satisfaction and well-being, Performance, Activity, Communication and collaboration, Efficiency and flow                                                               | Productivity can't be reduced to one metric. Use several dimensions together and report at team level. See [The SPACE of Developer Productivity, ACM Queue ↗](https://queue.acm.org/detail.cfm?id=3454124)                                                                                                                                                                                                    |
| **DevEx**                                  | DX, University of Victoria, Microsoft Research (2023)     | Feedback loops, cognitive load, flow state                                                                                                                             | Combines developer surveys with data from engineering systems. See [DevEx: What Actually Drives Productivity, ACM Queue ↗](https://queue.acm.org/detail.cfm?id=3595878)                                                                                                                                                                                                                                       |
| **DX Core 4**                              | DX, with input from the DORA, SPACE, and DevEx authors    | Speed, Effectiveness, Quality, Impact                                                                                                                                  | Unifies DORA, SPACE, and DevEx. Balances speed against experience and quality; warns that activity metrics such as diffs per engineer are easy to game. See [Measuring developer productivity with the DX Core 4 ↗](https://getdx.com/research/measuring-developer-productivity-with-the-dx-core-4/)                                                                                                          |
| **Google: QUANTS, speed / ease / quality** | Google Engineering Productivity Research                  | Quality of code, Attention, iNtellectual complexity, Tempo and velocity, Satisfaction                                                                                  | No single metric; triangulate logs, surveys, interviews, and diary studies. Before choosing a metric, ask whether a bad result would change a decision. See [How Google measures developer productivity (DX) ↗](https://getdx.com/blog/how-google-measures-developer-productivity/)                                                                                                                           |
| **LinkedIn DPH Framework**                 | LinkedIn, open source                                     | Goals → Signals → Metrics, with "Persona Champions" representing each kind of engineer                                                                                 | Includes principles and common pitfalls for designing engineering metrics. See [The LinkedIn DPH Framework ↗](https://linkedin.github.io/dph-framework)                                                                                                                                                                                                                                                       |
| **GitHub Copilot impact**                  | GitHub with Accenture                                     | Randomized controlled trial on AI-assisted development in an enterprise, plus the Copilot usage metrics API (for example, acceptance rate)                             | Usage metrics come from IDE telemetry, so users without telemetry enabled are missing from the numbers. See [Quantifying GitHub Copilot's impact with Accenture ↗](https://github.blog/news-insights/research/research-quantifying-github-copilots-impact-in-the-enterprise-with-accenture/) and [Copilot usage metrics ↗](https://docs.github.com/en/copilot/concepts/copilot-usage-metrics/copilot-metrics) |

What they agree on, and what Andon and Banto follow:

- **No single metric.** Pair a speed metric with a quality metric (DORA throughput with instability; Lead Time with DRR and CFR).
- **Measure teams and systems, not individuals.**
- **Combine system data with what developers report** (SPACE, DevEx, Google, LinkedIn). In Andon, SPACE plays this role.
- **Judge AI by delivery outcomes and cost, not by adoption.** An AI-assisted ratio that goes up while rework or failures go up is not a gain (DORA 2024). That is why Banto's cost per outcome sits next to Andon's quality metrics.
