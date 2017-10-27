Outline > Module 2: A Unified Process Between Dev and Ops > Assessments > Assessments 

# Assessments #

Answer the questions in this section to test your knowledge of the topics covered in this module.

You have a maximum of **two** attempts to answer each question correctly. After you submit your second answer, you will be unable to change it.

Your scores from the Assessments sections will be combined, and account for 55% of your overall grade for the course.

*If you have any questions about grading or specific questions, please post them in the course discussion forum. However, please avoid posting any information that will reveal answers to your fellow students. In the event of a dispute, the course staff's decision is final.*

## Multiple Choice ##

<<display_name:Question 1; max_attempts:2; weight:10; rerandomize:never; showanswer:finished; show_reset_button:false>>

>>Which three of the following principles are from Agile Software Development and also apply to DevOps? 

[x] Source Control   
[ ] Long release cadence   
[x] Automated testing   
[x] Continuous Integration   
[ ] Timesheets

[explanation]   
Long release cadence and Timesheets are not from Agile Software Development. They cannot be applied to DevOps either. The  other three options are correct.    
[explanation]


## Choose One ##

<<display_name:Question 2; max_attempts:2; weight:10; rerandomize:always; showanswer:finished; show_reset_button:false>>

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

<<display_name:Question 3; max_attempts:2; weight:10; rerandomize:always; showanswer:finished; show_reset_button:false>>

>>Which of the following statements is correct?

Source Control in DevOps:

( ) only applies to developers.   
( ) only applies to the development and QA environments, but not to production.   
(x) should be applied in every area and environment   
( ) applies to everyone except testers. 

[explanation]   
Source Control in DevOps should be applied in every area and environment. It is critical to the ability to roll back to prior versions and environments, and provides a concrete representation of code, configuration and environment.   
[explanation]


## Choose One ##

<<display_name:Question 4; max_attempts:2; weight:10; rerandomize:always; showanswer:finished; show_reset_button:false>>

You work in the operations team of an organization that delivers software. 

Your team is having difficulty tracking down the root cause of issues in your production environment. You spend a long time deploying bug fixes and deploy on a schedule once every 2 months. You do not usually have enough time to test all the changes being deployed. 

>>Which of the following recommendations aligns most closely with the Agile Manifesto, and should help you improve the turnaround time of detecting and fixing bugs?

( ) Deploy every 3 months and perform more testing.   
( ) Automate the deployments.   
( ) Deploy every 2 months, and focus on automating the testing.    
(x) Deploy every 3 weeks, reducing the amount of changes that are deployed. 

[explanation]   
Deploying every 3 weeks is a good step that aligns with one of the key Agile Manifesto principles - "Deliver working software frequently, from a couple of weeks to a couple of months, with a preference to the shorter timescale." 

Slowing the deployment to every 3 months will mean more changes in production and will likely increase the time to find and eliminate bugs.

Automating the deployment is an excellent idea, and is an important part of a DevOps pipeline. However, the Agile Manifesto does not mention or encourage automation directly. Thus this answer is incorrect.

Automating testing is also an excellent idea, and may reduce the time it takes to find and eliminate bugs. However, reducing the amount of code changes being pushed at each deployment will likely have a faster and more powerful impact on finding and fixing bugs. Also, the Agile Manifesto does not mention or  encourage automation directly. Thus this answer is incorrect.   
[explanation]
