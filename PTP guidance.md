# Test Plan preparation questionnaire:

The project test plan plays a vital role in deliverables quality and confidence. Hence it is essential to understand the system users’ requirements and the way it will be used in real time before writing a test plan. It is also important to know how it will be built by the project team and understand the bigger picture of the system. An ideal test plan is accomplished by applying basic principles of risk and cost-benefit analysis.

Finding answers for following questions from your PM/BA/Tech lead/Dev/Client ahead of the test plan write up may help you to understand the system better and come up with a bespoke test plan that will test the user/system requirements. Note: Not all these questions apply to every project, ignore the questions that are not relevant to your project and use this as a guidance to frame your questions.

## Who are the users?

- How will the system be used by the user(s) when in production?
- How many users and concurrent users?
- Where are users based (regionally)?
- Public user facing or internal facing application?

Benefits: Quality attributes testing relevant to the project can be planned. For e.g: Accessibility, Usability, Scalability, Performance, Locale testing using representative test data.

 
## What is being built?

- What is the overview (requirements) of the project?
- What are the user workflows? (e.g: 1. Add an admin user, then the admin user creates other roles. 2. Add data to the system. 3. Approval workflow)
- What will be the expected backend data volume in production?
- Is it a new development/re-development/enhancement project?
- How many different user roles? (Normal user, Superuser, Admins)

Benefits: Understand projects bigger picture, various roles involved, backend data volume, data migration if any, and plan the necessary data migration, security testing and other types of functional testing necessary. Be aware of the project complexity before estimating the testing effort.


## What is the technology stack?

- Where is it hosted? (Server layer – AWS/Azure/Google/Private/hybrid/dedicated server)
- What are the application layers? (Tools, frameworks, Services, WebAPI, GUI)
- What type of Architecture? (n-tier/microservice/client-server/Desktop/Grid)
- What type of database? (SQL/mongodb/…)

Benefits: Helps to identify the testing tools and frameworks that play well with the tech stack, various testing that need to be performed in different layers of the application and training needs for the testers/developers.

 
## Governance
- Any standards to be followed? (ISO 12207:2017 (GxP compliance), ISO 27001:9001, IEC 62304, Medical compliance, others)
- Any compliance to be met? (client specific legal requirements, GxP, GDPR, others) 

Benefits: Know the standards and compliance that need to be tailored into the projects testing activities from the beginning.
 

## Test environments expectations
- How many environments would be required? (Dev, Test, Preprod/QA and Prod)
- Should the application be browser/OS compatible? (Chrome/IE/Safari/FF or Windows/Linux/Mac OSx)
- Should the application be mobile device compatible (mobiles/tablets/touchscreens)

Benefits: Identify the compatibility testing (browser, device, and operating system) and deployment testing requirements in various environments.

 
## Test deliverables expectations
- Will unit test results be published in a dashboard and monitored?
- Will integration tests results be published and monitored?
- What documents should be included in delivery package? (Test plan, Test scripts, User guide, SMG)
- What reports should be included in the delivery package? (Traceability matrix, known defect list, verification and validation report, weekly/monthly/release reports)

Benefits: Understand the client’s expectation of test deliverables like test coverage, test completeness, test evidence and others, and plan resources accordingly.