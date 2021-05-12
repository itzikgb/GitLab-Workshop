---
title: "Configure the .gitlab-ci.yml file in the project"
chapter: true
weight: 2
---


# Configure the CI/CD in the project

In the root of the project you imported in **lab2** there is already **.gitlab-ci.yml** file that includes **build** and **test** **stages**, and **jobs** in each stage.

- We will add two additional **stages** and **jobs** to this configuration file,  **deploy** and **teardown**.:
 - **deploy**  will deploy the website to **surge**.
 - **teardown** will be a [manual](https://docs.gitlab.com/ee/ci/yaml/#whenmanual) job that will cleanup the new domain we create in the **deploy** job.

- Open the Web IDE.
![yml-1](/images/yml-1.png)
- Open the .gitlab-ci.yml file.
![yml-2](/images/yml-2.png)
- You will notice **stages** keyword, with **build** and **test** stages. Add **deploy** and **teardown** stages to it.

Your stages now should look like this:

{{< highlight html >}}
stages:
  - build
  - test
  - deploy
  - teardown
{{< /highlight >}}

- Scroll down, and create a deploy job in the deploy stage.
  - Job name: **deploy to surge**
  - stage: **deploy**
  - add two scripts:
    - `npm install --global surge`
    - `surge --project ./public --domain gitlab1-ws.surge.sh`

Your deploy job should look like this one:

{{< highlight html >}}
deploy to surge:
  stage: deploy
  script:
    - npm install --global surge
    - surge --project ./public --domain <unique-name>.surge.sh
{{< /highlight >}}

 - Below the **deploy** job, add another job, tear down the domain:
  - Job name: **teardown surge**
  - stage: **teardown**
  - add two scripts:
    - `npm install --global surge`
    - `surge teardown <unique-name>.surge.sh`
  - set this job as manual job (The pipeline will wait until someone will start it manually) using the **manual** keyword: `when: manual`

Your tear down job should look like this one:

{{< highlight html >}}
teardown surge:
  stage: teardown
  script:
    - npm install --global surge
    - surge teardown gitlab-ws.surge.sh
  when: manual
{{< /highlight >}}

{{% notice warning %}}
The script **surge --project ./public --domain <unique-name>.surge.sh** creates a unique domain in Surge. You need to make sure you modify the **unique-name** with a unique string so that the domain is available. For instance, if you modify **unique-name** with johnsmith, try to open **http://johnsmith.surge.sh** in the browser. If you get message **project not found** you can use it, if not try to find another string.
Once you have a unique domain, replace it in the appropriate place in **deploy to surge** and **teardown surge** jobs you created.  
{{% /notice  %}}
