Outline > Final Exam > Final Exam > Final Exam 

# Final Exam #

Answer the questions in this Final Exam section to test your knowledge of the topics covered in this course.

You have only **one** attempt to answer each question correctly. After you submit your answer, you will be unable to change it.

Your score from the final exam accounts for 25% of your overall grade for the course.

*If you have any questions about grading or specific questions, please post them in the course discussion forum. However, please avoid posting any information that will reveal answers to your fellow students. In the event of a dispute, the course staff's decision is final.*


## Multiple Choice ##
*10.0 points possible (graded)*

<<display_name:Question 1; weight:10; max_attempts:1; rerandomize:always; showanswer:finished; show_reset_button:false>>

You are a software engineer in your organization. 

Your team uses traditional software development process and is interested in adopting DevOps.

>>Which three of the following practices should your organization start doing in order to embrace DevOps? 

[x] Try to minimize technical debt and keep your codebase as clean as possible.    
[x] Make releasing code into production one of the highest priorities for your team.     
[ ] Work on your branch separately and merge your code to the Master branch only right before production.    
[ ] Your operations team should manually deploy packages to the development and test environments.   
[x] Measure how customers are using your software and engage actively with customers to ensure that teams are building the right things.

[explanation]   
In order to embrace DevOps, you need to continuously integrate your code to the main branch throughout the process of software development. So it is incorrect to "work on your branch separately and merge your code to the Master branch only right before production."

Deployment automation and test automation are important practices for DevOps. So it is incorrect to say "Your operations team should manually deploy packages to the development and test environments."

The other three options are correct.    
[explanation]


## Multiple Choice ##
*10.0 points possible (graded)*

<<display_name:Question 2; weight:10; max_attempts:1; rerandomize:always; showanswer:finished; show_reset_button:false>>

>>Which two of the following statements about DevOps are correct? 

[X] The cultural practices of DevOps are predictive of organizational performance.    
[ ] DevOps only applies to the development and operations team in an organization.    
[ ] Your team needs to follow a DevOps standard or specification in order to achieve the best results.   
[x] In a DevOps practice, people, process, and tools all work together to enable continuous delivery of value to end users. 


[explanation]   
DevOps applies to all the team members, including developers, testers, operations, business analysts, etc., in an organization. So it is incorrect to say "DevOps only applies to the development and operations team in an organization."

There is no standard or specification of DevOps. So it is incorrect to say "Your team needs to follow a DevOps standard or specification in order to achieve the best results.". 

The other two options are correct.    
[explanation]


## Multiple Choice ##
*10.0 points possible (graded)*

<<display_name:Question 3; weight:10; max_attempts:1; rerandomize:always; showanswer:finished; show_reset_button:false>>

>>Which three of the following practices apply to DevOps?

[x] Continuous Integration   
[ ] Waterfall Requirements Analysis   
[x] Deployment Automation   
[ ] Budgeting   
[x] Test Automation


[explanation]   
Continuous Integration, Test Automation, and Deployment Automation are all part of DevOps as it is commonly implemented. Waterfall Requirements Analysis and Budgeting are not necessarily parts of DevOps, although they may be present in organizations that implement DevOps.    
[explanation]


## Multiple Choice ##
*10.0 points possible (graded)*

<<display_name:Question 4; weight:10; max_attempts:1; rerandomize:always; showanswer:finished; show_reset_button:false>>

Consider the following statement:

"Our team never configures servers manually. We configure every server via scripts. We checked scripts into source control and used them for automated deployment and testing and for detecting changes to environments."

>>Which of the following DevOps practice correctly describes what this team is doing? 

( ) Continuous Integration   
(x) Configuration as Code   
( ) Blue/Green Deployments   
( ) Automated Testing

[explanation]   
Configuration as Code correctly describes what the team is doing. Continuous Integration is the practice of ensuring that all code is merged regularly into a single branch, against which a build is generally run (including unit tests). Blue/Green Deployments is where a new version of the application or infrastructure is deployed alongside the existing production environment. At an appropriate time, some or all of the traffic is routed to the new environment. Automated Testing is used to quickly validate expected behaviors of an application, often during a deployment.    
[explanation]


## Choose One ##
*10.0 points possible (graded)*

<<display_name:Question 5; weight:10; max_attempts:1; rerandomize:never; showanswer:finished; show_reset_button:false>>

You work in the operations team of an organization that delivers software. 

Your team is having difficulty tracking down the root cause of issues in your production environment. You spend a long time deploying bug fixes and deploy on a schedule once every 2 months. You do not usually have enough time to test all the changes being deployed. 

>>Which of the following recommendations aligns most closely with the Agile Manifesto, and should help you improve the turnaround time of detecting and fixing bugs?

( ) Deploy every 3 months and perform more testing.   
( ) Automate the deployments.   
( ) Deploy every 2 months, and focus on automating the testing.    
(x) Deploy every 3 weeks, reducing the amount of changes that are deployed. 

[explanation]   
Deploying every 3 weeks is a good step that aligns with one of the key Agile Manifesto principles - "Deliver working software frequently, from a couple of weeks to a couple of months, with a preference to the shorter timescale." 

Slowing the deployment to every 3 months will mean more changes in production and will likely increase the time to find and eliminate bugs.

Automating the deployment is an excellent idea, and is an important part of a DevOps pipeline. However, the Agile Manifesto does not mention or encourage automation directly. Thus this answer is incorrect.

Automating testing is also an excellent idea, and may reduce the time it takes to find and eliminate bugs. However, reducing the amount of code changes being pushed at each deployment will likely have a faster and more powerful impact on finding and fixing bugs. Also, the Agile Manifesto does not mention or  encourage automation directly. Thus this answer is incorrect.   
[explanation]


## Choose One ##
*10.0 points possible (graded)*

<<display_name:Question 6; weight:10; max_attempts:1; rerandomize:always; showanswer:finished; show_reset_button:false>>

>>Which of the following definitions best describes “Integration Testing”?

(X) Code is deployed and automated tests are run that span numerous systems, testing end to end functionality of a system.   
( ) Unit tests are automated as part of a Continuous Integration build.   
( ) Large amounts of data and users are simulated to test application performance.   
( ) Quality Assurance performs manual tests every day.

[explanation]   
Integration Testing ensures that tests span multiple systems to verify the application is working as expected. 

Unit tests, simulated users in a load test and manual testing are all important parts of a good quality assurance strategy. They may even participate in some integration tests. However, they are not part of the core definition of integration testing.   
[explanation]


## Choose One ##
*10.0 points possible (graded)*

<<display_name:Question 7; weight:10; max_attempts:1; rerandomize:always; showanswer:finished; show_reset_button:false>>

>>Which three of the following are components of a Build Pipeline?

[X] Trigger - an event that initiates the build pipeline, for instance a code commit or schedule   
[X] Unit Tests - fast, automated tests that are run to validate code correctness   
[ ] Load Tests - tests simulating multiple users to ensure that the application performs expectedly   
[x] Packaging - application binaries and/or code is consolidated into a deployable package

[explanation]   
A Build Pipeline commonly includes triggers, a set of steps or tasks (sometime scripts), unit tests, code analysis, and packaging/versioning. These all occur prior to deployment into an environment. 

Load tests would not be part of a build pipeline, since load tests must be executed against an environment that contains the build.  Generally, load tests would be run in a release pipeline, instead. This is true even if the same tool is used to create both the build and release pipelines.   
[explanation]


## Choose One ##
*10.0 points possible (graded)*

<<display_name:Question 8; weight:10; max_attempts:1; rerandomize:always; showanswer:finished; show_reset_button:false>>

>>Which type of tests are typically run during a Continuous Integration (CI) build?

(X) Unit tests   
( ) Integration tests   
( ) Load tests   
( ) User Acceptance tests

[explanation]   
Unit tests are typically run during a Continuous Integration build.  

CI builds are generally part of the Build Pipeline, instead of the Deployment Pipeline. So integration, load and user acceptance tests cannot be run since they generally depend on a deployed application.   
[explanation]


## Multiple Choice ##
*10.0 points possible (graded)*

<<display_name:Question 9; weight:10; max_attempts:1; rerandomize:always; showanswer:finished; show_reset_button:false>>

>>Which two of the following statements describe the benefits of “Continuous Delivery (CD)”?

[X] CD ensures that code is tested frequently before being deployed to production.   
[ ] CD ensures that every code change is properly reviewed.   
[ ] CD ensures that developers code according to specifications.   
[x] CD ensures that source code is committed to the source repository before being deployed.

[explanation]   
Continuous Delivery ensures code is tested frequently as builds and deployments (with associated tests) occur frequently. Additionally, since build and deployment is done from a source repository, both code and configuration need to be source controlled in order to impact a deployment environment. 

Continuous Delivery does not validate that every code change is properly reviewed, or that developers code to specifications.   
[explanation]


## Multiple Choice ##
*10.0 points possible (graded)*

<<display_name:Question 10; weight:10; max_attempts:1; rerandomize:always; showanswer:finished; show_reset_button:false>>

>>Deployment pipelines have several characteristics. Select the three answers that best describe the characteristics of a deployment pipeline.

[x] Automates the deployment of code to environments   
[ ] Compiles the code and runs unit tests   
[x] Enforces automated or manual approval gates   
[x] Runs available automated tests against the deployed environment   
[ ] Runs a build every time new code is committed

[explanation]   
Deployment pipelines automate the deployment of code to environments, enforce automated or manual approval gates, and run available automated tests against the deployed environment. Not all of these characteristics need be present in early deployment pipelines, however, they are core characteristics to mature deployment pipelines. 

Deployment pipelines do not generally compile code and run unit tests. This is generally done by the Build pipeline.  In some tools, build and deployment is supported together, however, it is a good practice to compile once, and deploy the compiled and tested code from environment to environment.  Additionally, they generally do not run a build at every commit. That is common to a continuous integration environment, and is generally separate, at least conceptually, from a deployment pipeline.   
[explanation]


## Choose One ##
*10.0 points possible (graded)*

<<display_name:Question 11; weight:10; max_attempts:1; rerandomize:always; showanswer:finished; show_reset_button:false>>

>>Which of the following statements describes Release Management as it applies to DevOps?

( ) Release Management means checking builds in to the source control system.    
( ) Release Management requires that a change control board is established to approve releases.   
( ) Release Management requires that all changes to code are documented.    
(x) Release Management enables automated releases to multiple environments with approvals. 

[explanation]   
Release Management generally describes managing releases into multiple environment with either automated or manual approval steps. 

Checking builds into source control, approval by a change control board, and documenting code changes may be good (or bad) practices for a given environment, but are not a required part of how release management is used in a DevOps environment.   
[explanation]