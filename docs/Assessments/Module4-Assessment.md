Outline > Module 4: Configuration and Release Management > Assessments > Assessments 

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


## Multiple Choice ##
*10.0 points possible (graded)*

<<display_name:Question 1; max_attempts:2; weight:10; rerandomize:always; showanswer:finished; show_reset_button:false>>

>>What are some of the benefits of describing your infrastructure and configuration as code? Select three.

[x] Facilitates automation   
[ ] Prevents developers from updating configuration   
[x] Provides environment consistency   
[x] Allows configuration to be version controlled   
[ ] Supports modification of configuration directly in production environments

[explanation]   
Infrastructure and configuration as code facilitates automation, provides environment consistency and allows configuration to be version controlled. 

Infrastructure and configuration as code does not prevent developers from updating configuration. That could be a policy in place in your organization, however, DevOps best practices would suggest a collaboration between developers and operations staff.  

Additionally, configuration as code generally prevents, or at least discourages, configuration changes to be made directly in production environments.  Instead, all changes should go through version control.   
[explanation]


## Multiple Choice ##
*10.0 points possible (graded)*

<<display_name:Question 2; max_attempts:2; weight:10; rerandomize:always; showanswer:finished; show_reset_button:false>>

>>Which two of the following statements best reflect how configuration management in a DevOps environment differs from traditional configuration management.

[x] Configuration management in a DevOps environment emphasizes encapsulation of configuration in code over formal documentation.   
[X] Configuration management in a DevOps environment is often less formal than traditional configuration management.   
[ ] Configuration management in a DevOps environment requires everything to be fully automated, including approval steps.   
[ ] Formal sign-offs are not permitted when doing configuration management in a DevOps environment.

[explanation]   
Having configuration as code is one of the core principles of DevOps. Although organizations implementing DevOps are free to establish formal change and configuration control protocols, these are not required to adopt DevOps.   
[explanation]


## Multiple Choice ##
*10.0 points possible (graded)*

<<display_name:Question 3; max_attempts:2; weight:10; rerandomize:always; showanswer:finished; show_reset_button:false>>

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

<<display_name:Question 4; max_attempts:2; weight:10; rerandomize:always; showanswer:finished; show_reset_button:false>>

>>Which of the following statements describes Release Management as it applies to DevOps? 

( ) Release Management means checking builds in to the source control system.    
( ) Release Management requires that a change control board is established to approve releases.   
( ) Release Management requires that all changes to code are documented.    
(x) Release Management enables automated releases to multiple environments with approvals. 

[explanation]   
Release Management generally describes managing releases into multiple environment with either automated or manual approval steps. 

Checking builds into source control, approval by a change control board, and documenting code changes may be good (or bad) practices for a given environment, but are not a required part of how release management is used in a DevOps environment.   
[explanation]


