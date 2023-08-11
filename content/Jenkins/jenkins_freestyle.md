+++
title = "Jenkins FreeStyle Job "
weight = 21
chapter = false
pre = "<b> 1.6 </b>"
+++

A Jenkins Freestyle job, also known as a FreeStyle project, is a type of build job in Jenkins that allows you to create and configure custom build and automation tasks without being restricted by a predefined pipeline structure. It's one of the simplest and most straightforward ways to define and execute build processes in Jenkins.

In a Freestyle job, you have the flexibility to configure build steps, triggers, source code management, build parameters, post-build actions, and more using the Jenkins web interface. You can mix and match various plugins and tools to tailor the job to your specific requirements.

## Use Case - Setup FreeStyle Job for URL Monitoring
- **Ref Code** - https://github.com/codvatechlabs/devops-bootcamp/blob/main/Jenkins/
- Frequency (1 hour)

1. **Creating a Freestyle Job:**
   - Log in to your Jenkins instance.
   - Click on "New Item" to create a new job.
   - Choose "Freestyle project" as the job type.
   - Enter a name for the job and configure other settings as needed.

2. **Configuring Build Steps:**
   - Under the "Build" section, add build steps that define what actions Jenkins should perform during the build process.
   - You can add shell commands, execute scripts, run tests, or perform any other custom tasks.

3. **Configuring Triggers:**
   - Under the "Build Triggers" section, you can specify conditions that trigger the job to run, such as code commits, scheduled builds, or manual triggers.

4. **Configuring Source Code Management:**
   - If your job requires source code from a version control system like Git, you can configure the appropriate SCM tool (e.g., Git, SVN) under the "Source Code Management" section.

5. **Configuring Build Parameters:**
   - You can define parameters that allow you to customize the build process. These parameters can be used as variables in your build steps.

6. **Configuring Post-Build Actions:**
   - After the build completes, you can configure actions to take, such as sending notifications, archiving artifacts, deploying to a server, etc.

7. **Saving and Running the Job:**
   - Once you've configured the job settings, click on "Save" to save the job configuration.
   - You can manually trigger the job by clicking "Build Now" or wait for the defined triggers to initiate the build.

A Jenkins Freestyle job is a suitable choice for simpler build and automation tasks where you don't require the complexity of a scripted or declarative pipeline. It's particularly useful for users who are new to Jenkins or are looking for a straightforward way to automate their build processes without delving into extensive scripting or pipeline definitions.


