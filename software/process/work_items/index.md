# Work Items & Templates

Every piece of work a team tracks is a **work item** (Jira calls it an *issue*, Azure Boards a *work item*, GitHub an *issue*). This page explains what each item type is for, how they fit together, and gives a template you can copy into your tracker. The one rule that matters most: **a backlog is a structure, not a flat list. Link every item to its parent** (see [Keep the Backlog Structured](#keep-the-backlog-structured)).

The process around them (Scrum, Kanban, the SDLC phases) lives in [Lifecycle](https://locchh.github.io/handbook/software/process/lifecycle/index.md), and how each development model (waterfall, Scrum, hybrid, …) uses these items is in [Philosophies & Methodologies](https://locchh.github.io/handbook/software/process/methodologies/#methodologies-the-how-to-do). Documents you *write* rather than track (BRD, SRS, design doc, ADR, test plan, changelog, release notes, runbook) are on [SDLC Documents & Templates](https://locchh.github.io/handbook/software/process/sdlc_documents/index.md). Short definitions of every term are on the [Terms](https://locchh.github.io/handbook/software/terms/index.md) page.

## How Work Items Fit Together

Work is planned top-down and delivered bottom-up. Big goals are split until each piece fits in one sprint, and those pieces are split into tasks a person can finish in a day or two. **Every item except an initiative or epic has a parent**, and that parent link is what turns a backlog from a pile of tickets into a plan.

```
flowchart TD
    I[Initiative / Theme] --> E1[Epic]
    I --> E2[Epic]
    E1 --> S1[User Story]
    E1 --> S2[User Story]
    E1 --> SP[Spike]
    E1 --> B[Bug]
    S1 --> T1[Sub-task]
    S1 --> T2[Sub-task]
```

| Item                             | Typical size                  | Answers                                       | Usually written by                     | Done when                                                   |
| -------------------------------- | ----------------------------- | --------------------------------------------- | -------------------------------------- | ----------------------------------------------------------- |
| **Initiative / Theme**           | Quarters                      | Why are we investing here?                    | Leadership, product                    | The business outcome is measured                            |
| **Epic**                         | Several sprints               | What capability are we delivering?            | Product Owner / PM                     | Child items are done and the success metric is checked      |
| **Feature** (Azure Boards, SAFe) | Fits in one Program Increment | Which shippable piece of the epic comes next? | Product Manager / PO                   | Its stories are done and it is released or releasable       |
| **User Story**                   | Fits in one sprint            | What does the user get?                       | Product Owner, refined with the team   | Acceptance criteria pass and the Definition of Done is met  |
| **Task / Sub-task**              | Hours to a day or two         | What does the team have to do?                | Developers                             | The work is done                                            |
| **Spike**                        | Time-boxed                    | What do we need to learn first?               | Developers                             | The question is answered and written up                     |
| **Bug**                          | Varies                        | What is broken?                               | Anyone: QA, support, users, developers | The fix is verified and a regression test exists            |
| **Change Request**               | Varies                        | What agreed thing must change?                | Client, PM, or operations              | Approved or rejected; if approved, implemented and verified |
| **Production Incident**          | Hours                         | What is broken for users *right now*?         | On-call engineer                       | Service is restored and follow-ups are filed                |

Tools name the levels differently. Jira's defaults are Epic → Story / Task / Bug → Sub-task. Azure Boards' Agile process adds a **Feature** level (Epic → Feature → User Story → Task), and its Scrum process says **Product Backlog Item (PBI)** instead of User Story. The ideas are the same.

### Hierarchy by Framework

The number of levels grows with the size of the organization. A single Scrum team rarely needs more than three. Scaled frameworks such as SAFe add a Feature level and plan in **Program Increments (PI)**.

```
Scrum team                Enterprise / SAFe
Epic                      Epic
└─ User Story             └─ Feature
   └─ Task                   └─ User Story
                                └─ Task
```

The same backlog in both shapes:

```
Scrum team                                   Enterprise / SAFe
Product Backlog                              PI 1
└─ Epic: User Management                     └─ Epic: User Management
   ├─ Story: User can register                  └─ Feature: Authentication
   │  ├─ Task: Create API                          ├─ Story: Register
   │  ├─ Task: Create UI                           ├─ Story: Login
   │  └─ Task: Write tests                         └─ Story: Reset password
   ├─ Story: User can login
   │  ├─ Task: Implement authentication
   │  └─ Task: Write tests
   └─ Bug: Login error on Safari
```

Each level answers one question: the **Epic** says *what capability* we deliver, the **Feature** *which shippable piece* comes next, the **Story** *what value the user gets*, and the **Task** *what work the team does*.

A **PI** is a *timebox*, not a work item: a planning period of several sprints, typically 8–12 weeks in SAFe. Features are planned into a PI; stories are planned into the sprints inside it.

```
PI 1 (8–12 weeks)
├─ Sprint 1
├─ Sprint 2
├─ Sprint 3
└─ Sprint 4
```

### Keep the Backlog Structured

A backlog is a hierarchy, not a pile

The tool may show one ranked list, but behind it **every item must be linked to a parent**. A story without an epic, a bug without the story or release it affects, or work without the change request that caused it cannot be traced, measured, or closed.

Without parent links you can't answer the basic questions: which business goal does this story serve? Which change request created it? Is the epic finished? With them you get traceability, progress per epic, better planning, and a clear line from each item to its business value.

The linking rules:

- Every **story** has a parent **epic** (or **feature**, if you use that level).
- Every **task / sub-task** belongs to a story, or is a standalone task under an epic.
- Every **bug** is linked to the story or epic it affects, or to the release where it was found.
- Every approved **change request** is the parent of the epics or stories it creates.
- Only **initiatives / themes** and **epics** may sit at the top with no parent.

```
Flat: no way to trace        Structured: every item has a parent
Story A                      Epic: Authentication
Bug B                        ├─ Story: Login
Story C                      ├─ Story: Logout
CR D                         ├─ Story: Reset password
Story E                      └─ Bug: Login error on Safari
```

The same items have two views. The **hierarchy view** shows why each item exists. The **backlog view** shows what to do next. Both read the same parent links.

```
Hierarchy view: why          Backlog view: what next (ranked)
Epic                         1. Bug 101
└─ Feature                   2. Story 201
   └─ Story                  3. CR 301
                             4. Story 202
```

A [change request](#change-request) is traced the same way: once approved, it becomes the parent of the work it causes.

```
CR-001: Add MFA
└─ Epic: Multi-factor authentication
   ├─ Story: Email OTP
   ├─ Story: SMS OTP
   └─ Story: Recovery flow
```

## Work Items Across the SDLC

Each item type is born in one [SDLC phase](https://locchh.github.io/handbook/software/process/lifecycle/#sdlc-phases), worked in others, and often creates new items that flow back into the backlog. In waterfall you run the phases once for the whole project. In Scrum, each sprint runs Design → Development → Testing (and often Deployment) for the items it picked, so the same items still pass through the same phases, just in smaller batches.

```
flowchart TD
    CR["Scope Change Request"] -.->|impact analysis, re-baseline| AN
    AN["Analysis: Epic · User Story · Acceptance criteria"] -->|stories| BL[(Backlog)]
    BL -->|"sprint planning (Definition of Ready)"| DE["Design: Spike · ADR · Task breakdown"]
    DE --> DV["Development: Task · Sub-task · Pull Request"]
    DV --> TE["Testing: Bug · Acceptance check · Definition of Done"]
    TE --> DP["Deployment: Production Change · Release Notes"]
    DP --> MA["Maintenance: Incident · Postmortem · Hotfix"]
    TE -.->|bugs not fixed in sprint| BL
    MA -.->|bugs, postmortem actions, tech debt| BL
```

| Item                             | Born in                                                                                  | Worked in                                                              | Ends in, or what it feeds                                                                                                                                        |
| -------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Epic**                         | Analysis: from a business need or BRD                                                    | Across several sprints, Design → Deployment                            | Closes after release, once the success metric is checked                                                                                                         |
| **User Story**                   | Analysis: requirements split into stories with acceptance criteria                       | Refined before the sprint; built in Development; verified in Testing   | Deployment. Its acceptance criteria become the test cases in Testing                                                                                             |
| **Backlog**                      | Fed by Analysis, scope CRs, bugs, and postmortem actions                                 | Ordered and refined continuously                                       | Consumed by sprint planning                                                                                                                                      |
| **Sprint**                       | Sprint planning picks items that meet the Definition of Ready                            | Design → Development → Testing for those items                         | An increment that meets the Definition of Done; retro actions go to the next sprint                                                                              |
| **Spike**                        | Analysis or Design: an unknown blocks the estimate or design                             | Design                                                                 | An ADR, a recommendation, or new estimated stories                                                                                                               |
| **ADR / design doc**             | Design                                                                                   | Reviewed in Design                                                     | Guides Development; superseded later if the decision changes. See [SDLC Documents → ADR](https://locchh.github.io/handbook/software/process/sdlc_documents/#adr) |
| **Task / Sub-task**              | Design / sprint planning: a story broken into steps                                      | Development                                                            | Done in Development; checked in Testing                                                                                                                          |
| **Pull Request / Merge Request** | Development                                                                              | Development: review and CI                                             | Merged. Feeds Testing on the integration or staging environment                                                                                                  |
| **Bug**                          | Mostly Testing (QA). Also Development (CI, code review) and Maintenance (users, support) | Fixed in Development, retested in Testing                              | Shipped in the next Deployment. The earlier it is found, the cheaper the fix                                                                                     |
| **Phase / Milestone**            | Planned up front, before Analysis starts                                                 | Each phase covers one or more SDLC phases                              | Each phase ends at a milestone where a deliverable is signed off                                                                                                 |
| **Scope Change Request**         | Any phase after the requirements are signed off                                          | Impact analysis loops back to Analysis and Design                      | A re-baselined plan, plus new or changed stories in the backlog                                                                                                  |
| **Production Change Request**    | Deployment, or Maintenance for config and infra changes                                  | The change window                                                      | Verified in production, or rolled back                                                                                                                           |
| **Release Notes**                | Deployment                                                                               | Written from the changelog and merged items                            | Published with the version. See [SDLC Documents → Release Notes](https://locchh.github.io/handbook/software/process/sdlc_documents/#release-notes)               |
| **Production Incident**          | Maintenance: an alert or user report on a live service                                   | Mitigated by on-call; may trigger an emergency change or hotfix        | Resolved; leads to a postmortem                                                                                                                                  |
| **Hotfix**                       | Maintenance: from an incident or critical bug                                            | A short Development → Testing → Deployment path on a `hotfix/*` branch | Merged back so the next release keeps the fix                                                                                                                    |
| **Postmortem**                   | Maintenance, after an incident                                                           | Written and reviewed within days                                       | Action items go back to the backlog and start the cycle again                                                                                                    |

The dotted arrows show what makes it a *cycle*: Testing and Maintenance keep generating new backlog items, and those flow back through the same phases.

## Issue

**Issue** is the generic name for any tracked item. In Jira every work item is an issue, and its *issue type* (Epic, Story, Task, Bug, Sub-task) says what kind it is. GitHub and GitLab issues are generic: teams mark the kind with **labels**, or with [issue types ↗](https://docs.github.com/en/issues/tracking-your-work-with-issues/using-issues/managing-issue-types-in-an-organization) in GitHub organizations.

In project management, "issue" also has a narrower meaning. It is a problem that *has already happened* and needs a decision, while a *risk* is one that *might* happen. This is the "I" in a [RAID log](#other-item-types).

A good issue:

- covers one problem or request;
- has a title that says *what* and *where*, so it can be triaged from a list;
- gives enough context that someone else can pick it up without asking you;
- links the parent epic, related issues, and the PRs that fix it;
- carries labels for type, priority, and area, for example `type: bug`, `priority: P2`, `area: checkout`.

Use the [bug report](#bug) template for bugs. For everything else, a feature-request issue works:

**Template: Feature request issue** (`.github/ISSUE_TEMPLATE/feature_request.md`)

```
---
name: Feature request
about: Suggest an improvement
labels: "type: feature"
---
## Problem
<What is hard or impossible today? Who is affected, and how often?>

## Proposal
<What you would like to happen.>

## Alternatives considered
<Other ways to solve it, and why they are worse.>

## Acceptance criteria
- [ ] ...

## Additional context
<Screenshots, links, data.>
```

GitHub also supports **issue forms**: YAML templates that render as a web form with required fields, so nobody can skip "steps to reproduce". See [GitHub: Syntax for issue forms ↗](https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests/syntax-for-issue-forms).

**Template: Bug report issue form** (`.github/ISSUE_TEMPLATE/bug_report.yml`)

```
name: Bug report
description: Something is broken
title: "[Bug]: "
labels: ["type: bug", "needs-triage"]
body:
  - type: textarea
    id: steps
    attributes:
      label: Steps to reproduce
      placeholder: "1. Go to …\n2. Click …"
    validations:
      required: true
  - type: textarea
    id: expected-actual
    attributes:
      label: Expected vs actual result
    validations:
      required: true
  - type: input
    id: version
    attributes:
      label: Version / commit
  - type: dropdown
    id: environment
    attributes:
      label: Environment
      options: [Production, Staging, Local]
    validations:
      required: true
```

## Backlogs and Sprints Across Methods

Agile is a mindset and a family of methods, not one process. Scrum, Kanban, SAFe, XP, and Lean are ways to apply it:

```
Agile
├─ Scrum    fixed-length sprints, defined roles and events
├─ Kanban   continuous flow, WIP limits
├─ SAFe     Scrum / Kanban teams scaled with Program Increments
├─ XP       engineering practices: TDD, pair programming, CI
└─ Lean     remove waste, optimize the whole flow
```

All Scrum teams are Agile, but not all Agile teams use Scrum.

Not every method uses a backlog or sprints. The backlog is an Agile idea; plan-driven projects track work in a project plan instead (see [Phase, Milestone, and Deliverable](#phase-milestone-and-deliverable)). Each method is described in [Philosophies & Methodologies](https://locchh.github.io/handbook/software/process/methodologies/#methodologies-the-how-to-do).

| Method                  | Backlog?                                         | Sprints?                             | Main planning artifact                      |
| ----------------------- | ------------------------------------------------ | ------------------------------------ | ------------------------------------------- |
| **Scrum**               | Yes: Product Backlog and Sprint Backlog          | Yes, fixed length (usually 2 weeks)  | Product Backlog                             |
| **Kanban**              | Usually a backlog feeding the board              | No: continuous flow                  | Board with WIP limits                       |
| **SAFe**                | Yes: portfolio, program (ART), and team backlogs | Yes, grouped into Program Increments | Program backlog and PI plan                 |
| **Waterfall / V-Model** | No                                               | No: phases and milestones            | Requirements documents and project plan     |
| **Hybrid**              | Often, for the build phases                      | Often, inside the plan's phases      | Project plan + backlog + change request log |

Waterfall runs the phases once, in order, and manages work through requirement documents (BRD, SRS), the project plan, the change request log, and the issue log:

```
flowchart LR
    BR[Business requirements] --> SR[System requirements] --> DS[Design] --> DV[Development] --> TS[Testing] --> DP[Deployment]
```

Hybrid projects mix the two. Customers often want fixed scope and budget, while the team wants to deliver iteratively. Two common shapes:

```
flowchart LR
    subgraph H1["Plan up front, build in sprints"]
        direction LR
        A1["Requirements<br/>(waterfall-style)"] --> A2["Development<br/>(sprints)"] --> A3[UAT] --> A4[Release]
    end
    subgraph H2["Plan, sprint, deploy once"]
        direction LR
        B1[Project planning] --> B2[Sprint 1] --> B3[Sprint 2] --> B4[Sprint 3] --> B5[Final deployment]
    end
```

Scrum and Kanban differ mainly in *when* new work enters:

|                       | Scrum                             | Kanban                              |
| --------------------- | --------------------------------- | ----------------------------------- |
| Cadence               | Fixed-length sprints              | Continuous flow                     |
| New request mid-cycle | Usually waits for the next sprint | Pulled as soon as there is capacity |
| Main flow metrics     | Velocity                          | Cycle time, lead time, throughput   |
| Typical use           | Product development               | Support, operations, maintenance    |

For example, a change request (CR-101) arrives in the middle of the week:

```
Scrum: 2-week sprint, scope fixed            Kanban: board, pull when free
Sprint 12                                    To Do
├─ Story A                                   ├─ Story A
├─ Story B                                   ├─ CR-101   ← pulled as soon as
└─ Story C                                   └─ Bug-55     someone has capacity
CR-101 → waits for Sprint 13 planning
```

```
flowchart LR
    subgraph SC["Scrum: the sprint scope is fixed"]
        direction LR
        PB1[(Product Backlog)] -->|sprint planning| SB[Sprint Backlog] --> INC[Increment at sprint end]
    end
    subgraph KB["Kanban: items are pulled one by one"]
        direction LR
        PB2[(Backlog)] -->|pull when capacity| TD[To Do] --> IP[In Progress] --> TS[Testing] --> DN[Done]
    end
```

A hybrid project keeps the plan-driven shell for the client and runs the build inside it with a backlog:

```
Project
├─ Requirements documents (BRD, SRS)
├─ Product Backlog
│  ├─ Epic
│  │  └─ Story
│  └─ Bug
└─ Change request log   (an approved CR becomes the parent of new epics or stories)
```

## Phase, Milestone, and Deliverable

Plan-driven projects organize work in a **project plan** rather than a backlog. That covers [waterfall](https://locchh.github.io/handbook/software/process/methodologies/#1-waterfall-do-it-in-order-no-going-back), the V-Model, most fixed-price contracts, and the outer shell of [hybrid](https://locchh.github.io/handbook/software/process/methodologies/#10-hybrid-water-scrum-fall-plan-like-waterfall-build-like-scrum) projects. These are the items in a project plan:

| Item                | What it is                                                                                                                                    | Example                                           |
| ------------------- | --------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------- |
| **Phase**           | A stage of the project with its own goal and outputs, usually one SDLC phase or a group of them                                               | Requirements, Design, Build, Test, Deploy         |
| **Phase Gate**      | A review at the end of a phase where sponsors decide go / no-go for the next one                                                              | Design review signed off                          |
| **Milestone**       | A zero-duration checkpoint marking an important event, usually the approval of a deliverable. Contracts often tie payments to milestones      | M1: SRS signed off, 25 Jan                        |
| **Deliverable**     | A tangible output handed to the client or to the next phase                                                                                   | SRS v1.0, test summary report, the running system |
| **Work Package**    | The lowest level of the WBS: a chunk of work with one owner that can be estimated and tracked                                                 | Checkout module, detailed design                  |
| **Task / Activity** | One scheduled step of a work package, with an owner, dates, and dependencies. It becomes a bar on the Gantt chart                             | Write the DD for the address table, 2 days        |
| **Baseline**        | The approved scope, schedule, and cost that progress is measured against. Only an approved [change request](#scope-change-request) changes it | Plan v1.0, approved 10 Jan                        |
| **Critical Path**   | The longest chain of dependent tasks. Any delay on it delays the whole project                                                                | SRS → DD → build → SIT → UAT                      |

The word **task** means slightly different things in the two worlds. In a project plan, a task is a *scheduled activity* with dates and dependencies. In Scrum, a task is a *step of a story* with no dates, only To Do / Doing / Done (see [Task and Sub-task](#task-and-sub-task)).

A **WBS (Work Breakdown Structure)** splits the whole project into deliverables and then work packages. Follow the *100% rule*: the children of each node add up to all of the parent's work, and nothing outside it. A common rule of thumb keeps work packages between 8 and 80 hours of effort.

```
flowchart TD
    P[Online Shop v2] --> R[1 Requirements]
    P --> D[2 Design]
    P --> B[3 Build]
    P --> T[4 Test]
    P --> L[5 Deploy]
    R --> R1[1.1 BRD]
    R --> R2[1.2 SRS]
    D --> D1[2.1 Basic design]
    D --> D2[2.2 Detailed design]
    B --> B1[3.1 Checkout module]
    B --> B2[3.2 Payment integration]
    T --> T1[4.1 SIT]
    T --> T2[4.2 UAT]
    L --> L1[5.1 Rehearsal]
    L --> L2[5.2 Go-live]
```

Phases run in order, and each one ends at a milestone where its deliverables are signed off. In SDLC terms, the phases *are* the [SDLC phases](https://locchh.github.io/handbook/software/process/lifecycle/#sdlc-phases). On a hybrid project, the Build phase runs as sprints inside the plan:

```
gantt
    title Online Shop v2: phases and milestones
    dateFormat YYYY-MM-DD
    axisFormat %d %b
    section Requirements
    BRD and SRS                  :req, 2026-01-05, 20d
    M1 SRS signed off            :milestone, m1, after req, 0d
    section Design
    Basic and detailed design    :des, after m1, 15d
    M2 Design approved           :milestone, m2, after des, 0d
    section Build
    Sprints 1-4                  :build, after m2, 40d
    M3 Code complete             :milestone, m3, after build, 0d
    section Test
    SIT                          :sit, after m3, 10d
    UAT                          :uat, after sit, 10d
    M4 UAT signed off            :milestone, m4, after uat, 0d
    section Deploy
    Rehearsal and go-live        :live, after m4, 5d
    M5 Go-live                   :milestone, m5, after live, 0d
```

**Template: Milestone plan**

```
## Milestone plan: <project>

| ID | Milestone | Deliverables | Accepted by | Planned | Actual | Payment |
|---|---|---|---|---|---|---|
| M1 | Requirements signed off | BRD v1.0, SRS v1.0 | Client PO | 2026-01-25 | | 20% |
| M2 | Design approved | Basic + detailed design | Client architect | 2026-02-09 | | — |
| M3 | Code complete | Source code, unit test report | PM | 2026-03-21 | | 30% |
| M4 | UAT signed off | Test summary report, UAT sign-off | Client PO | 2026-04-10 | | 30% |
| M5 | Go-live | Production release, handover document | Client sponsor | 2026-04-15 | | 20% |
```

**Template: Task list (one work package)**

```
## Tasks: 2.2 Detailed design

| WBS | Task | Owner | Start | End | Effort (MD) | Depends on | % done | Status |
|---|---|---|---|---|---|---|---|---|
| 2.2.1 | DD: address table and API | Dev A | 01-27 | 01-29 | 3 | 1.2 | 100% | Done |
| 2.2.2 | DD: checkout flow sequence | Dev B | 01-27 | 01-30 | 4 | 1.2 | 60% | In progress |
| 2.2.3 | DD review | Tech lead | 02-02 | 02-03 | 1 | 2.2.1, 2.2.2 | 0% | Not started |
```

The deliverables themselves (BRD, SRS, design, test report, UAT sign-off) have templates on [SDLC Documents & Templates](https://locchh.github.io/handbook/software/process/sdlc_documents/index.md).

## Backlog

The **Product Backlog** is the single ordered list of everything that might be done to the product. **It looks like a list but is built as a hierarchy: every item is linked to a parent** (see [Keep the Backlog Structured](#keep-the-backlog-structured)). The Product Owner owns its order. The **Sprint Backlog** is the Sprint Goal plus the items the developers picked for this sprint and their plan to deliver them. The developers own it.

A product backlog holds more than stories:

```
Product Backlog
├─ Epic / Feature
├─ User Story
├─ Bug
├─ Change Request (approved)
├─ Spike
└─ Technical Debt
```

A story should fit in one sprint, but a sprint holds several stories, not one:

```
Sprint 1
├─ Story: Register account
├─ Story: Login
└─ Story: Forgot password
```

A healthy product backlog is ordered, not just tagged with priorities. The top items are small, clear, and estimated. Items near the bottom can stay rough until they move up. Order by value, risk, dependencies, and cost of delay. If everything is "High", nothing is.

**Backlog refinement** (or *grooming*) is the ongoing work of splitting, clarifying, and estimating upcoming items. Most teams hold a weekly session. A common rule of thumb is to spend no more than about 10% of the team's capacity on it.

**Template: Product backlog** (top = next)

```
| Rank | Key | Type | Title | Value / why | Estimate | Ready? | Epic |
|---|---|---|---|---|---|---|---|
| 1 | SHOP-101 | Story | Save shipping address at checkout | Removes a step for ~60% of orders | 5 | Yes | EPIC-12 |
| 2 | SHOP-482 | Bug | Checkout 500 on lowercase coupon | S2; ~3% of coupon orders fail | 2 | Yes | — |
| 3 | SHOP-130 | Spike | Postgres FTS vs OpenSearch for search | Unblocks the EPIC-15 estimate | 2 days | Yes | EPIC-15 |
| 4 | SHOP-117 | Story | Pay with a saved card | Faster repeat checkout | 8 | No: needs design | EPIC-12 |
| 5 | SHOP-140 | Tech debt | Replace deprecated payment SDK v2 | Vendor drops v2 next quarter | 5 | No: needs spike | — |
```

**Template: Sprint backlog**

```
## Sprint 24 backlog
Sprint goal: Customers can check out with a saved address.

| Key | Title | Points | Owner | Status |
|---|---|---|---|---|
| SHOP-101 | Save shipping address at checkout | 5 | Dev A | In progress |
| ↳ SHOP-101-1 | API: address endpoints | — | Dev A | Done |
| ↳ SHOP-101-2 | Checkout form pre-fill | — | Dev B | In progress |
| ↳ SHOP-101-3 | E2E test for saved address | — | QA | To do |
| SHOP-482 | Checkout 500 on lowercase coupon | 2 | Dev C | In review |
```

**Template: Refinement checklist**

```
## Backlog refinement — <date>

For each item near the top of the backlog:
- [ ] Title says the outcome, not the implementation
- [ ] Linked to its parent epic / feature (or the CR that created it)
- [ ] Description and acceptance criteria are written
- [ ] Small enough to finish in one sprint (split it if not)
- [ ] Dependencies and open questions are listed (create a spike if a question blocks the estimate)
- [ ] Estimated by the people who will build it
- [ ] Ordered against the items around it

Also:
- [ ] Close items untouched for 6+ months, or move them to an "icebox"
- [ ] Merge duplicates
```

### Definition of Ready and Definition of Done

- **Definition of Done (DoD)** is the quality bar every item must meet before it counts as done. It is a formal commitment in the [Scrum Guide ↗](https://scrumguides.org/scrum-guide.html). Work that misses it is not shown at the Sprint Review.
- **Definition of Ready (DoR)** is the bar an item must meet before the team pulls it into a sprint. It is a team practice, not part of the Scrum Guide. Use it as a checklist, not a gate that blocks conversation.

**Template: Definition of Ready**

```
An item is ready when:
- [ ] It has a clear title and a user or business value
- [ ] It is linked to its parent epic / feature
- [ ] Acceptance criteria are written and agreed with the PO
- [ ] UI designs / API contracts are linked (if needed)
- [ ] Dependencies are resolved or have a date
- [ ] It is estimated and fits in one sprint
```

**Template: Definition of Done**

```
An item is done when:
- [ ] Code is merged to the main branch through a reviewed PR
- [ ] Unit and integration tests are written and pass in CI
- [ ] Acceptance criteria are verified (by QA or the PO)
- [ ] No new lint, security, or accessibility violations
- [ ] Docs, changelog, and runbooks are updated
- [ ] Deployed to staging (or production, behind a flag if needed)
- [ ] Monitoring / alerts exist for new behavior
```

## Epic

An **epic** is a large body of work that delivers one capability and is too big for a single sprint. It is split into user stories, spikes, and bugs, and usually spans several sprints. An epic should describe an *outcome* ("Customers can pay with saved cards"), not a component ("Payment service refactor").

The epic closes when its child items are done and you have checked whether the success metric moved. Long-running epics that never close usually mean the goal was a theme, not an epic.

**Template: Epic**

```
# [Epic] <Outcome-oriented name: "Customers can pay with saved cards">

## Goal
<One or two sentences: the user or business outcome this epic delivers.>

## Problem / context
<Why now? The pain, opportunity, or request behind it. Link data, research, tickets.>

## Success metrics
- <Metric>: from <baseline> to <target> by <date>

## Scope
In scope:
- ...
Out of scope:
- ...

## Users / personas
- ...

## Non-functional requirements
- Performance, security, privacy, accessibility, compliance ...

## Child items
- [ ] STORY-101 ...
- [ ] STORY-102 ...
- [ ] SPIKE-7 ...

## Dependencies and risks
- ...

## Links
- Design: <link> · Spec: <link> · ADR: <link>

Owner: <PO / PM> · Target: <quarter or release>
```

## User Story

A **user story** is a small requirement written from the user's point of view. It describes *who* wants *what* and *why*, and leaves *how* to the team:

> **As a** returning customer, **I want** to save my shipping address, **so that** checkout takes fewer steps.

A story is a placeholder for a conversation, not a full spec. Ron Jeffries' *3 Cs* describe it: the **Card** (the short text), the **Conversation** (the discussion that fills in the details), and the **Confirmation** (the acceptance criteria that prove it works).

Good stories follow [INVEST ↗](https://xp123.com/articles/invest-in-good-stories-and-smart-tasks/): **I**ndependent, **N**egotiable, **V**aluable, **E**stimable, **S**mall, **T**estable.

A common anti-pattern is "As a developer, I want a `users` table". That is a task. A story should describe something a user can see or use. Technical work that serves no single story goes in as a task or a tech-debt item.

Stories carry *functional* requirements (what the system does). *Non-functional* requirements, such as latency, security, and accessibility, go in the acceptance criteria or the Definition of Done. See [Lifecycle → SDLC Phases](https://locchh.github.io/handbook/software/process/lifecycle/#sdlc-phases) for where stories sit next to BRDs and specs.

### Acceptance Criteria

**Acceptance criteria** are the testable conditions that say the story is done. They come in two styles:

- **Rule list**: "Address is validated against the postcode format of the selected country."
- **Scenarios** in [Gherkin ↗](https://cucumber.io/docs/gherkin/reference/) `Given / When / Then`. These map directly to BDD tests (see [Lifecycle → TDD and BDD](https://locchh.github.io/handbook/software/process/lifecycle/#tdd-and-bdd)):

```
Scenario: Saved address is pre-filled
  Given I am logged in and have a saved shipping address
  When I start checkout
  Then the shipping form is pre-filled with my saved address

Scenario: Customer has no saved address
  Given I am logged in and have no saved address
  When I start checkout
  Then the shipping form is empty
  And I can tick "Save this address"
```

Cover the happy path, the main edge cases, and the error cases. If you can't write the criteria, the story isn't ready.

**Template: User Story**

```
# [Story] <Short title: "Save shipping address at checkout">

As a <role / persona>
I want <capability>
so that <benefit / value>

## Acceptance criteria
Scenario: <happy path>
  Given <precondition>
  When <action>
  Then <observable result>

Scenario: <edge or error case>
  Given ...
  When ...
  Then ...

## Notes
- Out of scope: ...
- Non-functional: <e.g. p95 response < 300 ms, WCAG 2.1 AA>
- Design: <link> · API contract: <link>

Epic: EPIC-12 · Estimate: <story points> · Priority: <order or P1–P4>
```

## Task and Sub-task

A **task** is a concrete piece of work that is not a user-facing story and not a bug. Examples are upgrading a library, setting up a CI job, or writing a migration. A **sub-task** is one step of a story or task: "Add API endpoint", "Build form", "Write e2e test". Splitting a story into sub-tasks helps the team see who does what and spot work that is stuck.

```
Story: User can login
├─ Sub-task: Create login API
├─ Sub-task: Build login UI
└─ Sub-task: Write unit tests
```

Start the title with a verb and make "done" unambiguous.

**Template: Task**

```
# [Task] <Verb-first title: "Add index on orders.customer_id">

## What
<The concrete change.>

## Why
<Parent story or epic, or the reason if standalone: chore, upgrade, config, tech debt.>

## Done when
- [ ] ...
- [ ] ...

Parent: STORY-101 · Estimate: <hours or points> · Assignee: <name>
```

## Spike

A **spike** is a time-boxed investigation that answers a question the team needs answered before it can estimate or design something. The term comes from Extreme Programming. A spike produces *knowledge*: a recommendation, a measurement, a throwaway prototype. It does not produce shippable code. When the timebox runs out, stop and report what you have.

**Template: Spike**

```
# [Spike] <The question: "Can Postgres full-text search meet 200 ms p95 on 5M products?">

## Question
<What exactly do we need to know?>

## Why it matters
<Which story or epic is blocked or can't be estimated without the answer.>

## Timebox
<e.g. 2 days>

## Approach
- ...

## Output
- [ ] Findings written up: recommendation + evidence (numbers, links)
- [ ] Follow-up stories created and estimated
- [ ] Prototype code deleted or clearly marked as throwaway
```

## Bug

A **bug** (or **defect**) is behavior that deviates from the spec or from what users can reasonably expect. A bug found in production that is hurting users *now* is handled as a [production incident](#production-incident) first. The bug ticket holds the permanent fix.

One bug per ticket. The title should state the symptom and where it happens, so someone can triage it from the title alone.

A bug can sit in the backlog on its own, be linked to the story it breaks, or be pulled straight into the current sprint when it is urgent.

### Severity vs Priority

These are two different fields. Teams that use one number for both make bad trade-offs.

- **Severity** is how bad the impact is. It is set by whoever reports or triages the bug, usually QA or the developer.
- **Priority** is how soon we fix it. It is set by the Product Owner, who weighs the bug against other work.

| Severity        | Meaning                                                                    |
| --------------- | -------------------------------------------------------------------------- |
| **S1 Critical** | Crash, data loss, security hole, or a core flow blocked with no workaround |
| **S2 Major**    | Important feature broken; the workaround is painful                        |
| **S3 Minor**    | Feature misbehaves; an easy workaround exists                              |
| **S4 Trivial**  | Cosmetic: typo, alignment, wording                                         |

The two often disagree:

|                   | Low priority                                                  | High priority                           |
| ----------------- | ------------------------------------------------------------- | --------------------------------------- |
| **High severity** | Export crashes on a report one internal user runs once a year | Checkout fails for every card payment   |
| **Low severity**  | Icon slightly misaligned on the settings page                 | Company name misspelled on the homepage |

A typical bug lifecycle looks like this:

```
flowchart LR
    N[New] --> T[Triaged] --> IP[In Progress] --> F["Fixed (in review)"] --> Q[Ready for QA] --> V[Verified] --> C[Closed]
    Q -- fails retest --> R[Reopened]
    T -. other exits .-> X1[Duplicate]
    T -.-> X2[Cannot Reproduce]
    T -.-> X3[Won't Fix]
    T -.-> X4[Works as Designed]
```

**Template: Bug report**

```
# [Bug] <Symptom + where: "Checkout returns 500 when coupon code is lowercase">

## Environment
- App / version / commit: <web 2.14.3 (a1b2c3d)>
- Environment: production / staging / local
- Browser / OS / device: <Chrome 130, macOS 15>
- Account / tenant: <test user id — no real PII>

## Steps to reproduce
1. ...
2. ...
3. ...

## Expected result
...

## Actual result
... <error message, HTTP status>

## Frequency
Always / Intermittent (~1 in 5) / Happened once

## Impact
Who is affected, how many, is there a workaround?

## Evidence
- Screenshot / recording:
- Logs / trace id / request id:

Severity: S1–S4 · Priority: <set at triage> · Found in: <version> · Related: <story / incident>
```

The fix should come with a test that fails without it, so the bug can't quietly come back.

## Change Request

"**CR**" means two different things depending on who says it:

1. **Change Request.** This page covers it below. It has two flavors: a change to *agreed scope*, and a change to a *production system*.
1. **Code Review.** This is a review of a pull request before merge. See [Lifecycle → Code Review](https://locchh.github.io/handbook/software/process/lifecycle/#code-review), [Code Review](https://locchh.github.io/handbook/software/process/code_review/index.md), and the [Pull Request / Merge Request](#pull-request-merge-request) template below.

### Scope Change Request

In project work, and in fixed-price and outsourcing contracts especially, a **change request** is a formal request to change something that was already agreed and signed off. That can be a requirement, the scope, the timeline, or the budget. The CR exists so that "can you just add…" becomes a decision with a known cost instead of silent scope creep.

```
flowchart LR
    A[Raise] --> B[Log] --> C[Impact analysis] --> D{Approve / Reject / Defer} --> E["Re-plan (re-baseline)"] --> F[Implement] --> G[Verify] --> H[Close]
```

On larger projects, a **Change Control Board (CCB)** makes the decision. On smaller ones the client and PM decide together. Either way, get the approval in writing before the work starts.

**Template: Scope change request**

```
# [CR-<id>] <Short title of the requested change>

Requested by: <name, organization> · Date: <yyyy-mm-dd> · Project / contract: <...>

## Current baseline
<What was agreed: requirement id, spec section, story, contract clause.>

## Requested change
<What should be different.>

## Reason / business justification
...

## Impact analysis
| Area | Impact |
|---|---|
| Scope | <stories added / changed / removed> |
| Effort | <person-days> |
| Schedule | <milestones that move> |
| Cost | <amount; billable or not> |
| Quality / risk | <regression risk, NFRs affected> |
| Other teams / systems | ... |

## Options
1. Accept as requested — <effort, date>
2. Accept a reduced version — <what's cut>
3. Defer to a later phase / reject — <consequence>

## Decision
Status: Proposed / Approved / Rejected / Deferred
Approved by: <client, PM, CCB> · Date: ...
```

### Production Change Request

In IT operations ([ITIL ↗](<https://en.wikipedia.org/wiki/Change_management_(ITSM)>)), a **change** is any addition, modification, or removal that could affect a live service. Changes come in three types:

| Type          | Meaning                                                                                 | Approval                                            |
| ------------- | --------------------------------------------------------------------------------------- | --------------------------------------------------- |
| **Standard**  | Low-risk, repeatable, pre-approved (e.g. a routine deploy through the CI/CD pipeline)   | None per change; the procedure is approved once     |
| **Normal**    | Anything else that needs assessment (e.g. a database migration, a firewall rule change) | Change authority or **CAB** (Change Advisory Board) |
| **Emergency** | Must happen now, usually to fix an incident                                             | Fast-track approval; documented afterwards          |

Teams with strong CI/CD turn most changes into *standard* ones: the pipeline's tests, reviews, and rollback ability serve as the approval.

**Template: Production change**

```
# [Change] <What is changing: "Upgrade orders DB from Postgres 15 to 17">

Type: Standard / Normal / Emergency · Risk: Low / Medium / High
Window: <start – end, with timezone> · Implementer: <name> · Approver: <name>

## Description
<What changes, on which systems and environments.>

## Reason
<Linked story, bug, incident, or CR.>

## Impact
- Services and users affected:
- Expected downtime:
- Customer notice needed? yes / no

## Pre-checks
- [ ] Rehearsed in staging (link to evidence)
- [ ] Backup / snapshot taken and restore tested
- [ ] On-call and stakeholders informed

## Implementation steps
1. ...

## Verification
<Health checks, dashboards, and smoke tests that prove it worked.>

## Rollback plan
- Trigger: <e.g. error rate > 2% for 5 minutes>
- Steps: ...
- Time to roll back: <minutes>
```

## Production Incident

A **production incident** is an unplanned interruption or degradation of a live service. Examples are an outage, a spike in errors, a slowdown, or a data or security problem. A bug lives in the code. An incident is happening to users *now*. The first job is to **restore service** with a rollback, failover, feature-flag kill switch, or scale-up. Finding the root cause comes later.

```
flowchart LR
    A[Detect] --> B["Declare (assign SEV)"] --> C[Mitigate] --> D[Resolve] --> E["Follow up (postmortem + action items)"]
```

In ITIL terms, the underlying cause of one or more incidents is a **problem**, tracked separately until it is fixed for good.

### Severity Levels

Exact numbers vary by company: some start at SEV0, some say P1–P5. What matters is that the definitions are written down before 3 a.m., so nobody argues about them during an outage.

| Level    | Meaning                                                                       | Example                             | Response                                                                                       |
| -------- | ----------------------------------------------------------------------------- | ----------------------------------- | ---------------------------------------------------------------------------------------------- |
| **SEV1** | Critical: core service down, data loss, or security breach for many customers | Checkout down for everyone          | Page immediately, 24/7; incident commander assigned; updates every 30 min; postmortem required |
| **SEV2** | Major: key feature down or badly degraded for a subset; no good workaround    | Card payments failing in one region | Page on-call; regular updates; postmortem required                                             |
| **SEV3** | Minor: partial degradation; workaround exists                                 | Report export slow                  | Business hours; tracked as a ticket                                                            |
| **SEV4** | Low: cosmetic or internal-only                                                | Typo in the admin UI                | Normal backlog                                                                                 |

### Incident Roles

Clear roles stop five people from debugging the same thing while nobody updates the customers. See [Google SRE: Managing Incidents ↗](https://sre.google/sre-book/managing-incidents/) and the [PagerDuty Incident Response guide ↗](https://response.pagerduty.com/).

- **Incident Commander (IC):** coordinates, decides, and delegates. The IC does *not* debug.
- **Ops / Tech Lead:** hands on keyboard. Investigates and applies the mitigation.
- **Communications Lead:** posts updates to stakeholders and the status page on a fixed schedule.
- **Scribe:** records the timeline of what was seen, tried, and decided. This is the raw material for the postmortem.

On a small team one person may hold several roles, but someone must say "I am the IC" out loud. How severity and on-call connect to escalation is covered in [Becoming Senior → Escalation](https://locchh.github.io/handbook/software/career/becoming_senior/#escalation-is-a-designed-path). Step-by-step responses to known failures belong in [runbooks](https://locchh.github.io/handbook/software/tool_tip/server_operations/#11-runbooks).

**Template: Incident ticket**

```
# [INC-<id>] [SEV<n>] <Symptom users see: "Login failing for ~40% of EU users">

Status: Investigating / Identified / Mitigated / Resolved
Detected: <time, timezone> by <alert / customer / staff>
IC: <name> · Ops lead: <name> · Comms: <name> · Scribe: <name>
Channel / bridge: <#inc-1234> · <call link>

## Impact
- Who / how many are affected:
- Services / regions:
- Started at:

## Current hypothesis
...

## Actions taken (newest first)
- 14:32 Rolled back release 2.14.3 → 2.14.2
- 14:20 Declared SEV2, paged auth on-call
- ...

## Next update
<time>
```

**Template: Status update** (keep the same shape every time)

```
[SEV2] Login failures – EU – Update #3 – 14:45 UTC
Status: Mitigated
Impact: About 40% of EU logins failed between 13:58 and 14:35 UTC. Logins are succeeding now.
What we did: Rolled back release 2.14.3.
Next: Monitoring for 30 minutes; root-cause investigation continues.
Next update: 15:15 UTC, or sooner if anything changes.
```

## Postmortem

A **postmortem** (also *incident review* or *RCA report*) is a written record of an incident. It covers the impact, the timeline, the root causes, and the actions that stop it from happening again. Write one for every SEV1/SEV2 and for any incident with data loss, user-visible downtime, a manual rollback, or a monitoring miss.

A postmortem must be **blameless**. Write about how the *system* let a reasonable person make the mistake. If the answer is "Bob ran the wrong command", the real question is why the tooling let that command reach production. People who fear blame hide information, and then the same incident happens again.

To find root causes, ask **[5 Whys ↗](https://en.wikipedia.org/wiki/Five_whys)** until you reach something you can change in the system:

```
Logins failed.
 Why? The auth service rejected valid tokens.
 Why? The new release read the signing key from a renamed config variable.
 Why? The rename was missed in the production config.
 Why? Staging and production configs are edited separately by hand.
 Why? There is no config validation step in the deploy pipeline.   ← fix this
```

See [Google SRE: Postmortem Culture ↗](https://sre.google/sre-book/postmortem-culture/) and its [example postmortem ↗](https://sre.google/sre-book/example-postmortem/). For reading other companies' postmortems as practice, see [The Postmortem Habit](https://locchh.github.io/handbook/software/career/senior_curriculum/#the-postmortem-habit).

**Template: Postmortem**

```
# Postmortem: <Incident title> (INC-<id>)

Date: ... · Authors: ... · Status: Draft / In review / Final
Severity: SEV<n> · Duration: <start> → <end> (<total>)

## Summary
<Two or three sentences: what happened, the impact, and how it was resolved.>

## Impact
- Users / customers affected:
- SLA / SLO impact (error budget consumed):
- Revenue / data loss:

## Timeline (UTC)
| Time | Event |
|---|---|
| 13:52 | Release 2.14.3 deploy starts |
| 13:58 | Alert: login success rate < 90% |
| 14:20 | SEV2 declared |
| 14:32 | Rollback started |
| 14:35 | Logins recovered |

## Root cause
<The chain of events (5 Whys) down to the system weakness.>

## Trigger
<What set it off: deploy, config change, traffic spike, dependency failure.>

## Detection
<How we found out and how long it took. Could monitoring have caught it sooner?>

## Resolution
<What restored service.>

## What went well
- ...

## What went wrong
- ...

## Where we got lucky
- ...

## Action items
| Action | Type | Owner | Ticket | Due |
|---|---|---|---|---|
| Validate config keys in the deploy pipeline | Prevent | ... | OPS-123 | ... |
| Alert on login success rate, not only on 5xx | Detect | ... | OPS-124 | ... |
| Add the rollback steps to the auth runbook | Mitigate | ... | OPS-125 | ... |
```

Action items without an owner and a ticket don't get done. Review them until they are closed.

## Sprint

A **sprint** is a fixed timebox of one month or less, usually two weeks, in which the team turns backlog items into a usable increment. The Scrum events, roles, and artifacts are summarized in [Lifecycle → Agile, Scrum, Kanban](https://locchh.github.io/handbook/software/process/lifecycle/#agile-scrum-kanban). This section gives the templates.

```
flowchart LR
    PB[(Product Backlog)] --> PL[Sprint Planning] --> SP["Sprint (1–4 weeks)<br/>Daily Scrum every day"] --> RV[Sprint Review] --> RT[Retrospective] --> NX[Next sprint]
    NX -.-> PL
    RV -.->|feedback becomes new items| PB
```

The time limits below are the [Scrum Guide's ↗](https://scrumguides.org/scrum-guide.html) maximums for a one-month sprint; shorter sprints use shorter events.

### Sprint Planning

At most 8 hours. Planning answers three questions: *why* this sprint is valuable (the **Sprint Goal**), *what* can be done, and *how* the work will get done. Base the plan on real **capacity**: people's days available after leave and meetings, checked against recent **velocity** (points finished per sprint).

**Template: Sprint plan**

```
# Sprint <n> — <start date> → <end date>

## Sprint goal
<One sentence describing the outcome: "Customers can pay with saved cards.">

## Capacity
| Member | Days available | Notes |
|---|---|---|
| ... | 9 / 10 | 1 day leave |
Velocity (average of last 3 sprints): <n> points · Planned this sprint: <n> points

## Selected items
| Key | Title | Points | Owner |
|---|---|---|---|
| STORY-101 | ... | 5 | ... |

## Risks and dependencies
- ...

## Explicitly not in this sprint
- ...
```

### Daily Scrum

At most 15 minutes, for the developers. Inspect progress toward the Sprint Goal and re-plan the next day. The classic three questions (yesterday / today / blockers) are optional. Walking the board from right to left, starting with the items closest to done, often works better. Solve problems *after* the stand-up, with only the people who need to be there.

### Sprint Review

At most 4 hours. Show the working increment to stakeholders and adapt the backlog from their feedback. Treat it as a working session, not a slide show.

```
## Sprint <n> review — agenda
1. Sprint goal: met / partly / not met (1 min)
2. Demo of done items, in the product, not on slides (20 min)
3. What wasn't finished and why (5 min)
4. Stakeholder feedback → new or re-ordered backlog items (15 min)
5. What's next: the likely goal of the next sprint (5 min)
```

### Sprint Retrospective

At most 3 hours. The team looks at *how* it worked (people, process, tools, Definition of Done) and picks a few improvements. Many teams open by reading Norm Kerth's *Prime Directive*: everyone did the best job they could, given what they knew at the time. Vary the format so retros don't go stale. Common formats are *Start / Stop / Continue*, *Went well / To improve / Actions*, and *4Ls* (Liked, Learned, Lacked, Longed for).

**Template: Retrospective**

```
# Retro — Sprint <n>

Sprint goal met? yes / partly / no — <one line why>
Last retro's actions: <done / not done, and why>

## Start
- ...

## Stop
- ...

## Continue
- ...

## Actions (max 3)
| Action | Owner | Due |
|---|---|---|
| ... | ... | ... |
```

Pick at most three actions, give each an owner, and check them at the start of the next retro. Twenty sticky notes and no owners change nothing.

## Pull Request / Merge Request

A **pull request (PR)** (GitHub, Bitbucket, Azure Repos), or **merge request (MR)** (GitLab), proposes merging a branch. It is where code review happens. Keep each one small and about one thing; [Lifecycle → Code Review](https://locchh.github.io/handbook/software/process/lifecycle/#code-review) has the size rules, and [Code Review](https://locchh.github.io/handbook/software/process/code_review/index.md) covers what reviewers look for.

### MR Title and Description

- **Title:** write it like a commit subject, for example `feat(checkout): save shipping address`. With *squash merge*, the title becomes the commit on `main`, so it has to make sense in `git log` a year from now. Add the ticket key if your tools link by key: `SHOP-101 feat(checkout): …`.
- **Draft:** open it early as a draft (a *draft pull request* on GitHub, a `Draft:` title prefix on GitLab) to get CI results and early comments. Mark it ready when you want a full review.
- **Description:** a reviewer should understand *why* the change exists and *how to verify it* without asking you.

**Template: PR / MR description** (`.github/pull_request_template.md` or `.gitlab/merge_request_templates/Default.md`)

```
## What
<Summary of the change.>

## Why
Closes #123 / SHOP-101. <Context the reviewer needs.>

## How
<Approach, and anything non-obvious or that you want feedback on.>

## How to test
1. ...

## Screenshots / recordings
<For UI changes.>

## Risk and rollout
<Breaking changes, migrations, feature flags, how to roll back.>

## Checklist
- [ ] Tests added or updated
- [ ] Docs / changelog updated
- [ ] No secrets, PII, or debug code
```

### Linking Issues

Mention the issue in the PR description or a commit message, and the tools connect them. A *closing keyword* such as `Closes` also closes the issue on merge:

| Tool       | Write                                                                      | Effect                                                                                                                                                                                                                                                                                             |
| ---------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **GitHub** | `Closes #123`, `Fixes #123`, `Resolves #123`                               | The issue closes when the PR merges into the default branch ([docs ↗](https://docs.github.com/en/issues/tracking-your-work-with-issues/using-issues/linking-a-pull-request-to-an-issue))                                                                                                           |
| **GitLab** | `Closes #123`, `Fixes #123`, `Resolves #123`                               | The issue closes when the MR merges into the default branch ([docs ↗](https://docs.gitlab.com/user/project/issues/managing_issues/))                                                                                                                                                               |
| **Jira**   | The issue key, `SHOP-101`, in the branch name, commit message, or PR title | Branches, commits, and PRs show up on the Jira issue (needs the GitHub / GitLab / Bitbucket integration). [Smart Commits ↗](https://support.atlassian.com/jira-software-cloud/docs/process-issues-with-smart-commits/) such as `SHOP-101 #comment …` can also comment, log time, or move the issue |
| **Any**    | A plain `#123` or `Refs #123`                                              | Links without closing                                                                                                                                                                                                                                                                              |

### Commit Message

A commit message is written once and read many times: in `git log`, `git blame`, reviews, and generated changelogs. The widely used rules come from [How to Write a Git Commit Message ↗](https://cbea.ms/git-commit/):

1. Separate the subject from the body with a blank line.
1. Keep the subject short: about 50 characters, 72 at most.
1. Use the imperative mood: "Add", "Fix", "Remove", not "Added" or "Fixes".
1. Don't end the subject with a period.
1. Wrap the body at 72 characters.
1. Use the body to explain *what* changed and *why*. The diff already shows *how*.

Many teams prefix the subject with a [Conventional Commits](https://locchh.github.io/handbook/software/process/lifecycle/#conventional-commits) type (`feat`, `fix`, `docs`, …). That lets tools generate the [changelog](https://locchh.github.io/handbook/software/process/sdlc_documents/#changelog) and the next version number. The [spec ↗](https://www.conventionalcommits.org/en/v1.0.0/) also defines a `BREAKING CHANGE:` footer.

**Template: Commit message**

```
<type>(<scope>): <imperative summary, ~50 chars>

<What changed and WHY, wrapped at 72 columns. What was the problem?
Why this approach instead of the alternatives? Anything surprising?>

BREAKING CHANGE: <what breaks and how to migrate>   (only if any)
Refs: SHOP-101
Closes #482
```

**Example**

```
fix(auth): read signing key from AUTH_SIGNING_KEY

Release 2.14.3 renamed JWT_KEY to AUTH_SIGNING_KEY, but production
config still set the old name, so token validation used an empty key
and rejected every login (INC-1234).

Read the new name, fall back to the old one with a deprecation
warning, and fail at startup if neither is set.

Closes #482
```

Messages like `fix`, `update`, `WIP`, or `address review comments` tell a reader nothing. If the team squash-merges, only the MR title and description reach `main`, so work-in-progress commits on the branch don't matter much. If you merge or rebase *without* squashing, every commit lands on `main`, so clean them up first with an [interactive rebase](https://locchh.github.io/handbook/software/process/git/#5-interactive-rebase-cleaning-up-history).

To get the template every time you commit, save it as `~/.gitmessage` and run `git config --global commit.template ~/.gitmessage`.

## Delivery Metrics

Delivery dashboards compute DORA, SPACE, and cost metrics from the fields on these work items: start and closed dates, item type, release links, bug priority, and who found the bug. A wrong field gives a wrong number. What each metric means, and the fields it reads, are on [Delivery & Productivity Metrics](https://locchh.github.io/handbook/software/process/delivery_metrics/index.md). Its [Keep Work Items Measurable](https://locchh.github.io/handbook/software/process/delivery_metrics/#keep-work-items-measurable) section has a checklist to add to your Definition of Done.

## Other Item Types

| Item                          | What it is                                                                                                                                                                             |
| ----------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Initiative / Theme**        | A group of epics serving one strategic goal; spans quarters                                                                                                                            |
| **Feature**                   | Azure Boards / SAFe level between Epic and Story: a shippable capability                                                                                                               |
| **PBI**                       | Product Backlog Item: Scrum's generic name for any backlog entry                                                                                                                       |
| **Improvement / Enhancement** | A change to existing behavior that isn't a bug                                                                                                                                         |
| **Technical Debt**            | Work to pay back past shortcuts: refactoring, upgrades, missing tests. Record the cost of *not* doing it, or it never gets prioritized                                                 |
| **Chore**                     | Maintenance with no user-visible change: dependency bumps, CI tweaks                                                                                                                   |
| **Hotfix**                    | Urgent fix shipped straight to production, often after an incident. See [Lifecycle → Branching Models](https://locchh.github.io/handbook/software/process/lifecycle/#branching-models) |
| **Problem** (ITIL)            | The underlying cause of one or more incidents, managed until it is permanently fixed                                                                                                   |
| **Known Error** (ITIL)        | A problem whose root cause and workaround are documented                                                                                                                               |
| **Service Request**           | A routine user request such as access, a password reset, or a new environment. It is not a failure                                                                                     |
| **Impediment / Blocker**      | Something stopping the team. Removing it is the Scrum Master's job                                                                                                                     |
| **Action Item**               | A follow-up from a retro or postmortem, with an owner and a due date                                                                                                                   |
| **RAID log**                  | Project-level list of Risks, Assumptions, Issues, and Dependencies                                                                                                                     |

## Where Templates Live

Put templates where people create the items, so they are used by default:

- **GitHub:** issue templates and forms in `.github/ISSUE_TEMPLATE/`, and a PR template at `.github/pull_request_template.md`. See [GitHub: Issue templates ↗](https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests/configuring-issue-templates-for-your-repository).
- **GitLab:** `.gitlab/issue_templates/*.md` and `.gitlab/merge_request_templates/*.md`. See [GitLab: Description templates ↗](https://docs.gitlab.com/user/project/description_templates/).
- **Azure Boards:** built-in [work item templates ↗](https://learn.microsoft.com/en-us/azure/devops/boards/backlogs/work-item-template) pre-fill fields per item type.
- **Jira:** make the key fields required per issue type, such as severity, environment, and acceptance criteria. Keep the long-form templates (CR, postmortem, ADR) in the team wiki or the repo and link to them.
- **Git:** a commit message template in `~/.gitmessage`, enabled with `git config --global commit.template ~/.gitmessage`.

Document templates (BRD, SRS, design doc, ADR, test plan, changelog, release notes, runbook) and where to keep them are on [SDLC Documents & Templates](https://locchh.github.io/handbook/software/process/sdlc_documents/#where-documents-live).
