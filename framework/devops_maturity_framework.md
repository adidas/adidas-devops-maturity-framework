# How to use the framework?
1. First step will be to do a self assessment of the current status of your Product Team for each 
one of the identified capabilities. 

1. Define the desired end-point at the end of the next improvement cycle, a cycle can be a month, 
a quarter, a semester ... every team can define their improvement cycles although a good start would
be to set quarterly targets to be able to define meaningful actions.

1. Identify the actions you will need to achieve the desired end-point. 

#### DEVELOPMENT 

----------
CAPABILITY | CRAWL | WALK | RUN  
---------- | ----- | ---- | ---
Use version control for all production artifacts | No version control | Source code or other assets under version control | All production artifacts under version control
Automate deployment processes | Manual deployment process | Partially automated deployment process | Fully automated deployment process
Implement test automation | Manual test script execution | Partially automated testing (unit or regression or performance tests) | Fully automated testing (unit and regression and performance tests)
Implement infrastructure automation | Manual deployment process | Partially automated deployment process. Provisioning done by the teams | Fully automated deployment (infrastructure-as-code). Platform Engineering provides base images
Support test data management | No test data management | Partially automated test data management (e.g. manually triggered import and export of test data) | Fully automated test data management incl. strategy (e.g. consumer data only in PROD)
Implement continuous delivery | No continuous delivery | Partially automated delivery pipeline (e.g. automated build, test process with manual deployment) | Fully automated pipeline (automated build, test, deployment across environments)
Include NFR’s in Definition of Done | No NFR's used | Ad-hoc NFR checks | Standardised NFR checklist as acceptance criteria for successful releases
Shift left on security | No security aspects considered during development cycle | Security aspects considered during development cycle but shifted towards release (not a priority) | Security aspects included during development cycle from the very start
Build for resilience | No resilience build into system | Design infrastructure and code for failure | Design infrastructure and code for failure with fully automated error recovery (self healing)
Enable team for troubleshooting | No control over development lifecycle (e.g. access to PROD) | Team has full control over development lifecycle (e.g. access to PROD), but no access to logs and tools relevant for troubleshooting | Team has full control over development lifecycle (e.g. access to PROD) and full access to logs and tools for troubleshooting 

#### PRODUCT & PROCESSES 

----------

CAPABILITY | CRAWL | WALK | RUN  
---------- | ----- | ---- | ---
Gather and implement customer feedback | No customer (internal or external) feedback gathered in development cycles | Customer feedback (internal or external) gathered on an ad-hoc basis | Customer feedback (internal or external) gathered after all releases
Work in small batches and deploy more frequently | Big work batch size and releases on a monthly basis or longer | Work batch size optimized for weekly releases, but deployment frequency not in sync with business requirements (e.g lead time) | Work batch size optimized for frequent releases and deployment frequency in sync with business requirements (e.g. lead time)
Have a lightweight change approval process | Change approval needed from multiple parties outside the team | Change approval needed within the team | 	No change approval needed or change approval process totally automated
Integrate application data into Big Data Platform | No application data transferred at all | Partial business relevant application data transferred to Big Data Platform or provided via API | All business relevant application data transferred to Big Data Platform

#### MANAGEMENT & MONITORING 

---------- 

CAPABILITY | CRAWL | WALK | RUN  
---------- | ----- | ---- | ---
Monitor application and infrastructure performance | No monitoring in place | Application or infrastructure performance monitored, but no alerting in place |  place	Application and infrastructure performance monitored and alerting in place for relevant KPI's
Monitor software delivery performance | No metrics monitored | Selected metrics monitored | All key metrics monitored
Limit Work in Progress | More than 10 features in progress | Less than 10 features in progress | Not more than 5 features in progress

#### CULTURE 

---------- 

CAPABILITY | CRAWL | WALK | RUN  
---------- | ----- | ---- | ---
Build it and run it | Product teams build the system, operations run (and fix) it. No end to end ownership for product lifecycle. Dev and Ops staffed in separated teams | Full ownership for product teams to build and run the system. No further L2 support by operations. Additional temporary resource for ramp up support | Full ownership for product teams to build and run the system. T-shape engineering profiles within the product teams to operate in full DevOps mode
Foster and enable team experimentation linked to business value | No time or resources dedicated for teams experimentations | Irregular time slots or events blocked for team experimentations (e.g. team hackerthon) | Regular time slots or events blocked for team experimentation (e.g. team hackathon every month or quarter)
Support and facilitate collaboration among teams | No collaboration with other teams although necessary for the product | Irregular exchange between team members and or other teams (e.g. CoP, meetings, lunch, coffee, sports) | Regular exchange between among team members and other teams (e.g. CoP, meetings, lunch, coffee, sports)

#### ARCHITECTURE 

---------- 

CAPABILITY | CRAWL | WALK | RUN  
---------- | ----- | ---- | ---
Use a loosely coupled architecture | Monolithic application with high level of interdependencies | Re-architecture in progress moving from a monolithic solution to a microservice based architecture| System have no or very few direct dependencies to other systems. And those dependencies are tight to open standards and not tight to technologies and frameworks (e.g. Java RPC)
Focus on independent deployability and testability | Dependent deployability and testability across teams | Some components can be deployed and tested independently but parts of the components still have dependencies across teams| Teams can deploy and test their systems independently
Use established Platform Engineering solutions as a default | Custom solutions used even though provided by Platform Engineering | All solution aligned with Platform Engineering, Solution and Domain Architecture, but exceptions were granted | All solutions aligned with Platform Engineering, Solution and Domain Architecture and no custom solutions used that are provided by Platform Engineering