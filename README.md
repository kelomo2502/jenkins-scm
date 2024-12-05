# Jenkins-freestyle-project

This project explains  how to configure, customize, and automate your software development pipelines using the versatile and user-friendly features of Jenkins.

## Jenkins job

In Jenkins, a job is a unit of work or a task that can be executed by the Jenkins automation server.
A Jenkins job represents a specific task or set of tasks that needs to be performed as part of a build or deployment process. Jobs in Jenkins are created to automate the execution of various steps such as compiling code, running tests, packaging applications, and deploying them to servers. Each Jenkins job is configured with a series of build steps, post-build actions, and other settings that define how the job should be executed.

## Creating a freestyle project

Let's create our first build job

1. from the dashboard menu on the left, click on new menu
![New item](/images/new-item.png)
2. Connecting to Jenkins to source code management
3. Create a new github repository called jenkins-scm with a README.md file
4. Connect Jenkins to jenkins-scm  repository by pasting the repository url in the area selected below. Make sure your current branch is main
![Repo url](/images/repo-url.png)
5. Save configuration and run "build now" to connect jenkins to our repository
![Build now ](/images/build.png)
We have successfully connected jenkins with our github repository (jenkins-scm)

## Configure build trigger

As engineers, we need to be able to automate things and make our work easier in every possible way. We have connected jenkins , but we cannot run a new build with clicking on build now. To eliminate this, we need to confiure a build trigger to our jenkins job. With this, jenkins will run a new build anytime a change is made to our github repository

- Click "Configure" your job and add this configurations
![Configure](/images/configure.png)
- Click on build trigger to configure triggering the job from GitHub webhook
![Build trigger](/images/imagebuild-trigger.png)
- Create a github webhook using jenkins ip address and port
