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
| **Iteration / Timebox** | One cycle of build-and-review / a fixed, non-extendable slot of time | [Lifecycle → Agile, Scrum, Kanban](lifecycle.md#agile-scrum-kanban) |
| **Sprint Goal / Product Goal** | The single objective of a sprint / the long-term target the backlog serves | [Scrum Guide ↗](https://scrumguides.org/scrum-guide.html) |
| **Kanban Board / Swimlane** | Columns for workflow states (To Do → Doing → Done) / horizontal rows grouping work by type or owner | [Methodologies → Kanban](methodologies.md#4-kanban-finish-before-you-start-something-new), [Wikipedia: Kanban board ↗](https://en.wikipedia.org/wiki/Kanban_board) |
| **CFD** | Cumulative Flow Diagram: work items per state over time; widening bands show bottlenecks | [Wikipedia: Cumulative flow diagram ↗](https://en.wikipedia.org/wiki/Cumulative_flow_diagram) |
| **Planning Poker / T-shirt Sizing** | Team estimation by simultaneous cards / rough XS–XL sizing | [Wikipedia: Planning poker ↗](https://en.wikipedia.org/wiki/Planning_poker) |
| **INVEST** | Good user stories are Independent, Negotiable, Valuable, Estimable, Small, Testable | [Wikipedia: INVEST ↗](https://en.wikipedia.org/wiki/INVEST_(mnemonic)) |
| **Three Amigos** | Business, dev, and QA review a story together before work starts | [Agile Alliance: Three Amigos ↗](https://www.agilealliance.org/glossary/three-amigos/) |
| **ART / Release Train** | Agile Release Train: the team of teams in SAFe that plans and ships together each PI | [Wikipedia: SAFe ↗](https://en.wikipedia.org/wiki/Scaled_agile_framework) |
| **Kaizen** | Continuous small improvements, the Lean habit behind retrospectives | [Wikipedia: Kaizen ↗](https://en.wikipedia.org/wiki/Kaizen) |
| **Value Stream** | All steps from request to value delivered; mapped to find waste | [Wikipedia: Value-stream mapping ↗](https://en.wikipedia.org/wiki/Value-stream_mapping) |
| **Shift Left** | Move testing, security, and quality checks earlier in the lifecycle | [Wikipedia: Shift-left testing ↗](https://en.wikipedia.org/wiki/Shift-left_testing) |
| **Code Freeze / Feature Freeze** | No changes except critical fixes / no new features, before a release | [Wikipedia: Freeze ↗](https://en.wikipedia.org/wiki/Freeze_(software_engineering)) |
| **RC / GA** | Release Candidate (final test build) / General Availability (released to everyone) | [Wikipedia: Software release life cycle ↗](https://en.wikipedia.org/wiki/Software_release_life_cycle) |
| **LTS / EOL** | Long-Term Support release / End Of Life, when support stops | [Wikipedia: Long-term support ↗](https://en.wikipedia.org/wiki/Long-term_support), [Wikipedia: End-of-life product ↗](https://en.wikipedia.org/wiki/End-of-life_product) |
| **Deprecation** | Marking a feature as obsolete before removal so users can migrate | [Wikipedia: Deprecation ↗](https://en.wikipedia.org/wiki/Deprecation) |
| **Dogfooding** | Using your own product internally before customers do | [Wikipedia: Dogfooding ↗](https://en.wikipedia.org/wiki/Eating_your_own_dog_food) |
| **Maintenance** | The SDLC phase after release: fixes, monitoring, small improvements | [Lifecycle → SDLC Phases](lifecycle.md#sdlc-phases) |

## Management & Work Items

| Term | Meaning | Read more |
|---|---|---|
| **PO** | Product Owner: owns the backlog and its priorities | [Lifecycle → Roles](lifecycle.md#roles) |
| **SM** | Scrum Master: facilitates the process and removes blockers | [Lifecycle → Roles](lifecycle.md#roles) |
| **PM** | Product Manager (sometimes Project Manager) | [Lifecycle → Roles](lifecycle.md#roles) |
| **BA** | Business Analyst: turns business needs into specs | [Lifecycle → Roles](lifecycle.md#roles) |
| **Tech Lead / Architect** | Owns technical direction and system design | [Lifecycle → Roles](lifecycle.md#roles) |
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
| **Roadmap** | Time-ordered plan of goals and major deliverables, usually by quarter | [Wikipedia: Technology roadmap ↗](https://en.wikipedia.org/wiki/Technology_roadmap) |
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
| **CTO / EM / IC** | Chief Technology Officer / Engineering Manager (people lead) / Individual Contributor (hands-on track) | [Wikipedia: CTO ↗](https://en.wikipedia.org/wiki/Chief_technology_officer) |
| **Junior / Mid / Senior / Staff / Principal** | Engineering career levels, from guided work to org-wide technical leadership | [Becoming Senior → The Ladder](becoming_senior.md#the-ladder) |
| **PL** | Project Leader or Team Leader: leads a dev team day to day, under the PM | [Wikipedia: Team leader ↗](https://en.wikipedia.org/wiki/Team_leader) |
| **SME** | Subject Matter Expert: the go-to person for a domain | [Wikipedia: Subject-matter expert ↗](https://en.wikipedia.org/wiki/Subject-matter_expert) |
| **BrSE / Comtor** | Bridge System Engineer (links an offshore team with a Japanese client) / Communicator (interpreter on the project) | [Wikipedia: Offshore outsourcing ↗](https://en.wikipedia.org/wiki/Offshore_outsourcing) |
| **ODC / Onsite / Offshore** | Offshore Development Center (a dedicated remote team) / staff at the client site / staff in the vendor country | [Wikipedia: Offshore outsourcing ↗](https://en.wikipedia.org/wiki/Offshore_outsourcing) |
| **MM / MD / Effort** | Man-Month / Man-Day: the units for estimating and billing effort | [Wikipedia: Man-hour ↗](https://en.wikipedia.org/wiki/Man-hour), [Wikipedia: The Mythical Man-Month ↗](https://en.wikipedia.org/wiki/The_Mythical_Man-Month) |
| **Estimation** | Forecasting effort, cost, and time (bottom-up, analogy, story points) | [Atlassian: Estimation ↗](https://www.atlassian.com/agile/project-management/estimation) |
| **Baseline** | Approved version of scope, schedule, or cost that progress is measured against | [Wikipedia: Baseline ↗](https://en.wikipedia.org/wiki/Baseline_(configuration_management)) |
| **Q&A Sheet** | Shared log of questions to the client and their answers, used to clarify requirements | [Wikipedia: Requirements elicitation ↗](https://en.wikipedia.org/wiki/Requirements_elicitation) |
| **RFI / RFQ** | Request for Information / Request for Quotation, early steps of procurement | [Wikipedia: Request for information ↗](https://en.wikipedia.org/wiki/Request_for_information), [Wikipedia: Request for quotation ↗](https://en.wikipedia.org/wiki/Request_for_quotation) |
| **MSA** | Master Service Agreement: umbrella contract; each SOW adds specific work under it | [Wikipedia: Master service agreement ↗](https://en.wikipedia.org/wiki/Master_service_agreement) |
| **Priority / Severity** | How soon to fix (business order) / how bad the impact is (technical damage) | [Becoming Senior → Escalation](becoming_senior.md#escalation-is-a-designed-path), [Wikipedia: Bug tracking system ↗](https://en.wikipedia.org/wiki/Bug_tracking_system) |
| **P0 / P1 / P2** | Priority levels: drop everything / next up / normal queue | [Codex → GitHub Codex Review](../../ai/tool_tip/codex.md#github-codex-review) |
| **Defect Density** | Defects per size unit (per KLOC or per function point): a quality KPI | [Wikipedia: Software quality ↗](https://en.wikipedia.org/wiki/Software_quality) |
| **Onboarding / Handover** | Bringing someone up to speed / transferring ownership with docs and knowledge | [Wikipedia: Knowledge transfer ↗](https://en.wikipedia.org/wiki/Knowledge_transfer) |
| **Capacity Planning** | Matching people or infrastructure to forecast demand | [Becoming Senior → Deployment and Scale](becoming_senior.md#deployment-and-scale-are-part-of-the-design), [Wikipedia: Capacity planning ↗](https://en.wikipedia.org/wiki/Capacity_planning) |

## Requirements & Design

| Term | Meaning | Read more |
|---|---|---|
| **BRD** | Business Requirements Document: what the business needs and why | [Lifecycle → SDLC Phases](lifecycle.md#sdlc-phases) |
| **PRD** | Product Requirements Document: what the product must do, for whom | [Wikipedia: PRD ↗](https://en.wikipedia.org/wiki/Product_requirements_document) |
| **FR** | Functional Requirement: *what* the system does, e.g. "a user can reset their password by email" | [Lifecycle → Testing](lifecycle.md#testing), [Wikipedia: Functional requirement ↗](https://en.wikipedia.org/wiki/Functional_requirement) |
| **NFR** | Non-Functional Requirement: *how well* it does it: performance, security, availability, usability, scalability | [Lifecycle → Testing](lifecycle.md#testing), [System Design Notes → Types of APIs](system_design.md#going-deeper_1), [Wikipedia: NFR ↗](https://en.wikipedia.org/wiki/Non-functional_requirement) |
| **FRS** | Functional Requirements Specification: document listing what the system must do, feature by feature, with inputs, outputs, business rules, and error cases | [Lifecycle → SDLC Phases](lifecycle.md#sdlc-phases) |
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
| **UML** | Unified Modeling Language: standard diagrams (class, sequence, activity, state) | [Wikipedia: Unified Modeling Language ↗](https://en.wikipedia.org/wiki/Unified_Modeling_Language) |
| **Sequence Diagram** | Messages between participants over time | [Networking → Opening a URL](networking.md#what-happens-when-you-open-a-url), [Wikipedia: Sequence diagram ↗](https://en.wikipedia.org/wiki/Sequence_diagram) |
| **ERD** | Entity-Relationship Diagram: entities, attributes, relationships | [Data Modelling → What It Is](../../data/basics/data_modeling.md#what-it-is), [Wikipedia: ER model ↗](https://en.wikipedia.org/wiki/Entity–relationship_model) |
| **C4 Model** | Architecture diagrams at four zoom levels: Context, Container, Component, Code | [c4model.com ↗](https://c4model.com/) |
| **Flowchart / Activity Diagram** | Steps and decisions of a process | [Wikipedia: Flowchart ↗](https://en.wikipedia.org/wiki/Flowchart) |
| **Wireframe / Mockup / Prototype** | Low-fidelity layout / high-fidelity static design / clickable or working model | [Wikipedia: Wireframe ↗](https://en.wikipedia.org/wiki/Website_wireframe), [Wikipedia: Prototyping ↗](https://en.wikipedia.org/wiki/Software_prototyping) |
| **Persona / User Journey** | Archetype of a target user / the steps they take to reach a goal | [Wikipedia: Persona ↗](https://en.wikipedia.org/wiki/Persona_(user_experience)), [Wikipedia: Customer journey ↗](https://en.wikipedia.org/wiki/Customer_experience) |
| **RTM** | Requirements Traceability Matrix: links each requirement to its design, code, and tests | [Wikipedia: Traceability matrix ↗](https://en.wikipedia.org/wiki/Traceability_matrix) |
| **Assumption / Constraint** | Things taken as true without proof / fixed limits (budget, tech, law) | [Wikipedia: Requirement ↗](https://en.wikipedia.org/wiki/Requirement) |
| **Scope / Out of Scope** | What the project will deliver / what it explicitly won't | [Wikipedia: Scope ↗](https://en.wikipedia.org/wiki/Scope_(project_management)) |
| **Edge Case** | Unusual or boundary input or state the design must handle (empty, max size, concurrent, offline) | [Wikipedia: Happy path ↗](https://en.wikipedia.org/wiki/Happy_path), [Wikipedia: Edge case ↗](https://en.wikipedia.org/wiki/Edge_case) |
| **Conceptual / Logical / Physical Model** | What entities exist / which attributes and keys / how it's stored in a specific DB | [Data Modelling → What It Is](../../data/basics/data_modeling.md#what-it-is) |
| **Trade-off** | Choosing one quality at another's expense: consistency vs availability, speed vs cost | [Architecture → Choosing an Architecture](architecture.md#choosing-an-architecture), [Design Principles → When Principles Conflict](principles.md#when-principles-conflict) |

## Coding

| Term | Meaning | Read more |
|---|---|---|
| **OOP** | Object-Oriented Programming: organize code as objects that bundle data with the methods that act on it, using classes, encapsulation, inheritance, and polymorphism | [Fundamentals → Programming Paradigms](fundamentals.md#programming-paradigms) |
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
| **Mutex / Lock / Semaphore / Atomic** | Mutex or lock: only one holder at a time. Semaphore: at most N holders. Atomic: an operation other threads can never observe half-done | [Concurrency → Primitives & Models](concurrency.md#primitives-models) |
| **GIL** | Python's Global Interpreter Lock: one thread runs bytecode at a time | [Concurrency → Units of Execution](concurrency.md#units-of-execution) |
| **Pair / Mob Programming** | Two people / the whole team working on one change at one screen | [Methodologies → XP](methodologies.md#6-xp-extreme-programming), [Wikipedia: Pair programming ↗](https://en.wikipedia.org/wiki/Pair_programming) |
| **CLI** | Command Line Interface | [Wikipedia: CLI ↗](https://en.wikipedia.org/wiki/Command-line_interface), [LLM Landscape → CLI Coding Agents](../../ai/basics/landscape.md#cli-coding-agents) |
| **GUI** | Graphical User Interface | [Wikipedia: GUI ↗](https://en.wikipedia.org/wiki/Graphical_user_interface) |
| **IDE** | Integrated Development Environment | [Wikipedia: IDE ↗](https://en.wikipedia.org/wiki/Integrated_development_environment) |
| **JIT** | Just-in-time compilation: compile code at runtime | [Wikipedia: JIT ↗](https://en.wikipedia.org/wiki/Just-in-time_compilation) |
| **SRP / OCP / LSP / ISP / DIP** | The five SOLID principles: Single Responsibility, Open/Closed, Liskov Substitution, Interface Segregation, Dependency Inversion | [Design Principles → SOLID](principles.md#solid), [Methodologies → SOLID](methodologies.md#8-solid) |
| **Law of Demeter** | Talk only to immediate neighbors; avoid `a.getB().getC().do()` | [Design Principles → Other Principles](principles.md#other-principles-worth-knowing) |
| **Composition over Inheritance** | Prefer has-a over is-a to avoid fragile base classes | [Design Principles → Other Principles](principles.md#other-principles-worth-knowing) |
| **POLA** | Principle of Least Astonishment: behave the way a reasonable user expects | [Design Principles → Other Principles](principles.md#other-principles-worth-knowing) |
| **Coupling / Cohesion** | How much modules depend on each other (keep low) / how focused one module is (keep high) | [Design Principles](principles.md), [Wikipedia: Coupling ↗](https://en.wikipedia.org/wiki/Coupling_(computer_programming)), [Wikipedia: Cohesion ↗](https://en.wikipedia.org/wiki/Cohesion_(computer_science)) |
| **Encapsulation / Inheritance / Polymorphism / Abstraction** | The four pillars of OOP | [Fundamentals → Programming Paradigms](fundamentals.md#programming-paradigms), [Wikipedia: OOP ↗](https://en.wikipedia.org/wiki/Object-oriented_programming) |
| **Interface / Abstract Class** | A contract of methods / a partial base class that can't be instantiated | [Wikipedia: Interface ↗](https://en.wikipedia.org/wiki/Interface_(object-oriented_programming)) |
| **Imperative / Declarative** | Describe *how* step by step / describe *what* and let the runtime decide | [Fundamentals → Programming Paradigms](fundamentals.md#programming-paradigms) |
| **Pure Function / Side Effect / Immutability** | Same input → same output with nothing else changed / any change outside the function / data that never changes after creation | [Fundamentals → Programming Paradigms](fundamentals.md#programming-paradigms), [Wikipedia: Pure function ↗](https://en.wikipedia.org/wiki/Pure_function) |
| **Closure / Callback / Promise** | Function that captures its surrounding variables / function passed in to be called later / object representing a future result | [Wikipedia: Closure ↗](https://en.wikipedia.org/wiki/Closure_(computer_programming)), [Wikipedia: Promise ↗](https://en.wikipedia.org/wiki/Futures_and_promises) |
| **Recursion / Memoization** | Function that calls itself / caching results of expensive calls | [Algorithms → Algorithmic Patterns](algorithms.md#algorithmic-patterns), [Wikipedia: Memoization ↗](https://en.wikipedia.org/wiki/Memoization) |
| **Generics** | Code written once for many types (`List<T>`) | [Wikipedia: Generic programming ↗](https://en.wikipedia.org/wiki/Generic_programming) |
| **Static / Dynamic Typing / Type Hint** | Types checked at compile time / at runtime / optional annotations checked by tools (mypy, TypeScript) | [Frontend Toolchain → TypeScript 6](../tool_tip/frontend_tools.md#typescript-6-strict-by-default), [Wikipedia: Type system ↗](https://en.wikipedia.org/wiki/Type_system) |
| **Static Analysis** | Checking code without running it: linters, type checkers, security scanners (Semgrep, PMD) | [Claude Code → Verification as Backpressure](../../ai/tool_tip/claude_code.md#verification-as-backpressure), [Wikipedia: Static analysis ↗](https://en.wikipedia.org/wiki/Static_program_analysis) |
| **Compiler / Interpreter / Transpiler** | Translate to machine code ahead of time / execute source directly / translate to another source language (TS → JS) | [Wikipedia: Compiler ↗](https://en.wikipedia.org/wiki/Compiler), [Wikipedia: Transpiler ↗](https://en.wikipedia.org/wiki/Source-to-source_compiler) |
| **Runtime / VM / JVM** | Environment that runs the code / Virtual Machine / Java Virtual Machine | [Fundamentals → Code Unit Hierarchy](fundamentals.md#code-unit-hierarchy), [Wikipedia: JVM ↗](https://en.wikipedia.org/wiki/Java_virtual_machine) |
| **GC** | Garbage Collection: runtime frees memory no longer referenced | [Architecture → Performance Bottlenecks](architecture.md#performance-bottlenecks), [Wikipedia: GC ↗](https://en.wikipedia.org/wiki/Garbage_collection_(computer_science)) |
| **Code Unit Hierarchy** | Expression → statement → function → class → module → package → application → platform | [Fundamentals → Code Unit Hierarchy](fundamentals.md#code-unit-hierarchy) |
| **Regex / DSL / Parser** | Pattern for matching text / Domain-Specific Language / turns text into structure | [Fundamentals → Formal Languages](fundamentals.md#formal-languages-brief-note) |
| **Chomsky Hierarchy** | Classes of formal languages: regular, context-free, context-sensitive, unrestricted | [Fundamentals → Formal Languages](fundamentals.md#formal-languages-brief-note) |
| **Naming Conventions** | `snake_case`, `camelCase`, `PascalCase`, `kebab-case`, `UPPER_CASE` | [Styles → Code Conventions](styles.md#code-conventions), [Wikipedia: Naming convention ↗](https://en.wikipedia.org/wiki/Naming_convention_(programming)) |
| **Library / Framework / Package** | Code you call / code that calls you (inversion of control) / a distributable unit of code | [Fundamentals → Code Unit Hierarchy](fundamentals.md#code-unit-hierarchy), [Wikipedia: Software framework ↗](https://en.wikipedia.org/wiki/Software_framework) |
| **Package Manager / Lockfile** | Installs dependencies (pip, uv, npm, pnpm) / pins exact resolved versions | [Frontend Toolchain → Package Managers](../tool_tip/frontend_tools.md#package-managers-npmyarn-pnpm), [Software Tools → Python Workflow](../tool_tip/tools.md#a-small-python-workflow) |
| **Dependency / Transitive Dependency** | A package your code uses / a package your dependencies use | [Wikipedia: Dependency ↗](https://en.wikipedia.org/wiki/Coupling_(computer_programming)) |
| **Environment Variable / Config** | Value set outside the code (secrets, URLs) / settings that change per environment | [CI/CD → Environment Variables and Secrets](../tool_tip/cicd.md#8-environment-variables-and-secrets), [The Twelve-Factor App: Config ↗](https://12factor.net/config) |
| **Logging / Log Levels** | Recording events / DEBUG, INFO, WARN, ERROR, FATAL | [Error Handling → Best Practices](error_handling.md#best-practices), [Wikipedia: Logging ↗](https://en.wikipedia.org/wiki/Logging_(computing)) |
| **Debugger / Breakpoint / Stack Trace** | Tool to step through code / where execution pauses / the chain of calls at an error | [Error Handling → Raising and Chaining](error_handling.md#raising-and-chaining), [Wikipedia: Stack trace ↗](https://en.wikipedia.org/wiki/Stack_trace) |
| **Profiler / Flame Graph** | Measures where time and memory go / a visualization of sampled call stacks | [Architecture → Performance Bottlenecks](architecture.md#performance-bottlenecks) |
| **REPL** | Read-Eval-Print Loop: interactive shell for a language | [Wikipedia: REPL ↗](https://en.wikipedia.org/wiki/Read–eval–print_loop) |
| **CRUD** | Create, Read, Update, Delete: the four basic data operations | [APIs → Styles](apis.md#styles), [Wikipedia: CRUD ↗](https://en.wikipedia.org/wiki/Create,_read,_update_and_delete) |
| **N+1 Query** | One query for a list, then one more per item: a classic ORM performance bug | [Code Review → What Seniors Look For](code_review.md#8-what-seniors-look-for-in-a-pr-review) |
| **Serialization / Encoding** | Turn objects into bytes or text (JSON, Protobuf) / map characters to bytes (UTF-8) | [Wikipedia: Serialization ↗](https://en.wikipedia.org/wiki/Serialization) |
| **Anti-pattern** | A common "solution" that causes more problems than it solves | [Error Handling → Anti-Patterns](error_handling.md#anti-patterns), [Becoming Senior → Anti-Patterns](becoming_senior.md#anti-patterns) |
| **God Object / Spaghetti Code / Magic Number** | Class that does everything / tangled control flow / unexplained literal in code | [Wikipedia: God object ↗](https://en.wikipedia.org/wiki/God_object), [Wikipedia: Spaghetti code ↗](https://en.wikipedia.org/wiki/Spaghetti_code), [Wikipedia: Magic number ↗](https://en.wikipedia.org/wiki/Magic_number_(programming)) |
| **Boilerplate / Dead Code** | Repetitive setup code / code that never runs | [Wikipedia: Boilerplate code ↗](https://en.wikipedia.org/wiki/Boilerplate_code), [Wikipedia: Dead code ↗](https://en.wikipedia.org/wiki/Dead_code) |
| **Off-by-one / Null Pointer** | Loop or index wrong by one / dereferencing a missing value | [Wikipedia: Off-by-one error ↗](https://en.wikipedia.org/wiki/Off-by-one_error), [Wikipedia: Null pointer ↗](https://en.wikipedia.org/wiki/Null_pointer) |
| **Debounce / Throttle** | Run once after events stop / at most once per interval | [MDN: Debounce ↗](https://developer.mozilla.org/en-US/docs/Glossary/Debounce) |
| **Hot Reload** | Apply code changes to a running app without restarting it | [Vite: Features (HMR) ↗](https://vite.dev/guide/features) |
| **Code Generation / Scaffolding** | Producing boilerplate code from templates or specs | [Wikipedia: Scaffolding ↗](https://en.wikipedia.org/wiki/Scaffold_(programming)) |

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
| **Feature Branch / Release Branch / Hotfix Branch** | Short-lived branch per feature / stabilizing a version / urgent production fix | [Lifecycle → Branching Models](lifecycle.md#branching-models) |
| **Protected Branch** | Branch that only accepts changes through reviewed, passing PRs | [Git → Golden Rules](git.md#8-golden-rules) |
| **Detached HEAD** | Checked out a commit, not a branch; new commits belong to no branch | [Git → Local main is optional](git.md#local-main-is-optional-senior-devs-delete-it) |
| **Remote Tracking Branch** | Local read-only cache of a remote branch (`origin/main`) | [Git → origin/main is a local cache](git.md#originmain-is-a-local-cache-not-github-itself) |
| **Approve / Request Changes / LGTM** | Review outcomes; LGTM = "Looks Good To Me" | [GitHub Docs: PR reviews ↗](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/reviewing-changes-in-pull-requests/about-pull-request-reviews), [Google: Code review guide ↗](https://google.github.io/eng-practices/review/reviewer/) |
| **Nit** | Minor, non-blocking review comment (style, naming) | [Code Review → Claude Code Review](code_review.md#10-claude-code-review), [Google: Writing review comments ↗](https://google.github.io/eng-practices/review/reviewer/comments.html) |
| **CODEOWNERS** | File that assigns required reviewers per path | [GitHub Docs: CODEOWNERS ↗](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-code-owners) |
| **AI Code Review** | Automated PR review by an AI agent (Devin Review, Claude Code Review) | [Code Review → AI-Assisted Code Review](code_review.md#part-3-ai-assisted-code-review) |
| **Git Hooks / pre-commit** | Scripts Git runs on events / a hook that lints and tests before each commit | [Wikipedia: Git hooks ↗](https://en.wikipedia.org/wiki/Git#Hooks), [pre-commit.com ↗](https://pre-commit.com/) |
| **LFS** | Git Large File Storage for big binaries | [git-lfs.com ↗](https://git-lfs.com/) |

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
| **Mock / Stub** | Test doubles. A stub returns canned answers so the code under test can run; a mock also verifies it was called with the expected arguments | [Frontend Toolchain → Testing](../tool_tip/frontend_tools.md#testing-cypress-playwright-plus-vitest-and-msw), [Fowler: Mocks Aren't Stubs ↗](https://martinfowler.com/articles/mocksArentStubs.html) |
| **Fixture** | Fixed setup state or data a test runs against | [Wikipedia: Test fixture ↗](https://en.wikipedia.org/wiki/Test_fixture) |
| **Flaky Test** | Passes and fails on the same code; usually caused by timing, ordering, or shared state | [Fowler: Non-Determinism ↗](https://martinfowler.com/articles/nonDeterminism.html) |
| **Code Coverage** | Share of code executed by tests | [Wikipedia: Code coverage ↗](https://en.wikipedia.org/wiki/Code_coverage) |
| **QC** | Quality Control: inspect the product for defects (QA improves the process) | [Wikipedia: Quality control ↗](https://en.wikipedia.org/wiki/Quality_control) |
| **Happy Path / Negative Test** | Normal successful flow / invalid input that must be rejected gracefully | [Wikipedia: Happy path ↗](https://en.wikipedia.org/wiki/Happy_path) |
| **Boundary Value / Equivalence Partitioning** | Test at the edges of input ranges / one test per class of equivalent inputs | [Wikipedia: Boundary-value analysis ↗](https://en.wikipedia.org/wiki/Boundary-value_analysis), [Wikipedia: Equivalence partitioning ↗](https://en.wikipedia.org/wiki/Equivalence_partitioning) |
| **AAA / Given-When-Then** | Arrange-Act-Assert test structure / BDD form of the same idea | [Methodologies → BDD](methodologies.md#bdd-behavior-driven-development) |
| **Test Double / Fake / Spy** | Any stand-in for a real dependency / a working lightweight version / a double that records calls | [Fowler: Test Double ↗](https://martinfowler.com/bliki/TestDouble.html) |
| **Visual Regression Test** | Compare screenshots to catch unintended UI changes | [Playwright: Visual comparisons ↗](https://playwright.dev/docs/test-snapshots) |
| **Benchmark** | Repeatable measurement of performance for comparison | [Wikipedia: Benchmark ↗](https://en.wikipedia.org/wiki/Benchmark_(computing)) |
| **Manual / Automated Testing** | Human-executed / script-executed tests | [Wikipedia: Test automation ↗](https://en.wikipedia.org/wiki/Test_automation) |
| **Monkey Test** | Random input to see if anything crashes | [Wikipedia: Monkey testing ↗](https://en.wikipedia.org/wiki/Monkey_testing) |
| **Defect Lifecycle** | New → Assigned → Fixed → Retest → Closed (or Reopened) | [Wikipedia: Bug tracking system ↗](https://en.wikipedia.org/wiki/Bug_tracking_system) |
| **Test Environment / Test Data** | Where tests run (dev, staging) / the data they use, often masked production data | [Lifecycle → Environments](lifecycle.md#environments), [Data Security → De-identification](../../data/basics/data_security.md#what-it-is) |
| **Golden Master / Characterization Test** | Lock down existing behavior of legacy code before refactoring it | [Wikipedia: Characterization test ↗](https://en.wikipedia.org/wiki/Characterization_test) |
| **Verification / Validation** | Did we build it right? / did we build the right thing? | [Wikipedia: V&V ↗](https://en.wikipedia.org/wiki/Software_verification_and_validation) |
| **UT / IT / ST** | Short forms for Unit Test / Integration Test / System Test, common in test plans | [Lifecycle → Testing](lifecycle.md#testing) |

## System Design

| Term | Meaning | Read more |
|---|---|---|
| **Latency** | Time for one request to complete, usually reported as percentiles (p50/p95/p99) | [DevOps & SRE → p95/p99](#devops-sre), [Running a Server → Network](../tool_tip/server_operations.md#network), [System Design Notes → Retry and Resilience](system_design.md#going-deeper_6) |
| **Throughput** | Work completed per unit of time (requests/s, MB/s); can rise while latency worsens | [Running a Server → Network](../tool_tip/server_operations.md#network), [Running a Server → Matching the workload](../tool_tip/server_operations.md#matching-the-workload) |
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
| **CAP** | Consistency, Availability, Partition tolerance: partitions are unavoidable, so during one a distributed system must choose consistency (CP: refuse some requests) or availability (AP: answer with possibly stale data) | [Architecture → CAP Theorem](architecture.md#cap-theorem) |
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
| **Timeout / Deadline** | Give up on a slow call / a total time budget passed down the call chain | [System Design Notes → Retry and Resilience](system_design.md#going-deeper_6) |
| **Fallback** | Return something useful (cached data, a default) when a call fails | [System Design Notes → Retry and Resilience](system_design.md#going-deeper_6) |
| **Bulkhead** | Separate pools per dependency so one slow service can't starve the others | [System Design Notes → Retry and Resilience](system_design.md#going-deeper_6) |
| **Retry Storm / Thundering Herd** | Layered retries multiplying load / many clients hitting a resource at the same moment | [System Design Notes → Retry and Resilience](system_design.md#going-deeper_6), [Wikipedia: Thundering herd problem ↗](https://en.wikipedia.org/wiki/Thundering_herd_problem) |
| **Load Shedding** | Deliberately reject some requests to protect the rest under overload | [AWS Builders' Library ↗](https://aws.amazon.com/builders-library/using-load-shedding-to-avoid-overload/) |
| **Sticky Session** | Load balancer sends a client to the same instance every time | [Architecture → Scalability](architecture.md#scalability) |
| **L4 / L7 Load Balancing** | Route by IP and port (TCP/UDP) / by HTTP content (path, headers) | [Architecture → Load Balancers](architecture.md#load-balancers) |
| **Round Robin / Least Connections** | Load-balancing algorithms: rotate in turn / pick the least busy | [Architecture → Load Balancers](architecture.md#load-balancers) |
| **Token Bucket / Leaky Bucket / Sliding Window** | Rate-limiting algorithms | [Architecture → Rate Limiting](architecture.md#rate-limiting) |
| **Cache Stampede / Cache Invalidation** | Many misses rebuilding the same entry at once / keeping cached data in sync with the source | [Architecture → Caching](architecture.md#caching), [Wikipedia: Cache stampede ↗](https://en.wikipedia.org/wiki/Cache_stampede) |
| **Read-Through / Write-Around** | Cache loads from DB itself on miss / writes skip the cache | [Architecture → Caching](architecture.md#caching) |
| **DLQ** | Dead Letter Queue: where messages go after repeated processing failures | [Wikipedia: Dead letter queue ↗](https://en.wikipedia.org/wiki/Dead_letter_queue) |
| **At-most-once / At-least-once / Exactly-once** | Message delivery guarantees: may be lost, never duplicated / never lost, may be duplicated (consumers must be idempotent) / processed once with no loss or duplicates (costly, needs coordination) | [APIs → Idempotency](apis.md#idempotency), [Confluent: Delivery semantics ↗](https://docs.confluent.io/kafka/design/delivery-semantics.html) |
| **Idempotency Key** | Client-supplied ID that lets the server de-duplicate retried requests | [APIs → Idempotency](apis.md#idempotency) |
| **Fan-out / Fan-in** | One event to many consumers / many results combined into one | [Wikipedia: Fan-out ↗](https://en.wikipedia.org/wiki/Fan-out_(software)) |
| **Polling / Long Polling / Push** | Client asks repeatedly / server holds the request until data exists / server sends when ready | [System Design Notes → API Protocols](system_design.md#3-seven-api-protocols) |
| **Distributed Lock** | Mutual exclusion across machines (Redis, ZooKeeper, etcd) | [Wikipedia: Distributed lock manager ↗](https://en.wikipedia.org/wiki/Distributed_lock_manager) |
| **Consensus (Raft / Paxos)** | Algorithms for nodes to agree on one value despite failures | [Wikipedia: Raft ↗](https://en.wikipedia.org/wiki/Raft_(algorithm)), [Wikipedia: Paxos ↗](https://en.wikipedia.org/wiki/Paxos_(computer_science)) |
| **Gossip Protocol / Heartbeat** | Peers spread state by random exchange / periodic "I'm alive" signal | [Wikipedia: Gossip protocol ↗](https://en.wikipedia.org/wiki/Gossip_protocol), [Wikipedia: Heartbeat ↗](https://en.wikipedia.org/wiki/Heartbeat_(computing)) |
| **Clock Skew / NTP / Logical Clock** | Machines disagree on time / Network Time Protocol / ordering events without wall clocks (Lamport, vector clocks) | [Wikipedia: Clock skew ↗](https://en.wikipedia.org/wiki/Clock_skew), [Wikipedia: Lamport timestamp ↗](https://en.wikipedia.org/wiki/Lamport_timestamp) |
| **Bloom Filter** | Probabilistic set: "definitely not" or "maybe" in it, using tiny memory | [Wikipedia: Bloom filter ↗](https://en.wikipedia.org/wiki/Bloom_filter) |
| **Snowflake ID / ULID** | Time-ordered unique IDs generated without a central counter | [Wikipedia: Snowflake ID ↗](https://en.wikipedia.org/wiki/Snowflake_ID) |
| **Object Storage / Blob** | Flat store of files by key (S3, GCS) / a binary large object | [Data Engineering → Where Data Lands](../../data/basics/data_engineering.md#where-data-lands), [Wikipedia: Object storage ↗](https://en.wikipedia.org/wiki/Object_storage) |
| **Region / AZ / Multi-region** | Geographic cloud location / isolated data center within it / running across several regions | [Wikipedia: Availability zone ↗](https://en.wikipedia.org/wiki/Availability_zone) |
| **N-tier / Layered Architecture** | Presentation → business → data layers, each calling only the next | [Architecture → Application Layers](architecture.md#1-application-layers) |
| **Hexagonal / Clean Architecture** | Business logic at the center; databases, UIs, and APIs plug in through ports and adapters, so dependencies point inward | [Wikipedia: Hexagonal architecture ↗](https://en.wikipedia.org/wiki/Hexagonal_architecture_(software)), [Uncle Bob: Clean Architecture ↗](https://blog.cleancoder.com/uncle-bob/2012/08/13/the-clean-architecture.html) |
| **Deployment Topology** | How components map to machines: all-in-one, split DB, microservices, serverless | [Architecture → Deployment Topologies](architecture.md#4-deployment-topologies) |
| **Edge Computing** | Run logic close to users (CDN workers) to cut latency | [Wikipedia: Edge computing ↗](https://en.wikipedia.org/wiki/Edge_computing) |
| **Data Locality** | Move compute to where data lives instead of shipping data | [Big Data → Distributed Processing](../../data/basics/big_data.md#distributed-processing) |
| **Golden Signals / RED** | Latency, traffic, errors, saturation / Rate, Errors, Duration for services | [Google SRE: Monitoring ↗](https://sre.google/sre-book/monitoring-distributed-systems/) |

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
| **Cold Start** | Extra latency when a serverless function or new instance starts from zero | [Architecture → Serverless / FaaS](architecture.md#serverless-faas), [Wikipedia: Cold start ↗](https://en.wikipedia.org/wiki/Cold_start_(computing)) |
| **ORM / DTO / DAO** | Object–Relational Mapping (work with DB rows as objects) / Data Transfer Object / Data Access Object | [Architecture → DTO, DAO, ORM](architecture.md#talking-to-the-data-layer-dto-dao-orm) |
| **Monolith / Microservices / SOA** | One deployable unit / many small independent services / Service-Oriented Architecture | [Architecture → System-Level Patterns](architecture.md#3-system-level-patterns) |
| **Event-Driven** | Components react to published events instead of calling each other | [Architecture → Event-Driven](architecture.md#event-driven) |
| **UUID** | Universally Unique Identifier (128-bit) | [Wikipedia: UUID ↗](https://en.wikipedia.org/wiki/Universally_unique_identifier) |
| **UTC** | Coordinated Universal Time: store timestamps in it | [Wikipedia: UTC ↗](https://en.wikipedia.org/wiki/Coordinated_Universal_Time) |
| **Middleware** | Code in the request pipeline that runs before or after handlers (auth, logging, CORS) | [Wikipedia: Middleware ↗](https://en.wikipedia.org/wiki/Middleware) |
| **Connection Pool** | Reused set of open DB or HTTP connections | [Architecture → Performance Bottlenecks](architecture.md#performance-bottlenecks), [Wikipedia: Connection pool ↗](https://en.wikipedia.org/wiki/Connection_pool) |
| **Background Job / Worker / Queue Worker** | Work done outside the request (emails, reports) by processes reading a queue | [Wikipedia: Job queue ↗](https://en.wikipedia.org/wiki/Job_queue) |
| **Cron / Scheduler** | Run jobs on a time schedule | [Wikipedia: Cron ↗](https://en.wikipedia.org/wiki/Cron) |
| **Daemon / Service** | Long-running background process (systemd unit) | [Linux Commands → Services and Logs](../tool_tip/linux_commands.md#services-and-logs), [Wikipedia: Daemon ↗](https://en.wikipedia.org/wiki/Daemon_(computing)) |
| **Health Check / Readiness / Liveness** | Endpoint that reports service health / ready for traffic / still alive (restart if not) | [Kubernetes: Probes ↗](https://kubernetes.io/docs/tasks/configure-pod-container/configure-liveness-readiness-startup-probes/) |
| **Graceful Shutdown** | Finish in-flight requests before exiting | [Wikipedia: Graceful exit ↗](https://en.wikipedia.org/wiki/Graceful_exit) |
| **Correlation ID / Trace ID** | ID attached to a request so logs and spans across services can be joined | [Becoming Senior → Observability](becoming_senior.md#observability-is-a-property-of-the-pipeline) |
| **Structured Logging** | Logs as key–value JSON instead of free text | [Twelve-Factor: Logs ↗](https://12factor.net/logs) |
| **Twelve-Factor App** | Methodology for cloud-native services: config in env, stateless processes, logs as streams | [12factor.net ↗](https://12factor.net/) |
| **Headers / Body / Payload** | Request metadata / the content / the useful data being carried | [MDN: HTTP ↗](https://developer.mozilla.org/en-US/docs/Web/HTTP) |
| **MIME Type / Content-Type** | Label for the data format (`application/json`) | [MDN: MIME types ↗](https://developer.mozilla.org/en-US/docs/Web/HTTP/Guides/MIME_types) |
| **Protobuf** | Protocol Buffers: compact binary schema format used by gRPC | [protobuf.dev ↗](https://protobuf.dev/), [System Design Notes → Types of APIs](system_design.md#going-deeper_1) |
| **API Key** | Static secret identifying the calling app, not the user | [System Design Notes → Auth Methods](system_design.md#what-the-post-says_3) |
| **B2B / B2C / Partner API** | APIs for businesses / consumers / selected external partners | [System Design Notes → Types of APIs](system_design.md#2-types-of-apis) |
| **Throttling** | Slowing or rejecting a client that exceeds its quota (often returns 429) | [APIs → Status Codes](apis.md#status-codes), [System Design Notes → Retry and Resilience](system_design.md#going-deeper_6) |
| **LAMP / MEAN / MERN / JAMstack** | Classic stack combinations (Linux-Apache-MySQL-PHP, Mongo-Express-Angular/React-Node, JS-APIs-Markup) | [Tech Stacks → Classic Combinations](tech_stacks.md#classic-stack-combinations) |
| **Tech Stack** | The set of languages, frameworks, and services a product is built on | [Tech Stacks → The Layered View](tech_stacks.md#the-layered-view) |

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
| **SPA / MPA / SSR / PWA** | SPA: one page loaded once; JavaScript swaps views (client-side routing). MPA: the server returns a new page on each navigation. SSR: the server renders HTML per request for a fast first paint and SEO. PWA: a web app that can be installed and works offline via a service worker | [Frontend Toolchain](../tool_tip/frontend_tools.md), [MDN: SPA ↗](https://developer.mozilla.org/en-US/docs/Glossary/SPA) |
| **MVC / MVP / MVVM** | Patterns that separate UI from logic. MVC: a Controller handles input and updates the Model and View. MVP: a Presenter drives a passive View. MVVM: the View binds to state exposed by a ViewModel | [Architecture → UI Patterns](architecture.md#6-ui-architecture-patterns) |
| **Server State / Client State** | Data owned by the backend and cached / data that lives only in the UI | [Frontend Toolchain → Server vs Client State](../tool_tip/frontend_tools.md#server-state-vs-client-state-redux-query-zustand) |
| **Bundler** | Combines modules and assets into files the browser loads | [Frontend Toolchain → Bundlers](../tool_tip/frontend_tools.md#bundlers-webpack-vite-8) |
| **CORS** | Cross-Origin Resource Sharing: browser rules for cross-origin requests | [MDN: CORS ↗](https://developer.mozilla.org/en-US/docs/Web/HTTP/Guides/CORS) |
| **Component / Props / State** | Reusable UI unit / inputs passed in / data it owns that triggers re-render | [React: Thinking in React ↗](https://react.dev/learn/thinking-in-react) |
| **Virtual DOM / Reconciliation** | In-memory UI tree diffed against the real DOM to apply minimal updates | [React: Preserving and Resetting State ↗](https://react.dev/learn/preserving-and-resetting-state) |
| **CSR / SSG / ISR / Hydration** | Client-Side Rendering / Static Site Generation / Incremental Static Regeneration / attaching JS to server-rendered HTML | [Frontend Toolchain → The 16 kept](../tool_tip/frontend_tools.md#the-16-kept), [MDN: SSR ↗](https://developer.mozilla.org/en-US/docs/Glossary/SSR) |
| **State Management** | How app state is stored and shared (React Query, Zustand, Redux) | [Frontend Toolchain → Server vs Client State](../tool_tip/frontend_tools.md#server-state-vs-client-state-redux-query-zustand) |
| **Responsive Design / Mobile-first / Breakpoint** | Layout adapts to screen size / design for small screens first / width where layout changes | [MDN: Responsive design ↗](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/CSS_layout/Responsive_Design) |
| **Design System** | Shared components, tokens, and rules for a consistent UI (shadcn/ui, Material) | [Frontend Toolchain → Styling](../tool_tip/frontend_tools.md#styling-styled-components-tailwind-shadcnui) |
| **Utility-first CSS** | Compose styles from small single-purpose classes (Tailwind) | [Frontend Toolchain → Styling](../tool_tip/frontend_tools.md#styling-styled-components-tailwind-shadcnui) |
| **Tree Shaking / Code Splitting / Lazy Loading** | Drop unused code / split bundles / load code or images only when needed | [MDN: Tree shaking ↗](https://developer.mozilla.org/en-US/docs/Glossary/Tree_shaking) |
| **Minification / Polyfill** | Shrink code for delivery / code that adds a missing browser feature | [MDN: Polyfill ↗](https://developer.mozilla.org/en-US/docs/Glossary/Polyfill) |
| **Core Web Vitals (LCP / INP / CLS)** | Google's UX metrics: Largest Contentful Paint, Interaction to Next Paint, Cumulative Layout Shift | [web.dev: Web Vitals ↗](https://web.dev/articles/vitals) |
| **TTFB / FCP** | Time To First Byte / First Contentful Paint | [web.dev: TTFB ↗](https://web.dev/articles/ttfb) |
| **SEO** | Search Engine Optimization | [Wikipedia: Search engine optimization ↗](https://en.wikipedia.org/wiki/Search_engine_optimization) |
| **Web Components / Shadow DOM** | Native reusable custom elements / their encapsulated DOM and styles | [MDN: Web Components ↗](https://developer.mozilla.org/en-US/docs/Web/API/Web_components) |
| **Service Worker** | Background script that intercepts network requests (offline, PWA, MSW mocks) | [Frontend Toolchain → Testing](../tool_tip/frontend_tools.md#testing-cypress-playwright-plus-vitest-and-msw), [MDN: Service Worker API ↗](https://developer.mozilla.org/en-US/docs/Web/API/Service_Worker_API) |
| **LocalStorage / SessionStorage** | Browser key-value storage that persists / lasts for one tab session | [MDN: Web Storage ↗](https://developer.mozilla.org/en-US/docs/Web/API/Web_Storage_API) |
| **Event Bubbling / Delegation** | Events propagate up the DOM / one parent listener handles many children | [MDN: Event bubbling ↗](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Scripting/Event_bubbling) |
| **i18n / l10n** | Internationalization (make it translatable) / Localization (translate and adapt) | [Wikipedia: i18n and l10n ↗](https://en.wikipedia.org/wiki/Internationalization_and_localization) |
| **Schema Validation** | Check untrusted data against a schema at the boundary (Zod, Pydantic) | [Frontend Toolchain → Zod](../tool_tip/frontend_tools.md#zod-validate-at-trust-boundaries) |
| **Browser Automation** | Driving a real browser from code for tests or agents (Playwright) | [Frontend Toolchain → Testing](../tool_tip/frontend_tools.md#testing-cypress-playwright-plus-vitest-and-msw) |

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
| **IPv4 / IPv6** | 32-bit addresses (`192.168.1.10`) / 128-bit addresses | [Wikipedia: IPv6 ↗](https://en.wikipedia.org/wiki/IPv6) |
| **CIDR / Subnet** | Address-range notation (`10.0.0.0/16`) / a slice of a network | [Wikipedia: CIDR ↗](https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing) |
| **LAN / WAN** | Local Area Network / Wide Area Network | [Wikipedia: LAN ↗](https://en.wikipedia.org/wiki/Local_area_network) |
| **Router / Switch / Gateway** | Forwards between networks / within one network / the exit point to another network | [Wikipedia: Router ↗](https://en.wikipedia.org/wiki/Router_(computing)) |
| **VPC** | Virtual Private Cloud: your isolated network inside a cloud | [Wikipedia: Virtual private cloud ↗](https://en.wikipedia.org/wiki/Virtual_private_cloud) |
| **VPN** | Virtual Private Network: encrypted tunnel into a private network | [Wikipedia: VPN ↗](https://en.wikipedia.org/wiki/Virtual_private_network) |
| **Proxy (Forward)** | Server that makes requests on a client's behalf (vs a reverse proxy, which fronts servers) | [Wikipedia: Proxy server ↗](https://en.wikipedia.org/wiki/Proxy_server) |
| **ICMP / ping** | Internet Control Message Protocol / the tool that uses it to test reachability | [Networking → TCP/IP Model](networking.md#the-tcpip-model), [Linux Commands → Networking](../tool_tip/linux_commands.md#networking) |
| **DHCP / ARP / MAC Address** | Hands out IP addresses / maps IP to hardware address / a NIC's hardware address | [Wikipedia: DHCP ↗](https://en.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol), [Wikipedia: ARP ↗](https://en.wikipedia.org/wiki/Address_Resolution_Protocol) |
| **TLD / Domain / Subdomain** | Top-Level Domain (`.com`) / `example.com` / `api.example.com` | [Networking → Opening a URL](networking.md#what-happens-when-you-open-a-url) |
| **DNS Records (A / AAAA / CNAME / MX / TXT)** | IPv4 address / IPv6 address / alias / mail server / arbitrary text (verification, SPF) | [Wikipedia: DNS record types ↗](https://en.wikipedia.org/wiki/List_of_DNS_record_types) |
| **Resolver / Authoritative Server** | DNS server that looks names up for you / the one that holds the real answer | [Networking → Opening a URL](networking.md#what-happens-when-you-open-a-url) |
| **Handshake (TCP / TLS)** | SYN, SYN-ACK, ACK to open a connection / certificate and key exchange for encryption | [Networking → Opening a URL](networking.md#what-happens-when-you-open-a-url) |
| **RTT / Packet Loss / Jitter** | Round-Trip Time / dropped packets / variation in latency | [Wikipedia: RTT ↗](https://en.wikipedia.org/wiki/Round-trip_delay) |
| **MTU** | Maximum Transmission Unit: the largest packet a link carries (usually 1500 bytes) | [Wikipedia: Maximum transmission unit ↗](https://en.wikipedia.org/wiki/Maximum_transmission_unit) |
| **HTTP/2 / HTTP/3 / QUIC** | Multiplexed binary HTTP / HTTP over QUIC, a UDP-based transport | [APIs → Styles](apis.md#styles), [Wikipedia: HTTP/3 ↗](https://en.wikipedia.org/wiki/HTTP/3) |
| **Keep-Alive** | Reuse one TCP connection for many HTTP requests | [Wikipedia: HTTP persistent connection ↗](https://en.wikipedia.org/wiki/HTTP_persistent_connection) |
| **localhost / 127.0.0.1 / 0.0.0.0** | This machine / its loopback address / "listen on all interfaces" | [Wikipedia: Localhost ↗](https://en.wikipedia.org/wiki/Localhost), [Running a Server → The Exposure Chain](../tool_tip/server_operations.md#the-exposure-chain) |
| **Ingress / Egress** | Traffic coming in / going out | [CI/CD → How the Platform Reaches Your Code](../tool_tip/cicd.md#2-how-the-platform-reaches-your-code) |
| **Anycast** | One IP announced from many locations; routes to the nearest (used by CDNs, DNS) | [Wikipedia: Anycast ↗](https://en.wikipedia.org/wiki/Anycast) |

## DevOps & SRE

| Term | Meaning | Read more |
|---|---|---|
| **CI/CD** | Continuous Integration / Continuous Delivery or Deployment | [Lifecycle → CI/CD](lifecycle.md#cicd), [CI/CD Platforms](../tool_tip/cicd.md#0-cicd-is-three-things) |
| **Pipeline** | Automated stages from commit to deploy: lint → test → build → deploy | [Lifecycle → CI/CD](lifecycle.md#cicd), [CI/CD Platforms](../tool_tip/cicd.md) |
| **SRE** | Site Reliability Engineering: operations run as a software problem | [Lifecycle → Roles](lifecycle.md#roles), [Google SRE Book ↗](https://sre.google/sre-book/table-of-contents/) |
| **Environments** | Local → Dev → Staging → Production | [Lifecycle → Environments](lifecycle.md#environments) |
| **Hotfix** | Urgent fix shipped straight to production | [Lifecycle → SDLC Phases](lifecycle.md#sdlc-phases), [Lifecycle → Branching Models](lifecycle.md#branching-models) |
| **Release Notes** | User-facing summary of what changed in a release | [Lifecycle → SDLC Phases](lifecycle.md#sdlc-phases) |
| **Blue-Green / Canary / Rolling / Shadow / A/B** | Deployment strategies. Blue-green: two full environments, switch traffic at once. Canary: send a small share of users to the new version first. Rolling: replace instances one by one. Shadow: copy live traffic to the new version and discard its responses. A/B: split users to compare variants on a product metric | [System Design Notes → Deployment Strategies](system_design.md#6-six-deployment-strategies) |
| **Feature Flag** | Toggle that separates *deploy* from *release* | [System Design Notes → Deployment Strategies](system_design.md#going-deeper_5) |
| **Rollback** | Return to the previous known-good version | [System Design Notes → Deployment Strategies](system_design.md#going-deeper_5), [Becoming Senior → Deployment](becoming_senior.md#deployment-and-scale-are-part-of-the-design) |
| **IaC** | Infrastructure as Code: servers and networks defined in versioned files | [Wikipedia: IaC ↗](https://en.wikipedia.org/wiki/Infrastructure_as_code) |
| **Container / K8s** | Packaged app plus its dependencies / Kubernetes, the container orchestrator | [Running a Server → Containers](../tool_tip/server_operations.md#8-containers-and-orchestration), [Architecture → Container Orchestration](architecture.md#container-orchestration) |
| **Docker** | The standard tool for building and running containers | [Running a Server → Docker Eats the Disk](../tool_tip/server_operations.md#docker-eats-the-disk), [Linux Commands → Docker](../tool_tip/linux_commands.md#docker-essentials) |
| **Dockerfile / Docker Compose** | Recipe for building an image / YAML file that runs several containers together for local development | [Docker Docs: Dockerfile ↗](https://docs.docker.com/reference/dockerfile/), [Docker Docs: Compose ↗](https://docs.docker.com/compose/) |
| **OOM / Memory Leak** | Out Of Memory: the system runs out of RAM, and Linux's OOM killer terminates a process to recover / memory a program keeps allocating and never frees | [Running a Server → Out of Memory](../tool_tip/server_operations.md#out-of-memory), [Running a Server → Memory](../tool_tip/server_operations.md#memory) |
| **Inode** | Filesystem entry per file; a disk can run out of inodes before bytes | [Running a Server → Out of Inodes](../tool_tip/server_operations.md#cause-2-out-of-inodes) |
| **Metrics / Logs / Traces** | The three observability signals (Prometheus, Loki, Jaeger; Grafana to view) | [Running a Server → The Pipeline](../tool_tip/server_operations.md#the-pipeline) |
| **OpenTelemetry (OTel)** | Vendor-neutral standard and SDKs for emitting metrics, logs, and traces | [Running a Server → Tool Status](../tool_tip/server_operations.md#tool-status), [opentelemetry.io ↗](https://opentelemetry.io/docs/what-is-opentelemetry/) |
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
| **Build / Artifact** | Turn source into a deployable output / that output (binary, image, package) | [Lifecycle → CI/CD](lifecycle.md#cicd), [CI/CD → How the Deploy Happens](../tool_tip/cicd.md#10-how-the-deploy-actually-happens) |
| **Runner / Agent** | Machine that executes CI jobs | [CI/CD → How the Platform Reaches Your Code](../tool_tip/cicd.md#2-how-the-platform-reaches-your-code) |
| **GitHub Actions / GitLab CI / Jenkins / Azure Pipelines** | Common CI/CD platforms | [CI/CD Platforms](../tool_tip/cicd.md) |
| **Image / Registry** | Immutable container template / store for images (Docker Hub, GHCR, ECR) | [Running a Server → Containers](../tool_tip/server_operations.md#8-containers-and-orchestration) |
| **Pod / Node / Cluster / Namespace** | K8s: smallest deployable unit / a worker machine / the whole set / a logical partition | [Linux Commands → Kubernetes](../tool_tip/linux_commands.md#kubernetes-essentials), [Kubernetes: Concepts ↗](https://kubernetes.io/docs/concepts/) |
| **Requests / Limits** | Resources a K8s container is guaranteed / its hard cap | [Running a Server → Kubernetes](../tool_tip/server_operations.md#kubernetes-needs-requests-and-limits) |
| **Helm / Terraform / Ansible** | K8s package manager / declarative infrastructure provisioning / configuration management | [Wikipedia: Terraform ↗](https://en.wikipedia.org/wiki/Terraform_(software)), [Wikipedia: Ansible ↗](https://en.wikipedia.org/wiki/Ansible_(software)) |
| **GitOps** | Git is the source of truth; an agent (Argo CD, Flux) syncs the cluster to it | [opengitops.dev ↗](https://opengitops.dev/) |
| **Immutable Infrastructure / Pets vs Cattle** | Replace servers instead of patching them / treat servers as disposable | [Fowler: Immutable Server ↗](https://martinfowler.com/bliki/ImmutableServer.html) |
| **Configuration Drift** | Live systems slowly diverging from their declared config | [Wikipedia: Configuration management ↗](https://en.wikipedia.org/wiki/Configuration_management) |
| **VM / Hypervisor** | Virtual Machine / software that runs VMs | [Wikipedia: Hypervisor ↗](https://en.wikipedia.org/wiki/Hypervisor) |
| **VPS / Bare Metal** | Rented virtual server / a whole physical machine | [Running a Server → The Stack](../tool_tip/server_operations.md#1-the-stack-and-where-your-responsibility-starts) |
| **CPU / RAM / Disk / GPU / VRAM** | The resources you size; VRAM is GPU memory, the limit for LLM inference | [Running a Server → Sizing the Machine](../tool_tip/server_operations.md#2-sizing-the-machine), [Running a Server → GPU](../tool_tip/server_operations.md#gpu) |
| **IOPS** | Input/Output Operations Per Second: disk speed for random access | [Running a Server → Disk](../tool_tip/server_operations.md#disk) |
| **Load Average** | Average runnable processes; compare with the core count | [Running a Server → CPU Saturation](../tool_tip/server_operations.md#cpu-saturation) |
| **Swap / Page Cache / RSS** | Disk used as slow RAM / idle RAM caching files / memory a process actually holds | [Running a Server → Reading free -h](../tool_tip/server_operations.md#reading-free-h-correctly), [Running a Server → When Memory Runs Out](../tool_tip/server_operations.md#when-memory-runs-out) |
| **PID / Signal (SIGTERM / SIGKILL)** | Process ID / polite stop request / forced kill | [Linux Commands → Processes](../tool_tip/linux_commands.md#processes) |
| **systemd / journald** | Linux service manager / its log store | [Linux Commands → Services and Logs](../tool_tip/linux_commands.md#services-and-logs) |
| **Alert / Alert Fatigue** | Notification on a symptom / too many alerts so people ignore them | [Wikipedia: Alarm fatigue ↗](https://en.wikipedia.org/wiki/Alarm_fatigue), [Running a Server → The Pipeline](../tool_tip/server_operations.md#the-pipeline) |
| **APM** | Application Performance Monitoring | [Wikipedia: APM ↗](https://en.wikipedia.org/wiki/Application_performance_management) |
| **Prometheus / Grafana / Loki** | Metrics database / dashboards / log store | [Running a Server → The Pipeline](../tool_tip/server_operations.md#the-pipeline) |
| **Retention** | How long metrics, logs, or backups are kept | [Running a Server → Monitoring Stack Disk](../tool_tip/server_operations.md#your-monitoring-stack-will-try-to-fill-your-disk) |
| **Backup / Restore Test** | Copy of data / proving you can actually restore it | [Running a Server → Operational Baseline](../tool_tip/server_operations.md#10-operational-baseline) |
| **Toil** | Manual, repetitive operational work that scales with load | [Google SRE: Eliminating Toil ↗](https://sre.google/sre-book/eliminating-toil/) |
| **Blameless Culture** | Postmortems focus on systems, not on whom to blame | [Google SRE: Postmortem Culture ↗](https://sre.google/sre-book/postmortem-culture/) |
| **Dark Launch / Roll Forward** | Ship code hidden behind a flag / fix by deploying a new version instead of reverting | [System Design Notes → Deployment Strategies](system_design.md#going-deeper_5), [Fowler: Dark Launching ↗](https://martinfowler.com/bliki/DarkLaunching.html) |
| **Recreate Deployment** | Stop the old version, then start the new one (has downtime) | [System Design Notes → Deployment Strategies](system_design.md#what-the-post-says_5) |
| **CAB / ITIL** | Change Advisory Board that approves risky changes / IT service management framework | [Wikipedia: CAB ↗](https://en.wikipedia.org/wiki/Change-advisory_board), [Wikipedia: ITIL ↗](https://en.wikipedia.org/wiki/ITIL) |
| **Status Page** | Public page showing service health during incidents | [Google SRE: Managing Incidents ↗](https://sre.google/sre-book/managing-incidents/) |
| **FinOps** | Managing cloud cost as an engineering concern | [Becoming Senior → Deployment and Scale](becoming_senior.md#deployment-and-scale-are-part-of-the-design), [finops.org ↗](https://www.finops.org/introduction/what-is-finops/) |
| **Secret Manager / Vault / KMS** | Store and rotate secrets / HashiCorp's secret store / Key Management Service | [CI/CD → Environment Variables and Secrets](../tool_tip/cicd.md#8-environment-variables-and-secrets) |
| **First Sixty Seconds** | Quick triage checklist on a slow server: uptime, dmesg, vmstat, free, df | [Running a Server → First Sixty Seconds](../tool_tip/server_operations.md#4-the-first-sixty-seconds) |

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
| **IAM** | Identity and Access Management: users, roles, and policies that control who can do what in a system or cloud account | [Wikipedia: IAM ↗](https://en.wikipedia.org/wiki/Identity_and_access_management) |
| **Least Privilege** | Grant the minimum access needed | [Data Security → What It Is](../../data/basics/data_security.md#what-it-is) |
| **Hashing / Salt** | One-way fingerprint of data / random value added so equal passwords hash differently (bcrypt, argon2) | [Security → Crypto Basics](security.md#crypto-basics) |
| **Symmetric / Asymmetric Encryption** | One shared key (AES) / public–private key pair (RSA, ECC) | [Security → Crypto Basics](security.md#crypto-basics) |
| **Digital Signature / HMAC** | Signature: sign with a private key, anyone verifies with the public key, so it proves who sent the data and that it wasn't changed. HMAC: a hash keyed with a shared secret; it proves integrity, but any key holder could have produced it | [Security → Crypto Basics](security.md#crypto-basics) |
| **Certificate / CA / PKI** | Signed binding of a public key to a name / the authority that signs it / the whole trust system | [System Design Notes → Auth Methods](system_design.md#going-deeper_3), [Wikipedia: PKI ↗](https://en.wikipedia.org/wiki/Public_key_infrastructure) |
| **Encryption at Rest / in Transit** | Protect stored data / data moving over the network (TLS) | [Security → Crypto Basics](security.md#crypto-basics), [Data Security → What It Is](../../data/basics/data_security.md#what-it-is) |
| **Session / Cookie** | Session: login state kept on the server. Cookie: small name–value data the browser stores and sends with every request to that site, often carrying the session ID | [System Design Notes → Auth Methods](system_design.md#going-deeper_3) |
| **Data Classification** | Public / Internal / Confidential / Restricted tiers that decide protection | [Data Security → What It Is](../../data/basics/data_security.md#what-it-is) |
| **Masking / Tokenization / Anonymization / Pseudonymization** | Ways to de-identify data. Masking hides part of a value (`****1234`). Tokenization swaps it for a token mapped back in a secure vault. Anonymization removes identity irreversibly. Pseudonymization replaces identifiers with codes that can be re-linked with a key, so it is still personal data under GDPR | [Data Security → What It Is](../../data/basics/data_security.md#what-it-is) |
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
| **CIA Triad** | Confidentiality, Integrity, Availability: the goals of security | [Security](security.md), [Wikipedia: CIA triad ↗](https://en.wikipedia.org/wiki/Information_security) |
| **Defense in Depth** | Layered controls so no single failure exposes you | [Security → Rule of Thumb](security.md#rule-of-thumb) |
| **Zero Trust** | Never trust the network; verify every request | [Wikipedia: Zero trust ↗](https://en.wikipedia.org/wiki/Zero_trust_architecture) |
| **Threat Model / STRIDE** | Structured look at what can go wrong / Spoofing, Tampering, Repudiation, Info disclosure, DoS, Elevation of privilege | [Wikipedia: Threat model ↗](https://en.wikipedia.org/wiki/Threat_model), [Wikipedia: STRIDE ↗](https://en.wikipedia.org/wiki/STRIDE_model) |
| **Attack Surface** | All the points an attacker could try | [Wikipedia: Attack surface ↗](https://en.wikipedia.org/wiki/Attack_surface) |
| **ACL** | Access Control List: who may do what on a resource | [Security → Authentication vs Authorization](security.md#authentication-vs-authorization) |
| **Access Token / Refresh Token / Scope** | Short-lived credential / long-lived one used to get new access tokens / what the token may do | [System Design Notes → Auth Methods](system_design.md#going-deeper_3) |
| **PKCE** | Proof Key for Code Exchange: protects OAuth code flow for public clients (SPAs, mobile) | [System Design Notes → Auth Methods](system_design.md#going-deeper_3) |
| **MITM / Replay Attack** | Attacker intercepts traffic / reuses a captured valid request | [System Design Notes → How SSH Works](system_design.md#going-deeper_4), [Wikipedia: MITM ↗](https://en.wikipedia.org/wiki/Man-in-the-middle_attack) |
| **TOFU** | Trust On First Use: accept a host key the first time, then pin it (SSH) | [System Design Notes → How SSH Works](system_design.md#going-deeper_4) |
| **Brute Force / Credential Stuffing** | Guess passwords / reuse leaked username-password pairs | [Security → Common Risks](security.md#common-risks-owasp-condensed), [Wikipedia: Credential stuffing ↗](https://en.wikipedia.org/wiki/Credential_stuffing) |
| **Phishing / Social Engineering** | Tricking people rather than systems | [Wikipedia: Phishing ↗](https://en.wikipedia.org/wiki/Phishing) |
| **Session Fixation / Clickjacking** | Force a known session ID on a victim / hide a real button under a fake UI | [System Design Notes → Auth Methods](system_design.md#going-deeper_3), [Wikipedia: Clickjacking ↗](https://en.wikipedia.org/wiki/Clickjacking) |
| **CSP / HSTS / SameSite** | Content-Security-Policy (limit script sources) / force HTTPS / cookie flag that blocks cross-site sending | [Security → Common Risks](security.md#common-risks-owasp-condensed), [MDN: CSP ↗](https://developer.mozilla.org/en-US/docs/Web/HTTP/Guides/CSP) |
| **Supply Chain Attack / SBOM** | Compromise via a dependency or build tool / Software Bill of Materials listing every component | [Wikipedia: Supply chain attack ↗](https://en.wikipedia.org/wiki/Supply_chain_attack), [Wikipedia: SBOM ↗](https://en.wikipedia.org/wiki/Software_supply_chain) |
| **Dependency / Secret Scanning** | Flag known-vulnerable packages (Dependabot) / leaked keys in code | [Security → Common Risks](security.md#common-risks-owasp-condensed) |
| **Vulnerability / Exploit / Zero-day** | A weakness / code that uses it / a flaw with no fix yet | [Wikipedia: Zero-day ↗](https://en.wikipedia.org/wiki/Zero-day_vulnerability) |
| **CVSS** | Common Vulnerability Scoring System (0–10 severity) | [Wikipedia: CVSS ↗](https://en.wikipedia.org/wiki/Common_Vulnerability_Scoring_System) |
| **Hardening / Patching** | Reduce attack surface by config / apply security updates | [Security → Common Risks](security.md#common-risks-owasp-condensed) |
| **Bastion / Jump Host** | Single hardened entry point for admin access | [Wikipedia: Bastion host ↗](https://en.wikipedia.org/wiki/Bastion_host) |
| **Sandbox** | Restricted environment that limits what code can touch | [Wikipedia: Sandbox ↗](https://en.wikipedia.org/wiki/Sandbox_(computer_security)) |
| **HSM** | Hardware Security Module for keys | [Wikipedia: Hardware security module ↗](https://en.wikipedia.org/wiki/Hardware_security_module) |
| **Key Rotation** | Regularly replacing keys and secrets | [System Design Notes → Auth Methods](system_design.md#going-deeper_3) |
| **SPIFFE / SPIRE** | Standard and implementation for workload identity, issuing short-lived certs for mTLS | [System Design Notes → Auth Methods](system_design.md#going-deeper_3) |
| **CRL / OCSP** | Certificate Revocation List / Online Certificate Status Protocol | [System Design Notes → Auth Methods](system_design.md#going-deeper_3) |
| **KYC / AML** | Know Your Customer / Anti-Money Laundering: identity and fraud rules in finance | [Becoming Senior → Business Capabilities](becoming_senior.md#think-in-business-capabilities-not-frameworks) |
| **SOX** | Sarbanes-Oxley Act: US financial-reporting controls | [Becoming Senior → Business Capabilities](becoming_senior.md#think-in-business-capabilities-not-frameworks) |
| **Data Residency** | Laws or contracts requiring data to stay in a given country or region | [Becoming Senior → Business Capabilities](becoming_senior.md#think-in-business-capabilities-not-frameworks) |
| **ISMS** | Information Security Management System (ISO 27001) | [Data Security → Frameworks](../../data/basics/data_security.md#frameworks-that-apply) |
| **Consent / Right to be Forgotten** | Lawful basis for processing personal data / the GDPR right to erasure | [Introduction to Data → Ethics of Data](../../data/basics/introduction_to_data.md#ethics-of-data), [Wikipedia: Right to be forgotten ↗](https://en.wikipedia.org/wiki/Right_to_be_forgotten) |

## Data Engineering

| Term | Meaning | Read more |
|---|---|---|
| **DB / RDB / RDBMS** | Database / Relational Database / Relational Database Management System | [Databases → Relational vs NoSQL](../../data/basics/databases.md#relational-vs-nosql) |
| **SQL / NoSQL** | Structured Query Language / non-relational stores | [Databases → SQL in One Breath](../../data/basics/databases.md#sql-in-one-breath), [Databases → Relational vs NoSQL](../../data/basics/databases.md#relational-vs-nosql) |
| **DDL / DML** | Data Definition (CREATE, ALTER) / Data Manipulation (INSERT, UPDATE, DELETE) | [Databases → SQL in One Breath](../../data/basics/databases.md#sql-in-one-breath) |
| **PK / FK / JOIN** | Primary Key (unique row id) / Foreign Key (reference to another table) / combine rows across tables | [Databases → SQL in One Breath](../../data/basics/databases.md#sql-in-one-breath) |
| **Window Function** | SQL function computed over a set of related rows without collapsing them (`ROW_NUMBER() OVER (PARTITION BY …)`) | [Wikipedia: Window function ↗](https://en.wikipedia.org/wiki/Window_function_(SQL)) |
| **Cardinality** | Number of distinct values in a column (high = user IDs, low = country); drives index choice and observability cost | [Wikipedia: Cardinality ↗](https://en.wikipedia.org/wiki/Cardinality_(SQL_statements)) |
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
| **Transaction** | A group of operations that succeed or fail as one unit (`BEGIN … COMMIT` / `ROLLBACK`) | [Databases → Transactions & ACID](../../data/basics/databases.md#transactions-acid), [Wikipedia: Transaction ↗](https://en.wikipedia.org/wiki/Database_transaction) |
| **Schema Migration** | Versioned, scripted change to a database schema; on live systems done as expand → migrate → contract | [System Design Notes → Deployment Strategies](system_design.md#going-deeper_5), [Wikipedia: Schema migration ↗](https://en.wikipedia.org/wiki/Schema_migration) |
| **Isolation Levels** | Read Uncommitted → Read Committed → Repeatable Read → Serializable: stronger isolation means fewer anomalies and less concurrency | [Databases → Isolation Levels](../../data/basics/databases.md#isolation-levels) |
| **Normalization / 3NF / Denormalization** | Remove redundancy by splitting tables / third normal form / add redundancy back for read speed | [Data Modelling → Modelling Styles](../../data/basics/data_modeling.md#modelling-styles), [Wikipedia: Normalization ↗](https://en.wikipedia.org/wiki/Database_normalization) |
| **WAL** | Write-Ahead Log: log changes before applying them, for durability and recovery | [Wikipedia: WAL ↗](https://en.wikipedia.org/wiki/Write-ahead_logging) |
| **OLTP / OLAP** | Online Transaction Processing / Online Analytical Processing | [Data Modelling → Modelling Styles](../../data/basics/data_modeling.md#modelling-styles) |
| **ETL / ELT** | Extract-Transform-Load / Extract-Load-Transform | [Data Engineering → ETL vs ELT](../../data/basics/data_engineering.md#etl-vs-elt) |
| **Warehouse / Lake / Lakehouse** | Where data lands: modeled tables / raw files / both on one store | [Data Engineering → Where Data Lands](../../data/basics/data_engineering.md#where-data-lands) |
| **Batch / Streaming** | Process data in scheduled chunks / continuously as it arrives | [Data Engineering → Batch vs Streaming](../../data/basics/data_engineering.md#batch-vs-streaming) |
| **DAG** | Directed Acyclic Graph: pipeline tasks and their dependencies | [Data Engineering → Orchestration](../../data/basics/data_engineering.md#orchestration) |
| **MapReduce / Spark / HDFS** | MapReduce: process data in parallel *map* steps, then combine with *reduce* steps. Spark: an in-memory distributed engine that largely replaced it. HDFS: Hadoop's distributed file system that stores the data across nodes | [Big Data → Distributed Processing](../../data/basics/big_data.md#distributed-processing) |
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
| **Parquet / ORC / Avro** | Columnar formats for analytics / row-based format for streaming with schema evolution | [Data Engineering → File Formats](../../data/basics/data_engineering.md#file-formats) |
| **Delta Lake / Iceberg / Hudi** | Table formats adding ACID and time travel on top of lake files | [Data Engineering → Where Data Lands](../../data/basics/data_engineering.md#where-data-lands) |
| **Schema-on-Write / Schema-on-Read** | Validate structure when loading (warehouse) / interpret it when querying (lake) | [Data Engineering → Where Data Lands](../../data/basics/data_engineering.md#where-data-lands) |
| **Data Pipeline** | Automated flow that moves and transforms data | [Data Engineering](../../data/basics/data_engineering.md) |
| **Orchestrator (Airflow / Dagster / Prefect)** | Schedules and monitors pipeline DAGs | [Data Engineering → Orchestration](../../data/basics/data_engineering.md#orchestration) |
| **Incremental Load / Full Load / Backfill** | Load only new or changed rows / reload everything / re-run history for past dates | [Data Engineering → Rule of Thumb](../../data/basics/data_engineering.md#rule-of-thumb), [System Design Notes → Deployment Strategies (backfill)](system_design.md#going-deeper_5) |
| **CDC** | Change Data Capture: stream row changes from a database log | [Wikipedia: Change data capture ↗](https://en.wikipedia.org/wiki/Change_data_capture) |
| **Upsert / MERGE** | Insert or update in one operation | [Wikipedia: MERGE ↗](https://en.wikipedia.org/wiki/Merge_(SQL)) |
| **Reverse ETL** | Push warehouse data back into operational tools (CRM, ads) | [Wikipedia: ETL ↗](https://en.wikipedia.org/wiki/Extract,_transform,_load) |
| **dbt** | SQL-based transformation tool for ELT in the warehouse | [getdbt.com ↗](https://docs.getdbt.com/docs/introduction) |
| **Kafka** | Distributed log for event streaming | [Architecture → Message Queues](architecture.md#message-queues), [Wikipedia: Apache Kafka ↗](https://en.wikipedia.org/wiki/Apache_Kafka) |
| **Fact / Dimension Table** | Measurable events (sales) / descriptive context (customer, date) | [Data Modelling → Modelling Styles](../../data/basics/data_modeling.md#modelling-styles) |
| **SCD** | Slowly Changing Dimension: how to keep history when attributes change (Type 1 overwrite, Type 2 new row) | [Wikipedia: Slowly changing dimension ↗](https://en.wikipedia.org/wiki/Slowly_changing_dimension) |
| **Surrogate / Natural Key** | System-generated ID / a real-world identifier (email, tax ID) | [Wikipedia: Surrogate key ↗](https://en.wikipedia.org/wiki/Surrogate_key) |
| **Data Vault** | Warehouse model of hubs, links, satellites; auditable and easy to extend | [Data Modelling → Modelling Styles](../../data/basics/data_modeling.md#modelling-styles) |
| **Inmon / Kimball** | Top-down enterprise 3NF warehouse / bottom-up dimensional data marts | [Data Modelling → Frameworks](../../data/basics/data_modeling.md#frameworks-that-apply) |
| **Medallion (Bronze / Silver / Gold)** | Lakehouse layers: raw → cleaned → business-ready | [Data Modelling → Frameworks](../../data/basics/data_modeling.md#frameworks-that-apply) |
| **Data Mesh** | Domain teams own their data as products, on a shared platform | [Data Modelling → Frameworks](../../data/basics/data_modeling.md#frameworks-that-apply) |
| **Data Mart** | Subject-specific slice of a warehouse for one team | [Wikipedia: Data mart ↗](https://en.wikipedia.org/wiki/Data_mart) |
| **View / Materialized View** | Saved query / saved query whose result is stored and refreshed | [Wikipedia: Materialized view ↗](https://en.wikipedia.org/wiki/Materialized_view) |
| **Stored Procedure / Trigger** | Code stored in the DB / code that runs automatically on a table event | [Wikipedia: Stored procedure ↗](https://en.wikipedia.org/wiki/Stored_procedure), [Wikipedia: Database trigger ↗](https://en.wikipedia.org/wiki/Database_trigger) |
| **B-tree / LSM Tree** | Read-optimized index structure (most RDBMS) / write-optimized one (Cassandra, RocksDB) | [Databases → Indexing](../../data/basics/databases.md#indexing), [Wikipedia: LSM tree ↗](https://en.wikipedia.org/wiki/Log-structured_merge-tree) |
| **MVCC** | Multi-Version Concurrency Control: readers see a snapshot while writers proceed | [Wikipedia: MVCC ↗](https://en.wikipedia.org/wiki/Multiversion_concurrency_control) |
| **Query Plan / EXPLAIN** | How the DB will execute a query / the command that shows it | [Databases → Indexing](../../data/basics/databases.md#indexing) |
| **Data Lineage** | Where data came from and every step it went through | [Data Engineering → Rule of Thumb](../../data/basics/data_engineering.md#rule-of-thumb), [Data Governance](../../data/basics/data_governance.md#what-it-is) |
| **Data Catalog / Business Glossary** | Searchable inventory of datasets / agreed definitions of business terms | [Data Governance → What It Is](../../data/basics/data_governance.md#what-it-is) |
| **Data Owner / Steward / Custodian** | Accountable for a domain's data / manages its quality and meaning day to day / runs the systems that store it | [Data Governance → What It Is](../../data/basics/data_governance.md#what-it-is) |
| **DAMA-DMBOK / DCAM / COBIT** | Data management body of knowledge / EDM Council capability model / IT governance framework | [Data Governance → Frameworks](../../data/basics/data_governance.md#frameworks-that-apply) |
| **Data Quality Dimensions** | Accuracy, completeness, consistency, timeliness, validity, uniqueness | [Data Quality → What It Is](../../data/basics/data_quality.md#what-it-is), [Introduction to Data → Quality Dimensions](../../data/basics/introduction_to_data.md#data-quality-dimensions) |
| **Data Profiling / Cleansing** | Measure the defects first / fix them: standardize, de-duplicate, validate, handle missing values and outliers | [Data Quality → The Cleansing Workflow](../../data/basics/data_quality.md#the-cleansing-workflow) |
| **Data Contract** | Agreed schema and quality guarantees between data producer and consumer | [Data Quality → Frameworks](../../data/basics/data_quality.md#frameworks-that-apply) |
| **DMAIC / Six Sigma** | Define, Measure, Analyze, Improve, Control: a quality-improvement cycle | [Data Quality → Frameworks](../../data/basics/data_quality.md#frameworks-that-apply) |
| **Ingestion / Transformation / Aggregation** | Bring data in / reshape and clean it / summarize it | [Introduction to Data → Core Concepts](../../data/basics/introduction_to_data.md#core-concepts) |
| **Discrete / Continuous** | Countable values / any value on a scale | [Introduction to Data → Types of Data](../../data/basics/introduction_to_data.md#types-of-data) |
| **Quantitative / Qualitative** | Numerical / categorical data | [Introduction to Data → Types of Data](../../data/basics/introduction_to_data.md#types-of-data) |
| **Data Import Sources** | Flat files, databases, APIs, spreadsheets, web scraping | [Introduction to Data → Importing Data](../../data/basics/introduction_to_data.md#importing-data) |

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
| **Confounder** | Hidden variable that drives two others, faking a causal link | [Analytics → Traps to Avoid](../../data/basics/analytics.md#traps-to-avoid) |
| **Simpson's Paradox** | A trend in every subgroup reverses when the groups are combined | [Analytics → Traps to Avoid](../../data/basics/analytics.md#traps-to-avoid) |
| **Sampling Bias** | The sample doesn't represent the population | [Analytics → Traps to Avoid](../../data/basics/analytics.md#traps-to-avoid) |
| **Vanity Metric / Actionable Metric** | Looks good but drives no decision / changes what you do | [Analytics → Traps to Avoid](../../data/basics/analytics.md#traps-to-avoid) |
| **A/B Test / Hypothesis** | Randomized experiment comparing two variants / the claim it tests | [Analytics → Traps to Avoid](../../data/basics/analytics.md#traps-to-avoid), [System Design Notes → Deployment Strategies](system_design.md#going-deeper_5) |
| **Mode / Skew / Kurtosis** | Most frequent value / lopsidedness / tail heaviness | [Analytics → Descriptive Statistics](../../data/basics/analytics.md#descriptive-statistics) |
| **Normal Distribution** | Symmetric bell curve; mean = median = mode | [Wikipedia: Normal distribution ↗](https://en.wikipedia.org/wiki/Normal_distribution) |
| **Confidence Interval** | Range likely to contain the true value at a given confidence (e.g. 95%) | [Wikipedia: Confidence interval ↗](https://en.wikipedia.org/wiki/Confidence_interval) |
| **Regression (Statistics)** | Model the relationship between a target and predictors | [Wikipedia: Regression analysis ↗](https://en.wikipedia.org/wiki/Regression_analysis) |
| **Cohort / Funnel / Retention / Churn** | Group by start date / steps toward conversion / share who come back / share who leave | [Wikipedia: Cohort analysis ↗](https://en.wikipedia.org/wiki/Cohort_analysis), [Wikipedia: Churn rate ↗](https://en.wikipedia.org/wiki/Churn_rate) |
| **DAU / MAU** | Daily / Monthly Active Users | [Wikipedia: Active users ↗](https://en.wikipedia.org/wiki/Active_users) |
| **Conversion Rate** | Share of visitors who complete a goal | [Wikipedia: Conversion rate ↗](https://en.wikipedia.org/wiki/Conversion_rate_optimization) |
| **Segmentation** | Split data into meaningful groups before comparing | [Analytics → Traps to Avoid](../../data/basics/analytics.md#traps-to-avoid) |
| **Dimension / Measure** | Attribute you slice by (region) / number you aggregate (revenue) | [Data Modelling → Modelling Styles](../../data/basics/data_modeling.md#modelling-styles) |
| **Pivot Table / Drill-down** | Summarize by rows and columns / move from summary to detail | [Wikipedia: Pivot table ↗](https://en.wikipedia.org/wiki/Pivot_table) |
| **Seasonality / Trend / Forecast** | Repeating patterns / long-run direction / predicted future values | [Wikipedia: Time series ↗](https://en.wikipedia.org/wiki/Time_series), [Visualization → Pick the Chart](../../data/basics/visualization.md#pick-the-chart-by-the-relationship) |
| **Data Storytelling** | Present insights as a narrative with one message per chart | [Visualization → Design Principles](../../data/basics/visualization.md#design-principles) |
| **Chart Distortions** | Truncated axes, dual axes, 3D effects, overloaded pies | [Visualization → Common Distortions](../../data/basics/visualization.md#common-distortions) |
| **Operational / Strategic Dashboard** | Real-time monitoring / long-term KPI trends | [Visualization → Dashboards](../../data/basics/visualization.md#dashboards) |
| **Data-Driven Decision** | Question → data → analysis → insight → action | [Introduction to Data → From Data to Decision](../../data/basics/introduction_to_data.md#from-data-to-decision) |
| **Data Ethics** | Consent, privacy, fairness, and transparency in data use | [Introduction to Data → Ethics of Data](../../data/basics/introduction_to_data.md#ethics-of-data) |

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
| **Top-p / Top-k Sampling** | Sample the next token only from the smallest set covering probability p / from the k most likely tokens | [Wikipedia: Top-p sampling ↗](https://en.wikipedia.org/wiki/Top-p_sampling) |
| **Vibe Coding** | Building by prompting an AI and accepting its code without reading it closely | [Skills Map → Software Engineering Fundamentals](../../ai/basics/skills_map.md#2-software-engineering-fundamentals), [Wikipedia: Vibe coding ↗](https://en.wikipedia.org/wiki/Vibe_coding) |
| **Local Inference** | Running models on your own hardware (Ollama, vLLM, llama.cpp) | [AI Tools → Local Inference](../../ai/tool_tip/tools.md#local-inference-and-serving) |
| **Jupyter Notebook** | Interactive document mixing code, output, and notes; standard for data analysis and ML experiments | [Wikipedia: Project Jupyter ↗](https://en.wikipedia.org/wiki/Project_Jupyter) |
| **RAG** | Retrieval-Augmented Generation: fetch relevant documents (often from a vector DB) and put them in the prompt | [Skills Map → Building AI Apps](../../ai/basics/skills_map.md#1-building-and-deploying-ai-applications), [Wikipedia: RAG ↗](https://en.wikipedia.org/wiki/Retrieval-augmented_generation) |
| **Embedding / Vector DB** | Meaning as a vector / a store that searches by vector similarity | [Data Engineering](#data-engineering) |
| **Fine-tuning** | Further training a pre-trained model on task-specific data | [Wikipedia: Fine-tuning ↗](https://en.wikipedia.org/wiki/Fine-tuning_(deep_learning)) |
| **Hallucination** | Fluent output that is false or unsupported | [Wikipedia: Hallucination ↗](https://en.wikipedia.org/wiki/Hallucination_(artificial_intelligence) |
| **Evals** | Repeatable test sets and metrics that score model or agent output | [AI Tools → Track and Deploy](../../ai/tool_tip/tools.md#track-and-deploy), [Skills Map → Building AI Apps](../../ai/basics/skills_map.md#1-building-and-deploying-ai-applications) |
| **Guardrails** | Checks around a model or agent that block unsafe input, output, or actions | [Claude Code → Hooks](../../ai/tool_tip/claude_code.md#worked-examples) |
| **Prompt Injection** | Untrusted content (a web page, file, or email) smuggles instructions the model then follows | [Codex → Avoid the Sharp Edges](../../ai/tool_tip/codex.md#7-avoid-the-sharp-edges), [Wikipedia: Prompt injection ↗](https://en.wikipedia.org/wiki/Prompt_injection) |
| **Jailbreak** | A prompt crafted to bypass a model's safety rules | [OWASP Top 10 for LLM Apps ↗](https://owasp.org/www-project-top-10-for-large-language-model-applications/) |
| **Adversarial Test / Red Teaming** | Attack your own LLM system with hostile inputs (injection, jailbreaks, data extraction) before real attackers do | [Testing & QA](#testing-qa), [Wikipedia: Adversarial ML ↗](https://en.wikipedia.org/wiki/Adversarial_machine_learning), [Wikipedia: Red team ↗](https://en.wikipedia.org/wiki/Red_team) |
| **SDD** | Spec-Driven Development with AI agents | [Spec-Driven Development](../../ai/tool_tip/spec_driven_development.md) |
| **GSD / BMad / Spec Kit / Agent OS** | Spec-driven tools for AI coding. GSD: a discuss → plan → execute → verify → ship loop with state files. BMad: multi-role (product, architecture, UX, dev, test) delivery lifecycle. Spec Kit: GitHub's principles → spec → plan → tasks flow. Agent OS: captures codebase conventions to guide specs | [Spec-Driven Development → Four Tooling Approaches](../../ai/tool_tip/spec_driven_development.md#four-tooling-approaches) |
| **Rule-based / Statistical AI** | Hand-written if-then rules / models fitted to data | [AI Concepts → Rule-based](../../ai/basics/concepts.md#rule-based), [AI Concepts → Statistical](../../ai/basics/concepts.md#statistical) |
| **Supervised / Unsupervised / Reinforcement Learning** | Learn from labeled examples / find structure without labels / learn by reward | [AI Concepts → Machine Learning](../../ai/basics/concepts.md#machine-learning) |
| **Neural Network / Backpropagation** | Layers of weighted units that learn by passing errors backward to adjust the weights | [AI Concepts → Deep Learning](../../ai/basics/concepts.md#deep-learning), [Wikipedia: Backpropagation ↗](https://en.wikipedia.org/wiki/Backpropagation) |
| **Hyperparameter / Cross-validation** | Settings chosen before training (learning rate, depth) / rotating train–validation splits to estimate performance reliably | [AI Concepts → Machine Learning](../../ai/basics/concepts.md#machine-learning), [Wikipedia: Cross-validation ↗](https://en.wikipedia.org/wiki/Cross-validation_(statistics)) |
| **Feature Engineering / Feature Store** | Turning raw data into model inputs / a shared system that serves the same features to training and production | [AI Concepts → Statistical](../../ai/basics/concepts.md#statistical), [Wikipedia: Feature engineering ↗](https://en.wikipedia.org/wiki/Feature_engineering) |
| **Data Drift / Model Drift** | Production inputs shift away from the training data / the model's accuracy decays as a result | [Wikipedia: Concept drift ↗](https://en.wikipedia.org/wiki/Concept_drift) |
| **NLP** | Natural Language Processing | [Wikipedia: NLP ↗](https://en.wikipedia.org/wiki/Natural_language_processing) |
| **CNN / RNN / Transformer** | Convolutional net (images) / Recurrent net (sequences) / attention-based architecture behind LLMs | [AI Concepts → Deep Learning](../../ai/basics/concepts.md#deep-learning), [Wikipedia: Transformer ↗](https://en.wikipedia.org/wiki/Transformer_(deep_learning)) |
| **Attention** | Mechanism letting each token weigh every other token | [Wikipedia: Attention ↗](https://en.wikipedia.org/wiki/Attention_(machine_learning)) |
| **Parameters / Weights** | The learned numbers inside a model; model size is counted in them (7B, 70B) | [Wikipedia: LLM ↗](https://en.wikipedia.org/wiki/Large_language_model) |
| **Training / Inference** | Learning the weights / using the model to produce output | [AI Tools → Local Inference](../../ai/tool_tip/tools.md#local-inference-and-serving) |
| **Pre-training / RLHF** | Learn from huge unlabeled text / Reinforcement Learning from Human Feedback to align behavior | [Wikipedia: RLHF ↗](https://en.wikipedia.org/wiki/Reinforcement_learning_from_human_feedback) |
| **Feature / Label** | Input variable / the answer the model learns to predict | [Wikipedia: Feature ↗](https://en.wikipedia.org/wiki/Feature_(machine_learning)) |
| **Train / Validation / Test Split** | Data to fit / to tune / to measure final performance | [Wikipedia: Data splits ↗](https://en.wikipedia.org/wiki/Training,_validation,_and_test_data_sets) |
| **Overfitting / Underfitting** | Memorizes training data / too simple to capture the pattern | [Wikipedia: Overfitting ↗](https://en.wikipedia.org/wiki/Overfitting) |
| **Precision / Recall / F1 / Accuracy** | Of predicted positives, share correct / of actual positives, share found / their harmonic mean / overall share correct | [Wikipedia: Precision and recall ↗](https://en.wikipedia.org/wiki/Precision_and_recall) |
| **Confusion Matrix** | Table of true vs predicted classes | [Wikipedia: Confusion matrix ↗](https://en.wikipedia.org/wiki/Confusion_matrix) |
| **Loss / Gradient Descent / Epoch / Learning Rate** | Error to minimize / the optimization method / one pass over the data / step size | [Wikipedia: Gradient descent ↗](https://en.wikipedia.org/wiki/Gradient_descent) |
| **Quantization / Distillation / LoRA** | Lower-precision weights to save memory / train a small model from a big one / cheap fine-tuning with low-rank adapters | [Wikipedia: LoRA ↗](https://en.wikipedia.org/wiki/LoRA_(machine_learning)) |
| **Chain-of-Thought / Reasoning Model** | Step-by-step reasoning in the output / models trained to think before answering | [Wikipedia: Prompt engineering ↗](https://en.wikipedia.org/wiki/Prompt_engineering) |
| **Multimodal** | Handles more than text: images, audio, video | [Wikipedia: Multimodal learning ↗](https://en.wikipedia.org/wiki/Multimodal_learning) |
| **Context Engineering** | Deciding what goes into the context window: instructions, files, memory, tools | [Skills Map → Building AI Apps](../../ai/basics/skills_map.md#1-building-and-deploying-ai-applications), [Claude Code → Manage Context](../../ai/tool_tip/claude_code.md#1-manage-context) |
| **Tool Use / Function Calling** | Model emits a structured call that your code executes | [Claude Docs: Tool use ↗](https://docs.claude.com/en/docs/agents-and-tools/tool-use/overview) |
| **Structured Output** | Model output constrained to a JSON schema | [OpenAI: Structured Outputs ↗](https://platform.openai.com/docs/guides/structured-outputs) |
| **Chunking / Reranking / Semantic Search** | Split docs for retrieval / reorder candidates by relevance / search by meaning, not keywords | [Wikipedia: RAG ↗](https://en.wikipedia.org/wiki/Retrieval-augmented_generation) |
| **Grounding / Citation** | Tie answers to retrieved sources so they can be checked | [Wikipedia: RAG ↗](https://en.wikipedia.org/wiki/Retrieval-augmented_generation) |
| **Multi-agent / Orchestration** | Several agents with roles coordinated by a lead agent | [AI Concepts → AI Agents](../../ai/basics/concepts.md#ai-agents), [Codex → Orchestrate Multiple Agents](../../ai/tool_tip/codex.md#5-orchestrate-multiple-agents) |
| **HITL** | Human-in-the-Loop: a person approves or corrects agent steps | [Codex → Two Dials, Not One](../../ai/tool_tip/codex.md#two-dials-not-one) |
| **LLM-as-a-Judge** | Use a model to grade another model's output in evals | [AI Tools → Evaluate Before Expanding](../../ai/tool_tip/tools.md#evaluate-before-expanding) |
| **TTFT / Tokens per Second** | Time To First Token / generation speed | [NVIDIA: LLM inference metrics ↗](https://docs.nvidia.com/nim/benchmarking/llm/latest/metrics.html) |
| **Prompt Caching** | Reuse the processed prefix of a prompt to cut cost and latency | [Claude Docs: Prompt caching ↗](https://docs.claude.com/en/docs/build-with-claude/prompt-caching) |
| **Context Compaction** | Summarize old conversation to free the context window | [Claude Code → Session Hygiene](../../ai/tool_tip/claude_code.md#session-hygiene) |
| **Memory (Agent)** | Facts an agent persists across sessions (CLAUDE.md, AGENTS.md, memory files) | [Claude Code → Auto Memory](../../ai/tool_tip/claude_code.md#auto-memory), [Codex → Memories](../../ai/tool_tip/codex.md#memories) |
| **CLAUDE.md / AGENTS.md** | Repository instruction files that coding agents load each session | [Claude Code → CLAUDE.md](../../ai/tool_tip/claude_code.md#claudemd), [Codex → AGENTS.md](../../ai/tool_tip/codex.md#agentsmd) |
| **Plan Mode** | Agent proposes a plan before changing anything | [Claude Code → Plan Mode](../../ai/tool_tip/claude_code.md#plan-mode-and-extended-thinking), [Codex → Plan Mode](../../ai/tool_tip/codex.md#plan-mode) |
| **Permission Mode / Sandbox** | What an agent may do without asking / the OS-level box it runs in | [Claude Code → Permission Modes](../../ai/tool_tip/claude_code.md#permission-modes), [Codex → Two Dials](../../ai/tool_tip/codex.md#two-dials-not-one) |
| **Worktree (Agents)** | Separate Git working directory so parallel agents don't collide | [Codex → Worktrees](../../ai/tool_tip/codex.md#worktrees) |
| **Model Card / Responsible AI** | Documentation of a model's data, limits, and risks / building AI that is fair, safe, accountable | [Hugging Face: Model cards ↗](https://huggingface.co/docs/hub/model-cards) |
| **Bias / Fairness** | Systematic skew in model outcomes across groups | [Wikipedia: Algorithmic bias ↗](https://en.wikipedia.org/wiki/Algorithmic_bias) |
| **MLOps / LLMOps** | Practices for deploying, monitoring, and versioning models | [AI Tools → Track and Deploy](../../ai/tool_tip/tools.md#track-and-deploy), [Wikipedia: MLOps ↗](https://en.wikipedia.org/wiki/MLOps) |
| **AI Engineering** | Building products on top of models: evals, context, agents, deployment | [The AI Engineering Skills Map](../../ai/basics/skills_map.md) |
