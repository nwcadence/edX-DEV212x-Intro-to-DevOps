`Outline > Module 3: Continuous Integration, Continuous Delivery, and Continuous Testing > Continuous Integration, Continuous Delivery, and Continuous Testing > Continuous Integration and Continuous Delivery `

# Continuous Integration and Continuous Delivery #

### Continuous Integration ###
Continuous Integration (CI) is the practice of merging all developer working copies to a shared code line several times a day, and validating each integration with an automated build.

In practice, CI is often defined as having a build with unit tests that executes at every commit/ check-in to version control.

Continuous Integration (CI) provides many benefits, including: 

- Improving code quality based on rapid feedback
- Triggering for automated testing for every code change
- Better managing technical debt and conducting code analysis
- Reducing long, difficult and bug-inducing merges
- Increasing confidence in code long before production

### Continuous Delivery ###
Continuous Delivery is a software engineering approach in which teams produce software in short cycles, ensuring that software can be reliably released at any time.

- It aims to build, test and release software faster and more frequently.
- It reduces the cost, time, and risk of delivering changes by allowing for more incremental updates to production.

In practice, continuous delivery focuses on automated deployment pipeline. This may have one or more manual approval gates prior to reaching production.

Continuous delivery provides many benefits, including:

- It encourages Infrastructure as Code and Configuration as Code;
- It enables automated testing throughout the pipeline.
- It provides visibility and fast feedback cycles.
- It makes going to production a low stress activity.

### Continuous Delivery vs. Continuous Deployment ###
Continuous Deployment is generally defined as a Continuous Delivery pipeline with no manual gates between initial code check-in and production.

Feature flags are commonly used in both patterns, however, they are often necessary for Continuous Deployment. Feature flags ensure that code deployed to a production environment is not necessarily released to all end users.

## Continuous Integration and Continuous Delivery ##
![](http://i.imgur.com/mBKU7Le.jpg)<br>
**[Video link: https://youtu.be/vFRYaMAGL2o]**

For more information, you can see:   
Visual Studio Team Services: <a href="https://aka.ms/edx-dev212x-vsts" title="" target="_blank">https://aka.ms/edx-dev212x-vsts</a>


