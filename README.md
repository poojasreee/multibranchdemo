# multibranch-pipeline-demo
Jenkins Multibranch Pipeline Example Repo 

![jenkins](https://user-images.githubusercontent.com/107124664/185741750-c9526935-5c45-4b16-98d8-a0f44760dfcd.PNG)

Multi-branch pipeline supports PR based branch discovery. Meaning, branches get discovered automatically in the pipeline if someone raises a PR (pull request) from a branch. If you have this configuration enabled, builds will get triggered only if a PR is raised. So if you are looking for a PR based Jenkins build workflow, this is a great option.
So whenever the developer raises the PR from the feature branch to some other branch, the pipeline will run the unit testing and sonar analysis stages skipping the deployment stage.

Also, multi-branch pipelines are not limited to the continuous delivery of applications. You can use it to manage your infrastructure code as well.

Let’s say I want a Jenkins pipeline to build and deploy an application with the following conditions.

Development starts with a feature branch by developers committing code to the feature branch. 
Whenever a developer raises a PR from the feature branch to develop a branch, a Jenkins pipeline should trigger to run a unit test and static code analysis. 
After testing the code successfully in the feature branch, the developer merges the PR to the develop branch.
When the code is ready for release, developers raise a PR from the develop branch to the master. It should trigger a build pipeline that will run the unit test cases, code analysis, push artifact, and deploys it to dev/QA environments.

![multi](https://user-images.githubusercontent.com/107124664/185741867-ba42e382-7b4e-4bde-829e-ebeb7b1ea6d8.PNG)
![branch](https://user-images.githubusercontent.com/107124664/185741873-dc7edb3c-512a-4a20-879a-bf8de47f86e8.PNG)
