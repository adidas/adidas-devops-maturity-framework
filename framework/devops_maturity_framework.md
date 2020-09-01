# How to use the framework?
1. The first step will be to do a self-assessment of the current status of your Product Team for each 
one of the identified capabilities. 

1. Define the desired end-point at the end of the next improvement cycle, a cycle can be a month, 
a quarter, a semester ... every team can define their improvement cycles although a good start would
be to set quarterly targets to be able to define meaningful actions.

1. Identify the actions you will need to achieve the desired end-point. 

#### DEVELOPMENT 

----------
CAPABILITY | CRAWL | WALK | RUN  
---------- | ----- | ---- | ---
Use version control for all production artifacts | No version control | Source code or other assets under version control | Source code or other assets under version control and all production artifacts versioned and stored in the corresponding artifact repository
Automate deployment processes | Manual deployment process | Partially automated deployment process | Fully automated deployment process
Implement test automation | Manual test script execution | Partially automated testing (unit or regression or performance tests) | Fully automated testing (unit and reliability (regression and performance tests)
Implement infrastructure automation | Manual deployment process | Partially automated deployment process. Provisioning is done by the teams | Fully automated deployment (infrastructure-as-code). Platform Engineering provides base images
Support test data management | No test data management | Partially automated test data management (e.g. manually triggered import and export of test data) | Fully automated test data management incl. strategy (e.g. consumer data only in PROD)
Implement continuous delivery | No continuous delivery | Partially automated delivery pipeline (e.g. automated build, test process with the manual deployment) | Fully automated pipeline (automated build, test, deployment across environments)
Include NFR’s in Definition of Done | No NFR's used | Ad-hoc NFR checks | Standardised NFR checklist as acceptance criteria for successful releases
Shift left on security | No security aspects considered during development cycle | Security aspects considered during development cycle but shifted towards release (not a priority) | Security aspects included during development cycle from the very start
Build for resilience | No resilience build into system | Design infrastructure and code for failure | Design infrastructure and code for failure with fully automated error recovery (self-healing)
Enable team for troubleshooting | No control over development lifecycle (e.g. access to PROD) | Team has full control over development lifecycle (e.g. access to PROD), but no access to logs and tools relevant for troubleshooting | Team has full control over development lifecycle (e.g. access to PROD) and full access to logs and tools for troubleshooting 
Feature handling | No feature branches for controlled releases | Feature branches are implemented for controlled  releases of distinct features | Feature branching and toggles are implemented to facilitate development, roll-out and roll-back (if needed) of usable features to production
Releases | Releases to all users and all sites / geographies in one go | Releases to subset of users or  sites or geographies | Gradual releases to subset of users in specific sites / geographies thereby limiting the blast raduis for potential issues

#### PRODUCT & PROCESSES 

----------

CAPABILITY | CRAWL | WALK | RUN  
---------- | ----- | ---- | ---
Gather and implement customer feedback | No customer (internal or external) feedback gathered in development cycles | Customer feedback (internal or external) gathered on an ad-hoc basis | Customer feedback (internal or external) gathered after all releases
Work in small batches and deploy more frequently | Big work batch size and releases on a monthly basis or longer | Work batch size optimized for weekly releases, but deployment frequency not in sync with business requirements (e.g lead time) | Work batch size optimized for frequent releases and deployment frequency in sync with business requirements (e.g. lead time)
Have a lightweight change approval process | Change approval needed from multiple parties outside the team | Change approval needed within the team | 	No change approval needed or change approval process totally automated
Integrate application data into Big Data Platform | No application data transferred at all | Partial business-relevant application data transferred to Big Data Platform or provided via API | All business-relevant application data transferred to Big Data Platform
SRE role and activities | No clear SRE role and responsibilty from Product team perspective | SRE tasks are defined and agreed from Execution (Operations, Automation, Hotfix) perspective | SRE tasks are defined for  Execution and Governance areas and agreed with all stakeholders (Business, Development)
Postmortems | No causal analysis done for all outages | All outage RCA conducted and tied to change / release | Blameless Postmortems are conducted for all outages
Resiliency / Chaos Engineering | No resiliency tests are conducted | Define environment dependencies (failure points) and execute resiliency tests to ensure no customer impact | Regular chaos (resiliency) exercise scheduled basis stead state / functionality change

#### MANAGEMENT & MONITORING 

---------- 

CAPABILITY | CRAWL | WALK | RUN  
---------- | ----- | ---- | ---
Monitor application and infrastructure performance | No monitoring in place | Application or infrastructure performance monitored but no alerting in place | Application and infrastructure performance is monitored; alerting in place for relevant KPI's
Monitor software delivery performance | No metrics monitored | Selected metrics monitored | All key metrics monitored
Limit Work in Progress | More than 10 features in progress | Less than 10 features in progress | Not more than 5 features in progress
Release governance | Product changes rolled out to production are not regulated for stability and reliability | Production changes are regulated basis stability and reliability benchmarks in test environments | Error Budget consumption regulates future releases to a product and act as gate to production changes
Resilience Monitoring | No KPI's defined for MTTx as per ITIL guidelines | Infra and Monitoring KPI's are defined as per ITIL guidelines for MTTx, availability, throughput, reported and deviations tracked to closure | Key monitoring signals form SLI, SLO (latency, throughput, error rate, saturation) are captured, reported and tied to product flow from business perspective

#### CULTURE 

---------- 

CAPABILITY | CRAWL | WALK | RUN  
---------- | ----- | ---- | ---
Build it and run it | Product teams build the system, operations run (and fix) it. No end to end ownership for product lifecycle. Dev and Ops staffed in separated teams | Full ownership for product teams to build and run the system supported by SRE. No L2 support needed | Full ownership for product teams to build and run the system. T-shape engineering profiles within the product teams to operate in full DevOps mode with enabled SRE in the product teams
Foster and enable team experimentation linked to business value | No time or resources dedicated for teams experimentations | Irregular time slots or events blocked for team experimentations (e.g. team hackathon) | Regular time slots or events blocked for team experimentation (e.g. team hackathon every month or quarter)
Support and facilitate collaboration among teams | No collaboration with other teams although necessary for the product | Irregular exchange between team members and or other teams (e.g. CoP, meetings, lunch, coffee, sports) | Regular exchange between among team members and other teams (e.g. CoP, meetings, lunch, coffee, sports)
Collaboration | No collaboration with Operations around product design from stability, reliability perspective | Product teams take design inputs (feedback) around stability, reliability from SRE experts. SRE experts are involved during testing phase (in development cycle) or post issues in production | Product architects collaborate regularly (from planning) with SRE experts to evolve the design of the product from performance, stability, reliability

#### ARCHITECTURE 

---------- 

CAPABILITY | CRAWL | WALK | RUN  
---------- | ----- | ---- | ---
Use a loosely coupled architecture | Monolithic application with a high level of interdependencies | Re-architecture in progress moving from a monolithic solution to a microservice-based architecture| System has no or very few direct dependencies to other systems. And those dependencies are tied to open standards and not tied to technologies and frameworks (e.g. Java RPC)
Focus on independent deployability and testability | Dependent deployability and testability across teams | Some components can be deployed and tested independently but parts of the components still have dependencies across teams| Teams can deploy and test their systems independently
Use established Platform Engineering solutions as a default | Custom solutions used even though provided by Platform Engineering | All solution aligned with Platform Engineering, Solution and Domain Architecture, but exceptions were granted | All solutions aligned with Platform Engineering, Solution and Domain Architecture and no custom solutions used that are provided by Platform Engineering
