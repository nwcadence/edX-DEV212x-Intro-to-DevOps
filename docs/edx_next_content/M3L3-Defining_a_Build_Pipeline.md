`Outline > Module 3: Continuous Integration, Continuous Delivery, and Continuous Testing > Defining a Build Pipeline > Defining a Build Pipeline `

# Defining a Build Pipeline #

### Build Pipeline ###
A build pipeline is an automated system responsible for Continuous Integration.

- It builds code, runs unit tests, creates packages, etc.
- It's generally triggered by a code check-in, or on a schedule.

### Defining a build pipeline ###
Typically, a build pipeline is defined with the following components: 

- *Trigger*

   Typically, when code is checked into a branch or folder in source control, a build is automatically triggered.

   Builds are typically failed if anything in the pipeline fails, alerting the team for potential issues. Mechanisms such as gated check-in prevent code from being merged into the source repo if the build fails, ensuring that the main branch is always clean.

- *Tasks*

   The code is compiled and other tasks, such as client side minification, are executed.  

- *Unit Testing*

   Unit tests are performed to validate that the code is of high quality. 

- *Code Analysis*

   Static code analysis is performed and other quality metrics are gathered into a Technical Debt Management system, such as SonarQube.  

- *Packaging and Versioning*

   Assemblies are versioned and packaged so that it is ready for deployment. Sometimes the packages are uploaded to a package repository.


