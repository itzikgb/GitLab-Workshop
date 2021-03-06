---
title: "Summary"
chapter: true
weight: 9
---

# Summary

## In this workshop we learned:

- How to stand-up **GitLab Ultimate** in **AWS** via the **marketplace**.
- How to install GitLab **Runner** and register it to our GitLab project.
- How to create a new project and import a repository to it.
- How to configure GitLab CI/CD via the **.gitlab-ci.yml** file.
- How to use **GitLab DevOps platform** to **build**, **test** and **deploy** applications.


## Cleanup

We have create several resources in this workshop and we want to make sure that we remove them after we are done experimenting, so not incurs additional charges.

### S3 Bucket Removal
- In our AWS Console, Click **Services** -> **S3**.
- Select the bucket we created earlier, and click the **Delete** button on the upper right corner.
- You will get error message saying the bucket is not empty. Click on the link **empty bucket configuration** in that message.
- Confirm the bucket deletion by entering **permanently delete** in the input field.
- Then click **Empty**.
- Confirm that the bucket was delete by making sure its not on the bucket list.

### EC2 Machine Removal
- In our AWS Console, Click **Services** -> **EC2**.
- Select **Instances** from the left hand side, and select our Gitlab machine from the list.
- Click the **Instance State** button on the right hand side, and choose **Terminate instance**.
- Click **Terminate** in the dialog that opens, to confirm.

### Marketplace Subscription Removal
- In our AWS Console, Click **Services** -> **AWS Marketplace Subscriptions**.
- Under the **Gitlab Ultimate** subscription, click the **Manage** button.
- Click the **Actions** button on the right hand side and select **Cancel Subscription**.
- In the dialog that comes up, check the check box, and click **Yes, cancel subscription**.
