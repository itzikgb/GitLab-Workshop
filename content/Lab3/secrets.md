---
title: "Save the secrets in GitLab CI/CD variables"
chapter: true
weight: 8
---

Update the Surge account details in GitLab CI/CD variables

- In your project in GitLab, open the CI/CD settings.
  ![runner-3](/images/runner-3.png)
- Expand Variables.
  ![secret-1](/images/secret-1.png)
- Add a new variable.
  ![secret-2](/images/secret-2.png)
- Under **key** type `SURGE_LOGIN`, under **value** type the **email** you entered when created Surge account. Click **Add variable**.
- Add another variable, click **Add variable** , under **key** type `SURGE_TOKEN`, under **value** type the token you saved earlier. Click **Add Variable**.
  ![secret-3](/images/secret-3.png)
