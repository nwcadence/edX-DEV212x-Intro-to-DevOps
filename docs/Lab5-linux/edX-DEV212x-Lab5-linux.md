# EdX DEV212x Intro to DevOps - LAB 5 Linux #
This is the Linux Hands on Lab for module 5 of the Intro to DevOps course.

> **NOTE:** VSTS is a rapidly evolving service, with releases coming every 3 weeks. Some of the images and instructions in this lab may change slightly so that they look different when you go through this lab. If you take a deep breath and think of the goal you're trying to achieve, you should be able to work out where to go even if the user interface does not exactly match the LAB.

## LAB 5 - A/B Testing, Feedback & Monitoring with Visual Studio Team Services ##
Once you have completed the videos and other course material for Module 5, you can continue with this lab.

In this lab you have an application called MyShuttle2, committed to a Git repo
in Visual Studio Team Services (VSTS) and a Continuous Integration build that builds the app, runs
unit tests and publishes a container image to a container registry whenever code is pushed to the master branch. Please refer to the
[LAB 3](../Lab3/EdX212x-Lab3-linux.md) in order to see how the CI build was set up.

In [LAB 4](../Lab4/EdX212x-Lab4-linux.md) the Release Management section built a continuous delivery pipeline triggering releases on successful builds.  The stages of deployment demonstrated gating, approvals, code promotion, and running the containers on the Azure Linux VM.

At this point you're ready to deploy your container somewhere that customers can hit the site. Once deployed, you'll want to profile the application to understand you customer's needs as well as the effectiveness of the site. Application Insights can provides just this sort of information. Now you can deploy new versions of the application to a staging slot and divert a percentage of traffic to the slot. Then you can monitor the slot and the production site to determine if the new version is "better" than the current production version - where "better" may mean better performance, more clicks, better conversion rates or anything else that you may need to experiment with.

## Pre-requisites:

* You have completed [LAB 1](../Lab1/edX-DEV212x-Lab1-linux.md)
* You have completed [LAB 3](../Lab3/edX-DEV212x-Lab3-linux.md)
* You have completed [LAB 4](../Lab4/edX-DEV212x-Lab4-linux.md)

* An active Azure account to host the MyShuttle Website as a Web App for Containers

## Tasks Overview:

1. See how the site and its slot, database and Application Insights are conifgured in the ARM Templates

1. Modify the Release Definition to deploy the MyShuttle container to Azure, including deploying to a staging slot and diverting a percentage of traffic to the slot

1. Modify code and see different versions of the site

1. Review in AppInsights to see results


## Task 1: ##

Before you deploy the application to Azure, we will take a look at the Azure Resource Manager (ARM) template to understand how which resources are going to be deployed and how they are connected.

1. Navigate in your VSTS account to the Code hub. Click on the MyShuttle2 repo and browse the Files to MyShuttle2/env/azuredeploy.json.

    ![](media/azuredeploy.png)

    There are several resources that are configured in this template:
    * The `Microsoft.Web/sites` resource is the Web App for Containers resource. Notice how the `appSettings` include keys for the Docker Registry Container as well as the name of the image to run
    * The site also deploys a `slots` resource which creates a staging slot for the site. Notice how the slot has its own `appSettings` too
    * There are two  `Microsoft.Insights/components` resources (these are Application Insights resources) - one for the production slot (the main site) and one for the staging slot
    * The site and the slot both have has a setting called `APPLICATION_INSIGHTS_IKEY` which looks up the corresponding `Microsoft.Insights/components` in order to set the key correctly for the Application Insights component that runs in the Java application inside the container.
    * The site is deployed onto an application plan (the `Microsoft.Web/serverfarms` resource) which has its `kind` attribute set to `linux` which tells Azure that the web app(s) on this plan are going to be containers.
    * There is a `Microsoft.DBforMySQL/servers` which deploys a MySQL resource to host the database

## Task 2: ##

At this point we have two container images: `web` which contains the web app and runs it on Tomcat and `db` which is a mysql container. We're going to configure the application to deploy the web app container image to Azure Web Apps for Containers and rather than deploy another container for the database we'll create an Azure MySql database. The ARM template we looked at in Task 1 specify how Azure is to deploy these resources. In this task you'll configure a Release Definition in VSTS that will deploy the resources to Azure using the ARM template, deploy the database schema and some test data to the MySql database and configure the correct container image onto each slot in the web app. You'll also configure a Traffic Manager rule that will divert a percentage of the traffic to the staging slot - this is how to perform A/B testing.

1. Log into your VSTS account and browse to the Release hub. Open the Release Definition you created in Lab 4 (it should be called `MyShuttle2 - CD` or something similar). It should have a single environment called `AzureVM` that runs the containers from the triggering build in the Azure VM.

1. Click the `+ Add` button on the Artifacts block to add a new artifact. Set the properties as follows:

    | Parameter | Value | Notes |
    | --------------- | ---------------------------- | ----------------------------------------------------------- |
    | Source type | Git | We want to clone the source code - specifically for the deployment scripts and templates | 
    | Project | The name of your Team Project | The team project that contains the repo to clone | 
    | Source (repository) | `MyShuttle2` | The name of the repo to clone |
    | Default branch | `master` | The branch to clone |
    | Shallow fetch depth | 1 | We just need the latest commit in the repo - not the entire history |
    | Source alia | `Source` | The folder name that the repo will be cloned into |

    ![](media/add-artifact.png)

1. Add a new environment to the definition. This environment represents deployments to the staging slot (which you'll name `blue`).

    1. Click the `+ Add` button on the Environments block and add a new environment. Click the "Empty process" link to create an empty environment.

        ![](media/add-environment.png)

    1. Change the name of the environment to `PROD-blue`. 

        ![](media/name-environment.png)

    1. Click on the Pre-deployment conditions block of the new environment. Make sure that the trigger is set to deploy automatically after a successful deployment to the `AzureVM` environment:

        ![](media/configure-predeploy-conditions.png)

    1. Click on "Pre-deployment approvers" and set yourself as a predeployment approver:

        ![](media/configure-predeploy-approval.png)

1. Configure the tasks for the `PROD-blue` environment.



1. Click on the `PROD-blue` environment to select it. Then click on the `+ Add` button to add another environment. Use the "Empty process" link and set the name of the environment to `PROD-success`, 

## Task 3: ##

## Task 4: ##