# example-java-sb-maven
[![Build Status](https://jenkins.dxc.com/buildStatus/icon?job=AET%2Fexample-java-sb-maven%2Fmaster)](https://jenkins.dxc.com/view/All%20jobs/job/AET/job/example-java-sb-maven/job/master/)

Example CI Pipeline for Java Springboot App packaged with Maven

Chagne Text

Pipeline Stages Featured:
- Unit Testing:  JUnit
- Code Coverage: JaCoCo
- Static Code Analysis:  SonarQube
- Open Source Licenses:  mvn site
- Open Source Vulnerabilty Scanner: OWASP Dependacy Check 
- Save Jenkins Workspace:  archive unit testing reports 
- Package and Publish in Artifactory:  Maven Package

## Prerequisites
A project team must have:
- [Github.dxc.com](https://github.dxc.com/pages/Platform-DXC/devcloud-docs/github/) project repo and an admin level team member to access and set project specific settings.
- [Jenkins.dxc.com](https://github.dxc.com/pages/Platform-DXC/devcloud-docs/jenkins/) integrated with your github project and access to set credentials.
- [artifactory.dxc.com](https://github.dxc.com/pages/Platform-DXC/devcloud-docs/artifactory/) Application-level package repo created for the Organization/Project and a r/w Service Account name and password ready to use.

## Options
- MS Teams...

## Steps to run the pipeline
1) Fork the repository into your organization.  

if your organization is not integrated with **jenkins.dxc.com** complete the onboarding following the instructions located at: https://github.dxc.com/pages/Platform-DXC/devcloud-docs/jenkins/#add-your-userorganization

2) From jenkins.dxc.com, click on your organizations repository
- Click on **Credentials** on the left menu.  ( Note - you will need to be assigned as a Github administrator for your Organization )
- Click on <YOUR_ORGANIZATION/<REPO_NAME>
- Click on Global credentials (unrestricted)
- Click on Add Credentials on the left menu
- Select Username and Password for Kind field
- Type your Artifactory user as UserName
- Type your Artifactory password.
- Type **central** as ID
- Click OK

3) Change your project's Maven **pom.xml** file to add the Artifactory binary repository.

```
   <repository>
        <id>central</id>
        <name>DevCloudArtifactory-releases</name>
        <url>https://artifactory.dxc.com/artifactory/<YOUR_ORG_MAVEN_REPO_NAME></url>
    </repository>
    
   ```

4) Commit Your changes    
   
5) You will notice in jenkins.dxc.com a job running under <YOUR_ORGANIZATION/<REPO_NAME> on master branch.

6) Finally, When the job has finished, you will see in a Maven package has been added.  

## POST

## If you are having trouble getting the pipeline to work

1. Watch the video walk-though of the pipeline
2. Open an issue here: [link](https://github.dxc.com/AET/Pipeline-Library/issues).
3. Search [github.dxc.com](https://github.dxc.com/)
4. Submit a question on [DXC Workplace](https://dxc.workplace.com/)


## Steps to get the example-java-springboot-maven application working on your desktop IDE 

1. Follow the instructions present in the below page to set up github account locally 
[https://docs.github.com/en/free-pro-team@latest/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent#generating-a-new-ssh-key] 
2. ...
3. ....


## Contribute 

If you want to make changes to this example, please fork the repository and change it in your own private fork!  If you do make local changes we'd love a Pull Request back though! We love contributions and pull requests!
