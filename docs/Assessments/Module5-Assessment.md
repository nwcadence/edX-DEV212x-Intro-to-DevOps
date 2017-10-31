Outline > Module 5: Monitoring and Learning > Assessments > Assessments 

# Assessments #

Answer the questions in this section to test your knowledge of the topics covered in this module.

You have a maximum of **two** attempts to answer each question correctly. After you submit your second answer, you will be unable to change it.

Your scores from the module assessments will be combined, and account for 55% of your overall grade for the course.

*If you have any questions about grading or specific questions, please post them in the course discussion forum. However, please avoid posting any information that will reveal answers to your fellow students. In the event of a dispute, the course staff's decision is final.*


## Choose One ##
*10.0 points possible (graded)*

<<display_name:Question 1; max_attempts:2; weight:10; rerandomize:always; showanswer:finished; show_reset_button:false>>

>>Which statement below most accurately describes Application Performance Monitoring (APM)?

( ) Dynamically scale servers to ensure there is enough RAM, CPU and disk space.    
( ) Performing load tests on an application.    
(x) Monitoring usage and performance metrics in production.   
( ) Measuring the time taken between code check-in and deployment. 

[explanation]   
Application Performance Monitoring (APM) is used, among other things, to monitor usage and performance metrics of an application in production.

Often, based on APM metrics a team will configure tools to autoscale servers (including RAM, CPU and disk space), however this is not a core part of APM. Instead, it is in response to APM measurements. Additionally, although performing load tests while measuring responses with an APM tool is often done, it is not the core purpose of APM. Finally, the time between code check-in and deployment is an excellent measure, however it is not related to APM.   
[explanation]

## Choose One ##
*10.0 points possible (graded)*

<<display_name:Question 2; max_attempts:2; weight:10; rerandomize:always; showanswer:finished; show_reset_button:false>>

>>What does the typical blue-green deployment process look like?

( ) Deploy directly to production visible to everyone immediately without testing    
(x) Two identical production slots, deploy to idle blue slot, direct traffic from live green slot to blue and then swap slots for full cutover  
( ) Deploy in rings of users gradually

[explanation]   
Deploying directly to production immediately without testing should generally be avoided. Deploying in rings of users gradually generally refers to canary releases. Two identical production slots is the correct answer. 

Blue-green deployments uses the concept of A/B Testing to manage deployments and traffic that gets directed through a load balancer. In blue-green deployments, there are two identical production environments. While one environment is currently being used as the live production slot (such as green), a new feature is deployed to the idle environment (blue) and a load balancer is used to direct some traffic from the live production slot (green) to the other slot (blue). Once ready to switch all users over, swap the slots for blue and green (making blue live and green idle). 
[explanation]


## Multiple Choice ##
*10.0 points possible (graded)*

<<display_name:Question 3; max_attempts:2; weight:10; rerandomize:always; showanswer:finished; show_reset_button:false>>

>>What are some examples of using feature flags? Select three answers.

[x] Kill switch for performance issues with a feature   
[x] Early access for new features for some users  
[x] Scalable rollouts  
[x] A/B Testing   

[explanation]   
Feature flags can be used for more than the four answers above, but some examples are using them as kill switches in case of performance problems, opt-in early access, phased deployments/rollouts, and A/B testing.
[explanation]

## Multiple Choice ##
*10.0 points possible (graded)*

<<display_name:Question 4; max_attempts:2; weight:10; rerandomize:always; showanswer:finished; show_reset_button:false>>

>>What are some metrics that you can gather from Application Performance Monitoring? Select all that apply.

[x] User satisfaction   
[x] Average response time
[x] Failed request rate 
[x] Request rate

[explanation]   
User satisfaction (formula combining various metrics to determine how satisfied a user will be upon going to your site), average response time, failed request rate, and request rate are all examples of metrics you can use with Application Performance Monitoring.
[explanation]