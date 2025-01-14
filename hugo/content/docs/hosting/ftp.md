---
title: FTP/SFTP
weight: "5"
publishdate: 2017-12-31T04:00:00.000+00:00
expirydate: 2030-01-01T04:00:00.000+00:00
date: 2017-12-31T04:00:00.000+00:00
layout: single
images:
- "/uploads/2018/01/OGimage-01-docs-3x.jpg"
menu:
  docs:
    parent: Hosting
    weight: 4

---
{{% tip "Disclaimer" %}} This deployment method is soon to be deprecated in favor of CI integrations. We recommend everyone no to use this method anymore.  
Please read our docs on [how to deploy with Circle CI](/blog/automate-deploy-w-circle-ci/) or try a service like [Netlify](https://netlify.com). {{% /tip %}}

## Overview

In order for Forestry to deploy your site via FTP/SFTP, you will need:

* A webserver with FTP/SFTP support
* A valid FTP username and password
* The port your FTP server uses

If you are hosting your static site on an FTP server, you should be aware that Forestry will delete all files from your destination directory before writing the new, updated files.

This could be problematic if you keep non-website related files in your FTP account. If you don't want Forestry to empty all of your files, consider setting up your site in an empty subdirectory.

## Choosing an FTP Method

Forestry provides four FTP connection methods:

### FTP

Basic, unsecured FTP. Usually served via port 21.

### FTP with TLS/SSL (FTPES)

FTP secured via TLS/SSL encryption. Usually served via port 990. Also known as FTP with explicit SSL.

FTP with TSL/SSL will fallback to basic FTP if a secured connection cannot be established.

### FTP with Implicit SSL (FTPS)

FTP secured via TLS/SSL encryption. Usually served via port 990. Also known as FTP with explicit SSL.

FTP with Implicit SSL will not connect if a secured connection cannot be established.

### SFTP (SSH FTP)

FTP secured with SSH. Usually served over port 22.

SFTP can optionally authenticate using an SSH keypair instead of a username & password combination.

{{% tip %}}
Whenever possible, use SFTP or FTP with Implicit SSL to ensure the best security for your webserver.
{{% /tip %}}

## Configuring Forestry

Once you have your FTP credentials and have chosen the correct FTP method for your webserver, navigate to the _Settings_ page of your site in Forestry, click the _Hosting_ tab, and set the _Connection_ option to your desired FTP connection type.

### FTP, FTPS, & FTPES

![](/uploads/2018/01/30.png)Next, enter your webservers host, username, and password.

Under _Advanced Options_, ensure that the _Port_ is the correct port.

If you created a new directory to deploy your site to, provide the relative path from your FTP user's home folder to the new directory in the _Directory_ field.

Finally, click _Save Settings_.

From here on, every time you save or publish a page Forestry will build your site and deploy to your webserver.

{{% warning %}}
When saving your hosting settings, Forestry will attempt to connect to your FTP server. If a connection cannot be established, an error will be displayed.
{{% /warning %}}

### SFTP

![](/uploads/2018/01/33.png)Next, enter your webservers host, username, and password. If you're using an SSH keypair to authenticate, upload your public key using the _SSH Key_ field.

Under _Advanced Options_, ensure that the _Port_ is the correct port.

If you created a new directory to deploy your site to, provide the relative path from your FTP users home folder to the new directory in the _Directory_ field.

From here on, every time you save or publish a page Forestry will build your site and deploy to your webserver.

{{% warning %}}
When saving your hosting settings, Forestry will attempt to connect to your SFTP server. If a connection cannot be established, an error will be displayed.
{{% /warning %}}