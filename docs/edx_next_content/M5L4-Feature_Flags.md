` Outline > Module 5: Monitoring and Learning > Feature Flags `

Feature flags (also called feature toggles) are often used in combination with A/B Testing as a practice in DevOps for gated functionality. The concept of feature flags is relatively simple: For certain features that should be made visible or invisible to users, wrap those features in conditionals to control those features' visibility in the release. Feature Flags can be used either natively through code or with other tools. A simple example of a feature flag is if you release a new page to your app that is accessible through a button on your main page, set a feature flag on that button so that it makes the button visible for some and invisible for others. By setting a flag on a new feature, this isolates the effect on the overall app and gives flexibility to turn on or off a flag independently.

Feature flags provide many benefits for DevOps practices beyond just monitoring and learning. Continuous Delivery and feature flags work hand-in-hand by enabling frequent deployments. For instance, if a feature that is being developed is not quite done before it's time to deploy, rather than pushing out the release date or the feature later, wrapping the feature around a feature flag enables the deployment to proceed as normal while still making that new feature invisible to users. From the perspective of monitoring and learning, feature flags can also act as kill switches if performance for a feature drops, an opt-in beta access to users for new features, phased deployment for a subset of users (canary releases), deployment to a subset of users with different production environments (blue-green deployments), and running A/B tests for performance.

## Feature Flags ##
![](http://i.imgur.com/mBKU7Le.jpg)<br>
**[Video link: https://youtu.be/F0jpKJIHUq0]**

