Outline > Module 3: Continuous Integration, Continuous Delivery, and Continuous Testing > Assessments > Assessments 

# Assessments #

Answer the questions in this section to test your knowledge of the topics covered in this module.

You have a maximum of **two** attempts to answer each question correctly. After you submit your second answer, you will be unable to change it.

Your scores from the module assessments will be combined, and account for 55% of your overall grade for the course.

*If you have any questions about grading or specific questions, please post them in the course discussion forum. However, please avoid posting any information that will reveal answers to your fellow students. In the event of a dispute, the course staff's decision is final.*


## Multiple Choice ##
*10.0 points possible (graded)*

<<display_name:Question 1; max_attempts:2; weight:10; rerandomize:always; showanswer:finished; show_reset_button:false>>

>>Which two of the following statements describe the benefits of “Continuous Delivery (CD)”?

[X] CD ensures that code is tested frequently before being deployed to production.   
[ ] CD ensures that every code change is properly reviewed.   
[ ] CD ensures that developers code according to specifications.   
[x] CD ensures that source code is committed to the source repository before being deployed.   

[explanation]   
Continuous Delivery ensures code is tested frequently as builds and deployments (with associated tests) occur frequently. Additionally, since build and deployment is done from a source repository, both code and configuration need to be source controlled in order to impact a deployment environment. 

Continuous Delivery does not validate that every code change is properly reviewed, or that developers code to specifications.   
[explanation]


## Choose One ##
*10.0 points possible (graded)*

<<display_name:Question 2; max_attempts:2; weight:10; rerandomize:always; showanswer:finished; show_reset_button:false>>

>>Which statement below accurately describes "Continuous Integration (CI)"?

( ) Integration testing is performed daily.
( ) Code is deployed at least once a day.
(X) Every checkin triggers a build that builds and tests the code.
( ) Code review is performed for every checkin.

[explanation]
Continuous Integration implies the integration of all code lines into a single, merged branch on a very regular basis. In practice, it also generally includes a build and set of tests that run at every commit. 

Continuous Integration does not imply, however, that testing or deployment is done every day, or that a code review is performed at every checkin.
[explanation]


## Choose One ##
*10.0 points possible (graded)*

<<display_name:Question 3; max_attempts:2; weight:10; rerandomize:always; showanswer:finished; show_reset_button:false>>

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

<<display_name:Question 4; max_attempts:2; weight:10; rerandomize:always; showanswer:finished; show_reset_button:false>>

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

<<display_name:Question 5; max_attempts:2; weight:10; rerandomize:always; showanswer:finished; show_reset_button:false>>

>>Which of the following definitions best describes “Integration Testing”?

(X) Code is deployed and automated tests are run that span numerous systems, testing end to end functionality of a system.   
( ) Unit tests are automated as part of a Continuous Integration build.   
( ) Large amounts of data and users are simulated to test application performance.   
( ) Quality Assurance performs manual tests every day.

[explanation]   
Integration Testing ensures that tests span multiple systems to verify the application is working as expected. 

Unit tests, simulated users in a load test and manual testing are all important parts of a good quality assurance strategy. They may even participate in some integration tests. However, they are not part of the core definition of integration testing.   
[explanation]

