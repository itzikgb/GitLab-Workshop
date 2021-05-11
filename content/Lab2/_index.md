---
title: "Lab2 - Create GitLab project "
chapter: true
weight: 4
---

The following items are required for this workshop:

- AWS account and required IAM Roles - If you are at an AWS event, an account will be provided. Otherwise, go [here](https://portal.aws.amazon.com/billing/signup#/start) to create an AWS account.

- run untagged jobs
-
1. container setup
curl -fsSL https://get.docker.com -o get-docker.sh
 sudo sh get-docker.sh

 {{% notice tip %}} When creating additional sections or pages, copy the files and folders from another section, rename and edit.
 {{% /notice %}}

 {{% notice note %}} To make the creation of web page documentation easier, we utilize a tool called Hugo. You will write your documentation/instructions using markdown language and Hugo will create static html content that can be served via S3. Hugo additionally applies a theme so that the site will have an AWS look and feel plus add additional features to beautify and make content stand out.

 For more information about installing and using Hugo, visit https://gohugo.io/getting-started/installing/

 For more information about the learn theme used in Hugo, visit https://learn.netlify.com/en/ {{% /notice %}}