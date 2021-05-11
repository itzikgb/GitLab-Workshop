---
title: "Install and register Runner"
chapter: true
weight: 6
---

In this lab we will install Docker engine as all jobs will run inside a container images. than install GitLab runner, configure it and register it to work with our project.

- Install Docker engine   
  - Go to your Instance summary and click **Connect** in order to open the console.
  - Click Connect.
  - Install Container by running this script `curl -fsSL https://get.docker.com -o get-docker.sh
   sudo sh get-docker.sh`
  - Setup Runners
      - Download the binaries for Linux x86 `sudo curl -L --output /usr/local/bin/gitlab-runner "https://gitlab-runner-downloads.s3.amazonaws.com/latest/binaries/gitlab-runner-linux-386`
      - Give it permissions to execute: `sudo chmod +x /usr/local/bin/gitlab-runner`
      - Create a GitLab CI user: `sudo useradd --comment 'GitLab Runner' --create-home gitlab-runner --shell /bin/bash`
      - Install and run as service: `sudo gitlab-runner install --user=gitlab-runner --working-directory=/home/gitlab-runner
sudo gitlab-runner start`
 - Register the Runner
  - Run this command: `sudo gitlab-runner register`.
  - You will be prompt to enter URL.
  - Open your GitLab instance, under CI/CD settings:
    - Click Settings->CI/CD.
    - Expand **Runners**.
    - Copy the URL under specific runner.
  - Pater the URL in the console
  - You will be prompt to enter registration token, copy it from the Runner settings, and paste it in the console,
  - Enter Description for the runner: type **GitLab workshop**.
  - Add a tag to this runner, for example type **Linux**
  - Enter executor, type **docker**.
  - Enter the default Docker image, type **ruby:2.6**.
  - You will get this message **Runner registered successfully. Feel free to start it, but if it's running already the config should be automatically reloaded! **. 





   {{% notice warning %}}
   It is not recommended best practice to install Runners on the same machine when the server installed for security and performance reasons, but only for the sake of simplicity, in this workshop we will install it on the same machine.
   {{% /notice  %}}

- run untagged jobs
-
1. container setup
curl -fsSL https://get.docker.com -o get-docker.sh
 sudo sh get-docker.sh




 {{% notice warning %}}
 It is not recommended best practice to install Runners on the same machine when the server installed for security and performance reasons, but only for the sake of simplicity, in this workshop we will install it on the same machine.
 {{% /notice  %}}

{{% notice note %}}
For more information about running jobs in docker containers, visit https://docs.gitlab.com/ee/ci/docker/using_docker_images.html#run-your-cicd-jobs-in-docker-containers
{{% /notice  %}}

 {{% notice tip %}} GitLab Runner is open-source and written in Go. It can be run as a single binary; no language-specific requirements are needed. You can install GitLab Runner on several different supported operating systems. Other operating systems may also work, as long as you can compile a Go binary on them.
 {{% /notice %}}
