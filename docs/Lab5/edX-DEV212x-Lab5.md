# EdX DEV212x Intro to DevOps - LAB 5 #
This is the Hands on Lab for module 5 of the Intro to DevOps course.

> **NOTE:** VSTS is a rapidly evolving service, with releases coming every 3 weeks. Some of the images and instructions in this lab may change slightly so that they look different when you go through this lab. If you take a deep breath and think of the goal you're trying to achieve, you should be able to work out where to go even if the user interface does not exactly match the LAB.

## LAB 5 - Feedback & Monitoring with Visual Studio Team Services ##
Once you have completed the videos and other course material for Module 5, you can continue with this lab.

In this lab you have an application called PartsUnlimited, committed to a Git repo
in Visual Studio Team Services (VSTS) and a Continuous Integration build that builds the app and
runs unit tests whenever code is pushed to the master branch. Please refer to the
[LAB 3](../Lab3/EdX212x-Lab3.md) in order to see how the CI build was set up.

In [LAB 4](../Lab4/EdX212x-Lab4.md) the Release Management section built a continuous delivery pipeline triggering releases on successful builds.  The stages of development demonstrated gating, approvals, code promotion, and production deployment.

Now that the code is in the wild, it would be nice to profile your visitors to understand their website needs and effectiveness of the site.  App insights is deployed with the ARM template and provides just the information you need.

## Pre-requisites:

* You have completed [LAB 1](../Lab1/edX-DEV212x-Lab1.md)
* You have completed [LAB 3](../Lab3/edX-DEV212x-Lab3.md)
* You have completed [LAB 4](../Lab4/edX-DEV212x-Lab4.md)

* An active Azure account to host the PartsUnlimited Website as a Web App

## Tasks Overview:

1. See how Application Insights is setup in ARM Templates

1. View Data in Azure Portal

1. Query AppInsights and generate pie chart.

1. Create a new environment for A/B testing and direct traffic to the new slot

1. Modify code and see different versions of the site.

1. Review in AppInsights to see results


## Task 1: ##

* Navigate in your VSTS account to Files > PartsUnlimited > src > env > PartsUnlimitedEnv > Templates > AppInsights.json

![](media/app_insight_template.png)

Note the output of the InstrumentationKey which is needed by the Web App.

Clicking on the Website.json file shows where the AppInsight key is integrated with the website

![](media/app_insight_web_key.png)

App Insights is already setup on the PartsUnlimited website, so please generate some data by clicking on the production website (from [LAB 4](../Lab4/edX-DEV212x-Lab4.md)).


## Task 2: ##

Let's go look at the data from the clicks.

* Log into the Azure Portal

If the dashboard doesn't have a link to your newly created Web App, Navigate to the App Insights Panel via Resource Groups > YourWebsiteName-DevInsights

![](media/open_app_insights.png)


## Task 3: ##

* Navigate to the AppInsight servcie for the production website.

Review the metrics available in App Insights and then open the Analytics tab.

![](media/app_insight_overview.png)

* Open a new query by clicking on the **+**.  This will help sort through the data.

![](media/app_insight_newquery.png)





![](media/azure_web_app.png)

* After selecting the App Service scroll down in the left blade until the **Development Tools** section appears.  Select the **Testing in Production** option.

![](media/azure_testing_prod.png)

* In the Testing in Production window select from the dropdown of defined slots.  Add or change the percentage of traffic allocated to each slot.  Higher percentage will make this easier to verify, but typically a feature would start with a low percentage and increase until it made sense to switch the staging and production.  The balance of traffic will be sent to the production slot.  Click save to activate the changes.

![](media/testprod_split.png)
