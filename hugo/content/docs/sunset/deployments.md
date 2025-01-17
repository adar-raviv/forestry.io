---
title: FTP Deployments
description: Forestry is removing FTP deployments on September 2019 1st.
date: 2019-06-30T19:00:00-03:00
publishdate: 2019-06-30T19:00:00-03:00
expirydate: 2030-07-13T19:00:00-03:00
authors:
- team forestry
menu:
  sunset:
    weight: 1
    parent: Sunset Notices
---
Starting today, we're removing support for (S)FTP deployment. All sites newly created in Forestry are already not able to deploy through FTP.

Why the change? Because it involves a lot of machinery on our end to ensure a build pipeline for you and given only a few percents of our users are effectively using this option, we think it's better for us to focus on our core features like content modeling and editing. Plus you will benefit from better services and features from companies that do deployment for a living.   
Even if the current option has served you well until now, we think it's a smart move for everyone.

We strongly recommend to change your current deployment option with best-of-breeds services like [Netlify](https://netlify.com) or [Circle CI](https://circleci.com).

Just set Forestry to commit to your repository only. We plan to ease the process by adding direct integrations of services in your site deployment settings.

**We will be sunsetting FTP deployments on September 1, 2019.**

[Read how to automate your deployments with Circle CI](https://forestry.io/blog/automate-deploy-w-circle-ci/).