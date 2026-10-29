# Terms

Software, coding, and SDLC vocabulary with abbreviations expanded, grouped by domain. Each term links to the section of this handbook that defines or discusses it. Terms the handbook doesn't cover yet link to an external reference, marked ↗.

**Domains:** [SDLC & Process](#sdlc-process) · [Management & Work Items](#management-work-items) · [Requirements & Design](#requirements-design) · [Coding](#coding) · [Version Control & Review](#version-control-review) · [Testing & QA](#testing-qa) · [System Design](#system-design) · [Backend](#backend) · [Frontend](#frontend) · [Networking](#networking) · [DevOps & SRE](#devops-sre) · [Security, Privacy & Compliance](#security-privacy-compliance) · [Data Engineering](#data-engineering) · [Data Analysis](#data-analysis) · [AI & LLM](#ai-llm)

## SDLC & Process

| Term | Meaning | Read more |
|---|---|---|
| **SDLC** | Software Development Life Cycle: Analysis → Design → Development → Testing → Deployment → Maintenance | [Lifecycle → SDLC Phases](lifecycle.md#sdlc-phases) |
| **Waterfall** | Sequential phases, each finished before the next starts | [Methodologies → Waterfall](methodologies.md#1-waterfall-do-it-in-order-no-going-back) |
| **V-Model** | Waterfall where every phase has a matching test level | [Methodologies → V-Model](methodologies.md#2-v-model-for-every-step-define-how-youll-prove-it-worked) |
| **Agile** | Mindset of short iterations, working software, and responding to change | [Methodologies → Agile](methodologies.md#3-agile-able-to-move-quickly-and-change-direction-without-losing-balance), [Lifecycle → Agile, Scrum, Kanban](lifecycle.md#agile-scrum-kanban) |
| **Lean** | Eliminate waste, optimize the whole flow of value | [Methodologies → Lean](methodologies.md#2-lean) |
| **Scrum** | Agile framework of fixed-length sprints with defined roles, events, and artifacts | [Methodologies → Scrum](methodologies.md#3-scrum-build-a-little-show-it-improve) |
| **Kanban** | Continuous flow on a visual board with WIP limits | [Methodologies → Kanban](methodologies.md#4-kanban-finish-before-you-start-something-new) |
| **SAFe** | Scaled Agile Framework: Agile coordinated across many teams | [Methodologies → SAFe](methodologies.md#5-safe-scrum-but-for-50-teams) |
| **PI** | Program Increment: a SAFe timebox of about 10 weeks (several sprints) that all teams plan and deliver together, kicked off by *PI Planning* | [Methodologies → SAFe](methodologies.md#5-safe-scrum-but-for-50-teams), [Wikipedia: SAFe ↗](https://en.wikipedia.org/wiki/Scaled_agile_framework) |
| **XP** | Extreme Programming: pairing, TDD, continuous integration, small releases | [Methodologies → XP](methodologies.md#6-xp-extreme-programming) |
| **Shape Up** | Basecamp's fixed-appetite, six-week cycles with no backlog | [Methodologies → Shape Up](methodologies.md#7-shape-up-decide-how-much-time-its-worth-not-how-long-it-takes) |
| **RUP** | Rational Unified Process: iterative phases with formal milestones | [Methodologies → RUP](methodologies.md#8-rup-waterfall-iteration-formal-governance) |
| **Sprint** | Fixed timebox (usually 1–4 weeks) that produces a usable increment | [Lifecycle → Agile, Scrum, Kanban](lifecycle.md#agile-scrum-kanban) |
| **Backlog** | Ordered list of work. The *Product Backlog* holds everything wanted; the *Sprint Backlog* holds what this sprint commits to | [Lifecycle → Agile, Scrum, Kanban](lifecycle.md#agile-scrum-kanban), [Scrum Guide ↗](https://scrumguides.org/scrum-guide.html) |
| **Increment** | The usable, done work produced in a sprint | [Lifecycle → Agile, Scrum, Kanban](lifecycle.md#agile-scrum-kanban) |
| **Sprint Planning** | Scrum event at the start of a sprint: pick backlog items and agree the sprint goal | [Lifecycle → Agile, Scrum, Kanban](lifecycle.md#agile-scrum-kanban), [Scrum Guide ↗](https://scrumguides.org/scrum-guide.html) |
| **Daily Standup / Daily Scrum** | 15-minute daily sync: progress toward the sprint goal and blockers | [Lifecycle → Agile, Scrum, Kanban](lifecycle.md#agile-scrum-kanban), [Scrum Guide ↗](https://scrumguides.org/scrum-guide.html) |
| **Sprint Review / Demo** | Show the increment to stakeholders and adapt the backlog from their feedback | [Lifecycle → Agile, Scrum, Kanban](lifecycle.md#agile-scrum-kanban), [Scrum Guide ↗](https://scrumguides.org/scrum-guide.html) |
| **Retrospective (Retro)** | End-of-sprint meeting where the team inspects *how* it worked (what went well, what didn't) and commits to improvements | [Lifecycle → Agile, Scrum, Kanban](lifecycle.md#agile-scrum-kanban), [Methodologies → Scrum](methodologies.md#3-scrum-build-a-little-show-it-improve), [Scrum Guide ↗](https://scrumguides.org/scrum-guide.html) |
| **Backlog Refinement (Grooming)** | Ongoing work to split, clarify, and estimate upcoming backlog items | [Scrum Guide ↗](https://scrumguides.org/scrum-guide.html) |
| **Burndown / Burnup Chart** | Work remaining / work completed plotted over time in a sprint or release | [Wikipedia: Burndown chart ↗](https://en.wikipedia.org/wiki/Burndown_chart) |
| **Lead Time / Cycle Time** | Request → delivered / work started → delivered: the Kanban flow metrics | [Lifecycle → Agile, Scrum, Kanban](lifecycle.md#agile-scrum-kanban), [Wikipedia: Lead time ↗](https://en.wikipedia.org/wiki/Lead_time) |
| **DORA Metrics** | Deployment frequency, lead time for changes, change failure rate, time to restore: the four keys of delivery performance | [DORA: Four keys ↗](https://dora.dev/guides/dora-metrics-four-keys/) |
| **DoD** | Definition of Done: the shared quality bar every increment must meet | [Scrum Guide ↗](https://scrumguides.org/scrum-guide.html), [Atlassian: DoD ↗](https://www.atlassian.com/agile/project-management/definition-of-done) |
| **DoR** | Definition of Ready: what a backlog item needs before a sprint can take it | [Atlassian: DoR ↗](https://www.atlassian.com/agile/project-management/definition-of-ready) |
| **WIP** | Work In Progress, which Kanban limits | [Methodologies → Kanban](methodologies.md#4-kanban-finish-before-you-start-something-new) |
| **DevOps** | Dev and Ops share ownership of building and running software | [Methodologies → DevOps](methodologies.md#4-devops) |

## Management & Work Items

| Term | Meaning | Read more |
|---|---|---|
| **PO** | Product Owner: owns the backlog and its priorities | [Lifecycle → Roles](lifecycle.md#roles) |
| **SM** | Scrum Master: facilitates the process and removes blockers | [Lifecycle → Roles](lifecycle.md#roles) |
| **PM** | Product Manager (sometimes Project Manager) | [Lifecycle → Roles](lifecycle.md#roles) |
| **BA** | Business Analyst: turns business needs into specs | [Lifecycle → Roles](lifecycle.md#roles) |
| **Tech Lead / Architect** | Owns technical direction and system design | [Lifecycle → Roles](lifecycle.md#roles), [Becoming Senior → The Ladder](becoming_senior.md#the-ladder) |
| **Epic** | Large body of work split into stories, often spanning several sprints | [Atlassian: Epics, stories, initiatives ↗](https://www.atlassian.com/agile/project-management/epics-stories-themes) |
| **User Story** | Small requirement from the user's view: *As a <role>, I want <goal>, so that <benefit>*, with acceptance criteria | [Lifecycle → SDLC Phases](lifecycle.md#sdlc-phases), [Atlassian: User stories ↗](https://www.atlassian.com/agile/project-management/user-stories) |
| **Task / Sub-task** | Concrete unit of work that is not a story or a bug, such as a chore, config change, or story breakdown | [Jira: Issue types ↗](https://support.atlassian.com/jira-cloud-administration/docs/what-are-issue-types/) |
| **Bug / Defect** | Behavior that deviates from the spec or from what users expect, filed as a bug report | [Lifecycle → SDLC Phases](lifecycle.md#sdlc-phases), [Jira: Issue types ↗](https://support.atlassian.com/jira-cloud-administration/docs/what-are-issue-types/) |
| **Ticket / Issue** | A tracked work item (story, task, bug, …) in a tool like Jira or GitHub Issues | [Lifecycle → Development Workflow](lifecycle.md#development-workflow-example) |
| **CR** | Change Request: a formal request to change agreed scope, requirements, or a production system, assessed for impact before approval. Also short for *Code Review* (see [Version Control & Review](#version-control-review)) | [Wikipedia: Change request ↗](https://en.wikipedia.org/wiki/Change_request) |
| **Spike** | Time-boxed research task to reduce uncertainty before estimating | [Wikipedia: Spike ↗](https://en.wikipedia.org/wiki/Spike_(software_development)) |
| **Story Point** | Relative estimate of effort, complexity, and uncertainty | [Atlassian: Estimation ↗](https://www.atlassian.com/agile/project-management/estimation) |
| **Velocity** | Story points a team completes per sprint, used for forecasting rather than as a target | [Wikipedia: Velocity ↗](https://en.wikipedia.org/wiki/Velocity_(software_development)) |
| **Milestone** | A checkpoint marking the end of a phase or a key deliverable | [Methodologies → RUP](methodologies.md#8-rup-waterfall-iteration-formal-governance) |
| **MoSCoW** | Must / Should / Could / Won't prioritization | [Wikipedia: MoSCoW ↗](https://en.wikipedia.org/wiki/MoSCoW_method) |
| **OKR** | Objectives and Key Results: goal-setting framework | [Wikipedia: OKR ↗](https://en.wikipedia.org/wiki/Objectives_and_key_results) |
| **KPI** | Key Performance Indicator | [Wikipedia: KPI ↗](https://en.wikipedia.org/wiki/Performance_indicator) |
| **RACI** | Responsible, Accountable, Consulted, Informed: who does what on a task | [Wikipedia: RACI ↗](https://en.wikipedia.org/wiki/Responsibility_assignment_matrix) |
| **PMO** | Project (or Program / Portfolio) Management Office: the group that sets project-management standards, tracks status, budget, and resources across projects, and reports to leadership | [Wikipedia: PMO ↗](https://en.wikipedia.org/wiki/Project_management_office) |
| **PMP** | Project Management Professional, the PMI certification | [Wikipedia: PMP ↗](https://en.wikipedia.org/wiki/Project_Management_Professional) |
| **Steering Committee** | Senior stakeholders who set direction, approve scope and budget, and resolve escalations | [Wikipedia: Steering committee ↗](https://en.wikipedia.org/wiki/Steering_committee) |
| **Stakeholder** | Anyone affected by or with influence over the project | [Wikipedia: Stakeholder ↗](https://en.wikipedia.org/wiki/Stakeholder_(corporate)) |
| **Project Charter / Kickoff** | Document that authorizes the project and its goals / the meeting that starts it | [Wikipedia: Project charter ↗](https://en.wikipedia.org/wiki/Project_charter) |
| **RFP / SOW** | Request for Proposal (a client asks vendors to bid) / Statement of Work (agreed scope, deliverables, timeline) | [Wikipedia: RFP ↗](https://en.wikipedia.org/wiki/Request_for_proposal), [Wikipedia: SOW ↗](https://en.wikipedia.org/wiki/Statement_of_work) |
| **NDA** | Non-Disclosure Agreement | [Wikipedia: NDA ↗](https://en.wikipedia.org/wiki/Non-disclosure_agreement) |
| **T&M / Fixed Price** | Contract models: pay for time spent / pay an agreed amount for agreed scope | [Wikipedia: T&M ↗](https://en.wikipedia.org/wiki/Time_and_materials), [Wikipedia: Fixed-price ↗](https://en.wikipedia.org/wiki/Fixed-price_contract) |
| **WBS** | Work Breakdown Structure: scope decomposed into deliverables and work packages | [Wikipedia: WBS ↗](https://en.wikipedia.org/wiki/Work_breakdown_structure) |
| **Gantt Chart / Critical Path** | Timeline bars of tasks and dependencies / the longest dependent chain, which sets the end date | [Wikipedia: Gantt chart ↗](https://en.wikipedia.org/wiki/Gantt_chart), [Wikipedia: Critical path ↗](https://en.wikipedia.org/wiki/Critical_path_method) |
| **RAID Log** | Risks, Assumptions, Issues, Dependencies tracked in one register | [Wikipedia: Risk register ↗](https://en.wikipedia.org/wiki/Risk_register) |
| **Scope Creep** | Uncontrolled growth of scope without matching time or budget; controlled through CRs | [Wikipedia: Scope creep ↗](https://en.wikipedia.org/wiki/Scope_creep) |
| **Go-live / Sign-off** | The moment the system goes to production users / formal acceptance of a deliverable | [Lifecycle → Environments](lifecycle.md#environments), [Lifecycle → Testing (UAT)](lifecycle.md#testing) |
| **ROI / TCO** | Return on Investment / Total Cost of Ownership (build + run + maintain) | [Wikipedia: ROI ↗](https://en.wikipedia.org/wiki/Return_on_investment), [Wikipedia: TCO ↗](https://en.wikipedia.org/wiki/Total_cost_of_ownership) |
| **CapEx / OpEx** | Capital Expenditure (buy assets up front) / Operating Expenditure (pay as you go, e.g. cloud) | [Wikipedia: CapEx ↗](https://en.wikipedia.org/wiki/Capital_expenditure) |
| **POC** | Proof of Concept: a throwaway build that shows an idea is feasible | [Wikipedia: Proof of concept ↗](https://en.wikipedia.org/wiki/Proof_of_concept) |
| **MVP** | Minimum Viable Product: smallest product that tests the core hypothesis with real users (also *Model-View-Presenter*, see [Frontend](#frontend)) | [Wikipedia: MVP ↗](https://en.wikipedia.org/wiki/Minimum_viable_product) |

## Requirements & Design

| Term | Meaning | Read more |
|---|---|---|
| **BRD** | Business Requirements Document: what the business needs and why | [Lifecycle → SDLC Phases](lifecycle.md#sdlc-phases) |
| **PRD** | Product Requirements Document: what the product must do, for whom | [Wikipedia: PRD ↗](https://en.wikipedia.org/wiki/Product_requirements_document) |
| **FR** | Functional Requirement: *what* the system does, e.g. "a user can reset their password by email" | [Lifecycle → Testing](lifecycle.md#testing), [Wikipedia: Functional requirement ↗](https://en.wikipedia.org/wiki/Functional_requirement) |
| **NFR** | Non-Functional Requirement: *how well* it does it: performance, security, availability, usability, scalability | [Lifecycle → Testing](lifecycle.md#testing), [System Design Notes → Types of APIs](system_design.md#going-deeper_1), [Wikipedia: NFR ↗](https://en.wikipedia.org/wiki/Non-functional_requirement) |
| **FRS** | Functional Requirements Specification | [Lifecycle → SDLC Phases](lifecycle.md#sdlc-phases) |
| **SRS** | Software Requirements Specification: functional plus non-functional requirements | [Lifecycle → SDLC Phases](lifecycle.md#sdlc-phases) |
| **Use Case** | A user goal described as a sequence of interactions with the system | [Lifecycle → SDLC Phases](lifecycle.md#sdlc-phases) |
| **AC** | Acceptance Criteria: testable conditions that make a story "done" | [Spec-Driven Development → What the Spec Should Contain](../../ai/tool_tip/spec_driven_development.md#what-the-spec-should-contain) |
| **BD / HLD** | Basic Design / High-Level Design: components, interfaces, data flow | [Lifecycle → SDLC Phases](lifecycle.md#sdlc-phases) |
| **DD / LLD** | Detailed Design / Low-Level Design: classes, schemas, algorithms | [Lifecycle → SDLC Phases](lifecycle.md#sdlc-phases), [System Design Notes → Design Patterns](system_design.md#what-the-post-says) |
| **SD** | System Design: how components, data, and infrastructure fit together at scale | [Architecture → Building Blocks](architecture.md#5-system-design-building-blocks), [System Design Notes](system_design.md) |
| **Design Doc** | Written proposal for a change: context, options, decision, risks | [Becoming Senior → Communication](becoming_senior.md#communication-is-part-of-the-system) |
| **ADR** | Architecture Decision Record: a short, immutable note of one decision, its context, and its consequences | [Becoming Senior → Communication](becoming_senior.md#communication-is-part-of-the-system), [adr.github.io ↗](https://adr.github.io/) |
| **RFC** | Request for Comments: a proposal circulated for feedback, either an internal design RFC or an IETF standard such as the SSH RFCs | [System Design Notes → How SSH Works](system_design.md#going-deeper_4), [Wikipedia: RFC ↗](https://en.wikipedia.org/wiki/Request_for_Comments) |
| **Spec / SDD** | Specification / Spec-Driven Development: write the spec first, then generate and verify code against it | [Spec-Driven Development](../../ai/tool_tip/spec_driven_development.md) |

## Coding

| Term | Meaning | Read more |
|---|---|---|
| **OOP** | Object-Oriented Programming | [Fundamentals → Programming Paradigms](fundamentals.md#programming-paradigms) |
| **FP** | Functional Programming: pure functions, immutability, composition | [Fundamentals → Programming Paradigms](fundamentals.md#programming-paradigms), [Wikipedia: FP ↗](https://en.wikipedia.org/wiki/Functional_programming) |
| **SOLID** | Single responsibility, Open/closed, Liskov substitution, Interface segregation, Dependency inversion | [Design Principles → SOLID](principles.md#solid) |
| **DRY / KISS / YAGNI** | Don't Repeat Yourself / Keep It Simple, Stupid / You Aren't Gonna Need It | [Design Principles → The Core Three](principles.md#the-core-three-dry-kiss-yagni) |
| **SoC** | Separation of Concerns | [Methodologies → SoC](methodologies.md#6-separation-of-concerns-soc) |
| **CoC** | Convention over Configuration | [Methodologies → CoC](methodologies.md#7-convention-over-configuration-coc) |
| **Clean Code** | Readable code: clear names, small functions, no surprises | [Design Principles → Clean Code Habits](principles.md#clean-code-habits) |
| **Design Pattern** | Reusable solution to a recurring design problem (Singleton, Factory, Observer, …) | [System Design Notes → Seven Design Patterns](system_design.md#1-seven-design-patterns) |
| **DDD** | Domain-Driven Design: model code around the business domain, its language, and its boundaries (bounded contexts) | [Methodologies → DDD](methodologies.md#ddd-domain-driven-design) |
| **DI** | Dependency Injection: pass dependencies in instead of creating them inside | [System Design Notes → Design Patterns](system_design.md#going-deeper), [Fowler ↗](https://martinfowler.com/articles/injection.html) |
| **Refactoring** | Changing structure without changing behavior | [Lifecycle → TDD and BDD](lifecycle.md#tdd-and-bdd), [refactoring.com ↗](https://refactoring.com/) |
| **Tech Debt** | The future cost of a shortcut taken now | [Fowler: Technical Debt ↗](https://martinfowler.com/bliki/TechnicalDebt.html) |
| **Code Smell** | A surface sign of a deeper design problem | [Fowler: Code Smell ↗](https://martinfowler.com/bliki/CodeSmell.html) |
| **Linter** | Static checker for style and common mistakes | [Lifecycle → Code Review](lifecycle.md#code-review), [Frontend Toolchain → Linting](../tool_tip/frontend_tools.md#linting-eslint-oxlint) |
| **Big-O** | How cost grows with input size | [Algorithms → Big-O](algorithms.md#big-o-measuring-growth) |
| **Data Structures** | Array, linked list, hash map, stack, queue, tree, heap, graph | [Algorithms → Core Data Structures](algorithms.md#core-data-structures) |
| **Algorithmic Patterns** | Two pointers, sliding window, BFS/DFS, binary search, dynamic programming | [Algorithms → Algorithmic Patterns](algorithms.md#algorithmic-patterns) |
| **Fail Fast** | Detect and report errors at the earliest point | [Error Handling → Fail Fast](error_handling.md#fail-fast) |
| **EAFP / LBYL** | Easier to Ask Forgiveness than Permission / Look Before You Leap | [Error Handling → EAFP vs LBYL](error_handling.md#eafp-vs-lbyl) |
| **Exception / Context Manager** | Error object that unwinds the stack / `with` block that guarantees cleanup | [Error Handling → Python Specifics](error_handling.md#python-specifics), [Error Handling → Context Managers](error_handling.md#context-managers) |
| **Race Condition / Deadlock** | Concurrency hazards: outcome depends on timing / threads wait on each other forever | [Concurrency → Hazards](concurrency.md#hazards) |
| **Process / Thread / Coroutine** | Isolated memory / shared memory in one process / cooperative task on one thread | [Concurrency → Units of Execution](concurrency.md#units-of-execution) |
| **Concurrency vs Parallelism** | Dealing with many things at once / doing many things at the same instant | [Concurrency & Parallelism](concurrency.md) |
| **I/O-bound / CPU-bound** | Limited by waiting on network or disk (use async) / by computation (use more cores) | [Concurrency → Units of Execution](concurrency.md#units-of-execution) |
| **Async / Event Loop** | Non-blocking I/O where one thread interleaves many tasks | [Concurrency → Primitives & Models](concurrency.md#primitives-models) |
| **Mutex / Lock / Semaphore / Atomic** | One holder at a time / at most N holders / an uninterruptible operation | [Concurrency → Primitives & Models](concurrency.md#primitives-models) |
| **GIL** | Python's Global Interpreter Lock: one thread runs bytecode at a time | [Concurrency → Units of Execution](concurrency.md#units-of-execution) |
| **Pair / Mob Programming** | Two people / the whole team working on one change at one screen | [Methodologies → XP](methodologies.md#6-xp-extreme-programming), [Wikipedia: Pair programming ↗](https://en.wikipedia.org/wiki/Pair_programming) |
| **CLI** | Command Line Interface | [Wikipedia: CLI ↗](https://en.wikipedia.org/wiki/Command-line_interface), [LLM Landscape → CLI Coding Agents](../../ai/basics/landscape.md#cli-coding-agents) |
| **GUI** | Graphical User Interface | [Wikipedia: GUI ↗](https://en.wikipedia.org/wiki/Graphical_user_interface) |
| **IDE** | Integrated Development Environment | [Wikipedia: IDE ↗](https://en.wikipedia.org/wiki/Integrated_development_environment) |
| **JIT** | Just-in-time compilation: compile code at runtime | [Wikipedia: JIT ↗](https://en.wikipedia.org/wiki/Just-in-time_compilation) |

## Version Control & Review

| Term | Meaning | Read more |
|---|---|---|
| **VCS** | Version Control System (Git is the standard) | [Lifecycle → Version Control](lifecycle.md#version-control) |
| **Repository / Clone / Fork** | A project's tracked history / a local copy of it / your own server-side copy of someone else's repo | [Git → Daily Workflow](git.md#7-professional-daily-workflow), [git clone ↗](https://git-scm.com/docs/git-clone) |
| **Commit / Branch / HEAD** | A snapshot with a message / a movable pointer to a line of commits / the commit you have checked out | [Lifecycle → Version Control](lifecycle.md#version-control), [git commit ↗](https://git-scm.com/docs/git-commit) |
| **Working Tree / Staging Area (Index)** | Your files on disk / the changes selected for the next commit (`git add`) | [Pro Git: What is Git? ↗](https://git-scm.com/book/en/v2/Getting-Started-What-is-Git%3F) |
| **Remote / origin / upstream** | A hosted copy of the repo / the default remote you cloned from / the original repo a fork tracks | [Git → Three Layers](git.md#originmain-is-a-local-cache-not-github-itself) |
| **Fetch / Pull / Push** | Download remote changes only / fetch and merge into your branch / upload your commits | [Git → What git fetch does](git.md#what-git-fetch-does-and-does-not-do), [git push ↗](https://git-scm.com/docs/git-push) |
| **Merge / Rebase** | Combine branches with a merge commit / replay commits on a new base | [Git → Merge](git.md#3-git-merge), [Git → Rebase](git.md#4-git-rebase) |
| **Fast-Forward** | Merge that just moves the branch pointer because there is no divergence | [git merge ↗](https://git-scm.com/docs/git-merge) |
| **Squash** | Fold several commits into one | [Git → Interactive Rebase](git.md#5-interactive-rebase-cleaning-up-history) |
| **Interactive Rebase** | `git rebase -i`: reorder, squash, edit, or drop commits before sharing them | [Git → Interactive Rebase](git.md#5-interactive-rebase-cleaning-up-history) |
| **Cherry-pick** | Copy one specific commit from another branch onto the current one, e.g. backport a fix to a release branch | [git cherry-pick ↗](https://git-scm.com/docs/git-cherry-pick) |
| **Revert** | New commit that undoes an earlier one; safe on shared branches | [git revert ↗](https://git-scm.com/docs/git-revert) |
| **Reset** | Move the branch pointer back (`--soft` / `--mixed` / `--hard`); rewrites history, so use only locally | [git reset ↗](https://git-scm.com/docs/git-reset) |
| **Amend** | `git commit --amend`: replace the last commit with a fixed version | [git commit ↗](https://git-scm.com/docs/git-commit) |
| **Stash** | Shelve uncommitted changes and restore them later | [git stash ↗](https://git-scm.com/docs/git-stash) |
| **Force Push** | Overwrite the remote branch; prefer `--force-with-lease`, and never on shared branches | [git push ↗](https://git-scm.com/docs/git-push) |
| **Bisect** | Binary-search history to find the commit that introduced a bug | [git bisect ↗](https://git-scm.com/docs/git-bisect) |
| **Blame** | Show which commit last changed each line | [git blame ↗](https://git-scm.com/docs/git-blame) |
| **.gitignore** | Patterns for files Git should never track | [gitignore ↗](https://git-scm.com/docs/gitignore) |
| **Submodule** | A repo embedded inside another at a pinned commit | [git submodule ↗](https://git-scm.com/docs/git-submodule) |
| **Conflict** | Two changes touch the same lines; a human must choose | [Git → Resolving Conflicts](git.md#6-resolving-conflicts) |
| **Git Flow / GitHub Flow / Trunk-Based** | Branching models, from heavy to light | [Lifecycle → Branching Models](lifecycle.md#branching-models) |
| **PR / MR** | Pull Request / Merge Request: a reviewed request to merge one branch into another | [Code Review → Understanding a PR/MR](code_review.md#6-beyond-the-diff-understanding-a-prmr) |
| **CR** | Code Review: a second engineer checks a change before merge (also *Change Request*, see [Management & Work Items](#management-work-items)) | [Lifecycle → Code Review](lifecycle.md#code-review), [How to Review Code](code_review.md) |
| **Diff / Hunk** | The changes between two versions / one contiguous block of them | [Code Review → What is a Git Diff?](code_review.md#what-is-a-git-diff) |
| **Conventional Commits** | `type(scope): subject` commit message convention | [Lifecycle → Conventional Commits](lifecycle.md#conventional-commits) |
| **SemVer** | Semantic Versioning: `MAJOR.MINOR.PATCH` | [Lifecycle → Semantic Versioning](lifecycle.md#semantic-versioning) |
| **Release / Tag** | A versioned, shippable snapshot, marked by a Git tag | [Lifecycle → Development Workflow](lifecycle.md#development-workflow-example) |
| **Changelog** | Human-readable list of notable changes per version | [keepachangelog.com ↗](https://keepachangelog.com/) |
| **Monorepo** | Many projects in one repository | [Architecture → Code Organization](architecture.md#by-kind-anti-pattern) |

## Testing & QA

| Term | Meaning | Read more |
|---|---|---|
| **QA** | Quality Assurance: test strategy and verification | [Lifecycle → Roles](lifecycle.md#roles) |
| **Test Plan / Test Case / Test Suite** | The testing strategy and scope / one scenario with steps and an expected result / a group of related cases | [Lifecycle → SDLC Phases](lifecycle.md#sdlc-phases), [Wikipedia: Test case ↗](https://en.wikipedia.org/wiki/Test_case_(software)) |
| **Testing Pyramid** | Many unit tests, fewer integration tests, very few E2E tests | [Lifecycle → Testing](lifecycle.md#testing), [Fowler: Practical Test Pyramid ↗](https://martinfowler.com/articles/practical-test-pyramid.html) |
| **Unit Test** | Tests one function or class in isolation; fast, run on every commit | [Lifecycle → Testing](lifecycle.md#testing), [Wikipedia: Unit testing ↗](https://en.wikipedia.org/wiki/Unit_testing) |
| **Integration Test** | Tests components working together, e.g. a service and its real database | [Lifecycle → Testing](lifecycle.md#testing), [Wikipedia: Integration testing ↗](https://en.wikipedia.org/wiki/Integration_testing) |
| **SIT** | System Integration Testing: the integrated system tested against its external interfaces | [Wikipedia: System integration testing ↗](https://en.wikipedia.org/wiki/System_integration_testing) |
| **System Test** | Tests the complete, integrated system against the requirements | [Lifecycle → Testing](lifecycle.md#testing), [Wikipedia: System testing ↗](https://en.wikipedia.org/wiki/System_testing) |
| **E2E Test** | End-to-End: drives the whole stack as a user would, e.g. a browser through to the database | [Lifecycle → Testing](lifecycle.md#testing), [Frontend Toolchain → Testing](../tool_tip/frontend_tools.md#testing-cypress-playwright-plus-vitest-and-msw) |
| **Contract Test** | Checks that a provider and its consumers still agree on the API shape | [Fowler: Contract Test ↗](https://martinfowler.com/bliki/ContractTest.html) |
| **Functional Test** | Verifies a functional requirement (FR): *does it do the right thing?* | [Lifecycle → Testing](lifecycle.md#testing) |
| **Non-Functional Test** | Verifies an NFR: performance, security, usability, reliability | [Lifecycle → Testing](lifecycle.md#testing) |
| **Smoke Test** | Quick, shallow check that the build starts and its critical paths work, run before deeper testing or right after deploy | [Wikipedia: Smoke testing ↗](https://en.wikipedia.org/wiki/Smoke_testing_(software)) |
| **Sanity Test** | Narrow check that a specific fix or change works, before a full regression run | [Wikipedia: Sanity check ↗](https://en.wikipedia.org/wiki/Sanity_check) |
| **Regression Test** | Re-runs existing tests to make sure a change didn't break old behavior; add one for every fixed bug | [Wikipedia: Regression testing ↗](https://en.wikipedia.org/wiki/Regression_testing) |
| **UAT** | User Acceptance Testing: the business confirms requirements are met and signs off | [Lifecycle → Testing](lifecycle.md#testing), [Wikipedia: Acceptance testing ↗](https://en.wikipedia.org/wiki/Acceptance_testing) |
| **Alpha / Beta Test** | Pre-release testing by internal users / by a limited group of real users | [Wikipedia: Alpha and beta testing ↗](https://en.wikipedia.org/wiki/Software_testing#Alpha_testing) |
| **Performance Test** | Measures speed and resource use (latency, throughput) under a given load | [Wikipedia: Performance testing ↗](https://en.wikipedia.org/wiki/Software_performance_testing) |
| **Load Test** | Behavior at expected peak load | [Lifecycle → Testing](lifecycle.md#testing) |
| **Stress Test** | Push past capacity to find the breaking point and how the system fails | [Lifecycle → Testing](lifecycle.md#testing), [Wikipedia: Stress testing ↗](https://en.wikipedia.org/wiki/Stress_testing_(software)) |
| **Spike Test** | Sudden, sharp jump in load; checks auto-scaling and recovery | [Wikipedia: Performance testing ↗](https://en.wikipedia.org/wiki/Software_performance_testing) |
| **Soak / Endurance Test** | Normal load held for hours or days to expose leaks and slow degradation | [Wikipedia: Soak testing ↗](https://en.wikipedia.org/wiki/Soak_testing) |
| **Security Test / Pentest** | Probe for vulnerabilities; a penetration test is an authorized simulated attack | [Security → Common Risks](security.md#common-risks-owasp-condensed), [Wikipedia: Penetration test ↗](https://en.wikipedia.org/wiki/Penetration_test) |
| **SAST / DAST** | Static (source code) / Dynamic (running app) Application Security Testing | [Wikipedia: SAST ↗](https://en.wikipedia.org/wiki/Static_application_security_testing), [Wikipedia: DAST ↗](https://en.wikipedia.org/wiki/Dynamic_application_security_testing) |
| **Fuzz Test** | Feed random or malformed input to find crashes and unhandled cases | [Wikipedia: Fuzzing ↗](https://en.wikipedia.org/wiki/Fuzzing) |
| **Adversarial Test** | For LLM and ML systems: deliberately crafted hostile inputs (prompt injection, jailbreaks, perturbed data) that try to make the model misbehave, leak data, or bypass guardrails | [AI & LLM](#ai-llm), [Wikipedia: Adversarial ML ↗](https://en.wikipedia.org/wiki/Adversarial_machine_learning) |
| **Accessibility Test** | Checks the UI against WCAG: keyboard use, screen-reader names, contrast | [Frontend → a11y](#frontend), [W3C: WCAG ↗](https://www.w3.org/WAI/standards-guidelines/wcag/) |
| **Usability Test** | Watch real users attempt tasks to find friction | [Wikipedia: Usability testing ↗](https://en.wikipedia.org/wiki/Usability_testing) |
| **Compatibility / Cross-Browser Test** | Same behavior across browsers, devices, and OS versions | [Frontend Toolchain → Testing](../tool_tip/frontend_tools.md#testing-cypress-playwright-plus-vitest-and-msw), [Wikipedia: Compatibility testing ↗](https://en.wikipedia.org/wiki/Compatibility_testing) |
| **Snapshot Test** | Compare output (rendered UI, serialized data) with a stored snapshot | [Jest: Snapshot testing ↗](https://jestjs.io/docs/snapshot-testing) |
| **Mutation Test** | Inject small bugs into the code; good tests should fail (kill the mutant) | [Wikipedia: Mutation testing ↗](https://en.wikipedia.org/wiki/Mutation_testing) |
| **Property-Based Test** | Generate many inputs and assert a property that must always hold | [Wikipedia: Property testing ↗](https://en.wikipedia.org/wiki/Software_testing#Property_testing) |
| **Exploratory Test** | Unscripted testing where a tester learns and designs tests on the fly | [Wikipedia: Exploratory testing ↗](https://en.wikipedia.org/wiki/Exploratory_testing) |
| **Black-Box / White-Box Test** | Tests from the outside, without seeing the code / tests designed from the code's internals | [Wikipedia: Black-box ↗](https://en.wikipedia.org/wiki/Black-box_testing), [Wikipedia: White-box ↗](https://en.wikipedia.org/wiki/White-box_testing) |
| **Chaos Test** | Deliberately inject failures in production-like systems to prove resilience | [Wikipedia: Chaos engineering ↗](https://en.wikipedia.org/wiki/Chaos_engineering) |
| **TDD** | Test-Driven Development: Red → Green → Refactor | [Lifecycle → TDD and BDD](lifecycle.md#tdd-and-bdd), [Methodologies → TDD](methodologies.md#tdd-test-driven-development) |
| **BDD** | Behavior-Driven Development: Given / When / Then | [Methodologies → BDD](methodologies.md#bdd-behavior-driven-development) |
| **Mock / Stub** | Test doubles that stand in for real dependencies | [Frontend Toolchain → Testing](../tool_tip/frontend_tools.md#testing-cypress-playwright-plus-vitest-and-msw), [Fowler: Mocks Aren't Stubs ↗](https://martinfowler.com/articles/mocksArentStubs.html) |
| **Fixture** | Fixed setup state or data a test runs against | [Wikipedia: Test fixture ↗](https://en.wikipedia.org/wiki/Test_fixture) |
| **Flaky Test** | Passes and fails on the same code; usually caused by timing, ordering, or shared state | [Fowler: Non-Determinism ↗](https://martinfowler.com/articles/nonDeterminism.html) |
| **Code Coverage** | Share of code executed by tests | [Wikipedia: Code coverage ↗](https://en.wikipedia.org/wiki/Code_coverage) |

## System Design

| Term | Meaning | Read more |
|---|---|---|
| **Latency** | Time for one request to complete, usually reported as percentiles (p50/p95/p99) | [Architecture → Performance Bottlenecks](architecture.md#performance-bottlenecks), [DevOps & SRE → p95/p99](#devops-sre) |
| **Throughput** | Work completed per unit of time (requests/s, MB/s); can rise while latency worsens | [Architecture → Performance Bottlenecks](architecture.md#performance-bottlenecks) |
| **Bandwidth** | Maximum data rate of a link; throughput is what you actually achieve | [Wikipedia: Bandwidth ↗](https://en.wikipedia.org/wiki/Bandwidth_(computing)) |
| **RPS / QPS / TPS** | Requests / Queries / Transactions Per Second | [Wikipedia: Queries per second ↗](https://en.wikipedia.org/wiki/Queries_per_second) |
| **Back-of-the-Envelope Estimation** | Rough numbers (users → RPS → storage → bandwidth) to size a design before drawing it | [Wikipedia: Back-of-the-envelope ↗](https://en.wikipedia.org/wiki/Back-of-the-envelope_calculation) |
| **Scalability** | Handle more load by adding resources without a redesign | [Architecture → Scalability](architecture.md#scalability) |
| **Vertical / Horizontal Scaling** | Scale up (bigger machine) / scale out (more machines behind a load balancer) | [Architecture → Scalability](architecture.md#scalability), [Big Data → Scale Up vs Scale Out](../../data/basics/big_data.md#scale-up-vs-scale-out) |
| **Elasticity / Auto-scaling** | Add and remove capacity automatically as load changes | [Wikipedia: Autoscaling ↗](https://en.wikipedia.org/wiki/Autoscaling) |
| **Stateless / Stateful** | Service keeps no per-client state between requests (easy to scale out) / it does (needs sticky sessions or shared storage) | [Architecture → Scalability](architecture.md#scalability) |
| **Availability** | Share of time the system serves requests successfully, measured in nines | [DevOps & SRE → Nines](#devops-sre), [Architecture → CAP Theorem](architecture.md#cap-theorem) |
| **Reliability** | The system keeps doing the right thing over time, despite faults | [Becoming Senior → Reliability](becoming_senior.md#reliability-is-measured-not-felt) |
| **Durability** | Once written and acknowledged, data survives crashes | [Databases → Transactions & ACID](../../data/basics/databases.md#transactions-acid), [Wikipedia: Durability ↗](https://en.wikipedia.org/wiki/Durability_(database_systems)) |
| **HA** | High Availability: redundancy plus automatic failover so one failure doesn't cause an outage | [Wikipedia: High availability ↗](https://en.wikipedia.org/wiki/High_availability) |
| **Fault Tolerance / Redundancy** | Keep working when parts fail / spare copies of components that make it possible | [Wikipedia: Fault tolerance ↗](https://en.wikipedia.org/wiki/Fault_tolerance) |
| **Failover** | Switch traffic to a standby when the primary fails | [Wikipedia: Failover ↗](https://en.wikipedia.org/wiki/Failover) |
| **SPOF** | Single Point of Failure: one component whose failure takes the whole system down | [Architecture → Peer-to-Peer](architecture.md#peer-to-peer-p2p), [Wikipedia: SPOF ↗](https://en.wikipedia.org/wiki/Single_point_of_failure) |
| **DR** | Disaster Recovery: restore service after losing a site or region, sized by RPO / RTO | [Becoming Senior → Deployment and Scale](becoming_senior.md#deployment-and-scale-are-part-of-the-design), [Wikipedia: DR ↗](https://en.wikipedia.org/wiki/Disaster_recovery) |
| **LB** | Load Balancer: spreads traffic across instances (round robin, least connections; L4 or L7) | [Architecture → Load Balancers](architecture.md#load-balancers) |
| **Reverse Proxy** | Server in front of your apps that terminates TLS, routes, caches, and hides internals (NGINX, Caddy) | [Running a Server → The Exposure Chain](../tool_tip/server_operations.md#the-exposure-chain), [Wikipedia: Reverse proxy ↗](https://en.wikipedia.org/wiki/Reverse_proxy) |
| **API Gateway** | Single entry point for clients that handles routing, auth, and rate limiting for many services | [Architecture → Microservices](architecture.md#microservices), [microservices.io ↗](https://microservices.io/patterns/apigateway.html) |
| **Service Discovery / Service Mesh** | How services find each other / an infrastructure layer that handles service-to-service traffic, retries, and mTLS | [microservices.io: Discovery ↗](https://microservices.io/patterns/server-side-discovery.html), [Wikipedia: Service mesh ↗](https://en.wikipedia.org/wiki/Service_mesh) |
| **Cache** | Fast copy of data closer to the reader | [Architecture → Caching](architecture.md#caching) |
| **Cache-Aside / Write-Through / Write-Behind** | Caching strategies: app loads on miss / write cache and DB together / write cache now, DB later | [Architecture → Caching](architecture.md#caching) |
| **TTL / Eviction (LRU)** | Time To Live before an entry expires / which entry to drop when full (Least Recently Used) | [Architecture → Caching](architecture.md#caching), [Wikipedia: Cache replacement ↗](https://en.wikipedia.org/wiki/Cache_replacement_policies) |
| **CDN** | Content Delivery Network: edge caches near users | [Architecture → CDN](architecture.md#cdn-content-delivery-network) |
| **Partitioning / Sharding** | Split data across nodes by range, hash, or directory | [Architecture → Partitioning](architecture.md#partitioning-sharding) |
| **Consistent Hashing** | Hash scheme where adding or removing a node moves only a small share of keys | [Wikipedia: Consistent hashing ↗](https://en.wikipedia.org/wiki/Consistent_hashing) |
| **Hot Spot / Hot Key** | One shard or key that gets far more traffic than the rest | [Wikipedia: Shard ↗](https://en.wikipedia.org/wiki/Shard_(database_architecture)) |
| **Replication / Read Replica** | Copies of data on several nodes (leader–follower, multi-leader) / a copy that serves reads | [Wikipedia: Replication ↗](https://en.wikipedia.org/wiki/Replication_(computing)) |
| **Quorum / Leader Election** | Majority agreement needed for a read or write / choosing one node to coordinate | [Wikipedia: Quorum ↗](https://en.wikipedia.org/wiki/Quorum_(distributed_computing)), [Wikipedia: Leader election ↗](https://en.wikipedia.org/wiki/Leader_election) |
| **CAP** | Consistency, Availability, Partition tolerance: pick two under partition | [Architecture → CAP Theorem](architecture.md#cap-theorem) |
| **PACELC** | CAP extended: if Partitioned choose A or C, Else choose Latency or Consistency | [Wikipedia: PACELC ↗](https://en.wikipedia.org/wiki/PACELC_design_principle) |
| **Strong / Eventual Consistency** | Every read sees the latest write / replicas converge eventually | [Databases → Consistency at Scale](../../data/basics/databases.md#consistency-at-scale), [Wikipedia: Eventual consistency ↗](https://en.wikipedia.org/wiki/Eventual_consistency) |
| **BASE** | Basically Available, Soft state, Eventually consistent: the opposite trade-off to ACID | [Databases → Consistency at Scale](../../data/basics/databases.md#consistency-at-scale) |
| **MQ** | Message Queue: buffers work between producers and consumers (Kafka, RabbitMQ, SQS) | [Architecture → Message Queues](architecture.md#message-queues) |
| **Pub/Sub** | Publishers emit events; every subscriber gets a copy | [Architecture → Message Queues](architecture.md#message-queues), [System Design Notes → Design Patterns](system_design.md#going-deeper) |
| **Stream Processing** | Continuous processing of event streams (Kafka Streams, Flink) | [Architecture → Stream Processing](architecture.md#stream-processing) |
| **Backpressure** | A slow consumer signals producers to slow down instead of being overwhelmed | [Wikipedia: Back pressure ↗](https://en.wikipedia.org/wiki/Back_pressure) |
| **2PC / Saga** | Two-Phase Commit (atomic commit across nodes) / a chain of local transactions with compensating steps | [Wikipedia: 2PC ↗](https://en.wikipedia.org/wiki/Two-phase_commit_protocol), [microservices.io: Saga ↗](https://microservices.io/patterns/data/saga.html) |
| **CQRS / Event Sourcing** | Separate write and read models / store state as an append-only log of events | [Fowler: CQRS ↗](https://martinfowler.com/bliki/CQRS.html), [Fowler: Event Sourcing ↗](https://martinfowler.com/eaaDev/EventSourcing.html) |
| **Rate Limiting** | Cap requests per client or key (token bucket, leaky bucket, sliding window) | [Architecture → Rate Limiting](architecture.md#rate-limiting) |
| **Retry / Backoff / Jitter** | Re-try transient failures with growing, randomized delays | [Error Handling → Retry with Backoff](error_handling.md#retry-with-backoff), [System Design Notes → Retry and Resilience](system_design.md#7-retry-and-resilience) |
| **Circuit Breaker** | Stop calling a failing dependency for a while | [Error Handling → Circuit Breaker](error_handling.md#circuit-breaker) |
| **Graceful Degradation** | Serve a reduced result instead of failing outright | [Error Handling → Graceful Degradation](error_handling.md#graceful-degradation) |
| **Bottleneck** | The resource (CPU, memory, I/O, network) that limits the whole system | [Architecture → Performance Bottlenecks](architecture.md#performance-bottlenecks) |

## Backend

| Term | Meaning | Read more |
|---|---|---|
| **API** | Application Programming Interface | [API Design](apis.md) |
| **REST / SOAP / GraphQL** | Resource-oriented HTTP style / XML messaging protocol / client-shaped query language | [APIs → Styles](apis.md#styles), [System Design Notes → Types of APIs](system_design.md#2-types-of-apis) |
| **RPC / gRPC** | Remote Procedure Call / Google's binary RPC over HTTP/2 | [APIs → Styles](apis.md#styles), [System Design Notes → API Protocols](system_design.md#3-seven-api-protocols) |
| **WebSocket** | Full-duplex connection upgraded from HTTP | [System Design Notes → API Protocols](system_design.md#going-deeper_2) |
| **Idempotency** | Doing an operation twice has the same effect as doing it once | [APIs → Idempotency](apis.md#idempotency) |
| **HTTP Methods** | GET (read), POST (create), PUT (replace), PATCH (modify), DELETE (remove) | [Networking → HTTP Methods](networking.md#http-methods) |
| **Status Codes** | 2xx success, 3xx redirect, 4xx client error, 5xx server error | [APIs → Status Codes](apis.md#status-codes) |
| **API Versioning / Pagination** | Evolve an API without breaking clients / return large lists page by page (cursor or offset) | [APIs → Versioning](apis.md#versioning), [APIs → Pagination](apis.md#pagination) |
| **Webhook / SSE / MQTT** | Server calls your URL when an event happens / one-way server push over HTTP / lightweight pub/sub for IoT | [System Design Notes → API Protocols](system_design.md#3-seven-api-protocols) |
| **OpenAPI (Swagger)** | Machine-readable REST API description used for docs, clients, and tests | [System Design Notes → Types of APIs](system_design.md#going-deeper_1), [openapis.org ↗](https://www.openapis.org/) |
| **SDK** | Software Development Kit: client libraries and tools for a platform or API | [LLM Landscape → Provider SDKs](../../ai/basics/landscape.md#official-provider-sdks), [Wikipedia: SDK ↗](https://en.wikipedia.org/wiki/Software_development_kit) |
| **Client-Server / P2P / Pipe and Filter** | Architecture styles: central server / equal peers / a chain of processing steps | [Architecture → Client-Server](architecture.md#client-server), [Architecture → P2P](architecture.md#peer-to-peer-p2p), [Architecture → Pipe and Filter](architecture.md#pipe-and-filter) |
| **Serverless / FaaS** | Stateless functions run on demand; no servers to manage | [Architecture → Serverless / FaaS](architecture.md#serverless-faas) |
| **ORM / DTO / DAO** | Object–Relational Mapping (work with DB rows as objects) / Data Transfer Object / Data Access Object | [Architecture → DTO, DAO, ORM](architecture.md#talking-to-the-data-layer-dto-dao-orm) |
| **Monolith / Microservices / SOA** | One deployable unit / many small independent services / Service-Oriented Architecture | [Architecture → System-Level Patterns](architecture.md#3-system-level-patterns) |
| **Event-Driven** | Components react to published events instead of calling each other | [Architecture → Event-Driven](architecture.md#event-driven) |
| **UUID** | Universally Unique Identifier (128-bit) | [Wikipedia: UUID ↗](https://en.wikipedia.org/wiki/Universally_unique_identifier) |
| **UTC** | Coordinated Universal Time: store timestamps in it | [Wikipedia: UTC ↗](https://en.wikipedia.org/wiki/Coordinated_Universal_Time) |

## Frontend

| Term | Meaning | Read more |
|---|---|---|
| **HTML / CSS / JS** | Page structure / styling / behavior | [MDN: Web docs ↗](https://developer.mozilla.org/en-US/docs/Web) |
| **DOM** | Document Object Model: the browser's tree of the page | [MDN: DOM ↗](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model) |
| **Accessibility Tree** | The browser's parallel tree of the DOM exposing role, name, and state to assistive tech such as screen readers. Playwright and AI browser agents read it too | [MDN: Accessibility tree ↗](https://developer.mozilla.org/en-US/docs/Glossary/Accessibility_tree) |
| **a11y** | Accessibility ("a" + 11 letters + "y"): usable by people with disabilities | [MDN: Accessibility ↗](https://developer.mozilla.org/en-US/docs/Web/Accessibility) |
| **WCAG** | Web Content Accessibility Guidelines: the W3C standard, levels A / AA / AAA | [W3C: WCAG ↗](https://www.w3.org/WAI/standards-guidelines/wcag/) |
| **ARIA** | Accessible Rich Internet Applications: `role` and `aria-*` attributes that fill gaps in native HTML semantics | [MDN: ARIA ↗](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA) |
| **UI / UX** | User Interface / User Experience | [Lifecycle → Roles](lifecycle.md#roles) |
| **SPA / MPA / SSR / PWA** | Single-Page App / Multi-Page App / Server-Side Rendering / Progressive Web App | [Frontend Toolchain](../tool_tip/frontend_tools.md), [MDN: SPA ↗](https://developer.mozilla.org/en-US/docs/Glossary/SPA) |
| **MVC / MVP / MVVM** | Model-View-Controller / Model-View-Presenter / Model-View-ViewModel | [Architecture → UI Patterns](architecture.md#6-ui-architecture-patterns) |
| **Server State / Client State** | Data owned by the backend and cached / data that lives only in the UI | [Frontend Toolchain → Server vs Client State](../tool_tip/frontend_tools.md#server-state-vs-client-state-redux-query-zustand) |
| **Bundler** | Combines modules and assets into files the browser loads | [Frontend Toolchain → Bundlers](../tool_tip/frontend_tools.md#bundlers-webpack-vite-8) |
| **CORS** | Cross-Origin Resource Sharing: browser rules for cross-origin requests | [MDN: CORS ↗](https://developer.mozilla.org/en-US/docs/Web/HTTP/Guides/CORS) |

## Networking

| Term | Meaning | Read more |
|---|---|---|
| **IP / TCP / UDP** | Internet Protocol / Transmission Control Protocol / User Datagram Protocol | [Networking → TCP/IP Model](networking.md#the-tcpip-model), [Networking → TCP vs UDP](networking.md#tcp-vs-udp) |
| **OSI Model** | 7-layer reference model (physical → application); TCP/IP is the practical 4-layer version | [Wikipedia: OSI ↗](https://en.wikipedia.org/wiki/OSI_model) |
| **Port** | Number that identifies a service on a host (22 SSH, 80 HTTP, 443 HTTPS) | [Running a Server → Network, Ports](../tool_tip/server_operations.md#7-network-ports-and-exposure) |
| **Firewall** | Allows or blocks traffic by rule | [Running a Server → The Exposure Chain](../tool_tip/server_operations.md#the-exposure-chain) |
| **HTTP / HTTPS** | HyperText Transfer Protocol / HTTP over TLS | [Networking → HTTP Methods](networking.md#http-methods), [Networking → Opening a URL](networking.md#what-happens-when-you-open-a-url) |
| **DNS** | Domain Name System: names → IP addresses | [Networking → Opening a URL](networking.md#what-happens-when-you-open-a-url) |
| **TLS / SSL** | Transport Layer Security / its deprecated predecessor, Secure Sockets Layer | [Networking → Opening a URL](networking.md#what-happens-when-you-open-a-url), [Security → Crypto Basics](security.md#crypto-basics) |
| **SSH** | Secure Shell | [System Design Notes → How SSH Works](system_design.md#5-how-ssh-works) |
| **FTP / FTPS / SFTP** | File Transfer Protocol / FTP over TLS / SSH File Transfer Protocol (runs over SSH, not "Secure FTP") | [Wikipedia: SFTP ↗](https://en.wikipedia.org/wiki/SSH_File_Transfer_Protocol) |
| **SMTP / IMAP / POP3** | Send mail / read mail on the server / download mail | [Networking → TCP/IP Model](networking.md#the-tcpip-model), [Wikipedia: Email protocols ↗](https://en.wikipedia.org/wiki/Email#Protocols) |
| **NAT** | Network Address Translation | [CI/CD → How the Platform Reaches Your Code](../tool_tip/cicd.md#2-how-the-platform-reaches-your-code) |
| **ISP** | Internet Service Provider | [Wikipedia: ISP ↗](https://en.wikipedia.org/wiki/Internet_service_provider) |
| **URL / URI** | Uniform Resource Locator / Identifier | [Networking → Opening a URL](networking.md#what-happens-when-you-open-a-url), [MDN: URI ↗](https://developer.mozilla.org/en-US/docs/Web/URI) |

## DevOps & SRE

| Term | Meaning | Read more |
|---|---|---|
| **CI/CD** | Continuous Integration / Continuous Delivery or Deployment | [Lifecycle → CI/CD](lifecycle.md#cicd), [CI/CD Platforms](../tool_tip/cicd.md#0-cicd-is-three-things) |
| **Pipeline** | Automated stages from commit to deploy: lint → test → build → deploy | [Lifecycle → CI/CD](lifecycle.md#cicd), [CI/CD Platforms](../tool_tip/cicd.md) |
| **SRE** | Site Reliability Engineering: operations run as a software problem | [Lifecycle → Roles](lifecycle.md#roles), [Google SRE Book ↗](https://sre.google/sre-book/table-of-contents/) |
| **Environments** | Local → Dev → Staging → Production | [Lifecycle → Environments](lifecycle.md#environments) |
| **Hotfix** | Urgent fix shipped straight to production | [Lifecycle → SDLC Phases](lifecycle.md#sdlc-phases), [Lifecycle → Branching Models](lifecycle.md#branching-models) |
| **Release Notes** | User-facing summary of what changed in a release | [Lifecycle → SDLC Phases](lifecycle.md#sdlc-phases) |
| **Blue-Green / Canary / Rolling / Shadow / A/B** | Deployment strategies that trade cost, speed, and risk | [System Design Notes → Deployment Strategies](system_design.md#6-six-deployment-strategies) |
| **Feature Flag** | Toggle that separates *deploy* from *release* | [System Design Notes → Deployment Strategies](system_design.md#going-deeper_5) |
| **Rollback** | Return to the previous known-good version | [System Design Notes → Deployment Strategies](system_design.md#going-deeper_5), [Becoming Senior → Deployment](becoming_senior.md#deployment-and-scale-are-part-of-the-design) |
| **IaC** | Infrastructure as Code: servers and networks defined in versioned files | [Wikipedia: IaC ↗](https://en.wikipedia.org/wiki/Infrastructure_as_code) |
| **Container / K8s** | Packaged app plus its dependencies / Kubernetes, the container orchestrator | [Running a Server → Containers](../tool_tip/server_operations.md#8-containers-and-orchestration), [Architecture → Container Orchestration](architecture.md#container-orchestration) |
| **Docker** | The standard tool for building and running containers | [Running a Server → Docker Eats the Disk](../tool_tip/server_operations.md#docker-eats-the-disk), [Linux Commands → Docker](../tool_tip/linux_commands.md#docker-essentials) |
| **OOM / Memory Leak** | Out Of Memory, when the kernel kills a process / memory that grows and is never freed | [Running a Server → Out of Memory](../tool_tip/server_operations.md#out-of-memory), [Running a Server → Memory](../tool_tip/server_operations.md#memory) |
| **Inode** | Filesystem entry per file; a disk can run out of inodes before bytes | [Running a Server → Out of Inodes](../tool_tip/server_operations.md#cause-2-out-of-inodes) |
| **Metrics / Logs / Traces** | The three observability signals (Prometheus, Loki, Jaeger; Grafana to view) | [Running a Server → The Pipeline](../tool_tip/server_operations.md#the-pipeline) |
| **tmux** | Terminal multiplexer: persistent sessions, windows, panes | [tmux Cheatsheet](../tool_tip/tmux.md) |
| **SaaS / PaaS / IaaS / FaaS** | Software / Platform / Infrastructure / Functions as a Service | [Architecture → Serverless / FaaS](architecture.md#serverless-faas), [Wikipedia: Cloud service models ↗](https://en.wikipedia.org/wiki/Cloud_computing#Service_models) |
| **Observability** | Understanding a system from its logs, metrics, and traces | [Becoming Senior → Observability](becoming_senior.md#observability-is-a-property-of-the-pipeline) |
| **USE Method** | Utilization, Saturation, Errors: check every resource | [Running a Server → The USE Method](../tool_tip/server_operations.md#3-the-use-method) |
| **SLA** | Service Level Agreement: a contract with customers, with penalties if missed | [Becoming Senior → Business Capabilities](becoming_senior.md#think-in-business-capabilities-not-frameworks), [Google SRE: SLOs ↗](https://sre.google/sre-book/service-level-objectives/) |
| **SLO** | Service Level Objective: the internal target, e.g. 99.5% over 30 days | [Becoming Senior → Reliability](becoming_senior.md#reliability-is-measured-not-felt) |
| **SLI** | Service Level Indicator: the measured value, e.g. success rate or p99 latency | [Becoming Senior → Reliability](becoming_senior.md#reliability-is-measured-not-felt) |
| **Error Budget** | `100% − SLO`: the failure you may spend on change | [Becoming Senior → Reliability](becoming_senior.md#reliability-is-measured-not-felt) |
| **Nines** | Availability as a count of nines: 99.9% ≈ 43 min down per month, 99.99% ≈ 4.3 min | [Google SRE: Availability table ↗](https://sre.google/sre-book/availability-table/) |
| **p50 / p90 / p95 / p99** | Latency percentiles: p95 = 95% of requests are faster than this. p50 is the median; p99 and p99.9 show the tail that averages hide | [Becoming Senior → Reliability](becoming_senior.md#reliability-is-measured-not-felt), [Running a Server → Matching the workload](../tool_tip/server_operations.md#matching-the-workload), [System Design Notes → Retry and Resilience](system_design.md#going-deeper_6) |
| **MTTR / MTBF / MTTD** | Mean Time To Recovery / Between Failures / To Detect | [Wikipedia: MTTR ↗](https://en.wikipedia.org/wiki/Mean_time_to_recovery), [Wikipedia: MTBF ↗](https://en.wikipedia.org/wiki/Mean_time_between_failures) |
| **RPO / RTO** | Recovery Point Objective (data you may lose) / Recovery Time Objective (downtime you may take) | [Becoming Senior → Deployment](becoming_senior.md#deployment-and-scale-are-part-of-the-design) |
| **Incident / On-call / SEV** | Unplanned disruption / the engineer paged to respond / severity level | [Becoming Senior → Escalation](becoming_senior.md#escalation-is-a-designed-path) |
| **Runbook** | Step-by-step guide for handling a known operational situation | [Running a Server → Runbooks](../tool_tip/server_operations.md#11-runbooks) |
| **Postmortem** | Blameless write-up of an incident: impact, timeline, causes, actions | [Becoming Senior → How to Practice](becoming_senior.md#how-to-practice), [Google SRE: Postmortem Culture ↗](https://sre.google/sre-book/postmortem-culture/) |
| **RCA** | Root Cause Analysis | [Wikipedia: RCA ↗](https://en.wikipedia.org/wiki/Root_cause_analysis) |

## Security, Privacy & Compliance

| Term | Meaning | Read more |
|---|---|---|
| **AuthN / AuthZ** | Authentication (who you are) / Authorization (what you may do) | [Security → Authentication vs Authorization](security.md#authentication-vs-authorization) |
| **MFA** | Multi-Factor Authentication | [Security → Authentication vs Authorization](security.md#authentication-vs-authorization) |
| **SSO** | Single Sign-On | [Security → Authentication vs Authorization](security.md#authentication-vs-authorization), [System Design Notes → Auth Methods](system_design.md#4-six-auth-methods) |
| **OAuth 2.0** | Authorization framework for delegated access | [System Design Notes → Auth Methods](system_design.md#4-six-auth-methods) |
| **OIDC** | OpenID Connect: authentication on top of OAuth 2.0 | [Security → Authentication vs Authorization](security.md#authentication-vs-authorization) |
| **JWT** | JSON Web Token: compact, signed claims-based token | [System Design Notes → Auth Methods](system_design.md#going-deeper_3) |
| **SAML / mTLS** | XML-based enterprise SSO / mutual TLS, where both sides present certificates | [System Design Notes → Auth Methods](system_design.md#going-deeper_3) |
| **RBAC / ABAC** | Role- / Attribute-Based Access Control | [Data Security → What It Is](../../data/basics/data_security.md#what-it-is) |
| **Least Privilege** | Grant the minimum access needed | [Data Security → What It Is](../../data/basics/data_security.md#what-it-is) |
| **Hashing / Salt** | One-way fingerprint of data / random value added so equal passwords hash differently (bcrypt, argon2) | [Security → Crypto Basics](security.md#crypto-basics) |
| **Symmetric / Asymmetric Encryption** | One shared key (AES) / public–private key pair (RSA, ECC) | [Security → Crypto Basics](security.md#crypto-basics) |
| **Digital Signature / HMAC** | Proves who sent data and that it wasn't changed | [Security → Crypto Basics](security.md#crypto-basics) |
| **Certificate / CA / PKI** | Signed binding of a public key to a name / the authority that signs it / the whole trust system | [System Design Notes → Auth Methods](system_design.md#going-deeper_3), [Wikipedia: PKI ↗](https://en.wikipedia.org/wiki/Public_key_infrastructure) |
| **Encryption at Rest / in Transit** | Protect stored data / data moving over the network (TLS) | [Security → Crypto Basics](security.md#crypto-basics), [Data Security → What It Is](../../data/basics/data_security.md#what-it-is) |
| **Session / Cookie** | Server-side login state / the browser value that points to it | [System Design Notes → Auth Methods](system_design.md#going-deeper_3) |
| **Data Classification** | Public / Internal / Confidential / Restricted tiers that decide protection | [Data Security → What It Is](../../data/basics/data_security.md#what-it-is) |
| **Masking / Tokenization / Anonymization / Pseudonymization** | Ways to de-identify data for non-prod and analytics | [Data Security → What It Is](../../data/basics/data_security.md#what-it-is) |
| **Audit Log** | Record of who accessed or changed what, and when | [Data Security → What It Is](../../data/basics/data_security.md#what-it-is) |
| **DDoS / WAF** | Distributed Denial of Service flood / Web Application Firewall that filters malicious HTTP | [Architecture → CDN](architecture.md#cdn-content-delivery-network), [Wikipedia: WAF ↗](https://en.wikipedia.org/wiki/Web_application_firewall) |
| **OWASP** | Open Worldwide Application Security Project, known for its Top 10 web risks | [Security → Common Risks](security.md#common-risks-owasp-condensed) |
| **XSS / CSRF / SSRF / SQLi** | Cross-Site Scripting / Cross-Site Request Forgery / Server-Side Request Forgery / SQL Injection | [Security → Common Risks](security.md#common-risks-owasp-condensed) |
| **Path Traversal** | Using `../` in a file path to read files outside the allowed directory | [OWASP: Path Traversal ↗](https://owasp.org/www-community/attacks/Path_Traversal) |
| **CVE** | Common Vulnerabilities and Exposures: public IDs for known flaws | [Security → Common Risks](security.md#common-risks-owasp-condensed) |
| **Secrets** | Credentials and keys, which belong in a secret store and never in code | [CI/CD → Environment Variables and Secrets](../tool_tip/cicd.md#8-environment-variables-and-secrets) |
| **PII** | Personally Identifiable Information: data that identifies a person (name, email, ID number) | [Data Security → What It Is](../../data/basics/data_security.md#what-it-is) |
| **PHI** | Protected Health Information: health data tied to a person (US, HIPAA) | [Data Security → What It Is](../../data/basics/data_security.md#what-it-is) |
| **PCI DSS** | Payment Card Industry Data Security Standard: rules for card data | [Data Security → Frameworks](../../data/basics/data_security.md#frameworks-that-apply) |
| **HIPAA** | US Health Insurance Portability and Accountability Act: protects PHI | [Data Security → Frameworks](../../data/basics/data_security.md#frameworks-that-apply), [Wikipedia: HIPAA ↗](https://en.wikipedia.org/wiki/Health_Insurance_Portability_and_Accountability_Act) |
| **GDPR** | EU General Data Protection Regulation: protects personal data of people in the EU | [Data Security → Frameworks](../../data/basics/data_security.md#frameworks-that-apply) |
| **CCPA** | California Consumer Privacy Act | [Data Security → Frameworks](../../data/basics/data_security.md#frameworks-that-apply) |
| **SOC 2** | Audit report on a service provider's security, availability, and confidentiality controls | [Wikipedia: SOC 2 ↗](https://en.wikipedia.org/wiki/System_and_Organization_Controls) |
| **ISO/IEC 27001 / NIST CSF** | Information-security management standard / US cybersecurity framework | [Data Security → Frameworks](../../data/basics/data_security.md#frameworks-that-apply) |
| **DLP** | Data Loss Prevention | [Data Security → What It Is](../../data/basics/data_security.md#what-it-is) |

## Data Engineering

| Term | Meaning | Read more |
|---|---|---|
| **DB / RDB / RDBMS** | Database / Relational Database / Relational Database Management System | [Databases → Relational vs NoSQL](../../data/basics/databases.md#relational-vs-nosql) |
| **SQL / NoSQL** | Structured Query Language / non-relational stores | [Databases → SQL in One Breath](../../data/basics/databases.md#sql-in-one-breath), [Databases → Relational vs NoSQL](../../data/basics/databases.md#relational-vs-nosql) |
| **DDL / DML** | Data Definition (CREATE, ALTER) / Data Manipulation (INSERT, UPDATE, DELETE) | [Databases → SQL in One Breath](../../data/basics/databases.md#sql-in-one-breath) |
| **PK / FK / JOIN** | Primary Key (unique row id) / Foreign Key (reference to another table) / combine rows across tables | [Databases → SQL in One Breath](../../data/basics/databases.md#sql-in-one-breath) |
| **Relational DB** | Tables with fixed schema, joins, ACID transactions (PostgreSQL, MySQL) | [Architecture → Databases](architecture.md#databases) |
| **Document DB** | Stores JSON-like documents with flexible schema (MongoDB) | [Architecture → Databases](architecture.md#databases), [Wikipedia: Document DB ↗](https://en.wikipedia.org/wiki/Document-oriented_database) |
| **Key-Value Store** | Lookup by key only; fastest and simplest (Redis, DynamoDB) | [Architecture → Databases](architecture.md#databases), [Wikipedia: Key–value DB ↗](https://en.wikipedia.org/wiki/Key%E2%80%93value_database) |
| **Wide-Column Store** | Rows with dynamic columns, partitioned for huge write volume (Cassandra, HBase) | [Architecture → Databases](architecture.md#databases), [Wikipedia: Wide-column ↗](https://en.wikipedia.org/wiki/Wide-column_store) |
| **Graph DB** | Nodes and edges as first-class data; fast relationship traversal (Neo4j, Neptune) | [Architecture → Databases](architecture.md#databases), [Wikipedia: Graph database ↗](https://en.wikipedia.org/wiki/Graph_database) |
| **Vector DB** | Stores embeddings and finds nearest neighbors by similarity, the retrieval layer for RAG (pgvector, Pinecone, Qdrant) | [Wikipedia: Vector database ↗](https://en.wikipedia.org/wiki/Vector_database) |
| **Time-Series DB** | Optimized for timestamped metrics and events (InfluxDB, TimescaleDB, Prometheus) | [Wikipedia: Time series DB ↗](https://en.wikipedia.org/wiki/Time_series_database) |
| **Search Engine** | Inverted index for full-text search and ranking (Elasticsearch, OpenSearch) | [Wikipedia: Search engine ↗](https://en.wikipedia.org/wiki/Search_engine_(computing)) |
| **In-Memory DB** | Keeps data in RAM for microsecond access (Redis, Memcached) | [Tech Stacks → Databases](tech_stacks.md#databases-at-a-glance), [Wikipedia: In-memory DB ↗](https://en.wikipedia.org/wiki/In-memory_database) |
| **NewSQL** | Relational and ACID, but scales out horizontally (CockroachDB, Spanner) | [Wikipedia: NewSQL ↗](https://en.wikipedia.org/wiki/NewSQL) |
| **Embedding** | A vector of numbers that represents the meaning of text, images, or other data | [Wikipedia: Embedding ↗](https://en.wikipedia.org/wiki/Embedding_(machine_learning)) |
| **Index** | Lookup structure that speeds reads and slows writes | [Databases → Indexing](../../data/basics/databases.md#indexing) |
| **ACID** | Atomicity, Consistency, Isolation, Durability | [Databases → Transactions & ACID](../../data/basics/databases.md#transactions-acid) |
| **Isolation Levels** | Read Uncommitted → Read Committed → Repeatable Read → Serializable: stronger isolation means fewer anomalies and less concurrency | [Databases → Isolation Levels](../../data/basics/databases.md#isolation-levels) |
| **Normalization / 3NF / Denormalization** | Remove redundancy by splitting tables / third normal form / add redundancy back for read speed | [Data Modelling → Modelling Styles](../../data/basics/data_modeling.md#modelling-styles), [Wikipedia: Normalization ↗](https://en.wikipedia.org/wiki/Database_normalization) |
| **WAL** | Write-Ahead Log: log changes before applying them, for durability and recovery | [Wikipedia: WAL ↗](https://en.wikipedia.org/wiki/Write-ahead_logging) |
| **OLTP / OLAP** | Online Transaction Processing / Online Analytical Processing | [Data Modelling → Modelling Styles](../../data/basics/data_modeling.md#modelling-styles) |
| **ETL / ELT** | Extract-Transform-Load / Extract-Load-Transform | [Data Engineering → ETL vs ELT](../../data/basics/data_engineering.md#etl-vs-elt) |
| **Warehouse / Lake / Lakehouse** | Where data lands: modeled tables / raw files / both on one store | [Data Engineering → Where Data Lands](../../data/basics/data_engineering.md#where-data-lands) |
| **Batch / Streaming** | Process data in scheduled chunks / continuously as it arrives | [Data Engineering → Batch vs Streaming](../../data/basics/data_engineering.md#batch-vs-streaming) |
| **DAG** | Directed Acyclic Graph: pipeline tasks and their dependencies | [Data Engineering → Orchestration](../../data/basics/data_engineering.md#orchestration) |
| **MapReduce / Spark / HDFS** | Distributed processing and storage across many nodes | [Big Data → Distributed Processing](../../data/basics/big_data.md#distributed-processing) |
| **Star / Snowflake Schema** | Fact table surrounded by dimension tables (normalized dimensions in snowflake) | [Data Modelling → Modelling Styles](../../data/basics/data_modeling.md#modelling-styles) |
| **OBT** | One Big Table: wide denormalized table for simple BI | [Data Modelling → Modelling Styles](../../data/basics/data_modeling.md#modelling-styles) |
| **Structured / Semi-structured / Unstructured** | Tables / self-describing formats like JSON / free text, images, audio | [Introduction to Data → Types of Data](../../data/basics/introduction_to_data.md#types-of-data) |
| **Metadata** | Data about data: schema, source, owner, freshness | [Introduction to Data → Metadata](../../data/basics/introduction_to_data.md#metadata-the-context-around-data) |
| **Data Lifecycle** | Create → store → use → share → archive → destroy | [Introduction to Data → Data Lifecycle](../../data/basics/introduction_to_data.md#data-lifecycle) |
| **5 V's of Big Data** | Volume, Velocity, Variety, Veracity, Value | [Big Data → The V's](../../data/basics/big_data.md#the-vs) |
| **JSON / XML / YAML** | JavaScript Object Notation / eXtensible Markup Language / YAML Ain't Markup Language | [Introduction to Data → Types of Data](../../data/basics/introduction_to_data.md#types-of-data) |
| **CSV / TSV** | Comma- / Tab-Separated Values | [Data Engineering → File Formats](../../data/basics/data_engineering.md#file-formats) |
| **Data Quality** | Accuracy, completeness, consistency, timeliness of data | [Introduction to Data → Quality Dimensions](../../data/basics/introduction_to_data.md#data-quality-dimensions), [Data Quality](../../data/basics/data_quality.md) |
| **Data Governance** | Ownership, policies, and stewardship of data | [Data Governance](../../data/basics/data_governance.md#what-it-is) |

## Data Analysis

| Term | Meaning | Read more |
|---|---|---|
| **Descriptive / Diagnostic / Predictive / Prescriptive** | What happened / why / what will happen / what to do | [Analytics → Four Kinds](../../data/basics/analytics.md#four-kinds-of-analytics) |
| **EDA** | Exploratory Data Analysis | [Analytics → EDA](../../data/basics/analytics.md#exploratory-data-analysis-eda) |
| **Mean / Median / Percentile** | Average / middle value / value below which a given share of data falls | [Analytics → Descriptive Statistics](../../data/basics/analytics.md#descriptive-statistics) |
| **Variance / Std Dev / IQR / Outlier** | Spread around the mean / its square root / middle 50% range / a point far from the rest | [Analytics → Descriptive Statistics](../../data/basics/analytics.md#descriptive-statistics) |
| **Levels of Measurement** | Nominal, ordinal, interval, ratio: which math is valid on a variable | [Introduction to Data → Levels of Measurement](../../data/basics/introduction_to_data.md#levels-of-measurement) |
| **p-value / Statistical Significance** | Chance of seeing a result this extreme if there were no real effect / below a chosen threshold (often 0.05) | [Wikipedia: p-value ↗](https://en.wikipedia.org/wiki/P-value) |
| **Chart Choice** | Pick the chart by the relationship: comparison, trend, distribution, composition | [Visualization → Pick the Chart](../../data/basics/visualization.md#pick-the-chart-by-the-relationship) |
| **Correlation vs Causation** | Moving together is not proof that one causes the other | [Analytics → Traps to Avoid](../../data/basics/analytics.md#traps-to-avoid) |
| **BI** | Business Intelligence: reporting and dashboards on modeled data | [Data Engineering → Where Data Lands](../../data/basics/data_engineering.md#where-data-lands) |
| **Dashboard** | At-a-glance view of key metrics | [Visualization → Dashboards](../../data/basics/visualization.md#dashboards) |
| **DIKW** | Data → Information → Knowledge → Wisdom | [Introduction to Data → DIKW](../../data/basics/introduction_to_data.md#the-dikw-pyramid) |
| **KPI** | Key Performance Indicator (see [Management & Work Items](#management-work-items)) | [Wikipedia: KPI ↗](https://en.wikipedia.org/wiki/Performance_indicator) |

## AI & LLM

| Term | Meaning | Read more |
|---|---|---|
| **ML / DL** | Machine Learning (learn patterns from data) / Deep Learning (many-layer neural networks) | [AI Concepts → Machine Learning](../../ai/basics/concepts.md#machine-learning), [AI Concepts → Deep Learning](../../ai/basics/concepts.md#deep-learning) |
| **GenAI** | Generative AI: models that produce text, images, code, audio | [AI Concepts → Generative AI](../../ai/basics/concepts.md#generative-ai) |
| **LLM** | Large Language Model | [The LLM Landscape](../../ai/basics/landscape.md), [Wikipedia: LLM ↗](https://en.wikipedia.org/wiki/Large_language_model) |
| **Token / Context Window** | The unit a model reads and writes (roughly ¾ of a word) / how many tokens it can attend to at once | [Claude Code → Manage Context](../../ai/tool_tip/claude_code.md#1-manage-context) |
| **Prompt / Prompt Engineering** | The input given to a model / shaping that input for reliable output | [Wikipedia: Prompt engineering ↗](https://en.wikipedia.org/wiki/Prompt_engineering) |
| **Agent** | LLM that plans and calls tools in a loop toward a goal | [AI Concepts → AI Agents](../../ai/basics/concepts.md#ai-agents), [Skills Map → Coding Agents](../../ai/basics/skills_map.md#3-using-coding-agents) |
| **MCP** | Model Context Protocol: open standard connecting models to tools and data | [LLM Landscape → Protocols](../../ai/basics/landscape.md#protocols), [modelcontextprotocol.io ↗](https://modelcontextprotocol.io/) |
| **A2A / ACP** | Agent-to-Agent protocol / Agent Client Protocol (agents ↔ editors) | [LLM Landscape → Protocols](../../ai/basics/landscape.md#protocols) |
| **Agent SDK** | Library for building agents: tool loop, memory, handoffs | [LLM Landscape → Agent SDKs](../../ai/basics/landscape.md#official-agent-sdks) |
| **Subagent** | Child agent with its own context window that reports a summary back | [Claude Code → Subagent Memory](../../ai/tool_tip/claude_code.md#subagent-memory), [Codex → Subagents](../../ai/tool_tip/codex.md#subagents) |
| **Skill / Hook / Plugin** | Packaged instructions loaded on demand / script run on agent events / bundle of both for sharing | [Claude Code → Skills](../../ai/tool_tip/claude_code.md#skills), [Claude Code → Hooks](../../ai/tool_tip/claude_code.md#hooks), [Claude Code → Plugins](../../ai/tool_tip/claude_code.md#plugins) |
| **Ralph Loop** | Run an agent repeatedly against a spec until the work is done | [Claude Code → The Ralph Loop](../../ai/tool_tip/claude_code.md#the-ralph-loop) |
| **System Prompt / Few-shot / Temperature** | Standing instructions / examples in the prompt / randomness of sampling | [Wikipedia: Prompt engineering ↗](https://en.wikipedia.org/wiki/Prompt_engineering) |
| **Local Inference** | Running models on your own hardware (Ollama, vLLM, llama.cpp) | [AI Tools → Local Inference](../../ai/tool_tip/tools.md#local-inference-and-serving) |
| **RAG** | Retrieval-Augmented Generation: fetch relevant documents (often from a vector DB) and put them in the prompt | [Skills Map → Building AI Apps](../../ai/basics/skills_map.md#1-building-and-deploying-ai-applications), [Wikipedia: RAG ↗](https://en.wikipedia.org/wiki/Retrieval-augmented_generation) |
| **Embedding / Vector DB** | Meaning as a vector / a store that searches by vector similarity | [Data Engineering](#data-engineering) |
| **Fine-tuning** | Further training a pre-trained model on task-specific data | [Wikipedia: Fine-tuning ↗](https://en.wikipedia.org/wiki/Fine-tuning_(deep_learning)) |
| **Hallucination** | Fluent output that is false or unsupported | [AI Posts](../../ai/basics/posts.md), [Wikipedia: Hallucination ↗](https://en.wikipedia.org/wiki/Hallucination_(artificial_intelligence)) |
| **Evals** | Repeatable test sets and metrics that score model or agent output | [AI Tools → Evaluate Before Expanding](../../ai/tool_tip/tools.md#evaluate-before-expanding), [LLM Landscape → Observability & Evaluation](../../ai/basics/landscape.md#observability-evaluation) |
| **Guardrails** | Checks around a model or agent that block unsafe input, output, or actions | [Claude Code → Hooks](../../ai/tool_tip/claude_code.md#worked-examples) |
| **Prompt Injection** | Untrusted content (a web page, file, or email) smuggles instructions the model then follows | [Codex → Avoid the Sharp Edges](../../ai/tool_tip/codex.md#7-avoid-the-sharp-edges), [Wikipedia: Prompt injection ↗](https://en.wikipedia.org/wiki/Prompt_injection) |
| **Jailbreak** | A prompt crafted to bypass a model's safety rules | [OWASP Top 10 for LLM Apps ↗](https://owasp.org/www-project-top-10-for-large-language-model-applications/) |
| **Adversarial Test / Red Teaming** | Attack your own LLM system with hostile inputs (injection, jailbreaks, data extraction) before real attackers do | [Testing & QA](#testing-qa), [Wikipedia: Adversarial ML ↗](https://en.wikipedia.org/wiki/Adversarial_machine_learning), [Wikipedia: Red team ↗](https://en.wikipedia.org/wiki/Red_team) |
| **SDD** | Spec-Driven Development with AI agents | [Spec-Driven Development](../../ai/tool_tip/spec_driven_development.md) |
| **GSD / BMad / Spec Kit / Agent OS** | Spec-driven tooling approaches for AI coding | [Spec-Driven Development → Four Tooling Approaches](../../ai/tool_tip/spec_driven_development.md#four-tooling-approaches) |
