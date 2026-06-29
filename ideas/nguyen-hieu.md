# Ideas - Hieu Nguyen

## Initial Understanding

TOMI is an automotive company in Aachen with two product lines: GEO for compact cars and TEO for sedan cars.

The iGEO project should extend the GEO line with Internet of Moving Things features. The main idea is not to build an autonomous driving system, but to add separated software features that improve comfort and customer experience.

A key point is that the IoMT features must be clearly decoupled from the normal GEO hardware and software. They must not influence safety critical driving functions.

The planned system includes the iGEO IoMT Hardware, a dedicated IoMT Display, a hosting application, and deployable software modules.

The two exemplary modules are the Welcoming Home Module and the Smart Commercials Module. The WH Module has more technical and privacy complexity because it interacts with smartphones, cloud profiles, smart home devices, lighting, heating, and garage access. The SC Module is more about customer acceptance, configurability, and avoiding distracting or annoying notifications.

The project starts on 1 June 2023, must be finished within one year, and must not exceed 1,000,000 euros.

## Suggested WBS Items

### Project Definition

Define scope, business goals, project goals, constraints, assumptions, stakeholders, and success criteria.

The out-of-scope part should be stated clearly: iGEO must not control safety critical driving behavior.

### Stakeholder Analysis

Create the stakeholder list, socio-diagram, power-interest matrix, and involvement actions, since several stakeholders are not openly resistant, but their statements show hidden concerns.

### Requirements Engineering

Collect and structure requirements for the hosting app, display, WH Module, SC Module, deployment process, security, privacy, and usability. 

### Safety, Security, and Privacy Concept

Define how IoMT software and hardware are separated from the GEO system.

Also define data protection rules for smartphone data, location data, cloud profiles, smart home credentials, and commercial preferences.

### Supplier Selection

Select the supplier using a small set of weighted criteria. Possible criteria: security maturity, IoT experience, process flexibility, budget fit, and collaboration quality.

Decision should not be based only on price because a failure in security or integration could become more expensive than the supplier fee.

### Hardware and Display Selection

Select the iGEO IoMT Hardware and Display.

For the display, usability research should be included because the display must fit into GEO cars and should not distract the driver.

### Hosting Application Development

Develop the hosting application as the platform for deploying, enabling, disabling, and managing modules.

This should include GUI, module lifecycle management, logging, compatibility checks, and access control.

### WH Module Development

Develop the Welcoming Home Module with smart home integration, passenger identification, room climatization, lighting, garage notification, and optional message sending.

This module probably has the highest complexity because it combines many external systems.

### SC Module Development

Develop the Smart Commercials Module with nearby offer notifications, filters, user preferences, and an option to disable the feature.

The main risk is not technical difficulty alone, but poor user acceptance if the feature feels like spam.

### Integration and Testing

Integrate hardware, display, hosting app, WH Module, SC Module, cloud services, and IoT devices.

Testing should include unit tests, integration tests, system tests, usability tests, security tests, privacy checks, and acceptance tests.

### Deployment and Release Process

Define how new modules are deployed, tested, enabled, disabled, updated, and rolled back.

This should become a repeatable process because iGEO is intended to support more modules later.

### Project Controlling

Track budget, schedule, supplier deliverables, risks, and stakeholder concerns throughout the project.

The strict budget limit makes continuous controlling necessary.

## Stakeholder Observations

| Stakeholder     | Role                             | Likely attitude         | Interest | Power  |
| --------------- | -------------------------------- | ----------------------- | -------- | ------ |
| Tom Wards       | CTO                              | Supportive but cautious | High     | High   |
| George Wein     | Project Manager                  | Strongly supportive     | High     | Medium |
| Jim Becker      | Executive Marketing              | Rather supportive       | Medium   | Medium | 
| Julia Andersen  | Finance and Controlling Director | Skeptical               | High     | High   | 
| Peter Scofield  | Executive IT                     | Skeptical               | High     | High   | 
| Anne Smith      | Lead IT Architect                | Hidden supportive       | High     | Medium | 
| Jane Wilson     | Sales Manager                    | Neutral                 | Medium   | Low    | 
| Jim Bucksley    | Developer                        | Supportive              | Medium   | Low    | 
| David Renegan   | Developer                        | Hidden resistant        | Medium   | Low    | 
| John Burton     | GEO Product Line Manager         | Supportive              | High     | High   | 
| Jonathan Newman | TEO Product Line Manager         | Hidden resistant        | Medium   | Medium |

## Supplier Decision Ideas

The supplier decision should balance innovation, safety, cost, and process fit.

FunIOT is attractive because it is cheaper, agile, open to changing requirements, and has some smart car experience. This fits the innovative and still unclear nature of iGEO.

ProfCar is attractive because it has more automotive experience, 5G technology, ISO certification, stronger warranties, and experience with process models. This fits the safety and security concerns of TOMI.

My current tendency would be to prefer ProfCar if security, reliability, and stakeholder trust are weighted highest. FunIOT would be more attractive if budget and flexibility are the main arguments.

A reasonable compromise idea would be to select ProfCar for hardware and display related work, but ask whether a smaller and more agile software scope could be handled separately. If the task requires choosing one supplier only, ProfCar seems safer for this specific automotive context.

Possible decision criteria:

- Security and safety maturity
- Smart car and IoT experience
- Process and quality maturity
- Cost and budget fit
- Flexibility and collaboration quality

## Estimation Assumptions

The project duration is fixed to one year.

The budget limit is fixed to 1,000,000 euros.

Supplier work includes hardware choice, display choice, and development of the hosting application with GUI.

Internal work still includes requirements, architecture decisions, stakeholder management, module development, integration, testing, acceptance, and project controlling.

The WH Module should receive a higher estimate than the SC Module because it has more external interfaces and more privacy sensitive data.

The hosting application should also receive a high estimate because it is the basis for module deployment and future extensibility.

For Planning Poker, a Fibonacci-like scale could be used because uncertainty increases with larger work packages.

For Use Case Points, the team should use the provided use case diagram and specifications. The main actors appear to be the iGEO Production Team, Driver, IoT Devices, and iGEO Cloud. The Driver should probably be classified as complex because the driver interacts through a graphical interface.

## Scheduling and Resource Planning Ideas

Should start with scope clarification, stakeholder analysis, requirements, and supplier selection.

Some activities can run in parallel after the first requirements baseline such as market analysis, display usability research, supplier evaluation, and security concept work can overlap.

The hosting application should start before the two modules because both modules depend on deployment and lifecycle functionality.

The WH Module and SC Module can be developed partly in parallel after the hosting interfaces are defined.

Integration and testing should not be pushed only to the end. Early integration tests are important because many risks come from external systems and supplier deliverables.

Likely critical path:

1. Scope and requirements clarification
2. Architecture and safety concept
3. Supplier selection
4. Hosting application development
5. WH Module development
6. Integration
7. System, security, and acceptance testing
8. Deployment preparation

## Open Questions

Which supplier work packages are fixed and which ones can still be negotiated?

Do we have to choose exactly one supplier for all outsourced tasks?

How many internal developers are available and how much time can they actually work on the project?

Which customer segment should iGEO target first?

How strict are the security and privacy acceptance criteria?

Do we need to include maintenance and after-sales support in the 1,000,000 euro budget?

Should the Use Case Point estimation include alternative flows fully or only where they add relevant transactions?
