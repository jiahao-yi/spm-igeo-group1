# Ideas - Wang, Jingru

## Initial Understanding

TOMI Automobiles produces two car lines: GEO (compact cars) and TEO (sedans).
George Wein wants to extend the GEO line with a new model, **iGEO**, that adds
Internet of Moving Things (IoMT) software features to increase customer
satisfaction and keep TOMI competitive against rivals already adopting IoT.

Key constraint decided by the CTO: for safety/security reasons the IoMT software
must be **completely decoupled** from the GEO-specific software and hardware, and
**must never influence driving-critical functions** (e.g. accelerating/braking).

Technical setup as I understand it:

- **iGEO IoMT Hardware** — a dedicated processor running the IoMT features.
- **Hosting Application** — a customized server on the hardware where iGEO
  modules can be deployed, enabled, and disabled.
- **iGEO IoMT Display** — a dedicated extra display showing the hosting app GUI
  and all module GUIs.
- Two example modules: **WH Module** ("Drive to Welcoming Home" — talks to smart
  home devices: heating, lights, garage gate) and **SC Module** ("Smart
  Commercials" — notifies driver of nearby store offers, can be filtered/off).

Project frame (from the description):

- Start: 1 June 2023, duration: 1 year.
- Budget ceiling: **1,000,000 EUR**.
- George Wein is the project manager.
- TOMI lacks capacity, so part of the work is **outsourced**: choice of the IoMT
  Hardware (with reasoning vs alternatives), choice of the IoMT Display (usability
  tested with GEO cars), and development of the hosting application + GUI.

Draft of the project-definition elements (Task 1.1):

- **Scope**: deliver the iGEO model = IoMT hardware + hosting app + dedicated
  display + WH and SC modules, decoupled from driving functions. *Out of scope*:
  changes to GEO driving software/hardware, additional modules beyond WH/SC.
- **Business goals**: increase customer satisfaction; stay competitive in IoMT;
  open a software-feature differentiation for the GEO line.
- **Project goals**: working iGEO prototype + 2 modules within 1 year and within
  1,000,000 EUR, fully decoupled and safe.
- **Critical success factors**: clear & stable requirements; strict decoupling
  from driving functions; data privacy/GDPR compliance; right supplier choice;
  staying within budget and schedule.
- **Assumptions**: see the Estimation Assumptions section below.
- **Constraints**: 1 year, ≤ 1,000,000 EUR, no impact on driving-critical
  functions, GDPR compliance, limited internal capacity (outsourcing needed).
- **Stakeholders**: see the Stakeholder Observations section below.

## Suggested WBS Items

At least 10 work packages (Task 2 needs ≥ 10). First-cut breakdown:

1. **Project setup & planning** — kickoff, plan, roles, budget baseline.
2. **Requirements engineering** — elicit & specify IoMT + WH + SC requirements
   (CTO stressed clear requirements; several stakeholders flagged this as risky).
3. **Architecture & decoupling design** — define how IoMT software is isolated
   from GEO driving software/hardware.
4. **Supplier selection & contracting** — criteria, comparison, contract.
5. **iGEO IoMT Hardware selection** — evaluate options, choose, justify (outsourced).
6. **iGEO IoMT Display selection** — usability evaluation with GEO cars (outsourced).
7. **Hosting Application + GUI development** (outsourced).
8. **WH Module development**.
9. **SC Module development**.
10. **Data privacy / GDPR compliance assessment**.
11. **Integration** — modules + hosting app + hardware + display.
12. **Testing** — unit, integration, system, acceptance, safety/decoupling tests.
13. **Market / user acceptance survey**.
14. **Deployment & roll-out**.
15. **Project management & supplier coordination** (ongoing).

Dependency intuition (useful for Task 4): Requirements → Architecture →
(Supplier + Hardware + Display selection in parallel) → Hosting app + modules
development → Integration → Testing → Deployment. Compliance assessment runs in
parallel once requirements exist.

## Stakeholder Observations

From the executive meeting statements. Attitude reasoning matters for the
socio-diagram (Task 2a) and power-matrix (Task 2b).

| Stakeholder | Role | Attitude | Interest | Power | Reasoning |
| --- | --- | --- | --- | --- | --- |
| George Wein | Project Manager / initiator | Champion | High | Medium | Came up with iGEO; drives the project but is not C-level. |
| Tom Wards | CTO | Supportive | High | High | Likes the idea but insists on starting slow, security first, clear requirements. |
| Jim Becker | Executive Marketing | Neutral/positive | Medium | Medium | Easy to market; only worry is price/affordability. |
| Julia Andersen | Finance & Controlling Director | Skeptical | High | High | Sees it as financially risky; worried about cost vs profit per unit. |
| Peter Scofield | Executive IT | Resistant | High | High | Security/privacy fears + no spare IT capacity (busy on another project). |
| Anne Smith | Lead IT Architect | Hidden supportive | High | Medium | Privately confident decoupling is safe, but keeps low profile to avoid clashing with Peter. |
| Jane Wilson | Sales Manager | Neutral | Medium | Low | Needs a target-customer/region sales strategy before committing. |
| Jim Bucksley | Developer | Supportive | High | Low | Enthusiastic; thinks it's cheap and low-risk (maybe underestimates effort). |
| David Renegan | Developer | Hidden resistant | Low | Low | Publicly agrees but privately reluctant; expects Tom/Peter to lobby him. |
| John Burton | GEO Product Line Manager | Supportive | High | High | iGEO fits GEO's strategy of adopting new tech. |
| Jonathan Newman | TEO Product Line Manager | Hidden resistant | Medium | Low | Privately thinks the idea is "insane"; rival product line, avoids open conflict. |

Relations to capture in the socio-diagram:

- Peter (resistant) vs Anne (her boss); Anne stays quiet — tension, no open conflict.
- Tom & Peter likely to lobby David (David expects it).
- John (GEO) vs Jonathan (TEO) — product-line rivalry.
- Jonathan plans to talk to Tom privately at a dinner party — informal influence.

Counter-action ideas (Task 2c):

- Julia (skeptical, high power): early business case + cost/benefit + per-unit
  profit analysis; involve in budget gate decisions.
- Peter (resistant, high power): show the decoupling architecture and a security
  plan; address the capacity concern (that's what outsourcing is for).
- Anne (hidden supportive): give her a visible technical-lead role so her support
  becomes active.
- Jonathan & David (hidden resistant): surface their concerns early via 1:1s so
  hidden resistance doesn't undermine the project later.

## Supplier Decision Ideas

Two candidates for the outsourced work (hardware, display, hosting app + GUI):
**FunIOT** (start-up) vs **ProfCar** (long-established). My proposed selection
criteria (Task 2 needs 2–5):

1. **Cost / service charge** — FunIOT 650 €/person-day vs ProfCar 1000 €/person-day;
   min initial contract 100k vs 300k €. Budget is capped at 1,000,000 €, so cost
   matters a lot.
2. **Flexibility to changing requirements** — FunIOT is Agile/SCRUM and welcomes
   change; ProfCar is Waterfall with strict change rules. iGEO requirements are
   new and immature, so flexibility is valuable.
3. **Security & safety track record / process maturity** — ProfCar has CMMI+ITIL,
   ISO certification, long safety-car success; FunIOT has no SPI/CMMI experience,
   no certification. Both had a reputation scandal (FunIOT: faulty parts → fatal
   accident; ProfCar: security breach → hacked data center).
4. **IoT / technical capability** — ProfCar: 5 successful smart-car projects, 5G;
   FunIOT: 1 project, 4G, but partners with a strong technical university.
5. **Support & warranty** — ProfCar 3-yr warranty but pricier support (250 €/h);
   FunIOT 1-yr warranty, cheaper support (100 €/h).

My early leaning: **FunIOT**, because the project is budget-constrained and the
requirements are new and likely to change a lot, which suits an Agile start-up.
But the security scandal + lack of certification is a real risk given the CTO's
security emphasis — needs weighing. Final answer should come from the paired
comparison + grid analysis (Task 2), not from gut feeling.

## Estimation Assumptions

For Planning Poker (Task 3.1) and Use Case Points (Task 3.2):

- The project must finish within **1 year** and cost **≤ 1,000,000 EUR**.
- The team has basic skills across engineering, architecture, testing, and
  management; the chosen supplier is capable of delivering the outsourced work.
- Only WH and SC modules are in scope (no extra modules).
- Requirements may change during the project (immature idea) — estimates carry
  uncertainty, especially for requirements-heavy and integration work packages.
- For Use Case Points, where a factor needs actor knowledge (e.g. Application
  Experience), we treat our own team members as the actors (per the assignment note).
- Hardest WPs to estimate (my guess): Requirements engineering and the
  decoupling/architecture design — high uncertainty, so I expect the biggest gap
  between highest and lowest poker estimates there.

## Scheduling/Resource Planning Ideas

For the activity network (Task 4.1) and Gantt (Task 4.2):

- Likely sequence: Requirements → Architecture/decoupling → (Supplier selection,
  Hardware selection, Display selection in parallel) → Hosting app + WH + SC
  development → Integration → Testing → Deployment.
- Parallelizable: market/user survey, GDPR compliance assessment, and supplier
  selection can run alongside early design work.
- WH and SC module development can largely run in parallel once the hosting app
  interface is defined.
- Critical path candidate: Requirements → Architecture → Hosting app → module
  development → Integration → Testing → Deployment.
- Use the four precedence types (FS, SS, FF, SF) — e.g. testing can start before
  all development finishes (SS), deployment finishes only after testing finishes (FF).
- Resources: we use our actual team members (6 people) with fictitious working-time
  data allowed. Need a skills table (Task 4.2b): e.g. Web Design, Database,
  Programming, Sales+Mkg, scored 1–6 per member, then assign people to activities
  by capacity.

## Open Questions

- How many internal developers does TOMI actually have, and how many work-days
  per person per year should we assume?
- Are the internal developers responsible only for the WH and SC modules, while
  the supplier builds the hosting app/hardware/display?
- What point scale should we use for Planning Poker (Fibonacci, T-shirt sizes)?
- How do we quantify the budget split between internal effort and the outsourced
  contract (FunIOT min 100k vs ProfCar min 300k)?
- For the supplier scandal risk — should "reputation/security" be a hard
  knock-out criterion or just a weighted criterion in the grid analysis?
- Which precedence relations genuinely apply between our WPs (need group agreement
  before drawing the activity network)?
